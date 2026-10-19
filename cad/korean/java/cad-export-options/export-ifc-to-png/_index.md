---
date: 2026-10-19
description: 몇 줄의 코드만으로 Aspose.CAD for Java를 사용하여 PNG 썸네일 IFC 파일을 만드는 방법을 배워보세요.
keywords:
- create png thumbnail ifc
- ifc to png conversion
- aspose cad java
- java image processing
- bIM visualization
lastmod: 2026-10-19
linktitle: IFC를 PNG로 내보내기
og_description: Aspose.CAD for Java를 사용하여 PNG 썸네일 IFC 파일을 손쉽게 만들 수 있습니다. 이 단계별 가이드에서는
  IFC 모델을 로드하고, 래스터화하며, 고품질 PNG 이미지로 저장하는 방법을 보여줍니다.
og_image_alt: Developer guide showing Java code that converts IFC files to PNG thumbnails
  using Aspose.CAD
og_title: Aspose.CAD for Java로 PNG 썸네일 IFC 만들기
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  headline: How to create PNG thumbnail IFC with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  name: How to create PNG thumbnail IFC with Aspose.CAD for Java
  steps:
  - name: load the IFC file
    text: First, point to the folder where your IFC file lives and load it with `CadImage.load`.
      `CadImage.load` reads a CAD file and returns an image object that can be rasterized.
      > **Why this matters:** Loading the file as a `CadImage` gives you access to
      vector‑raster conversion options that control resol
  - name: set rasterization options
    text: Define the output dimensions and any other vector‑related settings through
      `VectorRasterizationOptions`. `VectorRasterizationOptions` lets you specify
      output size, background color, and other rasterization parameters. > Adjust
      `PageWidth` and `PageHeight` to control the final PNG resolution, which i
  - name: configure PNG options
    text: Link the rasterization options to the PNG exporter by creating a `PngOptions`
      instance.
  - name: save the image as PNG
    text: Finally, write the rasterized image to disk using the `save` method. `save`
      writes the rasterized image to the specified file path in the chosen format.
      > After this step you have successfully **created a PNG thumbnail IFC** and
      can use the resulting `example.png` anywhere you need a raster image.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports many formats (DWG, DXF, DGN, etc.). Simply change
      the file extension and load the appropriate image class.
    question: Can I use this approach to convert other CAD formats to PNG?
  - answer: DPI is controlled indirectly via `PageWidth`/`PageHeight`. Adjust these
      values relative to the desired physical size to achieve the required DPI.
    question: Does the library let me set a custom DPI?
  - answer: PNG is a lossless format, so the rasterized image retains the full visual
      fidelity of the original vector data.
    question: Is the PNG output loss‑less?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- ifc conversion
- png thumbnail
- aspose.cad
- java image processing
- bim visualization
title: Aspose.CAD for Java로 PNG 썸네일 IFC 만들기
url: /ko/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java를 사용한 IFC를 PNG로 내보내기

## 소개

이 튜토리얼에서는 Aspose.CAD for Java를 사용하여 **PNG 썸네일 IFC** 파일을 만드는 방법을 배웁니다. BIM 포털을 위한 빠른 미리보기, 문서 관리 시스템을 위한 썸네일 생성, 혹은 배치 변환 자동화가 필요하든, 아래 단계들을 통해 3‑D IFC 모델을 선명한 2‑D PNG 이미지로 래스터화하는 작업을 몇 줄의 Java 코드만으로 수행할 수 있습니다.

## 빠른 답변
- **필요한 라이브러리는 무엇인가요?** Aspose.CAD for Java.  
- **몇 줄의 코드로 PNG 썸네일 IFC를 만들 수 있나요?** 예 – 전체 워크플로는 20줄 미만으로 구현됩니다.  
- **프로덕션에 라이선스가 필요합니까?** 테스트용 임시 라이선스로 동작하지만, 상업적 배포에는 정식 라이선스가 필요합니다.  
- **출력이 확장 가능합니까?** 원하는 픽셀 크기를 설정할 수 있으므로 PNG를 필요에 따라 언제든지 확대할 수 있습니다.  
- **지원되는 Java 버전은 무엇인가요?** Java 8 이상.

