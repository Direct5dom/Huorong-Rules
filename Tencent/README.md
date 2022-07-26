## 允许访问

- Tencent自己的目录。包括`TencentFiles`，聊天记录，多媒体，下载文件等；
- 微信的目录，聊天记录，多媒体，下载文件等；
- 部分系统目录，包括部分系统DLL (可能之后还会再精准一点) 、字体、图标缓存、Prefetch，等正常运行所需的目录/文件 (包括Flash，不需要可以自己关) 。

## 拒绝访问 (显式) 

- Chrome相关文件；
- `hosts`；
- 桌面 (主要读取了`lnk`，禁止了，看之后还读到啥再加) 一些会正常启动会被尝试读取，频繁弹提示的文件 (可有可无，不影响启动，使用的文件) ；
- 部分游戏平台的目录。

---

以上没有允许的，一概提示处理 (`AppData`可以参考另外一个规则，因为有误伤可能，只做了Chrome的显式拒绝，全盘拦截所以其他如遇到的会直接报提示处理)。

## 使用方法

火绒->防护中心->左下角高级防护->自定义防护 (注意启用，然后点文字进去) 

分别导入"自动处理规则" (`tencent-auto.json`) 、"自定义规则" (`tencent-custom.json`) ，启用即可。 (注意两个文件要分别在不同选项卡中导入，窗口顶部切换) 

**敲黑板，不要在弹出的提示内选择“记住本次操作”，否则会对所有文件生效。如有需要修改可以至自动处理规则内添加。**
