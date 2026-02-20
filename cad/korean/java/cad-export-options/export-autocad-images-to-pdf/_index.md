---
date: 2026-02-20
description: Java용 Aspose.CAD를 사용하여 AutoCAD PDF를 내보내는 방법을 배워보세요. 이 단계별 가이드는 **DWG를
  PDF로 변환**, **CAD를 PDF로 저장**, 그리고 라이선스 처리를 보여줍니다.
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: DWG를 PDF로 변환 - Aspose.CAD for Java로 AutoCAD 이미지 PDF 내보내기
url: /ko/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export AutoCAD PDF - Aspose.CAD for Java를 사용한 AutoCAD 이미지 PDF 내보내기

## 소개

Java를 사용하여 **DWG를 PDF로 변환**하려고 하시나요? 더 이상 찾지 마세요! 이 튜토리얼에서는 Aspose.CAD for Java를 사용하여 AutoCAD 이미지를 PDF로 변환하는 방법을 단계별로 안내합니다. 이 강력한 라이브러리를 통해 **DWG를 PDF로 변환** 작업이 손쉽게 이루어집니다. 마지막까지 진행하면 **CAD를 PDF로 저장**하는 방법, 사용자 정의 래스터화 설정 적용 방법, 그리고 프로덕션 사용을 위한 Aspose.CAD 라이선스 활용 방법을 이해하게 됩니다.

## 빠른 답변
- **Java로 DWG를 PDF로 변환할 수 있나요?** 예, Aspose.CAD for Java는 DWG, DXF 및 기타 많은 형식을 처리합니다.  
- **라이선스가 필요합니까?** 무제한 사용을 위해 **Aspose CAD license**가 필요하며, 평가용 임시 라이선스도 제공됩니다.  
- **지원되는 Java 버전은 무엇입니까?** Java 8+ (모든 최신 JDK와 호환됩니다).  
- **PDF 페이지 크기를 맞춤 설정할 수 있나요?** 물론입니다 – 래스터화 옵션에서 `pageWidth`와 `pageHeight`를 조정하면 됩니다.  
- **3‑D 래스터화가 가능합니까?** 예, 전체 3‑D 렌더링을 위해 `TypeOfEntities.Entities3D`를 활성화하십시오.

## **export autocad pdf**란?
AutoCAD PDF 내보내기는 벡터 기반 CAD 도면(DWG, DXF, DWF 등)을 레이어, 선 굵기 및 선택적으로 3‑D 기하 정보를 유지한 채 휴대용 PDF 문서로 변환하는 것을 의미합니다. 이는 클라이언트와 디자인을 공유하거나, 보관하거나, CAD 소프트웨어 없이 인쇄할 때 유용합니다.

## 왜 Aspose.CAD for Java로 DWG를 PDF로 변환해야 할까요?
- **Full format support** – DWG, DXF, DWF 등 다양한 형식을 지원합니다.  
- **No external dependencies** – 순수 Java 라이브러리이며 네이티브 DLL이 필요 없습니다.  
- **High‑quality rasterization** – DPI, 페이지 크기 및 레이아웃을 제어할 수 있어 프로젝트 요구에 맞게 **PDF 페이지 크기 맞춤**이 가능합니다.  
- **License flexibility** – 무료 체험으로 시작한 뒤 영구 **Aspose CAD license**로 업그레이드할 수 있습니다.  

## 사전 요구 사항

시작하기 전에 다음을 준비하십시오:

- **Java Development Environment** – JDK 8 이상이 설치되어 있어야 합니다.  
- **Aspose.CAD for Java Library** – **[download link](https://releases.aspose.com/cad/java/)**에서 다운로드합니다.  
- **Document Directory** – 소스 CAD 파일과 생성된 PDF가 저장될 **귀하의** 컴퓨터에 있는 폴더입니다.

## 네임스페이스 가져오기

Java 프로젝트에서 Aspose.CAD와 작업하기 위해 필요한 클래스를 가져옵니다:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

이제 코드를 단계별로 살펴보겠습니다.

## Aspose.CAD for Java로 DWG를 PDF로 변환하는 방법

### 단계 1: 리소스 디렉터리 경로 설정

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Pro tip:** `"Your Document Directory"`를 사전 요구 사항에서 만든 폴더의 절대 경로로 교체하십시오.

### 단계 2: CAD 이미지 로드

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Why this matters:** CAD 파일을 `Image` 객체로 로드하면 Aspose.CAD의 래스터화 엔진에 완전하게 접근할 수 있습니다.

### 단계 3: 래스터화 옵션 설정

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth`와 `pageHeight`를 조정하여 **PDF 페이지 크기 맞춤**을 할 수 있습니다.  
- 3‑D 엔터티가 필요하면 `setTypeOfEntities` 라인의 주석을 해제하십시오. (**java convert cad pdf**와 같은 경우).  
- `setLayouts` 호출은 렌더링할 레이아웃(모델, Layout1 등)을 선택합니다.

### 단계 4: PDF 옵션 구성

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

이 설정은 래스터화 옵션을 PDF 출력에 연결하여 벡터 데이터가 올바르게 변환되도록 합니다.

### 단계 5: PDF 저장

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

생성된 파일 `Export3DImagestoPDF_out_.pdf`는 원본 AutoCAD 도면의 **CAD를 PDF로 저장** 표현입니다.

## 일반적인 문제 및 해결책

| 증상 | 가능한 원인 | 해결 방법 |
|------|------------|----------|
| 빈 PDF 출력 | 래스터화 옵션이 설정되지 않았거나 레이아웃이 일치하지 않음 | `setLayouts`가 CAD 파일의 레이아웃 이름과 일치하는지 확인하십시오. |
| 저해상도 이미지 | `pageWidth`/`pageHeight`가 너무 작음 | 크기를 늘리거나 `rasterizationOptions.setResolution(...)`를 사용해 DPI를 높이십시오. |
| 라이선스 예외 | 유효한 라이선스가 적용되지 않음 | **Aspose CAD license**를 적용하거나 테스트용 임시 라이선스를 사용하십시오. |

## 자주 묻는 질문

### Q1: Aspose.CAD for Java를 다른 CAD 파일 형식과 함께 사용할 수 있나요?
A1: 예, Aspose.CAD는 DWG, DWF, DGN 등을 포함한 다양한 형식을 지원하므로 프로젝트에서 유연하게 사용할 수 있습니다.

### Q2: Aspose.CAD for Java용 임시 라이선스를 어떻게 얻을 수 있나요?
A2: 평가용 임시 라이선스를 받으려면 [here](https://purchase.aspose.com/temporary-license/)를 방문하십시오.

### Q3: 래스터화에 대한 레이아웃 옵션이 있나요?
A3: 예, `setLayouts` 메서드를 통해 `"Model"`, `"Layout1"` 등 원하는 레이아웃을 맞춤 설정하여 어떤 뷰를 렌더링할지 제어할 수 있습니다.

### Q4: 출력 PDF 파일의 크기를 맞춤 설정할 수 있나요?
A4: 물론입니다! 래스터화 옵션에서 `pageWidth`와 `pageHeight` 매개변수를 조정하여 원하는 치수에 맞출 수 있습니다.

### Q5: Aspose.CAD for Java와 관련된 도움이나 토론을 어디서 할 수 있나요?
A5: 전용 지원 및 커뮤니티 토론을 위해 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)으로 이동하십시오.

**마지막 업데이트:** 2026-02-20  
**테스트 환경:** Aspose.CAD for Java 24.10  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}