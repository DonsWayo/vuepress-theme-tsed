<template>
  <nav class="nav-links"
       v-if="userLinks.length || repoLink">
    <!-- user links -->
    <div class="nav-item"
         v-for="item in userLinks"
         :key="item.link">

      <DropdownLink v-if="item.type === 'links'"
                    :item="item"/>

      <NavLink v-else :href="item.link" v-html="item.text" :title="item.title"></NavLink>
    </div>

  </nav>
</template>

<script>
  import { resolveNavLinkItem } from '../../utils'
  import DropdownLink from '../dropdown/DropdownLink.vue'
  import NavLink from './NavLink.vue'

  export default {
    name: 'NavLinks',
    components: { NavLink, DropdownLink },

    computed: {
      userNav () {
        return this.$themeLocaleConfig.nav || this.$site.themeConfig.nav || []
      },

      nav () {
        const { locales } = this.$site
        if (locales && Object.keys(locales).length > 1) {
          const currentLink = this.$page.path
          const routes = this.$router.options.routes
          const themeLocales = this.$site.themeConfig.locales || {}
          const languageDropdown = {
            text: this.$themeLocaleConfig.selectText || 'Languages',
            items: Object.keys(locales).map(path => {
              const locale = locales[path]
              const text = themeLocales[path] && themeLocales[path].label || locale.lang
              let link
              // Stay on the current page
              if (locale.lang === this.$lang) {
                link = currentLink
              } else {
                // Try to stay on the same page
                link = currentLink.replace(this.$localeConfig.path, path)
                // fallback to homepage
                if (!routes.some(route => route.path === link)) {
                  link = path
                }
              }
              return { text, link }
            })
          }
          return [...this.userNav, languageDropdown]
        }
        return this.userNav
      },

      userLinks () {
        return (this.nav || []).map(link => {
          return Object.assign(resolveNavLinkItem(link), {
            items: (link.items || []).map(resolveNavLinkItem)
          })
        })
      }
    }
  }
</script>

<style lang="scss" src="./NavLinks.scss"></style>
