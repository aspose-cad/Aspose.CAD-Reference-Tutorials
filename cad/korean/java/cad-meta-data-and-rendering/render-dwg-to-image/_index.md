---
date: 2025-12-28
description: Aspose.CAD for Java를 사용하여 DWG를 PDF로 변환해 CAD에서 PDF를 만드는 방법을 배웁니다. 단계별
  지침에 따라 DWG 레이아웃을 PDF로 내보내고 이미지를 생성합니다.
linktitle: Render DWG Document to Image with Java
second_title: Aspose.CAD Java API
title: 'CAD에서 PDF 생성 - Aspose.CAD for Java를 사용한 DWG를 이미지로 변환'
url: /ko/java/cad-meta-data-and-rendering/render-dwg-to-image/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java를 사용하여 DWG 문서를 이미지로 렌더링

## 소개

동적인 Java 개발 세계에서 Aspose.CAD는 컴퓨터 지원 설계(CAD) 파일을 처리하는 강력한 도구로 돋보입니다. **이 튜토리얼은 DWG 문서를 이미지로 렌더링한 다음 PDF로 내보내어 CAD에서 PDF를 만드는 방법**을 보여줍니다. 숙련된 개발자이든 코딩 여정을 시작한 초보자이든, 이 단계별 가이드는 명확하고 쉽게 과정을 안내합니다.

## 빠른 답변
- **어떤 라이브러리가 필요합니까?** Aspose.CAD for Java.
- **DWG를 PDF로 변환할 수 있나요?** Yes – the example demonstrates converting a DWG layout to PDF.
- **프로덕션에 라이선스가 필요합니까?** A valid Aspose.CAD license is required for non‑evaluation use.
- **지원되는 IDE는 무엇입니까?** Eclipse, IntelliJ IDEA, NetBeans, and any IDE that supports Java.
- **사용 가능한 출력 형식은 무엇입니까?** PDF, PNG, JPEG, BMP, and other raster formats.

## CAD에서 PDF 만들기란 무엇인가요?
CAD에서 PDF를 만든다는 것은 벡터 기반 도면(예: DWG 파일)을 PDF 문서로 래스터화하거나 벡터화하는 것을 의미합니다. 이를 통해 원본 CAD 애플리케이션 없이도 기술 도면을 쉽게 공유, 인쇄 및 보관할 수 있습니다.

## 왜 Aspose.CAD for Java를 사용하나요?
- **외부 종속성 없음** – 라이브러리가 바로 사용할 수 있습니다.
- **고충실도 렌더링** – 선 굵기, 레이어 및 레이아웃을 유지합니다.
- **배치 처리** – 한 번에 여러 도면을 변환할 수 있습니다.
- **크로스‑플랫폼** – Windows, Linux, macOS에서 작동합니다.

## 전제 조건

- **Java Development Environment** – JDK 8 이상이 설치되어 있어야 합니다.
- **Aspose.CAD for Java Library** – [download link](https://releases.aspose.com/cad/java/)에서 다운로드합니다.
- **DWG Document** – 렌더링하려는 DWG 파일(샘플 또는 직접 보유한 파일)입니다.

## 네임스페이스 가져오기

Java 코드에서 Aspose.CAD 기능을 활용하기 위해 필요한 클래스를 가져옵니다:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

이제 예제 코드를 여러 단계로 나누어 자세히 살펴보겠습니다:

## 단계 1: 리소스 디렉터리 지정

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

`"Your Document Directory"`를 DWG 파일이 저장된 실제 경로로 교체합니다.

## 단계 2: DWG 문서 로드

```java
String srcFile = dataDir + "visualization_-_conference_room.dwg";
Image image = Image.load(srcFile);
```

이 코드는 DWG 파일을 Aspose.CAD가 작업할 수 있는 `Image` 객체로 로드합니다.

## 단계 3: 래스터화 옵션 설정

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[] {"Layout1"});
```

여기서 도면을 어떻게 래스터화할지 정의합니다: 페이지 크기와 렌더링할 특정 레이아웃. 이는 **render dwg to image**와 **export dwg layout pdf**를 위한 핵심 단계입니다.

## 단계 4: PDF 옵션 생성

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

`PdfOptions`는 래스터화 설정을 PDF 출력 형식에 연결합니다.

## 단계 5: PDF로 내보내기

```java
image.save(dataDir + "ExportSpecificLayoutToPDF_out_.pdf", pdfOptions);
```

`save` 메서드는 렌더링된 이미지를 PDF 파일로 저장하여 **convert dwg to pdf**를 실현합니다.

## 일반적인 문제 및 해결책
| 문제 | 해결책 |
|-------|----------|
| **파일을 찾을 수 없음** | `dataDir`가 올바른 폴더를 가리키고 있는지, DWG 파일 이름이 정확한지 확인합니다. |
| **빈 PDF 출력** | 레이아웃 이름(`"Layout1"`)이 DWG 파일에 존재하는지 확인하고, `image.getAvailableLayouts()`를 사용해 레이아웃 목록을 확인합니다. |
| **낮은 이미지 품질** | `PageWidth`와 `PageHeight`를 늘리거나 `rasterizationOptions.setResolution(300);`을 설정합니다. |

## 자주 묻는 질문

### Q1: 단일 DWG 파일에서 여러 레이아웃을 렌더링할 수 있나요?
A1: Yes, you can. Simply modify the layout names in the `setLayouts` array accordingly.

### Q2: Aspose.CAD는 다양한 Java IDE와 호환되나요?
A2: Yes, Aspose.CAD is compatible with popular Java IDEs like Eclipse, IntelliJ IDEA, and others.

### Q3: 추가적인 도움과 지원을 어디서 찾을 수 있나요?
A3: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community support and discussions.

### Q4: Aspose.CAD 임시 라이선스를 어떻게 얻을 수 있나요?
A4: You can acquire a temporary license from [here](https://purchase.aspose.com/temporary-license/).

### Q5: Aspose.CAD에서 더 많은 렌더링 옵션을 제공하나요?
A5: Certainly, explore the extensive [documentation](https://reference.aspose.com/cad/java/) for detailed information.

---

**마지막 업데이트:** 2025-12-28  
**테스트 환경:** Aspose.CAD for Java 24.11  
**작성자:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
