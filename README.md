# 利用etcd实现的分布式任务调度

因为项目已经上线，只能长传无关核心逻辑的部分代码，里面利用etcd的分布式锁+mongodb存储实现了分布式cron功能，非常好的实现
## 目录说明

### gopath


完整的项目开发环境，包括：源码+依赖库。


编译步骤：

* export GOPATH指向gopath目录的绝对路径
* 进入gopath/src/github.com/owenliang/下面的各个项目，执行go build编译得到二进制


### source

仅包含项目源代码，不包含依赖的第三方库，通常你用不到这个目录。


### thirdparty

项目依赖的第三方库。

原因是：自从开发之后，etcd与mongodb的SDK均发生不向下兼容的升级


创建包含第三方依赖的新项目步骤：

* mkdir 创建一个空目录
* export GOPATH指向这个空目录
* 在$GOPATH下面创建src目录
* 将thirdparty目录下的github.com完整拷贝到$GOPATH/src下


