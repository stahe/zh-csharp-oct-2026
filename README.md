# 使用 .NET 10 学习 C# 14

📖 **阅读教程：[https://stahe.github.io/zh-csharp-oct-2026/](https://stahe.github.io/zh-csharp-oct-2026/)**

本课程**通过实践示例**讲授 [C#](https://learn.microsoft.com/fr-fr/dotnet/csharp/) 14 语言和 [.NET](https://dotnet.microsoft.com) 10 平台：两百多个程序（近 300 个 C# 文件），逐行加以注释，并附有其执行结果。课程从语言基础开始，涵盖数据库访问、网络编程和 Web 服务。

这是对课程《[使用 .NET 3.5 框架学习 C# 语言 3.0 版](https://stahe.github.io/zh-csharp-mai-2008/)》（2008 年）面向 C# 14 和 .NET 10 的重写：提纲相同，示例相同，贯穿始终的主题也相同，但代码已是最新的。所有程序使用 .NET 10 SDK 编译，**没有错误或警告**，并且都已运行；课程中展示的结果就是这些运行的结果。

| C# 3.0 课程（2008） | C# 14 课程（2026） |
|---|---|
| C# 3.0，.NET 3.5 框架，仅限 Windows | C# 14，.NET 10（LTS），Windows、Linux、macOS |
| Visual C# 2008 Express | VS Code + C# Dev Kit 或 Visual Studio 2026，`dotnet` 命令 |
| `.sln` 项目和解决方案 | 单文件应用程序（`dotnet run prog.cs`），`.slnx` 解决方案 |
| Windows Forms 图形用户界面 | 该章已删除（界面现在都基于 Web） |
| LINQ“未涉及” | 详细讲解 LINQ |
| `ArrayList`、`Hashtable`、`BinaryFormatter` | 泛型集合，`System.Text.Json` |
| NUnit 2.4，Spring.NET | MSTest 4，Microsoft.Extensions.DependencyInjection |
| `BackgroundWorker`，`BeginXxx` / `EndXxx` 模式 | `Task`，`async` / `await`，取消，`IAsyncEnumerable` |
| SQL Server 2005，ODBC，OLE DB | MySQL 8（Laragon），MySqlConnector，Entity Framework Core |
| `WebClient`，`WebRequest` | 异步 `HttpClient`，`TcpClient` / `TcpListener` |
| SOAP ASMX Web 服务 | 使用 ASP.NET Core Minimal API 的 REST / JSON Web 服务 |

## 课程提纲

| 章节 | 内容 |
|---|---|
| 安装 | .NET 10 SDK，VS Code / Visual Studio 2026，`dotnet` 命令，单文件应用程序，项目，`.slnx` 解决方案 |
| 语言基础 | 类型、字面量、可空类型、转换、数组、索引和范围、运算符（`??`、`??=`）、`switch` 表达式和模式匹配、异常、枚举、参数传递、本地函数、元组 |
| 类、结构、接口 | 属性（`init`、`required`、C# 14 的 `field` 关键字）、继承、多态、运算符、索引器、结构、接口、泛型、记录、主构造函数、C# 14 扩展成员、可空引用类型 |
| 常用的 .NET 类 | 字符串、数组、集合、**LINQ**、文本和二进制文件、JSON、正则表达式（`[GeneratedRegex]`） |
| 分层架构 | [DAO] / [业务] / [UI] 层，**MSTest** 单元测试，**依赖注入** |
| 委托、lambda 和事件 | `Func`、`Action`、lambda 表达式、闭包、事件、表达式树 |
| 执行线程 | `Thread`、同步（C# 13 的 `Lock`、`Monitor`、`Interlocked`……）、并发集合、`Parallel` |
| **异步编程**（新增） | `Task`、`async` / `await`、`WhenAll`、取消、进度、异步流、`Parallel.ForEachAsync`、`Channel<T>` |
| 使用 ADO.NET 访问数据库 | MySQL、`MySqlConnector`、参数化查询与 SQL 注入、事务、异步方法、`DbProviderFactory` |
| **Entity Framework Core**（新增） | 模型、CRUD、LINQ-to-SQL、关系、迁移、乐观并发、原生 SQL、依赖注入 |
| Web 编程 | TCP/IP、IPv6、异步 TCP 客户端和服务器、HTTP、`HttpClient`、SMTP |
| Web 服务 | 使用 ASP.NET Core Minimal API 的 REST / JSON、控制台客户端、JavaScript Web 客户端 |

## 贯穿始终的主线：9 个版本的所得税计算器

在整个课程中，我们逐个版本地构建一个**所得税计算器**应用程序：

- **版本 1**：单个程序；**版本 2**：类和接口；**版本 3**：从文本或 JSON 文件读取数据；
- **版本 4 和 5**：分层架构，使用 MSTest 测试，并通过依赖注入集成；
- **版本 6 和 7**：数据存放在 MySQL 数据库中，先用 ADO.NET 读取，再用 Entity Framework Core 读取；
- **版本 8**：一个税款计算 TCP 服务器及其客户端；
- **版本 9**：一个 REST Web 服务、它的控制台客户端和它的 Web 客户端。

## 技术

C# 14 · .NET 10 · VS Code · Visual Studio 2026 · MSTest 4 · Microsoft.Extensions.DependencyInjection · System.Text.Json · MySQL 8 · MySqlConnector · Entity Framework Core 9 · Pomelo.EntityFrameworkCore.MySql · ASP.NET Core 10 · Laragon

## 先决条件

- 具备任意一种语言的编程经验。
- [.NET 10 SDK](https://dotnet.microsoft.com/download/dotnet/10.0) 和一个代码编辑器（安装了 C# Dev Kit 扩展的 [VS Code](https://code.visualstudio.com)，或 Visual Studio 2026）；用于 MySQL 的 [Laragon](https://laragon.org)（数据库相关章节）。课程中提供了安装说明。

## 作者

本课程及其代码由 **Claude**（来自 [Anthropic](https://www.anthropic.com) 的 AI）应 Serge Tahé 的请求，基于他 2008 年的 C# 课程编写（2026 年 10 月）。

审阅者：[Serge Tahé](https://stahe.github.io)
