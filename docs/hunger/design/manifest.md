# Manifest
**Manifest** 是提供给 App 的一系列信息，它会使用 JSON 格式。
目前使用还比较基础。

文件应存放于 `/extensions/?/manifest.json`。
# App 内使用
请看 [App 的文档](https://github.com/Dobby233Liu/extension-installer/blob/master/docs/hunger/design/README.md#%E9%A6%96%E9%A1%B5%E9%9D%A2)。
# 格式（p-code）
```javascript
{
  "name": "damn",
  "description": "youre out of luck",
  "version": "6.9.0",
  "internalVersion": 69,
  "author": "Dobby233Liu",
  "port": false // 是否是移植
}
```
