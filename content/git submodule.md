### git submodule

### 背景 ###
Git 工具的 submodule 功能就是建立了当前项目与子模块之间的依赖关系：子模块路径、子模块的远程仓库、子模块的版本号。

### 命令 ###

#### 创建子模块 ####

使用 `git submodule add <submodule_url>` 命令可以在项目中创建一个子模块。

#### 获取子模块 ####

如果希望子模块代码也获取到，一种方式是在克隆主项目的时候带上参数 `--recurse-submodules`，这样会递归地将项目中所有子模块的代码拉取。

另外一种可行的方式是，在当前主项目中执行：

``` shell
git submodule init
git submodule update
``` 