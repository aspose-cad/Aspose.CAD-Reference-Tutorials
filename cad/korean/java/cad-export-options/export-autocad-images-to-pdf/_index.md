---
date: 2026-10-19
description: Aspose.CAD for Java를 사용하여 AutoCAD 도면을 사용자 지정 PDF 페이지 크기로 PDF로 내보내는 방법을
  배웁니다. 이 단계별 가이드에서는 DWG를 PDF로 변환하고, 래스터화 옵션 및 라이선스에 대해 설명합니다.
keywords:
- custom pdf page size
- export autocad to pdf
- save cad as pdf
- generate pdf from dwg
- dwg to pdf java
lastmod: 2026-10-19
linktitle: AutoCAD 이미지 PDF로 내보내기
og_description: Aspose.CAD for Java를 사용하여 AutoCAD 도면을 PDF로 내보낼 때 사용자 지정 PDF 페이지 크기를
  설정합니다. 몇 분 안에 DWG를 PDF로 변환하고, 래스터화 설정 및 라이선스를 배우세요.
og_image_alt: Guide showing how to export AutoCAD drawings to PDF with custom page
  dimensions using Aspose.CAD for Java
og_title: Aspose.CAD를 사용한 AutoCAD 내보내기에서 사용자 지정 PDF 페이지 크기 설정
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  headline: Set custom PDF page size for AutoCAD export with Aspose.CAD
  type: TechArticle
- description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  name: Set custom PDF page size for AutoCAD export with Aspose.CAD
  steps:
  - name: set the resource directory path
    text: '> **Pro tip:** Replace `"Your Document Directory"` with the absolute path
      to the folder you created in the prerequisites.'
  - name: load the CAD image
    text: The `Image` class loads the CAD file and gives you access to Aspose.CAD’s
      rasterization engine. > **Why this matters:** Once the CAD file is loaded, you
      can manipulate rasterization options before rendering to PDF.
  - name: set rasterization options
    text: The `CadRasterizationOptions` class specifies how the CAD drawing is rasterized
      before being saved as PDF. Adjust `pageWidth` and `pageHeight` to define a **custom
      PDF page size**. You can also enable 3‑D rendering by uncommenting the `setTypeOfEntities`
      line. - `pageWidth` / `pageHeight` – measured
  - name: configure PDF options
    text: The `PdfOptions` class holds PDF‑specific settings and links the rasterization
      options to the output file, ensuring the custom page dimensions are applied
      correctly.
  - name: save the PDF
    text: The `save` method writes the rendered image to the specified PDF file. The
      resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf** representation
      of your original AutoCAD drawing with the exact page dimensions you specified.
  type: HowTo
- questions:
  - answer: Yes, the library supports DWG, DXF, DWF, DGN, and many more, giving you
      flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")` or specify other layout names to
      control which view is rendered.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to any dimensions you need.
    question: Can I customize the size of the output PDF file?
  - answer: The dedicated [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) offers
      community support and official responses from the Aspose team.
    question: Where can I get help or discuss issues related to Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
- PDF generation
- DWG export
title: Aspose.CAD를 사용한 AutoCAD 내보내기에서 사용자 지정 PDF 페이지 크기 설정
url: /ko/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# AutoCAD PDF 내보내기 - Aspose.CAD for Java를 사용하여 AutoCAD 이미지를 PDF로 내보내기

## 소개

DWG를 **PDF로 변환**하고 출력 파일의 정확한 크기를 제어해야 한다면, 여기가 바로 정답입니다. 이 튜토리얼에서는 Aspose.CAD for Java를 사용하여 AutoCAD 이미지를 PDF로 내보낼 때 **사용자 정의 PDF 페이지 크기**를 설정하는 방법을 보여줍니다. 가이드를 마치면 DWG를 로드하고, DPI 및 페이지 너비/높이와 같은 래스터화 옵션을 구성하고, 라이선스를 적용한 뒤, 프로덕션 준비가 된 PDF를 생성하는 방법을 알게 됩니다.

## 빠른 답변
- **Java로 DWG를 PDF로 변환할 수 있나요?** 예 – Aspose.CAD for Java는 DWG, DXF, DWF 및 기타 많은 CAD 형식을 기본적으로 지원합니다.  
- **프로덕션 사용을 위해 라이선스가 필요합니까?** 전체 Aspose.CAD 라이선스를 적용하면 모든 평가 제한이 해제됩니다; 테스트용 임시 라이선스도 제공됩니다.  
- **어떤 Java 버전과 호환되나요?** 이 라이브러리는 Java 8 및 이후 모든 JDK와 호환됩니다.  
- **PDF 페이지 크기를 어떻게 변경하나요?** `PdfOptions.getRasterizationOptions()`에서 `pageWidth`와 `pageHeight`를 원하는 크기로 설정하면 됩니다.  
- **3‑D 렌더링이 지원되나요?** 예 – `TypeOfEntities.Entities3D`를 활성화하면 3‑D 엔터티를 래스터화할 수 있습니다.

