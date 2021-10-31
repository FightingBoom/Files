时间：2021年10月27日23:18:57

[TOC]

# 1 参考资料

&emsp;&emsp;在准备考试过程中，参考了很多资料，非常感谢各位前辈的帮助。整理资料链接如下：

- [【鲲鹏HCIA考试】错题集（https://blog.csdn.net/qq_44745905/article/details/108725463）](https://blog.csdn.net/qq_44745905/article/details/108725463)

- [鲲鹏云HCIA知识总结（一）（https://blog.csdn.net/qq_43531669/article/details/105271419）](https://blog.csdn.net/qq_43531669/article/details/105271419)

- [鲲鹏云HCIA知识总结（二）（https://blog.csdn.net/qq_43531669/article/details/105361593）](https://blog.csdn.net/qq_43531669/article/details/105361593)

- [华为鲲鹏 HCIA 专栏（https://blog.csdn.net/qq_44826711/category_10616182.html）](https://blog.csdn.net/qq_44826711/category_10616182.html)

&emsp;&emsp;这位前辈的文章中有链接，可以进行模拟考试，尊重原创，谢谢前辈帮助！

- [华为鲲鹏HCIA-Kunpeng Application Developer V1.5考试样题（https://blog.csdn.net/qq_44826711/article/details/110579406）](https://blog.csdn.net/qq_44826711/article/details/110579406)

&emsp;&emsp;温馨提示：浏览器阅读文章时，可以使用<font color=#ff0000 size=4> `Ctrl + F` </font>快捷键搜索关键字。

&emsp;&emsp;本节主要总结自己学习过程中的笔记，分享讲义中的思考题，希望能对您有帮助！需要说明的是，培训的讲课内容是 V1.0 版本，但是在 2021 年之后，考试的版本为 V1.5 版本。从我自己考试的情况来看，V1.0 版本的内容在 V1.5 版本中，大概占比为 **60% ~ 70%** 。



# 2 笔记分享

## 2.1 鲲鹏生态介绍

### 2.1.1 计算产业发展趋势

&emsp;&emsp;简要总结本节知识点如下：

1、传统 PC 在往移动端迁移；

2、多种计算架构并存的组合是最优的解决路径；

3、文本、图片、语音、视频等数据，统称为 **非结构化数据** ；

4、计算分为两大类

   - 整型计算：文本处理，大数据分析；

   - 浮点计算：科学计算，视频处理；

5、Inter X86 架构设计，性能提升较难；



### 2.1.2 鲲鹏计算产业概述

&emsp;&emsp;简要总结本节知识点如下：

1、**鲲鹏计算产业** 是基于 Kunpeng 处理器构建的全栈 IT 基础设施、行业应用及服务，包括 PC 、服务器、存储、操作系统、中间件、虚拟化、数据库、云服务、行业应用以及咨询管理服务等。

2、**鲲鹏计算产业目标** 是建立完善的开发者和产业人才体系，通过产业联盟、开源社区、OpenLab、行业标准组织一起完善产业链，打通行业全栈，使鲲鹏生态成为开发者和用户的首选。

3、全自研服务器 TaiShan ，主要分为 5 大部分，具体如下：

   - **算**：鲲鹏 920，ARM 处理器芯片；
   - **存**：Hi1812 ，智能 SSD 控制芯片；
   - **传**：Hi1822 ，智能融合网络芯片；
   - **管**：Hi1710 ，智能管理芯片；
   - **智（ AI ）**：Ascend 310/910 ，人工智能芯片；达芬奇架构；

4、鲲鹏计算产业的典型应用

   - 大数据
   - 分布式存储
   - 数据库
   - 原生应用
   - 云服务

&emsp;&emsp;具体可参考下图：

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210123090502.png)


5、利用自己的优势，使能伙伴发展；

6、硬件开放，软件开源；

7、多路处理器意思是：一个服务器支持多路 CPU ；

8、95% 的安防行业都在使用海思芯片；

9、HDD：机械硬盘；SSD：固态硬盘；

10、为什么会有鲲鹏？

&emsp;&emsp;备胎转正，主要市场在中国；

11、优势：与 ARM 共享优势生态；

12、核数越多，并发数越高；



### 2.1.3 鲲鹏计算产业生态

1、鲲鹏计算产业生态全景

   - 技术生态；
   - 高校合作；
   - 产业生态；
   - 伙伴生态；
   - 社区建设；
   - 开发者生态；

2、华为鲲鹏伙伴计划

   - 华为鲲鹏 **凌云** 伙伴计划：华为云服务鲲鹏子计划；
   - 华为鲲鹏 **展翅** 伙伴计划：华为 TaiShan 服务器鲲鹏子计划；
   - 华为鲲鹏 **智数** 伙伴计划：华为智能数据 & 存储鲲鹏子计划；



### 2.1.4 思考题

1、华为鲲鹏计算产业相关产品有哪些？（ **ABC** ）

A. 华为鲲鹏处理器

B. TaiShan服务器

C. 华为云鲲鹏云服务

2、围绕鲲鹏计算产业，华为提供（ **ABCD** ）支持。

A. 云服务

B. 工具链

C. 社区服务

D. 专业服务



## 2.2 华为鲲鹏处理器介绍

### 2.2.1 华为鲲鹏处理器概述

&emsp;&emsp;华为鲲鹏处理器是华为自主研发的基于 ARM 架构的企业级系列处理器产品，包含 “算、存、传、管、智” 五个产品系统体系。

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210123092209.png)



### 2.2.2 华为鲲鹏处理器架构介绍

1、华为鲲鹏处理器基于 ARM 架构。ARM 是一种 CPU 架构，有别于 Intel 、AMD CPU 采用的 CISC 复杂指令集，ARM CPU 采用 RISC 精简指令集（ reduced instruction set computer ，精简指令集计算机）。

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210123092316.png)

2、ARM 是一家英国公司，**华为拿到了 ARMv8 最高级别永久授权**；授权级别分三层，由低到高分别是：

   - ARM
   - 架构
   - 指令集

3、两种指令集之间的区别

&emsp;&emsp;复杂指令集 CISC ：

- 英特尔开始没设计好，后面不断完善追加，长度不一样；
- 举例：吃饭这个动作，要先拿碗筷，再开始吃，吃完还要刷完等；

&emsp;&emsp;精简指令集 RISC：

- 类似吃饭，一个指令即可完成全部动作；

- 长度固定；**重要知识点！**

- 80% 场景提前了，加速处理；

4、华为鲲鹏处理器架构（ ARM ）特点

&emsp;&emsp;优点：

- 采用 ARM 架构，同样功能性能占用的芯片面积小、功耗低、集成度更高，更多的硬件 CPU 核具备更好的并发性能。

- 支持 16 位、32 位、64 位多种指令集，能很好的兼容从 IOT 、终端到云端的各类应用场景。

- 大量使用寄存器，大多数数据操作都在寄存器中完成，指令执行速度更快。

- 采用 RISC 指令集，指令长度固定，寻址方式灵活简单，执行效率高。

&emsp;&emsp;缺点：

- 在 **数据中心领域** 属于新进入者，其生态仍处于快速发展阶段。



### 2.2.3 华为鲲鹏处理器型号及规格介绍

1、华为鲲鹏 920 处理器规格

- 集成最多 64* 自研核，支持 64 核、48 核、32 核等多种型号
  - 指令集兼容 ARMv8.2 ，最高主频达 2.6GHz
  - 每核集成 64KB L1 I/D 缓存
  - 每核独享 512KB L2 缓存
  - 平均每核 1MB L3 cache
- 8 * DDR4 控制器，最高可达 2933MT/s
- 集成 PCIe/SAS 接口
  - 支持 PCIe 4.0 ，向下兼容 PCIe 3.0/2.0/1.0
  - 支持 x16，x8，x4，x2，x1 PCIe 4.0，集成 PCIe 控制器
  - 支持 16 * SAS/SATA 3.0 控制器
- 支持 CCIX 接口，支持加速器的缓存一致性
- 支持 2 * 100G RoCE v2 ，支持 25GE/50GE/100GE 标准 NIC
- 支持 2P/4P 扩展
- 封装大小：60mm * 75mm

2、华为鲲鹏 920 处理器性能

- 高性能
- 高吞吐
- 高集成
- 高能效



### 2.2.4 华为鲲鹏处理器技术创新

1、华为鲲鹏处理器技术创新

- 内核全自研
- 内存/网络接口 & IO协议
- 制程工艺领先
- 可靠性提升

2、内核全自研，性能提升

- 高性能
- 高集成；集成 RoCE 网卡、SAS 控制器、南桥、CPU ；
- 高能效
- 低能耗

3、内置多种加速引擎

- SSL 加速引擎
- 加解密加速引擎
- 压缩解压缩加速引擎



### 2.2.5 思考题

1、以下哪些关于华为鲲鹏 920 处理器的描述是正确的？（ **ABCD** ）

A. 采用了 7nm 的制造工艺；

B. 支持 8 通道的 DDR4 控制器；

C. 支持 PCIe 4.0 接口，并兼容 PCIe 3.0/2.0/1.0 ；

D. 支持多种加速器；

2、华为鲲鹏 920 处理器内置了哪些加速器？（ **ABC** ）

A. SSL 加速引擎

B. 加解密加速引擎

C. 压缩解压缩加速引擎



## 2.3 TaiShan 服务器

### 2.3.1 TaiShan 服务器概述

&emsp;&emsp;泰山服务器，TaiShan100 与 TaiShan200 对比：

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210123152525.png)

> 问：一个 CPU 最多支持 8 通道内存技术，为什么最多可支持 32 个 DDR4 内存？

&emsp;&emsp;如果一台服务器是 4 路 CPU，自然可以支持 32 个 DDR4 内存；如果一台服务器是 1路 / 2路 CPU，则就是在一路中加装内存，无非就是扩大容量而已，对性能提升没有太大帮助。

&emsp;&emsp;自我理解一下就是，内存技术是 8 通道的，至于每个通道最多是可以接多少块内存条，只是扩大了每一路通道的内存容量而已，与通道数无关。



### 2.3.2 TaiShan200 机架服务器产品介绍

&emsp;&emsp;机架服务器全景图如下：

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210123154333.png)

