---
title: NuGet Publisher task Version 0.*
ms.custom: seodec18
description: Learn all about how you can publish NuGet packages when building code in Azure Pipelines and Team Foundation Server
ms.technology: vs-devops-package
ms.assetid: E592A505-C253-4190-86D2-E4F679F5FCBE
ms.date: 08/10/2016
monikerRange: '<= tfs-2017'
---

# Package: NuGet Publisher task version 0.*

[!INCLUDE [version-lt-eq-2017](../../../../includes/version-lt-eq-2017.md)]

Use this task to publish your NuGet package to a server and update your feed.

## Demands

None

## Arguments

<table>
<thead>
<tr>
<th>Argument</th>
<th>Description</th>
</tr>
</thead>
<tr>
<td>Path/Pattern to nupkg</td>
<td>
<p>Specify the packages you want to publish.</p>
<ul>
<li>Default value: <code><strong>*.nupkg;-:</strong>\packages*<em>*.nupkg</code></li>
<li>To publish a single package, click the <strong>...</strong> button and select the file.</li>
<li>Use single-folder wildcards (<code></em></code>) and recursive wildcards (<code><strong></code>) to publish multiple packages.</li>
<li>Use <a href="../../../build/variables.md" data-raw-source="[variables](../../../build/variables.md)">variables</a> to specify directories. For example, if you specified <code>$(Build.StagingDirectory)\packages</code> as the <strong>package folder</strong> in the NuGet Packager task, you could specify <code>$(Build.StagingDirectory)\packages\</strong>*.nupkg</code> here.</li>
</ul>
<!-- https://github.com/Microsoft/vso-agent-tasks/blob/master/Tasks/NugetPublisher/task.json says you can specify multiple patterns separated by semicolons. That doesn't seem to work -->
</td>
</tr>
<tr>
<td>Feed type</td>
<td>
<ul>
<li><strong>External NuGetFeed</strong> publishes to an external server such as <a href="https://www.nuget.org/" data-raw-source="[NuGet](https://www.nuget.org/)">NuGet</a> or <a href="http://www.myget.org/" data-raw-source="[MyGet](https://www.myget.org/)">MyGet</a>. After you select this option, you create and select a <strong>NuGet server endpoint</strong>.
</li>
<li><strong>Internal NuGet Feed</strong> publishes to an internal or Azure Artifacts feed. After you select this option, you specify the <strong>internal feed URL</strong>.
</li>
</ul>
</td>
</tr>
</table>

### Advanced options

<table>
<thead>
<tr>
<th>Argument</th>
<th>Description</th>
</tr>
</thead>
<tr>
<td>NuGet Arguments</td>
<td>
(Optional) Additional arguments passed to <a href="https://docs.nuget.org/consume/command-line-reference#user-content-push-command" data-raw-source="[nuget push](https://docs.nuget.org/consume/command-line-reference#user-content-push-command)">nuget push</a>.
</td>
</tr>

[!INCLUDE [temp](../../includes/nuget-step-arguments.md)]

</table>

[!INCLUDE [temp](../../includes/control-options-arguments.md)]

</table>

## Examples

[!INCLUDE [temp](../../includes/nuget-create-step-examples.md)]
