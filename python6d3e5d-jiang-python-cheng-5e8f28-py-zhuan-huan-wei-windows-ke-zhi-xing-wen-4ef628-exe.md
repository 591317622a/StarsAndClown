#### python开发者向普通windows用户分享程序,要给程序加图形化的界面 传送门:[这可能是最好玩的python GUI入门实例! ](http://www.jianshu.com/p/8abcf73adba3),并要将软件打包为可执行文件(.exe结尾),如何将.py转为.exe ?


> ![将.py转为.exe](https://raw.githubusercontent.com/zhaoolee/GraphBed/master/StarsAndClown/b9fd540ea3884155a8dbeb5f77a97da5.png)


## 第一步:安装pyinstaller(临时调用了国内豆瓣镜像源,这样下载比较快)

` pip install pyinstaller -i https://pypi.douban.com/simple`

## 第二步:更改编码方式(window用户专用)
> 由于windows默认编码是gbk,而我们的开发环境(unix环境)默认编码使用utf-8,为解决编码问题,我们需要对pyinstaller源码进行一些修改

> ![修改读取方式为:utf-8](https://raw.githubusercontent.com/zhaoolee/GraphBed/master/StarsAndClown/101a0305a0534556862791cd1fe25e3c.png)
将`pyinstaller`中winmainifest.py中的第1075行,修改为`with open(filename,encoding="UTF-8") as f:  `

> `winmainifest.py`的位置:`C:\Program Files (x86)\Python36-32\Lib\site-packages\PyInstaller\utils\win32\winmanifest.py`,如果找不到,可以先尝试第三步,如果转换过程报错,会打印出这个文件在本机的位置.
如果权限不够，无法保存修改，可以先将修改后的文件,保存到桌面(保持原来的文件名)，用桌面的文件替换原目录中的文件即可!


## 第三步:将.py转换为.exe

＞ 这里以｀Python GUI入门实例｀为例（Python GUI入门实例传送门：http://www.jianshu.com/p/8abcf73adba3）

命令:`pyinstaller --onefile 011根据ip查询地理位置.py`
![创建打包为.exe文件](https://raw.githubusercontent.com/zhaoolee/GraphBed/master/StarsAndClown/6c8982e3c2cb49aea6a6f9d05fd62462.png)



# 第四步:运行测试


> ![编译后的目录](https://raw.githubusercontent.com/zhaoolee/GraphBed/master/StarsAndClown/f2c5f789a3fa415cbf1fa6808396cb92.png)

> 生成的.exe文件在dist文件夹内

#### 将数据库文件GeoLiteCity.dat拷贝到dist文件夹中


> ![完整的程序](https://raw.githubusercontent.com/zhaoolee/GraphBed/master/StarsAndClown/804605c7bc35491fa37cbd86fba43a25.png)

#### 运行可执行文件(.exe)


> ![以管理员身份运行](https://raw.githubusercontent.com/zhaoolee/GraphBed/master/StarsAndClown/07057ea5b04547dbb8168708a30408bd.png)


> ![成功运行效果](https://raw.githubusercontent.com/zhaoolee/GraphBed/master/StarsAndClown/246ce0e1939e40249bfcb65d3605bd36.png)

---
#### 本仓库Github链接: [https://github.com/pyinstaller/pyinstaller](https://github.com/pyinstaller/pyinstaller)

---

## 写在最后(我需要你的支持)
- 本文属于**Github星聚弃疗榜** 项目的一部分, 项目Github地址: [https://github.com/zhaoolee/StarsAndClown](https://github.com/zhaoolee/StarsAndClown)

- **Github星聚弃疗榜**, 为Github优秀创意项目写一封推荐信，让Github优秀项目造福人类~, 如果你喜欢这个项目, 希望你能为本项目添加一颗 🌟星.

- StarsAndClown, Write a letter of recommendation for Github's outstanding creative projects, and let Github's outstanding projects benefit mankind~, If you like this project, I hope you can add a star 🌟 to this project.




