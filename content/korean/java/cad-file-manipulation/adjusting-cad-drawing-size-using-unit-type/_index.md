---
title: Java용 Aspose.CAD와 함께 단위 유형을 사용하여 CAD 도면 크기 조정
linktitle: 단위 유형을 사용하여 CAD 도면 크기 조정
second_title: Aspose.CAD 자바 API
description: CAD 도면 크기를 쉽게 조정할 수 있는 Aspose.CAD for Java의 기능을 살펴보세요. 정확성과 적응성을 위한 단계별 가이드를 따르세요.
type: docs
weight: 14
url: /ko/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
---
## 소개

끊임없이 진화하는 CAD(Computer-Aided Design) 영역에서는 정확성과 적응성이 무엇보다 중요합니다. 일반적인 요구 사항 중 하나는 특정 단위 유형에 따라 CAD 도면의 크기를 조정하는 것입니다. Aspose.CAD for Java는 CAD 파일을 프로그래밍 방식으로 조작하기 위한 원활한 기능을 제공하는 강력한 동맹으로 등장합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

- Java 개발 환경: 컴퓨터에 기능적인 Java 개발 환경이 설정되어 있는지 확인하십시오.

-  Java 라이브러리용 Aspose.CAD: Aspose.CAD 라이브러리를 다운로드하여 Java 프로젝트에 통합하세요. 라이브러리를 얻을 수 있습니다[여기](https://releases.aspose.com/cad/java/).

## 네임스페이스 가져오기

Java 코드에 Aspose.CAD 기능에 액세스하는 데 필요한 네임스페이스를 포함합니다. 다음 가져오기를 추가합니다.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

이제 단위 유형을 사용하여 CAD 도면 크기를 조정하는 프로세스를 관리 가능한 단계로 나누어 보겠습니다.

## 1단계: 데이터 디렉터리 정의

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

CAD 파일이 있는 디렉터리의 경로를 설정합니다.

## 2단계: CAD 도면 로드

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

 Aspose.CAD를 사용하여 CAD 도면을 로드합니다.`Image` 수업.

## 3단계: BMP 옵션 생성

```java
BmpOptions bmpOptions = new BmpOptions();
```

 인스턴스화`BmpOptions` CAD 레이아웃을 BMP 형식으로 내보내는 클래스입니다.

## 4단계: 래스터화 옵션 구성

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

 인스턴스 만들기`CadRasterizationOptions` 그리고 그것을`BmpOptions` 벡터 래스터화용.

## 5단계: 단위 유형 설정

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

CAD 도면에 대해 원하는 단위 유형을 지정합니다. 이 예에서는 이를 센티미터로 설정했습니다.

## 6단계: 레이아웃 설정

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

내보내는 동안 고려할 레이아웃을 정의합니다. 이 경우에는 "모델" 레이아웃을 선택했습니다.

## 7단계: BMP로 내보내기

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

마지막으로 수정된 CAD 도면을 BMP 형식으로 저장합니다.

## 결론

Aspose.CAD for Java를 사용하면 CAD 도면 크기를 쉽게 조정할 수 있습니다. 이 튜토리얼에서는 정확한 결과를 얻는 데 있어 각 단계의 중요성을 강조하면서 프로세스를 안내했습니다.

## FAQ

### Q1: Aspose.CAD for Java를 다른 프로그래밍 언어와 함께 사용할 수 있나요?

A1: Aspose.CAD는 주로 Java를 지원하지만 .NET과 같은 다른 언어에도 사용할 수 있는 버전이 있습니다.

### Q2: Aspose.CAD에 대한 라이센스 옵션이 있습니까?

 A2: 예, 라이선스 옵션을 살펴보고 Aspose.CAD를 구입할 수 있습니다.[여기](https://purchase.aspose.com/buy).

### Q3: Aspose.CAD에 대한 무료 평가판이 있습니까?

 A3: 물론 무료 평가판에 액세스할 수 있습니다.[여기](https://releases.aspose.com/).

### Q4: Java용 Aspose.CAD에 대한 지원을 어떻게 받을 수 있나요?

 A4: Aspose.CAD 포럼을 방문하세요.[여기](https://forum.aspose.com/c/cad/19) 포괄적인 지원을 위해.

### Q5: Aspose.CAD의 임시 라이선스를 얻을 수 있나요?

 A5: 예, 임시 라이센스를 취득할 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).