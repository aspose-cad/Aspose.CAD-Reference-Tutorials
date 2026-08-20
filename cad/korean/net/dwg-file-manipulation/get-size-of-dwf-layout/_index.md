---
date: 2026-04-06
description: Aspose.CAD를 사용하여 C#에서 DWF를 JPG로 변환하는 방법을 배우고, DWG 파일에서 DWF 레이아웃 크기를 추출하는
  방법을 알아보세요.
keywords:
- convert dwf to jpg
- how to extract dwf
- convert dwg to jpg
linktitle: C#에서 DWG 파일 작업 - DWF 레이아웃 크기 가져오기
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: C#에서 DWF를 JPG로 변환 – DWG에서 DWF 레이아웃 크기 가져오기
url: /ko/net/dwg-file-manipulation/get-size-of-dwf-layout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C#에서 DWF를 JPG로 변환 – DWG에서 DWF 레이아웃 크기 가져오기

## 소개

If you need to **DWF를 JPG로 변환** while also figuring out the exact layout dimensions, you’re in the right place. In this tutorial we’ll walk through a complete, end‑to‑end example that uses Aspose.CAD for .NET to open a DWG‑derived DWF file, read each layout’s size, and save the layout as a high‑quality JPG image. By the end you’ll not only know how to extract DWF layout information but also have a reusable code snippet you can drop into any C# project.

## 빠른 답변
- **“DWF를 JPG로 변환”은 무엇을 의미하나요?** It means rasterizing a vector DWF layout into a bitmap JPEG image.  
- **먼저 레이아웃 크기를 읽는 이유는?** Knowing the exact extents lets you set the correct page dimensions, avoiding stretched or clipped output.  
- **어떤 라이브러리가 이를 처리하나요?** Aspose.CAD for .NET provides full support for DWG, DWF and raster image conversion.  
- **라이선스가 필요합니까?** A temporary license works for evaluation; a full license is required for production.  
- **지원되는 .NET 버전은?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## “DWF를 JPG로 변환”이란 무엇이며 왜 중요한가요?

Converting a DWF (Design Web Format) file to JPG creates a portable image that can be displayed in browsers, embedded in reports, or shared with stakeholders who don’t have CAD software. The conversion also gives you the flexibility to manipulate the image (resize, compress, watermark) using standard image‑processing tools.

## DWF 레이아웃 크기를 추출해야 하는 이유

A DWF file can contain multiple layouts, each with its own coordinate system and units (inches, millimeters, etc.). Extracting the layout size lets you:

1. Preserve the original aspect ratio when rasterizing.  
2. Choose the correct DPI for high‑resolution output.  
3. Automate batch processing of many layouts without manual tweaking.

## 사전 요구 사항

To follow this tutorial seamlessly, make sure you have the following prerequisites in place:

- Aspose.CAD for .NET: Ensure that you have Aspose.CAD for .NET installed. You can download it from the [Aspose.CAD for .NET 다운로드 페이지](https://releases.aspose.com/cad/net/).

Having the library ready means you can focus on the code rather than hunting down dependencies.

## 네임스페이스 가져오기

Before we start coding, import the required namespaces. These provide the classes we’ll need to work with CAD files, rasterization options, and file I/O.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## 단계 1: 환경 설정

Create a new C# console or class‑library project, add a reference to the **Aspose.CAD.dll**, and ensure the project targets a compatible .NET version.

## 단계 2: 파일 경로 정의 (DWF 추출 방법)

Specify where your source DWF file lives and where the generated JPG files should be written.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

> **Pro tip:** Use `Path.Combine(MyDir, "blocks_and_tables.dwf")` for safer path handling on different OSes.

## 단계 3: DWF 이미지 로드

Load the DWF file into an `Aspose.CAD.Image` object. We cast it to `DwfImage` because we need access to page‑specific properties.

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Code for further steps will go here
}
```

## 단계 4: 페이지 순회

A DWF can contain several pages (layouts). Loop through each one so we can process them individually.

```csharp
foreach (var page in image.Pages)
{
    // Code for further steps will go here
}
```

## 단계 5: 레이아웃 정보 가져오기

Inside the loop, retrieve the layout name. This name will be used both for logging and for naming the output JPG file.

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## 단계 6: JPG 옵션 설정

Create a `JpegOptions` instance and configure rasterization options. The `Layouts` property tells Aspose.CAD which layout to render.

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Code for further steps will go here
}
```

## 단계 7: 페이지 크기 결정 (dwg를 jpg로 변환)

Calculate the width and height of the layout in its native units. This information is essential for setting the raster page size correctly.

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Code for further steps will go here
```

## 단계 8: 페이지 차원 설정

Convert the native units (inch or millimeter) to pixels using the helper methods provided by Aspose.CAD. If the unit type is neither, we fall back to using the raw values.

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## 단계 9: JPG 파일 저장

Finally, bind the rasterization options to the JPEG options and save the image to disk.

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

When the loop finishes, you’ll have a JPG file for each layout, each sized exactly to match the original DWF dimensions.

## 일반적인 문제와 해결책

| 증상 | 가능 원인 | 해결 방법 |
|---------|--------------|-----|
| Empty JPG output | `options.Layouts` not set correctly | Verify the layout name matches `page.Name`. |
| Distorted image | Wrong DPI conversion | Use `CommonHelper.DPI = 300` (or your target DPI) before conversion. |
| File not found | Incorrect `MyDir` path | Use absolute paths or `Path.Combine`. |
| License exception | No license applied | Load a temporary or permanent license before calling `Image.Load`. |

## 자주 묻는 질문

### Q1: Aspose.CAD가 최신 DWG 파일 형식을 지원하나요?

A1: Aspose.CAD supports various DWG file formats, including the latest versions. Refer to the [documentation](https://reference.aspose.com/cad/net/) for specific compatibility details.

### Q2: Aspose.CAD를 상업용 및 개인 프로젝트 모두에 사용할 수 있나요?

A2: Yes, Aspose.CAD offers flexible licensing options for both commercial and personal use. Visit the [purchase page](https://purchase.aspose.com/buy) for more details.

### Q3: Aspose.CAD 임시 라이선스는 어떻게 얻나요?

A3: You can get a temporary license from [here](https://purchase.aspose.com/temporary-license/) for evaluation purposes.

### Q4: Aspose.CAD 지원을 어디서 받을 수 있나요?

A5: For any queries or assistance, visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

### Q5: Aspose.CAD 무료 체험판이 있나요?

A5: Yes, you can access a free trial version of Aspose.CAD [here](https://releases.aspose.com/).

### Q6: DWG 파일을 직접 JPG로 변환하려면 어떻게 해야 하나요?

A6: You can load the DWG file with `Aspose.CAD.Image.Load` and use the same rasterization workflow; just set `options.Layouts` to the desired layout name(s) from the DWG.

### Q7: 변환이 벡터 품질을 유지하나요?

A7: Once rasterized to JPG, the image is bitmap‑based, so vector scalability is lost. For lossless scaling, consider exporting to PNG or SVG instead.

---

**Last Updated:** 2026-04-06  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}