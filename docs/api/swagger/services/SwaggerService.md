---
sidebar: auto
---
# SwaggerService <Badge text="Service" type="service"/>
<!-- Summary -->
<section class="symbol-info"><table class="is-full-width"><tbody><tr><th>Module</th><td><div class="lang-typescript"><span class="token keyword">import</span> { SwaggerService }&nbsp;<span class="token keyword">from</span>&nbsp;<span class="token string">"@tsed/swagger"</span></div></td></tr><tr><th>Source</th><td><a href="https://github.com/Romakita/ts-express-decorators/blob/v4.30.0/src//swagger/services/SwaggerService.ts#L0-L0">/swagger/services/SwaggerService.ts</a></td></tr></tbody></table></section>

<!-- Overview -->
## Overview


::: v-pre
<pre><code class="typescript-lang "><span class="token keyword">class</span> SwaggerService <span class="token punctuation">{</span>
    <span class="token keyword">constructor</span><span class="token punctuation">(</span>controllerService<span class="token punctuation">:</span> <a href="#api/common/mvc/controllerservice"><span class="token">ControllerService</span></a><span class="token punctuation">,</span> serverSettingsService<span class="token punctuation">:</span> <a href="#api/common/config/serversettingsservice"><span class="token">ServerSettingsService</span></a><span class="token punctuation">,</span> expressApplication<span class="token punctuation">:</span> Express.Application<span class="token punctuation">)</span><span class="token punctuation">;</span>
    $<span class="token function">afterRoutesInit</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span> <span class="token keyword">void</span><span class="token punctuation">;</span>
    $<span class="token function">onServerReady</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span> <span class="token keyword">void</span><span class="token punctuation">;</span>
    <span class="token function">getOpenAPISpec</span><span class="token punctuation">(</span>conf<span class="token punctuation">:</span> <a href="#api/swagger/iswaggersettings"><span class="token">ISwaggerSettings</span></a><span class="token punctuation">)</span><span class="token punctuation">:</span> Spec<span class="token punctuation">;</span>
    <span class="token function">getDefaultSpec</span><span class="token punctuation">(</span>conf<span class="token punctuation">:</span> <a href="#api/swagger/iswaggersettings"><span class="token">ISwaggerSettings</span></a><span class="token punctuation">)</span><span class="token punctuation">:</span> Spec<span class="token punctuation">;</span>
<span class="token punctuation">}</span></code></pre>
:::


<!-- Members -->




## Members


<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang ">$<span class="token function">afterRoutesInit</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span> <span class="token keyword">void</span></code></pre>
:::
</div>




***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang ">$<span class="token function">onServerReady</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span> <span class="token keyword">void</span></code></pre>
:::
</div>




***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang "><span class="token function">getOpenAPISpec</span><span class="token punctuation">(</span>conf<span class="token punctuation">:</span> <a href="#api/swagger/iswaggersettings"><span class="token">ISwaggerSettings</span></a><span class="token punctuation">)</span><span class="token punctuation">:</span> Spec</code></pre>
:::
</div>




***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang "><span class="token function">getDefaultSpec</span><span class="token punctuation">(</span>conf<span class="token punctuation">:</span> <a href="#api/swagger/iswaggersettings"><span class="token">ISwaggerSettings</span></a><span class="token punctuation">)</span><span class="token punctuation">:</span> Spec</code></pre>
:::
</div>


::: v-pre
Return the global api information.
:::