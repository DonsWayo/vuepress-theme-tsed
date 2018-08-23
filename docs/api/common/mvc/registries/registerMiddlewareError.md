---
sidebar: auto
---
# registerMiddlewareError <Badge text="Function" type="function"/>
<!-- Summary -->
<section class="symbol-info"><table class="is-full-width"><tbody><tr><th>Module</th><td><div class="lang-typescript"><span class="token keyword">import</span> { registerMiddlewareError }&nbsp;<span class="token keyword">from</span>&nbsp;<span class="token string">"@tsed/common"</span></div></td></tr><tr><th>Source</th><td><a href="https://github.com/Romakita/ts-express-decorators/blob/v4.30.0/src//common/mvc/registries/MiddlewareRegistry.ts#L0-L0">/common/mvc/registries/MiddlewareRegistry.ts</a></td></tr></tbody></table></section>

<!-- Overview -->
## Overview


::: v-pre
<pre><code class="typescript-lang ">function <span class="token function">registerMiddlewareError</span><span class="token punctuation">(</span>provider<span class="token punctuation">:</span> <span class="token keyword">any</span> | <a href="#api/common/di/iprovider"><span class="token">IProvider</span></a>&lt<span class="token punctuation">;</span><span class="token keyword">any</span>&gt<span class="token punctuation">;</span><span class="token punctuation">,</span> instance?<span class="token punctuation">:</span> <span class="token keyword">any</span><span class="token punctuation">)</span><span class="token punctuation">:</span> <span class="token keyword">void</span><span class="token punctuation">;</span></code></pre>
:::



<!-- Params -->
::: v-pre
Param | Type | Description
---|---|---
 provider|<code>any &#124; &lt;a href="#api/common/di/iprovider"&gt;&lt;span class="token"&gt;IProvider&lt;/span&gt;&lt;/a&gt;&lt;any&gt;</code>|Provider configuration.

:::


<!-- Description -->
## Description

::: v-pre
Add a new middleware in the `ProviderRegistry`. This middleware will be built when `InjectorService` will be loaded.

#### Example

```typescript
import {registerMiddlewareError, InjectorService} from "@tsed/common";

export default class FooMiddleware {
    constructor(){}
    use() {
        return "test";
    }
}

registerMiddlewareError({provide: MyFooService});
// or
registerMiddlewareError(MyFooService);

const injector = new InjectorService();
injector.load();

const fooMiddleware = injector.get<FooMiddleware>(FooMiddleware);
fooMiddleware.use(); // test
```

:::