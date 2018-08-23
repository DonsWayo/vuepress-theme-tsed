---
sidebar: auto
---
# TypeORMService <Badge text="Service" type="service"/>
<!-- Summary -->
<section class="symbol-info"><table class="is-full-width"><tbody><tr><th>Module</th><td><div class="lang-typescript"><span class="token keyword">import</span> { TypeORMService }&nbsp;<span class="token keyword">from</span>&nbsp;<span class="token string">"@tsed/typeorm"</span></div></td></tr><tr><th>Source</th><td><a href="https://github.com/Romakita/ts-express-decorators/blob/v4.30.0/src//typeorm/services/TypeORMService.ts#L0-L0">/typeorm/services/TypeORMService.ts</a></td></tr></tbody></table></section>

<!-- Overview -->
## Overview


::: v-pre
<pre><code class="typescript-lang "><span class="token keyword">class</span> TypeORMService <span class="token punctuation">{</span>
    <span class="token function">createConnection</span><span class="token punctuation">(</span>id<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">,</span> settings<span class="token punctuation">:</span> ConnectionOptions<span class="token punctuation">)</span><span class="token punctuation">:</span> Promise&lt<span class="token punctuation">;</span><span class="token keyword">any</span>&gt<span class="token punctuation">;</span><span class="token punctuation">;</span>
    <span class="token function">get</span><span class="token punctuation">(</span>id?<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">)</span><span class="token punctuation">:</span> Connection | undefined<span class="token punctuation">;</span>
    <span class="token function">has</span><span class="token punctuation">(</span>id?<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">)</span><span class="token punctuation">:</span> <span class="token keyword">boolean</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span></code></pre>
:::


<!-- Members -->




## Members


<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang "><span class="token function">createConnection</span><span class="token punctuation">(</span>id<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">,</span> settings<span class="token punctuation">:</span> ConnectionOptions<span class="token punctuation">)</span><span class="token punctuation">:</span> Promise&lt<span class="token punctuation">;</span><span class="token keyword">any</span>&gt<span class="token punctuation">;</span></code></pre>
:::
</div>




***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang "><span class="token function">get</span><span class="token punctuation">(</span>id?<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">)</span><span class="token punctuation">:</span> Connection | undefined</code></pre>
:::
</div>




***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang "><span class="token function">has</span><span class="token punctuation">(</span>id?<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">)</span><span class="token punctuation">:</span> <span class="token keyword">boolean</span></code></pre>
:::
</div>