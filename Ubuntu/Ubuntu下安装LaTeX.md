## 安装texlive

```
使用图形化安装：sudo apt install perl-tk
将texlive.iso复制到home下
使用mount命令挂载到mnt:sudo mount -o loop texlive.iso /mnt
移动到mnt下: cd /mnt
运行（以图形化）：sudo ./install-tl -gui
按照步骤安装
选择安装方案。初级用户推荐直接选择 scheme-full 全部安装。如果磁盘空间有限也可以选择small或者median模式。高级用户可以选择scheme-custom进一步定制。这里我选择了scheme-custom，并且在“进一步定制”里去掉了自己不会用到的一些语言包和ConTeXt相关组件。
由于这里是安装到系统里，因此portable setup选择了否，安装路径为默认。
选项里面选择默认为A4纸张大小，其它一些选项基本都选了是。其中要注意的是创建符号链接会在 /usr/local/bin里面创建指向可执行程序的软链接，从而可以直接使用latex,pdflatex等命令，此外还可以使用man latex等命令查看帮助。
建议在最后的get package updates一项选否，等安装好了之后手动安装更新。
最后卸载镜像文件：sudo umount /mnt
```

## 安装texstudio
直接在网上下载deb包然后安装就好了,推荐一个好的软件——GDEbi.

## texstudio的配置
在`选项`中选`设置TeXStudio`,可以先把语言调好(选择zh-CN).

选择`构建`,把默认编辑器改成`XeLaTeX`.

选择`命令`,在XeLaTeX中添加`-shell-escape -8bit`

然后就可以了.

## 参考资料
[sycstudio的文档](https://github.com/SYCstudio/Vnote/blob/master/oi/%E5%85%B6%E5%AE%83/Ubuntu%E6%93%8D%E4%BD%9C%E8%AE%B0%E5%BD%95.md#%E4%B8%BB%E4%BD%93%E5%AE%89%E8%A3%85)
