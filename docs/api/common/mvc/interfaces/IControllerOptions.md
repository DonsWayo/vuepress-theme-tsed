---
sidebar: auto
---
# IControllerOptions <Badge text="Interface" type="interface"/>
<!-- Summary -->
<section class="symbol-info"><table class="is-full-width"><tbody><tr><th>Module</th><td><div class="lang-typescript"><span class="token keyword">import</span> { IControllerOptions }&nbsp;<span class="token keyword">from</span>&nbsp;<span class="token string">"@tsed/common"</span></div></td></tr><tr><th>Source</th><td><a href="https://github.com/Romakita/ts-express-decorators/blob/v4.30.0/src//common/mvc/interfaces/IControllerOptions.ts#L0-L0">/common/mvc/interfaces/IControllerOptions.ts</a></td></tr></tbody></table></section>

<!-- Overview -->
## Overview


::: v-pre
<pre><code class="typescript-lang "><span class="token keyword">interface</span> IControllerOptions <span class="token punctuation">{</span>
    path?<span class="token punctuation">:</span> <a href="#api/common/mvc/pathparamstype"><span class="token">PathParamsType</span></a><span class="token punctuation">;</span>
    dependencies?<span class="token punctuation">:</span> <a href="#api/core/type"><span class="token">Type</span></a>&lt<span class="token punctuation">;</span><span class="token keyword">any</span>&gt<span class="token punctuation">;</span><span class="token punctuation">[</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
    routerOptions?<span class="token punctuation">:</span> <a href="#api/common/config/iroutersettings"><span class="token">IRouterSettings</span></a><span class="token punctuation">;</span>
    middlewares?<span class="token punctuation">:</span> <a href="#api/common/mvc/icontrollermiddlewares"><span class="token">IControllerMiddlewares</span></a><span class="token punctuation">;</span>
<span class="token punctuation">}</span></code></pre>
:::


<!-- Members -->




## Members


<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang ">path?<span class="token punctuation">:</span> <a href="#api/common/mvc/pathparamstype"><span class="token">PathParamsType</span></a></code></pre>
:::
</div>




***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang ">dependencies?<span class="token punctuation">:</span> <a href="#api/core/type"><span class="token">Type</span></a>&lt<span class="token punctuation">;</span><span class="token keyword">any</span>&gt<span class="token punctuation">;</span><span class="token punctuation">[</span><span class="token punctuation">]</span></code></pre>
:::
</div>




***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang ">routerOptions?<span class="token punctuation">:</span> <a href="#api/common/config/iroutersettings"><span class="token">IRouterSettings</span></a></code></pre>
:::
</div>




***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang ">middlewares?<span class="token punctuation">:</span> <a href="#api/common/mvc/icontrollermiddlewares"><span class="token">IControllerMiddlewares</span></a></code></pre>
:::
</div>