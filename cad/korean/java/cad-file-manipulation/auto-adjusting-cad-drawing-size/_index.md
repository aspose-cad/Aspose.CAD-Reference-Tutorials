---
title: Aspose.CAD for Java를 사용하여 CAD 도면 크기 자동 조정
linktitle: CAD 도면 크기 자동 조정
second_title: Aspose.CAD 자바 API
description: Aspose.CAD를 사용하여 Java에서 CAD 도면 크기를 자동 조정하는 원활한 프로세스를 살펴보세요. 효율적인 CAD 파일 조작을 위한 단계별 가이드를 따르십시오.
weight: 13
url: /ko/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java를 사용하여 CAD 도면 크기 자동 조정

## 소개

CAD(Computer-Aided Design) 세계에서는 도면 크기 조정이 일반적인 요구 사항이며 Aspose.CAD for Java를 사용하면 원활한 프로세스가 됩니다. 이 강력한 라이브러리는 Java 애플리케이션에서 CAD 파일을 처리하기 위한 포괄적인 도구를 제공합니다. 이 튜토리얼에서는 Aspose.CAD를 사용하여 CAD 도면 크기를 자동 조정하는 단계별 프로세스를 살펴보겠습니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

1.  Java 개발 환경: 컴퓨터에 Java가 설치되어 있는지 확인하세요. 당신은 그것을 다운로드 할 수 있습니다[여기](https://www.java.com/en/download/).

2.  Aspose.CAD 라이브러리: 다음에서 Java용 Aspose.CAD 라이브러리를 다운로드하여 설치하세요.[여기](https://releases.aspose.com/cad/java/).

3. 샘플 CAD 파일: 문서 디렉토리에 샘플 CAD 파일(예: 샘플.dwg)이 있습니다.

## 네임스페이스 가져오기

Java 애플리케이션에 Aspose.CAD 기능을 활용하는 데 필요한 네임스페이스를 포함합니다. 예는 다음과 같습니다.

```java

import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

이제 CAD 도면 크기를 자동 조정하는 프로세스를 관리 가능한 단계로 나누어 보겠습니다.

## 1단계: CAD 도면 로드

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "sample.dwg";
Image objImage = Image.load(sourceFilePath);
```

이 단계에는 지정된 파일 경로에서 CAD 도면을 로드하는 작업이 포함됩니다.

## 2단계: BmpOptions 생성

```java
BmpOptions bmpOptions = new BmpOptions();
```

 인스턴스화`BmpOptions` BMP 형식에 대한 다양한 옵션을 설정하는 데 사용되는 클래스입니다.

## 3단계: CadRasterizationOptions 생성

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

 인스턴스 만들기`CadRasterizationOptions` CAD 파일의 래스터화 설정을 사용자 정의합니다.

## 4단계: 레이아웃 속성 설정

```java
cadRasterizationOptions.setLayouts(new String[]{"Model"});
```

출력에 포함할 레이아웃을 지정합니다. 이 경우 "모델" 레이아웃을 사용합니다.

## 5단계: BMP 형식으로 내보내기

```java
String outPath = sourceFilePath + ".bmp";
objImage.save(outPath, bmpOptions);
```

마지막으로 조정된 CAD 도면을 BMP 형식으로 지정된 출력 경로에 저장합니다.

Java 애플리케이션에서 이 단계를 반복하면 Aspose.CAD for Java를 사용하여 CAD 도면 크기를 성공적으로 자동 조정하게 됩니다.

## 결론

이 튜토리얼에서는 Aspose.CAD for Java를 사용하여 CAD 도면 크기를 자동 조정하는 과정을 살펴보았습니다. 이 라이브러리는 CAD 파일 조작을 단순화하여 개발자에게 강력한 솔루션을 제공합니다.

## FAQ

### Q1: Aspose.CAD는 다른 CAD 파일 형식과 호환됩니까?

A1: 예, Aspose.CAD는 DWG, DXF, DGN 등을 포함한 다양한 CAD 형식을 지원합니다.

### Q2: Aspose.CAD를 상업용 프로젝트에 사용할 수 있나요?

 A2: 물론이죠! 방문하다[여기](https://purchase.aspose.com/buy) 라이선스 옵션을 살펴보세요.

### Q3: 테스트 목적으로 임시 라이센스를 얻으려면 어떻게 해야 합니까?

 A3: 임시 라이센스 취득[여기](https://purchase.aspose.com/temporary-license/) 테스트 및 평가를 위해.

### Q4: Aspose.CAD에 대한 지원은 어디서 찾을 수 있나요?

 A4: Aspose.CAD 커뮤니티에 가입하세요[법정](https://forum.aspose.com/c/cad/19) 도움과 토론을 위해.

### Q5: Aspose.CAD for Java에 대한 무료 평가판이 있습니까?

 A5: 예, 무료 평가판에 액세스할 수 있습니다.[여기](https://releases.aspose.com/) 도서관의 기능을 탐색합니다.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
