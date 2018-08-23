---
sidebar: auto
---
# AcceptMime <Badge text="Decorator" type="decorator"/>
<!-- Summary -->
<section class="symbol-info"><table class="is-full-width"><tbody><tr><th>Module</th><td><div class="lang-typescript"><span class="token keyword">import</span> { AcceptMime }&nbsp;<span class="token keyword">from</span>&nbsp;<span class="token string">"@tsed/common/lib/mvc/decorators/method/acceptMime"</span></div></td></tr><tr><th>Source</th><td><a href="https://github.com/Romakita/ts-express-decorators/blob/v4.30.0/src//common/mvc/decorators/method/acceptMime.ts#L0-L0">/common/mvc/decorators/method/acceptMime.ts</a></td></tr></tbody></table></section>

<!-- Overview -->
## Overview


::: v-pre
<pre><code class="typescript-lang ">function <span class="token function">AcceptMime</span><span class="token punctuation">(</span>...mimes<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">[</span><span class="token punctuation">]</span><span class="token punctuation">)</span><span class="token punctuation">:</span> Function<span class="token punctuation">;</span></code></pre>
:::


<!-- Description -->
## Description

::: v-pre
Set a mime list as acceptable for a request on a specific endpoint.

```typescript
 @ControllerProvider('/mypath')
 provide MyCtrl {

   @Get('/')
   @AcceptMime('application/json')
   public getResource(){}
 }
```

:::