&emsp;&emsp;部分说明如下：

- U：高度单位；1U = 4.445cm，2U = 8.89cm，4U = 17.78cm；
- 2 路：2 个 CPU；4 路：4 个CPU；

&emsp;&emsp;TaiShan200 机架服务器价值特性，主要是一些设计，结构，功能等方面的优势；



### 2.3.3 TaiShan200 高密服务器介绍

&emsp;&emsp;X6000 高密服务器，部分截图如下：

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210123154805.png)

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210123154812.png)



&emsp;&emsp;其他服务器类型介绍

- **ECS**：弹性云服务器，会智能调度；
- **BMS**：裸金属服务器，把底层应用资源全部分配给你使用；
- **BMC**：控制系统；



### 2.3.4 思考题

1、TaiShan 200 机架服务器包含哪些型号？（ **ABC** ）

A. 2280

B. 5280

C. 2480

D. X6000



## 2.4 服务器相关

1、华为鲲鹏伙伴计划

- 华为鲲鹏 **凌云** 伙伴计划：华为 **云服务** 鲲鹏子计划；
- 华为鲲鹏 **展翅** 伙伴计划：华为 **TaiShan服务器** 鲲鹏子计划；
- 华为鲲鹏 **智数** 伙伴计划：华为 **智能数据&存储** 鲲鹏子计划；
- 主要重点是：一云两翼双引擎

