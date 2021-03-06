
---
title: "GetUsers"
title_tag: "Function GetUsers | Package Azure AD"
meta_desc: "Explore the GetUsers function of the Azure AD package, including examples, input properties, output properties, and supporting types. Gets Object IDs or UPNs for multiple Azure Active Directory users."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Gets Object IDs or UPNs for multiple Azure Active Directory users.

> **NOTE:** If you're authenticating using a Service Principal then it must have permissions to `Read directory data` within the `Windows Azure Active Directory` API.



{{% examples %}}
## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}

{{% example csharp %}}
```csharp
using Pulumi;
using AzureAD = Pulumi.AzureAD;

class MyStack : Stack
{
    public MyStack()
    {
        var users = Output.Create(AzureAD.GetUsers.InvokeAsync(new AzureAD.GetUsersArgs
        {
            UserPrincipalNames = 
            {
                "kat@hashicorp.com",
                "byte@hashicorp.com",
            },
        }));
    }

}
```
{{% /example %}}

{{% example go %}}
Coming soon!
{{% /example %}}

{{% example python %}}
```python
import pulumi
import pulumi_azuread as azuread

users = azuread.get_users(user_principal_names=[
    "kat@hashicorp.com",
    "byte@hashicorp.com",
])
```
{{% /example %}}

{{% example typescript %}}
```typescript
import * as pulumi from "@pulumi/pulumi";
import * as azuread from "@pulumi/azuread";

const users = pulumi.output(azuread.getUsers({
    userPrincipalNames: [
        "kat@hashicorp.com",
        "byte@hashicorp.com",
    ],
}, { async: true }));
```
{{% /example %}}

{{% /examples %}}


## Using GetUsers {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getUsers<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/azuread/#GetUsersArgs">GetUsersArgs</a></span><span class="p">, </span><span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/azuread/#GetUsersResult">GetUsersResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">function </span> get_users(</span>mail_nicknames=None<span class="p">, </span>object_ids=None<span class="p">, </span>user_principal_names=None<span class="p">, </span>opts=None<span class="p">)</span></code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetUsers<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">args</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-azuread/sdk/v2/go/azuread/?tab=doc#GetUsersArgs">GetUsersArgs</a></span><span class="p">, </span><span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-azuread/sdk/v2/go/azuread/?tab=doc#GetUsersResult">GetUsersResult</a></span>, error)</span></code></pre></div>

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetUsers </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.AzureAD/Pulumi.AzureAD.GetUsersResult.html">GetUsersResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.AzureAD/Pulumi.AzureAD.GetUsersArgs.html">GetUsersArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:



