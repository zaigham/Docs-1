---
title: "Successful Installation, Now What Do I Do?"
_old_id: "1688"
_old_uri: "2.x/getting-started/installation/successful-installation,-now-what-do-i-do"
---

<div>- [Creating the first page](#SuccessfulInstallation%2CNowWhatDoIDo%3F-Creatingthefirstpage)
- [Creating a Template](#SuccessfulInstallation%2CNowWhatDoIDo%3F-CreatingaTemplate)
 
</div> After a successful installation, you'll be presented with the Manager login page. Use the login and password you specified during the installation, log in. You will be presented with something like this

 ![](/download/attachments/18678051/first_login.png)

 Since Revolution RC1 doesn't come with any default content, there aren't any pages, which is why this list of error messages. Therefore, the first thing to do is create a page to make these errors go away.

Creating the first page
-----------------------

 This being MODx, there are several ways to create a new resource (document). The main Site menu has a "New Document" menu item, the Tree View block on the left will have the first section, Web Resources, open (if it's not open, click on the Web Resources bar to open it) with its menu bar so you can use the Create Resource button (the third from the left, the yellow folder with the green plus sign on it), or you can right-click on the web context icon, choose Create, then Create a Document Here.

 The New Document window will appear. On the right, taking up most of the page, will be the document's fields. To begin with, just give the document a title, Home, a Menu Title, First Document, and some content. Make sure to check the Published check box. Click on the floating Save button to save your new document.

 ![](/download/attachments/18678051/first_document.png?version=1&modificationDate=1269279147000)

 And now, if you view the tree on the left, you'll see your new document listed. Go to the main Site menu, click the Preview menu item, and view your page in all its glory!

Creating a Template
-------------------

 Obviously, the page alone is missing something. We need to create a template to give it some structure and style. Click on the Tree View's 'Elements' tab. This will open a selection of elements you can create and manage to add dynamic content to your page. Right-click on the Template element, and you'll see two choices for creating a new template, New Template and Quick Create Template.

- The Quick Create Template opens a pop-up window to allow for quickly creating a template without moving from the page you're working on.
- The New Template changes the right panel to a more complex form for creating a new template.

 In either case, give the template a name, My Template, a description, First Revolution Template, and then the HTML code for the template. MODx templates are basically just HTML pages, with the content parts replaced with MODx tags. So to begin with, let's just create a really simple template.

 ```
<pre class="brush: php">

<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en">
<head>
    <title>My First Revolutionary Page</title>
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
    <style type="text/css" media="screen">
        #content{width:80%;margin:auto;border:5px groove #a484ce;}
        #content h1{color:#a484ce;padding:10px 20px;text-align:center;}
        #content p{padding:20px;text-align:center;}
    </style>
</head>
<body>
    <div id="content">
        [[*content]]
    </div>
</body>
</html>

``` Save the new template. Now if you open your first document for editing, you'll see that it's been assigned the template (since it's the only one, and the document didn't have one). Go back to the site and refresh the page. And now, if you click the main Home menu, you'll get the Manager home page without that long list of errors!

</body></html>