## AutoCAD PDF 내보내기란?
AutoCAD PDF 내보내기는 벡터 기반 CAD 도면(DWG, DXF, DWF 등)을 레이어, 라인 두께 및 선택적 3‑D 기하 정보를 유지하면서 휴대용 PDF 문서로 변환하는 것을 의미합니다. 이를 통해 클라이언트와 디자인을 공유하거나, 도면을 보관하거나, CAD 소프트웨어 없이 인쇄할 수 있습니다.

## DWG를 PDF로 변환하기 위해 Aspose.CAD for Java를 사용하는 이유
Aspose.CAD for Java는 DWG를 PDF로 변환할 때 포맷 지원이 풍부하고, 순수 Java 구현으로 네이티브 종속성이 없으며, DPI 및 페이지 크기에 대한 완전한 제어가 가능한 고해상도 래스터화를 제공하고, 트라이얼에서 프로덕션까지 확장 가능한 유연한 라이선싱을 제공하기 때문에 이상적입니다.

- **광범위한 포맷 지원** – DWG, DXF, DWF, DGN 및 PDF를 포함한 50개 이상의 입력·출력 포맷을 지원합니다.  
- **순수 Java 구현** – 네이티브 DLL이나 외부 종속성이 없으므로 모든 플랫폼에 손쉽게 배포할 수 있습니다.  
- **고해상도 래스터화** – DPI, 페이지 크기 및 레이아웃을 지정할 수 있어 결과물의 **사용자 정의 PDF 페이지 크기**를 완벽히 제어할 수 있습니다.  
- **확장 가능한 라이선스** – 무료 트라이얼로 시작한 뒤 영구 **Aspose CAD 라이선스**로 업그레이드할 수 있습니다.  

## 전제 조건

