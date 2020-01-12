# 0.关于

变量本质上就是对信息进行一个命名，因此你可以创建一个变量叫做``local_ip_v4``来代替像``192.1689.1.1``这样的信息。现在当你需要指定 IP 地址时，可以直接使用``${local_ip_v4}``来引用变量而不是直接输入实际的 IP 地址。变量的值存储在你的服务器内存中，当你需要用到变量时，``Freeswitch``会从内存中提取变量的当前值。下面是使用变量的一些好处：

- 管理更改 - 通过使用变量定义 IP 地址，你只需要输入一次实际的 IP 地址，然后在需要 IP 地址的任何地方使用该变量。如果 IP 地址变了，你只需要改一个地方就可以。
- 可读性 - 通过对一个特殊值命名，可以更好的理解配置。例如，在配置文件中如果你看到一个数字``1000``，你不能确定这个数字是不是表示一个分机？或者是一个超时时长？你必须花时间尝试从上下文中理解这个数字。因此使用具有实际意义的变量名称，可以避免这样的猜测。
- 传递数据 - 因为``Freeswitch``是建立在模块化的架构上的，因此变量提供了不同模块直接共享数据的一种便捷方式。
- 方便配置 - ``Freeswitch``内核和许多模块的配置都有一些预定义的变量，这些通常都有一[Variables Master List](https://freeswitch.org/confluence/display/FREESWITCH/Variables+Master+List)个默认值，你可以修改这些变量的值。通过修改预定义变量的值可以实际控制``Freeswitch``的行为。

# 全局变量（Global Variable）

顾名思义，全局变量对于整个``Freeswitch``系统都是可用的，在所有通道（channels）中值都是相同的。它的目的是用于定义不经常更改的变量。

可以使用``set pre-processor``命令创建或修改配置中的全局变量。你还可以使用  [global_setvar](../../Modules/mod_commands.md) 这个 API 命令来设置全局变量。

``Freeswitch``内核以及一些模块有许多预设变量，一些在 [默认配置](../../Configuration/Default_Configuration.md) 文件 [vars.xml](../../Configuration/Configuring_FreeSWITCH/vars.xml.md) 中定义了，其他一些则由``Freeswitch``内核分配默认值。预定义变量详见[全局变量](Global_Variables.md) 页面。

# 通道变量（Channel Variables）

通道变量是指特定单个通道中的变量，例如主叫号码，被叫号码等等。你可以使用  [set](../../Modules/mod_dptools/mod_dptools_set.md)  来定义一个通道变量。因为通道变量是属于特定通道的，它们仅在具体通道的上下文中（例如在拨号计划中）或者在拨号计划中运行的脚本中可用。

# 使用变量（Retrieving Variables）

使用美元符号来使用变量，如``${variable_name}``。无论你在何处使用变量，``Freeswitch``引擎都会将它替换为变量的当前值。对于全局变量，所有通道中值都相同。通道变量仅仅在通道的上下文中可用，并且作为当前通道的值。例如，在拨号计划中，你可以根据 [被叫号码](../../Dialplan/Variables_Master_List.md) 创建规则。当拨号计划被作为一个通道时，它将查找这个通道中的被叫号码。

你还可以在 [CLI](../Client_and_Developer_Interfaces/Command-Line_Interface_fs_cli.md) 中使用  [eval](../../Modules/mod_dptools/mod_dptools_set.md)  命令检查当前全局变量的值。

```
$${variable_name} 和 ${variable_name} 的区别

对于使用变量时单个 $ 和两个 $ 作为前缀的困惑。在配置文件中，预处理器会删除使用两个 $ 的语法文本，并且查找到对应的全局变量值进行文本替换。如果没有找到对应的全局变量，则它的值为空。因为是由预处理器处理的，因此只有在配置文件加载到内存中时才会去检索值（启动时或重新加载时）。

单个 $ 的语法不受预处理器影响，它是在运行时实时检索值的，所以如果你在拨号计划中使用它，那么每一通电话都会重新检索值。因此如果你更改了全局变量，单个 $ 语法将直接获取到新值。另一个区别是单个 $ 语法即可以检索全局变量也可以检索通道变量，而两个 $ 只能检索全局变量。

为了不增加混淆，这种区别只存在于配置文件中。在脚本，CLI，API calls等等中，一个 $ 和两个 $ 的语法没有什么不同，两个都可以用于检索全局变量和通道变量，并且都是运行时实时检索。
```

# 系统定义变量（System Defined Variables）

除了使用 set 命令创建变量，``Freeswitch``内核和许多模块还创建加载了数百个变量。变量的完整列表详见 [主变量列表](../../Dialplan/Variables_Master_List.md) 。