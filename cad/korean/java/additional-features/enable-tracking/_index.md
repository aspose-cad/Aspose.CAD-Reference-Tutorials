---
date: 2025-12-03
description: Aspose.CAD for Java를 사용하여 DWG를 PDF로 변환할 때 PDF 페이지 크기를 설정하고 DWG 파일에서 추적
  기능을 활성화하는 방법을 배우세요 – 정밀하게 CAD 도면을 PDF로 내보내는 완벽한 가이드.
language: ko
linktitle: Set PDF Page Size and Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: Java에서 Aspose.CAD를 사용해 PDF 페이지 크기 설정 및 DWG 파일 추적 활성화
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java를 사용하여 DWG 파일에서 PDF 페이지 크기 설정 및 추적 활성화

## 소개

DWG를 PDF로 변환할 때 **PDF 페이지 크기**를 **설정**하고 렌더링 문제를 추적하고 싶다면, Aspose.CAD for Java가 두 작업을 모두 수행할 수 있는 깔끔하고 프로그래밍 방식의 방법을 제공합니다. 이 튜토리얼에서는 페이지 차원을 구성하고, 추적을 활성화하며, CAD 도면을 PDF로 내보내는 정확한 단계를 Java 코드로 설명합니다. 마지막까지 진행하면 CAD 도면에 적절한 페이지 크기를 지정하는 것이 왜 중요한지, 그리고 내보내기 과정에서 상세 추적 정보를 어떻게 캡처하는지 이해하게 됩니다.

## 빠른 답변
- **“PDF 페이지 크기 설정”은 무엇에 영향을 미치나요?** 결과 PDF 캔버스의 너비와 높이를 정의하여 도면이 정확히 맞도록 합니다.  
- **이 기능을 사용하려면 라이선스가 필요합니까?** 테스트용 트라이얼은 가능하지만, 상용 환경에서는 상업용 라이선스가 필요합니다.  
- **필요한 Aspose.CAD 버전은?** `CadRasterizationOptions`를 지원하는 최신 버전이면 모두 사용 가능합니다.  
- **다른 CAD 형식에서도 사용할 수 있나요?** 예제는 DWG/DXF를 사용하지만, 대부분 지원되는 형식에서도 동일한 접근 방식을 적용할 수 있습니다.  
- **변환 시간은 얼마나 걸리나요?** 보통 작은 파일은 1초 미만, 큰 도면은 더 오래 걸릴 수 있습니다.

## CAD 내보내기 맥락에서 “PDF 페이지 크기 설정”이란?
PDF 페이지 크기를 설정하면 렌더러에게 출력 캔버스의 정확한 차원(픽셀 또는 포인트)을 알려줍니다. 이는 스케일과 레이아웃을 유지해야 하는 기술 도면에서 특히 중요합니다. 페이지 크기를 명시하지 않으면 PDF가 기본 크기로 생성되어 도면이 잘리거나 왜곡될 수 있습니다.

## CAD 도면을 내보낼 때 PDF 페이지 크기를 설정해야 하는 이유
- **스케일 보존** – 엔지니어는 실제 스케일 인쇄물을 필요로 합니다.  
- **용지에 맞춤** – 프로젝트 사양에 맞는 A4, Letter 또는 사용자 정의 크기를 선택합니다.  
- **가독성 향상** – 큰 페이지는 확대 없이도 세부 사항을 명확히 보여줍니다.  
- **출력 일관성** – 자동화 파이프라인이 매 실행마다 동일한 차원의 PDF를 생성합니다.

## DWG를 PDF로 변환할 때 PDF 페이지 크기를 설정하는 방법
아래에서는 `CadRasterizationOptions`에 사용자 정의 너비와 높이 값을 지정한 뒤 내보내는 과정을 보여줍니다. 이 단계가 바로 주요 키워드 **PDF 페이지 크기 설정**을 구현합니다.

## 사전 요구 사항

