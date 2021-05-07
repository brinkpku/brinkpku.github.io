## 概述
mock 是一种测试方法，主要是通过对interface的模拟实现，达到测试复杂依赖项的目的，如数据库连接、文件io等。

## 安装
> go get -u github.com/golang/mock/gomock 
>
> go get -u github.com/golang/mock/mockgen

> mockgen -source=db.go -destination=db_mock.go -package=main

## 使用示例



reference: [gomock](https://geektutu.com/post/quick-gomock.html)