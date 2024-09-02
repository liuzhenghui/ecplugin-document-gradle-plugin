# ecplugin-document-gradle-plugin

**[Chinese](README.md) | [English](README-en.md)**

This project is a Gradle plugin that uses markdown to write documents and generate online HTML

document: https://liuzhenghui.github.io/ecplugin-document-gradle-plugin/

## Usage

```groovy
plugins {
    id 'com.ecplugin.gradle.plugin.document' version '<version>'
}
```

`Gradle docBuild` to generate HTML

## Methods

| Task       | Description                                                                        |
|------------|------------------------------------------------------------------------------------|
| DocInit    | Initialize the markdown document directory and edit MD documents in this directory |
| DocBuild   | Convert *. md files to HTML files                                                  |
| DocSummary | View document outline                                                              |
| DocConfig  | View related configuration items                                                   |

## Configurations

| Parameter          | Description                                                                                                     |
|--------------------|-----------------------------------------------------------------------------------------------------------------|
| Title              | Document Title                                                                                                  |
| Description        | Document Description                                                                                            |
| Author             | Author                                                                                                          |
| Copyright          | Copyright Description                                                                                           |
| Root               | Document source file directory (md file directory)                                                              |
| Output             | HTML output directory                                                                                           |
| Keep Serial Number | Do you want to keep the sequence numbers of the source files and directories in the left directory tree of HTML |
| Preview            | Automatically open browser preview after executing ` docBuild `                                                 |

Default configuration:

```groovy
doc {
    Title = 'Online Document'
    Description = 'Online document'
    author = 'ecplugin.com'
    copyright = 'Copyright &copy ecplugin.com'
    root = 'docs/'
    output = 'build/document/'
    keepSerialNumber = false
    preview = true
}
```

## Explanation

1. The plugin has been released to Gradle Plugin Portal. If it prompts download failure, add the following configuration in ` settings. gradle `:

```groovy
pluginManagement {
    repositories {
        gradlePluginPortal()
        ...
    }
}
...
```