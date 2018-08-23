---
sidebar: auto
---
# ParamMetadata <Badge text="Class" type="class"/>
<!-- Summary -->
<section class="symbol-info"><table class="is-full-width"><tbody><tr><th>Module</th><td><div class="lang-typescript"><span class="token keyword">import</span> { ParamMetadata }&nbsp;<span class="token keyword">from</span>&nbsp;<span class="token string">"@tsed/common"</span></div></td></tr><tr><th>Source</th><td><a href="https://github.com/Romakita/ts-express-decorators/blob/v4.30.0/src//common/filters/class/ParamMetadata.ts#L0-L0">/common/filters/class/ParamMetadata.ts</a></td></tr></tbody></table></section>

<!-- Overview -->
## Overview


::: v-pre
<pre><code class="typescript-lang "><span class="token keyword">class</span> ParamMetadata <span class="token keyword">extends</span> <a href="#api/core/storable"><span class="token">Storable</span></a> <span class="token keyword">implements</span> <a href="#api/common/filters/iparamoptions"><span class="token">IParamOptions</span></a>&lt<span class="token punctuation">;</span><span class="token keyword">any</span>&gt<span class="token punctuation">;</span> <span class="token punctuation">{</span>
    <span class="token keyword">protected</span> _expression<span class="token punctuation">:</span> <span class="token keyword">string</span> | RegExp<span class="token punctuation">;</span>
    <span class="token keyword">protected</span> _useConverter<span class="token punctuation">:</span> <span class="token keyword">boolean</span><span class="token punctuation">;</span>
    <span class="token keyword">protected</span> _service<span class="token punctuation">:</span> <span class="token keyword">string</span> | <a href="#api/core/type"><span class="token">Type</span></a>&lt<span class="token punctuation">;</span><span class="token keyword">any</span>&gt<span class="token punctuation">;</span> | symbol<span class="token punctuation">;</span>
    <span class="token keyword">protected</span> _required<span class="token punctuation">:</span> <span class="token keyword">boolean</span><span class="token punctuation">;</span>
    expression<span class="token punctuation">:</span> <span class="token keyword">string</span> | RegExp<span class="token punctuation">;</span>
    service<span class="token punctuation">:</span> <a href="#api/core/type"><span class="token">Type</span></a>&lt<span class="token punctuation">;</span><span class="token keyword">any</span>&gt<span class="token punctuation">;</span> | symbol<span class="token punctuation">;</span>
    useConverter<span class="token punctuation">:</span> <span class="token keyword">boolean</span><span class="token punctuation">;</span>
    useValidation<span class="token punctuation">:</span> <span class="token keyword">boolean</span><span class="token punctuation">;</span>
    required<span class="token punctuation">:</span> <span class="token keyword">boolean</span><span class="token punctuation">;</span>
    allowedRequiredValues<span class="token punctuation">:</span> <span class="token keyword">any</span><span class="token punctuation">[</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
    paramType<span class="token punctuation">:</span> <a href="#api/common/filters/paramtypes"><span class="token">ParamTypes</span></a><span class="token punctuation">;</span>
    <span class="token function">isValidRequiredValue</span><span class="token punctuation">(</span>value<span class="token punctuation">:</span> <span class="token keyword">any</span><span class="token punctuation">)</span><span class="token punctuation">:</span> <span class="token keyword">boolean</span><span class="token punctuation">;</span>
    <span class="token function">isRequired</span><span class="token punctuation">(</span>value<span class="token punctuation">:</span> <span class="token keyword">any</span><span class="token punctuation">)</span><span class="token punctuation">:</span> <span class="token keyword">boolean</span><span class="token punctuation">;</span>
    <span class="token function">toJSON</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
        service<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">;</span>
        name<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">;</span>
        expression<span class="token punctuation">:</span> <span class="token keyword">string</span> | RegExp<span class="token punctuation">;</span>
        required<span class="token punctuation">:</span> <span class="token keyword">boolean</span><span class="token punctuation">;</span>
        use<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">;</span>
        baseType<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span></code></pre>
:::


<!-- Members -->




## Members


<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang "><span class="token keyword">protected</span> _expression<span class="token punctuation">:</span> <span class="token keyword">string</span> | RegExp</code></pre>
:::
</div>




***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang "><span class="token keyword">protected</span> _useConverter<span class="token punctuation">:</span> <span class="token keyword">boolean</span></code></pre>
:::
</div>




***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang "><span class="token keyword">protected</span> _service<span class="token punctuation">:</span> <span class="token keyword">string</span> | <a href="#api/core/type"><span class="token">Type</span></a>&lt<span class="token punctuation">;</span><span class="token keyword">any</span>&gt<span class="token punctuation">;</span> | symbol</code></pre>
:::
</div>




***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang "><span class="token keyword">protected</span> _required<span class="token punctuation">:</span> <span class="token keyword">boolean</span></code></pre>
:::
</div>


::: v-pre
Required entity.
:::



***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang ">expression<span class="token punctuation">:</span> <span class="token keyword">string</span> | RegExp</code></pre>
:::
</div>




***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang ">service<span class="token punctuation">:</span> <a href="#api/core/type"><span class="token">Type</span></a>&lt<span class="token punctuation">;</span><span class="token keyword">any</span>&gt<span class="token punctuation">;</span> | symbol</code></pre>
:::
</div>




***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang ">useConverter<span class="token punctuation">:</span> <span class="token keyword">boolean</span></code></pre>
:::
</div>




***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang ">useValidation<span class="token punctuation">:</span> <span class="token keyword">boolean</span></code></pre>
:::
</div>




***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang ">required<span class="token punctuation">:</span> <span class="token keyword">boolean</span></code></pre>
:::
</div>


::: v-pre
Change the state of the required data.
:::



***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang ">allowedRequiredValues<span class="token punctuation">:</span> <span class="token keyword">any</span><span class="token punctuation">[</span><span class="token punctuation">]</span></code></pre>
:::
</div>


::: v-pre
Set the allowed values when the value is required.
:::



***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang ">paramType<span class="token punctuation">:</span> <a href="#api/common/filters/paramtypes"><span class="token">ParamTypes</span></a></code></pre>
:::
</div>




***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang deprecated "><span class="token function">isValidRequiredValue</span><span class="token punctuation">(</span>value<span class="token punctuation">:</span> <span class="token keyword">any</span><span class="token punctuation">)</span><span class="token punctuation">:</span> <span class="token keyword">boolean</span></code></pre>
:::
</div>


::: v-pre
This method use `EntityDescription.required` and `allowedRequiredValues` to validate the value.
:::



***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang "><span class="token function">isRequired</span><span class="token punctuation">(</span>value<span class="token punctuation">:</span> <span class="token keyword">any</span><span class="token punctuation">)</span><span class="token punctuation">:</span> <span class="token keyword">boolean</span></code></pre>
:::
</div>




***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang "><span class="token function">toJSON</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
     service<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">;</span>
     name<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">;</span>
     expression<span class="token punctuation">:</span> <span class="token keyword">string</span> | RegExp<span class="token punctuation">;</span>
     required<span class="token punctuation">:</span> <span class="token keyword">boolean</span><span class="token punctuation">;</span>
     use<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">;</span>
     baseType<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">;</span>
 <span class="token punctuation">}</span><span class="token punctuation">;</span></code></pre>
:::
</div>