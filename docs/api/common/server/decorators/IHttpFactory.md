---
sidebar: auto
---
# IHttpFactory <Badge text="Decorator" type="decorator"/>
<!-- Summary -->
<section class="symbol-info"><table class="is-full-width"><tbody><tr><th>Module</th><td><div class="lang-typescript"><span class="token keyword">import</span> { IHttpFactory }&nbsp;<span class="token keyword">from</span>&nbsp;<span class="token string">"@tsed/common/lib/server/decorators/httpServer"</span></div></td></tr><tr><th>Source</th><td><a href="https://github.com/Romakita/ts-express-decorators/blob/v4.30.0/src//common/server/decorators/httpServer.ts#L0-L0">/common/server/decorators/httpServer.ts</a></td></tr></tbody></table></section>

<!-- Overview -->
## Overview


::: v-pre
<pre><code class="typescript-lang "><span class="token keyword">interface</span> IHttpFactory <span class="token punctuation">{</span>
    <span class="token punctuation">(</span>target<span class="token punctuation">:</span> <a href="#api/core/type"><span class="token">Type</span></a>&lt<span class="token punctuation">;</span><span class="token keyword">any</span>&gt<span class="token punctuation">;</span><span class="token punctuation">,</span> targetKey<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">,</span> descriptor<span class="token punctuation">:</span> TypedPropertyDescriptor&lt<span class="token punctuation">;</span>Function&gt<span class="token punctuation">;</span> | <span class="token keyword">number</span><span class="token punctuation">)</span><span class="token punctuation">:</span> <span class="token keyword">any</span><span class="token punctuation">;</span>
    <span class="token function">get</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span> Http.Server<span class="token punctuation">;</span>
<span class="token punctuation">}</span></code></pre>
:::


<!-- Members -->




## Members


<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang "><span class="token punctuation">(</span>target<span class="token punctuation">:</span> <a href="#api/core/type"><span class="token">Type</span></a>&lt<span class="token punctuation">;</span><span class="token keyword">any</span>&gt<span class="token punctuation">;</span><span class="token punctuation">,</span> targetKey<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">,</span> descriptor<span class="token punctuation">:</span> TypedPropertyDescriptor&lt<span class="token punctuation">;</span>Function&gt<span class="token punctuation">;</span> | <span class="token keyword">number</span><span class="token punctuation">)</span><span class="token punctuation">:</span> <span class="token keyword">any</span></code></pre>
:::
</div>




***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang deprecated "><span class="token function">get</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span> Http.Server</code></pre>
:::
</div>