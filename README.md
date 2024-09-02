# ecplugin-document-gradle-plugin

**[中文](README.md) | [English](README_en.md)**

本项目为 Gradle 插件，使用 markdown 编写文档，生成在线 html

详细说明请查看[在线文档](https://liuzhenghui.github.io/ecplugin-document-gradle-plugin/)

## 使用方法

```
plugins {
    id 'com.ecplugin.gradle.plugin.document' version '<version>'
}
```

执行 `gradle docBuild` 生成 html

## 方法

| task       | 说明                              |
|------------|---------------------------------|
| docInit    | 初始化 markdown 文档目录，在该目录下编辑 md 文档 |
| docBuild   | 将 *.md 文件转化为 html 文件            |
| docSummary | 查看文档大纲                          |
| docConfigs | 查看相关配置项                         |

## 配置参数

| 参数               | 说明                        |
|------------------|---------------------------|
| title            | 文档标题                      |
| description      | 文档描述                      |
| author           | 作者                        |
| copyright        | 版权说明                      |
| root             | 文档源文件目录(md文件目录)           |
| output           | html输出目录                  |
| keepSerialNumber | 是否保留源文件及目录的序号到 html 左侧目录树 |
| preview          | 执行`docBuild`后是否自动打开浏览器预览  |

默认配置:

```groovy
doc {
    title = '在线文档'
    description = '在线文档'
    author = 'ecplugin.com'
    copyright = 'Copyright &copy ecplugin.com'
    root = 'docs/'
    output = 'build/document/'
    keepSerialNumber = false
    preview = true
}
```

## 说明

1. 插件已发布至 Gradle Plugin Portal ，如提示下载失败，在`settings.gradle`增加配置如下:

```
pluginManagement {
    repositories {
        gradlePluginPortal()
        ...
    }
}
...
```
