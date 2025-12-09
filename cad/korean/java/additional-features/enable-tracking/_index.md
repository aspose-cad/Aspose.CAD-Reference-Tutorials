---
date: 2025-12-09
description: dwg 추적 Java를 활성화하는 방법과 Aspose.CAD를 사용하여 dxf를 pdf로 Java 변환하는 방법을 배워보세요.
  이 단계별 가이드는 협업 CAD 프로젝트를 위한 전체 워크플로우를 보여줍니다.
linktitle: Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: Java에서 Aspose.CAD를 사용하여 DWG 파일에 추적 활성화
url: /ko/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java에서 Aspose.CAD를 사용해 DWG 파일 추적 활성화

## 소개

현대 CAD 워크플로에서 **enable dwg tracking java** 를 활성화하는 것은 변경 사항을 모니터링하고, 오류를 조기에 포착하며, 모든 이해관계자가 동일한 정보를 공유하도록 하는 데 필수적입니다. 이 튜토리얼에서는 Aspose.CAD for Java를 사용해 DWG 파일에 추적을 켜는 정확한 단계를 안내하고, 그 과정에서 **java convert dxf pdf** 를 수행하는 방법도 보여줍니다. 최종적으로 변환뿐 아니라 렌더링 문제를 보고하는 실행 가능한 코드 스니펫을 얻게 됩니다.

## 빠른 답변
- **“enable dwg tracking java”는 무엇을 하나요?** Aspose.CAD의 오류 처리 콜백을 활성화하여 내보내기 중 렌더링 문제를 확인할 수 있게 합니다.  
- **라이선스가 필요합니까?** 테스트용 트라이얼은 사용 가능하지만, 실제 운영 환경에서는 상용 라이선스가 필요합니다.  
- **DXF를 PDF로 변환할 수도 있나요?** 네 – DWG에 사용한 `PdfOptions`가 DXF에도 적용되어 *java convert dxf pdf* 시나리오를 충족합니다.  
- **필요한 JDK 버전은?** Java 8 이상.  
- **추가 예제는 어디서 찾을 수 있나요?** 아래 링크된 Aspose.CAD Java 문서를 확인하세요.

## enable dwg tracking java란?
Java 애플리케이션에서 DWG 추적을 활성화한다는 것은 CAD 파일이 래스터화되거나 내보내지는 동안 경고, 오류 및 기타 진단 정보를 캡처하는 커스텀 렌더 핸들러를 연결하는 것을 의미합니다. 이러한 가시성은 변환 파이프라인을 디버깅하고 고품질 결과물을 보장하는 데 도움이 됩니다.

## 왜 Aspose.CAD for Java를 사용하나요?
- **전체 기능 CAD 지원** – DWG, DXF, DGN 등 다양한 포맷 지원.  
- **외부 종속성 없음** – 순수 Java 라이브러리로 서버‑사이드 자동화에 최적.  
- **내장 추적** – `CadRenderHandler`를 통한 상세 렌더 결과 제공.  
- **간편 PDF 내보내기** – 벡터 데이터를 보존하면서 한 줄 코드로 변환.

## 사전 요구 사항

구현에 앞서 다음 항목이 준비되어 있는지 확인하세요:

- Java Development Kit (JDK): 시스템에 Java가 설치되어 있어야 합니다.  
- Aspose.CAD for Java: [download link](https://releases.aspose.com/cad/java/)에서 다운로드 및 설치합니다.  
- 문서 디렉터리: DWG 파일이 저장된 폴더를 준비합니다.

## 네임스페이스 가져오기

Java 프로젝트에서 Aspose.CAD 기능을 사용하려면 필요한 네임스페이스를 가져와야 합니다:

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

## 1단계: DWG 파일 로드

DWG(또는 DXF) 파일을 Java 애플리케이션에 로드합니다. 파일 경로는 상황에 맞게 조정하세요:

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## 2단계: PDF 내보내기 옵션 설정

CAD용 벡터 래스터화 옵션을 지정하면서 PDF 내보내기 옵션을 설정합니다. 여기서 *java convert dxf pdf* 기능도 확인할 수 있습니다:

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## 3단계: 추적 구현

커스텀 오류 핸들러 클래스를 사용해 추적을 구현합니다. 이 클래스는 렌더링 문제를 캡처하고 콘솔에 출력합니다:

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## 4단계: PDF로 내보내기

추적이 활성화된 상태에서 DWG/DXF 파일을 PDF로 변환하는 내보내기 프로세스를 시작합니다:

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## 5단계: CadRenderHandler 클래스

렌더링 결과를 처리하고 추적 정보를 출력하도록 `ErrorHandler` 클래스를(`CadRenderHandler` 상속) 정의합니다:

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

- **`RenderResult`에서 `NullPointerException`** – Aspose.CAD 23.10 이상 버전을 사용하세요; 이전 버전에는 `RenderResult` API가 없습니다.  
- **파일을 찾을 수 없음** – `dataDir`가 올바른 폴더를 가리키는지, 파일 이름이 대소문자까지 정확히 일치하는지 확인합니다.  
- **추적 출력이 없음** – 커스텀 `ErrorHandler`가 `cadRasterizationOptions.RenderResult`에 올바르게 할당되었는지 검증합니다.

## 자주 묻는 질문

**Q:** Aspose.CAD for Java를 사용해 다른 CAD 포맷에서도 추적을 활성화할 수 있나요?  
**A:** Aspose.CAD는 주로 DWG 추적을 지원합니다. 다른 포맷에 대한 내용은 공식 문서를 참고하세요.

**Q:** Aspose.CAD for Java에서 추가 내보내기 옵션을 어떻게 다루나요?  
**A:** 자세한 내용은 [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/)을 확인하세요.

**Q:** Aspose.CAD for Java의 체험판이 있나요?  
**A:** 네, [Aspose.CAD Free Trial](https://releases.aspose.com/)에서 체험판을 다운로드할 수 있습니다.

**Q:** Aspose.CAD for Java와 관련된 지원이나 토론은 어디서 받을 수 있나요?  
**A:** 커뮤니티 지원은 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)에서 이용할 수 있습니다.

**Q:** Aspose.CAD for Java용 임시 라이선스는 어떻게 얻나요?  
**A:** [Temporary License](https://purchase.aspose.com/temporary-license/) 페이지의 절차를 따르세요.

## 결론

Aspose.CAD와 Java를 활용해 DWG 추적을 활성화하면 변환 문제에 대한 가시성을 확보할 뿐 아니라 협업 디자인 워크플로를 효율화할 수 있습니다. 위 단계들을 따라 **enable dwg tracking java** 를 구현하고, DXF를 PDF로 변환하며, 렌더링 이슈를 우아하게 처리하세요.

---

**마지막 업데이트:** 2025-12-09  
**테스트 환경:** Aspose.CAD for Java 24.12  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}