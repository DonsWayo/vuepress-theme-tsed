---
sidebar: auto
---
# MongoosePreHookAsyncCB <Badge text="Interface" type="interface"/>
<!-- Summary -->
<section class="symbol-info"><table class="is-full-width"><tbody><tr><th>Module</th><td><div class="lang-typescript"><span class="token keyword">import</span> { MongoosePreHookAsyncCB }&nbsp;<span class="token keyword">from</span>&nbsp;<span class="token string">"@tsed/mongoose"</span></div></td></tr><tr><th>Source</th><td><a href="https://github.com/Romakita/ts-express-decorators/blob/v4.30.0/src//mongoose/interfaces/MongooseModelOptions.ts#L0-L0">/mongoose/interfaces/MongooseModelOptions.ts</a></td></tr></tbody></table></section>

<!-- Overview -->
## Overview


::: v-pre
<pre><code class="typescript-lang "><span class="token keyword">interface</span> MongoosePreHookAsyncCB&lt<span class="token punctuation">;</span>T&gt<span class="token punctuation">;</span> <span class="token punctuation">{</span>
    <span class="token punctuation">(</span>doc<span class="token punctuation">:</span> <a href="#api/mongoose/mongoosedocument"><span class="token">MongooseDocument</span></a>&lt<span class="token punctuation">;</span>T&gt<span class="token punctuation">;</span><span class="token punctuation">,</span> next<span class="token punctuation">:</span> HookNextFunction<span class="token punctuation">,</span> done<span class="token punctuation">:</span> HookDoneFunction<span class="token punctuation">)</span><span class="token punctuation">:</span> <span class="token keyword">any</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span></code></pre>
:::


<!-- Members -->




## Members


<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang "><span class="token punctuation">(</span>doc<span class="token punctuation">:</span> <a href="#api/mongoose/mongoosedocument"><span class="token">MongooseDocument</span></a>&lt<span class="token punctuation">;</span>T&gt<span class="token punctuation">;</span><span class="token punctuation">,</span> next<span class="token punctuation">:</span> HookNextFunction<span class="token punctuation">,</span> done<span class="token punctuation">:</span> HookDoneFunction<span class="token punctuation">)</span><span class="token punctuation">:</span> <span class="token keyword">any</span></code></pre>
:::
</div>