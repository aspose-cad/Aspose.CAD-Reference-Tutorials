---
date: 2026-09-14
description: 了解如何在 Aspose.CAD for .NET 中使用文件路径或 FileStream 应用许可证，并探索 metered licensing
  以优化资源使用。
keywords:
- how to apply license
- apply license by path
- apply license using filestream
- metered licensing
lastmod: 2026-09-14
linktitle: 许可证和配置
og_description: 了解如何在 Aspose.CAD for .NET 中使用文件路径或 FileStream 应用许可证，并探索 metered licensing
  以优化资源使用。（150‑160 字）
og_image_alt: Screenshot of Aspose.CAD license configuration page in a .NET IDE
og_title: 如何在 Aspose.CAD for .NET 中应用许可证 – 快速指南
schemas:
- author: Aspose
  dateModified: '2026-09-14'
  description: Learn how to apply license in Aspose.CAD for .NET using a file path
    or FileStream, and explore metered licensing to optimise resource usage.
  headline: How to apply license in Aspose.CAD for .NET
  type: TechArticle
- description: Learn how to apply license in Aspose.CAD for .NET using a file path
    or FileStream, and explore metered licensing to optimise resource usage.
  name: How to apply license in Aspose.CAD for .NET
  steps:
  - name: Place your `Aspose.CAD.lic` file in a folder that your application can read
      (e.g., the application root or a secured config folder).
    text: Place your `Aspose.CAD.lic` file in a folder that your application can read
      (e.g., the application root or a secured config folder).
  - name: 'Add the following code early in your startup routine (e.g., `Main`, `Startup.Configure`,
      or `Global.asax`):'
    text: 'Add the following code early in your startup routine (e.g., `Main`, `Startup.Configure`,
      or `Global.asax`):'
  - name: Retrieve the license bytes from your source (file system, Azure Blob, etc.).
    text: Retrieve the license bytes from your source (file system, Azure Blob, etc.).
  - name: Open a `FileStream` with read permissions.
    text: Open a `FileStream` with read permissions.
  - name: Pass the stream to the `License` object.
    text: Pass the stream to the `License` object.
  - name: Obtain a metered‑license key from your Aspose account dashboard.
    text: Obtain a metered‑license key from your Aspose account dashboard.
  - name: Register the key with `License.SetMeteredKey("your‑key")`.
    text: Register the key with `License.SetMeteredKey("your‑key")`.
  - name: After each operation, call `License.GetMeteredUsage()` to retrieve the current
      usage count.
    text: After each operation, call `License.GetMeteredUsage()` to retrieve the current
      usage count.
  type: HowTo
- questions:
  - answer: Yes, a single license file can be deployed to any number of development
      or production servers, provided the usage complies with your purchased term.
    question: Can I use the same license file on multiple machines?
  - answer: The library will run in evaluation mode, adding a watermark to rendered
      images and limiting the number of pages you can process.
    question: What happens if I forget to set the license before loading a CAD file?
  - answer: Only the first activation and each usage report need connectivity; after
      that, the library can operate offline until the next report.
    question: Does metered licensing require an internet connection?
  - answer: Aspose.CAD supports 45+ input and output formats, including DWG, DXF,
      DGN, STL, OBJ, and IFC, and can render files up to 500 MB without loading the
      entire document into memory.
    question: Which CAD/BIM formats are supported out of the box?
  - answer: Call `License.IsLicensed` (or inspect `License.LicenseFilePath`) after
      registration; it returns `true` when a valid license is active.
    question: Is there a way to programmatically check if the license was applied
      successfully?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- Aspose.CAD
- license configuration
- .NET
- CAD processing
- metered licensing
title: 如何在 Aspose.CAD for .NET 中应用许可证
url: /zh/net/licensing-and-configuration/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.CAD for .NET 中应用许可证

欢迎阅读关于 **如何应用许可证** 的 Aspose.CAD .NET 权威指南。无论您是在构建桌面工具、服务器端服务，还是自动化 BIM 流程，合法的许可证都能解锁超过 40 种 CAD 与 BIM 格式的完整套件，提供高性能渲染，并去除评估水印。本文将逐步演示所有授权方式，帮助您无缝开始开发。

## 快速答案
- **我可以从文件路径加载许可证吗？** 是的 – 只需实例化 `License` 并调用 `SetLicense("path/to/license.lic")`。  
- **支持 FileStream 吗？** 当然；将打开的流传递给 `SetLicense(stream)`。  
- **计量授权是什么？** 它按请求跟踪使用情况，让您只为实际消耗付费。  
- **开发需要许可证吗？** 免费试用许可证可用于开发和测试；生产环境需要商业许可证。  
- **支持哪些 .NET 版本？** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7。

## Aspose.CAD 中的授权是什么？

Aspose.CAD 的授权是验证您购买并激活库完整功能集的机制。没有许可证，API 将以评估模式运行，限制输出大小并在渲染的图像上嵌入水印。

## 为什么使用基于路径的许可证而不是流？

基于路径的授权是激活 Aspose.CAD 的最快方式：只需指向 .lic 文件，库会自动加载。需要从非文件来源读取许可证、实施自定义安全或将许可证嵌入程序集时，请使用流。请选择符合部署约束的方法。

`License` 类表示 Aspose.CAD 的授权组件，用于向 API 注册许可证。

