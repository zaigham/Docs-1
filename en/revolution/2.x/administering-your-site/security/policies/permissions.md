---
title: "Permissions"
_old_id: "217"
_old_uri: "2.x/administering-your-site/security/policies/permissions"
---

What is a Permission? 
----------------------

A Permission in Revolution is a single access control that allows or denies execution of a single task. You can think of a permission as a checkbox: can a user perform an action or not?

An example Permission is "content\_types" - if a user's Policy does not contain this Permission, then the user will not be able to perform that action. In this case, the user can not view the Content Types page.

Normally you don't deal with permissions individually, but in groups called [Access Policies](/display/revolution20/Policies "Policies"). An [Access Policy](/display/revolution20/Policies "Policies") is a list of individual permissions (also called an Access Control List or ACL). For example, if you need to grant users the permissions necessary to edit content in the manager, you can assign them to use the "Content Editor" policy.

MODX permissions are always additive: if a permission exists on "Access Policy A" and not on "Access Policy B" and you add both policies to a user, the effective policy is a collection of all the permissions defined in both policies. Adding more policies will never remove permissions for a user. For example, if you add a limited "Load Only" policy to an administrator user, the administrator user will still be able to do all the things defined in the Administrator policy.

Usage 
------

In practice, Access Policies are associated with User Groups (not with individual users). Access Policies are associated with a User Group, and users may be added to the group.

Access Policies (ACLs) define lists of permissions (see Security --> Access Controls). These lists contain groups of permissions that belong together.

1. [Permissions - Administrator Policy](/revolution/2.x/administering-your-site/security/policies/permissions/permissions-administrator-policy)
2. [Permissions - Resource Policy](/revolution/2.x/administering-your-site/security/policies/permissions/permissions-resource-policy)

See Also 
---------

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

There are also "Policy Templates" -- these help organize the lists of permission in the Access Policies. An Access Policy is a list of checkboxes, the Policy Templates define which checkboxes are available for an Access Policy. Because the full list of permissions may be quite long, it's not efficient to define Access Policies while having to wade through hundreds of checkboxes. Policy Templates allow you to narrow down the options available to an Access Policy.