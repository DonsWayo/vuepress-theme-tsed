---
sidebar: auto
---
# ProxyRegistry <Badge text="Class" type="class"/>
<!-- Summary -->
<section class="symbol-info"><table class="is-full-width"><tbody><tr><th>Module</th><td><div class="lang-typescript"><span class="token keyword">import</span> { ProxyRegistry }&nbsp;<span class="token keyword">from</span>&nbsp;<span class="token string">"@tsed/core"</span></div></td></tr><tr><th>Source</th><td><a href="https://github.com/Romakita/ts-express-decorators/blob/v4.30.0/src//core/class/ProxyRegistry.ts#L0-L0">/core/class/ProxyRegistry.ts</a></td></tr></tbody></table></section>

<!-- Overview -->
## Overview


::: v-pre
<pre><code class="typescript-lang "><span class="token keyword">abstract</span> <span class="token keyword">class</span> ProxyRegistry&lt<span class="token punctuation">;</span>T<span class="token punctuation">,</span> I&gt<span class="token punctuation">;</span> <span class="token keyword">extends</span> <a href="#api/core/proxymap"><span class="token">ProxyMap</span></a>&lt<span class="token punctuation">;</span><a href="#api/core/registrykey"><span class="token">RegistryKey</span></a><span class="token punctuation">,</span> T&gt<span class="token punctuation">;</span> <span class="token punctuation">{</span>
    <span class="token keyword">protected</span> registry<span class="token punctuation">:</span> <a href="#api/core/registry"><span class="token">Registry</span></a>&lt<span class="token punctuation">;</span>T<span class="token punctuation">,</span> I&gt<span class="token punctuation">;</span><span class="token punctuation">;</span>
    <span class="token keyword">constructor</span><span class="token punctuation">(</span>registry<span class="token punctuation">:</span> <a href="#api/core/registry"><span class="token">Registry</span></a>&lt<span class="token punctuation">;</span>T<span class="token punctuation">,</span> I&gt<span class="token punctuation">;</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token function">set</span><span class="token punctuation">(</span>key<span class="token punctuation">:</span> <a href="#api/core/registrykey"><span class="token">RegistryKey</span></a><span class="token punctuation">,</span> value<span class="token punctuation">:</span> T<span class="token punctuation">)</span><span class="token punctuation">:</span> this<span class="token punctuation">;</span>
<span class="token punctuation">}</span></code></pre>
:::


<!-- Members -->




## Members


<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang "><span class="token keyword">protected</span> registry<span class="token punctuation">:</span> <a href="#api/core/registry"><span class="token">Registry</span></a>&lt<span class="token punctuation">;</span>T<span class="token punctuation">,</span> I&gt<span class="token punctuation">;</span></code></pre>
:::
</div>




***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang "><span class="token function">set</span><span class="token punctuation">(</span>key<span class="token punctuation">:</span> <a href="#api/core/registrykey"><span class="token">RegistryKey</span></a><span class="token punctuation">,</span> value<span class="token punctuation">:</span> T<span class="token punctuation">)</span><span class="token punctuation">:</span> this</code></pre>
:::
</div>