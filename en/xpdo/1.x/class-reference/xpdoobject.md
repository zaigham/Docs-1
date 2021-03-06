---
title: "xPDOObject"
_old_id: "1628"
_old_uri: "1.x/class-reference/xpdoobject"
---

Most of the magic of xPDO is packed into the class xPDOObject. This class is the base persistence class which every domain class and table class you create with xPDO will derive it's properties and behavior from. xPDOObject is a domain class and an Active Record pattern implementation, where each instance represents a row in a specific database table.

1. [Static Object Loaders](/xpdo/1.x/class-reference/xpdoobject/static-object-loaders)
  1. [load](/xpdo/1.x/class-reference/xpdoobject/static-object-loaders/load)
  2. [loadCollection](/xpdo/1.x/class-reference/xpdoobject/static-object-loaders/loadcollection)
  3. [loadCollectionGraph](/xpdo/1.x/class-reference/xpdoobject/static-object-loaders/loadcollectiongraph)
  4. [Using Custom Loader Classes](/xpdo/1.x/class-reference/xpdoobject/static-object-loaders/using-custom-loader-classes)
2. [Configuration Accessors](/xpdo/1.x/class-reference/xpdoobject/configuration-accessors)
  1. [getOption](/xpdo/1.x/class-reference/xpdoobject/configuration-accessors/getoption)
  2. [setOption](/xpdo/1.x/class-reference/xpdoobject/configuration-accessors/setoption)
3. [Field Accessors](/xpdo/1.x/class-reference/xpdoobject/field-accessors)
  1. [get](/xpdo/1.x/class-reference/xpdoobject/field-accessors/get)
  2. [set](/xpdo/1.x/class-reference/xpdoobject/field-accessors/set)
  3. [toArray](/xpdo/1.x/class-reference/xpdoobject/field-accessors/toarray)
  4. [fromArray](/xpdo/1.x/class-reference/xpdoobject/field-accessors/fromarray)
  5. [toJSON](/xpdo/1.x/class-reference/xpdoobject/field-accessors/tojson)
  6. [fromJSON](/xpdo/1.x/class-reference/xpdoobject/field-accessors/fromjson)
4. [Related Object Accessors](/xpdo/1.x/class-reference/xpdoobject/related-object-accessors)
  1. [getOne](/xpdo/1.x/class-reference/xpdoobject/related-object-accessors/getone)
  2. [getMany](/xpdo/1.x/class-reference/xpdoobject/related-object-accessors/getmany)
  3. [addOne](/xpdo/1.x/class-reference/xpdoobject/related-object-accessors/addone)
  4. [addMany](/xpdo/1.x/class-reference/xpdoobject/related-object-accessors/addmany)
5. [Persistence Methods](/xpdo/1.x/class-reference/xpdoobject/persistence-methods)
  1. [save](/xpdo/1.x/class-reference/xpdoobject/persistence-methods/save)
  2. [remove](/xpdo/1.x/class-reference/xpdoobject/persistence-methods/remove)
6. [Metadata Accessors](/xpdo/1.x/class-reference/xpdoobject/metadata-accessors)
  1. [getSelectColumns](/xpdo/1.x/class-reference/xpdoobject/metadata-accessors/getselectcolumns)
  2. [getPK](/xpdo/1.x/class-reference/xpdoobject/metadata-accessors/getpk)
  3. [getPKType](/xpdo/1.x/class-reference/xpdoobject/metadata-accessors/getpktype)
  4. [getFKClass](/xpdo/1.x/class-reference/xpdoobject/metadata-accessors/getfkclass)
  5. [getFKDefinition](/xpdo/1.x/class-reference/xpdoobject/metadata-accessors/getfkdefinition)
  6. [getFieldName](/xpdo/1.x/class-reference/xpdoobject/metadata-accessors/getfieldname)
7. [Validation](/xpdo/1.x/class-reference/xpdoobject/validation)
  1. [addValidationRule](/xpdo/1.x/class-reference/xpdoobject/validation/addvalidationrule)
  2. [removeValidationRules](/xpdo/1.x/class-reference/xpdoobject/validation/removevalidationrules)
  3. [getValidator](/xpdo/1.x/class-reference/xpdoobject/validation/getvalidator)
  4. [validate](/xpdo/1.x/class-reference/xpdoobject/validation/validate)
  5. [isValidated](/xpdo/1.x/class-reference/xpdoobject/validation/isvalidated)
8. [State Accessors](/xpdo/1.x/class-reference/xpdoobject/state-accessors)
  1. [isLazy](/xpdo/1.x/class-reference/xpdoobject/state-accessors/islazy)
  2. [isDirty](/xpdo/1.x/class-reference/xpdoobject/state-accessors/isdirty)
  3. [isNew](/xpdo/1.x/class-reference/xpdoobject/state-accessors/isnew)