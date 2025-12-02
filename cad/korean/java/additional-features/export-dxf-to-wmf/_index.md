---
date: 2025-11-29
description: Aspose.CAD for Java를 사용하여 DXF를 WMF로 변환하고, DXF 도면을 로드하며, 필요에 따라 Aspose를
  이용해 PDF로 내보내는 방법을 배웁니다. 코드 예제가 포함된 단계별 가이드.
language: ko
linktitle: Export DXF to WMF Format Using Java
second_title: Aspose.CAD Java API
title: Java에서 Aspose.CAD를 사용하여 DXF를 WMF로 변환
url: /java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java를 사용하여 DXF를 WMF로 변환하기

## 소개

이 튜토리얼에서는 **Aspose.CAD for Java**를 사용해 **DXF를 WMF로 변환**하는 방법을 알아봅니다. Windows 기반 보고서에 CAD 도면을 삽입하거나 가벼운 벡터 형식이 필요할 때, DXF를 WMF로 변환하는 요구는 흔합니다. DXF 도면을 로드하고, 래스터화 옵션을 설정한 뒤, WMF로 저장하는 과정을 단계별로 안내하고, 선택적으로 Aspose를 이용해 PDF로 내보내는 방법도 소개합니다.

## 빠른 답변
- **무료 체험으로 DXF를 WMF로 변환할 수 있나요?** 예 – Aspose는 30일 완전 기능 체험판을 제공합니다.  
- **필요한 Java 버전은?** Java 8 이상.  
- **코드를 실행하려면 라이선스가 필요한가요?** 프로덕션에서는 라이선스가 필요하지만, 개발 및 테스트 단계에서는 체험판으로 동작합니다.  
- **변환이 무손실인가요?** 벡터 데이터는 보존되며, 래스터화 옵션을 통해 해상도를 조절할 수 있습니다.  
- **같은 도면을 PDF로도 내보낼 수 있나요?** 물론입니다 – 아래 “PDF로 내보내기” 단계를 참고하세요.

## “DXF를 WMF로 변환”이란?

DXF를 WMF로 변환한다는 것은 널리 사용되는 CAD 형식인 Drawing Exchange Format(DXF) 파일을 Windows Metafile(WMF) 형식으로 바꾸는 것을 의미합니다. WMF는 벡터 이미지 형식으로 Microsoft Office, Windows 애플리케이션 및 다양한 보고서 도구와 원활하게 통합됩니다.

## 왜 Aspose.CAD for Java를 사용하나요?

- **외부 의존성 없음** – 순수 Java 구현, 네이티브 DLL 필요 없음.  
- **고품질 보존** – 레이어, 색상, 라인 스타일을 그대로 유지.  
- **내장 래스터화** – 페이지 크기, 해상도, 배경을 세밀하게 조정 가능.  
- **올인원 솔루션** – 동일 API로 PDF, PNG, SVG 등 다양한 포맷으로 내보내기 지원.

## 사전 준비

시작하기 전에 다음을 준비하세요:

- **Aspose.CAD for Java**를 프로젝트에 통합합니다. 공식 사이트에서 다운로드: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- **문서 디렉터리**에 DXF 파일이 저장된 경로가 있어야 합니다(예: `Your Document Directory/DXFDrawings/`).  

## 네임스페이스 가져오기

Java 소스 파일에서 필요한 Aspose.CAD 클래스를 import 합니다:

```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

## 단계별 가이드

### 단계 1: DXF 도면 로드

먼저 변환하려는 **DXF 도면을 로드**합니다. `Image.load` 메서드가 파일을 메모리로 읽어들입니다.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### 단계 2: 래스터화 옵션 구성

출력 WMF의 크기를 제어하는 래스터화 매개변수를 설정합니다. 여기서는 100 × 100 단위 페이지를 예시로 사용합니다.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

### 단계 3: WMF로 저장

앞서 정의한 옵션을 사용해 로드한 도면을 WMF 파일로 저장합니다.

```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

### 단계 4: 리소스 해제

많은 도면을 처리할 경우 메모리 누수를 방지하기 위해 리소스를 적절히 해제합니다.

