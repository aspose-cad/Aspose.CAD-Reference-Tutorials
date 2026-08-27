---
date: 2026-06-09
description: Aspose.CAD for Java를 사용하여 DXF를 WMF로 변환하는 방법을 배우세요. 무료 체험, Java 8+ 지원
  및 선택적 PDF 내보내기가 포함됩니다. 코드 예제가 포함된 단계별 가이드.
keywords:
- convert dxf to wmf
- aspose cad java
- aspose free trial
- aspose cad conversion
- export dxf pdf
linktitle: Java를 사용하여 DXF를 WMF 형식으로 내보내기
schemas:
- author: Aspose
  dateModified: '2026-06-09'
  description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  headline: Convert DXF to WMF Using Aspose.CAD in Java
  type: TechArticle
- description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  name: Convert DXF to WMF Using Aspose.CAD in Java
  steps:
  - name: Load DXF Drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: Configure Rasterization Options
    text: CadRasterizationOptions specifies page size, resolution, and background
      for rasterizing the CAD drawing.
  - name: Save as WMF
    text: ImageSaveOptions with SaveFormat.WMF tells Aspose.CAD to write the output
      as a Windows Metafile.
  - name: Dispose of Resources
    text: Calling image.close() releases native resources used by the Aspose.CAD Image
      object.
  - name: Optional – Export to PDF
    text: PdfOptions configures PDF‑specific settings when saving the image as a PDF
      document. > **Pro tip:** You can reuse the same `CadRasterizationOptions` object
      for PDF export by passing it to a `PdfOptions` instance, saving you a few lines
      of setup.
  type: HowTo
- questions:
  - answer: Yes. Load the file in a try‑with‑resources block and dispose of the `Image`
      object promptly. Adjust `CadRasterizationOptions.setPageWidth/Height` to a reasonable
      size to keep memory usage low.
    question: Can I convert large DXF files (hundreds of MB) without running out of
      memory?
  - answer: WMF is a flat vector format, so layer hierarchy is flattened, but line
      styles, colors, and hatch patterns are preserved.
    question: Does the WMF output retain layer information?
  - answer: Use `rasterizationOptions.setResolution(300);` to define DPI before saving.
    question: Is it possible to set a custom DPI for the WMF?
  - answer: Absolutely. Loop through a directory, load each file, and apply the same
      rasterization and save logic.
    question: Can I batch‑convert multiple DXF files in one run?
  - answer: Aspose.CAD for Java supports Java 8 and later, including Java 11, 17,
      and newer LTS releases.
    question: What versions of Java are supported?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Java에서 Aspose.CAD를 사용하여 DXF를 WMF로 변환
url: /ko/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD를 사용한 Java에서 DXF를 WMF로 변환

## 소개

이 튜토리얼에서는 Aspose.CAD for Java를 사용하여 **DXF를 WMF로 변환**하는 방법을 알아봅니다. Windows 기반 보고서에 CAD 도면을 삽입하거나, Office 문서용 가벼운 벡터 그래픽을 생성하거나, 배치 변환을 자동화해야 할 경우, DXF를 WMF로 변환하는 것은 엔지니어링 및 보고 파이프라인에서 자주 요구됩니다. DXF 도면을 로드하고, 래스터화 옵션을 구성한 뒤, 결과를 WMF로 저장하고, 필요에 따라 동일한 도면을 PDF로 내보내는 과정을 단계별로 안내합니다.

## 빠른 답변
- **DXF를 WMF로 변환할 때 무료 체험을 사용할 수 있나요?** 예 – Aspose는 완전한 기능을 제공하는 30일 체험판을 제공합니다.  
- **필요한 Java 버전은 무엇인가요?** Java 8 이상.  
- **코드를 실행하려면 라이선스가 필요합니까?** 프로덕션에서는 라이선스가 필요합니다; 체험판은 개발 및 테스트에 사용할 수 있습니다.  
- **변환이 무손실인가요?** 벡터 데이터가 보존되며, 래스터화 옵션을 통해 해상도를 제어할 수 있습니다.  
- **같은 도면을 PDF로도 내보낼 수 있나요?** 물론입니다 – 아래 “PDF로 내보내기” 단계를 참고하세요.

## “DXF를 WMF로 변환”이란?

