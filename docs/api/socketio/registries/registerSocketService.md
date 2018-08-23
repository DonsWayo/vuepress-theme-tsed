---
sidebar: auto
---
# registerSocketService <Badge text="Function" type="function"/>
<!-- Summary -->
<section class="symbol-info"><table class="is-full-width"><tbody><tr><th>Module</th><td><div class="lang-typescript"><span class="token keyword">import</span> { registerSocketService }&nbsp;<span class="token keyword">from</span>&nbsp;<span class="token string">"@tsed/socketio/lib/registries/SocketServiceRegistry"</span></div></td></tr><tr><th>Source</th><td><a href="https://github.com/Romakita/ts-express-decorators/blob/v4.30.0/src//socketio/registries/SocketServiceRegistry.ts#L0-L0">/socketio/registries/SocketServiceRegistry.ts</a></td></tr></tbody></table></section>

<!-- Overview -->
## Overview


::: v-pre
<pre><code class="typescript-lang "><span class="token keyword">const</span> registerSocketService<span class="token punctuation">:</span> <span class="token punctuation">(</span>provider<span class="token punctuation">:</span> <span class="token keyword">any</span><span class="token punctuation">,</span> instance?<span class="token punctuation">:</span> <span class="token keyword">any</span><span class="token punctuation">)</span> =&gt<span class="token punctuation">;</span> <span class="token keyword">void</span><span class="token punctuation">;</span></code></pre>
:::


<!-- Description -->
## Description

::: v-pre
Add a new service in the `ProviderRegistry`. This service will be built when `InjectorService` will be loaded.

#### Example

```typescript
import {registerSocketService, InjectorService} from "@tsed/common";

export default class MyFooService {
    constructor(){}
    getFoo() {
        return "test";
    }
}

registerSocketService({provide: MyFooService});
// or
registerSocketService(MyFooService);

const injector = new InjectorService();
injector.load();

const myFooService = injector.get<MyFooService>(MyFooService);
myFooService.getFoo(); // test
```

:::