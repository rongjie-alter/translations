## How to contribute (for translators)

Edit `translations/<locale>/<filename>.tsv`.

### Note

Don't edit files in `master-data/`, these files are generated by program.

---

## Workflow (for developers)

1. Export first series **.tsv** files that based on ja-JP master data
    * Tool: `translate-gen-tsv`
2. Upload to Google Drive, then create sheets by different datatype and locale
    * example sheets: `skills-ja_JP`, `skills-zh_TW`, etc.
3. Translate (edit) on the sheets
4. Download the translated data from cloud
    * Tool: `download-translation-tsv`
5. Export formatted data
    * Toold: `translate-gen-master-json`
6. Update main project

---

## Tools (for developers)

### download-official-master-data

Download official master data (**ja-JP**) with current version.

```shell
yarn download:official-master-data
```

### translate-gen-tsv

Convert the JSON of **ja-JP** master data into **.tsv** files.

```shell
yarn translate:gen-tsv
```

### download-translation-tsv

Download translated **.tsv** files from cloud.

```shell
yarn download:translation-tsv
```

### translate-gen-master-json

Transform translated **.tsv** files to master data JSON.

```shell
yarn translate:gen-master-json
```
