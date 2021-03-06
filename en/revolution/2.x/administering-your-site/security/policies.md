---
title: "Policies"
_old_id: "243"
_old_uri: "2.x/administering-your-site/security/policies"
---

What is an Access Policy?
-------------------------

 An Access Policy is a set of [Permissions](/revolution/2.x/administering-your-site/security/policies/permissions "Permissions") containing one or many Permissions, as defined in the manager. By default MODX comes with pre-configured Access Policies:

- **Administrator**: Context administration policy with all default permissions.
- **Context Editor**: Context administration policy with limited, content-editing related Permissions, but no publishing Permissions.
- **Context**: A standard Context policy that you can apply when creating Context ACLs for basic read/write and view\_unpublished access within a Context.
- **Element**: MODX Element policy with all attributes.
- **Load Only**: A minimal policy with permission to load an object.
- **Load, List and View**: Provides load, list and view permissions only.
- **Media Source Admin**: Media Source administration policy.
- **Media Source User**: Media Source user policy, with basic viewing and using - but no editing - of Media Sources.
- **Object**: An Object policy with all permissions.
- **Resource**: MODX Resource Policy with all attributes.

<div class="warning"> If you customize any of the above default Access Policies, duplicate (and rename) them before customizing! If you don't do that all customizations will be lost when updating MODX to a newer version as they get overridden by the setup script. </div>Creating and Editing
--------------------

 To create an Access Policy in the manager, navigate to

 **Security -> Access Controls -> Access Policies**

 From there you can add new policies. To edit an Access Policy in the manager, simply right-click the Policy you want to edit.

Usage
-----

 Policies can be used in a myriad of different ways. Here are 3 example usages that come by default in MODx:

### Context Access

 Access Policies can be assigned as [Access Control Lists](/revolution/2.x/administering-your-site/security/policies/acls "ACLs") (ACLs) to a Context and User Group, with a specified Minimum [Role](/revolution/2.x/administering-your-site/security/roles "Roles"). When done, this means that all the Users in that User Group with at least the Role specified as the Minimum Role can use the Permissions in the Policy in the Context specified in the [ACL](/revolution/2.x/administering-your-site/security/policies/acls "ACLs").

 MODx comes with a default ["Administrator" Policy](/revolution/2.x/administering-your-site/security/policies/permissions/permissions-administrator-policy "Permissions - Administrator Policy") that contains all the [Permissions](/revolution/2.x/administering-your-site/security/policies/permissions "Permissions") one would use in a Context ACL. It's best to duplicate this policy when creating a custom access policy for restricting manager users.

### Resource Group Access

 They can also be Resource ACLs, that limit access to Resources based on Roles and Resource Groups. MODx comes packaged with a default ["Resource" Policy](/revolution/2.x/administering-your-site/security/policies/permissions/permissions-resource-policy "Permissions - Resource Policy") that contains all the basic Permissions one would use in a Resource Group ACL.

 An example would be to assign the "Resource" policy to a Resource Group called 'HR Documents'. Then, you would give a User Group called "HR Department" access to this Resource Group via the Resource ACL:

 ![](/download/attachments/18678084/acl-rg1.png?version=1&modificationDate=1280162069000)

 This would restrict all Resources in the "HR Documents" Resource Group to Users only in the "HR Department" group.

### Element Category Access

 Elements can be restricted from view by ACLs on Categories. For example, if you had a User Group called 'Developers', and wanted Users in that group to be the only Group that could see Elements in the Category 'Gallery', you would create an ACL like such, in the "Element Category Access" tab when editing the User Group:

 ![](/download/attachments/18678084/acl-ecat1.png?version=1&modificationDate=1280162231000)

 This would allow only Users in the "Developers" User Group access to see Elements in the "Gallery" Category.

Examples
--------

 Here's an example custom policy:

 ![](/download/attachments/18678084/policy1.png?version=1&modificationDate=1268850255000)

 and its permissions:

 ![](/download/attachments/18678084/policy1-perm.png?version=1&modificationDate=1268850259000)

 Any User that had access to this Policy would have the permissions 'view\_accounts' and 'save\_accounts'.

See Also
--------

1. [Users](/revolution/2.x/administering-your-site/security/users)
2. [User Groups](/revolution/2.x/administering-your-site/security/user-groups)
3. [Resource Groups](/revolution/2.x/administering-your-site/security/resource-groups)
4. [Roles](/revolution/2.x/administering-your-site/security/roles)
5. [Policies](/revolution/2.x/administering-your-site/security/policies)
  1. [Permissions](/revolution/2.x/administering-your-site/security/policies/permissions)
      1. [Permissions - Administrator Policy](/revolution/2.x/administering-your-site/security/policies/permissions/permissions-administrator-policy)
      2. [Permissions - Resource Policy](/revolution/2.x/administering-your-site/security/policies/permissions/permissions-resource-policy)
  2. [ACLs](/revolution/2.x/administering-your-site/security/policies/acls)
  3. [PolicyTemplates](/revolution/2.x/administering-your-site/security/policies/policytemplates)
6. [Security Tutorials](/revolution/2.x/administering-your-site/security/security-tutorials)
  1. [Giving a User Manager Access](/revolution/2.x/administering-your-site/security/security-tutorials/giving-a-user-manager-access)
  2. [Making Member-Only Pages](/revolution/2.x/administering-your-site/security/security-tutorials/making-member-only-pages)
  3. [Creating a Second Super Admin User](/revolution/2.x/administering-your-site/security/security-tutorials/creating-a-second-super-admin-user)
  4. [Restricting an Element from Users](/revolution/2.x/administering-your-site/security/security-tutorials/restricting-an-element-from-users)
  5. [More on the Anonymous User Group](/revolution/2.x/administering-your-site/security/security-tutorials/more-on-the-anonymous-user-group)
7. [Hardening MODX Revolution](/revolution/2.x/administering-your-site/security/hardening-modx-revolution)
8. [Security Standards](/revolution/2.x/administering-your-site/security/security-standards)
9. [Troubleshooting Security](/revolution/2.x/administering-your-site/security/troubleshooting-security)
  1. [Resetting a User Password Manually](/revolution/2.x/administering-your-site/security/troubleshooting-security/resetting-a-user-password-manually)