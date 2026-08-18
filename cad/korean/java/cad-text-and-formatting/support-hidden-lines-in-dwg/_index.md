---
date: 2026-03-05
description: 이 단계별 튜토리얼에서 Aspose.CAD for Java를 사용하여 DWG를 PDF로 내보내고, 숨은 선을 활성화하며, DWG를
  PDF로 변환하는 방법을 배워보세요.
linktitle: Export DWG as PDF Using Java
second_title: Aspose.CAD Java API
title: 숨겨진 선을 포함한 DWG를 PDF로 내보내기 – Aspose.CAD for Java
url: /ko/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 숨은 선을 포함한 DWG를 PDF로 내보내기 – Aspose.CAD for Java

## Introduction

이 튜토리얼에서는 Aspose.CAD for Java를 사용하여 **export dwg to pdf** 를 수행하면서 숨은 선을 유지하는 방법을 배웁니다. **DWG를 PDF로 변환** 하거나, **dwg to pdf tutorial** 형식의 가이드를 만들거나, 단순히 **DWG를 PDF로 저장** 하면서 숨은 선을 지원하고 싶을 때, 단계별로 안내해 드립니다. 끝까지 따라오시면 Java 프로젝트에 바로 적용할 수 있는 완전한 솔루션을 얻을 수 있습니다.

## Quick Answers
- **What does this tutorial cover?** Aspose.CAD for Java를 사용하여 DWG를 PDF로 내보낼 때 숨은 선 렌더링을 활성화하는 방법.  
- **Which primary operation is performed?** `export dwg to pdf`.  
- **Do I need a license?** 테스트용 무료 체험판을 사용할 수 있으며, 실제 운영 환경에서는 상용 라이선스가 필요합니다.  
- **What are the prerequisites?** Java 개발 환경, Aspose.CAD for Java 라이브러리, 그리고 DWG 파일.  
- **How long does implementation take?** 기본 설정 기준으로 약 10‑15분 정도 소요됩니다.

## What is “export dwg to pdf”?
DWG 파일을 PDF로 내보내면 벡터 기반 CAD 도면을 휴대용 문서 형식으로 변환하면서 레이어, 라인 타입 및 선택적인 숨은 선 렌더링을 유지합니다. 이를 통해 CAD 소프트웨어가 없는 이해관계자와도 설계도를 쉽게 공유할 수 있습니다.

## How to Enable Hidden Lines When Exporting DWG to PDF
숨은 선은 래스터화 옵션의 레이아웃 설정을 통해 제어됩니다. **Model** 레이아웃을 선택하면 Aspose.CAD가 숨은 에지를 보이지 않게 처리하여 3‑D 모델을 2‑D로 깔끔하게 표현합니다.

## Why enable hidden lines when exporting?
숨은 선을 포함하면 복잡한 3‑D 모델을 2‑D 페이지에 표시할 때 가시적인 가장자리만 강조되어 시각적 가독성이 향상됩니다. 이는 엔지니어링 문서에서 흔히 요구되는 사항입니다.

## Prerequisites

1. **Aspose.CAD for Java** – 공식 사이트에서 라이브러리를 다운로드하세요 [here](https://releases.aspose.com/cad/java/).  
2. **DWG files** – 소스 DWG 도면을 미리 지정된 디렉터리에 보관합니다.  
3. **Java development environment** – JDK 8 이상 및 선호하는 IDE(Eclipse, IntelliJ 등).  

준비가 끝났다면 코드 작성을 시작해 보겠습니다.

## Import Namespaces

CAD 이미지와 PDF 옵션을 다루기 위해 필요한 클래스를 임포트합니다.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## Step 1: Set Up Your Project

Java 프로젝트를 생성하고 Aspose.CAD JAR 파일을 빌드 경로에 추가합니다. 그런 다음 DWG 파일이 위치한 디렉터리를 정의합니다.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **Pro tip:** 절대 경로를 사용하거나 프로젝트의 resources 폴더를 기준으로 상대 경로를 설정하세요.

## Step 2: Load DWG File

소스 DWG 파일을 `CadImage` 객체에 로드하여 조작할 수 있게 합니다.

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## Step 3: Configure Rasterization Options

포함할 레이어를 선택하고 페이지 크기를 원본 도면에 맞게 설정합니다. 여기서 레이아웃을 지정해 숨은 선 렌더링을 활성화합니다.

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## Step 4: Set PDF Options

Aspose.CAD에 벡터 데이터를 PDF로 래스터화하도록 지시하고, “Model” 레이아웃을 사용해 숨은 선을 숨깁니다.

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Step 5: Save the Result

마지막으로 DWG를 PDF 파일로 내보냅니다. 설정한 레이아웃에 따라 숨은 선이 올바르게 처리됩니다.

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **Common Pitfall:** 레이아웃을 `"Model"` 로 설정하지 않으면 모든 선(숨은 선 포함)이 PDF에 실선으로 표시됩니다.

## Common Issues and Solutions

| Issue | Why it Happens | How to Fix |
|-------|----------------|------------|
| PDF shows all lines solid | Layout not set to **Model** | Ensure `rasterizationOptions.setLayouts(new String[] { "Model" });` is called before saving. |
| Missing layers in output | Incorrect layer names | Verify the layer names in the DWG file and match them exactly in the `list`. |
| Out‑of‑memory error on large files | Large rasterization size | Reduce page dimensions or process the drawing in chunks if possible. |

## Frequently Asked Questions

### Q1: Can I use Aspose.CAD for Java with other CAD file formats?
A1: Yes, Aspose.CAD supports various CAD formats such as DWG, DXF, DWF, and more.

### Q2: Is there a free trial available for Aspose.CAD for Java?
A2: Yes, you can find the free trial [here](https://releases.aspose.com/).

### Q3: How do I get support for Aspose.CAD for Java?
A3: Visit the Aspose.CAD forum [here](https://forum.aspose.com/c/cad/19) for community support.

### Q4: Where can I find detailed documentation for Aspose.CAD for Java?
A4: Refer to the documentation [here](https://reference.aspose.com/cad/java/).

### Q5: Can I purchase a temporary license for Aspose.CAD for Java?
A5: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).

### Q6: Does this method also work for converting DWG to PDF in a headless server environment?
A6: Absolutely. Since the code uses only the Aspose.CAD API, it runs without any UI dependencies, making it ideal for server‑side automation.

## Conclusion

이제 Aspose.CAD for Java를 사용해 숨은 선을 지원하는 **export dwg to pdf** 방법을 완전하게 구현했습니다. 이 접근 방식은 배치 처리 도구, 웹 서비스, 데스크톱 애플리케이션 등에 통합하여 CAD‑to‑PDF 변환을 자동화할 수 있습니다.

---

**Last Updated:** 2026-03-05  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}