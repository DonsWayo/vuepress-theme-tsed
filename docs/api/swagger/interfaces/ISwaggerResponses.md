---
sidebar: auto
---
# ISwaggerResponses <Badge text="Interface" type="interface"/>
<!-- Summary -->
<section class="symbol-info"><table class="is-full-width"><tbody><tr><th>Module</th><td><div class="lang-typescript"><span class="token keyword">import</span> { ISwaggerResponses }&nbsp;<span class="token keyword">from</span>&nbsp;<span class="token string">"@tsed/swagger"</span></div></td></tr><tr><th>Source</th><td><a href="https://github.com/Romakita/ts-express-decorators/blob/v4.30.0/src//swagger/interfaces/ISwaggerResponses.ts#L0-L0">/swagger/interfaces/ISwaggerResponses.ts</a></td></tr></tbody></table></section>

<!-- Overview -->
## Overview


::: v-pre
<pre><code class="typescript-lang "><span class="token keyword">interface</span> ISwaggerResponses <span class="token punctuation">{</span>
    use?<span class="token punctuation">:</span> <a href="#api/core/type"><span class="token">Type</span></a>&lt<span class="token punctuation">;</span><span class="token keyword">any</span>&gt<span class="token punctuation">;</span><span class="token punctuation">;</span>
    type?<span class="token punctuation">:</span> <a href="#api/core/type"><span class="token">Type</span></a>&lt<span class="token punctuation">;</span><span class="token keyword">any</span>&gt<span class="token punctuation">;</span><span class="token punctuation">;</span>
    collection?<span class="token punctuation">:</span> <a href="#api/core/type"><span class="token">Type</span></a>&lt<span class="token punctuation">;</span><span class="token keyword">any</span>&gt<span class="token punctuation">;</span><span class="token punctuation">;</span>
    description?<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">;</span>
    examples?<span class="token punctuation">:</span> <span class="token punctuation">{</span>
        <span class="token punctuation">[</span>exampleName<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">]</span><span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span><span class="token punctuation">;</span>
    headers?<span class="token punctuation">:</span> <span class="token punctuation">{</span>
        <span class="token punctuation">[</span>headerName<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">]</span><span class="token punctuation">:</span> <a href="#api/common/mvc/header"><span class="token">Header</span></a><span class="token punctuation">;</span>
    <span class="token punctuation">}</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span></code></pre>
:::


<!-- Members -->




## Members


<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang deprecated ">use?<span class="token punctuation">:</span> <a href="#api/core/type"><span class="token">Type</span></a>&lt<span class="token punctuation">;</span><span class="token keyword">any</span>&gt<span class="token punctuation">;</span></code></pre>
:::
</div>


::: v-pre
Use IResponseOptions.type instead of
:::



***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang ">type?<span class="token punctuation">:</span> <a href="#api/core/type"><span class="token">Type</span></a>&lt<span class="token punctuation">;</span><span class="token keyword">any</span>&gt<span class="token punctuation">;</span></code></pre>
:::
</div>




***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang ">collection?<span class="token punctuation">:</span> <a href="#api/core/type"><span class="token">Type</span></a>&lt<span class="token punctuation">;</span><span class="token keyword">any</span>&gt<span class="token punctuation">;</span></code></pre>
:::
</div>




***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang ">description?<span class="token punctuation">:</span> <span class="token keyword">string</span></code></pre>
:::
</div>




***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang ">examples?<span class="token punctuation">:</span> <span class="token punctuation">{</span>
     <span class="token punctuation">[</span>exampleName<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">]</span><span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">;</span>
 <span class="token punctuation">}</span><span class="token punctuation">;</span></code></pre>
:::
</div>




***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang ">headers?<span class="token punctuation">:</span> <span class="token punctuation">{</span>
     <span class="token punctuation">[</span>headerName<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">]</span><span class="token punctuation">:</span> <a href="#api/common/mvc/header"><span class="token">Header</span></a><span class="token punctuation">;</span>
 <span class="token punctuation">}</span><span class="token punctuation">;</span></code></pre>
:::
</div>