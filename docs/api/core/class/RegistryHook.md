---
sidebar: auto
---
# RegistryHook <Badge text="Interface" type="interface"/>
<!-- Summary -->
<section class="symbol-info"><table class="is-full-width"><tbody><tr><th>Module</th><td><div class="lang-typescript"><span class="token keyword">import</span> { RegistryHook }&nbsp;<span class="token keyword">from</span>&nbsp;<span class="token string">"@tsed/core"</span></div></td></tr><tr><th>Source</th><td><a href="https://github.com/Romakita/ts-express-decorators/blob/v4.30.0/src//core/class/Registry.ts#L0-L0">/core/class/Registry.ts</a></td></tr></tbody></table></section>

<!-- Overview -->
## Overview


::: v-pre
<pre><code class="typescript-lang "><span class="token keyword">interface</span> RegistryHook&lt<span class="token punctuation">;</span>T&gt<span class="token punctuation">;</span> <span class="token punctuation">{</span>
    onCreate?<span class="token punctuation">(</span>key<span class="token punctuation">:</span> <a href="#api/core/registrykey"><span class="token">RegistryKey</span></a><span class="token punctuation">,</span> item<span class="token punctuation">:</span> T<span class="token punctuation">)</span><span class="token punctuation">:</span> <span class="token keyword">void</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span></code></pre>
:::


<!-- Members -->




## Members


<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang ">onCreate?<span class="token punctuation">(</span>key<span class="token punctuation">:</span> <a href="#api/core/registrykey"><span class="token">RegistryKey</span></a><span class="token punctuation">,</span> item<span class="token punctuation">:</span> T<span class="token punctuation">)</span><span class="token punctuation">:</span> <span class="token keyword">void</span></code></pre>
:::
</div>