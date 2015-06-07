# Packages

### Install Package Control

安装好 Sublime 之后，通过安装 [Package Control](https://packagecontrol.io/) 来管理其大量的插件。

  * 打开 Sublime Text 然后按 `ctrl + `` 打开控制台
  * 粘贴下面的代码到控制台，然后回车


    import urllib.request,os,hashlib; h = '7183a2d3e96f11eeadd761d777e62404' + 'e330c659d4bb41d3bdf022e94cab3cd0'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)

待 Package Control 安装完成之后，用 `cmd + shift + p` 打开命令面板输入 `PC` 即可看到和 Package Control 相关的选项。紧接着就可以安装（管理）各种插件了。
