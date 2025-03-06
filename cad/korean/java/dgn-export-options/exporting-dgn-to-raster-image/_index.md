---
title: Aspose.CAD 튜토리얼을 사용하여 Java DGN에서 JPEG로 변환
linktitle: AutoCAD 형식의 DGN을 래스터 이미지 형식으로 내보내기
second_title: Aspose.CAD 자바 API
description: Aspose.CAD를 사용하여 Java에서 DGN 파일을 JPEG 이미지로 내보내는 방법을 알아보세요. 이 단계별 튜토리얼은 프로세스를 쉽게 안내합니다.
weight: 13
url: /ko/java/dgn-export-options/exporting-dgn-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD 튜토리얼을 사용하여 Java DGN에서 JPEG로 변환

## 소개

Java용 Aspose.CAD를 사용하여 DGN(디자인) 파일을 래스터 이미지 형식으로 내보내는 방법에 대한 포괄적인 튜토리얼에 오신 것을 환영합니다. Aspose.CAD는 Java 개발자가 CAD 파일을 원활하게 사용할 수 있게 해주는 강력한 라이브러리입니다. 이 튜토리얼에서는 DGN 파일을 JPEG 이미지로 변환하는 과정을 안내하고 단계별 지침과 코드 예제를 제공합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.
1.  Aspose.CAD 라이브러리: Java 라이브러리용 Aspose.CAD가 설치되어 있는지 확인하세요. 당신은 그것을 다운로드 할 수 있습니다[여기](https://releases.aspose.com/cad/java/).
2. JDK(Java Development Kit): 컴퓨터에 Java가 설치되어 있는지 확인하세요.
3. 통합 개발 환경(IDE): IntelliJ 또는 Eclipse와 같은 Java 호환 IDE를 사용합니다.

## 패키지 가져오기

Java 프로젝트에서 Aspose.CAD에 필요한 패키지를 가져옵니다. 코드에 다음 줄을 추가합니다.

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## 1단계: DGN 파일 로드

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## 2단계: JpegOptions 객체 생성

```java
ImageOptionsBase options = new JpegOptions();
```

## 3단계: 래스터화 옵션 할당

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## 4단계: 변환된 이미지 저장

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

특정 DGN 파일에 대해 이 단계를 반복하여 그에 따라 파일 경로를 조정합니다.

## 결론

축하해요! Java용 Aspose.CAD를 사용하여 DGN 파일을 래스터 이미지 형식으로 내보내는 방법을 성공적으로 배웠습니다. 이 튜토리얼에서는 이 기능을 Java 애플리케이션에 통합하는 데 필요한 지식을 제공합니다.

## FAQ

### Q1: Aspose.CAD for Java를 다른 CAD 파일 형식과 함께 사용할 수 있습니까?

A1: 예, Aspose.CAD는 다양한 CAD 형식을 지원하여 Java 개발자에게 다양한 솔루션을 제공합니다.

### Q2: Aspose.CAD for Java에 대한 무료 평가판이 있습니까?

 A2: 예, 무료 평가판에 액세스할 수 있습니다.[여기](https://releases.aspose.com/).

### Q3: Aspose.CAD for Java에 대한 문서는 어디서 찾을 수 있나요?

 A3: 설명서를 참조하세요[여기](https://reference.aspose.com/cad/java/).

### Q4: Java용 Aspose.CAD에 대한 지원을 어떻게 받을 수 있나요?

 A4: 지원 포럼을 방문하세요.[여기](https://forum.aspose.com/c/cad/19).

### Q5: Aspose.CAD for Java 라이선스는 어디서 구입할 수 있나요?

 A5: 라이센스를 구매할 수 있습니다[여기](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