## “IFC를 PNG로 변환”이란?
IFC(Industry Foundation Classes)를 PNG로 변환한다는 것은 3‑D 건축 모델을 2‑D 비트맵 이미지로 래스터화하는 것을 의미합니다. 이 과정은 전체 CAD 뷰어 없이도 브라우저, 보고서, 모바일 앱 등에 표시할 수 있는 시각적 썸네일을 생성합니다.

## 왜 Aspose.CAD for Java를 사용하나요?
Aspose.CAD는 **30개 이상의 CAD 및 BIM 포맷**(IFC, DWG, DXF, DGN 등)을 지원하며, **2 GB**까지의 파일을 전체 문서를 메모리에 로드하지 않고 처리할 수 있습니다. 라이브러리는 순수 Java이며 **외부 종속성이 전혀 없고**, Windows, Linux, macOS에서 실행되어 서버‑사이드 이미지 생성에 최적화되었습니다.  
고성능 래스터화, 광범위한 포맷 지원, 그리고 Java 애플리케이션에 손쉽게 통합할 수 있는 장점을 제공합니다.

## 전제 조건

- **Aspose.CAD Library** – 최신 JAR 파일을 [download link](https://releases.aspose.com/cad/java/)에서 다운로드합니다.  
- **Java Development Kit** – 머신에 JDK 8 이상이 설치되어 있어야 합니다.  
- **IFC source file** – 코드에서 참조할 수 있는 폴더에 파일을 배치합니다.

## 네임스페이스 가져오기

`com.aspose.cad` 패키지는 필요한 모든 클래스를 제공합니다. `CadImage`는 CAD 파일을 로드하기 위한 진입점이며, `PngOptions`는 래스터화 설정을 구성합니다.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Java에서 PNG 썸네일 IFC를 만드는 방법

IFC 파일을 로드하고, 래스터화 옵션을 정의한 뒤 PNG 이미지로 저장합니다 – 이것이 전체 변환 워크플로입니다. 아래 섹션에서는 각 단계를 자세히 설명하므로, 코드를 복사‑붙여넣기만 하면 바로 실행할 수 있습니다.

### 단계 1: IFC 파일 로드
먼저 IFC 파일이 위치한 폴더를 지정하고 `CadImage.load`로 로드합니다.  
`CadImage.load`는 CAD 파일을 읽어 래스터화 가능한 이미지 객체를 반환합니다.

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

> **왜 중요한가:** 파일을 `CadImage`로 로드하면 해상도, 배경색, 선 두께 등을 제어할 수 있는 벡터‑래스터 변환 옵션에 접근할 수 있습니다.

### 단계 2: 래스터화 옵션 설정
`VectorRasterizationOptions`를 통해 출력 크기 및 기타 벡터 관련 설정을 정의합니다.  
`VectorRasterizationOptions`를 사용하면 출력 크기, 배경색 및 기타 래스터화 매개변수를 지정할 수 있습니다.

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

> `PageWidth`와 `PageHeight`를 조정하여 최종 PNG 해상도를 제어합니다. 이는 **save PNG java** 파일을 고품질 인쇄물이나 웹 썸네일용으로 저장할 때 필수적입니다.

### 단계 3: PNG 옵션 구성
래스터화 옵션을 PNG 익스포터에 연결하기 위해 `PngOptions` 인스턴스를 생성합니다.

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

### 단계 4: 이미지를 PNG로 저장
마지막으로 `save` 메서드를 사용해 래스터화된 이미지를 디스크에 기록합니다.  
`save`는 지정된 파일 경로에 선택한 포맷으로 래스터화 이미지를 씁니다.

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

> 이 단계를 마치면 **PNG 썸네일 IFC**가 성공적으로 생성되며, `example.png` 파일을 래스터 이미지가 필요한 어디에서든 사용할 수 있습니다.

## 일반적인 사용 사례
- 웹 포털에서 BIM 모델의 **썸네일 생성**.  
- PDF 또는 Word 보고서에 **평면도 스냅샷 삽입**.  
- 대규모 IFC 라이브러리의 **자동 배치 변환**을 통한 보관 또는 마이그레이션 프로젝트.

## 문제 해결 및 팁
- **메모리 문제:** 매우 큰 IFC 파일의 경우 JVM 힙을 (`-Xmx2g` 이상) 늘려 주세요.  
- **텍스처 누락:** IFC 파일의 외부 리소스가 `dataDir`에서 접근 가능하도록 확인하세요.  
- **전문가 팁:** 기본 투명 PNG 대신 흰색 배경을 원한다면 `vectorOptions.setBackgroundColor(Color.getWhite())`를 사용하세요.

## FAQ

### Q1: Aspose.CAD가 모든 버전의 IFC 파일과 호환되나요?
A1: Aspose.CAD는 다양한 IFC 버전을 지원합니다. 자세한 호환성 정보는 [documentation](https://reference.aspose.com/cad/java/)을 참고하세요.

### Q2: 래스터화 옵션을 더 세부적으로 조정할 수 있나요?
A2: 물론입니다! DPI 제어, 안티앨리어싱, 선 두께 등 고급 설정은 [documentation](https://reference.aspose.com/cad/java/)에서 확인할 수 있습니다.

### Q3: 체험판 버전을 사용할 수 있나요?
A3: 예, [Aspose.CAD free trial](https://releases.aspose.com/)에서 무료 체험판을 다운로드할 수 있습니다.

### Q4: 테스트용 임시 라이선스를 어떻게 얻나요?
A4: [Aspose.CAD temporary license page](https://purchase.aspose.com/temporary-license/)에서 임시 라이선스를 발급받으세요.

### Q5: 질문을 하거나 이슈를 보고하려면 어디에 문의해야 하나요?
A5: [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)에서 Aspose 엔지니어와 다른 개발자들의 지원을 받을 수 있습니다.

## 자주 묻는 질문

**Q: 이 방법을 사용해 다른 CAD 포맷을 PNG로 변환할 수 있나요?**  
A: 예, Aspose.CAD는 다양한 포맷(DWG, DXF, DGN 등)을 지원합니다. 파일 확장자를 변경하고 해당 이미지 클래스를 로드하면 됩니다.

**Q: 라이브러리에서 사용자 정의 DPI를 설정할 수 있나요?**  
A: DPI는 `PageWidth`/`PageHeight`를 통해 간접적으로 제어됩니다. 원하는 물리적 크기에 맞게 값을 조정하면 목표 DPI를 얻을 수 있습니다.

**Q: PNG 출력이 손실이 없나요?**  
A: PNG는 무손실 포맷이므로 래스터화된 이미지는 원본 벡터 데이터의 시각적 충실도를 그대로 유지합니다.

## 결론

이제 Aspose.CAD for Java를 사용해 **PNG 썸네일 IFC** 파일을 생성하는 완전한 프로덕션‑레디 방법을 갖추었습니다. 이 단계를 데스크톱 도구, 서버‑사이드 서비스 또는 클라우드 함수에 통합하여 BIM 시각화 파이프라인을 자동화하고 최종 사용자에게 빠르고 고품질의 썸네일을 제공하세요.

---

**Last Updated:** 2026-10-19  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose

## 관련 튜토리얼

- [How to Convert STL to PNG with Aspose.CAD for Java](/cad/java/cad-export-options/export-stl-to-png/)
- [Convert DWG to PNG – Save CAD as PNG Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)
- [Export DWG to PDF in Java – Set PDF Page Size with Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}