---
sidebar: auto
---
# MulterFileSize <Badge text="Decorator" type="decorator"/>
<!-- Summary -->
<section class="symbol-info"><table class="is-full-width"><tbody><tr><th>Module</th><td><div class="lang-typescript"><span class="token keyword">import</span> { MulterFileSize }&nbsp;<span class="token keyword">from</span>&nbsp;<span class="token string">"@tsed/multipartfiles"</span></div></td></tr><tr><th>Source</th><td><a href="https://github.com/Romakita/ts-express-decorators/blob/v4.30.0/src//multipartfiles/decorators/multerFileSize.ts#L0-L0">/multipartfiles/decorators/multerFileSize.ts</a></td></tr></tbody></table></section>

<!-- Overview -->
## Overview


::: v-pre
<pre><code class="typescript-lang ">function <span class="token function">MulterFileSize</span><span class="token punctuation">(</span>fileSize<span class="token punctuation">:</span> <span class="token keyword">number</span><span class="token punctuation">)</span><span class="token punctuation">:</span> <span class="token punctuation">(</span>target<span class="token punctuation">:</span> <span class="token keyword">any</span><span class="token punctuation">,</span> propertyKey<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">,</span> descriptor<span class="token punctuation">:</span> PropertyDescriptor<span class="token punctuation">)</span> =&gt<span class="token punctuation">;</span> PropertyDescriptor<span class="token punctuation">;</span></code></pre>
:::


<!-- Description -->
## Description

::: v-pre
Define file size limit.

```typescript
import {Controller, Post} from "@tsed/common";
import {MulterOptions, MultipartFile} from "@tsed/multipartfiles";
import {Multer} from "@types/multer";

type MulterFile = Express.Multer.File;

@Controller('/')
class MyCtrl {
  @Post('/file2')
  @MulterFileSize(1024) // (Ko). Applied for all fields
  private uploadFile(@MultipartFile("file1") file: MulterFile, @MultipartFile("file2") file2: MulterFile) {

  }
}
```

> See the tutorial on the [multer configuration](tutorials/upload-files-with-multer.md).
:::