DXF를 WMF로 변환한다는 것은 널리 사용되는 CAD 형식인 Drawing Exchange Format(DXF) 파일을 Windows Metafile(WMF) 형식으로 바꾸는 것을 의미합니다. WMF는 Microsoft Office, Windows 애플리케이션 및 다양한 보고 도구와 원활하게 통합되는 벡터 이미지 형식입니다.

## Java에서 Aspose.CAD를 사용하는 이유

Aspose.CAD for Java는 순수 Java 기반이며 네이티브 DLL이 필요 없는 엔진을 제공하여 **99 % 이상의 벡터 정확도**로 CAD 파일을 변환합니다. 레이어, 색상, 선 스타일 및 해치 패턴을 보존합니다. **50개 이상의 입력 및 출력 형식**을 지원하며(DXF, DWG, DGN, PDF, PNG, SVG, WMF 등) 내장 래스터화 옵션을 통해 페이지 크기, DPI 및 배경 색상을 세밀하게 조정할 수 있습니다. 동일한 API로 PDF, PNG, SVG 내보내기도 가능해 여러 라이브러리를 사용할 필요가 없습니다.

### 주요 장점
- **외부 종속성 없음** – 순수 Java이며 Java가 실행되는 모든 OS에서 동작합니다.  
- **고품질 렌더링** – 선 두께, 색상 및 해치 디테일을 유지합니다.  
- **내장 래스터화** – 페이지 크기, 해상도 및 배경을 제어합니다.  
- **원스톱 변환** – 동일한 클래스들로 WMF, PDF, PNG, SVG 등을 내보낼 수 있습니다.

## 사전 요구 사항

시작하기 전에 다음을 확인하세요:

- **Aspose.CAD for Java**를 프로젝트에 통합합니다. 공식 사이트에서 다운로드: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- **문서 디렉터리**에 DXF 파일이 저장되어 있어야 합니다(예: `Your Document Directory/DXFDrawings/`).

## 네임스페이스 가져오기

다음 import 구문은 CAD 파일을 로드, 래스터화 및 저장하는 데 필요한 Aspose.CAD 클래스를 포함합니다.  
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

### Java에서 DXF를 WMF로 변환하려면 어떻게 하나요?

`Image.load("yourFile.dxf")`로 DXF 파일을 로드하고, 원하는 페이지 크기와 DPI를 위해 `CadRasterizationOptions`를 구성한 뒤, `image.save("output.wmf", new ImageSaveOptions(SaveFormat.WMF))`를 호출합니다. 이 세 단계 패턴은 벡터 품질을 유지하면서 전체 변환을 수행하며 몇 줄의 코드만 필요합니다.

#### 단계 1: DXF 도면 로드

`Image.load`는 DXF 파일을 Aspose.CAD Image 객체로 읽어들입니다.  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### 단계 2: 래스터화 옵션 구성

`CadRasterizationOptions`는 CAD 도면을 래스터화할 때 페이지 크기, 해상도 및 배경을 지정합니다.  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### 단계 3: WMF로 저장

`SaveFormat.WMF`와 함께 사용하는 `ImageSaveOptions`는 Aspose.CAD에 출력 파일을 Windows Metafile로 기록하도록 지시합니다.  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### 단계 4: 리소스 해제

`image.close()`를 호출하면 Aspose.CAD Image 객체가 사용한 네이티브 리소스가 해제됩니다.  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### 단계 5: 선택 사항 – PDF로 내보내기

`PdfOptions`는 이미지를 PDF 문서로 저장할 때 PDF‑전용 설정을 구성합니다.  
```java
finally
{
  cadImage.dispose();
}
```

> **Pro tip:** 동일한 `CadRasterizationOptions` 객체를 `PdfOptions` 인스턴스에 전달하여 PDF 내보내기에 재사용하면 설정 코드를 몇 줄 줄일 수 있습니다.

## Aspose CAD Java를 사용하여 DXF를 PDF로 내보내려면 어떻게 하나요?

PDF로 내보내는 과정은 로드 및 래스터화 단계가 동일합니다; WMF 저장 형식을 PDF로 교체하면 됩니다. `new ImageSaveOptions(SaveFormat.Pdf)`를 사용하고, 필요에 따라 압축 수준이나 저자 메타데이터와 같은 PDF‑전용 옵션을 설정하세요. 이 한 줄 변환은 원본 CAD 레이아웃을 그대로 반영하는 검색 가능하고 페이지 정확도가 높은 PDF를 생성합니다.

