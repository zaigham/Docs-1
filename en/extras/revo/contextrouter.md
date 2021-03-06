---
title: "ContextRouter"
_old_id: "622"
_old_uri: "revo/contextrouter"
---

ContextRouter is a plugin by Mark Hamstra which can be used to route contexts based on domains or subdomains. You can not route subfolders with ContextRouter.

Installation & Configuration
----------------------------

Simply install ContextRouter through package management or from the [MODX Extras](http://modx.com/extras/package/contextrouter) site. There's no manager component or configuration you need to manage, however ContextRouter does depend on your individual contexts being configured properly and it has several system settings you can enable if needed.

### Context Configuration

For ContextRouter you will at the very least need each context you want routed to have a **http\_host** context setting. This should contain the host used to access the context, for example "sub.domain.com" or "otherdomain.tld". If you want multiple hosts to route to the specific context, you can specify them as a comma separated list in a **http\_host\_aliases** context setting.

For MODX to properly function, you'll also want to define the **base\_url** (eg "/"), **site\_url** (eg <http://sub.domain.com/>) and **site\_start** (eg 15 for resource 15) settings.

If you already had these configured when you installed ContextRouter, it should automatically fetch these the first time you make a front end request. If you are configuring these settings after installing ContextRouter, you may have to hit Site > Clear Cache to ensure it is collecting them.

### System Settings

Go to System > System Settings and choose contextrouter in the namespace dropdown (the one that defaults to "core").

<table><tbody><tr><th>Key</th><th>Description</th></tr><tr><td>contextrouter.includeWww</td><td>When enabled, ContextRouter will automatically alias www and no-www variations of a host to the current context.</td></tr><tr><td>contextrouter.defaultContext</td><td>The key of the context that any hosts that are not specifically routed should be routed to.</td></tr></tbody></table>### 