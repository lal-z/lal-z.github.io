---
title: 搭建hexo记录
thumbnail: /images/3123.jpg # 略缩图
categories: 记录 # 分类
---
Welcome to [Hexo](https://hexo.io/)! This is your very first post. Check [documentation](https://hexo.io/docs/) for more info. If you get any problems when using Hexo, you can find the answer in [troubleshooting](https://hexo.io/docs/troubleshooting.html) or you can ask me on [GitHub](https://github.com/hexojs/hexo/issues).

## Quick Start

### Create a new post

``` bash
$ hexo new "My New Post"
```

More info: [Writing](https://hexo.io/docs/writing.html)

### Run server

``` bash
$ hexo server
```

More info: [Server](https://hexo.io/docs/server.html)

### Generate static files

``` bash
$ hexo generate
```

More info: [Generating](https://hexo.io/docs/generating.html)

### Deploy to remote sites

``` bash
$ hexo deploy
```

More info: [Deployment](https://hexo.io/docs/one-command-deployment.html)

### 搭建流程
#### 安装hexo脚手架-初始化-本地启动-下载主题
``` bash
$ npm install -g hexo-cli
$ hexo init hexo-blog
$ hexo s
$ git clone theme地址 themes/theme名字
```
#### 修改根目录下_config.yml 文件 中的 'theme' 变量为 'theme名字'

#### 连接github-新建仓库（注：名字一定要跟账户名一致.github.io）
``` bash
$ git init
$ git remote add origin https://github.com/xxx/xxx.github.io.git(使用https链接)
```
#### 修改根目录下_config.yml 文件
> deploy:
  type: git
  repo: https://github.com/xxx/xxx.github.io
  branch: master
#### 使用hexo 打包部署
``` bash
$ yarn add/npm install hexo-deployer-git
$ npm run deploy/hexo deploy
```
#### 之后仓库的settings-Github Pages中就有已经发布了博客地址
> master上打包的是public下的产物 so~~项目源码要新建一个分支进行存放
    点击vscode 左下角-选择新建分支myFile
    将myFile push 到远程上游的地址 git push --set-upstream origin myFile
    ---git remote  查看远端仓库名字---
    ---git remote rm 远端仓库名字  删除远端仓库---
#### 配置gitHub actions
> 根目录下创建 .github/workflows/deploy.yml文件
  修改例子里的md文件 界面就有相应的变化
  提交更改的文件
   
``` bash
$ git add.
$ git commit -m 'change'
$ git push
```
> 文件已经更改


