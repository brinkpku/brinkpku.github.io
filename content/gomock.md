## 概述
mock 是一种测试方法，主要是通过对interface的模拟实现，达到模拟复杂依赖项的目的，如数据库连接、文件io等逻辑。

## 安装
> go get -u github.com/golang/mock/gomock 
>
> go get -u github.com/golang/mock/mockgen # 生成mock代码工具

## 使用示例
待测试code<sup>[1]</sup>
```go
// db.go
package main

type DB interface {
	Get(key string) (int, error)
}

func GetFromDB(db DB, key string) int {
	if value, err := db.Get(key); err == nil {
		return value
	}
	return -1
}
```

生成测试需要依赖的mock代码
> mockgen -source=db.go -destination=db_mock.go -package=main

编写测试代码<sup>[2]</sup>
```go
func TestGetFromDB(t *testing.T) {
	ctrl := gomock.NewController(t)
	defer ctrl.Finish() 

	m := NewMockDB(ctrl)
	m.EXPECT().Get(gomock.Eq("Tom")).Return(100, errors.New("not exist"))

	if v := GetFromDB(m, "Tom"); v != -1 {
		t.Fatal("expected -1, but got", v)
	}
}
```

reference:  
[1]. [gomock](https://geektutu.com/post/quick-gomock.html) 

[2]. <https://www.jianshu.com/p/598a11bbdafb>
