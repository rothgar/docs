---
title: Module resourcegroups
---

<!-- WARNING: this page was generated by a tool. Do not edit it by hand. -->
<!-- To change it, please see https://github.com/pulumi/docs/tree/master/tools/tscdocgen. -->

<a href="../index.html">@pulumi/aws</a> &gt; resourcegroups

<div class="toggleVisible" markdown="1">
<div class="collapsed" markdown="1">
<h2 class="pdoc-module-header toggleButton" title="Click to show Index">Index ▹</h2>
</div>
<div class="expanded" markdown="1">
<h2 class="pdoc-module-header toggleButton" title="Click to hide Index">Index ▾</h2>
<div class="pdoc-module-contents" markdown="1">
* <a href="#Group">class Group</a>
* <a href="#GroupArgs">interface GroupArgs</a>
* <a href="#GroupState">interface GroupState</a>

<a href="https://github.com/pulumi/pulumi-aws/blob/a998eb1436459bca87792641e7c9fb49e4a5e61c/sdk/nodejs/resourcegroups/group.ts">resourcegroups/group.ts</a> 
</div>
</div>
</div>


<h2 class="pdoc-module-header" id="Group">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws/blob/a998eb1436459bca87792641e7c9fb49e4a5e61c/sdk/nodejs/resourcegroups/group.ts#L34">class <b>Group</b></a>
</h2>
<div class="pdoc-module-contents" markdown="1">
<pre class="highlight"><span class='kd'>extends</span> <a href='https://pulumi.io/reference/pkg/nodejs/@pulumi/pulumi/#CustomResource'>CustomResource</a></pre>

Provides a Resource Group.

## Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const test = new aws.resourcegroups.Group("test", {
    resourceQuery: {
        query: `{
  "ResourceTypeFilters": [
    "AWS::EC2::Instance"
  ],
  "TagFilters": [
    {
      "Key": "Stage",
      "Values": ["Test"]
    }
  ]
}
`,
    },
});
```

<h3 class="pdoc-member-header" id="Group-constructor">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/a998eb1436459bca87792641e7c9fb49e4a5e61c/sdk/nodejs/resourcegroups/group.ts#L62"> <b>constructor</b></a>
</h3>
<div class="pdoc-member-contents" markdown="1">

<pre class="highlight"><span class='kd'></span><span class='kd'>new</span> Group(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, args: <a href='#GroupArgs'>GroupArgs</a>, opts?: <a href='https://pulumi.io/reference/pkg/nodejs/@pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>)</pre>


Create a Group resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

</div>
<h3 class="pdoc-member-header" id="Group-get">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/a998eb1436459bca87792641e7c9fb49e4a5e61c/sdk/nodejs/resourcegroups/group.ts#L43">method <b>get</b></a>
</h3>
<div class="pdoc-member-contents" markdown="1">

<pre class="highlight"><span class='kd'>public static </span>get(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, id: <a href='https://pulumi.io/reference/pkg/nodejs/@pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='https://pulumi.io/reference/pkg/nodejs/@pulumi/pulumi/#ID'>pulumi.ID</a>&gt;, state?: <a href='#GroupState'>GroupState</a>, opts?: <a href='https://pulumi.io/reference/pkg/nodejs/@pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>): <a href='#Group'>Group</a></pre>


Get an existing Group resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

</div>
<h3 class="pdoc-member-header" id="Group-getProvider">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/a998eb1436459bca87792641e7c9fb49e4a5e61c/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L14">method <b>getProvider</b></a>
</h3>
<div class="pdoc-member-contents" markdown="1">

<pre class="highlight"><span class='kd'></span>getProvider(moduleMember: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>): ProviderResource | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span></pre>

</div>
<h3 class="pdoc-member-header" id="Group-isInstance">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/a998eb1436459bca87792641e7c9fb49e4a5e61c/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L107">method <b>isInstance</b></a>
</h3>
<div class="pdoc-member-contents" markdown="1">

<pre class="highlight"><span class='kd'>static </span>isInstance(obj: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>): <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean'>boolean</a></span></pre>


Returns true if the given object is an instance of CustomResource.  This is designed to work even when
multiple copies of the Pulumi SDK have been loaded into the same process.

</div>
<h3 class="pdoc-member-header" id="Group-arn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/a998eb1436459bca87792641e7c9fb49e4a5e61c/sdk/nodejs/resourcegroups/group.ts#L50">property <b>arn</b></a>
</h3>
<div class="pdoc-member-contents" markdown="1">
<pre class="highlight"><span class='kd'>public </span>arn: <a href='https://pulumi.io/reference/pkg/nodejs/@pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>

The ARN assigned by AWS for this resource group.

</div>
<h3 class="pdoc-member-header" id="Group-description">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/a998eb1436459bca87792641e7c9fb49e4a5e61c/sdk/nodejs/resourcegroups/group.ts#L54">property <b>description</b></a>
</h3>
<div class="pdoc-member-contents" markdown="1">
<pre class="highlight"><span class='kd'>public </span>description: <a href='https://pulumi.io/reference/pkg/nodejs/@pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</pre>

A description of the resource group.

</div>
<h3 class="pdoc-member-header" id="Group-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/a998eb1436459bca87792641e7c9fb49e4a5e61c/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L102">property <b>id</b></a>
</h3>
<div class="pdoc-member-contents" markdown="1">
<pre class="highlight"><span class='kd'></span>id: <a href='https://pulumi.io/reference/pkg/nodejs/@pulumi/pulumi/#Output'>Output</a>&lt;<a href='https://pulumi.io/reference/pkg/nodejs/@pulumi/pulumi/#ID'>ID</a>&gt;;</pre>

id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

</div>
<h3 class="pdoc-member-header" id="Group-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/a998eb1436459bca87792641e7c9fb49e4a5e61c/sdk/nodejs/resourcegroups/group.ts#L58">property <b>name</b></a>
</h3>
<div class="pdoc-member-contents" markdown="1">
<pre class="highlight"><span class='kd'>public </span>name: <a href='https://pulumi.io/reference/pkg/nodejs/@pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>

The resource group's name. A resource group name can have a maximum of 127 characters, including letters, numbers, hyphens, dots, and underscores. The name cannot start with `AWS` or `aws`.

</div>
<h3 class="pdoc-member-header" id="Group-resourceQuery">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/a998eb1436459bca87792641e7c9fb49e4a5e61c/sdk/nodejs/resourcegroups/group.ts#L62">property <b>resourceQuery</b></a>
</h3>
<div class="pdoc-member-contents" markdown="1">
<pre class="highlight"><span class='kd'>public </span>resourceQuery: <a href='https://pulumi.io/reference/pkg/nodejs/@pulumi/pulumi/#Output'>pulumi.Output</a>&lt;{
    query: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;
    type: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;
}&gt;;</pre>

A `resource_query` block. Resource queries are documented below.

</div>
<h3 class="pdoc-member-header" id="Group-urn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/a998eb1436459bca87792641e7c9fb49e4a5e61c/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L12">property <b>urn</b></a>
</h3>
<div class="pdoc-member-contents" markdown="1">
<pre class="highlight"><span class='kd'></span>urn: <a href='https://pulumi.io/reference/pkg/nodejs/@pulumi/pulumi/#Output'>Output</a>&lt;<a href='https://pulumi.io/reference/pkg/nodejs/@pulumi/pulumi/#URN'>URN</a>&gt;;</pre>

urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

</div>
</div>
<h2 class="pdoc-module-header" id="GroupArgs">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws/blob/a998eb1436459bca87792641e7c9fb49e4a5e61c/sdk/nodejs/resourcegroups/group.ts#L119">interface <b>GroupArgs</b></a>
</h2>
<div class="pdoc-module-contents" markdown="1">

The set of arguments for constructing a Group resource.

<h3 class="pdoc-member-header" id="GroupArgs-description">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/a998eb1436459bca87792641e7c9fb49e4a5e61c/sdk/nodejs/resourcegroups/group.ts#L123">property <b>description</b></a>
</h3>
<div class="pdoc-member-contents" markdown="1">
<pre class="highlight"><span class='kd'></span>description?: <a href='https://pulumi.io/reference/pkg/nodejs/@pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>

A description of the resource group.

</div>
<h3 class="pdoc-member-header" id="GroupArgs-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/a998eb1436459bca87792641e7c9fb49e4a5e61c/sdk/nodejs/resourcegroups/group.ts#L127">property <b>name</b></a>
</h3>
<div class="pdoc-member-contents" markdown="1">
<pre class="highlight"><span class='kd'></span>name?: <a href='https://pulumi.io/reference/pkg/nodejs/@pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>

The resource group's name. A resource group name can have a maximum of 127 characters, including letters, numbers, hyphens, dots, and underscores. The name cannot start with `AWS` or `aws`.

</div>
<h3 class="pdoc-member-header" id="GroupArgs-resourceQuery">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/a998eb1436459bca87792641e7c9fb49e4a5e61c/sdk/nodejs/resourcegroups/group.ts#L131">property <b>resourceQuery</b></a>
</h3>
<div class="pdoc-member-contents" markdown="1">
<pre class="highlight"><span class='kd'></span>resourceQuery: <a href='https://pulumi.io/reference/pkg/nodejs/@pulumi/pulumi/#Input'>pulumi.Input</a>&lt;{
    query: <a href='https://pulumi.io/reference/pkg/nodejs/@pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;
    type: <a href='https://pulumi.io/reference/pkg/nodejs/@pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;
}&gt;;</pre>

A `resource_query` block. Resource queries are documented below.

</div>
</div>
<h2 class="pdoc-module-header" id="GroupState">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws/blob/a998eb1436459bca87792641e7c9fb49e4a5e61c/sdk/nodejs/resourcegroups/group.ts#L97">interface <b>GroupState</b></a>
</h2>
<div class="pdoc-module-contents" markdown="1">

Input properties used for looking up and filtering Group resources.

<h3 class="pdoc-member-header" id="GroupState-arn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/a998eb1436459bca87792641e7c9fb49e4a5e61c/sdk/nodejs/resourcegroups/group.ts#L101">property <b>arn</b></a>
</h3>
<div class="pdoc-member-contents" markdown="1">
<pre class="highlight"><span class='kd'></span>arn?: <a href='https://pulumi.io/reference/pkg/nodejs/@pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>

The ARN assigned by AWS for this resource group.

</div>
<h3 class="pdoc-member-header" id="GroupState-description">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/a998eb1436459bca87792641e7c9fb49e4a5e61c/sdk/nodejs/resourcegroups/group.ts#L105">property <b>description</b></a>
</h3>
<div class="pdoc-member-contents" markdown="1">
<pre class="highlight"><span class='kd'></span>description?: <a href='https://pulumi.io/reference/pkg/nodejs/@pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>

A description of the resource group.

</div>
<h3 class="pdoc-member-header" id="GroupState-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/a998eb1436459bca87792641e7c9fb49e4a5e61c/sdk/nodejs/resourcegroups/group.ts#L109">property <b>name</b></a>
</h3>
<div class="pdoc-member-contents" markdown="1">
<pre class="highlight"><span class='kd'></span>name?: <a href='https://pulumi.io/reference/pkg/nodejs/@pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>

The resource group's name. A resource group name can have a maximum of 127 characters, including letters, numbers, hyphens, dots, and underscores. The name cannot start with `AWS` or `aws`.

</div>
<h3 class="pdoc-member-header" id="GroupState-resourceQuery">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/a998eb1436459bca87792641e7c9fb49e4a5e61c/sdk/nodejs/resourcegroups/group.ts#L113">property <b>resourceQuery</b></a>
</h3>
<div class="pdoc-member-contents" markdown="1">
<pre class="highlight"><span class='kd'></span>resourceQuery?: <a href='https://pulumi.io/reference/pkg/nodejs/@pulumi/pulumi/#Input'>pulumi.Input</a>&lt;{
    query: <a href='https://pulumi.io/reference/pkg/nodejs/@pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;
    type: <a href='https://pulumi.io/reference/pkg/nodejs/@pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;
}&gt;;</pre>

A `resource_query` block. Resource queries are documented below.

</div>
</div>