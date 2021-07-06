## lerna开发脚手架
### 脚手架项目初始化
  1. 初始化npm项目
  1. 安装lerna
  1. lerna init 初始化项目*

### 创建package
  1. lerna create 创建Package*
  1. lerna add 安装依赖
  > lerna add默认是给packages下所有包安装依赖，若要给某包单独安装，方法实例(给packeges/core/安装@lerna-cli-dg-dev/util)： `lerna add @lerna-cli-dg-dev/util packeges/core/`
  1. lerna link 链接依赖

### 脚手架开发和测试
  1. lerna exec执行shell脚本
  > lerna exec默认在packeges所有包下执行命令，在某包下单独执行(在core包下删除依赖包)：`lerna exec --scope @lerna-cli-dg-dev/core rimraf node_modules`
  1. lerna run 执行npm命令*
  > 认在packeges所有包下执行命令; 单包：lerna run test --scope @lerna-cli-dg-dev/utils
  1. lerna clean 清空依赖
  1. lerna bootstrap 重装依赖

### 脚手架发布上线
  1. lerna version bump version
  1. lerna changed 查看上版本以来所有变更
  1. lerna diff 查看diff
  1. lerna publish 项目发布*

## lerna源码分析
