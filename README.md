# Circle-ci
    持续集成Circle-ci

* 使用github登入Circle-ci

* Circle-ci会识别github仓库内部的文件夹

## 仓库根目录

* .circleci/config.yml

* 测试文件

* 源文件


## 教程:
    增加.circleci文件夹config.yml文件
    可以使得Circle-ci识别config.yml文件
```
# Javascript Node CircleCI 2.0 configuration file
#
# Check https://circleci.com/docs/2.0/language-javascript/ for more details
#
version: 2 //版本号
jobs:
  build:  
    docker:
      - image: circleci/node:10.8.0 //安装依赖
      
    steps:
      - checkout
      - run: npm install  //安装依赖
      - run: npm test     //文件测试
```