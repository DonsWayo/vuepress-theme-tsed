---
sidebar: auto
---
# ILoggerSettings <Badge text="Interface" type="interface"/>
<!-- Summary -->
<section class="symbol-info"><table class="is-full-width"><tbody><tr><th>Module</th><td><div class="lang-typescript"><span class="token keyword">import</span> { ILoggerSettings }&nbsp;<span class="token keyword">from</span>&nbsp;<span class="token string">"@tsed/common"</span></div></td></tr><tr><th>Source</th><td><a href="https://github.com/Romakita/ts-express-decorators/blob/v4.30.0/src//common/config/interfaces/IServerSettings.ts#L0-L0">/common/config/interfaces/IServerSettings.ts</a></td></tr></tbody></table></section>

<!-- Overview -->
## Overview


::: v-pre
<pre><code class="typescript-lang "><span class="token keyword">interface</span> ILoggerSettings <span class="token punctuation">{</span>
    debug<span class="token punctuation">:</span> <span class="token keyword">boolean</span><span class="token punctuation">;</span>
    requestFields?<span class="token punctuation">:</span> <span class="token punctuation">(</span>"reqId" | "method" | "url" | "headers" | "body" | "query" | "params" | "duration"<span class="token punctuation">)</span><span class="token punctuation">[</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
    ignoreUrlPatterns?<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">[</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
    logRequest?<span class="token punctuation">:</span> <span class="token keyword">boolean</span><span class="token punctuation">;</span>
    jsonIndentation?<span class="token punctuation">:</span> <span class="token keyword">number</span><span class="token punctuation">;</span>
    reqIdBuilder?<span class="token punctuation">:</span> <span class="token punctuation">(</span><span class="token punctuation">)</span> =&gt<span class="token punctuation">;</span> <span class="token keyword">number</span><span class="token punctuation">;</span>
    disableRoutesSummary?<span class="token punctuation">:</span> <span class="token keyword">boolean</span><span class="token punctuation">;</span>
    format?<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span></code></pre>
:::


<!-- Members -->




## Members


<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang ">debug<span class="token punctuation">:</span> <span class="token keyword">boolean</span></code></pre>
:::
</div>


::: v-pre
Enable debug mode. By default debug is false.
:::



***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang ">requestFields?<span class="token punctuation">:</span> <span class="token punctuation">(</span>"reqId" | "method" | "url" | "headers" | "body" | "query" | "params" | "duration"<span class="token punctuation">)</span><span class="token punctuation">[</span><span class="token punctuation">]</span></code></pre>
:::
</div>


::: v-pre
Fields displayed when a request is logged. Possible values: `reqId`, `method`, `url`, `headers`, `body`, `query`,`params`, `duration`.
:::



***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang ">ignoreUrlPatterns?<span class="token punctuation">:</span> <span class="token keyword">string</span><span class="token punctuation">[</span><span class="token punctuation">]</span></code></pre>
:::
</div>


::: v-pre
List of regexp to ignore log.
:::



***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang ">logRequest?<span class="token punctuation">:</span> <span class="token keyword">boolean</span></code></pre>
:::
</div>


::: v-pre
Log all incoming request. By default is true and print the configured `logger.requestFields`.
:::



***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang ">jsonIndentation?<span class="token punctuation">:</span> <span class="token keyword">number</span></code></pre>
:::
</div>


::: v-pre
The number of space characters to use as white space in JSON output. Default is 2 (0 in production).
:::



***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang ">reqIdBuilder?<span class="token punctuation">:</span> <span class="token punctuation">(</span><span class="token punctuation">)</span> =&gt<span class="token punctuation">;</span> <span class="token keyword">number</span></code></pre>
:::
</div>


::: v-pre
A function called for each incoming request to create a request id.
:::



***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang ">disableRoutesSummary?<span class="token punctuation">:</span> <span class="token keyword">boolean</span></code></pre>
:::
</div>


::: v-pre
Disable routes table displayed in the logger. By default debug is `false`.
:::



***



<div class="method-overview">
::: v-pre
<pre><code class="typescript-lang ">format?<span class="token punctuation">:</span> <span class="token keyword">string</span></code></pre>
:::
</div>


::: v-pre
Specify log format. Example: `%[%d{[yyyy-MM-dd hh:mm:ss,SSS}] %p%] %m`. See [ts-log-debug configuration](https://romakita.github.io/ts-log-debug/).
:::