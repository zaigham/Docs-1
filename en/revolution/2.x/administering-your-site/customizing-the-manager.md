---
title: "Customizing the Manager"
_old_id: "83"
_old_uri: "2.x/administering-your-site/customizing-the-manager"
---

<div>- [What is Form Customization?](#CustomizingtheManager-WhatisFormCustomization%3F)
- [How Does it Work?](#CustomizingtheManager-HowDoesitWork%3F)
  - [What Forms can I Customize?](#CustomizingtheManager-WhatFormscanICustomize%3F)
- [See Also](#CustomizingtheManager-SeeAlso)
 
</div>What is Form Customization?
---------------------------

 Form Customization is a new feature that allows users to create Rules, which govern how manager pages render their forms in the MODX Revolution Manager. It is similar to ManagerManager in MODX Evolution.

 <object height="350" width="500"><param name="movie" value="https://www.youtube.com/v/iJB_IXg7NNc&hl=en&fs=1"></param><param name="allowFullScreen" value="true"></param><param name="allowscriptaccess" value="always"></param><embed allowfullscreen="true" allowscriptaccess="always" flashvars="$flashVars" height="350" src="https://www.youtube.com/v/iJB_IXg7NNc&hl=en&fs=1" type="application/x-shockwave-flash" width="500"></embed></object>How Does it Work?
-----------------

 Currently, Form Customization has 3 layers:

> Profile -> Sets -> Rules

 A Profile is a collection of Sets, and Sets are collections of Rules. Profiles can be restricted to specific User Groups.

 A Set is a collection of Rules, and is tied to a certain view. Normally, you would have a Set for the Resource/Create page, and a Set for the Resource/Update page. Sets can also be tied to specific [Templates](/revolution/2.x/making-sites-with-modx/structuring-your-site/templates "Templates") (meaning they load only when the Resource is using that Template). They can also have a 'Constraint' set, which limits the Set's execution to the restriction made in the Constraint.

 A Rule is all the variations applied in a Set. Rules are hidden from view in MODX Revolution, but are instead shown as fields on the Set Editing page.

 More information about each of the parts of Form Customization can be found in each part's respective page:

1. [Customizing the Manager via Plugins](/revolution/2.x/administering-your-site/customizing-the-manager/customizing-the-manager-via-plugins)
2. [Form Customization Profiles](/revolution/2.x/administering-your-site/customizing-the-manager/form-customization-profiles)
3. [Form Customization Sets](/revolution/2.x/administering-your-site/customizing-the-manager/form-customization-sets)
  1. [Customizing Tabs via Form Customization](/revolution/2.x/administering-your-site/customizing-the-manager/form-customization-sets/customizing-tabs-via-form-customization)
4. [Manager Templates and Themes](/revolution/2.x/administering-your-site/customizing-the-manager/manager-templates-and-themes)

### What Forms can I Customize?

 The Resource Create and Update pages can be customized at this time in Form Customization.

See Also
--------

1. [Customizing the Manager via Plugins](/revolution/2.x/administering-your-site/customizing-the-manager/customizing-the-manager-via-plugins)
2. [Form Customization Profiles](/revolution/2.x/administering-your-site/customizing-the-manager/form-customization-profiles)
3. [Form Customization Sets](/revolution/2.x/administering-your-site/customizing-the-manager/form-customization-sets)
  1. [Customizing Tabs via Form Customization](/revolution/2.x/administering-your-site/customizing-the-manager/form-customization-sets/customizing-tabs-via-form-customization)
4. [Manager Templates and Themes](/revolution/2.x/administering-your-site/customizing-the-manager/manager-templates-and-themes)