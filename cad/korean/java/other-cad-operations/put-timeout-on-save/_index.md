---
title: Aspose.CAD를 사용한 CAD 저장 시 시간 초과
linktitle: 저장 시 시간 초과 설정
second_title: Aspose.CAD 자바 API
description: Aspose.CAD를 사용하여 Java 애플리케이션의 성능을 향상시키는 방법을 알아보세요. CAD 도면 저장 시 시간 초과를 설정합니다. 단계별 가이드를 따르세요.
weight: 15
url: /ko/java/other-cad-operations/put-timeout-on-save/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD를 사용한 CAD 저장 시 시간 초과

## 소개

Aspose.CAD for Java를 사용하여 저장 시 시간 초과를 설정하는 방법에 대한 튜토리얼에 오신 것을 환영합니다. 이 가이드에서는 애플리케이션 성능을 향상시키기 위해 CAD 도면 저장 시간 제한을 설정하는 과정을 안내합니다. Aspose.CAD for Java는 Java 애플리케이션에서 CAD 파일을 원활하게 사용할 수 있게 해주는 강력한 라이브러리입니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.
-  Java 라이브러리용 Aspose.CAD: 프로젝트에 Java 라이브러리용 Aspose.CAD가 통합되어 있는지 확인하세요. 라이브러리는 다음에서 다운로드할 수 있습니다.[웹사이트](https://releases.aspose.com/cad/java/).
- 개발 환경: 필요한 모든 도구와 종속성을 사용하여 Java 개발 환경을 설정합니다.

## 패키지 가져오기

시작하려면 필요한 패키지를 Java 프로젝트로 가져옵니다. Java 파일 시작 부분에 다음 줄을 추가합니다.

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

이제 예제 코드를 단계별 지침으로 나누어 보겠습니다.

## 1단계: 소스 및 출력 디렉터리 설정

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

CAD 도면에 대한 올바른 소스 및 출력 디렉토리가 있는지 확인하십시오.

## 2단계: 중단 토큰 소스 생성

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

저장 작업 중 중단을 관리하려면 중단 토큰 소스를 초기화합니다.

## 3단계: CAD 도면 로드

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

 CAD 도면을`CadImage` 물체.

## 4단계: 래스터화 옵션 구성

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

CAD 도면에 대한 래스터화 옵션을 구성합니다.

## 5단계: PDF 옵션 구성

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

벡터 래스터화 옵션과 중단 토큰을 사용하여 PDF 옵션을 설정하세요.

## 6단계: 시간 초과로 도면 저장

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

지정된 시간 제한을 사용하여 CAD 도면을 PDF 파일로 저장합니다.

## 7단계: 중단 처리

```java
java.lang.Thread thread = new java.lang.Thread(new Runnable() {
    @Override
    public void run() {
        try {
            cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
        } catch (Throwable th) {
            System.out.println("interrupted !!!");
        }
    }
});
thread.start();
TimeUnit.SECONDS.sleep(3);
source.interrupt();
thread.join();
```

저장 작업을 처리하고 지정된 시간 초과 후 중단하는 스레드를 만듭니다.

## 결론

축하해요! Aspose.CAD for Java를 사용하여 저장 시 시간 초과를 설정하는 방법을 성공적으로 배웠습니다. 이 기능은 CAD 관련 응용 프로그램의 효율성을 크게 향상시킬 수 있습니다.

## FAQ

### Q1: Java용 Aspose.CAD를 어떻게 다운로드할 수 있나요?

 A1: 다음에서 다운로드할 수 있습니다.[릴리스 페이지](https://releases.aspose.com/cad/java/).

### Q2: Aspose.CAD for Java 설명서는 어디서 찾을 수 있나요?

 A2: 다음을 참조하세요.[선적 서류 비치](https://reference.aspose.com/cad/java/) 포괄적인 정보를 얻으려면.

### Q3: 무료 평가판이 제공됩니까?

A3: 예, 다음에서 무료 평가판을 받을 수 있습니다.[이 링크](https://releases.aspose.com/).

### Q4: 임시 라이센스는 어떻게 얻나요?

 A4: 방문[여기](https://purchase.aspose.com/temporary-license/) 임시 라이선스 세부정보를 확인하세요.

### Q5: 도움이 필요하거나 질문이 있나요?

 A5: 다음으로 가세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 지역 사회 지원을 위해.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