2、服务器不同型号，适用的不同场景

- 鲲鹏 920 ：适用于服务器
- 鲲鹏 920s ：适用于工作站
- 鲲鹏 920lite：适用于 PC

3、鲲鹏 920 内置 3 个加速引擎

- 内置 SSL 加速引擎
- 内置加密算法加速引擎
- 内置压缩引擎

4、2280E 弱于 2280；

5、水冷不是真的自来水，而是一种特殊介质的水，散热导热效率比较好；

6、TaiShan200 机架服务器的价值特性：算、存、传、管、AI（智）；

7、ECS：弹性云服务器

8、BMS：裸金属服务器

- 2 路 CPU ，最高 128 核；
- 全部资源都分配给你来用，但是弹性云服务器 ECS 会池化，只分配一部分给你用；



## 2.5 TPCC

&emsp;&emsp;TPCC 交易类型，有如下几种类型：

- 新订单
- 支付操作
- 发货
- 订单状态查询
- 库存状态查询

&emsp;&emsp;具体交易类型解析可参考下图

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210123164042.png)



&emsp;&emsp;TPCC 性能衡量指标，**这几个数值都是越大越好**

- 流量指标，tpmc
- 性价比，price / tpmc

- tpmtotal
- tpmTOTAL



## 2.6 BenchmarkSQL 测试工具

1、编译安装需求：**需要 JDK7 或以上版本**

2、支持的数据库有

- Oracle
- PostgreSQL
- EnterpriseDB
- DB2
- SQL Server
- GaussDB，华为自研数据库（ OpenGauss ）

3、不同数据库创建的配置文件

- Oracle：**props.ora**
- PostgreSQL：**props.pg**
- FirebirdSQL：**props.fb**
- GaussDB：**props.gb**

4、数据库连接

- db：数据库，例如 Oracle 、PostgreSQL
- driver：数据库驱动；
- conn：数据库连接字符串
- user/password：数据库用户名及密码

5、场景配置参数

- warehouse：指定仓库数量。
- loadWorkers：指定装载数据的并发数。
- Terminals：指定并发用户数。
- runMins：指定测试时间。
- runTxnsPerTerminal：指定每个 Terminal 运行的事务数量，runMins 必须等于0。
- limitTxnsPerMin：指定每分钟总事务数。
- terminalWarehouseFixed：指定每个终端是否绑定固定 warehouse 。

6、衡量指标

- tpmC（ NewOrders ）
- tpmTOTAL（ TPS ）

7、性能优化思路，看个眼熟

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210123171623.png)



## 2.7 HiBench

1、大数据基准测试套件「HiBench」。基本简介、支持的框架、开源版本组件等如下图

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210123172010.png)

2、HiBench 测试分类如下，共有 6 种测试类别

- micro
- ml（机器学习）
- sql
- graph
- websearch
- streaming

3、HiBench 文件配置如下，修改 ${HiBench}/conf/hadoop.conf

- 设置 hadoop 安装目录（注：因个人环境而异）

```shell
hibench.hadoop.home ${hadoop_home}
```

- 设置 hadoop 执行目录

```shell
hibench.hadoop.executable ${hibench.hadoop.home}/bin/hadoop
```

- 设置 hadoop 配置目录

```shell
hibench.hadoop.configure.dir ${hibench.hadoop.home}/etc/hadoop
```

- 设置 HDFS root 路径，用于存储 HiBench 数据

```shell
hibench.hdfs.master hdfs://hacluster
```

4、测试报告，衡量标准：Throughput（吞吐量），越高越好；数值越高，性能越优！



## 2.8 HPC 性能测试

1、什么是 HPC ？

&emsp;&emsp;HPC ( High Performance Computing ）高性能计算，是通过 **高速网络** 将大量服务器进行互联形成计算机 **集群** ，与高性能 **存储** 一起，求解科研、工业界最复杂的 **科学计算** 问题（科学研究领域三大范式：理论科学，实验科学，计算科学）。

2、典型应用领域

- 环境科学
- 生命科学
- 材料学/化学
- 天文物理
- 能源
- 制造

3、HPC 典型应用 - WRF ，具体介绍资料参考下图

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210123173508.png)

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210123173515.png)



## 2.9 性能调优分析工具

1、华为鲲鹏性能优化工具，V1.5 版本的名字：Kunpeng Tuning kit

2、性能调优概述，参考下图

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210123185151.png)

3、华为鲲鹏性能优化工具，**主要针对应用程序部署在 TaiShan 服务器的场景下**，具体参考下图

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210123185537.png)

4、华为鲲鹏性能优化工具的功能特点

- 支持采集整个系统或指定进程的 CPU Cycles 性能事件，能够快速定位热点函数。

- 支持热点函数按照 CPU核/线程/模块进行分组，支持查看热点函数调用栈。
- 支持通过火焰图查看热点函数及其调用栈。
- 支持代码映射功能，即查看函数内的热点指令及该指令对应的高级语言文件及行号。
- 支持显示汇编代码的控制流图。
- 支持分析 Java 代码的热点函数及热点指令。

