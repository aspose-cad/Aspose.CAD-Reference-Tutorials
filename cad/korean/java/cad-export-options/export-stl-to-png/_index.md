---
title: Java용 Aspose.CAD를 사용하여 STL을 PNG로 내보내기
linktitle: STL을 PNG로 내보내기
second_title: Aspose.CAD 자바 API
description: Aspose.CAD를 사용하여 Java에서 STL 파일을 PNG로 내보내는 원활한 프로세스를 살펴보세요. 작업 흐름을 단순화하고 Java 프로젝트를 손쉽게 향상하세요.
weight: 20
url: /ko/java/cad-export-options/export-stl-to-png/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java용 Aspose.CAD를 사용하여 STL을 PNG로 내보내기

## 소개

Java를 사용하여 STL 파일을 PNG로 내보내려고 하시나요? Aspose.CAD for Java가 여러분에게 필요한 솔루션입니다! 이 튜토리얼에서는 프로세스를 단계별로 안내합니다. 숙련된 SEO 작가로서 저는 콘텐츠가 유익할 뿐만 아니라 검색 엔진에 최적화되도록 하겠습니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

- 컴퓨터에 JDK(Java Development Kit)가 설치되어 있습니다.
-  Java 라이브러리용 Aspose.CAD를 다운로드했습니다. 당신은 그것을 얻을 수 있습니다[여기](https://releases.aspose.com/cad/java/).
-  유효한 면허증 또는 임시 면허증[여기](https://purchase.aspose.com/temporary-license/).

## 네임스페이스 가져오기

Java 프로젝트에서 필요한 네임스페이스를 가져옵니다.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

이제 예제를 여러 단계로 나누어 보겠습니다.

## 1단계: 프로젝트 설정

새 Java 프로젝트를 생성하고 Java용 Aspose.CAD 라이브러리를 프로젝트 종속성에 추가합니다.

## 2단계: STL 파일 지정

STL 파일의 경로를 정의합니다. 예를 들어:

```java
String dataDir = "Your Document Directory" + "ExportingSTL/";
String fileName = dataDir + "example.stl";
```

## 3단계: STL 파일 로드

 다음을 사용하여 STL 파일을 로드합니다.`Image.load` 방법:

```java
CadImage cadImage = (CadImage)Image.load(fileName);
```

## 4단계: 래스터화 옵션 구성

벡터화를 위한 래스터화 옵션을 설정합니다.

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

## 5단계: PNG 옵션 구성

PNG 내보내기 옵션을 지정합니다.

```java
PngOptions pngOptions = new PngOptions();
// 벡터 래스터화 옵션을 설정하려면 아래 줄의 주석 처리를 제거하세요.
// pngOptions.setVectorRasterizationOptions(벡터옵션);
```

## 6단계: PNG로 저장

CAD 이미지를 PNG 파일로 저장합니다.

```java
String outPath = dataDir + "galeon.stl.png";
cadImage.save(outPath, pngOptions);
```

축하해요! Aspose.CAD for Java를 사용하여 STL 파일을 PNG로 성공적으로 내보냈습니다.

## 결론

이 튜토리얼에서는 Java용 Aspose.CAD를 활용하여 STL 파일을 PNG로 쉽게 내보내는 방법을 살펴보았습니다. 이 강력한 라이브러리는 복잡한 작업을 단순화하여 Java 프로젝트에 귀중한 자산이 됩니다.

## FAQ

### Q1: Aspose.CAD for Java는 모든 STL 파일 버전과 호환됩니까?

A1: Aspose.CAD for Java는 다양한 STL 파일 버전을 지원하여 가장 일반적인 형식과의 호환성을 보장합니다.

### Q2: 상용 프로젝트에서 Aspose.CAD for Java를 사용할 수 있나요?

 A2: 네, 가능합니다. 간단히 유효한 라이센스를 얻으십시오.[여기](https://purchase.aspose.com/buy).

### Q3: 무료 평가판을 사용하려면 임시 라이선스가 필요합니까?

 A3: 아니요. 무료 평가판에는 임시 라이선스가 필요하지 않습니다. 평가판 버전으로 바로 시작할 수 있습니다[여기](https://releases.aspose.com/).

### Q4: 추가 지원을 찾거나 질문을 할 수 있는 곳은 어디입니까?

 A4: Aspose.CAD 포럼을 방문하세요.[여기](https://forum.aspose.com/c/cad/19) 어떤 지원이나 문의 사항이 있으면.

### Q5: 사용 가능한 포괄적인 문서가 있습니까?

 A5: 예, 문서를 찾을 수 있습니다.[여기](https://reference.aspose.com/cad/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