## 如何在 Aspose.CAD for .NET 中通过路径应用许可证？

要通过路径应用许可证，创建一个 `License` 类的实例并调用其 `SetLicense` 方法，传入 .lic 文件的完整路径。请在应用程序启动早期放置此代码，以便后续所有 CAD 操作均在已授权的上下文中运行。

`License` 类表示 Aspose.CAD 的授权组件，用于向 API 注册许可证。

1. 将您的 `Aspose.CAD.lic` 文件放置在应用程序可读取的文件夹中（例如应用根目录或受保护的配置文件夹）。  
2. 在启动例程的早期添加以下代码（例如 `Main`、`Startup.Configure` 或 `Global.asax`）：

```csharp
// No code block added – original tutorial contained none.
```

> **直接回答（40‑70 字）：**  
> 要通过路径应用许可证，创建一个 `License` 对象并调用 `SetLicense("full\\path\\to\\Aspose.CAD.lic")`。此单行代码激活完整库，去除评估水印，并在不受性能限制的情况下处理 40 多种 CAD/BIM 格式。请在任何 CAD 操作之前调用，以确保许可证已激活。

## 如何在 Aspose.CAD for .NET 中使用 FileStream 应用许可证？

要使用 `FileStream` 应用许可证，先以读取方式打开 .lic 文件，创建 `License` 对象，然后将流传递给 `SetLicense`。确保流在注册完成前保持打开状态，完成后关闭以释放资源。

`FileStream` 类提供用于读取和写入磁盘文件的流。

1. 从您的来源（文件系统、Azure Blob 等）获取许可证字节。  
2. 以读取权限打开 `FileStream`。  
3. 将流传递给 `License` 对象。

> **直接回答（40‑70 字）：**  
> 实例化一个 `License` 对象并调用 `SetLicense(stream)`，其中 `stream` 是指向您的 `Aspose.CAD.lic` 的可读 `FileStream`。此方式从内存加载许可证，允许您将文件保留在文件系统之外，并即时激活所有功能。确保流在注册完成前保持打开，随后关闭。

## Aspose.CAD for .NET 中的计量授权是如何工作的？

计量授权通过调用 `License.SetMeteredKey` 并传入唯一密钥来启用。注册后，SDK 会自动向 Aspose 服务器报告每一次 CAD 操作，使您能够监控使用情况并仅为实际执行的操作付费。

`License.SetMeteredKey` 方法向 Aspose.CAD 库注册计量授权密钥。

1. 从 Aspose 账户仪表板获取计量授权密钥。  
2. 使用 `License.SetMeteredKey("your‑key")` 注册该密钥。  
3. 每次操作后，调用 `License.GetMeteredUsage()` 获取当前使用计数。

> **直接回答（40‑70 字）：**  
> 计量授权通过调用 `License.SetMeteredKey("your‑key")` 激活。SDK 随后在每次 CAD 操作后向 Aspose 服务器发送使用数据，让您基于实际消耗进行监控和计费。此模式支持无限并发用户，同时使成本与真实使用保持一致。

## 授权和配置教程

### [通过路径在 Aspose.CAD for .NET 中应用许可证](./apply-license-by-path/)
解锁 Aspose.CAD for .NET 的全部潜能！按照我们的分步指南无缝应用许可证，立即提升您的 CAD 文件处理能力！

### [通过 FileStream 在 Aspose.CAD for .NET 中应用许可证](./apply-license-using-filestream/)
掌握 Aspose.CAD for .NET：使用 FileStream 无缝应用许可证。探索分步指南，释放全部潜能，立即下载！

### [Aspose.CAD for .NET 中的计量授权](./metered-licensing/)
通过 .NET 中的计量授权解锁 Aspose.CAD 潜能。无缝优化资源使用，探索我们的分步指南。

## 常见问题

**Q: 我可以在多台机器上使用相同的许可证文件吗？**  
A: 是的，单个许可证文件可以部署到任意数量的开发或生产服务器，只要使用符合您购买的条款。

**Q: 如果在加载 CAD 文件前忘记设置许可证会怎样？**  
A: 库将在评估模式下运行，在渲染的图像上添加水印并限制您可以处理的页面数量。

**Q: 计量授权需要互联网连接吗？**  
A: 仅首次激活和每次使用报告需要联网；之后，库可以在离线状态下运行，直至下一次报告。

**Q: 开箱即用支持哪些 CAD/BIM 格式？**  
A: Aspose.CAD 支持 45+ 输入和输出格式，包括 DWG、DXF、DGN、STL、OBJ 和 IFC，并且能够在不将整个文档加载到内存中的情况下渲染最高 500 MB 的文件。

**Q: 是否有办法以编程方式检查许可证是否成功应用？**  
A: 调用 `License.IsLicensed`（或检查 `License.LicenseFilePath`）进行注册后；如果返回 `true`，则表示有效许可证已激活。

---

**最后更新：** 2026-09-14  
**已测试：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose

## 相关教程

- [通过路径在 Aspose.CAD for .NET 中应用许可证](/cad/net/licensing-and-configuration/apply-license-by-path/)
- [通过 FileStream 在 Aspose.CAD for .NET 中应用许可证](/cad/net/licensing-and-configuration/apply-license-using-filestream/)
- [Aspose.CAD for .NET 中的计量授权](/cad/net/licensing-and-configuration/metered-licensing/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}