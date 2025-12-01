---
date: 2025-12-01
description: Aspose.CAD for Java를 사용하여 PDF 페이지 크기를 설정하고, DWG를 PDF로 변환하며, DWG 변경 사항
  추적을 활성화하는 방법을 배웁니다.
language: ko
linktitle: Set PDF Page Size and Track DWG with Java
second_title: Aspose.CAD Java API
title: Aspose.CAD Java로 PDF 페이지 크기 설정 및 DWG 추적
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PDF 페이지 크기 설정 및 Aspose.CAD Java로 DWG 추적

## 소개

CAD 프로젝트를 협업할 때 일관된 레이아웃을 위해 **PDF 페이지 크기 설정**, **DWG를 PDF로 변환**, 그리고 도면에 이루어진 모든 변경 사항을 추적해야 할 때가 많습니다. Aspose.CAD for Java는 이러한 모든 작업을 하나의 간소화된 워크플로우로 구현할 수 있게 해줍니다. 이 튜토리얼에서는 **PDF 페이지 크기 설정**, **DWG 변경 사항 추적** 활성화, 그리고 도면을 PDF로 내보내는 정확한 단계를 Java를 사용해 살펴보겠습니다.

## 빠른 답변
- **PDF 페이지 크기를 어떻게 설정하나요?** 내보내기 전에 `CadRasterizationOptions.setPageWidth()`와 `setPageHeight()`를 사용합니다.  
- **내보내면서 추적을 할 수 있나요?** 예 – 커스텀 `CadRenderHandler`를 구현해 추적 결과를 캡처합니다.  
- **DWG를 PDF로 변환하는 메서드는?** 옵션을 구성한 뒤 `image.save(stream, pdfOptions)`를 호출합니다.  
- **주요 전제 조건은 무엇인가요?** JDK, Aspose.CAD for Java, 그리고 DWG/DXF 파일이 들어 있는 폴더.  
- **프로덕션에 라이선스가 필요한가요?** 예, 비시험 배포에는 유효한 Aspose.CAD 라이선스가 필요합니다.

## “PDF 페이지 크기 설정”이 DWG 내보내기와 관련된 의미는?

PDF 페이지 크기 설정은 결과 PDF 캔버스의 차원(너비 × 높이, 픽셀)을 결정합니다. 이는 특정 용지 크기나 화면 레이아웃에 맞게 내보낸 도면을 맞추고, 모든 요소가 정확히 기대한 위치에 표시되도록 하는 데 필수적입니다.

## DWG 파일을 내보낼 때 추적을 활성화하는 이유는?

추적(변경 추적)은 변환 과정에서 발생하는 렌더링 문제, 누락된 폰트, 지원되지 않는 엔티티 등을 기록합니다. 이 정보를 캡처하면 다음을 수행할 수 있습니다:

- 최종 전달 전에 수정이 필요한 문제를 빠르게 식별합니다.  
- 무엇이 변경되었거나 누락되었는지 팀원에게 명확히 피드백합니다.  
- 규제가 엄격한 산업 분야를 위한 감사 추적을 유지합니다.

## 전제 조건

