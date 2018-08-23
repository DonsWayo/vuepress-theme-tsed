---
sidebar: auto
---
# PropertyName <Badge text="Decorator" type="decorator"/>
<!-- Summary -->
<section class="symbol-info"><table class="is-full-width"><tbody><tr><th>Module</th><td><div class="lang-typescript"><span class="token keyword">import</span> { PropertyName }&nbsp;<span class="token keyword">from</span>&nbsp;<span class="token string">"@tsed/common"</span></div></td></tr><tr><th>Source</th><td><a href="https://github.com/Romakita/ts-express-decorators/blob/v4.30.0/src//common/jsonschema/decorators/propertyName.ts#L0-L0">/common/jsonschema/decorators/propertyName.ts</a></td></tr></tbody></table></section>

<!-- Overview -->
## Overview


::: v-pre
<pre><code class="typescript-lang ">function <span class="token function">PropertyName</span><span class="token punctuation">(</span>name<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">)</span><span class="token punctuation">:</span> Function<span class="token punctuation">;</span></code></pre>
:::


<!-- Description -->
## Description

::: v-pre
Create an alias of the propertyKey that must be used by the converter.

?> This decorator is used by the Converters to deserialize correctly you model.

## Example

```typescript
class Model {
   @PropertyType(String)
   property: string[];
}
```

:::