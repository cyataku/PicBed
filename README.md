# PicBed
# PicGo + GitHub 搭建个人图床工具

# 1.Github仓库的设置

> 流程：新建 public 仓库 -> 创建 token -> 复制 token 备用


## 1.1新建仓库

点击 git 主页右上角的 `+` 创建 `New repository`；



填写仓库信息，例如我就创建了一个 `cloudimg` 的仓库。这里注意，仓库得设置为 `Public` 因为后面通过客户端访问算是外部访问，因此无法访问 `Private` ，这样的话图片传上来之后只能存储不能显示。所以要设置为 `Public`。

![](https://imgconvert.csdnimg.cn/aHR0cHM6Ly9yYXcuZ2l0aHVidXNlcmNvbnRlbnQuY29tL3llZmNpb24vUGljRGF0YS9tYXN0ZXIvaW1nLzIwMTkwMzExMjIyNTE0LnBuZw#alt=img)

## 1.2 创建 token 并复制保存

此时仓库已经建立，点击右上角头像，然后进入设置；

![](https://imgconvert.csdnimg.cn/aHR0cHM6Ly9yYXcuZ2l0aHVidXNlcmNvbnRlbnQuY29tL3llZmNpb24vUGljRGF0YS9tYXN0ZXIvaW1nLzIwMTkwMzExMjIyOTI1LnBuZw#alt=img)

在页面最下找到 `Developer settings`，点击进入；

![](https://imgconvert.csdnimg.cn/aHR0cHM6Ly9yYXcuZ2l0aHVidXNlcmNvbnRlbnQuY29tL3llZmNpb24vUGljRGF0YS9tYXN0ZXIvaW1nLzE1NTIzMTQ2OTEyMzIucG5n#alt=img)

创建 `token`；

![](https://imgconvert.csdnimg.cn/aHR0cHM6Ly9yYXcuZ2l0aHVidXNlcmNvbnRlbnQuY29tL3llZmNpb24vUGljRGF0YS9tYXN0ZXIvaW1nLzIwMTkwMzExMjIzMzE3LnBuZw?x-oss-process=image/format,png#alt=img)

填 description（也是随心填），勾选复选框 repo ，接着到页面底部 `Generate token` 就完成了；

![](https://imgconvert.csdnimg.cn/aHR0cHM6Ly9yYXcuZ2l0aHVidXNlcmNvbnRlbnQuY29tL3llZmNpb24vUGljRGF0YS9tYXN0ZXIvaW1nLzE1NTIzMTQ5MDc3OTQucG5n?x-oss-process=image/format,png#alt=img)

然后复制生成一串字符 token，这个 token 只出现一次，所以要保存一下。



# 2. PicGo 客户端配置

## 2.1 下载&安装

PicGo是开源的图床工具，非常优秀。可以到 [Github](https://github.com/Molunerfinn/PicGo/releases)下载。

## 2.2配置

先上图

![](https://imgconvert.csdnimg.cn/aHR0cHM6Ly9yYXcuZ2l0aHVidXNlcmNvbnRlbnQuY29tL3llZmNpb24vUGljRGF0YS9tYXN0ZXIvaW1nLzIwMTkwMzExMjI0NDQzLnBuZw#alt=img)

- 仓库名 即你的仓库名
- 分支名 默认 `master`
- Token 就是刚刚复制的那一串字符
- 存储路径 这个可以填也可以不填，填了的话图片就上传到 git 中 data 这个文件夹
- 域名`https://raw.githubusercontent.com/yefcion/cloudimg/master`这个要改一下 格式`https://raw.githubusercontent.com/[username]/[仓库名]/master`

然后点确定就可以了

> 注：这里提供一个加速访问图片的方法：CDN加速，具体原理自行百度（我还不是很懂）

将上面的域名改为：

原 [https://raw.githubusercontent.com/yefcion/cloudimg/master](https://raw.githubusercontent.com/yefcion/cloudimg/master)

现 [https://cdn.jsdelivr.net/gh/yefcion/cloudimg@master](https://cdn.jsdelivr.net/gh/yefcion/cloudimg@master)


然后关于上传的快捷键设置。默认的是 Mac 按键，推荐改成 `Ctrl + alt +c`。

![](https://imgconvert.csdnimg.cn/aHR0cHM6Ly9yYXcuZ2l0aHVidXNlcmNvbnRlbnQuY29tL3llZmNpb24vUGljRGF0YS9tYXN0ZXIvaW1nLzIwMTkwMzExMjI0OTM1LnBuZw#alt=img)

> 综上，操作完成。

> 本方案唯一缺点，不能私人。但是考虑到 GitHub 上传的图在列表里没法预览，应该没人会闲着没事翻记录。

> 来源:[yefcion](https://blog.csdn.net/yefcion/article/details/88412025)