5、华为鲲鹏性能优化工具目前 **只支持单机部署** ，即将华为鲲鹏性能优化工具所有组件部署在一台服务器上，完成对该台服务器软件的性能数据采集和分析。部署环境要求如下表所示：

|   类别   |         子类         | 要求                                                         |
| :------: | :------------------: | :----------------------------------------------------------- |
|   硬件   |        服务器        | TaiShan 200 服务器，采用华为鲲鹏 920 处理器                  |
| 操作系统 | CentOS<br/>openEuler | 1、CentOS 7.6 ，内核版本要求 4.14.0 以上<br/>2、openEuler 开源社区版本 |

6、华为鲲鹏性能优化工具业务流程

（1）输入

- 创建性能分析任务
- 配置任务属性参数（分析类型、应用路径、CPU 采样周期等）
- 运行待分析软件和分析任务

（2）分析处理

- 采集处理器性能指标数据
- 采集函数（ C/C++/Java ）性能指标数据
- 将采集数据文件按不同指标维度数据库化保存
- 统计分析，对比经验指标，定位出性能瓶颈

（3）输出；输出结果很重要，不是只有这三类

- Top 热点函数
- 热点代码块（源码 & 汇编展示）
- 火焰图展示函数间调用关系



## 2.10 NUMA

1、物理上，一个 DDR 只挂载在一个 node 上，其它 node 要访问这个 node 上的 DDR 需要通过片内总线或片间总线进行通信。

2、内存访问延迟从高到低为：<font color=#ff0000 size=4> `跨Socket > 跨NUMA不跨Socket > NUMA内` </font>



## 2.11 思考题

1、TPCC衡量标准是什么？( **C** ）

A. QphH

B. 响应时间

C. tpmC

D. TPS

2、BenchmarkSQL配置文件中loadWorkers指的是什么（ **B** ）。

A. 并发用户数

B. 数据库装载并发数

C. 数据库并行数

D. 数据库表的数量

3、HiBench支持的框架有哪些？（ **ABCD** ）

A. flinkbench

B. hadoopbench

C. stormbench

D. sparkbench

4、下列哪些选项可能会影响 WRF 性能（ **ABCD** ）

A. 网络带宽

B. 并行线程数

C. 内存刷新频率

D. 存储读写速度

5、华为鲲鹏性能优化工具支持从哪些维度分析应用的性能瓶颈？（ **AB** ）

A. C/C++

B. Java Mixed-Mode

C. Locks and Waits

D. LLC&DDR

6、华为鲲鹏性能优化工具能够提供（ **ABCD** ）方面的性能分析结果。

A. 分析 Top 热点函数

B. 分析函数火焰图

C. 分析热点函数代码映射

D. 分析不同函数对应 top-down 模型的各指标值



## 2.12 交叉编译

&emsp;&emsp;为什么会有交叉编译？

- Speed：目标平台的运行速度往往比主机慢得多，许多专用的嵌入式硬件被设计为低成本和低功耗，没有太高的性能；
- Capability：整个编译过程是非常消耗资源的，嵌入式系统往往没有足够的内存或磁盘空间；
- Availability：即使目标平台资源很充足，可以本地编译，但是第一个在目标平台上运行的本地编译器总需要通过交叉编译获得；
- Flexibility：一个完整的 Linux 编译环境需要很多支持包，交叉编译使我们不需要花时间将各种支持包移植到目标板上；



## 2.13 Linux 安装软件

1、Linux 目前安装软件的方式有三种：源码安装，yum 安装软件，RPM 安装安装。

2、源码安装

- 可以自定义安装目录和一些配置文件
- 但需要事先调整编译参数

3、Yum 安装软件

- 全自动安装，自动安装依赖
- 但缺乏自主性，软件的功能和存放的位置均已设置好

4、RPM 安装

- 自主制作的 RPM 包能够实现全自动安装，且可自定义安装路径等配置
- 但需提前识别依赖并手动安装



## 2.14 RPMbuild

&emsp;&emsp;RPMbuild 是用来指示转换的源码编译成二进制文件的包，如果想发布 rpm 格式的源码包或者是二进制包，就要使用 RPMbuild 工具。

&emsp;&emsp;RPMbuild 文件夹的目录结构如下：

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124132018.png)

&emsp;&emsp;RPM 包制作流程，如下图所示

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124132053.png)

&emsp;&emsp;rpmbuild 目录如下图所示

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124132153.png)



## 2.15 镜像服务

&emsp;&emsp;镜像是用于创建服务器或磁盘的模板。

- 镜像分为 **公共镜像、私有镜像、共享镜像、市场镜像** 。

- 公共镜像为系统默认提供的镜像，私有镜像为用户自己创建的镜像，共享镜像为其他用户共享的私有镜像。

&emsp;&emsp;镜像服务具有以下功能：

- 提供常见的主流操作系统公共镜像（支持的操作系统类型请以控制台镜像服务页面的显示为准)。
- 创建私有镜像。
- 管理镜像。
- 通过镜像创建云服务器。





## 2.16 思考题

1、RPM打包使用的是什么命令，这个命令来自以下哪个包？（ **B** ）

A. rpm , rpmbuild包

B. rpmbuild ，rpm-build包

C. rpmbuild , rpmbuild包

D. rpm , rpm-build包

2、下载的源码包放在哪个目录下? ( **C** )

A.BUILD

B.RPMS

