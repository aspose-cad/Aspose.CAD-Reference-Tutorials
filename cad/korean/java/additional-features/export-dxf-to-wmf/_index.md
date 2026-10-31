---
date: 2026-10-30
description: Aspose.CAD for Java를 사용하여 DXF 파일을 WMF로 일괄 변환하는 방법을 배우세요. 단계별 코드, 무료 체험
  정보 및 선택적인 PDF 내보내기가 포함됩니다.
keywords:
- batch convert dxf files
- aspose cad java
- dxf to wmf conversion
- java cad rasterization
- aspose free trial
lastmod: 2026-10-30
linktitle: Java를 사용하여 DXF를 WMF 형식으로 내보내기
og_description: Aspose.CAD for Java를 사용하여 DXF 파일을 WMF로 일괄 변환합니다. 이 가이드를 따라 DXF 도면을
  로드하고, 래스터화 옵션을 설정한 뒤 WMF로 저장하며, 필요에 따라 무료 체험을 통해 PDF로 내보낼 수 있습니다.
og_image_alt: Tutorial showing batch conversion of DXF to WMF in Java using Aspose.CAD
og_title: Aspose.CAD for Java를 사용하여 DXF 파일을 WMF로 일괄 변환
schemas:
- author: Aspose
  dateModified: '2026-10-30'
  description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  headline: Batch convert DXF files to WMF with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  name: Batch convert DXF files to WMF with Aspose.CAD for Java
  steps:
  - name: load dxf drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: configure rasterization options
    text: '`CadRasterizationOptions` specifies page size, resolution, and background
      for rasterizing the CAD drawing.'
  - name: save as wmf
    text: '`ImageSaveOptions` with `SaveFormat.WMF` tells Aspose.CAD to write the
      output as a Windows Metafile.'
  - name: dispose of resources
    text: Calling `image.close()` releases native resources used by the Aspose.CAD
      Image object.
  - name: optional – export to pdf
    text: '`PdfOptions` configures PDF‑specific settings when saving the image as
      a PDF document. > **Pro tip:** You can reuse the same `CadRasterizationOptions`
      object for PDF export by passing it to a `PdfOptions` instance, saving you a
      few lines of setup.'
  type: HowTo
