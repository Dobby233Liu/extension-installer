# 列表源
**列表源**是一系列由远程服务器提供的 JSON 数组，内含关于一些插件的信息。
# App 内的使用
用户在“选择列表”下拉选项框内选择任意用户添加或者应用内置的源（默认选择官方插件列表），然后 App 下载相关列表源的数据，提供给 JSON 库解析，完成后使用获得的信息在“下载插件”界面内显示插件。
```
extInfo.name       extNew?"*NEW*":""
    extInfo.description
```
（当然，还会 truncate）
# 格式（p-code）
```javascript
[
  {
    "name": "Example", // 插件名字，字符有限
    "internalName": "dokimod-neptune-example", // 检测本地版本
    "version": "1.0.0", // 简洁的 semver，可能不会实装
    "internalVersion": 1, // 检测本地版本
    "description": "插件紧缺，帮帮我们", // 我们需要很短的简介，最多也只有 20 字左右
    "archiveUrl": "https://example.com/dokimod/data/netpune-example-1.zip", // 可下载的 zip 地址，内部结构需要符合 Example Extension 的格式。可能会支持其他格式。
    "depth": 0 // 防止 codeload.github.com 套文件夹
  },
  ...
]
```