C.SOURCES

D.SPEC

3、使用镜像创建云服务器的好处是什么？

&emsp;&emsp;节省时间成本，减少重复劳动等；

4、RPM 和 SRPM 包（ filename.rpm 和 filename.src.rpm ）区别是什么？

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124132833.png)

5、rpm 方式安装与 yum 安装联系与区别？

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124132905.png)

6、Porting Advisor工具在移植源码过程中的作用是？（ **B** ）

A. 分析源码，并给出移植工作量

B. 分析源码，并给出分析报告和源码修改建议

C. 分析源码，并修改源码

D. 分析源码，并给出性能优化建议



## 2.17 华为鲲鹏

1、华为鲲鹏处理器发展图

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124135350.png)

2、鲲鹏计算产业目标

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124135435.png)

3、全自研服务器 TaiShan 

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124135517.png)

4、鲲鹏生态兼容的操作系统介绍如下图， SUSE 支持鲲鹏版本为 15.1 ；

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124135614.png)

5、鲲鹏计算产业生态全景

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124135828.png)

6、华为鲲鹏伙伴计划

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124135949.png)

7、华为鲲鹏处理器架构（ARM）特点

（1）优点

- 采用ARM架构，同样功能性能占用的芯片面积小、功耗低、集成度更高，更多的硬件 CPU 核具备更好的并发性能。
- 支持 16 位、32 位、64 位多种指令集，能很好的兼容从 IOT 、终端到云端的各类应用场景。
- 大量使用寄存器，大多数数据操作都在寄存器中完成，指令执行速度更快。
- 采用 RISC 指令集，指令长度固定，寻址方式灵活简单，执行效率高。

（2）不足

- 在数据中心领域属于新进入者，其生态仍处于快速发展阶段。

8、华为鲲鹏通用计算处理器，三代芯片，三个第一如下：

- 2014 年，鲲鹏 912 （Hi1612），第一颗基于 ARM 的 64 位 CPU ；
- 2016 年，鲲鹏 916 ，业界第一颗支持多路 ARM CPU ；
- 2019 年，鲲鹏 920 ，业界第一颗 7nm 数据中心 ARM CPU ；

9、华为鲲鹏 920 处理器规格

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124140548.png)

10、华为鲲鹏处理器技术创新

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124140634.png)

11、鲲鹏 920 内置多种加速引擎

- 内置 SSL 加速引擎
- 内置加密算法加速引擎
- 内置压缩引擎

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124140749.png)



## 2.18 TaiShan 服务器

1、TaiShan 100 服务器与 TaiShan 200 服务器对比图

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124141026.png)

2、TaiShan 200 服务器全景图

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124141042.png)

3、TaiShan 200 机架服务器特点

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124141118.png)



## 2.19 华为云鲲鹏云服务

1、华为鲲鹏弹性云服务器优势，最大规格 60U480G ；

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124141331.png)



## 2.20 openEuler

1、openEuler 发展时间点：

- 2019.09.19 合作伙伴内测
- 2019.12.31 全面开放开源

2、ISula 容器解决方案，特点如下：

- 快速灵活&轻量级
- 可信&安全启动
- 升级不中断业务
- 增强安全性和调测特性

3、A-Tune 资源调优自动化

&emsp;&emsp;A-Tune 是一种 **通过非侵入式系统画像的负载感知方法** ，识别业务并匹配最佳资源模型，实时响应业务特征变化的 Al 自动调优系统。

4、openEuler 开源社区，备注：题目中链接的网址一般都没问题，除非域名直接有问题。

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124142009.png)



## 2.21 鲲鹏处理器与 X86 处理器的指令差异

1、加法代码，参考指令差异如下图

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124142158.png)



## 2.22 编译型语言 & 解释型语言

1、编译型语言：典型如 C/C++/Go 语言，都属于编译型语言。编译型语言开发的程序在从 x86 处理器迁移到鲲鹏处理器时，必须经过重新编译才能运行。

2、从源码到程序的过程：源码需要由编译器、汇编器翻译成机器指令，再通过链接器链接库函数生成机器语言程序。机器语言必须与 CPU 的指令集匹配，在运行时通过加载器加载到内存，由 CPU 执行指令。简要图示如下：

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124142418.png)



3、解释型语言：典型的如 Java/Python 语言，都属于解释型语言，解释型语言开发的程序在迁移到鲲鹏处理器时，**一般不需要重新编译**。

4、解释型语言的源代码由编译器生成字节码，然后再由虚拟机解释执行。虚拟机将不同 CPU 指令集的差异屏蔽，因此解释型语言的可移植性很好。但是如果程序中调用了编译型语言所开发的 so 库，那么这些 so 库需要重新移植编译。简要图示如下：

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124142729.png)

5、编译型语言，总结如下：

- C
- C++
- Go
- Swift
- Pascal

6、解释型语言，总结如下：

- Java
- Python
- lua
- Ruby
- PHP
- Scala
- Perl
- TypeScript
- JavaScript

7、编译型语言、解释型语言，参考图示如下：

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124143240.png)





## 2.23 移植选项

1、C/C++ 代码 builtin 函数、数据类型移植

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124142912.png)

2、C/C++ 代码编译选项、编译宏移植

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124142951.png)



## 2.8 华为鲲鹏代码迁移工具

1、业务流程如下图所示

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124143452.png)

2、CLI 方式进行代码分析，命令功能，命令格式及参数说明等

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124143529.png)



## 2.24 容器与虚拟机

1、容器和虚拟机之间的主要区别在于虚拟化层的位置和操作系统资源的使用方式。

