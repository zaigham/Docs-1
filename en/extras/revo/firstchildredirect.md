---
title: "FirstChildRedirect"
_old_id: "641"
_old_uri: "revo/firstchildredirect"
---

<div>- [Installation & bugs](#FirstChildRedirect-Installation%26bugs)
- [Snippet usage](#FirstChildRedirect-Snippetusage)

</div>FirstChildRedirect is a snippet that will redirect a certain resource to its first child resource. There is a version for both Revolution and Evolution, of which the Revolution one allows more easy customization.

Installation & bugs
-------------------

FirstChildRedirect can be installed through the MODX Revolution Package Manager, or installed manually by downloading the package from the MODX Extras website, uploading it to core/packages and adding a new package through the package manager from a local search.

FirstChildRedirect is also available for MODX Evolution, however that does not support all additional parameters as described below.

Snippet usage
-------------

The snippet is really easy to use, just call uncached it in the content or template of the container resource you want to redirect to its first child.

```
<pre class="brush: php">
[[!FirstChildRedirect]]

```Alternatively, you can specify one or more parameters in the snippet call which influence how the redirect will be handled.

<table><tbody><tr><th>Parameter   
</th><th>Evo/Revo   
</th><th>Details   
</th><th>Default   
</th></tr><tr><td>&docid   
</td><td>Yes/Yes   
</td><td>Setting a docid parameter to another resource's ID will tell the snippet to use that resource as the container to look in for the first child.   
</td><td>current resource ID (ie \[\[\*id\]\]   
</td></tr><tr><td>&default   
</td><td>No\*/Yes   
</td><td>The resource to redirect to when there are no children resources found. This can be either a resource ID or one of the following settings: site\_start, site\_unavailable\_page, error\_page or unauthorized\_page. \* In Evolution, this also defaults to site\_start and can be modified in the actual snippet code if required. Just find $modx->config\['site\_start'\] and replace that by an ID or one of the system settings mentioned.   
</td><td>site\_start setting   
</td></tr><tr><td>&sortBy   
</td><td>No/Yes   
</td><td>Any valid resource fieldname to sort the children found on.   
</td><td>menuindex setting   
</td></tr><tr><td>&sortDir   
</td><td>No/Yes   
</td><td>Either 'desc' for descending (redirects to highest menuindex or &sortBy field found) or 'asc' for ascending (redirects to lowest menuindex or &sortBy field found).   
</td><td>"asc"   
</td></tr><tr><td>&responseCode</td><td>No/Yes</td><td>The response code (status code) for sending the redirect. Defaults to a 301 ("HTTP/1.1 301 Moved Permanently") but also contains shortcuts for 302 (temporarily) - you can also specify the complete response code (including the HTTP part and name) for others. _Added in 2.3.1._</td><td>301</td></tr></tbody></table>Using &sortBy=`RAND()` seems to work in 2.1.3 :)

This is good for A/B Split Testing, for example.