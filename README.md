# test-hugo-theme-docdock
Project to test the hugo theme *docdock* with the changed added to use Multilanguage.


## Only one language

When only one language is used you don't need to specify languages in any place: either the config file nor the contents, header or index files.

## Multilanguages

### Config

To use more than one language you need to specify which languages to use in the config file, for instance:

```
[Languages]
[Languages.en]
title = "Docdock test - En"
weight = 1
languageName = "English"

[Languages.es]
title = "Docdock test - Es"
weight = 10
languageName = "Español"
```


### Content

Content files have to specify the language in the filename, if the file doesn't specify it it is taken as the default language, for this example it is English so `some-content.md` will be shown when English is selected. However, if you prefer yo can specify the language: `some-content.en.md`.
In comparison, to show contents in another language, Spanish for this site, you have to specify it in the filename this way: `some-content.es.md`.

### Index and header

To show correctly the index and the header in the different languages you have to specify the language in the filenames, even for the default language so you'd need to add these files (for this example): 
- `_index.en.md`
- `_index.es.md`
- `_header.en.md`
- `_header.es.md`

And `_index.md` shouldn't exist.