2、容器与虚拟机参数对比

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124144024.png)



## 2.25 Docker

1、Docker 架构如下图

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124144158.png)

2、Dockerfile 是一个文本格式的配置文件，包含创建镜像所需要的全部指令。基于在 Dockerfile 中的指令，用户可以快速创建自定义的镜像。

- Docker image 的表述
- 简单语法用来构建镜像
- 自动化的脚本创建镜像

3、Docker 容器迁移有两种策略：使用 Docker pull 获取镜像或使用 Dockerfile 构建镜像。

（1）Docker pull 获取镜像

- Docker pull 命令直接获取基于 ARM 平台的 docker 镜像
- 使用 Docker pull 命令的对象必须是适用于 ARM 的镜像，如 arm64v8/centos:7

（2）Dockerfile 构建镜像

- 使用 dockerfile 构建基于 ARM 平台的 docker 镜像
- 基础镜像和构建后的镜像均只能使用于 ARM 平台

4、Docker 镜像常用命令记录

- 获取镜像

```shell
docker pull
```

- 查看镜像

```shell
docker images
```

- 启动容器

```shell
docker run
```

- 退出

```shell
# 按下 Ctrl + D
# 输入命令
exit
```

- 查看容器，运行中和未运行的容器

```shell
docker ps -a
```

- 通过 Dockerfile 创建镜像

```shell
docker build
```



## 2.26 TPCC

1、TPCC 性能衡量指标

- 流量指标
- 性价比



## 2.27 BenchmarkSQL

1、编译安装需求：**需要 JDK7 或以上版本**

2、支持的数据库有

- Oracle
- PostgreSQL
- EnterpriseDB
- DB2
- SQL Server
- GaussDB，华为自研数据库（ OpenGauss ）

3、不同数据库创建的配置文件

- Oracle：**props.ora**
- PostgreSQL：**props.pg**
- FirebirdSQL：**props.fb**
- GaussDB：**props.gb**

4、数据库连接

- db：数据库，例如 Oracle 、PostgreSQL
- driver：数据库驱动；
- conn：数据库连接字符串
- user/password：数据库用户名及密码

5、场景配置参数

- warehouse：指定仓库数量。
- loadWorkers：指定装载数据的并发数。
- Terminals：指定并发用户数。
- runMins：指定测试时间。
- runTxnsPerTerminal：指定每个 Terminal 运行的事务数量，runMins 必须等于0。
- limitTxnsPerMin：指定每分钟总事务数。
- terminalWarehouseFixed：指定每个终端是否绑定固定 warehouse 。

6、衡量指标

- tpmC（ NewOrders ）
- tpmTOTAL（ TPS ）

7、性能优化思路，看个眼熟

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210123171623.png)



## 2.28 HiBench

1、大数据基准测试套件「HiBench」。基本简介、支持的框架、开源版本组件等如下图

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210123172010.png)

2、HiBench 测试分类如下，共有 6 种测试类别

- micro
- ml（机器学习）
- sql
- graph
- websearch
- streaming

3、HiBench 文件配置如下，修改 ${HiBench}/conf/hadoop.conf

- 设置 hadoop 安装目录（注：因个人环境而异）

```shell
hibench.hadoop.home ${hadoop_home}
```

- 设置 hadoop 执行目录

```shell
hibench.hadoop.executable ${hibench.hadoop.home}/bin/hadoop
```

- 设置 hadoop 配置目录

```shell
hibench.hadoop.configure.dir ${hibench.hadoop.home}/etc/hadoop
```

- 设置 HDFS root 路径，用于存储 HiBench 数据

```shell
hibench.hdfs.master hdfs://hacluster
```

4、测试报告，衡量标准：Throughput（吞吐量），越高越好；数值越高，性能越优！



## 2.29 HPC 性能测试

1、什么是 HPC ？

&emsp;&emsp;HPC ( High Performance Computing ）高性能计算，是通过 **高速网络** 将大量服务器进行互联形成计算机 **集群** ，与高性能 **存储** 一起，求解科研、工业界最复杂的 **科学计算** 问题（科学研究领域三大范式：理论科学，实验科学，计算科学）。

2、典型应用领域

- 环境科学
- 生命科学
- 材料学/化学
- 天文物理
- 能源
- 制造

3、HPC 典型应用 - WRF ，具体介绍资料参考下图

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210123173508.png)

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210123173515.png)



## 2.30 性能调优分析工具

1、华为鲲鹏性能优化工具，V1.5 版本的名字：Kunpeng Tuning kit

2、性能调优概述，参考下图

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210123185151.png)

3、华为鲲鹏性能优化工具，**主要针对应用程序部署在 TaiShan 服务器的场景下**，具体参考下图

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210123185537.png)

4、华为鲲鹏性能优化工具的功能特点

- 支持采集整个系统或指定进程的 CPU Cycles 性能事件，能够快速定位热点函数。

- 支持热点函数按照 CPU核/线程/模块进行分组，支持查看热点函数调用栈。
- 支持通过火焰图查看热点函数及其调用栈。
- 支持代码映射功能，即查看函数内的热点指令及该指令对应的高级语言文件及行号。
- 支持显示汇编代码的控制流图。
- 支持分析 Java 代码的热点函数及热点指令。

5、华为鲲鹏性能优化工具目前 **只支持单机部署** ，即将华为鲲鹏性能优化工具所有组件部署在一台服务器上，完
成对该台服务器软件的性能数据采集和分析。部署环境要求如下表所示：

