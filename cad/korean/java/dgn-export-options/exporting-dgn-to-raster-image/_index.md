---
date: 2026-05-25
description: Aspose.CAD for Java를 사용하여 dgn 파일을 JPEG 이미지로 내보내는 방법을 배웁니다. 이 단계별 가이드는
  dgn을 jpeg으로 효율적으로 변환하는 방법을 보여줍니다.
keywords:
- how to export dgn
- convert dgn to jpeg
- java convert cad to image
linktitle: AutoCAD 형식의 DGN을 Raster Image Format으로 내보내기
schemas:
- author: Aspose
  dateModified: '2026-05-25'
  description: Learn how to export dgn files to JPEG images with Aspose.CAD for Java.
    This step‑by‑step guide shows you how to convert dgn to jpeg efficiently.
  headline: How to Export DGN to JPEG with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export dgn files to JPEG images with Aspose.CAD for Java.
    This step‑by‑step guide shows you how to convert dgn to jpeg efficiently.
  name: How to Export DGN to JPEG with Aspose.CAD for Java
  steps:
  - name: '**Aspose.CAD Library** – download the latest JAR from the official site [here](https://releases.aspose.com/cad/java/).
      You can also explore other product releases [here](https://releases.aspose.com/).'
    text: '**Aspose.CAD Library** – download the latest JAR from the official site [here](https://releases.aspose.com/cad/java/).
      You can also explore other product releases [here](https://releases.aspose.com/).'
  - name: '**Java Development Kit (JDK)** – Java 8 or newer installed on your machine.'
    text: '**Java Development Kit (JDK)** – Java 8 or newer installed on your machine.'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor you prefer.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports over 30 vector formats, including DWG, DXF, DWF,
      and SVG, enabling a single API for many conversion scenarios.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Yes, you can access a free trial [here](https://releases.aspose.com/).
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: Refer to the official docs [here](https://reference.aspose.com/cad/java/).
    question: Where can I find documentation for Aspose.CAD for Java?
  - answer: Visit the support forum [here](https://forum.aspose.com/c/cad/19).
    question: How can I get support for Aspose.CAD for Java?
  - answer: You can buy a license [here](https://purchase.aspose.com/buy).
    question: Where can I purchase a license for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java를 사용하여 DGN을 JPEG로 내보내는 방법
url: /ko/java/dgn-export-options/exporting-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD를 사용한 Java DGN에서 JPEG 변환 튜토리얼

## 소개

이 포괄적인 가이드에서는 Aspose.CAD for Java를 사용하여 **how to export dgn** 파일을 JPEG 이미지로 내보내는 방법을 알아봅니다. 배치 처리 서비스를 구축하거나 CAD 뷰어에 실시간 미리보기 생성을 추가하든, 이 튜토리얼은 소스 파일 로드부터 래스터 출력 저장까지 모든 단계를 안내합니다. 또한 코드를 깔끔하고 성능 좋게 유지하는 실용적인 팁도 확인할 수 있습니다.

## 빠른 답변
- **필요한 라이브러리는 무엇인가요?** Aspose.CAD for Java (download [here](https://releases.aspose.com/cad/java/)).
- **DGN을 JPEG로 한 줄로 변환할 수 있나요?** 예 – `CadImage.load` 로 로드하고 `JpegOptions` 와 함께 `save` 를 호출하면 됩니다.
- **프로덕션에 라이선스가 필요합니까?** 예, 상용 라이선스를 사용하면 평가 워터마크가 제거됩니다.
- **지원되는 Java 버전은 무엇인가요?** Java 8 부터 17까지 완전 지원됩니다.
- **얼마나 큰 DGN 파일을 처리할 수 있나요?** 전체 파일을 메모리에 로드하지 않고도 최대 2 GB 파일을 처리할 수 있습니다.

## “how to export dgn”란 무엇인가요?
*“how to export dgn”*는 MicroStation DGN 설계 파일을 JPEG와 같은 래스터 이미지 형식으로 변환하는 과정을 의미합니다. 이 변환을 통해 CAD 소프트웨어가 없는 이해관계자도 디자인을 검토하고, 문서에 이미지를 삽입하거나 웹 갤러리를 위한 썸네일을 생성할 수 있어 팀 간 접근성과 협업이 향상됩니다.

## 왜 Aspose.CAD for Java를 사용하나요?
Aspose.CAD는 **30개 이상의 CAD 형식**(DGN, DWG, DXF 포함)을 지원하며 원본 CAD 애플리케이션 없이도 **2 GB**까지 파일을 렌더링할 수 있습니다. 래스터 엔진은 표준 서버 하드웨어에서 **초당 50프레임** 이상으로 다중 페이지 도면을 처리하며, 단일 API 호출만으로 고품질 JPEG 출력을 제공합니다.

## 사전 요구 사항

시작하기 전에 다음을 준비하십시오:

1. **Aspose.CAD Library** – 공식 사이트 [here](https://releases.aspose.com/cad/java/)에서 최신 JAR를 다운로드하십시오. 다른 제품 릴리스를 확인하려면 [here](https://releases.aspose.com/)를 방문하세요.  
2. **Java Development Kit (JDK)** – Java 8 이상 버전이 설치되어 있어야 합니다.  
3. **IDE** – IntelliJ IDEA, Eclipse 또는 선호하는 Java 호환 편집기 중 하나를 사용하십시오.

## 패키지 가져오기

Java 프로젝트에서 필요한 Aspose.CAD 클래스를 가져옵니다:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## Aspose.CAD를 사용하여 Java에서 dgn를 JPEG로 내보내는 방법

`CadImage` 클래스는 메모리에 로드된 CAD 문서를 나타내며, 렌더링 및 저장 메서드를 제공합니다.

`CadImage.load("source.dgn")` 로 DGN 파일을 로드하고, `JpegOptions`(품질 및 해상도 포함)를 구성한 뒤, 페이지 크기와 배경색 같은 `RasterizationOptions` 를 설정합니다. 마지막으로 `image.save("output.jpg", jpegOptions)` 를 호출하면 벡터‑래스터 변환이 수행되고, 일반적인 도면은 1초 미만에 고품질 JPEG 파일이 생성됩니다.

## 1단계: DGN 파일 로드

`CadImage` 클래스는 메모리에 로드된 CAD 문서를 나타냅니다.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## 2단계: JpegOptions 객체 생성

`JpegOptions`는 JPEG 출력에 특화된 설정(압축 품질 및 해상도 등)을 정의합니다.

```java
ImageOptionsBase options = new JpegOptions();
```

## 3단계: Rasterization Options 할당

`RasterizationOptions`는 벡터 그래픽을 래스터화하는 방식을 결정하며, 페이지 크기, DPI, 배경색 및 안티앨리어싱 등을 포함합니다.

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## 4단계: 변환된 이미지 저장

`save` 를 호출하면 지정한 옵션을 사용하여 래스터 이미지를 디스크에 기록합니다.

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

### 일반적인 사용 사례

- **웹 미리보기 생성** – 엔지니어링 도면을 가벼운 JPEG 썸네일로 변환하여 브라우저에서 빠르게 표시합니다.  
- **배치 보관** – MicroStation 없이도 수천 개의 DGN 파일을 JPEG로 자동 변환하여 장기 보관합니다.  
- **보고서 작성** – Java 코드에서 직접 CAD 스냅샷을 PDF 또는 HTML 보고서에 삽입합니다.

### 일반적인 문제 및 해결책

| 문제 | 해결책 |
|-------|----------|
| **이미지가 빈 화면으로 표시됨** | `RasterizationOptions.setPageWidth/Height` 가 도면 범위와 일치하는지 확인하고, 투명하지 않은 배경색을 설정하십시오. |
| **출력 품질 저하** | `JpegOptions.setQuality(100)` 로 품질을 높이고, DPI를 더 높은 값(예: `RasterizationOptions.setResolution(300)`)으로 설정하십시오. |
| **메모리 부족 오류** | `CadImage.load` 시 `loadOptions.setLoadMode(LoadMode.Memory)` 를 사용하여 대용량 파일을 스트리밍 방식으로 로드하십시오. |

## 자주 묻는 질문

**Q: Aspose.CAD for Java를 다른 CAD 파일 형식과 함께 사용할 수 있나요?**  
A: 예, Aspose.CAD는 DWG, DXF, DWF, SVG 등을 포함한 30개 이상의 벡터 형식을 지원하므로 다양한 변환 시나리오에 단일 API를 사용할 수 있습니다.

**Q: Aspose.CAD for Java에 대한 무료 체험판이 있나요?**  
A: 예, 무료 체험판은 [here](https://releases.aspose.com/)에서 이용할 수 있습니다.

**Q: Aspose.CAD for Java 문서는 어디에서 찾을 수 있나요?**  
A: 공식 문서는 [here](https://reference.aspose.com/cad/java/)에서 확인하십시오.

**Q: Aspose.CAD for Java에 대한 지원을 어떻게 받을 수 있나요?**  
A: 지원 포럼은 [here](https://forum.aspose.com/c/cad/19)에서 방문하십시오.

**Q: Aspose.CAD for Java 라이선스는 어디서 구매하나요?**  
A: 라이선스 구매는 [here](https://purchase.aspose.com/buy)에서 가능합니다.

---

**마지막 업데이트:** 2026-05-25  
**테스트 환경:** Aspose.CAD 24.11 for Java  
**작성자:** Aspose

## 관련 튜토리얼

- [Aspose.CAD for Java를 사용한 손쉬운 DGN → AutoCAD PDF 내보내기](/cad/java/dgn-export-options/exporting-dgn-to-pdf/)
- [Aspose.CAD for Java – DGN을 DWG로 내보내기 튜토리얼](/cad/java/dgn-export-options/)
- [CAD를 PNG로 저장 – Aspose.CAD for Java를 사용한 CAD 도면을 래스터 이미지 형식으로 변환](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}