```java
finally
{
  cadImage.dispose();
}
```

### 단계 5: 선택 사항 – Aspose를 이용한 PDF 내보내기

같은 도면을 PDF 형식으로도 필요하다면 Aspose.CAD가 한 줄 코드로 처리해 줍니다.

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

> **전문가 팁:** `CadRasterizationOptions` 객체를 그대로 재사용하여 `PdfOptions` 인스턴스에 전달하면 PDF 내보내기가 가능합니다.

## 일반적인 문제와 해결책

| 문제 | 원인 | 해결 방법 |
|-------|-------|-----|
| **`NullPointerException` on `cadImage.save`** | 변수 `cadImage`가 정의되지 않음(정확히는 `image`여야 함). | `cadImage`를 `image`로 교체하거나 변수명을 일관되게 변경합니다. |
| **출력 WMF가 빈 화면** | 래스터화 페이지 크기가 너무 작거나 배경색이 투명하게 설정됨. | `PageWidth`/`PageHeight`를 늘리거나 `rasterizationOptions.setBackgroundColor(Color.getWhite());`와 같이 배경색을 지정합니다. |
| **라이선스 예외** | 프로덕션 환경에서 유효한 Aspose 라이선스 없이 실행. | 애플리케이션 시작 시 라이선스 파일을 적용합니다: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## 결론

이제 **Aspose.CAD for Java**를 사용해 **DXF를 WMF로 변환**하고, 필요에 따라 **PDF로 내보내는** 전체 프로덕션 워크플로우를 완성했습니다. 이 방법을 통해 Windows 기반 보고서 및 문서 도구와 원활히 통합되는 고품질 벡터 출력을 얻을 수 있습니다.

## FAQ

### Q1: Aspose.CAD 문서는 어디서 찾을 수 있나요?

A1: 문서는 [여기](https://reference.aspose.com/cad/java/)에서 확인할 수 있습니다.

### Q2: Aspose.CAD for Java를 어떻게 다운로드하나요?

A2: 라이브러리는 [여기](https://releases.aspose.com/cad/java/)에서 다운로드합니다.

### Q3: 무료 체험판이 있나요?

A3: 예, 무료 체험판은 [여기](https://releases.aspose.com/)에서 받을 수 있습니다.

### Q4: 임시 라이선스 옵션이 필요합니다?

A4: 임시 라이선스는 [여기](https://purchase.aspose.com/temporary-license/)에서 확인하세요.

### Q5: 지원을 어디서 받을 수 있나요?

A5: Aspose.CAD 지원 포럼은 [여기](https://forum.aspose.com/c/cad/19)에서 이용할 수 있습니다.

## 자주 묻는 질문

**Q: 수백 MB 규모의 대용량 DXF 파일을 메모리 부족 없이 변환할 수 있나요?**  
A: 가능합니다. `try‑with‑resources` 블록으로 파일을 로드하고 `Image` 객체를 즉시 해제하세요. `CadRasterizationOptions.setPageWidth/Height`를 적절히 조정하면 메모리 사용량을 낮출 수 있습니다.

**Q: WMF 출력에 레이어 정보가 유지되나요?**  
A: WMF는 평면 벡터 형식이므로 레이어 구조는 평탄화되지만, 라인 스타일과 색상은 그대로 보존됩니다.

**Q: WMF에 사용자 정의 DPI를 설정할 수 있나요?**  
A: 저장 전에 `rasterizationOptions.setResolution(300);`와 같이 DPI를 지정하면 됩니다.

**Q: 한 번에 여러 DXF 파일을 배치 변환할 수 있나요?**  
A: 물론입니다. 디렉터리를 순회하면서 각 파일을 로드하고 동일한 래스터화·저장 로직을 적용하면 됩니다.

**Q: 지원되는 Java 버전은 어떤 것이 있나요?**  
A: Aspose.CAD for Java는 Java 8 이상을 지원하며, Java 11, 17 및 최신 LTS 버전도 포함됩니다.

---

**마지막 업데이트:** 2025-11-29  
**테스트 환경:** Aspose.CAD for Java 24.11  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}