{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span id="mailnicknames_csharp">
<a href="#mailnicknames_csharp" style="color: inherit; text-decoration: inherit;">Mail<wbr>Nicknames</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">List&lt;string&gt;</a></span>
    </dt>
    <dd>{{% md %}}The email aliases of the Azure AD Users.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="objectids_csharp">
<a href="#objectids_csharp" style="color: inherit; text-decoration: inherit;">Object<wbr>Ids</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">List&lt;string&gt;</a></span>
    </dt>
    <dd>{{% md %}}The Object IDs of the Azure AD Users.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="userprincipalnames_csharp">
<a href="#userprincipalnames_csharp" style="color: inherit; text-decoration: inherit;">User<wbr>Principal<wbr>Names</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">List&lt;string&gt;</a></span>
    </dt>
    <dd>{{% md %}}The User Principal Names of the Azure AD Users.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span id="mailnicknames_go">
<a href="#mailnicknames_go" style="color: inherit; text-decoration: inherit;">Mail<wbr>Nicknames</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">[]string</a></span>
    </dt>
    <dd>{{% md %}}The email aliases of the Azure AD Users.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="objectids_go">
<a href="#objectids_go" style="color: inherit; text-decoration: inherit;">Object<wbr>Ids</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">[]string</a></span>
    </dt>
    <dd>{{% md %}}The Object IDs of the Azure AD Users.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="userprincipalnames_go">
<a href="#userprincipalnames_go" style="color: inherit; text-decoration: inherit;">User<wbr>Principal<wbr>Names</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">[]string</a></span>
    </dt>
    <dd>{{% md %}}The User Principal Names of the Azure AD Users.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span id="mailnicknames_nodejs">
<a href="#mailnicknames_nodejs" style="color: inherit; text-decoration: inherit;">mail<wbr>Nicknames</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string[]</a></span>
    </dt>
    <dd>{{% md %}}The email aliases of the Azure AD Users.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="objectids_nodejs">
<a href="#objectids_nodejs" style="color: inherit; text-decoration: inherit;">object<wbr>Ids</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string[]</a></span>
    </dt>
    <dd>{{% md %}}The Object IDs of the Azure AD Users.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="userprincipalnames_nodejs">
<a href="#userprincipalnames_nodejs" style="color: inherit; text-decoration: inherit;">user<wbr>Principal<wbr>Names</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string[]</a></span>
    </dt>
    <dd>{{% md %}}The User Principal Names of the Azure AD Users.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span id="mail_nicknames_python">
<a href="#mail_nicknames_python" style="color: inherit; text-decoration: inherit;">mail_<wbr>nicknames</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">List[str]</a></span>
    </dt>
    <dd>{{% md %}}The email aliases of the Azure AD Users.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="object_ids_python">
<a href="#object_ids_python" style="color: inherit; text-decoration: inherit;">object_<wbr>ids</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">List[str]</a></span>
    </dt>
    <dd>{{% md %}}The Object IDs of the Azure AD Users.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="user_principal_names_python">
<a href="#user_principal_names_python" style="color: inherit; text-decoration: inherit;">user_<wbr>principal_<wbr>names</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">List[str]</a></span>
    </dt>
    <dd>{{% md %}}The User Principal Names of the Azure AD Users.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## GetUsers Result {#result}

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="mailnicknames_csharp">
<a href="#mailnicknames_csharp" style="color: inherit; text-decoration: inherit;">Mail<wbr>Nicknames</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">List&lt;string&gt;</a></span>
    </dt>
    <dd>{{% md %}}The email aliases of the Azure AD Users.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="objectids_csharp">
<a href="#objectids_csharp" style="color: inherit; text-decoration: inherit;">Object<wbr>Ids</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">List&lt;string&gt;</a></span>
    </dt>
    <dd>{{% md %}}The Object IDs of the Azure AD Users.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="userprincipalnames_csharp">
<a href="#userprincipalnames_csharp" style="color: inherit; text-decoration: inherit;">User<wbr>Principal<wbr>Names</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">List&lt;string&gt;</a></span>
    </dt>
    <dd>{{% md %}}The User Principal Names of the Azure AD Users.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="mailnicknames_go">
<a href="#mailnicknames_go" style="color: inherit; text-decoration: inherit;">Mail<wbr>Nicknames</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">[]string</a></span>
    </dt>
    <dd>{{% md %}}The email aliases of the Azure AD Users.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="objectids_go">
<a href="#objectids_go" style="color: inherit; text-decoration: inherit;">Object<wbr>Ids</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">[]string</a></span>
    </dt>
    <dd>{{% md %}}The Object IDs of the Azure AD Users.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="userprincipalnames_go">
<a href="#userprincipalnames_go" style="color: inherit; text-decoration: inherit;">User<wbr>Principal<wbr>Names</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">[]string</a></span>
    </dt>
    <dd>{{% md %}}The User Principal Names of the Azure AD Users.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="mailnicknames_nodejs">
<a href="#mailnicknames_nodejs" style="color: inherit; text-decoration: inherit;">mail<wbr>Nicknames</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string[]</a></span>
    </dt>
    <dd>{{% md %}}The email aliases of the Azure AD Users.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="objectids_nodejs">
<a href="#objectids_nodejs" style="color: inherit; text-decoration: inherit;">object<wbr>Ids</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string[]</a></span>
    </dt>
    <dd>{{% md %}}The Object IDs of the Azure AD Users.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="userprincipalnames_nodejs">
<a href="#userprincipalnames_nodejs" style="color: inherit; text-decoration: inherit;">user<wbr>Principal<wbr>Names</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string[]</a></span>
    </dt>
    <dd>{{% md %}}The User Principal Names of the Azure AD Users.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="mail_nicknames_python">
<a href="#mail_nicknames_python" style="color: inherit; text-decoration: inherit;">mail_<wbr>nicknames</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">List[str]</a></span>
    </dt>
    <dd>{{% md %}}The email aliases of the Azure AD Users.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="object_ids_python">
<a href="#object_ids_python" style="color: inherit; text-decoration: inherit;">object_<wbr>ids</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">List[str]</a></span>
    </dt>
    <dd>{{% md %}}The Object IDs of the Azure AD Users.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="user_principal_names_python">
<a href="#user_principal_names_python" style="color: inherit; text-decoration: inherit;">user_<wbr>principal_<wbr>names</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">List[str]</a></span>
    </dt>
    <dd>{{% md %}}The User Principal Names of the Azure AD Users.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}









<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-azuread">https://github.com/pulumi/pulumi-azuread</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>This Pulumi package is based on the [`azuread` Terraform Provider](https://github.com/terraform-providers/terraform-provider-azuread).</dd>
</dl>

