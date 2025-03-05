---
title: Java용 Aspose.CAD를 사용하여 CAD 레이어를 래스터 이미지 형식으로 변환
linktitle: CAD 레이어를 래스터 이미지 형식으로 변환
second_title: Aspose.CAD 자바 API
description: Aspose.CAD for Java를 사용하여 CAD 레이어를 래스터 이미지로 쉽게 변환하는 방법을 알아보세요. 원활한 문서 시각화를 위한 단계별 가이드를 따르세요.
type: docs
weight: 11
url: /ko/java/cad-drawing-conversion/convert-cad-layer-to-raster-image/
---
## 소개

CAD(Computer-Aided Design) 영역에서 CAD 레이어를 래스터 이미지 형식으로 원활하게 변환하는 기능은 문서 조작 및 시각화의 중요한 측면입니다. Aspose.CAD for Java는 이러한 변환 프로세스를 간소화하기 위한 수많은 기능을 제공하는 강력한 도구로 등장합니다. 이 단계별 가이드는 프로세스를 안내하여 Aspose.CAD for Java의 잠재력을 최대한 활용하도록 보장합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

- Java 개발 환경: 컴퓨터에 Java 개발 환경이 설정되어 있는지 확인하십시오.

-  Aspose.CAD 라이브러리: 다음에서 Java용 Aspose.CAD 라이브러리를 다운로드하고 설치합니다.[다운로드 링크](https://releases.aspose.com/cad/java/).

## 네임스페이스 가져오기

이 단계에서는 프로세스를 시작하는 데 필요한 네임스페이스를 가져옵니다.

### Aspose.CAD 클래스 가져오기

Java 코드에서 다음 가져오기 문을 사용하여 Aspose.CAD 클래스를 포함합니다.

```java
import com.aspose.cad.Image;


import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## CAD 레이어를 래스터 이미지 형식으로 변환

이제 원활한 변환 프로세스를 보장하기 위해 튜토리얼을 여러 단계로 나누어 보겠습니다.

### 1단계: CAD 파일 설정

먼저 CAD 파일의 경로를 지정하고 이를 Image 클래스의 인스턴스에 로드합니다.

```java
// 리소스 디렉터리의 경로입니다.
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### 2단계: 래스터화 옵션 구성

래스터화 설정을 정의하려면 CadRasterizationOptions 인스턴스를 만듭니다.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
```

### 3단계: CAD 레이어 지정

래스터화 옵션에 원하는 CAD 레이어를 추가합니다.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("0"));
rasterizationOptions.setLayers(stringList);
```

### 4단계: JPEG 옵션 설정

JpegOptions(또는 래스터 형식의 경우 ImageOptions) 인스턴스를 생성하고 CadRasterizationOptions에 연결합니다.

```java
JpegOptions options = new JpegOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

### 5단계: JPEG로 내보내기

마지막으로 각 레이어를 JPEG 형식으로 내보냅니다.

```java
image.save(dataDir + "CADLayersToRasterImageFormats_out_.jpg", options);
```

추가 레이어에 대해 이 단계를 반복하거나 요구 사항에 따라 설정을 사용자 정의하세요.

## 결론

이 포괄적인 가이드를 따르면 Java용 Aspose.CAD의 기능을 성공적으로 활용하여 CAD 레이어를 래스터 이미지 형식으로 변환할 수 있습니다. 이 도구를 사용하면 문서 시각화 및 조작을 쉽게 향상할 수 있습니다.

## FAQ

### Q1: Aspose.CAD for Java를 다른 프로그래밍 언어와 함께 사용할 수 있나요?

A1: Aspose.CAD는 주로 Java를 지원하지만 .NET과 같은 다른 언어에도 사용할 수 있는 버전이 있습니다.

### Q2: 추가 지원이나 도움은 어디서 찾을 수 있나요?

 A2: 질문이나 도움이 필요하면 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19).

### Q3: 무료 평가판이 제공됩니까?

 A3: 예, 다음에서 무료 평가판을 받아 Aspose.CAD를 탐색할 수 있습니다.[여기](https://releases.aspose.com/).

### Q4: Aspose.CAD의 임시 라이선스는 어떻게 얻을 수 있나요?

 A4: 다음에서 임시 라이센스를 취득하세요.[이 링크](https://purchase.aspose.com/temporary-license/).

### Q5: Aspose.CAD for Java에 대한 특정 시스템 요구 사항이 있습니까?

A5: 호환 가능한 Java 개발 환경이 있는지 확인하세요. 자세한 요구 사항은 설명서를 참조하세요.