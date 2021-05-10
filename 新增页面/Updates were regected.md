有些协同办公开发的时候，还是使用GIT版本控制比较好一些，而且有些开源的软件提供下载发布在GITHUB或者GITEE上容易版本的迭代，否则每次都要重新打包最新版本发布压缩包。但是前者由于在国内的速度不好，所以老蒋最近开始准备使用GITEE。

在推送版本更新的时候有出现：

> error: failed to push some refs to 'https://gitee.com/\*\*\*/\*\*\*\*.git'  
> hint: Updates were rejected because the tip of your current branch is behind  
> hint: its remote counterpart. Integrate the remote changes (e.g.  
> hint: 'git pull ...') before pushing again.  
> hint: See the 'Note about fast-forwards' in 'git push --help' for details.

出现这样的问题，应该是没有在本地修改文件和同步保存，而是直接在GITEE上面删除和修改文件导致的，导致文件不对等。那我们这里采用一个办法，直接确保是文件没有问题的，直接强行推送过去更新、

> git push -f origin master

这里我们要谨慎使用，确保你要更新的是对应的。他的错误提醒是善意的，因为确实发现你文件不对等。

