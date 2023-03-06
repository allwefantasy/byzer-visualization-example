## Byzer Visualization Example

本项目主要演示 Byzer-yaml 的可视化能力。视频演示： https://m.bilibili.com/video/BV1ct4y1V7BC

## 安装 Byzer 桌面版


[安装教程](https://zhuanlan.zhihu.com/p/603399058)


## 安装可视化插件

打开任意一个 .mlsqlnb 文件，然后新建一个 cell 执行如下代码（需要联网）：

```
!plugin app add - "byzer-yaml-visualization-3.3"; 
```

卸载：

```
!plugin app remove  "byzer-yaml-visualization-3.3";
```

## 引擎配置

拷贝 `.mlsql.config.example` 为 `.mlsql.config` 在里面用户可以配置内存。

## Python 环境

Byzer-yaml 可视化依赖于 Byzer-python。 用户需要在本机安装 [Miniconda](https://docs.conda.io/en/latest/miniconda.html)。

> 注意：你可能根据需要修改 enviroment-*.yml 文件中的 prefix 字段。

Mac/Linux 还原Python虚拟环境：

```
conda env create --file environment-mac.yml
```

这样可以得到一个名字叫做 `ray-1.12.0` 的环境。


Windows 下还原 Python 虚拟环境：

```
conda env create --file environment-win.yml
```
我们可以得到一个名字叫 `dev` 的环境。

## 使用说明

用户可以直接打开 ./src/visual.mlsqlnb cell by cell 操作。我们已经把数据提前防止在 data目录中，并且以 delta lake 形式提供。


## 项目文件说明

### ./src/plugin.mlsqlnb

执行该 Notebook 安装 Byzer 可视化插件。

### ./src/prepare-data.mlsqlnb

这个文件主要是把一些 Python 库里的示例数据导出到 Byzer 存储中。

### ./src/basic_usage.mlsqlnb 

Byzer 的一些基础语法特性介绍。

### ./src/story2.mlsqlnb

使用 Byzer-python进行可视化

### ./src/story1.mlsqlnb

使用 Byzer-yaml 进行可视化

### ./src/visual.mlsqlnb

绘制各种图示例