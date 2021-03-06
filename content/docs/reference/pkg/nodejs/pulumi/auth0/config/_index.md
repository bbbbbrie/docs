---
title: "Module config"
title_tag: "Module config | Package @pulumi/auth0 | Node.js SDK"
linktitle: "config"
meta_desc: "Explore members of the config module in the @pulumi/auth0 package."
git_sha: "b00c60b36a1c2a10552cee99cbaccb6855931a0f"
---

<!-- WARNING: this page was generated by a tool. Do not edit it by hand. -->
<!-- To change it, please see https://github.com/pulumi/docs/tree/master/tools/tscdocgen. -->


> This provider is a derived work of the [Terraform Provider](https://github.com/terraform-providers/terraform-provider-auth0)
> distributed under [MPL 2.0](https://www.mozilla.org/en-US/MPL/2.0/). If you encounter a bug or missing feature,
> first check the [`pulumi/pulumi-auth0` repo](https://github.com/pulumi/pulumi-auth0/issues); however, if that doesn't turn up anything,
> please consult the source [`terraform-providers/terraform-provider-auth0` repo](https://github.com/terraform-providers/terraform-provider-auth0/issues).







<h3>APIs</h3>
<ul class="api">
    <li><a href="#clientId"><span class="symbol api"></span>clientId</a></li>
    <li><a href="#clientSecret"><span class="symbol api"></span>clientSecret</a></li>
    <li><a href="#debug"><span class="symbol api"></span>debug</a></li>
    <li><a href="#domain"><span class="symbol api"></span>domain</a></li>
</ul>




<h2 id="apis">APIs</h2>
<h3 class="pdoc-module-header" id="clientId" data-link-title="clientId">
    <a href="https://github.com/pulumi/pulumi-auth0/blob/b00c60b36a1c2a10552cee99cbaccb6855931a0f/sdk/nodejs/config/vars.ts#L9">
        let <strong>clientId</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kd'>let</span> clientId: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> = <span class='s2'> __config.get(&#34;clientId&#34;) || utilities.getEnv(&#34;AUTH0_CLIENT_ID&#34;)</span>;</code></pre>
<h3 class="pdoc-module-header" id="clientSecret" data-link-title="clientSecret">
    <a href="https://github.com/pulumi/pulumi-auth0/blob/b00c60b36a1c2a10552cee99cbaccb6855931a0f/sdk/nodejs/config/vars.ts#L10">
        let <strong>clientSecret</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kd'>let</span> clientSecret: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> = <span class='s2'> __config.get(&#34;clientSecret&#34;) || utilities.getEnv(&#34;AUTH0_CLIENT_SECRET&#34;)</span>;</code></pre>
<h3 class="pdoc-module-header" id="debug" data-link-title="debug">
    <a href="https://github.com/pulumi/pulumi-auth0/blob/b00c60b36a1c2a10552cee99cbaccb6855931a0f/sdk/nodejs/config/vars.ts#L11">
        let <strong>debug</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kd'>let</span> debug: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean'>boolean</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> = <span class='s2'> __config.getObject&lt;boolean&gt;(&#34;debug&#34;) || utilities.getEnvBoolean(&#34;AUTH0_DEBUG&#34;)</span>;</code></pre>
<h3 class="pdoc-module-header" id="domain" data-link-title="domain">
    <a href="https://github.com/pulumi/pulumi-auth0/blob/b00c60b36a1c2a10552cee99cbaccb6855931a0f/sdk/nodejs/config/vars.ts#L12">
        let <strong>domain</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kd'>let</span> domain: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> = <span class='s2'> __config.get(&#34;domain&#34;) || utilities.getEnv(&#34;AUTH0_DOMAIN&#34;)</span>;</code></pre>
