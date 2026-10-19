---
date: 2026-10-19
description: Aspose.CAD를 사용하여 Java에서 DWG를 PDF로 변환하는 방법을 배웁니다. 이 단계별 가이드는 AutoCAD PDF를
  내보내고, CAD를 PDF로 저장하며, 라이선스를 적용하는 방법을 보여줍니다.
keywords:
- dwg to pdf java
- export autocad pdf
- java pdf export library
- aspose cad license
- save cad pdf
- customize pdf page size
lastmod: 2026-10-19
linktitle: AutoCAD 이미지를 PDF로 내보내기
og_description: Aspose.CAD를 사용하여 Java에서 DWG를 PDF로 변환하는 방법을 배웁니다. 이 가이드는 AutoCAD PDF를
  내보내고, CAD를 PDF로 저장하며, 라이선스를 적용하는 과정을 안내합니다.
og_image_alt: 'Tutorial: convert DWG to PDF in Java with Aspose.CAD'
og_title: Aspose.CAD를 사용하여 Java에서 DWG를 PDF로 변환
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  headline: Convert DWG to PDF in Java using Aspose.CAD
  type: TechArticle
- description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  name: Convert DWG to PDF in Java using Aspose.CAD
  steps:
  - name: set the resource directory path
    text: Replace `"Your Document Directory"` with the absolute path to the folder
      you created in the prerequisites. > **Pro tip:** Use `Paths.get(...).toAbsolutePath()`
      to avoid path‑related errors on different operating systems.
  - name: load the CAD image
    text: Loading the CAD file into an `Image` object gives you full access to Aspose.CAD’s
      rasterization engine. The `Image` class loads the DWG file and prepares it for
      conversion. > **Why this matters:** Once the drawing is in memory, you can query
      its layouts, layers, and metadata before rasterizing.
  - name: set rasterization options
    text: Adjust `pageWidth` and `pageHeight` to **customize PDF page size**. Enabling
      `setTypeOfEntities(TypeOfEntities.Entities3D)` allows full 3‑D rendering when
      needed. The `RasterizationOptions` object controls DPI, page dimensions, and
      entity types for the output. - `pageWidth` / `pageHeight` are measur
  - name: configure PDF options
    text: Tie the rasterization settings to the PDF output, ensuring the vector data
      is correctly transformed. The `PdfOptions` class links the rasterization configuration
      with the final PDF file.
  - name: save the PDF
    text: The resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf**
      representation of your original AutoCAD drawing. The `save` method writes the
      rasterized image to a PDF file on disk.
  type: HowTo
- questions:
  - answer: Yes – the library supports DWG, DXF, DWF, DGN, and over 30 additional
      formats, giving you flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")`, `setLayouts("Layout1")`, etc.,
      to choose which view is rendered into the PDF.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to match any required page dimensions.
    question: Can I change the size of the output PDF file?
  - answer: The dedicated community is available at the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where you can ask questions and share solutions.
    question: Where can I get help if I run into problems?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- dwg to pdf
- aspose.cad
- java cad conversion
- export autocad pdf
title: Aspose.CAD를 사용하여 Java에서 DWG를 PDF로 변환
url: /ko/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# AutoCAD PDF 내보내기 – Aspose.CAD for Java를 사용하여 AutoCAD 이미지를 PDF로 내보내기

## 소개

Java에서 **DWG를 PDF로 변환**해야 한다면, 여기가 바로 적합한 곳입니다. 이 튜토리얼에서는 순수 Java 라이브러리인 Aspose.CAD for Java를 사용하여 AutoCAD 이미지를 PDF로 내보내는 방법을 보여줍니다. 이 라이브러리는 네이티브 종속성 없이 DWG, DXF, DWF 및 기타 많은 CAD 형식을 처리합니다. 튜토리얼을 마치면 **CAD를 PDF로 저장**하고, 페이지 크기와 같은 래스터화 옵션을 조정하며, 프로덕션 사용을 위해 **Aspose CAD 라이선스**를 올바르게 적용할 수 있게 됩니다.

