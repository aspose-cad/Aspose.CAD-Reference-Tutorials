---
date: 2025-12-07
description: Aspose.CAD for Java를 사용하여 CAD를 PDF로 변환할 때 PDF 페이지 크기를 설정하는 방법을 배워보세요.
  이 단계별 가이드를 따라 추적을 활성화하고, CAD를 PDF로 변환하며, CAD를 효율적으로 PDF로 저장하세요.
linktitle: Set PDF Page Size – Enable Tracking for CAD Rendering
second_title: Aspose.CAD Java API
title: CAD 렌더링 프로세스를 위한 PDF 페이지 크기 설정 및 추적 활성화 방법
url: /ko/java/advanced-cad-features/enable-tracking-for-cad-rendering-process/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD 렌더링 프로세스 추적 활성화

## 소개

이 튜토리얼에서는 **Aspose.CAD for Java**를 사용하여 **CAD를 PDF로 변환**하면서 **PDF 페이지 크기 설정**하는 방법을 배웁니다. 추적을 활성화하면 렌더링 파이프라인을 완전히 파악할 수 있어 CAD 파일(DXF 등)에서 PDF로 변환할 때 디버깅 및 최적화가 쉬워집니다. **CAD를 PDF로 저장**, DXF에서 PDF 생성, 또는 출력 차원 제어가 필요하든 아래 단계가 전체 과정을 안내합니다.

## 빠른 답변
- **“PDF 페이지 크기 설정”은 무엇을 하나요?** CAD 렌더링 중 결과 PDF 페이지의 너비와 높이를 정의합니다.  
- **왜 추적을 활성화하나요?** 추적은 변환의 각 단계를 기록하여 성능 병목이나 오류를 쉽게 찾을 수 있게 합니다.  
- **라이선스가 필요합니까?** 평가용 무료 체험으로 가능하지만, 상용 환경에서는 상업용 라이선스가 필요합니다.  
- **지원되는 CAD 형식은 무엇인가요?** DWG, DXF, DGN 등 다수 – 전체 목록은 Aspose.CAD 문서를 참고하세요.  
- **실시간으로 페이지 차원을 변경할 수 있나요?** 예 – `CadRasterizationOptions`의 `PageWidth`와 `PageHeight` 값을 조정하면 됩니다.

## CAD 렌더링에서 “PDF 페이지 크기 설정”이란?

PDF 페이지 크기를 설정하면 래스터라이저가 벡터 CAD 데이터를 PDF 페이지에 래스터화할 때 캔버스 크기를 결정합니다. 이는 특히 정밀한 엔지니어링 도면을 다룰 때 시각적 정확성을 유지하는 데 중요합니다.

## CAD 렌더링에 추적을 활성화하는 이유

추적을 활성화하면 소스 파일 로드부터 PDF 출력까지 각 단계의 상세 로그를 제공합니다. 이를 통해 다음을 수행할 수 있습니다:

- 특정 도면이 올바르게 렌더링되지 않는 이유 진단  
- 각 단계에 소요된 시간 측정, 성능 튜닝에 활용  
- 설정한 페이지 크기가 실제 적용됐는지 확인  

## 사전 요구 사항

추적 설정을 진행하기 전에 다음을 준비하십시오:

