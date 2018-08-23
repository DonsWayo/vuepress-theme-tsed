---
sidebar: auto
---
# Authenticated <Badge text="Decorator" type="decorator"/>
<!-- Summary -->
<section class="symbol-info"><table class="is-full-width"><tbody><tr><th>Module</th><td><div class="lang-typescript"><span class="token keyword">import</span> { Authenticated }&nbsp;<span class="token keyword">from</span>&nbsp;<span class="token string">"@tsed/common"</span></div></td></tr><tr><th>Source</th><td><a href="https://github.com/Romakita/ts-express-decorators/blob/v4.30.0/src//common/mvc/decorators/method/authenticated.ts#L0-L0">/common/mvc/decorators/method/authenticated.ts</a></td></tr></tbody></table></section>

<!-- Overview -->
## Overview


::: v-pre
<pre><code class="typescript-lang ">function <span class="token function">Authenticated</span><span class="token punctuation">(</span>options?<span class="token punctuation">:</span> <span class="token keyword">any</span><span class="token punctuation">)</span><span class="token punctuation">:</span> Function<span class="token punctuation">;</span></code></pre>
:::


<!-- Description -->
## Description

::: v-pre
Set authentication strategy on your endpoint.

```typescript
@ControllerProvider('/mypath')
class MyCtrl {

  @Get('/')
  @Authenticated({role: 'admin'})
  public getResource(){}
}
```

:::