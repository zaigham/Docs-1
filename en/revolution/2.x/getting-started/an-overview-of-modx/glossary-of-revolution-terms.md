---
title: "Glossary of Revolution Terms"
_old_id: "157"
_old_uri: "2.x/getting-started/an-overview-of-modx/glossary-of-revolution-terms"
---

<div>- [Add-on](#GlossaryofRevolutionTerms-Addon)
- [Asset](#GlossaryofRevolutionTerms-Asset)
- [Back-end](#GlossaryofRevolutionTerms-Backend)
- [Category](#GlossaryofRevolutionTerms-Category)
- [Chunk Tags](#GlossaryofRevolutionTerms-ChunkTags)
- [Component](#GlossaryofRevolutionTerms-Component)
- [Content Type](#GlossaryofRevolutionTerms-ContentType)
- [Context](#GlossaryofRevolutionTerms-Context)
- [Context Setting](#GlossaryofRevolutionTerms-ContextSetting)
- [Core Workspace](#GlossaryofRevolutionTerms-CoreWorkspace)
- [Document](#GlossaryofRevolutionTerms-Document)
- [Document Identifier](#GlossaryofRevolutionTerms-DocumentIdentifier)
- [Element](#GlossaryofRevolutionTerms-Element)
- [Extension](#GlossaryofRevolutionTerms-Extension)
- [File Resolver](#GlossaryofRevolutionTerms-FileResolver)
- [Language Tags](#GlossaryofRevolutionTerms-LanguageTags)
- [Lexicon](#GlossaryofRevolutionTerms-Lexicon)
- [Lexicon Topic (formerly Foci)](#GlossaryofRevolutionTerms-LexiconTopic%28formerlyFoci%29)
- [Link Tags](#GlossaryofRevolutionTerms-LinkTags)
- [Manager](#GlossaryofRevolutionTerms-Manager)
- [Namespace](#GlossaryofRevolutionTerms-Namespace)
- [Placeholder Tags](#GlossaryofRevolutionTerms-PlaceholderTags)
- [Resource Field](#GlossaryofRevolutionTerms-Resource%26nbsp%3BField)
- [Property](#GlossaryofRevolutionTerms-Property)
- [Property Set](#GlossaryofRevolutionTerms-PropertySet)
- [Resource](#GlossaryofRevolutionTerms-Resource)
- [Resource Identifier](#GlossaryofRevolutionTerms-ResourceIdentifier)
- [Resource Tags](#GlossaryofRevolutionTerms-ResourceTags)
- [Resolver (for xPDOVehicles)](#GlossaryofRevolutionTerms-Resolver%28forxPDOVehicles%29)
- [Setting Tags](#GlossaryofRevolutionTerms-SettingTags)
- [Snippet Tags](#GlossaryofRevolutionTerms-SnippetTags)
- [Static Resource](#GlossaryofRevolutionTerms-StaticResource)
- [Symlink](#GlossaryofRevolutionTerms-Symlink)
- [System Setting](#GlossaryofRevolutionTerms-SystemSetting)
- [Template Variables](#GlossaryofRevolutionTerms-TemplateVariables)
- [Transport Package](#GlossaryofRevolutionTerms-TransportPackage)
- [Transport Provider (formerly Provisioner)](#GlossaryofRevolutionTerms-TransportProvider%28formerlyProvisioner%29)
- [Transport Vehicles](#GlossaryofRevolutionTerms-TransportVehicles)
- [User Setting](#GlossaryofRevolutionTerms-UserSetting)
- [Weblink](#GlossaryofRevolutionTerms-Weblink)
- [Validator (for xPDOVehicles)](#GlossaryofRevolutionTerms-Validator%28forxPDOVehicles%29)
- [xPDOVehicle](#GlossaryofRevolutionTerms-xPDOVehicle)

</div>- - - - - -

### Add-on

A MODx Third-party Component (3PC) that does not modify the Core or extend any of its classes, but yet still provides extra functionality to the MODx instance.

- - - - - -

### Asset

Any type of file resource that is usually located in the /assets directory, as defined by the constant MODX\_ASSETS\_PATH; can include Third-party Components, libraries, image files, css files, JavaScript files, class files, etc.

- - - - - -

### Back-end

A synonym for the MODx manager interface.

- - - - - -

### Category

An optional classifying name that can be attached to any Element or PropertySet (and other objects in later versions of Revolution) that separates it from other similar objects.

- - - - - -

### Chunk Tags

Tags in the form \[\[$ChunkName\]\] that can be used in reference to Chunks.

- - - - - -

### Component

Also called "Third-party Component", or 3PC, a Component usually provides extra functionality to MODx, usually in the form of an Add-on, Core Extension, or Template.

- - - - - -

### Content Type

Sets the extension, mime-type and binary setting for any Resource.

- - - - - -

### Context

A delineator of resources and settings that can be used for a variety of reasons; usually used to create multiple-context sites, such as subdomains, multi-language sites, etc.

- - - - - -

### Context Setting

A single setting for that Context that either creates a new setting or overrides a System Setting.

- - - - - -

### Core Workspace

Each unique MODx Core is represented by a named Workspace. When you install Revolution initially, the MODx Core used by the setup application is recorded into the MODx database as the Default MODx Workspace. In future MODx Revolution releases, there will be an ability to manage multiple Workspaces from a single database, directly from the manager application. This will make it easy to isolate upgrades to the MODx Core; by quickly adding a new Core Workspace and selecting a menu option, you'll be able to apply an entire new MODx Core installation to production sites after testing on a staging site, or quickly revert to a previous Core Workspace you know works. This will be especially important for multi-site configurations running on shared MODx Core installations.

- - - - - -

### Document

A specific type of Resource, usually pertaining to a normal website page.

- - - - - -

### Document Identifier

See Resource Identifier.

- - - - - -

### Element

Also called "Content Elements", a single Template, Template Variable, Chunk, Snippet, Plugin, Category, or Property Set visible in the Manager Elements tree.

- - - - - -

### Extension

Also called "Core Extension". A MODx Third-party Component that modifies the MODx Core, such as a custom User or authentication class, caching mechanisms, or context manipulation classes.

- - - - - -

### File Resolver

A type of xPDOVehicle Resolver that copies files from the source location to the target location in a Transport Package.

- - - - - -

### Language Tags

Tags in the form \[\[%LanguageStringKey\]\] that reference MODx Lexicon entries.

- - - - - -

### Lexicon

A Lexicon is a dictionary of words and phrases organized by Culture (more specific than language, i.e. en-UK) that is used to internationalize the manager application and can be used by Add-On and Core Extension developers to provide localization facilities for their own components. This replaces the legacy MODx language files and allows customization of the entries directly from the manager application.

- - - - - -

### Lexicon Topic (formerly Foci)

A set of Lexicon Entries focused on a particular subject. Revolution only loads Lexicon Entries as it needs them, by their Topic, to reduce load times.

- - - - - -

### Link Tags

Tags in the form \[\[~ResourceId\]\] that reference the URL of a particular Resource.

- - - - - -

### Manager

The back-end of the MODx interface.

- - - - - -

### Namespace

An organizational tag for Components to use to identify Lexicon Entries, Settings, and other objects related to the Component in a Revolution site. Also specifies an absolute path in which the Component may be found.

- - - - - -

### Placeholder Tags

Tags in the form \[\[+PlaceholderName\]\] that reference MODx Placeholders, usually set with $modx->setPlaceholder('placeholderName','value') in a Snippet or Plugin.

- - - - - -

### Resource Field

Any of the fields of the site\_content table, such as pagetitle, longtitle, introtext, alias, menuindex, etc. Some fields are available on the Document Create/Edit screen and via Resource Tags; Others can only be accessed via the documentObject.

- - - - - -

### Property

A single variable for an Element; used to set a specific parameter for the Element.

- - - - - -

### Property Set

A collection of variables used for a particular purpose with an Element. Property Sets are attached to Elements and pass in the Properties that they carry as parameters to the Element. An example is a custom Property Set for a Snippet that passes in specific parameters to the Element, overriding the default behavior.

- - - - - -

### Resource

A type of container that is interpreted by the Parser to fetch content. Can have any number of derivative classes; the most common is a Document.

- - - - - -

### Resource Identifier

Also called a Document ID, Resource ID, or Document Identifier; the number in parenthesis in the MODx Resource Tree in the Manager that uniquely identifies the Resource specified.

- - - - - -

### Resource Tags

Tags in the form \[\[\*ResourceField/TV\]\], which can be used to refer to Resource Fields, or Template Variables.

- - - - - -

### Resolver (for xPDOVehicles)

Post-processor: a script or predefined action that is evaluated after a Vehicle is installed or uninstalled. Resolvers always occur after the vehicle's object is save()'d, and can then perform actions on MODx before anything else happens in the install/uninstall process.

An example of a PHP Resolver is one that attaches Plugin Events to a newly-installed Plugin.

An example of a file Resolver is one that copies the assets/ditto directory in the xPDOVehicle path to /modx/assets/ditto.

- - - - - -

### Setting Tags

Tags in the form \[\[++SettingName\]\] that reference MODx System Settings, Context Settings, and User Settings.

- - - - - -

### Snippet Tags

Tags in the form \[\[SnippetName\]\], also referred to as Snippet Calls.

- - - - - -

### Static Resource

A specific type of Resource that is a direct reference to a specific file on the MODx site. The content is replaced with the contents of that file.

- - - - - -

### Symlink

A type of Resource that references a single, local MODx Resource; the Resource's content will replace the Symlink's content.

- - - - - -

### System Setting

A site-wide variable accessible to the MODx site. Can be overridden by Context Settings and User Settings.

- - - - - -

### Template Variables

Custom Resource Fields created by the user on the Document Create/Edit Screen and referenced using Content Tags.

- - - - - -

### Transport Package

A packaged and zipped collection of Transport Vehicles, that can be easily distributed ("transported") from one Core Workspace to another.

- - - - - -

### Transport Provider (formerly Provisioner)

A web service that enables remote installation of Transport Packages directly from the MODx manager application.

- - - - - -

### Transport Vehicles

An intelligent container that encapsulates any artifact that can be distributed in a Transport Package. Transport Vehicles store their payloads in a portable format.

- - - - - -

### User Setting

A user-specific setting that either creates a new setting or overrides the similar Context Setting and System Setting. Used to provide unique settings to that user.

- - - - - -

### Weblink

A type of Resource that references a specific URL or MODx Resource, redirecting the visitor to that URL or Resource.

- - - - - -

### Validator (for xPDOVehicles)

Pre-processor: a script or predefined action that executes prior to the vehicle being installed or uninstalled. If the validator returns true, the install/uninstall action will proceed as normal. If the validator returns false, MODx will not uninstall or install the package.

A Validator could be used to determine if a directory exists and is writable, to see if other modx elements are already installed, or to determine if a certain version of MySQL and PHP are used on a server.

- - - - - -

### xPDOVehicle

The base Transport Vehicle class, xPDOVehicle, stores xPDOObject instances (which represent a row of data in a table) in it's payload, along with various attributes that control how the object is installed/uninstalled in a Core Workspace (see xPDOVehicle Validators and xPDOVehicle Resolvers).