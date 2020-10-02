# App
我们安装器的主体。
# 首页面
|工程|插件|
|---|---|
|ProjectNeptune|Example Extension 1.0<br>测试|
|用户本次打开的工程|工程安装了的插件|
# 菜单
|文件|
|---|
|打开工程|
|关闭工程|
|安装线上插件|
|安装本地插件|
|...|
|退出|

|插件|
|---|
|重新安装|
|卸载|
# 选择线上插件
选择哪个插件？

|插件|介绍|
|---|---|
|列表源|DokiMod 官方<br>...<br>添加源...|
|Example|真的没有什么 *NEW*(如果internalVersion大于本地同插件internalVersion的话)|

---
## 添加源

```
请填写这些文本框blahblah

名字 DankyModz
URL https://torito.org.cn.net.com.uk/~sixty-nine/dokimod-hell/zzz.json
```
完成后保存信息，在背后下载源然后显示出来就好了。

## 选择已有源
在某个地方（来一个JSON设置/注册表？）拿先前保存好的对应源信息，解析一下。
---

用户选择一个插件后我们就显示进度条，背后使用某下载器下载并解压插件。
# 后续
（如果使用本地插件，我们想要解压后的插件）
将插件文件夹先移动到 game 目录。

- 如果只有一种有效 override，执行仅有的类型相关的操作。（如果仅有 whole 类型，而且目录有其他的文件夹和 rpy* 文件，警告用户。）
- 如果插件有 add 和 whole 类型的 override，提示用户选择 override 类型。

|类型|特点|
|---|---|
|Add|不影响现有修改，但是某些情况下需要二次修改|
|Whole|替换文件，覆盖设置|

---

如果选择 Add，删除 whole 相关的文件；
如果选择 Whole，将 add 相关文件删除，whole 相关文件移动到 game 目录。
