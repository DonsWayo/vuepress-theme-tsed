---
sidebar: auto
---
# PropertyRegistry <Badge text="Class" type="class"/>
<!-- Summary -->
<section class="symbol-info"><table class="is-full-width"><tbody><tr><th>Module</th><td><div class="lang-typescript"><span class="token keyword">import</span> { PropertyRegistry }&nbsp;<span class="token keyword">from</span>&nbsp;<span class="token string">"@tsed/common"</span></div></td></tr><tr><th>Source</th><td><a href="https://github.com/Romakita/ts-express-decorators/blob/v4.30.0/src//common/jsonschema/registries/PropertyRegistry.ts#L0-L0">/common/jsonschema/registries/PropertyRegistry.ts</a></td></tr></tbody></table></section>

<!-- Overview -->
## Overview


::: v-pre
<pre><code class="typescript-lang "><span class="token keyword">class</span> PropertyRegistry <span class="token punctuation">{</span>
    <span class="token keyword">static</span> <span class="token function">get</span><span class="token punctuation">(</span>target<span class="token punctuation">:</span> <a href="#api/core/type"><span class="token">Type</span></a>&lt<span class="token punctuation">;</span><span class="token keyword">any</span>&gt<span class="token punctuation">;</span><span class="token punctuation">,</span> propertyKey<span class="token punctuation">:</span> <span class="token keyword">string</span> | symbol<span class="token punctuation">)</span><span class="token punctuation">:</span> <a href="#api/common/jsonschema/propertymetadata"><span class="token">PropertyMetadata</span></a><span class="token punctuation">;</span>
    <span class="token keyword">static</span> <span class="token function">getProperties</span><span class="token punctuation">(</span>target<span class="token punctuation">:</span> <a href="#api/core/type"><span class="token">Type</span></a>&lt<span class="token punctuation">;</span><span class="token keyword">any</span>&gt<span class="token punctuation">;</span><span class="token punctuation">)</span><span class="token punctuation">:</span> Map&lt<span class="token punctuation">;</span><span class="token keyword">string</span> | symbol<span class="token punctuation">,</span> <a href="#api/common/jsonschema/propertymetadata"><span class="token">PropertyMetadata</span></a>&gt<span class="token punctuation">;</span><span class="token punctuation">;</span>
    <span class="token keyword">static</span> <span class="token function">getOwnProperties</span><span class="token punctuation">(</span>target<span class="token punctuation">:</span> <a href="#api/core/type"><span class="token">Type</span></a>&lt<span class="token punctuation">;</span><span class="token keyword">any</span>&gt<span class="token punctuation">;</span><span class="token punctuation">)</span><span class="token punctuation">:</span> Map&lt<span class="token punctuation">;</span><span class="token keyword">string</span> | symbol<span class="token punctuation">,</span> <a href="#api/common/jsonschema/propertymetadata"><span class="token">PropertyMetadata</span></a>&gt<span class="token punctuation">;</span><span class="token punctuation">;</span>
    <span class="token keyword">static</span> <span class="token function">set</span><span class="token punctuation">(</span>target<span class="token punctuation">:</span> <a href="#api/core/type"><span class="token">Type</span></a>&lt<span class="token punctuation">;</span><span class="token keyword">any</span>&gt<span class="token punctuation">;</span><span class="token punctuation">,</span> propertyKey<span class="token punctuation">:</span> <span class="token keyword">string</span> | symbol<span class="token punctuation">,</span> property<span class="token punctuation">:</span> <a href="#api/common/jsonschema/propertymetadata"><span class="token">PropertyMetadata</span></a><span class="token punctuation">)</span><span class="token punctuation">:</span> <span class="token keyword">void</span><span class="token punctuation">;</span>
    <span class="token keyword">static</span> <span class="token function">required</span><span class="token punctuation">(</span>target<span class="token punctuation">:</span> <a href="#api/core/type"><span class="token">Type</span></a>&lt<span class="token punctuation">;</span><span class="token keyword">any</span>&gt<span class="token punctuation">;</span><span class="token punctuation">,</span> propertyKey<span class="token punctuation">:</span> <span class="token keyword">string</span> | symbol<span class="token punctuation">,</span> allowedRequiredValues?<span class="token punctuation">:</span> <span class="token keyword">any</span><span class="token punctuation">[</span><span class="token punctuation">]</span><span class="token punctuation">)</span><span class="token punctuation">:</span> typeof PropertyRegistry<span class="token punctuation">;</span>
    <span class="token keyword">static</span> <span class="token function">decorate</span><span class="token punctuation">(</span>fn<span class="token punctuation">:</span> <span class="token punctuation">(</span>propertyMetadata<span class="token punctuation">:</span> <a href="#api/common/jsonschema/propertymetadata"><span class="token">PropertyMetadata</span></a><span class="token punctuation">,</span> parameters<span class="token punctuation">:</span> <a href="#api/core/decoratorparameters"><span class="token">DecoratorParameters</span></a><span class="token punctuation">)</span> =&gt<span class="token punctuation">;</span> <span class="token keyword">void</span><span class="token punctuation">)</span><span class="token punctuation">:</span> Function<span class="token punctuation">;</span>
<span class="token punctuation">}</span></code></pre>
:::


