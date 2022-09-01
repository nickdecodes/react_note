# react基础环境安装

## 依赖安装

### [npm、node.js官网安装](https://nodejs.org/)

npm升级

```bash
sudo npm install -g npm to update
#使用淘宝镜像
npm install -g cnpm --registry=https://registry.npm.taobao.org
```

node.js升级

```bash
#第一步，先查看本机node.js版本：
node -v
#第二步，清除node.js的cache：
sudo npm cache clean -f
#第三步，安装 n 工具，这个工具是专门用来管理node.js版本的，别怀疑这个工具的名字，是他是他就是他，他的名字就是 "n"
sudo npm install -g n
#第四步，安装最新版本的node.js
sudo n stable
#第五步，再次查看本机的node.js版本：
node -v
#第六步，更新npm到最新版：
sudo npm install npm@latest -g
```

### [npm、node.js卸载](https://nodejs.org/)

```bash
在 node 官网上下载的安装包，用安装包安装的node.应该可以用一下命令行卸载：
在终端输入以下命令：
sudo rm -rf /usr/local/{bin/{node,npm},lib/node_modules/npm,lib/node,share/man/*/node.*}

1.删除/usr/local/lib中的所有node和node_modules
2.删除/usr/local/lib中的所有node和node_modules的文件夹
3.如果是从brew安装的, 运行brew uninstall node
4.检查~/中所有的local, lib或者include文件夹, 删除里面所有node和node_modules
5.在/usr/local/bin中, 删除所有node的可执行文件
6.最后运行以下代码:(可能具体安装路径会有区别 ,find ~ -name "node"   可以找到所有

sudo rm /usr/local/bin/npm
sudo rm /usr/local/share/man/man1/node.1
sudo rm /usr/local/lib/dtrace/node.d
sudo rm -rf ~/.npm
sudo rm -rf ~/.node-gyp
sudo rm /opt/local/bin/node
sudo rm /opt/local/include/node
sudo rm -rf /opt/local/lib/node_modules
```

### npm、node.js brew安装

```bash
brew install node
brew install watchman
brew install flow
```

```bash
#安装一个 全部安装node.js npm
brew install node
#使用nrm工具切换淘宝源
npx nrm use taobao

#如果之后需要切换回官方源可使用
npx nrm use npm
#Yarn是 Facebook 提供的替代 npm 的工具，可以加速 node 模块的下载。
npm install -g yarn
```

### nvm包管理工具

```bash
brew install nvm
#安装成功
==> Summary
🍺 /usr/local/Cellar/nvm/0.33.11: 7 files, 138.6KB, built in 13 seconds
```

安装成功之后，还不能直接使用nvm命令，需要进行以下配置，将以下命令复制到终端执行：

```bash
echo "source $(brew --prefix nvm)/nvm.sh" >> .bash_profile
. ~/.bash_profile
nvm list
#👌
```

## 基础学习

### react特点

- 声明式

    > 声明式：不直接操作DOM，我只是声明一下数据去哪里
    >
    > 命令式：直接操作DOM

- 组件化

    > 模块化：js
    >
    > 组件：页面上一个资源的功能代码+资源整合
    >
    > 组件化：创建拥有各自状态的组件，再由这些组件构成更加复杂的 UI

- 一次学习，随处编写

    > react-native

