---
title: 探索 DWG 文件的底层标志 - Aspose.CAD 教程
linktitle: 探索 DWG 文件的参考底图标记
second_title: Aspose.CAD .NET - CAD 和 BIM 文件格式
description: 释放 Aspose.CAD for .NET 在探索 DWG 文件底层标记方面的强大功能。请遵循我们的分步指南。
type: docs
weight: 13
url: /zh/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
---
## 介绍

如果您正在深入研究 CAD 文件（特别是 DWG 文件）的复杂世界，并且想要解开底层标志的神秘面纱，那么您来对地方了。本教程将引导您完成使用强大的 Aspose.CAD for .NET 库探索 DWG 文件中的底层标志的过程。

## 先决条件

在我们深入学习本教程之前，请确保您具备以下条件：

- 对 C# 和 .NET 编程有基本了解。
- 安装了 Aspose.CAD for .NET 库。如果没有的话可以下载[这里](https://releases.aspose.com/cad/net/).
- 用于测试的 DWG 文件。您可以使用教程中提供的示例文件“BlockRefDgn.dwg”。

## 导入命名空间

首先，您需要导入必要的命名空间。这是一个可以帮助您的片段：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;

```

## 第 1 步：加载 DWG 文件并转换为 CadImage

首先加载现有的 DWG 文件并将其转换为 CadImage：

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

//加载 DWG 文件并转换为 CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    //您后续步骤的代码将位于此处
}
```

## 第 2 步：迭代实体

接下来，迭代 DWG 文件中的每个实体：

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    //您后续步骤的代码将位于此处
}
```

## 步骤 3：检查 CadDgnUnderlay 类型

检查实体是否为 CadDgnUnderlay 类型：

```csharp
if (entity is CadDgnUnderlay)
{
    //您后续步骤的代码将位于此处
}
```

## 第 4 步：访问底层标志

访问不同的底层标志并提取相关信息：

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

## 结论

恭喜！您已使用 Aspose.CAD for .NET 成功探索了 DWG 文件的底层标记。本教程为您提供了导航实体和提取有关底层的重要信息的知识。

## 常见问题解答

### Q1：我可以将 Aspose.CAD for .NET 与其他 CAD 文件格式一起使用吗？

A1：Aspose.CAD支持多种CAD格式，包括DWG、DXF、DGN等。检查文档以获取完整列表。

### 问题 2：Aspose.CAD for .NET 是否有临时许可证？

 A2：是的，您可以获得临时许可证[这里](https://purchase.aspose.com/temporary-license/).

### 问题 3：在哪里可以找到对 Aspose.CAD for .NET 的支持？

 A3：访问支持论坛[这里](https://forum.aspose.com/c/cad/19)寻求帮助。

### Q4：如何购买 Aspose.CAD for .NET？

A4：购买图书馆[这里](https://purchase.aspose.com/buy).

### Q5: 有免费试用吗？

 A5：是的，您可以免费试用[这里](https://releases.aspose.com/).
