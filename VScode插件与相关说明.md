1.相似Sublime Text插件 Sublime Text Keymap and Settings Importer

![image-20201128155057562](C:\Users\raisound\AppData\Roaming\Typora\typora-user-images\image-20201128155057562.png)

2.php语法检查和补全插件，需要先下载php到C盘，然后输入php安装推荐的相关插件



3.代码区域放大缩小

​	文件 --> 首选项 --> 设置 --> 搜索‘用户设置’ --> settings.json

​	editor.mouseWheelZoom": true,



4.HTML配置补全插件

安装HTML Snippets

​	文件 --> 首选项 --> 设置 --> 搜索‘用户设置’ --> settings.json

加入以下代码

```json
 "files.associations": {

​    ".vue": "html"

  },

  "emmet.triggerExpansionOnTab": true,

  "emmet.includeLanguages": {

​    "vue-html": "html",

​    "vue": "html"

  }
```

5.远程服务端到目录到本地

​	（1）先安装sftp插件，然后打开Ctrl+Shift+P打开命令端口输入：sftp.json配置相关参数

​				

```json
{
    "name": "api.raisound.com", //服务器名称
    "host": "api.raisound.com", //服务器地址
    "protocol": "sftp",
    "port": 22,
    "username": "root",
     "password": "Imsl86329312",
    "remotePath": "/home/www/api.datashenzhen.ne  //需要同步的远端服务器
    "uploadOnSave": true
}
```

