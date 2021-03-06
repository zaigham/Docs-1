---
title: "FormitFastPack"
_old_id: "1708"
_old_uri: "revo/formitfastpack/"
---

What is FormitFastPack?
-----------------------

 FFP simplifies the management of HTML associated with form-processing snippets like FormIt and Login.

Installation
------------

 Install from the [MODX package manager](http://modx.com/extras/package/formitfastpack).

Getting Started
---------------

 Below is a simple example of using the _field_ snippet with a FormIt form. For a more detailed example, check out the [Tutorial](https://rtfm.modx.com/extras/revo/formitfastpack/formitfastpack.tutorial).

 ```
<pre class="brush: html">[[!FormIt? &hooks=`email,redirect` &emailTpl=`ContactFormReport` &emailTo=`[[++emailsender]]` &emailSubject=`New contact form submission` 
           &validate=`email:email:required,message:required` &redirectTo=`1` ]]
<form action="[[~[[*id]]]]" method="post">
[[!field? &type=`text` &name=`email` &req=`1`]]
[[!field? &type=`textarea` &name=`message` &class=`cleardefault` &req=`1`]]
[[!field? &type=`submit` &name=`submitForm` &label=` ` &message=`Send this Message!`]]
</form>

```Included Snippets
-----------------

 [**field**](http://rtfm.modx.com/extras/revo/formitfastpack/formitfastpack.field): One snippet call generates the HTML for a single form field. The HTML for all fields of a single design can be managed with only two chunks (one outer and one inner), and dynamic values such as the current field value and error messages are processed correctly. Selective caching speeds up option processing.

 [**fieldSetDefaults**](http://rtfm.modx.com/extras/revo/formitfastpack/formitfastpack.fieldsetdefaults): This snippet outputs nothing, but any parameters passed to it will change the default value for all subsequently-processed field snippets. This method of setting defaults will not work if a property set is used with the field snippet.

 **fieldPropSetExample**: This is a dummy snippet that holds a complete property set for the "field" snippet. Because property sets cannot work with fieldSetDefaults, the field snippet does not come with a property set. This property set is provided for those who prefer to use property sets over fieldSetDefaults.

 [**fiGenerateReport**](http://rtfm.modx.com/extras/revo/formitfastpack/formitfastpack.figeneratereport): A FormIt hook which generates an email report by iterating all field submitted names and values through a row template chunk.

 [fiProcessArrays](https://rtfm.modx.com/extras/revo/formitfastpack/fiprocessarrays): A FormIt hook which transforms array values into concatenated strings. Later versions of FormIt now provide similar functionality.

 _formCollectErrors_ (coming soon): Outputs a list of form errors.

Automatic Labels
----------------

 By naming your fields properly, you can use FFP's method of generating labels from field names. Alternatively, you can manually specify labels.

 The labels are generated using simple output filters that can be customized: `[[+name:replace=`_== `:ucwords]]`

<div>  _Example results:_  </div> <table><tbody><tr><td> **Field Name** </td> <td> **Generated Label** </td> </tr><tr><td> name </td> <td> Name </td> </tr><tr><td> first\_name </td> <td> First Name </td> </tr><tr><td> company\_address </td> <td> Company Address </td> </tr><tr><td> number\_of\_employees </td> <td> Number Of Employees </td></tr></tbody></table>Support
-------

- Submit issues, questions, and feature requests to the [Issue Tracker](https://github.com/yoleg/FormitFastPack/issues).
- Track development on [GitHub](https://github.com/yoleg/FormitFastPack)
- Discuss on [MODX Forum](http://forums.modx.com/index.php/topic,65244.0.html)
- Contact the author at [websitezen.com/contact](https://websitezen.com/contact).