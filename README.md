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
