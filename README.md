# TYPO3 Extension rte_ckeditor_iframe

A simple extension to integrate [IFrame Dialog](https://ckeditor.com/cke4/addon/iframe) into TYPO3's default editor ckeditor.

## Installation

* `composer require svenjuergens/rte-ckeditor-iframe`
* Install extension via extension manager in the backend

### Set yout RTE Preset in PageTS
```
RTE.default.preset = default+iframes
```

### SET TypoScript
```
lib.parseFunc_RTE.externalBlocks := addToList(iframe)
```

### Manuel Insert

Add the 2 necessary files to your Default.yaml file (have a look at rte_ckeditor_iframe/Configuration/RTE/Default.yaml)

```yaml
imports:
...
  - { resource: "EXT:rte_ckeditor_iframe/Configuration/RTE/Processing.yaml" }
  - { resource: "EXT:rte_ckeditor_iframe/Configuration/RTE/Plugin.yaml" }
```
and then it's important to have the toolbarGroups ```insert``` active

```yaml
editor:
    toolbarGroups:
      ...
      - { name: insert, groups: [ insert ] }
```
optional remove other buttons from toolbarGroup ```insert```:

```yaml
    removeButtons:
        ...
      - Table
      - HorizontalRule
      - SpecialChar
```