- **Java Development Kit** – JDK 8 이상이 설치되어 있어야 합니다.  
- **Aspose.CAD for Java** – 최신 JAR 파일을 [download link](https://releases.aspose.com/cad/java/)에서 다운로드합니다.  
- **작업 디렉터리** – 소스 DWG 파일이 들어 있고 생성된 PDF가 저장될 폴더를 준비합니다.

## 네임스페이스 가져오기

`Image` 클래스는 메모리 내에서 CAD 도면을 나타내는 Aspose.CAD의 핵심 객체입니다. 코딩을 시작하기 전에 필요한 패키지를 가져옵니다.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

이제 코드를 단계별로 살펴보겠습니다.

## DWG를 PDF로 내보낼 때 사용자 정의 PDF 페이지 크기를 설정하는 방법

DWG를 로드하고 원하는 페이지 너비와 높이를 정의한 뒤 PDF로 저장하면 됩니다. 아래 단계가 정확한 순서와 최소 코드 예시를 보여줍니다.

### 단계 1: 리소스 디렉터리 경로 설정

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **프로 팁:** `"Your Document Directory"`를 전제 조건에서 만든 폴더의 절대 경로로 교체하세요.

### 단계 2: CAD 이미지 로드

`Image` 클래스는 CAD 파일을 로드하고 Aspose.CAD의 래스터화 엔진에 접근할 수 있게 해줍니다.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **이것이 중요한 이유:** CAD 파일이 로드되면 PDF로 렌더링하기 전에 래스터화 옵션을 조정할 수 있습니다.

### 단계 3: 래스터화 옵션 설정

`CadRasterizationOptions` 클래스는 CAD 도면이 PDF로 저장되기 전에 어떻게 래스터화될지를 지정합니다. `pageWidth`와 `pageHeight`를 조정하여 **사용자 정의 PDF 페이지 크기**를 정의합니다. 필요에 따라 `setTypeOfEntities` 라인을 주석 해제하면 3‑D 렌더링을 활성화할 수 있습니다.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` – 픽셀 단위; A4, Letter 또는 원하는 모든 커스텀 치수에 맞게 값을 변경하세요.  
- `setTypeOfEntities(TypeOfEntities.Entities3D)` – 필요 시 3‑D 엔터티를 렌더링합니다.  
- `setLayouts` – 래스터화할 레이아웃(Model, Layout1 등)을 선택합니다.

### 단계 4: PDF 옵션 구성

`PdfOptions` 클래스는 PDF 전용 설정을 보관하고 래스터화 옵션을 출력 파일에 연결하여 사용자 정의 페이지 치수가 올바르게 적용되도록 합니다.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 단계 5: PDF 저장

`save` 메서드는 렌더링된 이미지를 지정된 PDF 파일에 기록합니다.

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

결과 파일인 `Export3DImagestoPDF_out_.pdf`는 원본 AutoCAD 도면을 정확히 지정한 페이지 치수로 **CAD를 PDF로 저장**한 형태입니다.

## 일반적인 문제 및 해결책

| 증상 | 가능한 원인 | 해결 방법 |
|------|------------|----------|
| 빈 PDF 출력 | 래스터화 옵션이 설정되지 않았거나 레이아웃이 일치하지 않음 | `setLayouts`가 CAD 파일의 레이아웃 이름과 일치하는지 확인하세요. |
| 저해상도 이미지 | `pageWidth`/`pageHeight`가 너무 작거나 DPI가 낮음 | 차원을 늘리거나 `rasterizationOptions.setResolution(...)`를 사용해 높은 DPI를 지정하세요. |
| 라이선스 예외 | 유효한 라이선스가 적용되지 않음 | 영구 Aspose.CAD 라이선스를 적용하거나 테스트용 임시 라이선스를 사용하세요. |

## 자주 묻는 질문

**Q: Aspose.CAD for Java를 다른 CAD 파일 형식과 함께 사용할 수 있나요?**  
A: 예, 라이브러리는 DWG, DXF, DWF, DGN 등 다양한 형식을 지원하므로 프로젝트 전반에 걸쳐 유연하게 사용할 수 있습니다.

**Q: Aspose.CAD for Java용 임시 라이선스는 어떻게 얻나요?**  
A: [temporary license page](https://purchase.aspose.com/temporary-license/)에서 평가용 시간 제한 라이선스를 요청하세요.

**Q: 래스터화에 사용할 레이아웃 옵션이 있나요?**  
A: 물론입니다. `setLayouts("Model")`을 사용하거나 다른 레이아웃 이름을 지정하여 렌더링할 뷰를 제어할 수 있습니다.

**Q: 출력 PDF 파일의 크기를 맞춤 설정할 수 있나요?**  
A: 네 – 래스터화 옵션의 `pageWidth`와 `pageHeight`를 원하는 모든 치수로 수정하면 됩니다.

**Q: Aspose.CAD for Java와 관련된 도움을 받거나 이슈를 논의할 수 있는 곳은 어디인가요?**  
A: 전용 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)에서 커뮤니티 지원 및 Aspose 팀의 공식 답변을 받을 수 있습니다.

## 추가 FAQ (AI 친화적 형식)

**Q: Aspose.CAD가 Windows나 Linux에서 네이티브 라이브러리를 필요로 하나요?**  
A: 아니요. Aspose.CAD for Java는 순수 Java 라이브러리이므로 JDK를 지원하는 모든 플랫폼에서 추가 네이티브 DLL 없이 실행됩니다.

**Q: 라이브러리가 처리할 수 있는 DWG 파일 크기는 어느 정도인가요?**  
A: 스트리밍 아키텍처 덕분에 전체 파일을 메모리에 로드하지 않고도 500 MB까지, 수백 페이지에 달하는 도면을 처리할 수 있습니다.

**Q: 한 번에 여러 DWG 파일을 배치 변환할 수 있나요?**  
A: 예. 디렉터리를 순회하면서 각 파일을 `Image.load()`로 로드하고 동일한 래스터화 옵션을 적용한 뒤 `save()`를 호출하면 됩니다.

**Q: 일반적인 서버에서 기대할 수 있는 성능은 어떠한가요?**  
A: 표준 2.5 GHz CPU에서 300 DPI로 100페이지 DWG를 변환하는 데 약 12 초가 소요된다고 Aspose 벤치마크 테스트에서 보고되었습니다.

**Q: 라이브러리가 PDF에 레이어 정보를 보존하나요?**  
A: 출력은 래스터화되지만 레이어, 라인 두께 및 색상의 시각적 표현은 정확히 재현됩니다.

---

**마지막 업데이트:** 2026-10-19  
**테스트 환경:** Aspose.CAD for Java 24.10  
**작성자:** Aspose

## 관련 튜토리얼

- [Aspose.CAD Java를 사용하여 DWG를 PDF로 내보내고 추적 활성화](/cad/java/additional-features/enable-tracking/)
- [Aspose.CAD Java를 사용하여 DWG를 PDF로 내보내기: 특정 레이아웃](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Aspose.CAD for Java를 사용하여 DWG를 BMP로 내보내고 단위 유형으로 CAD 크기 조정](/cad/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}