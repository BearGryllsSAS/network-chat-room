# 网络聊天室 [English Introduce](README-EN.md)

相关概念参考：

- [维基百科-网络聊天室](https://zh.m.wikipedia.org/wiki/%E7%B6%B2%E8%B7%AF%E8%81%8A%E5%A4%A9%E5%AE%A4 "点击跳转维基百科页面")
- [百度百科-网络聊天室](https://baike.baidu.com/item/%E7%BD%91%E7%BB%9C%E8%81%8A%E5%A4%A9%E5%AE%A4/2324705?_swebfr=220011 "点击跳转百度百科页面")

## 项目简介

在这个梦幻般的网络公共聊天室中，我倾注了毕生的心血，打造了一个令人惊叹的交流空间。这个聊天室拥有着无与伦比的性能和高效的并发处理能力，让每一次互联网冒险都变得如丝般顺滑。无论您是匆匆路过的游客，还是渴望分享心情的常驻用户，这里都将成为您畅谈的乐园。登录、注册、畅聊，一切尽在指尖之间。选择成为会员，更将开启一段独特的旅程，尽享专属特权和精彩体验。在这个充满活力和可能性的聊天室里，每一次交流都是一场启发灵感的冒险，每一次登录都是一次奇妙的邂逅。这里融合了技术的力量和人性的温暖，成就了一个真正意义上的数字家园，期待您的加入，共同书写属于我们的精彩故事。

## 系统架构图

项目主体骨架基于非阻塞 `Socket`+`Epoll` 网络监听体系，使用线程池处理与客户端数据的收发，采用 `MySQL` 数据库连接池封装多个 `MySQL` 对象进行数据持久化管理，采用基于升序链表的定时器记录客户端的活跃状态以避免资源浪费，同时实现了同步/异步日志系统记录服务器运行状态。

## 项目结构说明
>  网络聊天室  
>
> > `documents` -- 环境搭建、编码规范、项目需求等文档资源
> > 
> > `server-cpp` -- `C++` 服务器项目主体
> >
> > `.gitignore` -- 忽略提交配置
> >
> > `LICENSE` -- `Apache` 许可证
> > 
> > `README-CN.md` -- 项目自述文件-中文版
> > 
> > `README-EN.md` -- 项目自述文件-英文版


## 环境要求

### 开发工具

| 工具            | 说明                  | 版本      | 备注                                                         |
| --------------- | --------------------- | --------- | ------------------------------------------------------------ |
| `DataGrip`      | 数据库连接工具        |  `2023.3.2`   | https://www.jetbrains.com/datagrip/cn/                        |
| `CMake`         | 跨平台编译工具       | `8.0.27`    |https://cmake.org/ |               |
| `Git`           | 项目版本管控工具      | `1.8.3.1`    | https://git-scm.com/                                         |
| `GitHub`        | 项目源码托管平台      | `latest`    |https://github.com/                                    |
| `Axure`         | 原型设计工具          | `9`         | https://www.axure.com/                                       |
| `MindMaster`    | 思维导图设计工具      | `latest`    | http://www.edrawsoft.cn/mindmaster                           |
| `Visio`         | 流程图绘制工具        | `latest`    | https://www.microsoft.com/zh-cn/microsoft-365/visio/flowchart-software |

### 服务器环境

| 依赖环境    | 版本                                                         | 备注                                                         |
| ----------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `CentOS` | `7.9`                                                      | https://www.centos.org/                               |
| `MySQL`     | `5.7.44`                                                       | https://www.mysql.com/cn/                                    |      |

## 特别鸣谢

网络聊天室的诞生离不开开源软件和社区的支持，感谢以下开源项目及项目维护者：

- `TinyWebServer`: https://github.com/qinguoyi/TinyWebServer.git
- `Linux`: https://github.com/torvalds/linux.git

同时也感谢其他没有明确写出来的开源组件提供给与维护者。

## 支持一下

如果觉得框架和项目还不错，点个⭐Star，这将是对**01星球**极大的鼓励与支持。

想了解更多关于计算机方向选择、学习建议等相关信息，可以关注[**01星球B站主页~**](https://space.bilibili.com/1653229811?spm_id_from=333.1007.0.0)