|   类别   |         子类         | 要求                                                         |
| :------: | :------------------: | :----------------------------------------------------------- |
|   硬件   |        服务器        | TaiShan 200 服务器，采用华为鲲鹏 920 处理器                  |
| 操作系统 | CentOS<br/>openEuler | 1、CentOS 7.6 ，内核版本要求 4.14.0 以上<br/>2、openEuler 开源社区版本 |

6、华为鲲鹏性能优化工具业务流程

（1）输入

- 创建性能分析任务
- 配置任务属性参数（分析类型、应用路径、CPU 采样周期等）
- 运行待分析软件和分析任务

（2）分析处理

- 采集处理器性能指标数据
- 采集函数（ C/C++/Java ）性能指标数据
- 将采集数据文件按不同指标维度数据库化保存
- 统计分析，对比经验指标，定位出性能瓶颈

（3）输出；输出结果很重要，不是只有这三类

- Top 热点函数
- 热点代码块（源码 & 汇编展示）
- 火焰图展示函数间调用关系



## 2.31 NUMA

1、物理上，一个 DDR 只挂载在一个 node 上，其它 node 要访问这个 node 上的 DDR 需要通过片内总线或片间总线进行通信。

2、内存访问延迟从高到低为：<font color=#ff0000 size=4> `跨Socket > 跨NUMA不跨Socket > NUMA内` </font>



## 2.32 镜像

1、镜像类型：公共镜像、私有镜像、共享镜像、市场镜像；

2、镜像简要说明如下

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124150932.png)



## 2.33 系统盘

1、系统盘类型：普通IO、高速高IO、超高IO、超高IO（时延优化）；

2、系统盘简要说明如下图

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124151055.png)



## 2.34 弹性公网 IP

1、弹性公网 IP  ( Elastic IP ，简称 EIP ）提供独立的公网 IP 资源，包括公网 IP 地址与公网出口带宽服务。可以与弹性云服务器、裸金属服务器、虚拟 IP 、弹性负载均衡、NAT 网关等资源灵活地绑定及解绑。拥有多种灵活的计费方式，可以满足各种业务场景的需要。

2、一个弹性公网 IP 只能绑定一个云资源使用。



## 2.35 BGP 类型

1、静态 BGP ：网络结构发生变化时，无法实时自动调整网络设置以保障用户体验。

2、全动态 BGP ：可以根据设定的寻路协议实时自动优化网络结构，以保持客户使用的网络持续稳定、高效。



## 2.36 编译

1、编译通常指利用编译程序从源语言编写的源程序产生目标程序的过程，或者动作。一般包括两种类型，本地编译和交叉编译。

2、本地编译

（1）本地编译可以理解为，在当前编译平台下，编译出来的程序只能放到当前平台下运行。平时我们常见的软件开发，都是属于本地编译；

（2）比如，我们在 x86 平台上，编写程序并编译成可执行程序。这种方式下，我们使用 x86 平台上的工具，开发针对 x86 平台本身的可执行程序，这个编译过程称为本地编译。

3、交叉编译

（1）交叉编译可以理解为，在当前编译平台下，编译出来的程序能运行在体系结构不同的另一种目标平台上，但是编译平台本身却不能运行该程序；

（2）比如，我们在 x86 平台上，编写程序并编译成能运行在 ARM 平台的程序，编译得到的程序在 x86 平台上是不能运行的，必须放到 ARM 平台上才能运行。

4、为什么会有交叉编译？

- Speed：目标平台的运行速度往往比主机慢得多，许多专用的嵌入式硬件被设计为低成本和低功耗，没有太高的性能；
- Capability：整个编译过程是非常消耗资源的，嵌入式系统往往没有足够的内存或磁盘空间；
- Availability：即使目标平台资源很充足，可以本地编译，但是第一个在目标平台上运行的本地编译器总需要通过交叉编译获得；
- Flexibility：一个完整的 Linux 编译环境需要很多支持包，交叉编译使我们不需要花时间将各种支持包移植到目标板上；



## 2.37 Linux 安装软件

1、Linux 目前安装软件的方式有三种：源码安装，yum 安装软件，RPM 安装安装。

2、源码安装

- 可以自定义安装目录和一些配置文件
- 但需要事先调整编译参数

3、Yum 安装软件

- 全自动安装，自动安装依赖
- 但缺乏自主性，软件的功能和存放的位置均已设置好

4、RPM 安装

- 自主制作的 RPM 包能够实现全自动安装，且可自定义安装路径等配置
- 但需提前识别依赖并手动安装

5、RPM概述

（1）RPM（ Redhat Package Manager）是用于 Redhat 、CentOS 、Fedora 等 Linux 操作系统的常见软件包管理器。它允许分发已编译的软件，支持一键安装软件。

（2）由于 RPM 是经过预先编译并打包成为 RPM 文件格式后，再加以安装的一种方式，并且还能够进行数据库的记载，所以RPM有以下的优点：

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124152145.png)



## 2.38 RPMbuild

&emsp;&emsp;RPMbuild 是用来指示转换的源码编译成二进制文件的包，如果想发布 rpm 格式的源码包或者是二进制包，就要使用 RPMbuild 工具。

&emsp;&emsp;RPMbuild 文件夹的目录结构如下：

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124132018.png)

&emsp;&emsp;RPM 包制作流程，如下图所示

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124132053.png)

&emsp;&emsp;rpmbuild 目录如下图所示

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124132153.png)



## 2.39 华为云发布的鲲鹏行业解决方案