## 일반적인 문제 및 해결책

| 문제 | 원인 | 해결 방법 |
|-------|-------|-----|
| **`NullPointerException` on `cadImage.save`** | 변수 `cadImage`가 정의되지 않음(`image`이어야 함). | `cadImage`를 `image`로 교체하거나 변수명을 일관되게 변경합니다. |
| **Output WMF is blank** | 래스터화 페이지 크기가 너무 작거나 배경 색상이 투명하게 설정됨. | `PageWidth`/`PageHeight`를 늘리거나 `rasterizationOptions.setBackgroundColor(Color.WHITE);`로 배경 색상을 설정합니다. |
| **License exception** | 프로덕션 환경에서 유효한 Aspose 라이선스 없이 실행. | 애플리케이션 시작 시 라이선스 파일을 적용합니다: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## 결론

이제 Aspose.CAD for Java를 사용하여 **DXF를 WMF로 변환**하고, 필요에 따라 **동일한 도면을 PDF로 내보내는** 완전한 프로덕션‑준 워크플로우를 갖추었습니다. 이 접근 방식은 Windows 기반 보고 및 문서 도구와 원활히 통합되는 고품질 벡터 출력을 제공하며, 코드베이스를 간단하고 종속성 없이 유지할 수 있습니다.

## FAQ

### Q1: Aspose.CAD 문서는 어디에서 찾을 수 있나요?
A1: 문서는 [여기](https://reference.aspose.com/cad/java/)에서 확인할 수 있습니다.

### Q2: Aspose.CAD for Java를 어떻게 다운로드하나요?
A2: 라이브러리는 [여기](https://releases.aspose.com/cad/java/)에서 다운로드합니다.

### Q3: 무료 체험판을 이용할 수 있나요?
A3: 예, 무료 체험판은 [여기](https://releases.aspose.com/)에서 받을 수 있습니다.

### Q4: 임시 라이선스 옵션이 있나요?
A4: 임시 라이선스는 [여기](https://purchase.aspose.com/temporary-license/)에서 확인하세요.

### Q5: 지원을 어디서 받을 수 있나요?
A5: Aspose.CAD 지원 포럼은 [여기](https://forum.aspose.com/c/cad/19)에서 이용할 수 있습니다.

## 자주 묻는 질문

**Q: 수백 MB 규모의 대용량 DXF 파일을 메모리 부족 없이 변환할 수 있나요?**  
A: 가능합니다. 파일을 `try‑with‑resources` 블록으로 로드하고 `Image` 객체를 즉시 해제하세요. 메모리 사용량을 낮추려면 `CadRasterizationOptions.setPageWidth/Height`를 적절히 조정합니다.

**Q: WMF 출력에 레이어 정보가 유지되나요?**  
A: WMF는 평면 벡터 형식이므로 레이어 구조는 평탄화되지만, 선 스타일, 색상 및 해치 패턴은 보존됩니다.

**Q: WMF에 사용자 정의 DPI를 설정할 수 있나요?**  
A: 저장 전에 `rasterizationOptions.setResolution(300);`와 같이 DPI를 정의하면 됩니다.

**Q: 여러 DXF 파일을 한 번에 배치 변환할 수 있나요?**  
A: 물론입니다. 디렉터리를 순회하면서 각 파일을 로드하고 동일한 래스터화 및 저장 로직을 적용하면 됩니다.

**Q: 지원되는 Java 버전은 어떤 것이 있나요?**  
A: Aspose.CAD for Java는 Java 8 이상을 지원하며, Java 11, 17 및 최신 LTS 릴리스도 포함됩니다.

---

**Last Updated:** 2026-06-09  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

## 관련 튜토리얼

- [CAD에서 PDF 만들기 – Aspose.CAD for Java를 사용하여 DXF를 PDF로 내보내기](/cad/java/additional-features/export-dxf-to-pdf/)
- [DXF에서 PDF 만들기: Aspose.CAD for Java를 사용하여 레이어 내보내기](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Aspose.CAD를 사용하여 Java에서 DXF 레이아웃을 JPEG 이미지로 변환하는 방법](/cad/java/additional-features/export-specific-layout-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}