<!-- Members -->




## Members


<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang "><span class="token keyword">static</span> <span class="token function">get</span><span class="token punctuation">(</span>target<span class="token punctuation">:</span> <a href="#api/core/type"><span class="token">Type</span></a>&lt<span class="token punctuation">;</span><span class="token keyword">any</span>&gt<span class="token punctuation">;</span><span class="token punctuation">,</span> propertyKey<span class="token punctuation">:</span> <span class="token keyword">string</span> | symbol<span class="token punctuation">)</span><span class="token punctuation">:</span> <a href="#api/common/jsonschema/propertymetadata"><span class="token">PropertyMetadata</span></a></code></pre>
:::
</div>




***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang "><span class="token keyword">static</span> <span class="token function">getProperties</span><span class="token punctuation">(</span>target<span class="token punctuation">:</span> <a href="#api/core/type"><span class="token">Type</span></a>&lt<span class="token punctuation">;</span><span class="token keyword">any</span>&gt<span class="token punctuation">;</span><span class="token punctuation">)</span><span class="token punctuation">:</span> Map&lt<span class="token punctuation">;</span><span class="token keyword">string</span> | symbol<span class="token punctuation">,</span> <a href="#api/common/jsonschema/propertymetadata"><span class="token">PropertyMetadata</span></a>&gt<span class="token punctuation">;</span></code></pre>
:::
</div>




***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang "><span class="token keyword">static</span> <span class="token function">getOwnProperties</span><span class="token punctuation">(</span>target<span class="token punctuation">:</span> <a href="#api/core/type"><span class="token">Type</span></a>&lt<span class="token punctuation">;</span><span class="token keyword">any</span>&gt<span class="token punctuation">;</span><span class="token punctuation">)</span><span class="token punctuation">:</span> Map&lt<span class="token punctuation">;</span><span class="token keyword">string</span> | symbol<span class="token punctuation">,</span> <a href="#api/common/jsonschema/propertymetadata"><span class="token">PropertyMetadata</span></a>&gt<span class="token punctuation">;</span></code></pre>
:::
</div>




***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang "><span class="token keyword">static</span> <span class="token function">set</span><span class="token punctuation">(</span>target<span class="token punctuation">:</span> <a href="#api/core/type"><span class="token">Type</span></a>&lt<span class="token punctuation">;</span><span class="token keyword">any</span>&gt<span class="token punctuation">;</span><span class="token punctuation">,</span> propertyKey<span class="token punctuation">:</span> <span class="token keyword">string</span> | symbol<span class="token punctuation">,</span> property<span class="token punctuation">:</span> <a href="#api/common/jsonschema/propertymetadata"><span class="token">PropertyMetadata</span></a><span class="token punctuation">)</span><span class="token punctuation">:</span> <span class="token keyword">void</span></code></pre>
:::
</div>




***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang "><span class="token keyword">static</span> <span class="token function">required</span><span class="token punctuation">(</span>target<span class="token punctuation">:</span> <a href="#api/core/type"><span class="token">Type</span></a>&lt<span class="token punctuation">;</span><span class="token keyword">any</span>&gt<span class="token punctuation">;</span><span class="token punctuation">,</span> propertyKey<span class="token punctuation">:</span> <span class="token keyword">string</span> | symbol<span class="token punctuation">,</span> allowedRequiredValues?<span class="token punctuation">:</span> <span class="token keyword">any</span><span class="token punctuation">[</span><span class="token punctuation">]</span><span class="token punctuation">)</span><span class="token punctuation">:</span> typeof <a href="#api/common/jsonschema/propertyregistry"><span class="token">PropertyRegistry</span></a></code></pre>
:::
</div>




***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang "><span class="token keyword">static</span> <span class="token function">decorate</span><span class="token punctuation">(</span>fn<span class="token punctuation">:</span> <span class="token punctuation">(</span>propertyMetadata<span class="token punctuation">:</span> <a href="#api/common/jsonschema/propertymetadata"><span class="token">PropertyMetadata</span></a><span class="token punctuation">,</span> parameters<span class="token punctuation">:</span> <a href="#api/core/decoratorparameters"><span class="token">DecoratorParameters</span></a><span class="token punctuation">)</span> =&gt<span class="token punctuation">;</span> <span class="token keyword">void</span><span class="token punctuation">)</span><span class="token punctuation">:</span> Function</code></pre>
:::
</div>