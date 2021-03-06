---
title: "sekFormTools"
_old_id: "704"
_old_uri: "revo/sekformtools"
---

What is sekFormTools?
---------------------

SekFormTools is a quick way to add combo boxes with a customized appearance, auto-complete text fields, date pickers, and input fields with prompts to your form. Grab data from any table object and display in a combo box or filter through an auto-complete field with no snippet or chunk modification, just a simple json array of data. Methods have been built in to filter a combo box based on the selection of another combo box. Have text input or text area fields with a prompt overlaying the field. Add a date picker to the form with an easy to use snippet call.

### Requirements

- MODx Revolution 2.2.0-pl2 or later
- PHP5 or later

### History

SekFormTools was written by Stephen Smith, and first released on May 3th, 2012.

### Download

It can be downloaded from within the MODx Revolution manager via [Package Management](http://rtfm.modx.com/display/revolution20/Package+Management), or from the MODx Extras Repository, here: <http://modx.com/extras/package/sekformtools>.

### Development and Bug Reporting

SekFormTools is on GitHub: <https://github.com/insomnix/sekFormTools>, report any issues or feature requests here: <https://github.com/insomnix/sekFormTools/issues>.

### Data

SekFormTools will install 5 tables, a country, state, US cities, US zipcodes, and a US city zip cross reference. Because of the size of the data files and number of records, the data for these tables are optionally downloaded and installed. If you wish to install this data, download [sekformtoolsdata.zip](http://www.seknetsolutions.com/downloads/sekformtoolsdata.zip), copy/paste each file into a temporary snippet, and run the snippet to install the data to the database. If anyone wishes to contribute to the these files, please contact me or post to the [current support thread](http://forums.modx.com/thread/76302/support-comments-for-sekformtools-beta).

Usage
-----

The sekFormTools is called through several snippets using the below tags?

- [sekFormTools.input.autocomplete](/extras/revo/sekformtools/sekformtools.input.autocomplete "sekFormTools.input.autocomplete") - A jquery auto-complete field.
- [sekFormTools.input.combobox](/extras/revo/sekformtools/sekformtools.input.combobox "sekFormTools.input.combobox") - A jquery auto-complete combo box.
- [sekFormTools.input.datepicker](/extras/revo/sekformtools/sekformtools.input.datepicker "sekFormTools.input.datepicker") - A jquery date picker field.
- [sekFormTools.input.textfield](/extras/revo/sekformtools/sekformtools.input.textfield "sekFormTools.input.textfield") - A jquery text field with suggestion overlay.
- [sekFormTools.input.helper](/extras/revo/sekformtools/sekformtools.input.helper "sekFormTools.input.helper") - Called from a blank page, used to fill auto-complete and combo boxes from a database.
- spellchecker - Call the \[\[spellchecker\]\] snippet from anywhere on a page will load spelling and grammar checking on every textarea.

For more complex setups, try [Advanced Examples](/extras/revo/sekformtools/sekformtools-advanced-examples "sekFormTools Advanced Examples").

Available Settings
------------------

<table><tbody><tr><th>Name   
</th><th>Description   
</th><th>Default   
</th><th>Version   
</th></tr><tr><td>sekformtools.load\_jquery</td><td>This will enable or disable JQuery from being loaded when sekFormTools is called on a page. If JQuery is being loaded from another extra used on the same pages as sekFormTools, or it is loaded in a template, this setting should be set to No/False.   
</td><td>Yes/True   
</td><td>>0.0.1   
</td></tr><tr><td>sekformtools.customcss</td><td>Location of the css file in relation to the modx assets folder.</td><td> </td><td>>0.0.1</td></tr><tr><td>sekformtools.theme</td><td>The theme to use for the form fields.</td><td>smoothness</td><td>>0.0.1</td></tr><tr><td>sekformtools.helper\_resource\_id</td><td>The id of the page making the jquery calls.This only needs to be set if you plan to use the autocomplete snippet or filter a combobox,   
</td><td> </td><td>>0.0.1</td></tr></tbody></table>Themes
------

SekFormTools comes with 8 themes. Additional themes can be downloaded from the jquery.ui website and placed in the css folder.

<table><tbody><tr><th>Theme Name</th><th>Version   
</th></tr><tr><td>blitzer</td><td>>0.0.1</td></tr><tr><td>eggplant</td><td>>0.0.1</td></tr><tr><td>flick</td><td>>0.0.1</td></tr><tr><td>overcast</td><td>>0.0.1</td></tr><tr><td>pepper-grinder</td><td>>0.0.1</td></tr><tr><td>redmond</td><td>>0.0.1</td></tr><tr><td>smoothness</td><td>>0.0.1</td></tr><tr><td>ui-lightness</td><td>>0.0.1</td></tr><tr><td>humanity</td><td>>0.0.5</td></tr></tbody></table>