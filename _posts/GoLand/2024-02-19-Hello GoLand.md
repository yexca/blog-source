---
id: 154
layout: post
title: 'Hello GoLand'
author: yexca
date: 2024-02-19 07:58 +0800
permalink: /archives/154
categories:
    - 编程基础
    - 编程语言
tags:
    - Go
---

Go 下载：<https://go.dev/dl/>

JetBrains GoLand：<https://www.jetbrains.com/go/>

## Go 简介

Go 可以直接编译，直接运行即可部署，静态类型语言

```bash
# 直接运行
go run hello.go

# 编译
go build hello.go
# 编译后运行
./hello
```

Go 的一些应用

(1)、云计算基础设施领域

代表项目：docker、kubernetes、etcd、consul、cloudflare CDN、七牛云存储等

(2)、基础后端软件

代表项目：tidb、influxdb、cockroachdb 等

(3)、微服务

代表项目：go-kit、micro、monzo bank的typhon、bilibili 等

(4)、互联网基础设施

代表项目：以太坊、hyperledger 等

## Hello Go

```go
package main	// 定义包名
/* 
 * 必须在源文件非注释第一行指明文件属于哪个包
 * main 表示一个可独立执行的程序，每个 Go 应用程序都包含一个名为 main 的包
 */

import "fmt"	// 导入 fmt 包，实现了格式化 IO 的函数

func main(){	// 函数
    fmt.println("Hello Go")
}
```

一般 mian 函数是启动后第一个执行的函数，如果有 init 函数会先执行该函数

> 定义函数时，`{` 必须与函数名在同一行