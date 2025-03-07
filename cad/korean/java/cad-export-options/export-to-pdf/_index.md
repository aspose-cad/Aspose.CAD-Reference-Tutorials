---
title: Java용 Aspose.CAD를 사용하여 PDF로 내보내기
linktitle: PDF로 내보내기
second_title: Aspose.CAD 자바 API
description: Aspose.CAD for Java를 사용하여 CAD 파일을 PDF로 쉽게 내보내는 방법을 알아보세요. 원활한 통합을 위한 단계별 가이드를 따르세요.
weight: 13
url: /ko/java/cad-export-options/export-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java용 Aspose.CAD를 사용하여 PDF로 내보내기

## 소개

Aspose.CAD for Java를 사용하여 CAD 파일을 PDF로 내보내는 방법에 대한 포괄적인 튜토리얼에 오신 것을 환영합니다. CAD 도면을 널리 지원되는 PDF 형식으로 원활하게 변환하려는 경우 올바른 위치에 있습니다. 이 단계별 가이드에서는 성공적인 PDF 내보내기를 위한 각 단계를 이해할 수 있도록 프로세스를 세분화합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

-  Java용 Aspose.CAD: Java 환경에 Aspose.CAD 라이브러리가 설치되어 있는지 확인하세요. 당신은 그것을 다운로드 할 수 있습니다[여기](https://releases.aspose.com/cad/java/).

- 리소스 디렉터리: CAD 파일이 저장되는 디렉터리를 설정합니다. 제공된 코드 조각의 "문서 디렉터리"를 실제 경로로 바꾸세요.

이제 주요 단계로 넘어가겠습니다.

## 네임스페이스 가져오기

Java 프로젝트에서 Aspose.CAD 기능을 사용하려면 필요한 네임스페이스를 가져오는 것부터 시작하세요.

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

## 1단계: CAD 파일 로드

CAD 파일을 Aspose.CAD Image 개체에 로드합니다. "site.dwf"를 실제 CAD 파일 이름으로 바꾸십시오.

```java
String fileName = (dataDir + "site.dwf");
Image image = Image.load(fileName);
```

## 2단계: PDF 옵션 구성

페이지 높이, 너비, 레이아웃과 같은 벡터 래스터화 옵션을 포함한 PDF 내보내기 옵션을 설정합니다.

```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);

rasterizationOptions.setPageHeight(500);
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setLayouts(new String[] { "Model" });
```

## 3단계: PDF로 내보내기

생성된 PDF 파일의 출력 경로를 지정하고 구성된 PDF 옵션으로 이미지를 저장합니다.

```java
String outPath = dataDir + "site.pdf";
image.save(outPath, pdfOptions);
```

축하해요! Aspose.CAD for Java를 사용하여 CAD 파일을 PDF로 성공적으로 내보냈습니다.

## 결론

이 튜토리얼에서는 Aspose.CAD for Java를 사용하여 CAD 파일을 PDF로 내보내는 단계별 프로세스를 살펴보았습니다. 이러한 간단하면서도 효과적인 단계를 따르면 이 기능을 Java 애플리케이션에 원활하게 통합할 수 있습니다.

## FAQ

### Q1: Aspose.CAD는 모든 CAD 파일 형식과 호환됩니까?

A1: 예, Aspose.CAD는 다양한 CAD 형식을 지원하여 다양한 설계 소프트웨어와의 호환성을 보장합니다.

### Q2: PDF 출력 설정을 사용자 정의할 수 있습니까?

A2: 물론이죠. 튜토리얼에서는 사용자 정의 옵션을 간략하게 설명하지만 필요에 따라 출력을 맞춤화하기 위해 더 자세히 탐색할 수 있습니다.

### Q3: Aspose.CAD에 대한 추가 지원은 어디서 찾을 수 있나요?

 A3: 질문이나 문제가 있는 경우[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 지역사회의 도움을 구합니다.

### Q4: 무료 평가판이 제공됩니까?

 A4: 예, Aspose.CAD 무료 평가판에 액세스할 수 있습니다.[여기](https://releases.aspose.com/).

### Q5: Aspose.CAD의 임시 라이선스는 어떻게 얻을 수 있나요?

 A5: 임시 라이선스를 받으려면 다음을 방문하세요.[이 링크](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
