---
title: "Adding a Translation"
_old_id: "344"
_old_uri: "2.x/developing-in-modx/advanced-development/internationalization/adding-a-translation"
---

<div>- [The Core Manager Lexicon](#AddingaTranslation-TheCoreManagerLexicon)
- [The Setup Lexicon](#AddingaTranslation-TheSetupLexicon)
- [Extras Lexicons](#AddingaTranslation-ExtrasLexicons)
- [Contributing Translations](#AddingaTranslation-ContributingTranslations)

</div> Adding translations is fairly simple in MODX.

The Core Manager Lexicon
------------------------

 If your language is not in the provided translations, you can fairly simply add a translation of the manager interface by copying the following directory, and renaming to your IANA code for your language (example: "de" for German, "it" for Italian):

 <span style="">`core/lexicon/en/ -> core/lexicon/[mylanguage]/`</span>

 So, for example, if we wanted to create a Haitian translation ("ht"), we would just copy core/lexicon/en/ to core/lexicon/ht/. Then we would edit the .inc.php files in the core/lexicon/ht/ directory, translating the string values there into Haitian.

The Setup Lexicon
-----------------

 A similar process can be done for the installer, if you so choose. Just copy the following directory and rename - similarly to how you do the core manager lexicon:

 <span style="">`setup/lang/en/ -> setup/lang/[mylanguage]/`</span>

Extras Lexicons
---------------

 Often, Extras lexicons can be found in their respective directories in the core/components/ directory. For example, [Quip's](/extras/revo/quip "Quip") is found here:

 <span style="">`core/components/quip/lexicon/en/`</span>

 <span style=""> You can copy the "en" directory and repeat the normal process to translate it as well.</span>

Contributing Translations
-------------------------

<div class="info">  **Update** (27/06/2014)   
 We are currently using Crowdin for translations.   
 Please join our project <https://crowdin.net/project/modx-revolution> and suggest changes there. </div> More information can be found [in this forum post](http://forums.modx.com/thread/91796/revolution-translation).

 <s>Consider contributing your core translations to the MODX core by submitting a Pull Request on [GitHub](https://github.com/modxcms/revolution). Contributions require a [CLA signature](http://modx.com/cla/). More information can be found [in this wiki](/community/contribute/becoming-a-contributor "Becoming a Contributor").</s>