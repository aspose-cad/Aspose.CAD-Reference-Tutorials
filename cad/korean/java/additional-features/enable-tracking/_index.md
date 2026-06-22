---
date: 2026-02-10
description: Aspose.CAD for Java를 사용하여 DWG 파일에서 추적을 활성화하는 방법과 사용자 정의 오류 처리기를 사용해 DXF를
  PDF로 변환하는 단계별 가이드.
linktitle: Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: Java에서 Aspose.CAD를 사용하여 DWG 파일에서 추적 기능 활성화하는 방법
url: /ko/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java에서 Aspose.CAD를 사용하여 DWG 파일에서 추적을 활성화하는 방법

## Introduction

협업 CAD 프로젝트를 진행하고 있다면 **추적을 활성화하는 방법**을 아는 것이 큰 변화를 가져옵니다. 실시간으로 렌더링 문제를 파악하고, 변환 오류를 조기에 포착하며, 모든 이해관계자에게 정보를 제공할 수 있습니다. 이 튜토리얼에서는 Aspose.CAD for Java를 사용하여 추적을 활성화하는 정확한 단계들을 안내하고, 동일한 파이프라인의 일부로 **DXF를 PDF로 변환하는 방법**도 시연합니다. 마지막까지 진행하면 도면을 내보내는 동안 **custom error handler Java** 클래스를 통해 오류를 보고하는 완전한 프로덕션 준비 코드 스니펫을 얻을 수 있습니다.

## Quick Answers
- **“enable dwg tracking java”가 무엇을 하나요?** Aspose.CAD의 오류 처리 콜백을 활성화하여 내보내기 중에 렌더링 문제를 확인할 수 있습니다.  
- **라이선스가 필요합니까?** 테스트용으로는 체험판을 사용할 수 있지만, 프로덕션에서는 상용 라이선스가 필요합니다.  
- **DXF를 PDF로 변환할 수도 있나요?** 네 – DWG에 사용한 동일한 `PdfOptions`가 DXF에도 적용되어 *java convert dxf pdf* 시나리오를 충족합니다.  
- **필요한 JDK 버전은?** Java 8 이상.  
- **추가 예제를 어디서 찾을 수 있나요?** 아래 링크된 Aspose.CAD Java Documentation을 확인하세요.

## Aspose.CAD를 사용하여 DWG 파일에서 추적을 활성화하는 방법

Java 애플리케이션에서 DWG 추적을 활성화한다는 것은 CAD 파일이 래스터화되거나 내보내지는 동안 경고, 오류 및 기타 진단 정보를 캡처하는 커스텀 렌더 핸들러를 연결하는 것을 의미합니다. 이러한 가시성은 개발자가 변환 파이프라인을 디버깅하는 데 도움을 주며, 더 높은 품질의 결과물을 보장합니다.

## 왜 Java용 Aspose.CAD를 사용해야 할까요?

- **전체 기능 CAD 지원** – DWG, DXF, DGN 등.  
- **외부 종속성 없음** – 순수 Java 라이브러리로 서버 측 자동화에 이상적입니다.  
- **내장 추적** – `CadRenderHandler`를 통해 상세한 렌더 결과를 제공합니다.  
- **간편 PDF 내보내기** – 벡터 데이터를 유지하면서 한 줄로 변환합니다.  

## Prerequisites

구현에 들어가기 전에 다음 전제 조건이 준비되어 있는지 확인하세요:

- Java Development Kit (JDK): 시스템에 Java가 설치되어 있는지 확인하세요.  
- Aspose.CAD for Java: [다운로드 링크](https://releases.aspose.com/cad/java/)에서 Aspose.CAD for Java를 다운로드하고 설치하세요.  
- Document Directory: DWG 파일이 위치한 디렉터리를 준비하세요.

## Import Namespaces

Java 프로젝트에서 Aspose.CAD 기능을 활용하기 위해 필요한 네임스페이스를 가져오는 것으로 시작하세요:

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

## Step 1: Load the DWG File

먼저 DWG(또는 DXF) 파일을 Java 애플리케이션에 로드합니다. 파일 경로를 적절히 조정하세요:

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Step 2: Configure PDF Export Options (How to Convert DXF to PDF)

CAD용 벡터 래스터화 옵션을 지정하여 PDF 내보내기 옵션을 설정합니다. 이는 *java convert dxf pdf* 기능을 시연하는 예시이기도 합니다:

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## Step 3: Implement Tracking (Custom Error Handler Java)

커스텀 오류 처리 클래스를 사용해 추적을 구현합니다. 이 클래스는 렌더링 문제를 캡처하여 콘솔에 표시합니다:

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Step 4: Export to PDF

추적이 활성화된 상태에서 DWG/DXF 파일을 PDF로 변환하는 내보내기 프로세스를 시작합니다:

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Step 5: CadRenderHandler Class

`ErrorHandler` 클래스(`CadRenderHandler`를 상속)를 정의하여 렌더링 결과를 처리하고 추적 정보를 출력합니다:

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

## 왜 이것이 중요한가

추적을 활성화하면 모든 변환 단계에 대한 명확한 감사 로그를 확보할 수 있습니다. 이는 정확한 렌더링 증명이 규정 준수 감사를 위해 필요한 건축, 엔지니어링, 건설 등 규제 산업에서 특히 유용합니다. 커스텀 오류 처리기는 문제를 모니터링 시스템에 기록하거나 자동 재시도를 트리거하는 훅도 제공합니다.

## Common Issues and Solutions

- **`RenderResult`에서 `NullPointerException`** – Aspose.CAD 버전 23.10 이상을 사용하고 있는지 확인하세요; 이전 릴리스에는 `RenderResult` API가 없습니다.  
- **파일을 찾을 수 없음** – `dataDir`이 올바른 폴더를 가리키는지, 파일 이름이 대소문자를 포함해 정확히 일치하는지 확인하세요.  
- **추적 출력 누락** – 커스텀 `ErrorHandler`가 `cadRasterizationOptions.RenderResult`에 올바르게 할당되었는지 확인하세요.

## Frequently Asked Questions

**Q:** Aspose.CAD for Java를 사용해 다른 CAD 파일 형식에서도 추적을 활성화할 수 있나요?  
A: Aspose.CAD는 주로 DWG 추적을 지원합니다. 다른 형식에 대해서는 공식 문서를 참고하세요.

**Q:** Aspose.CAD for Java에서 추가 내보내기 옵션을 어떻게 처리할 수 있나요?  
A: [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/)에서 자세한 내용을 확인하세요.

**Q:** Aspose.CAD for Java용 체험판이 있나요?  
A: 네, [Aspose.CAD Free Trial](https://releases.aspose.com/)에서 체험판을 이용할 수 있습니다.

**Q:** Aspose.CAD for Java와 관련된 지원을 받거나 문제를 논의하려면 어디로 가면 되나요?  
A: 커뮤니티 지원을 위해 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)을 방문하세요.

**Q:** Aspose.CAD for Java용 임시 라이선스를 어떻게 얻을 수 있나요?  
A: [Temporary License](https://purchase.aspose.com/temporary-license/)에 안내된 절차를 따르세요.

## 결론

Java에서 Aspose.CAD를 사용해 DWG 추적을 활성화하면 변환 문제에 대한 가시성을 제공할 뿐 아니라 협업 디자인 워크플로를 효율화합니다. 위 단계들을 따르면 **추적을 활성화하는 방법**을 익히고, DXF를 PDF로 변환하며, 렌더링 문제를 원활하게 처리할 수 있습니다.

---

**마지막 업데이트:** 2026-02-10  
**테스트 환경:** Aspose.CAD for Java 24.12  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}