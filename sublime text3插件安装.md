1.中文插件

​	（1）启动并进入sublime主界面，打开Sublime Text的控制台（快捷键 ctrl + ~）

​	（2）安装Package Control

```js
import urllib.request,os,hashlib; h = '6f4c264a24d933ce70df5dedcf1dcaee' + 'ebe013ee18cced0ef93d5f746d80ef60'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```

​	（3）点击菜单 Preferences -> Package Control，然后选择 Package Control：Install Package，稍等片刻过后会弹出命令界面，输入ChineseLocalization回车。等待安装成功

2.