- **Java Development Kit (JDK)** – 최신 버전(8 이상)  
- **Aspose.CAD for Java** – 공식 [Aspose CAD 다운로드 페이지](https://releases.aspose.com/cad/java/)에서 다운로드  
- **문서 디렉터리** – 처리하려는 DWG/DXF 파일이 들어 있는 폴더

## 네임스페이스 가져오기

필요한 Aspose.CAD 클래스와 표준 Java I/O 클래스를 가져옵니다.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
```

## 1단계: DWG(또는 DXF) 파일 로드

소스 도면을 `Image` 객체에 로드합니다. 경로를 자신의 디렉터리로 조정하세요.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## 2단계: PDF 내보내기 옵션 구성(페이지 크기 포함)

여기서 PDF 옵션을 설정하고 **PDF 페이지 크기**를 800 × 600 픽셀로 명시적으로 **설정**합니다. 주요 키워드가 적용되는 부분입니다.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // set PDF page width
cadRasterizationOptions.setPageHeight(600);  // set PDF page height
```

## 3단계: 추적 구현

변환 과정 중에 추적 정보를 받을 커스텀 오류 처리기를 생성합니다.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## 4단계: PDF로 내보내기

옵션과 추적 핸들러가 준비되면 도면을 내보냅니다. 이 단계는 **DWG를 PDF로 변환**(또는 예제에서는 DXF를 PDF로 변환)합니다.

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## 5단계: CadRenderHandler 클래스 – 추적 결과 캡처

`ErrorHandler` 클래스는 `CadRenderHandler`를 확장하고 **DWG 파일 변경 추적** 중 발생한 렌더링 문제를 출력합니다.

```java
public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler {
    @Override
    public void invoke(CadRenderResult result) {
        System.out.println("Tracking results of exporting");

        if (result.isRenderComplete())
            return;

        System.out.println("Have some problems:");

        int idxError = 1;
        for (RenderResult rr : result.getFailures()) {
            System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
            idxError++;
        }
    }
}
```

## 일반적인 문제 및 해결 방법

| 문제 | 발생 이유 | 해결 방법 |
|------|-----------|-----------|
| **폰트 누락** | CAD 파일이 서버에 설치되지 않은 폰트를 참조 | 필요한 폰트를 설치하거나 소스 도면에 포함 |
| **지원되지 않는 엔티티** | 일부 DWG 엔티티가 아직 Aspose.CAD에서 지원되지 않음 | 추적 출력을 사용해 해당 엔티티를 식별하고 도면을 단순화 |
| **잘못된 페이지 크기** | 내보내기 전에 `setPageWidth/Height`를 호출하지 않음 | 위 예시와 같이 `CadRasterizationOptions`에서 페이지 크기를 설정 |

## 자주 묻는 질문

### Q1: Aspose.CAD for Java를 사용해 다른 CAD 파일 형식에서도 추적을 활성화할 수 있나요?

A1: Aspose.CAD는 주로 DWG/DXF 파일에 대한 추적을 지원합니다. 다른 형식에 대한 기능은 공식 문서를 참고하세요.

### Q2: Aspose.CAD for Java에서 추가 내보내기 옵션을 어떻게 처리하나요?

A2: DPI, 배경 색상, 벡터 래스터화 등 다양한 옵션을 제공합니다. 자세한 내용은 [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/)을 확인하세요.

### Q3: Aspose.CAD for Java의 체험판 버전이 있나요?

A3: 예, [Aspose.CAD Free Trial](https://releases.aspose.com/)에서 무료 체험판을 다운로드할 수 있습니다.

### Q4: Aspose.CAD for Java와 관련된 지원이나 토론을 어디서 할 수 있나요?

A4: [Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)에서 질문하고 경험을 공유할 수 있습니다.

### Q5: Aspose.CAD for Java용 임시 라이선스를 어떻게 얻나요?

A5: 평가용 시간 제한 라이선스는 [Temporary License](https://purchase.aspose.com/temporary-license/) 페이지의 안내를 따라 요청하세요.

### Q6: **DWG를 PDF로 변환**하면서 레이어를 보존할 수 있나요?

A6: 예, `CadRasterizationOptions`를 구성하면 결과 PDF에 레이어 정보를 보존할 수 있습니다.

### Q7: 사용자 정의 페이지 크기로 **DWG를 PDF로 내보내는** 최적 방법은?

A7: `image.save()`를 호출하기 전에 `setPageWidth`와 `setPageHeight`로 원하는 너비와 높이를 설정하면 됩니다 – Step 2에서 보여준 대로.

## 결론

위 단계들을 따르면 Aspose.CAD for Java를 사용해 **PDF 페이지 크기 설정**, **DWG를 PDF로 변환**, 그리고 **DWG 파일의 변경 사항 추적**을 수행할 수 있습니다. 이 워크플로우는 출력 레이아웃에 대한 완전한 제어를 제공하고, CAD 협업을 원활하고 오류 없이 유지하는 데 필요한 진단 정보를 제공합니다. 추가 렌더링 옵션을 탐색하고 이 코드를 더 큰 자동화 파이프라인에 통합해 보세요.

---

**마지막 업데이트:** 2025-12-01  
**테스트 환경:** Aspose.CAD for Java 24.12 (작성 시 최신 버전)  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}