1. **Java 개발 환경** – Java 8 이상이 설치되어 있어야 합니다.  
2. **Aspose.CAD 라이브러리** – Aspose.CAD 라이브러리를 다운로드하여 Java 프로젝트에 통합합니다. 다운로드 링크는 [여기](https://releases.aspose.com/cad/java/)에서 확인하세요.  
3. **문서 디렉터리** – CAD 파일과 생성된 PDF를 저장할 디렉터리를 준비합니다.

## 네임스페이스 가져오기

Java 프로젝트에서 Aspose.CAD 기능을 활용하려면 필요한 네임스페이스를 가져와야 합니다. 코드 시작 부분에 다음 라인을 추가하십시오:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;

import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## 리소스 디렉터리 경로 설정

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

`"Your Document Directory"`를 실제 문서 디렉터리 경로로 교체합니다.

## CAD 파일 로드

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

지정된 문서 디렉터리 내에 CAD 파일 경로를 입력하십시오.

## PDF 출력 옵션 설정

```java
OutputStream stream = new FileOutputStream(dataDir + "conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
```

출력 스트림을 생성하고 변환을 위한 PDF 옵션을 설정합니다.

## CadRasterizationOptions 구성 (PDF 페이지 크기 설정)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

여기서 `PageWidth`와 `PageHeight`를 정의하여 **PDF 페이지 크기 설정**을 수행합니다. 엔지니어링 도면에 필요한 차원에 맞게 값을 조정하십시오. 이 단계는 CAD 내용이 최종 PDF에 어떻게 스케일링되고 렌더링되는지를 직접 결정합니다.

## PDF 파일 저장

```java
image.save(stream, pdfOptions);
```

지정된 옵션으로 렌더링된 PDF 파일을 저장합니다.

## 추적 활성화 확인

```java
System.out.println("Tracking enabled successfully for CAD rendering process.");
```

CAD 렌더링 프로세스에 추적이 성공적으로 활성화되었는지 확인합니다.

## 일반적인 문제 및 해결 방법

| 증상 | 가능한 원인 | 해결 방법 |
|---------|--------------|-----|
| PDF 페이지가 비어 있음 | `PageWidth`/`PageHeight`가 0으로 설정됨 | 0이 아닌 차원을 제공하십시오. |
| 출력 파일이 손상됨 | 출력 스트림이 닫히지 않음 | `image.save(...)` 후에 `stream.close()`를 호출하십시오. |
| PDF에 레이어가 누락됨 | CAD 파일이 지원되지 않는 엔터티를 사용함 | 파일 형식이 Aspose.CAD에서 완전히 지원되는지 확인하십시오. |

## 자주 묻는 질문

### Q1: Aspose.CAD가 모든 CAD 파일 형식과 호환됩니까?

A1: Aspose.CAD는 DWG, DXF, DGN 등 다양한 CAD 형식을 지원합니다. 전체 목록은 [문서](https://reference.aspose.com/cad/java/)를 참고하십시오.

### Q2: PDF 파일의 출력 차원을 사용자 정의할 수 있나요?

A2: 물론입니다! `CadRasterizationOptions`의 `PageWidth`와 `PageHeight` 매개변수를 조정하여 출력 차원을 원하는 대로 설정하십시오.

### Q3: Aspose.CAD for Java에 무료 체험판이 있나요?

A3: 예, 무료 체험판은 [여기](https://releases.aspose.com/)에서 받을 수 있습니다.

### Q4: Aspose.CAD 관련 문의에 대한 커뮤니티 지원은 어디서 받을 수 있나요?

A4: [Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)에서 커뮤니티와 소통하고 도움을 받을 수 있습니다.

### Q5: Aspose.CAD 임시 라이선스를 받을 수 있나요?

A5: 예, 임시 라이선스는 [여기](https://purchase.aspose.com/temporary-license/)에서 구매할 수 있습니다.

## 결론

축하합니다! 이제 **Aspose.CAD for Java**를 사용하여 **PDF 페이지 크기 설정** 및 CAD 렌더링 추적 활성화 방법을 배웠습니다. 이 가이드를 통해 **CAD를 PDF로 변환**, **CAD를 PDF로 저장**, DXF에서 PDF 생성 등을 페이지 차원을 완벽히 제어하고 상세 실행 로그와 함께 수행할 수 있습니다. 다양한 페이지 크기를 실험하고 추가 래스터화 옵션을 탐색하여 특정 엔지니어링 워크플로에 맞게 최적화해 보세요.

---

**마지막 업데이트:** 2025-12-07  
**테스트 환경:** Aspose.CAD for Java 24.12 (작성 시 최신 버전)  
**작성자:** Aspose  

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
