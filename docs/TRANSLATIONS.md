Implementation of TAPi18n on the first couple of pages (landing, home, and shared components (header, footer, ...)) is done in [#1819](https://github.com/Blockrazor/blockrazor/pull/1819).

As you can see, translation files have to be in the i18n folder and they have to have the .i18n.json or .i18n.yaml extension for JSON and YAML respectively. The language code (en for English, fr for French, sr for Serbian and so on) is prepended before the .i18n.json. A valid translation file name is home.en.i18n.json (for example).

When you change strings to translation keys in templates, _make sure that you scope translation keys properly_ (you can see how to do this in [#1819](https://github.com/Blockrazor/blockrazor/pull/1819)). If you don't do this you will cause problems if translation keys happen to be the same in multiple files, which is very likely. Using translations is as easy as using {{_ "translation_key"}} in templates. Although it's not very recommended, you can also use HTML in translation strings, but then you have to use three { ({{{_ "translation_key"}}}) in templates.