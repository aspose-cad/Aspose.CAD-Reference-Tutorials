---
date: 2026-06-29
description: Aspose.CAD for Java를 사용하여 DWG에서 PDF를 생성하고 PDF 레이아웃을 맞춤 설정하는 방법을 배웁니다.
  Java 개발자를 위한 쉬운 통합.
keywords:
- create pdf from dwg
- convert cad to pdf
- pdf different page sizes
- export dwg to pdf
- customize pdf layout
linktitle: 다양한 레이아웃을 가진 단일 PDF
schemas:
- author: Aspose
  dateModified: '2026-06-29'
  description: Learn how to create PDF from DWG and customize PDF layout using Aspose.CAD
    for Java. Easy integration for Java developers.
  headline: Create PDF from DWG with Aspose.CAD for Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD for Java integrates seamlessly with libraries such as
      Apache POI, Jackson, or Spring Boot.
    question: Can I use Aspose.CAD for Java with other Java libraries?
  - answer: Absolutely! You can access a free trial version [here](https://releases.aspose.com/).
    question: Is there a trial version available?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and discussions.
    question: Where can I find additional support?
  - answer: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license?
  - answer: Purchase the full version of Aspose.CAD for Java [here](https://purchase.aspose.com/buy).
    question: Where can I purchase the full version?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java를 사용하여 DWG에서 PDF 만들기
url: /ko/java/other-cad-operations/single-pdf-different-layouts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG에서 PDF 만들기 Aspose.CAD for Java 사용

## 소개

이 튜토리얼에서는 Aspose.CAD for Java를 사용하여 **DWG에서 PDF 만들기** 파일을 생성하고 여러 페이지 크기 레이아웃을 적용합니다. 건설 설계도, 엔지니어링 도면, 마케팅용 PDF를 생성해야 하든, 아래 단계에서는 CAD 도면을 PDF로 변환하고 각 레이아웃의 크기를 사용자 정의하며 단일 다중 페이지 문서를 생성하는 방법을 Java 환경을 떠나지 않고 보여줍니다.

## 빠른 답변
- **이 튜토리얼은 무엇을 다루나요?** DWG 도면을 여러 페이지 크기를 가진 단일 PDF로 변환합니다.  
- **필요한 라이브러리는?** Aspose.CAD for Java(최신 버전).  
- **라이선스가 필요합니까?** 개발용으로는 무료 체험판을 사용할 수 있으며, 상용 환경에서는 상업용 라이선스가 필요합니다.  
- **다른 형식으로 내보낼 수 있나요?** 네 – API는 PNG, JPEG, SVG로도 내보내기를 지원합니다.  
- **Java 8이면 충분한가요?** 라이브러리는 Java 8 및 이후 런타임에서 작동합니다.

## “DWG에서 PDF 만들기”란?

**DWG에서 PDF 만들기**는 AutoCAD DWG 파일을 PDF 문서로 변환하면서 벡터 정확도, 레이어, 선 굵기를 유지하고 레이아웃을 사용자 정의할 수 있게 하는 것을 의미합니다. Aspose.CAD는 이 변환을 메모리 내에서 완전히 수행하므로 외부 CAD 소프트웨어가 필요 없으며, 생성된 PDF는 직접 편집하거나 인쇄할 수 있습니다.

## DWG에서 PDF 레이아웃을 사용자 정의하는 이유

Aspose.CAD는 **30개 이상의 CAD 형식**을 지원하며 전체 파일을 메모리에 로드하지 않고도 **500 MB**까지 PDF를 생성할 수 있습니다. 각 레이아웃에 개별 페이지 크기를 정의하면 ISO, ANSI 또는 사용자 정의 치수에 맞는 인쇄용 시트를 만들 수 있어 시간 절약과 수동 후처리 제거라는 구체적인 이점을 제공합니다.

## 사전 요구 사항

이 과정을 시작하기 전에 다음이 준비되어 있는지 확인하십시오:
- Java 환경: 머신에 Java가 설치되어 있는지 확인하십시오.  
- Aspose.CAD 라이브러리: [download link](https://releases.aspose.com/cad/java/)에서 Aspose.CAD 라이브러리를 다운로드하고 설치하십시오.  
- 문서 디렉터리: DWG 도면을 위한 디렉터리를 설정하십시오.

## 패키지 가져오기

`CadImage` 클래스는 메모리 내에서 CAD 도면을 나타내는 Aspose.CAD의 핵심 객체입니다. 시작하기 전에 필요한 네임스페이스를 가져오세요:

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## 단계 1: CAD 도면 로드

`CadImage`는 DWG 파일을 로드하고 벡터 데이터에 접근할 수 있게 합니다. CAD 도면을 `CadImage` 객체에 로드하십시오:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## 단계 2: 래스터화 옵션 구성

`RasterizationOptions`는 CAD 벡터가 PDF에 배치되기 전에 어떻게 래스터화될지를 정의합니다. CAD 이미지에 대한 래스터화 옵션을 설정하십시오:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## 단계 3: 레이아웃 페이지 크기 사용자 정의

`PdfOptions`를 사용하면 DWG 내부의 각 레이아웃에 고유한 페이지 치수를 지정할 수 있습니다. CAD 도면 내 여러 레이아웃에 대해 사용자 정의 크기를 정의하십시오:

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## 단계 4: PDF 옵션 설정

`PdfOptions`는 래스터화 설정과 레이아웃 정의를 결합하는 컨테이너입니다. 래스터화 설정을 포함하여 PDF 옵션을 구성하십시오:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## 단계 5: PDF로 저장

`PdfSaveOptions`는 변환을 마무리하고 출력 파일을 기록합니다. 처리된 CAD 이미지를 PDF로 저장하십시오:

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

축하합니다! Aspose.CAD for Java를 사용하여 다양한 페이지 크기로 **DWG에서 PDF 만들기**를 성공적으로 수행했습니다.

## 일반적인 문제 및 해결책

- **출력 PDF에 빈 페이지가 표시됨** – `PageSize` 값이 DWG 파일의 실제 레이아웃 치수와 일치하는지 확인하십시오.  
- **대형 도면에서 메모리 부족 오류** – `CadImage.load(..., LoadOptions)`와 `LoadOptions.setLoadMode(LoadMode.Memory)`를 사용하여 파일을 전체 로드 대신 스트리밍하십시오.  
- **스케일링이 잘못됨** – 원하는 DPI(인치당 점)와 일치하도록 `RasterizationOptions.setPageWidth` 및 `setPageHeight`를 조정하십시오.

## 자주 묻는 질문

**Q: Aspose.CAD for Java를 다른 Java 라이브러리와 함께 사용할 수 있나요?**  
A: 네, Aspose.CAD for Java는 Apache POI, Jackson, Spring Boot와 같은 라이브러리와 원활하게 통합됩니다.

**Q: 체험판 버전이 제공되나요?**  
A: 물론입니다! 무료 체험판은 [here](https://releases.aspose.com/)에서 이용할 수 있습니다.

**Q: 추가 지원은 어디서 찾을 수 있나요?**  
A: 커뮤니티 지원 및 토론을 위해 [Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)을 방문하십시오.

**Q: 임시 라이선스는 어떻게 얻나요?**  
A: 임시 라이선스는 [here](https://purchase.aspose.com/temporary-license/)에서 받을 수 있습니다.

**Q: 정식 버전은 어디서 구매하나요?**  
A: Aspose.CAD for Java 정식 버전은 [here](https://purchase.aspose.com/buy)에서 구매하십시오.

---

**마지막 업데이트:** 2026-06-29  
**테스트 환경:** Aspose.CAD for Java 24.10  
**작성자:** Aspose

## 관련 튜토리얼

- [Aspose.CAD for Java를 사용하여 DWG를 PDF 또는 래스터로 내보내기](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Aspose.CAD for Java로 CAD 레이아웃을 PDF로 내보내기](/cad/java/cad-export-options/export-cad-layouts-to-pdf/)
- [Aspose.CAD for Java를 사용하여 특정 DWG 레이아웃을 PDF로 내보내기](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}