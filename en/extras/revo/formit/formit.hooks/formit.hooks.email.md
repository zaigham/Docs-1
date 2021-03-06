---
title: "FormIt.Hooks.email"
_old_id: "857"
_old_uri: "revo/formit/formit.hooks/formit.hooks.email"
---

<div>- [FormIt email Hook](#FormIt.Hooks.email-FormItemailHook)
- [Available Properties](#FormIt.Hooks.email-AvailableProperties)
- [Usage](#FormIt.Hooks.email-Usage)
  - [Specifying a Dynamic To Address](#FormIt.Hooks.email-SpecifyingaDynamicToAddress)
  - [Using a Subject Field as the Email Subject Line](#FormIt.Hooks.email-UsingaSubjectFieldastheEmailSubjectLine)
  - [Handling Checkboxes and Multi-Selects in the Email](#FormIt.Hooks.email-HandlingCheckboxesandMultiSelectsintheEmail)
- [See Also](#FormIt.Hooks.email-SeeAlso)

</div>FormIt email Hook
-----------------

 The email hook will email out your form contents to any email(s).

Available Properties
--------------------

 <table><tbody><tr><th> name </th> <th> description </th> </tr><tr><td> emailTpl </td> <td> Required. Tpl chunk for email message. If one is not specified, it will send a list of fields with their values. </td> </tr><tr><td> emailSubject </td> <td> The subject of the email. </td> </tr><tr><td> emailUseFieldForSubject </td> <td> If 1, and the field 'subject' is passed, then will use that field's value as the email's subject line. </td> </tr><tr><td> emailTo </td> <td> A comma-separated list of emails to send to. </td> </tr><tr><td> emailToName </td> <td> Optional. A comma-separated list of names to pair with the emailTo values. </td> </tr><tr><td> emailFrom </td> <td> Optional. If set, will specify the From: address for the email. If not set, will first look for an `email` form field. If none is found, will default to the `emailsender` system setting. NOTE: Always set the emailFrom to a valid emailaddress (that is allowed to send from your server) to avoid rejected emails due to SPF/ DMARC violations. </td> </tr><tr><td> emailFromName </td> <td> Optional. If set, will specify the From: name for the email. </td> </tr><tr><td> emailHtml </td> <td> Optional. Whether or not the email should be in HTML-format. Defaults to 1. </td> </tr><tr><td> emailConvertNewlines </td> <td> Optional. If set to 1, will convert all newlines to br tags. </td> </tr><tr><td> emailReplyTo </td> <td> An email to set as the reply-to. If not set, will first look for an `email` form field. If none is found, will default to value set in `emailFrom`.</td> </tr><tr><td> emailReplyToName </td> <td> Optional. The name for the Reply-To field. </td> </tr><tr><td> emailCC </td> <td> A comma-separated list of emails to send via cc. </td> </tr><tr><td> emailCCName </td> <td> Optional. A comma-separated list of names to pair with the emailCC values. </td> </tr><tr><td> emailBCC </td> <td> A comma-separated list of emails to send via bcc. </td> </tr><tr><td> emailBCCName </td> <td> Optional. A comma-separated list of names to pair with the emailBCC values. </td> </tr><tr><td> emailMultiWrapper </td> <td> Wraps values submitted by checkboxes/multi-selects with this value. Defaults to just the value. (1.6.0+) </td> </tr><tr><td> emailMultiSeparator </td> <td> Separates checkboxes/multi-selects with this value. Defaults to a newline. (1.6.0+) </td></tr></tbody></table><div class="note"> Any of the email hook properties can have placeholders of field names from your form in them that will be evaluated. </div>Usage
-----

 Simply specify it as a hook in your FormIt call, and then specify the email-specific properties in the FormIt call as well.

 ```
<pre class="brush: php">[[!FormIt?
   ...
   &hooks=`email`
   &emailTpl=`CentralizedDebtObligationEmailTpl`
   &emailSubject=`Some Sucker Bought Another CDO`
   &emailTo=`sales@mortgagemoney.com`
   &emailCC=`boss@mortgagemoney.com`
   &emailBCC=`fbi@gov.com`
   &emailBCCName=`CDO Fraud Informant`
]]

``` Note the &emailTpl property points to the name of a Chunk. In that Chunk, you'll have placeholders for each field in your form. Our Chunk could look like this:

 ```
<pre class="brush: php"><p>Hello,</p>
<p>[[+name]] just purchased the CDO package: [[+cdo_package]].</p>
<p>Their email: [[+email]]</p>
<p>Thanks!</p>

``` This assumes, of course, that you have the fields "name", "cdo\_package" and "email" in your form.

### Specifying a Dynamic To Address

 An example is using the form to specify who to send to:

 ```
<pre class="brush: php">[[!FormIt?
   ...
   &emailTo=`[[+addressTo]]`
]]
...
<select name="addressTo">
   <option value="john@doe.com" [[!+fi.addressTo:FormItIsSelected=`john@doe.com`]]>John</option>
   <option value="jane@doe.com" [[!+fi.addressTo:FormItIsSelected=`jane@doe.com`]]>Jane</option>
</select>

``` This will send the email to whoever is selected in the "addressTo" field.

### Using a Subject Field as the Email Subject Line

 Let's say you have a subject field in your form. You want that to be the subject of the email sent out. The email hook has the ability to do this:

 ```
<pre class="brush: php">[[!FormIt?
    ...
    &emailUseFieldForSubject=`1`
]]

``` This will then look for a field named "subject" that will be used in the email. If it's not found or empty, it will default to the &emailSubject property.

### Handling Checkboxes and Multi-Selects in the Email

 FormIt, as of 1.6.0+, will automatically handle checkboxes and combine them into one field. You can use the &emailMultiSeparator and &emailMultiWrapper properties to specify how they are joined. For example, to wrap checkboxes in LI tags:

 ```
<pre class="brush: php">[[!FormIt?
    ...
    &emailMultiWrapper=`<li>[[+value]]</li>`
]]

``` Or just to separate them with BR tags:

 ```
<pre class="brush: php">[[!FormIt?
    ...
    &emailMultiSeparator=`<br />`
]]

```See Also
--------

1. [FormIt.Hooks.email](/extras/revo/formit/formit.hooks/formit.hooks.email)
2. [FormIt.Hooks.FormItAutoResponder](/extras/revo/formit/formit.hooks/formit.hooks.formitautoresponder)
3. [FormIt.Hooks.FormItSaveForm](http://rtfm.modx.com/extras/revo/formit/formit.hooks/formit.hooks.formitsaveform)
4. [FormIt.Hooks.math](/extras/revo/formit/formit.hooks/formit.hooks.math)
5. [FormIt.Hooks.recaptcha](/extras/revo/formit/formit.hooks/formit.hooks.recaptcha)
6. [FormIt.Hooks.redirect](/extras/revo/formit/formit.hooks/formit.hooks.redirect)
7. [FormIt.Hooks.spam](/extras/revo/formit/formit.hooks/formit.hooks.spam)