# 0.关于

在这个介绍中我们提供了关于``Freeswitch``的简要概述。将介绍``Freeswitch``相关的所有关键概念，并指导你如何浏览文档。通过下面的介绍，你应该能够在任何时候设置``Freeswitch``基本部署配置。如果你决定深入挖掘，并熟悉更先进的功能，你可以通过我们的链接找到相关内容。最后我们将提供默认配置的介绍，这样你就可以得到一个实践教程，以及最常用的功能。

# 1.Freeswitch 是什么

``Freeswitch``是一个软件定义的电信协议栈，实现了从专用电信交换机到通用软件的转换，并且可以运行在任意硬件设备上。从树莓派到多核服务器，``Freeswitch``能够提供任何设备电信通讯能力。结合我们的托管云平台``SignalWire``，``Freeswitch``能够与外部世界互联并且能够扩展到任意大小。（详见[SignalWire](https://signalwire.com/)）

``Freeswitch``在``IP``网络和``PSTN``（常规固定电话）下提供了语音，视频以及文本通信能力。``Freeswitch``支持所有流行的``VoIP``协议以及``PRIs``的接口。在 [Endpoints](Endpoints.md) 页可以查看所有支持的协议。

``Freeswitch``的一些常用功能如下：

- [PBX](Glossary.md)（办公电话系统）

- [5级软交换](Glossary.md)（电话运营商）
- 应用服务，例如语音信箱，会议，IVR。
- [软电话](Glossary.md)

这个列表并不全面，``Freeswitch``能够以你想象的任何方式使用，非常灵活。

[默认配置](../Configuration/Default Configuration.md)展示了一个全功能的 [PBX](Glossary.md) 和许多应用程序。

# 2.如何运行 Freeswitch

``Freeswitch``的核心是一个库，可以嵌入到你的应用程序并且运行在任意设备中。然而更常见的是，``Freeswitch``被作为后台程序运行（Unix或Linux系统中的守护进程、Windows系统中的服务）。当你使用守护进程的形式运行``Freeswtich``时，你可以使用[CLI](../Client and Developer Interfaces/Command-Line Interface fs_cli.md) 与``Freeswitch``交互。

``Freeswitch``可以运行在任何平台上，包括Linux、Mac OS X、BSD、Solaris 甚至是 Windows。

>如果你不想操作自己的服务器，Freeswitch 的赞助商——[SignalWire](https://signalwire.com/)提供了云托管的 Freeswitch 服务器，从专用的 Freeswitch 服务器到可自动扩展的 Freeswitch 云托管服务器。

``Freeswitch``虽然可以在许多 Linux 发行版中运行，例如 Debian、Ubuntu、CentOS、Fedora 和 RHEL，我们首选的发行版是 Debian，因为我们已经解决了对 Debian 的所有依赖，所以您可以顺利的安装和启动。Debian 也是``FreeSWITCH``开发人员使用的，因此最有经验。如果您在其他发行版上运行，您可能很难正确地处理所有依赖。

> 有关最新支持的平台，请参阅[发行说明](../Release Notes/Release Notes.md)和 [安装说明](../Installation/Installation.md)。

硬件配置要求取决于如何使用``Freeswitch``，``Freeswitch``可以运行在像树莓派那样小的硬件中，也可以扩展到具有几十个 CPU 核心的强大数据中心服务器。``Freeswitch``可以同时处理上千的电话，取决于硬件配置和你使用的应用程序（applications）。

>有关硬件要求的更多信息，请参阅 [发行说明](../Release Notes/Release Notes.md) 、[性能测试和配置](../Configuration/Performance Testing and Configurations.md) 。

# 3.Freeswitch 的结构

在设计``Freeswitch``时目标是具有以下属性：

- **可扩展性** - 可以轻松添加新功能
- **灵活性** - 用户应该能够自由选择启用哪些功能，同时也运行他们用不同的实现替换系统的部分功能。
- **可伸缩性** - ``Freeswitch``可以运行在小到嵌入式[软电话](Glossary.md)或大到全套运营商交换机集群的系统上。
- **稳定性** - 某个功能的问题不应该导致整个系统崩溃。

为了实现这些目标，``Freeswitch``使用模块化构建系统：

- 提供所有模块使用的一个**内核**，但是大多数功能并不在这个内核中实现
- 而是在相互不依赖的**独立模块**中实现

当你使用[默认配置](../Configuration/Default Configuration.md) 安装``Freeswitch``时，默认启用了大多数常用场景下需要使用的模块。在后面的配置 [配置](../Modules/XML Modules Configuration.md) 部分将展示如何启用或者禁用特定模块。

模块按其提供的功能类型分组。我们现在将探讨模块的类型，以及每个模块提供的功能。

## 3.1 模块类型

| 类型                                                         | 描述                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [Endpoints](Endpoints.md)                                    | 该模块提供了对于通讯设备的支持，例如 [VoIP](Glossary.md)、[PSTN](Glossary.md)（即固定电话）、Skype、Google Talk等等。 |
| Application                                                  | 所有的 action 都发生在这里，默认配置中包含有数百个应用程序模块，例如播放一个文件，加入一个会议，将电话转入语音信箱，播放一个IVR菜单。[mod_dptools](../Modules/mod_dptools/mod_dptools.md)提供了更多的常见应用程序。 |
| [拨号计划（Dialplan）](../Dialplan/Dialplan.md)              | 拨号计划模块主要负责路由呼叫功能，基于呼叫者ID、被叫号码等。默认拨号计划是[XML Dialplan](../Dialplan/XML Dialplan.md)。我们将在[拨号计划](../Dialplan/Dialplan.md)部分详细介绍。 |
| [Directory](../Directory/Directory.md)                       | 为注册到``Freeswitch``的用户提供身份验证和配置，最常用的Directory module 是 [XML Directory](../Directory/XML User Directory.md)。 |
| [编解码器（Codecs）](../Codecs and Media/Codecs and Media.md) | 编解码器是用来编码和压缩音频流。                             |
| File Formats                                                 | [mod_dptools playback](../Modules/mod_dptools/mod_dptools playback.md)支持大多数常见音频文件格式。<br />注：支持的音频格式详见[mod_dptools playback](../Modules/mod_dptools/mod_dptools playback.md)的第 3 部分 |
| Loggers                                                      | 记录日志消息。其中一些日志记录器是[控制台（console）](../Modules/mod_console.md)和[日志文件](../Modules/mod_logfile.md)。[xml_cdr](../Modules/mod_xml_cdr.md)是另一种常见的日志记录器，用于记录详细通话数据。 |
| Languages                                                    | 拨号计划中支持运行的脚本语言。最流行的是[Lua](../Modules/mod_lua/mod_lua.md)语言。也支持[JavaScript](../Client and Developer Interfaces/JavaScript/JavaScript.md)和其他一些脚本语言。 |

还有更多类型的模块，但这些是最常见的。有关公共模块列表详见 [Modules](../Modules/Modules.md) 。如果你想要一些现有模块没有的功能，你可以[写一个自己的模块](../Community/Community.md) 。模块可以用许多流行的编程语言编写。详见 [开发者文档](../Client and Developer Interfaces/Developer Documentation.md) 。

**API**

许多模块也有 API 命令，这些命令可以从命令行、脚本或者通过 socket 连接的远程计算机发出。但是一些常见的功能包括返回状态信息（例如查询一个会议中有多少人参与），或者控制当前运行的应用程序（例如暂停正在播放的文件）不同模块中有数百个 API 可以调用。在命令行中，您可以输入``show api``来查看已加载的模块的所有 API 命令。

内核提供的一些 API 命令，详见 [Commands](../Modules/mod_commands.md) 模块。

**文档导航**

此表提供了浏览该文档的结构化路线图。

| 页面                                                         | 描述                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [安装（Installation）](../Installation/Installation.md)      | 如何下载安装 Freeswitch                                      |
| [配置（Configuration）](Understanding the Configuration Files.md) | Freeswitch 配置文件概述                                      |
| [运行 Freeswitch](https://freeswitch.org/confluence/pages/viewpage.action?pageId=15696307) | 如何在控制台运行 Freeswitch 或者作为后台程序运行             |
| [Call Legs](Call Legs.md)                                    | 解释拨号计划和 Endpoints 的重要概念                          |
| [ Endpoints](Endpoints.md)                                   | 解释 Endpoint 一般的概念，以及对 common endpoint 更详细的概述。 |
| [拨号计划简介](https://freeswitch.org/confluence/pages/viewpage.action?pageId=15696304) | 拨号计划是 Freeswitch 最复杂的部分之一。                     |
| [Directory](../Directory/Directory.md)                       | 如何设置用户和设备                                           |
| 日志和通话流水                                               | 设置日志和通话记录                                           |
| [数据库](../Databases/FreeSWITCH Databases.md)               | 如何配置 Freeswitch 在数据库中存储 channel state。           |
| [Default Configuration](../Configuration/Default Configuration.md) | 设定默认配置                                                 |
| Session Scripts                                              | 如何通过编写在拨号计划中运行的脚本来自定义功能。[mod_lua](../Modules/mod_lua/mod_lua.md), [mod_python](../Modules/mod_python/mod_python.md), [mod_perl](../Modules/mod_perl/mod_perl.md), [mod_v8](../Modules/mod_v8.md) (for Google V8 JavaScript), [mod_java](../Modules/mod_java.md) |
| [Event Socket](../Client and Developer Interfaces/Event Socket Library/Event Socket Library.md) | 允许外部程序通过网络连接与 Freeswitch 交互。[CLI](../Client and Developer Interfaces/Command-Line Interface fs_cli.md) 使用 Event Socket 允许你运行命令并查看 Freeswitch 的输出。 |

