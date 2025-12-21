---
date: 2025-12-21
description: Aspose.CAD for Java를 사용하여 특정 DWG 레이아웃을 PDF로 내보내 DWG를 PDF로 변환하는 방법을 배워보세요.
  CAD 작업 흐름을 간소화하기 위해 이 단계별 DWG to PDF 튜토리얼을 따라하세요.
linktitle: Export Specific DWG Layout to PDF
second_title: Aspose.CAD Java API
title: DWG를 PDF로 변환 – Aspose.CAD for Java로 레이아웃 내보내기
url: /ko/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG를 PDF로 변환 – Aspose.CAD for Java를 사용하여 특정 레이아웃 내보내기

## 소개

컴퓨터 지원 설계(CAD)의 역동적인 세계에서 **DWG를 PDF로 변환**은 클라이언트, 계약자 또는 비기술 이해관계자와 도면을 공유할 때 자주 요구되는 작업입니다. Aspose.CAD for Java는 이 변환을 손쉽게 수행하도록 해 주며, 다중 레이아웃 DWG 파일에서 단일 레이아웃을 선택할 수도 있습니다. 이번 튜토리얼에서는 **DWG 특정 레이아웃을 PDF로 내보내는 방법**을 단계별로 살펴보며, 불필요한 페이지나 수동 크롭 없이 프로젝트에 정확히 필요한 결과물을 제공하는 방법을 안내합니다.

## 빠른 답변
- **“DWG를 PDF로 변환”이란 무엇인가요?** DWG 도면을 PDF 문서로 변환하여 벡터 데이터와 레이아웃 정확성을 유지합니다.  
- **어떤 라이브러리가 변환을 담당하나요?** Aspose.CAD for Java가 즉시 사용 가능한 API를 제공합니다.  
- **프로덕션 환경에 라이선스가 필요하나요?** 예, 상용 라이선스가 필요합니다; 평가용 무료 체험판도 제공됩니다.  
- **단일 레이아웃을 선택할 수 있나요?** 물론입니다 – `Layouts` 속성을 원하는 레이아웃 이름으로 설정하면 됩니다.  
- **지원되는 Java 버전은 무엇인가요?** Java 8 이상과 완벽하게 호환됩니다.

## 사전 요구 사항

시작하기 전에 다음을 준비하세요:

- **Java 개발 환경** – JDK 8 이상 및 선호하는 IDE.  
- **Aspose.CAD 라이브러리** – 공식 사이트에서 최신 JAR을 **[여기](https://releases.aspose.com/cad/java/)**에서 다운로드합니다.  
- **DWG 파일** – 최소 하나 이상의 레이아웃을 포함한 도면(예: *visualization_-_conference_room.dwg*).

## 특정 DWG 레이아웃을 PDF로 내보내는 이유

많은 DWG 파일에는 여러 개의 종이 공간(레이아웃)이 포함되어 있습니다. 전체 파일을 내보내면 원하지 않는 페이지가 포함된 거대한 PDF가 생성될 수 있습니다. 단일 레이아웃을 선택하면:

- 파일 크기가 감소합니다.  
- 뷰어가 관련 도면 시트에 집중할 수 있습니다.  
- 프로젝트 문서 표준에 부합합니다.

## 단계별 가이드

### 단계 1: 프로젝트 환경 설정

새 Java 프로젝트(Maven, Gradle 또는 일반 IDE)를 만들고 Aspose.CAD JAR을 클래스패스에 추가합니다. JAR은 **[여기](https://releases.aspose.com/cad/java/)**에서 다운로드할 수 있습니다.

### 단계 2: 필요한 패키지 가져오기

Java 클래스에 필요한 Aspose.CAD 네임스페이스를 추가합니다.

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

### 단계 3: DWG 파일 로드

변환하려는 DWG 파일 경로를 지정하고 `Image` 객체에 로드합니다.

```java
String srcFile = dataDir + "visualization_-_conference_room.dwg";
Image image = Image.load(srcFile);
```

### 단계 4: 래스터화 옵션 구성

페이지 크기와 내보낼 레이아웃을 정의합니다.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
// Specify desired layout name
rasterizationOptions.setLayouts(new String[] {"Layout1"});
```

### 단계 5: PDF 내보내기 옵션 설정

래스터화 설정을 PDF 내보내기 도구에 연결합니다.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 단계 6: DWG를 PDF로 내보내기

결과를 PDF 파일로 저장합니다. 출력 파일에는 **Layout1**만 포함되어 깔끔한 **DWG를 PDF로 변환** 작업이 완료됩니다.

```java
image.save(dataDir + "ExportSpecificLayoutToPDF_out_.pdf", pdfOptions);
```

## 일반적인 문제와 해결책

| 문제 | 발생 원인 | 해결 방법 |
|------|----------|----------|
| **레이아웃을 찾을 수 없음** | 레이아웃 이름이 잘못 입력되었거나 DWG에 존재하지 않음 | `image.getLayoutNames()`를 사용해 사용 가능한 레이아웃을 나열한 후 올바른 이름을 선택합니다. |
| **PDF 해상도가 낮음** | `PageWidth`/`PageHeight` 값이 너무 작음 | 차원(예: 2000 × 2000)을 늘리거나 `rasterizationOptions.setResolution(300);`을 설정합니다. |
| **라이선스 예외** | 비시험 환경에서 유효한 라이선스 없이 실행 | 이미지 로드 전에 Aspose.CAD 라이선스를 적용합니다: `License license = new License(); license.setLicense("Aspose.CAD.lic");`. |

## 자주 묻는 질문

**Q1: Aspose.CAD for Java를 다른 Java 기반 CAD 라이브러리와 함께 사용할 수 있나요?**  
A: Aspose.CAD for Java는 독립형 라이브러리이지만, 확장 기능을 위해 다른 Java 기반 라이브러리와 통합할 수 있습니다.

**Q2: Aspose.CAD의 라이선스 옵션은 어떻게 되나요?**  
A: 라이선스 옵션 및 구매 상세 정보는 **[여기](https://purchase.aspose.com/buy)**에서 확인할 수 있습니다.

**Q3: Aspose.CAD 임시 라이선스를 어떻게 받을 수 있나요?**  
A: **[이 링크](https://purchase.aspose.com/temporary-license/)**를 방문하여 임시 라이선스를 요청하세요.

**Q4: Aspose.CAD 지원은 어디에서 받을 수 있나요?**  
A: 문의 사항이나 도움이 필요하면 **[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)**을 방문하세요.

**Q5: Aspose.CAD 무료 체험판이 있나요?**  
A: 예, 무료 체험판은 **[여기](https://releases.aspose.com/)**에서 이용할 수 있습니다.

## 결론

이 **dwg to pdf 튜토리얼**을 따라 하면 단일 레이아웃을 목표로 **DWG를 PDF로 변환**하는 신뢰할 수 있는 방법을 확보하게 됩니다. 이 접근 방식은 저장 공간을 절약하고 문서 공유 속도를 높이며 CAD 워크플로우를 깔끔하게 유지합니다. 프로젝트가 진행됨에 따라 다양한 래스터화 설정을 실험하거나 여러 레이아웃을 하나의 PDF로 결합해 보세요.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**마지막 업데이트:** 2025-12-21  
**테스트 환경:** Aspose.CAD for Java 24.12  
**작성자:** Aspose