## 빠른 답변
- **Java로 DWG를 PDF로 변환할 수 있나요?** 예 – Aspose.CAD for Java는 DWG, DXF 및 수십 개의 다른 CAD 형식을 기본적으로 지원합니다.  
- **라이선스가 필요합니까?** 영구 **Aspose CAD 라이선스**는 모든 평가 제한을 해제합니다; 테스트용 임시 라이선스도 제공됩니다.  
- **지원되는 Java 버전은 무엇인가요?** Java 8 이상을 완전히 지원합니다.  
- **PDF 페이지 크기를 제어할 수 있나요?** 물론입니다 – 래스터화 옵션에서 `pageWidth`와 `pageHeight`를 설정하세요.  
- **3‑D 렌더링이 가능한가요?** 예 – `TypeOfEntities.Entities3D`를 활성화하면 3‑D 엔티티를 래스터화합니다.

## export autocad pdf란?
AutoCAD PDF 내보내기는 벡터 CAD 도면을 휴대용 PDF 문서로 변환하는 과정입니다. 레이어, 선 굵기, 색상 및 선택적으로 3‑D 기하 정보를 보존하여, 클라이언트와 디자인을 쉽게 공유하거나 CAD 소프트웨어 없이도 보관할 수 있습니다.

## 왜 Aspose.CAD for Java로 DWG를 PDF로 변환하나요?
Aspose.CAD는 **50개 이상의 입력 및 출력 형식**을 지원하고, 전체 파일을 메모리에 로드하지 않고도 수백 페이지 도면을 처리하며, Java 8+를 지원하는 모든 플랫폼에서 실행됩니다. 이 라이브러리를 사용하면 DPI, 페이지 크기 및 레이아웃을 완전히 제어할 수 있어, 정확한 프로젝트 사양에 맞게 **PDF 페이지 크기를 사용자 정의**할 수 있으며, 네이티브 DLL을 설치할 필요가 없습니다.

## 전제 조건