1、目前华为云已经发布的鲲鹏行业解决方案分为两大类：鲲鹏通用解决方案和鲲鹏行业解决方案。

2、鲲鹏通用解决方案

- 全栈专属云 HCS Online
- 企业核心应用
- 鲲鹏分布式存储
- 高性能计算 HPC
- 大数据基础设施

3、鲲鹏行业解决方案

- ZF
- 金融
- 运营商
- 智能安防
- 游戏
- 媒体和娱乐
- 其他

4、HCS Online 解决方案核心价值

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210124152658.png)



## 2.40 思考题

1、以下哪些关于华为鲲鹏 920 处理器的描述是正确的？（ **ABCD** ）

A. 采用了 7nm 的制造工艺；

B. 支持 8 通道的 DDR4 控制器；

C. 支持 PCIe 4.0 接口，并兼容 PCIe 3.0/2.0/1.0 ；

D. 支持多种加速器；

2、华为鲲鹏 920 处理器内置了哪些加速器？（ **ABC** ）

A. SSL 加速引擎

B. 加解密加速引擎

C. 压缩解压缩加速引擎

3、TaiShan 200机架服务器包含哪些型号？（ **ABC** ）

A. 2280

B. 5280

C. 2480

D. X6000

4、华为鲲鹏 BMS 云服务器最高可提供多少核？（ **D** ）

A. 32

B. 48

C. 64

D. 128

5、华为鲲鹏代码迁移工具适用于以下哪些类型的应用程序？（ **AC** ）

A. C/C++

B. Java

C. 汇编

D. Python

6、华为鲲鹏代码迁移工具能够提供（ **BC** ）方面的移植评估结果。

A. 扫描源码中有多少个安装包

B. 扫描源码中有多少可以移植的依赖库 SO 文件

C. 扫描源码中有多少行可以移植的 C/C++ 代码、汇编代码

D. 预估移植所需的工作量

7、关于执行命令 “docker ps -a” 后，显示的标题含义描述，正确的是？（ **ABCD** ）

A. CONTAINER ID：容器的唯一表示 ID

B. IMAGE：创建容器时使用的镜像

C. COMMAND：容器最后运行的命令

D. CREATED：创建容器的时间

8、关于 Docker 的镜像仓库，说法正确的是？（ **ABCD** ）

A. 实现 Docker 镜像的全局存储

B. 提供 API 接口

C. 提供 Docker 镜像的下载/推送/查询

D. 可用于租户管理

9、在向鲲鹏处理器迁移软件时，以下哪些是可能导致编译错误或告警的原因？（ **ABC** ）

A. 编译选项

B. 数据类型不同

C. 汇编指令

D. 弱内存序问题

10、弱内存序问题主要与如下哪些因素相关？（ **ACE** ）

A. 多线程

B. 多进程

C. 不同 CPU 之间 Cache 同步

D. 一级、二级、三级 Cache 间数据同步

E. 不同 core 之间 Cache 同步

11、HiBench支持的框架有哪些？（ **ABCD** ）

A. flinkbench

B. hadoopbench

C. stormbench

D. sparkbench

12、下列哪些选项可能会影响 WRF 性能（ **ABCD** ）

A. 网络带宽

B. 并行线程数

C. 内存刷新频率

D. 存储读写速度

13、RPM打包使用的是什么命令，这个命令来自以下哪个包？（ **B** ）

A. rpm , rpmbuild包

B. rpmbuild ，rpm-build包

C. rpmbuild , rpmbuild包

D. rpm , rpm-build包

14、下载的源码包放在哪个目录下? ( **C** )

A.BUILD

B.RPMS

C.SOURCES

D.SPEC

15、Porting Advisor工具在移植源码过程中的作用是？（ **B** ）

A. 分析源码，并给出移植工作量

B. 分析源码，并给出分析报告和源码修改建议

C. 分析源码，并修改源码

D. 分析源码，并给出性能优化建议

16、以下哪些属于鲲鹏通用解决方案？（ **ABCD** ）

A. HCSO 解决方案；

B. 大数据解决方案；

C. HPC 解决方案；

D. 分布式存储；



# 3 题库分享

&emsp;&emsp;本次主要分享 V1.0 版本的题库，后续如果找到新版本 V1.5 的题库，也会分享出来！

## 3.1 资源获取

&emsp;&emsp;目前获取「华为鲲鹏 HCIA 认证考试 V1.0 」题库的方式有如下几种

- 【收费】CSDN 资源下载，链接：[https://download.csdn.net/download/Fighting_Boom/14921275](https://download.csdn.net/download/Fighting_Boom/14921275)
- 【免费】扫描下方二维码，关注公众号「编码小二」，公众号后台回复关键字「鲲鹏HCIA」即可免费获取。

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20211027234649.jpg)

- 【免费】扫描下方二维码，添加小二微信，回复关键字「鲲鹏HCIA」即可免费获取。**人工处理，可能稍慢，请多多包涵🤝🤝🤝**

![](https://gitee.com/FightingBoom/BlogPictures/raw/master/img_20200821/20210704170229.jpg)

## 3.2 模拟考试

&emsp;&emsp;【参考资料】中有分享大佬的题库，其中也有大佬自己做的模拟考试，我就总结了我记录的题库，也制作了一些模拟考试。

&emsp;&emsp;获取方式：关注微信公众号「编码小二」，后台回复关键字「鲲鹏模拟考试」即可免费获取。



# 4 结尾祝福

&emsp;&emsp;非常感谢您能看到这里，别忘了关注公众号「编码小二」获取免费资源呀！最后祝大家旗开得胜，马到成功！
