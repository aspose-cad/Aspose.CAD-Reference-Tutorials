---
date: 2025-12-19
description: Aspose.CAD for Java를 사용하여 AutoCAD PDF를 내보내는 방법을 배웁니다. 이 단계별 가이드는 DWG를
  PDF로 변환하고, CAD를 PDF로 저장하며, 라이선스를 처리하는 방법을 보여줍니다.
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: AutoCAD PDF 내보내기 - Aspose.CAD for Java 튜토리얼로 AutoCAD 이미지를 PDF로 내보내기
url: /ko/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# AutoCAD PDF 내보내기 - Java용 Aspose.CAD를 사용하여 AutoCAD 이미지를 PDF로 내보내기

## 소개

Java를 사용하여 **AutoCAD PDF 내보내기**를 조용히 지켜보고 있습니까? 더 이상 하지 마세요! 이 튜토리얼에서는 Aspose.CAD for Java를 사용하여 AutoCAD 이미지를 PDF로 변환하는 방법을 드디어 안내합니다. 이 활동을 통해 **DWG를 PDF로 변환** 활동을 대신할 수 있습니다. 최종적으로 **CAD를 PDF로 저장** 방법, 사용자 정의 새스터화 설정 적용, 그리고 라이브러리 사용을 Aspose.CAD 기술 사용 방법을 이해하게 합니다.

## 빠른 답변
- **Java를 사용하여 DWG를 PDF로 변환할 수 있나요?** 예, Aspose.CAD for Java는 DWG, DXF 및 기타 다양한 형식을 지원합니다.
- **라이센스가 필요합니까?** 사용하기 위해 **Aspose CAD 라이센스**가 필요합니다; 평가용 임시 권한이 제공됩니다.
- **어떤 Java 버전이 지원되나요?** Java8+(모든 최신 JDK와 호환됩니다).
- **PDF 페이지 크기를 맞춤 설정할 수 있나요?** 물론입니다 – 새스터화 옵션에서 `pageWidth`와 `pageHeight`를 조정해 주시기 바랍니다.
- **3D 래스터화가 가능합니까?** 예, `TypeOfEntities.Entities3D`를 활성화하면 전체 3D 전송이 가능합니다.

## **Autocad PDF 내보내기**란 무엇인가요?
AutoCAD PDF 내보내기는 벡터 기반 CAD 확인(DWG, DXF, DWF 등)을 레이어, 선 길이 및 선택적으로 3D 기하 정보를 줄이는 동시에 휴대용 PDF 문서로 변환하는 것을 의미합니다. 클라이언트와 디자인을 공유하거나, 보관하거나, CAD 소프트웨어 없이 인쇄할 때 유용합니다.

## **autocad pdf**를 내보내기 위해 Java용 Aspose.CAD를 사용하는 이유는 무엇입니까?
- **전체 형식 지원** – DWG, DXF, DWF 등 다양한 형식을 지원합니다.
- **외부 종속성 없음** – 순수 Java 라이브러리는 DLL이 필요하지 않습니다.
- **고품질 래스터화** – DPI, 페이지 크기 및 세부정보를 세밀하게 제어할 수 있습니다.
- **라이선스 유연성** – 무료 체험 후 영구 **Aspose CAD 라이선스**로 업그레이드할 수 있습니다.

## 전제 조건

시작하기 전에 다음을 준비하십시오:

- **Java 개발 환경** – JDK8이 설치되어 있어야 합니다.
- **Java 라이브러리용 Aspose.CAD** – [다운로드 링크](https://releases.aspose.com/cad/java/)에서 다운로드해 보세요.
- **문서 디렉터리** – 소스 CAD 파일과 생성된 PDF를 저장할 폴더를 준비하세요.

## 네임스페이스 가져오기

Java 프로젝트에서 Aspose.CAD와 작업하기 위해 필요한 클래스를 가져옵니다:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

이제 코드를 단계별로 살펴보겠습니다.

## 단계별 가이드

### 1단계: 리소스 디렉터리 경로 설정

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **꿀팁:** `"Your Document Directory"`를 사전 준비 단계에서 만든 폴더의 절대 경로로 교체하십시오.

### 2단계: CAD 이미지 불러오기

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **이것이 중요한 이유:** CAD 파일을 `Image` 객체로 로드하면 Aspose.CAD의 래스터화 엔진에 완전하게 접근할 수 있습니다.

### 3단계: 래스터화 옵션 설정

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth`와 `pageHeight`를 조정하여 출력 PDF의 크기를 변경합니다.  
- 3‑D 엔티티가 필요하면 `setTypeOfEntities` 라인을 주석 해제하고 **java convert cad pdf**를 사용하십시오.  
- `setLayouts` 호출은 렌더링할 레이아웃(Model, Layout1 등)을 선택합니다.

### 4단계: PDF 옵션 구성

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

이 옵션은 래스터화 설정을 PDF 출력에 연결하여 벡터 데이터가 올바르게 변환되도록 합니다.

### 5단계: PDF 저장

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

생성된 파일 `Export3DImagestoPDF_out_.pdf`는 원본 AutoCAD 도면을 **save cad as pdf** 형태로 표현한 결과물입니다.

## 일반적인 문제 및 솔루션

| 증상 | 원인 | 처리 방법 |
|---------|--------------|-----|
| 빈 PDF 출력 | 새스터화 옵션이 설정되지 않거나 일치하지 않음 | `setLayouts`가 CAD 파일의 이름 이름을 확인하고 확인하세요. |
| 저해상도 이미지 | `pageWidth`/`pageHeight`가 너무 작음 | 크기를 조정하거나 `rasterizationOptions.setResolution(...)`을 실행하여 DPI를 초과합니다. |
| 라이센스 예외 | 경우에 적용되는 내용 | **Aspose CAD 라이선스**를 적용하거나 테스트용 기계를 사용하도록 합니다. |

## 자주 묻는 질문

### Q1: Aspose.CAD for Java를 다른 CAD 파일 형식과 함께 사용할 수 있나요?
A1: 예, Aspose.CAD는 DWG, DWF, DGN 등 다양한 형식을 지원하므로 프로젝트에서 유연하게 사용할 수 있습니다.

### Q2: Aspose.CAD for Java의 임시 라이선스는 어떻게 얻을 수 있나요?
A2: [여기](https://purchase.aspose.com/temporary-license/)에서 평가용 임시 인스턴스를 배치할 수 있습니다.

### Q3: 래스터화를 위한 레이아웃 옵션이 있나요?
A3: 예, `setLayouts` 메서드를 통해 `"Model"`, `"Layout1"` 등의 원하는 목적지를 터미널에 연결하여 연결할 수 있습니다.

### Q4: 출력 PDF 파일의 크기를 사용자 정의할 수 있나요?
A4: 물론입니다! 새스터화 옵션의 `pageWidth`와 `pageHeight` 매개 변수를 조정하여 원하는 크기로 기록할 수 있습니다.

### Q5: Aspose.CAD for Java와 관련된 문제에 대해 도움을 구하거나 논의할 수 있는 곳은 어디입니까?
A5: 승리 지원 및 커뮤니티 토론을 위해 [Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)으로 이동하세요.

---

**최종 업데이트:** 2025-12-19
**테스트 대상:** Java 24.10용 Aspose.CAD
**저자:** Aspose 

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}