- **Java Development Kit** – 워크스테이션에 JDK 8 이상이 설치되어 있어야 합니다.  
- **Aspose.CAD for Java** – 최신 JAR 파일을 [download link](https://releases.aspose.com/cad/java/)에서 다운로드하십시오.  
- **작업 디렉터리** – 소스 DWG 파일과 생성된 PDF를 저장할 폴더.

## 네임스페이스 가져오기

`Image` 클래스는 래스터화 가능한 모든 CAD 도면을 나타내며, `RasterizationOptions`와 `PdfOptions`를 사용하여 변환을 세밀하게 조정할 수 있습니다.

`Image` 클래스는 메모리 내에 CAD 도면을 보관하는 Aspose.CAD의 최상위 객체입니다.  
`RasterizationOptions` 클래스는 PDF에 쓰기 전에 벡터 데이터를 어떻게 래스터화할지 정의합니다.  
`PdfOptions` 클래스는 래스터화 설정을 PDF 전용 출력 매개변수와 결합합니다.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

이제 코드를 단계별로 살펴보겠습니다.

## Aspose.CAD for Java로 DWG를 PDF로 변환하는 방법?

Aspose.CAD for Java를 사용하여 DWG 파일을 PDF로 변환하려면 Image 클래스로 도면을 로드하고, CadRasterizationOptions(DPI, 페이지 크기, 엔티티 유형 등)를 구성한 뒤 해당 옵션을 PdfOptions에 래핑하고, 마지막으로 .pdf 파일명을 지정하여 save 메서드를 호출합니다. 이 순서는 벡터 데이터가 올바르게 래스터화되고 결과 PDF가 레이아웃 요구사항에 맞도록 보장합니다.

### 단계 1: 리소스 디렉터리 경로 설정

`"Your Document Directory"`를 전제 조건에서 만든 폴더의 절대 경로로 교체하십시오.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **팁:** `Paths.get(...).toAbsolutePath()`를 사용하면 다양한 운영 체제에서 경로 관련 오류를 방지할 수 있습니다.

### 단계 2: CAD 이미지 로드

`Image` 객체에 CAD 파일을 로드하면 Aspose.CAD의 래스터화 엔진에 완전히 접근할 수 있습니다.

`Image` 클래스는 DWG 파일을 로드하고 변환을 위해 준비합니다.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **왜 중요한가:** 도면이 메모리에 로드되면 래스터화하기 전에 레이아웃, 레이어 및 메타데이터를 조회할 수 있습니다.

### 단계 3: 래스터화 옵션 설정

`pageWidth`와 `pageHeight`를 조정하여 **PDF 페이지 크기를 사용자 정의**합니다. `setTypeOfEntities(TypeOfEntities.Entities3D)`를 활성화하면 필요 시 전체 3‑D 렌더링이 가능합니다.

`RasterizationOptions` 객체는 출력의 DPI, 페이지 크기 및 엔티티 유형을 제어합니다.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight`는 포인트 단위이며 (1 pt = 1/72 인치).  
- 3‑D 래스터화를 위해 `setTypeOfEntities` 라인의 주석을 해제하십시오.  
- `setLayouts`는 렌더링할 레이아웃(Model, Layout1 등)을 선택합니다.

### 단계 4: PDF 옵션 구성

래스터화 설정을 PDF 출력에 연결하여 벡터 데이터가 올바르게 변환되도록 합니다.

`PdfOptions` 클래스는 래스터화 구성을 최종 PDF 파일과 연결합니다.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 단계 5: PDF 저장

생성된 파일 `Export3DImagestoPDF_out_.pdf`는 원본 AutoCAD 도면을 **CAD를 PDF로 저장**한 형태입니다.

`save` 메서드는 래스터화된 이미지를 디스크의 PDF 파일로 기록합니다.

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

## 일반적인 문제 및 해결책

| 증상 | 가능한 원인 | 해결 방법 |
|------|------------|----------|
| 빈 PDF 출력 | 래스터화 옵션이 설정되지 않았거나 레이아웃이 일치하지 않음 | `setLayouts`가 CAD 파일의 레이아웃 이름과 일치하는지 확인하십시오. |
| 저해상도 이미지 | `pageWidth`/`pageHeight`가 너무 작음 | 크기를 늘리거나 `rasterizationOptions.setResolution(...)`를 통해 더 높은 DPI를 설정하십시오. |
| 라이선스 예외 | 유효한 라이선스가 적용되지 않음 | **Aspose CAD 라이선스**를 적용하거나 테스트용 임시 라이선스를 사용하십시오. |

## 자주 묻는 질문

**Q: Aspose.CAD for Java를 다른 CAD 파일 형식과 함께 사용할 수 있나요?**  
A: 예 – 라이브러리는 DWG, DXF, DWF, DGN 및 30개 이상의 추가 형식을 지원하여 프로젝트 전반에 걸쳐 유연성을 제공합니다.

**Q: Aspose.CAD for Java용 임시 라이선스를 어떻게 얻나요?**  
A: 평가용 기간 제한 라이선스를 요청하려면 [temporary license page](https://purchase.aspose.com/temporary-license/)를 방문하십시오.

**Q: 래스터화에 레이아웃 옵션이 있나요?**  
A: 물론입니다. `setLayouts("Model")`, `setLayouts("Layout1")` 등으로 PDF에 렌더링할 뷰를 선택하십시오.

**Q: 출력 PDF 파일의 크기를 변경할 수 있나요?**  
A: 예 – 래스터화 옵션에서 `pageWidth`와 `pageHeight`를 수정하여 필요한 페이지 크기에 맞출 수 있습니다.

**Q: 문제가 발생하면 어디에서 도움을 받을 수 있나요?**  
A: 질문을 하고 해결책을 공유할 수 있는 전용 커뮤니티가 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)에서 제공됩니다.

---

**마지막 업데이트:** 2026-10-19  
**테스트 환경:** Aspose.CAD for Java 24.10  
**작성자:** Aspose

## 관련 튜토리얼

- [Java에서 DWG를 PDF로 내보내기 – Aspose.CAD로 PDF 페이지 크기 설정](/cad/java/cad-export-options/export-to-pdf/)
- [DWG를 PDF로 내보내기: Aspose.CAD for Java를 사용한 특정 레이아웃](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [DWG를 PDF로 내보내기 및 Aspose.CAD Java로 추적 활성화](/cad/java/additional-features/enable-tracking/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}