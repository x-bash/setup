# setup

Setup the softwares in on line.

```bash
curl https://x-bash.github.io/setup/kubectl | bash
curl https://x-bash.github.io/get/kubectl | bash

@src setup/kubectl
```

## using @setup

```bash
@src setup/init

@setup kubectl  # @src setup/kubectl
@setup docker   # @src setup/docker
@setup k8s
@setup pvm
```

## Docker化以及与static-build的关系

docker的普及，某种程度降低了这个工具的使用。可以将待安装的应用分成两类：

1. 需要系统级别的安装
2. 直接安装在用户目录，如同绿色软件，例如kubectl，docker命令行

对于第一类，我们尽量处理成docker化，虽然带来一定的不便利性，但胜在安全
关于第二类，我们一般回去软件库里面找寻，但有时候为了避免安装过多的系统依赖，会直接从static-build这个项目里面获取相关的版本。

static-build还有一个目标，就是将相关的软件版本和二进制都尽量地做一个备份，并同时在gitee等个类似的公开提供商（譬如阿里云，腾讯云）进行备份。

我们的脚本库将存放对应二进制代码的md5。
