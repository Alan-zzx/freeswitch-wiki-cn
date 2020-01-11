## 关于

在这个介绍中我们提供了关于``Freeswitch``的简要概述。将介绍``Freeswitch``相关的所有关键概念，并指导你如何浏览文档。通过下面的介绍，你应该能够在任何时候设置``Freeswitch``基本部署配置。如果你决定深入挖掘，并熟悉更先进的功能，你可以通过我们的链接找到相关内容。最后我们将提供默认配置的介绍，这样你就可以得到一个实践教程，以及最常用的功能。

## Freeswitch 是什么

``Freeswitch``是一个软件定义的电信协议栈，实现了从专用电信交换机到通用软件的转换，并且可以运行在任意硬件设备上。从树莓派到多核服务器，``Freeswitch``能够提供任何设备电信通讯能力。结合我们的托管云平台``SignalWire``，``Freeswitch``能够与外部世界互联并且能够扩展到任意大小。（详见[SignalWire](https://signalwire.com/)）

``Freeswitch``在``IP``网络和``PSTN``（常规固定电话）下提供了语音，视频以及文本通信能力。``Freeswitch``支持所有流行的``VoIP``协议以及``PRIs``的接口。在[端点( Endpoints)](Introduction/Endpoints.md)页可以查看所有支持的协议。

``Freeswitch``的一些常用功能如下：

- [PBX](Introduction/Glossary.md)（办公电话系统）

- [5级软交换](Introduction/Glossary.md)（电话运营商）
- 应用服务，例如语音信箱，会议，IVR。
- [软电话](Introduction/Glossary.md)

这个列表并不全面，``Freeswitch``能够以你想象的任何方式使用，非常灵活。

[默认配置](Configuration\Default Configuration.md) 展示了一个全功能的 [PBX](Introduction/Glossary.md) 和许多应用程序。

## 如何运行 Freeswitch

``Freeswitch``的核心是一个库，可以嵌入到你的应用程序并且运行在任意设备中。然而更常见的是，``Freeswitch``被作为后台程序运行（Unix或Linux系统中的守护进程、Windows系统中的服务）。当你使用守护进程的形式运行``Freeswtich``时，你可以使用[CLI](Client and Developer Interfaces\Command-Line Interface fs_cli.md) 与``Freeswitch``交互。

``Freeswitch``可以运行在任何平台上，包括Linux、Mac OS X、BSD、Solaris 甚至是 Windows。

>如果你不想操作自己的服务器，Freeswitch 的赞助商——[SignalWire](https://signalwire.com/)提供了云托管的 Freeswitch 服务器，从专用的 Freeswitch 服务器到可自动扩展的 Freeswitch 云托管服务器。

``Freeswitch``虽然可以在许多 Linux 发行版中运行，例如 Debian、Ubuntu、CentOS、Fedora 和 RHEL，我们首选的发行版是 Debian，因为我们已经解决了对 Debian 的所有依赖，所以您可以顺利的安装和启动。Debian 也是``FreeSWITCH``开发人员使用的，因此最有经验。如果您在其他发行版上运行，您可能很难正确地处理所有依赖。

> 有关最新支持的平台，请参阅 [发行说明](Introduction.md) 和 [安装说明](Introduction.md) 。

硬件配置要求取决于如何使用``Freeswitch``，``Freeswitch``可以运行在像树莓派那样小的硬件中，也可以扩展到具有几十个 CPU 核心的强大数据中心服务器。``Freeswitch``可以同时处理上千的电话，取决于硬件配置和你使用的应用程序（applications）。

>有关硬件要求的更多信息，请参阅 [发行说明](Introduction.md) 、 [性能测试和配置](Configuration\Performance Testing and Configurations.md) 。

## Freeswitch 的结构

在设计``Freeswitch``时目标是具有以下属性：

- 可扩展性 - 可以轻松添加新功能
- 灵活性 - 用户应该能够自由选择启用哪些功能，同时也运行他们用不同的实现替换系统的部分功能。
- 可伸缩性 - ``Freeswitch``可以运行在小到嵌入式[软电话](Introduction/Glossary.md)或大到全套运营商交换机集群的系统上。
- 稳定性 - 某个功能的问题不应该导致整个系统崩溃。

为了实现这些目标，``Freeswitch``使用模块化构建系统：