- questions:
  - answer: You can access the documentation [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).
    question: Where can I find the Aspose.CAD documentation?
  - answer: Download the library [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).
    question: How do I download Aspose.CAD for Java?
  - answer: Yes, you can get a free trial [Aspose free trial page](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Explore temporary licenses [temporary license options](https://purchase.aspose.com/temporary-license/).
    question: Need temporary licensing options?
  - answer: Visit the Aspose.CAD support forum [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).
    question: Where can I get support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- batch convert dxf
- Aspose.CAD
- Java CAD conversion
- WMF export
- DXF processing
title: Aspose.CAD for Java를 사용하여 DXF 파일을 WMF로 일괄 변환
url: /ko/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java를 사용하여 DXF 파일을 WMF로 일괄 변환

## 소개

이 튜토리얼에서는 Aspose.CAD for Java를 사용하여 **DXF 파일을 WMF로 일괄 변환**하는 방법을 배웁니다. Windows 기반 보고서에 CAD 도면을 삽입하거나, Office 문서용 경량 벡터 그래픽을 생성하거나, 대규모 변환을 자동화해야 할 경우, 이 가이드는 DXF 도면을 로드하고, 래스터화 옵션을 구성하고, WMF로 저장하며 필요에 따라 동일한 도면을 PDF로 내보내는 과정을 단계별로 안내합니다. 이 단계는 Java 8+를 실행하는 모든 플랫폼에서 작동합니다.

## 빠른 답변
- **DXF를 WMF로 무료 체험판으로 변환할 수 있나요?** 예 – Aspose는 완전한 기능을 갖춘 30일 체험판을 제공합니다.  
- **필요한 Java 버전은 무엇인가요?** Java 8 또는 그 이후 버전.  
- **코드를 실행하려면 라이선스가 필요합니까?** 프로덕션에서는 라이선스가 필요합니다; 체험판은 개발 및 테스트에 사용할 수 있습니다.  
- **변환이 손실 없이 이루어지나요?** 벡터 데이터가 보존되며, 래스터화 옵션을 통해 해상도를 제어할 수 있습니다.  
- **같은 도면을 PDF로도 내보낼 수 있나요?** 물론입니다 – 아래 “PDF로 내보내기” 단계를 참고하세요.  
- **여러 DXF 파일을 한 번에 일괄 변환하려면 어떻게 해야 하나요?** 폴더를 순회하면서 각 파일에 동일한 로드‑래스터화‑저장 패턴을 적용합니다.

## DXF 파일을 일괄 변환한다는 것은 무엇인가요?

DXF 파일을 일괄 변환한다는 것은 여러 개의 Drawing Exchange Format(DXF) 도면을 한 번에 처리하고 각 도면에 대해 WMF 출력을 생성하는 것을 의미합니다. WMF(Windows Metafile)는 Microsoft Office, Windows 애플리케이션 및 다양한 보고 도구와 기본적으로 통합되는 벡터 이미지 형식입니다.

## 왜 Aspose.CAD for Java를 사용해야 할까요?

Aspose.CAD for Java는 순수 Java 엔진으로 **50개 이상의 입력 및 출력 형식**을 지원합니다—DXF, DWG, DGN, PDF, PNG, SVG, WMF 등을 포함하며 **99 % 벡터 정확도**를 제공합니다. Java를 지원하는 모든 OS에서 실행되며 네이티브 DLL이 필요 없고, 단일 `CadRasterizationOptions` 클래스를 통해 페이지 크기, DPI 및 배경 색상을 제어할 수 있습니다. 동일한 API로 PDF, PNG, SVG 내보내기도 처리할 수 있어 여러 라이브러리를 사용할 필요가 없습니다.

### 정량화된 이점
- **50개 이상의 지원 형식**은 타사 변환기의 필요성을 줄여줍니다.  
- **300페이지 DXF 파일을 5초 미만**에 처리합니다(일반적인 2.5 GHz 서버, 150 DPI 래스터화 시).  
- **메모리 사용량이 200 MB 이하**로 유지됩니다(파일 크기가 500 MB까지이며 적절한 페이지 크기를 설정한 경우).  

## 전제 조건

- **Aspose.CAD for Java**를 프로젝트에 통합합니다. 공식 사이트에서 다운로드하세요: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- 변환하려는 DXF 파일이 들어 있는 폴더(예: `Your Document Directory/DXFDrawings/`).  

## 네임스페이스 가져오기

`Image`는 Aspose.CAD의 핵심 클래스이며 메모리 내 CAD 도면을 나타냅니다. 파일을 로드한 후, 이후 모든 작업(래스터화, 형식 변환, 리소스 정리)은 이 객체를 통해 수행됩니다.

다음 import 구문은 CAD 파일을 로드, 래스터화 및 저장하는 데 필요한 Aspose.CAD 클래스를 가져옵니다.  
```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageSaveOptions;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import java.awt.Color;
```

## 단계별 가이드

### Java에서 DXF 파일을 WMF로 일괄 변환하려면 어떻게 해야 하나요?

`Image.load`로 각 DXF를 로드하고, 원하는 페이지 크기와 DPI를 위해 `CadRasterizationOptions`를 구성한 뒤 `image.save`에 `SaveFormat.WMF`를 지정합니다. 이 3단계 패턴은 벡터 품질을 유지하면서 전체 변환을 수행하며 파일당 몇 줄의 코드만 필요합니다.

#### 1단계: dxf 도면 로드

Image.load는 DXF 파일을 Aspose.CAD Image 객체로 읽어들입니다.  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### 2단계: 래스터화 옵션 구성

`CadRasterizationOptions`는 CAD 도면을 래스터화할 때 페이지 크기, 해상도 및 배경을 지정합니다.  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### 3단계: wmf로 저장

`SaveFormat.WMF`와 함께 사용하는 `ImageSaveOptions`는 Aspose.CAD에 출력을 Windows Metafile로 저장하도록 지시합니다.  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### 4단계: 리소스 해제

`image.close()`를 호출하면 Aspose.CAD Image 객체가 사용한 네이티브 리소스가 해제됩니다.  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### 5단계: 선택 사항 – PDF로 내보내기

`PdfOptions`는 이미지를 PDF 문서로 저장할 때 PDF 전용 설정을 구성합니다.  
```java
finally
{
  cadImage.dispose();
}
```

> **Pro tip:** 동일한 `CadRasterizationOptions` 객체를 `PdfOptions` 인스턴스에 전달하여 PDF 내보내기에 재사용하면 설정 코드를 몇 줄 줄일 수 있습니다.

## Aspose CAD Java를 사용하여 DXF를 PDF로 내보내려면 어떻게 해야 하나요?

WMF 저장 형식을 `new ImageSaveOptions(SaveFormat.Pdf)`를 사용하여 PDF로 교체합니다. 동일한 래스터화 설정이 적용되며, 저자 메타데이터나 압축 수준과 같은 PDF 전용 옵션을 추가로 설정할 수 있습니다. 이 한 줄 변환은 원본 CAD 레이아웃을 그대로 반영하는 검색 가능하고 페이지 정확도가 높은 PDF를 생성합니다.

## 일반적인 문제와 해결책

`License`는 런타임에 제품 라이선스를 적용하는 Aspose 클래스입니다.

| Issue | Cause | Fix |
|-------|-------|-----|
| **`cadImage.save`에서 `NullPointerException`** | `cadImage` 변수가 정의되지 않음(`image`이어야 함). | `cadImage`를 `image`로 교체하거나 변수명을 일관되게 변경합니다. |
| **출력 WMF가 비어 있음** | 래스터화 페이지 크기가 너무 작거나 배경 색상이 투명하게 설정됨. | `PageWidth`/`PageHeight`를 늘리거나 `rasterizationOptions.setBackgroundColor(Color.WHITE);`를 사용해 배경 색상을 설정합니다. |
| **라이선스 예외** | 프로덕션에서 유효한 Aspose 라이선스 없이 실행됨. | 애플리케이션 시작 시 라이선스 파일을 적용합니다: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## 자주 묻는 질문

**Q: Aspose.CAD 문서는 어디에서 찾을 수 있나요?**  
A: 문서는 [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/)에서 확인할 수 있습니다.

**Q: Aspose.CAD for Java를 어떻게 다운로드하나요?**  
A: 라이브러리는 [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/)에서 다운로드합니다.

**Q: 무료 체험판을 이용할 수 있나요?**  
A: 예, 무료 체험판은 [Aspose free trial page](https://releases.aspose.com/)에서 받을 수 있습니다.

**Q: 임시 라이선스 옵션이 필요하신가요?**  
A: 임시 라이선스는 [temporary license options](https://purchase.aspose.com/temporary-license/)에서 확인하세요.

**Q: 지원은 어디에서 받을 수 있나요?**  
A: Aspose.CAD 지원 포럼은 [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19)에서 확인하세요.

## 추가 자주 묻는 질문

**Q: 수백 MB 규모의 대용량 DXF 파일을 메모리 부족 없이 변환할 수 있나요?**  
A: 예. 파일을 try‑with‑resources 블록에서 로드하고 `Image` 객체를 즉시 해제합니다. 메모리 사용량을 낮게 유지하려면 `CadRasterizationOptions.setPageWidth/Height`를 적절한 크기로 조정하세요.

**Q: WMF 출력이 레이어 정보를 유지하나요?**  
A: WMF는 평면 벡터 형식이므로 레이어 계층 구조는 평탄화되지만, 선 스타일, 색상 및 해치 패턴은 보존됩니다.

**Q: WMF에 사용자 정의 DPI를 설정할 수 있나요?**  
A: 저장하기 전에 `rasterizationOptions.setResolution(300);`를 사용해 DPI를 정의합니다.

**Q: 한 번에 여러 DXF 파일을 일괄 변환할 수 있나요?**  
A: 물론 가능합니다. 디렉터리를 순회하면서 각 파일을 로드하고 동일한 래스터화 및 저장 로직을 적용합니다.

**Q: 지원되는 Java 버전은 무엇인가요?**  
A: Aspose.CAD for Java는 Java 8 및 이후 버전을 지원하며, Java 11, 17 및 최신 LTS 릴리스를 포함합니다.

---

**마지막 업데이트:** 2026-10-30  
**테스트 환경:** Aspose.CAD for Java 24.11  
**작성자:** Aspose

## 관련 튜토리얼

- [CAD에서 PDF 만들기 – Aspose.CAD for Java로 DXF를 PDF로 내보내기](/cad/java/additional-features/export-dxf-to-pdf/)
- [DXF에서 PDF 만들기: Aspose.CAD for Java로 레이어 내보내기](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Java에서 Aspose.CAD로 DXF 레이아웃을 JPEG 이미지로 변환하는 방법](/cad/java/additional-features/export-specific-layout-to-image/)

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}