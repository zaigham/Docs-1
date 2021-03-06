---
title: "Discuss.Controllers"
_old_id: "813"
_old_uri: "revo/discuss/discuss.controllers"
---

The Discuss Controllers offer customisation through themes and the theme manifest.php files. This documentation is not yet finished (there's a lot of ground to cover, so to say, and your help is greatly appreciated if you can help out.

Please note that this document deals with **web** controllers, not mgr controllers powering the back-end component of Discuss.

The Controllers in Discuss
--------------------------

Please don't forget to read past this list to see common options and placeholders in the controller templates.

- [Discuss.Controllers.board](/extras/revo/discuss/discuss.controllers/discuss.controllers.board "Discuss.Controllers.board")
  - [Discuss.Controllers.board.xml](/extras/revo/discuss/discuss.controllers/discuss.controllers.board/discuss.controllers.board.xml "Discuss.Controllers.board.xml")
- [Discuss.Controllers.home](/extras/revo/discuss/discuss.controllers/discuss.controllers.home "Discuss.Controllers.home")
- [Discuss.Controllers.login](/extras/revo/discuss/discuss.controllers/discuss.controllers.login "Discuss.Controllers.login")
- [Discuss.Controllers.logout](/extras/revo/discuss/discuss.controllers/discuss.controllers.logout "Discuss.Controllers.logout")
- [Discuss.Controllers.profile](/extras/revo/discuss/discuss.controllers/discuss.controllers.profile "Discuss.Controllers.profile")
- [Discuss.Controllers.register](/extras/revo/discuss/discuss.controllers/discuss.controllers.register "Discuss.Controllers.register")
- [Discuss.Controllers.search](/extras/revo/discuss/discuss.controllers/discuss.controllers.search "Discuss.Controllers.search")
- [Discuss.Controllers.thread](/extras/revo/discuss/discuss.controllers/discuss.controllers.thread "Discuss.Controllers.thread")

Options
-------

Controller Options need to go into the theme's manifest file. If you don't know what that mean, please head over to the [Getting Started](/extras/revo/discuss/discuss.getting-started "Discuss.Getting Started") document!

Controller Template
-------------------

The Controller template is basically the content field of a controller. This contains all the neccessary markup and placeholders for the specific controller to be, like, useful to the visitor. The controller template is wrapped by either the pages/wrapper.tpl or pages/print-wrapper.tpl template.

On the subpages of this document all the different controllers are documented. These contain placeholders specific to that controller. On top of that, some placeholders are available in most (if not all) controllers, and are discussed in this section of this page.

<table><tbody><tr><th>Placeholder</th><th>Description</th></tr><tr><td>actionbuttons</td><td>Buttons generated from the chunks/disactionbutton.chunk.tpl chunk, wrapped in the chunks/disactionbuttons.chunk.tpl chunk. Actions are controller specific and can include login, logout, reply, subscribe, etc. All action buttons are assigned a class of dis-action-action\_name where action\_name is the name of the action; this can be used to style specific buttons differently.</td></tr><tr><td>discuss.user.\*</td><td>Call uncached. If logged in, the discuss.user.field\_name placeholder will contain information about the currently logged in user. Available fields:   
- id
- username
- fullname
- name\_first
- name\_last
- email
- posts
- posts\_formatted
- avatar\_url
- isModerator (1 or 0)
- ... and much more TBA

</td></tr><tr><td>discuss\_version</td><td>The current version of Discuss installed.</td></tr><tr><td>discuss.pagetitle</td><td>Call uncached. Contains the title of the current controller.</td></tr><tr><td> </td><td> </td></tr><tr><td> </td><td> </td></tr><tr><td> </td><td> </td></tr></tbody></table>