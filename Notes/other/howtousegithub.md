
---
layout: default
---

[返回主页](../../.)

### 上传我们的第一个github代码

*   这里以Linux系统为例子


1.  登录自己的github账号，在repositories创建一个new issue。
2.  然后进入自己新创的issue，复制下载指令，（在电脑中待下载的位置）打开终端输入下载指令。

  git clone + 下载代码（最好是ssh）
  
3.  随后在下载好的文件夹中加入自己需要上传的代码。
4.  进入拉取文件下的目录，打开终端，输入：

  git add *
  
  代表更新全部内容
5.  随后输入

  git commit -m "update”

  代表完成更新。
6.  最后输入
  
  git push origin main
  
  表示push到远程的main分支上。如果下载的时候用的是ssh方法，则此步骤不需要输入账号和密码。如果用的是http，则需要。
  
  上传成功后就会看到在GitHub上对应的profile会更新，而且前面的更新说明有update也会出现在这里

#### 一些注意事项

1.  团队合作（多人同时开发）时，需要在第6步骤前增加一个拉取操作，保证上传无遗漏。输入

  git pull

  拉取当前分支最新代码

2.  在第6步骤中不想输入密码，可以选择更改远程方式（http改为ssh）

  git remote -v   （查看当前远程方式）

  git remote rm origin   （移除旧的远程方式）

  git remote add origin + 复制并粘贴ssh下载代码   （添加新的远程方式，这里+不输入，仅表示and）

3.  查看当前仓库的状态：

  git status
