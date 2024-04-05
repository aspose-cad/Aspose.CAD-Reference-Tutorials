---
title: Java용 Aspose.CAD를 사용하여 포함된 DGN을 PDF로 내보내기
linktitle: 포함된 DGN 내보내기
second_title: Aspose.CAD 자바 API
description: Java용 Aspose.CAD를 사용하여 포함된 DGN 파일을 PDF로 내보내는 방법에 대한 단계별 가이드를 살펴보세요. 원활한 CAD 파일 조작으로 Java 애플리케이션을 강화하세요.
type: docs
weight: 11
url: /ko/java/dgn-export-options/export-embedded-dgn/
---
## 소개

Java용 Aspose.CAD를 사용하여 내장된 DGN 파일을 내보내는 방법에 대한 포괄적인 튜토리얼에 오신 것을 환영합니다. Aspose.CAD는 Java 개발자가 CAD 파일을 원활하게 사용할 수 있게 해주는 강력한 라이브러리입니다. 이 튜토리얼에서는 단계별 지침을 사용하여 포함된 DGN 파일을 PDF로 내보내는 과정을 안내합니다. 숙련된 개발자이든 이제 막 시작하는 개발자이든 이 튜토리얼은 Aspose.CAD의 기능을 활용하여 Java 애플리케이션을 향상시키는 데 도움이 될 것입니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.
- Java 개발 환경: 컴퓨터에 Java 개발 환경이 설정되어 있는지 확인하십시오.
-  Aspose.CAD for Java: 다음 사이트에서 Aspose.CAD for Java 라이브러리를 다운로드하여 설치하세요.[여기](https://releases.aspose.com/cad/java/).

## 패키지 가져오기

시작하려면 Java 프로젝트에서 필요한 패키지를 가져와야 합니다. 코드에 다음 가져오기 문을 추가합니다.

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

이제 예제 코드를 여러 단계로 나누어 보겠습니다.

## 1단계: 입력 및 출력 경로 설정

문서가 있는 디렉토리 경로를 정의하고 입력 DWG 파일 이름을 지정합니다.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

## 2단계: DWG 파일 로드

 DWG 파일을`Image` Aspose.CAD를 사용하여 개체를 만듭니다.

```java
Image objImage = Image.load(fileName);
```

## 3단계: 래스터화 옵션 구성

내보내기에 포함할 레이아웃과 같은 래스터화 옵션을 구성합니다.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

## 4단계: PDF 옵션 구성

벡터 래스터화 옵션을 포함한 PDF 옵션을 설정합니다.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## 5단계: PDF 파일 저장

구성된 옵션으로 PDF 파일을 저장합니다.
```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## 결론

축하해요! Java용 Aspose.CAD를 사용하여 포함된 DGN 파일을 PDF로 성공적으로 내보냈습니다. 이 튜토리얼에서는 효율적인 CAD 파일 조작을 위해 Aspose.CAD를 Java 애플리케이션에 통합하는 필수 단계를 다루었습니다.

## FAQ

### Q1: 상용 프로젝트에서 Aspose.CAD for Java를 사용할 수 있나요?

 A1: 네, Aspose.CAD for Java는 상용 라이브러리입니다. 에서 라이센스를 얻을 수 있습니다.[여기](https://purchase.aspose.com/buy).

### Q2: 무료 평가판이 있나요?

 A2:예, Aspose.CAD for Java 무료 평가판에 액세스할 수 있습니다.[여기](https://releases.aspose.com/).

### Q3: Java용 Aspose.CAD에 대한 지원을 어떻게 받을 수 있나요?

A3: Aspose.CAD 커뮤니티에서 지원을 요청할 수 있습니다.[법정](https://forum.aspose.com/c/cad/19).

### Q4: 임시 라이센스가 필요한 경우 어떻게 해야 합니까?

 A4: 임시 라이센스를 얻을 수 있습니다[여기](https://purchase.aspose.com/temporary-license/).

### Q5: 문서는 어디서 찾을 수 있나요?

 A5: 문서를 사용할 수 있습니다.[여기](https://reference.aspose.com/cad/java/).