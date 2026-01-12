---
date: 2026-01-12
description: Aspose.CAD for Java를 사용하여 DWG 파일에 이미지를 추가하고 DWG를 PDF로 변환하는 방법을 배워보세요.
  효율적인 개발을 위한 단계별 가이드를 따라하세요.
linktitle: Import Image to DWG File Using Java
second_title: Aspose.CAD Java API
title: Aspose.CAD Java를 사용하여 DWG 파일에 이미지를 손쉽게 추가하기
url: /ko/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD Java를 사용하여 DWG 파일에 이미지를 손쉽게 추가하기

현대 Java 애플리케이션에서 **DWG에 이미지 추가**는 일반적인 요구사항입니다—CAD 뷰어를 구축하거나, 도면 업데이트를 자동화하거나, 문서를 생성할 때 모두 해당됩니다. Aspose.CAD for Java는 전체 CAD 엔진 없이도 DWG 도면에 래스터 이미지를 직접 삽입할 수 있는 간단하고 고성능의 방법을 제공합니다. 이 튜토리얼에서는 DWG를 로드하고 결과를 PDF로 내보내는 전체 과정을 단계별로 안내합니다.

## Quick Answers
- **필요한 라이브러리는 무엇인가요?** Aspose.CAD for Java  
- **PDF로도 내보낼 수 있나요?** 예 – `PdfOptions`와 `CadRasterizationOptions`를 사용합니다  
- **개발에 라이선스가 필요합니까?** 테스트용으로는 무료 체험판을 사용할 수 있으며, 운영 환경에서는 상용 라이선스가 필요합니다  
- **지원되는 Java 버전은?** Java 8 이상  
- **구현 소요 시간은?** 기본 이미지 가져오기에 약 10‑15분 정도  

## What is “add image to dwg”?
DWG 파일에 이미지를 추가한다는 것은 래스터 사진(PNG, JPEG 등)을 `CadRasterImage` 객체로 도면의 모델 스페이스에 삽입하는 것을 의미합니다. 이미지는 CAD 엔티티 트리의 일부가 되며 다른 CAD 객체와 마찬가지로 위치 지정, 스케일링 및 클리핑이 가능합니다.

## Why use Aspose.CAD for Java to add image to dwg?
- **CAD 소프트웨어가 필요 없음** – API가 내부적으로 DWG 파싱을 처리합니다.  
- **세밀한 제어** 삽입 지점, 스케일링 벡터 및 클리핑에 대해.  
- **내장 PDF 변환** 기능으로 동일한 워크플로우에서 인쇄 가능한 PDF를 생성할 수 있습니다.  
- **크로스 플랫폼** – Windows, Linux, macOS에서 동작합니다.

## Prerequisites
- Aspose.CAD for Java: Aspose.CAD 라이브러리가 설치되어 있는지 확인하십시오. [여기](https://releases.aspose.com/cad/java/)에서 다운로드할 수 있습니다.  
- Java 개발 환경: JDK 8 이상과 선호하는 IDE(IntelliJ, Eclipse, VS Code 등).

## Import Packages
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Step‑by‑Step Guide

### Step 1: Load the DWG File
먼저, DWG 도면이 들어 있는 폴더를 지정하고 `Image.load`를 사용하여 로드합니다.
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### Step 2: Define the Raster Image Definition
`CadRasterImageDef`를 생성하여 삽입하려는 외부 PNG를 참조합니다. 생성자는 이미지 파일 이름과 픽셀 크기를 매개변수로 받습니다.
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### Step 3: Set Insertion Point and Scaling Vectors
삽입 지점은 이미지의 왼쪽 아래 모서리가 나타날 위치를 결정합니다. **U**와 **V** 벡터는 각각 수평 및 수직 스케일링을 제어합니다.
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Step 4: Create the CadRasterImage Object
정의, 삽입 지점 및 벡터를 결합하여 `CadRasterImage`를 생성합니다. 그림의 일부만 표시하려면 클리핑 경계를 설정할 수도 있습니다.
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### Step 5: Add the Image to Model Space
`*Model_Space` 블록에 래스터 이미지를 삽입한 후, 정의가 저장되도록 도면의 객체 컬렉션을 업데이트합니다.
```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadRasterImage);
CadBaseObject[] objs = cadImage.getObjects();
CadBaseObject[] arr = new CadBaseObject[objs.length + 1];
int ind = 0;
for (CadBaseObject obj : objs)
{
    arr[ind] = obj;
    ind++;
}
arr[ind] = cadRasterImageDef;
cadImage.setObjects(arr);
```

### Step 6: Configure PDF Export Options (Optional)
도면의 PDF 버전도 필요하면 `PdfOptions`와 `CadRasterizationOptions`를 함께 구성합니다. 이 단계에서는 동일한 흐름에서 **dwg를 pdf로 변환**하는 방법을 보여줍니다.
```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

### Step 7: Save the Resulting PDF
마지막으로, 수정된 도면을 PDF 파일로 내보냅니다. 동일한 `image` 인스턴스를 사용하므로 PDF에 새로 추가된 래스터 이미지가 반영됩니다.
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

이 단계들을 따라 하면 **dwg에 이미지 추가**를 빠르게 수행할 수 있으며 필요에 따라 **dwg를 pdf로 저장**도 할 수 있습니다.

## Common Issues and Solutions
- **이미지가 표시되지 않음** – 이미지 파일 경로(`road-sign-custom.png`)가 올바른지, 이미지 크기가 `CadRasterImageDef`에 전달된 값과 일치하는지 확인하십시오.  
- **스케일링 오류** – U와 V 벡터를 조정하십시오; 이는 픽셀당 도면 단위를 나타냅니다.  
- **PDF가 빈 화면** – `CadRasterizationOptions.setDrawType`이 `UseObjectColor` 또는 적절한 다른 모드로 설정되어 있는지 확인하십시오.

## Frequently Asked Questions

**Q: Aspose.CAD for Java가 모든 Java 개발 환경과 호환되나요?**  
A: 예, Aspose.CAD for Java는 대부분의 Java 개발 환경과 호환됩니다.

**Q: Aspose.CAD for Java를 상업 프로젝트에 사용할 수 있나요?**  
A: 예, Aspose.CAD for Java를 상업 프로젝트에 사용할 수 있습니다. 라이선스 상세 정보는 [여기](https://purchase.aspose.com/buy)를 방문하십시오.

**Q: Aspose.CAD for Java의 무료 체험판이 있나요?**  
A: 예, 무료 체험판은 [여기](https://releases.aspose.com/)에서 이용할 수 있습니다.

**Q: Aspose.CAD for Java에 대한 지원을 어떻게 받을 수 있나요?**  
A: [Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)에서 지원을 받을 수 있습니다.

**Q: Aspose.CAD for Java의 임시 라이선스를 받을 수 있나요?**  
A: 예, 임시 라이선스는 [여기](https://purchase.aspose.com/temporary-license/)에서 받을 수 있습니다.

---

**마지막 업데이트:** 2026-01-12  
**테스트 환경:** Aspose.CAD for Java 24.11  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}