- **Java Development Kit (JDK)** – Java 8 이상이 설치되어 있어야 합니다.  
- **Aspose.CAD for Java** – 공식 [Aspose CAD 다운로드 페이지](https://releases.aspose.com/cad/java/)에서 다운로드합니다.  
- **문서 디렉터리** – 처리하려는 DWG/DXF 파일이 들어 있는 폴더입니다.

## 네임스페이스 가져오기

먼저 필요한 클래스를 가져옵니다. 코드 블록은 원본 튜토리얼과 동일하게 유지됩니다.

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

## 1단계: DWG/DXF 파일 로드

소스 도면을 로드합니다. 경로를 자신의 파일 위치에 맞게 조정하세요.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## 2단계: PDF 내보내기 옵션 구성 (페이지 크기 포함)

여기서 페이지 너비와 높이를 설정합니다—바로 **PDF 페이지 크기 설정** 단계입니다. 값은 픽셀 단위이며, 필요에 따라 인치 또는 밀리미터에서 변환할 수 있습니다.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // <-- custom width
cadRasterizationOptions.setPageHeight(600);  // <-- custom height
```

> **팁:** 표준 용지 크기를 사용하려면 `1 inch = 72 points` 변환을 이용하세요. A4 용지(8.27 × 11.69 in)의 경우 `pageWidth = 595`, `pageHeight = 842` 로 설정합니다.

## 3단계: 추적 구현

추적은 렌더링 문제를 캡처합니다. 내보내기 후 호출되는 사용자 정의 핸들러를 연결합니다.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## 4단계: PDF로 내보내기

이제 변환을 수행합니다. 지정한 차원의 PDF가 생성되고, 추적 정보가 콘솔에 출력됩니다.

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## 5단계: CadRenderHandler 클래스

핸들러는 렌더링 중 발생한 실패를 출력합니다. 이는 **CAD 도면 PDF 내보내기** 시 문제를 디버깅하는 데 도움이 됩니다.

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

## 일반적인 문제와 해결책

| 문제 | 원인 | 해결 방법 |
|------|------|-----------|
| **빈 PDF** | 페이지 크기가 0이거나 너무 작음 | `setPageWidth`와 `setPageHeight`가 양수인지 확인 |
| **지오메트리 누락** | 핸들러가 캡처한 렌더링 오류 | `ErrorHandler`의 콘솔 출력을 검토하고 해당 `RenderCode`를 해결 |
| **파일을 찾을 수 없음** | `dataDir` 경로 오류 | 절대 경로를 사용하거나 디렉터리 존재 여부 확인 |
| **라이선스 예외** | 대용량 파일에 대해 트라이얼만 사용 | 이미지 로드 전에 Aspose.CAD 라이선스를 적용 |

## 자주 묻는 질문

**Q: Aspose.CAD for Java를 사용해 다른 CAD 파일 형식에서도 추적을 활성화할 수 있나요?**  
A: Aspose.CAD는 주로 DWG/DXF에 대한 추적을 지원합니다. 다른 형식에 대해서는 공식 문서를 참고하세요.

**Q: Aspose.CAD for에서 추가 내보내기 옵션을 어떻게 처리하나요?**  
A: DPI, 배경색, 벡터 래스터화 등 다양한 옵션을 제공합니다. 자세한 내용은 [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/)을 확인하세요.

**Q: Aspose.CAD for Java의 트라이얼 버전을 제공하나요?**  
A: 예, [Aspose.CAD Free Trial](https://releases.aspose.com/)에서 무료 트라이얼을 다운로드할 수 있습니다.

**Q: Aspose.CAD for Java와 관련된 지원이나 토론을 어디서 받을 수 있나요?**  
A: 커뮤니티 지원 및 공식 답변은 [Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)에서 확인하세요.

**Q: Aspose.CAD for Java용 임시 라이선스를 어떻게 얻나요?**  
A: [Temporary License](https://purchase.aspose.com/temporary-license/) 페이지에 안내된 절차를 따르세요.

---

**마지막 업데이트:** 2025-12-03  
**테스트 환경:** Aspose.CAD for Java 24.11 (작성 시 최신 버전)  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}