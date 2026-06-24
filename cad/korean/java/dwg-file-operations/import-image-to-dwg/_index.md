---
date: 2026-05-20
description: Aspose.CAD for Java를 사용하여 DWG 파일에 이미지를 추가하고 DWG를 PDF로 변환하는 방법을 알아보세요.
  효율적인 개발을 위한 단계별 가이드를 따라보세요.
keywords:
- add image to dwg
- convert dwg to pdf
- import image into dwg
- embed raster image dwg
- dwg file operations
linktitle: Java를 사용하여 DWG 파일에 이미지 가져오기
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  headline: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  type: TechArticle
- description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  name: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  steps:
  - name: Load the DWG File
    text: First, point to the folder that contains your DWG drawing and load it with
      `Image.load`.
  - name: Define the Raster Image Definition
    text: The `CadRasterImageDef` class defines the external raster image resource
      to be embedded in the drawing.
  - name: Set Insertion Point and Scaling Vectors
    text: The insertion point determines where the lower‑left corner of the image
      will appear. The **U** and **V** vectors control horizontal and vertical scaling.
  - name: Create the CadRasterImage Object
    text: The `CadRasterImage` entity represents a raster picture placed in the DWG
      model space.
  - name: Add the Image to Model Space
    text: Insert the raster image into the `*Model_Space` block, then update the drawing’s
      object collection so the definition is saved.
  - name: Configure PDF Export Options (Optional)
    text: '`PdfOptions` specifies settings for saving a CAD drawing as a PDF file.
      `CadRasterizationOptions` defines how the CAD content is rasterized during PDF
      conversion.'
  - name: Save the Resulting PDF
    text: 'Finally, export the modified drawing as a PDF file. The same `image` instance
      is used, so the PDF reflects the newly added raster image. By following these
      steps, you can **add image to dwg** files quickly and also **save dwg as pdf**
      when needed, covering the most common **dwg file operations** in '
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java works with any IDE that supports JDK 8+, including
      IntelliJ IDEA, Eclipse, and VS Code.
    question: Is Aspose.CAD for Java compatible with all Java development environments?
  - answer: Yes, you can use Aspose.CAD for Java for commercial projects. Visit **[here](https://purchase.aspose.com/buy)**
      for licensing details.
    question: Can I use Aspose.CAD for Java for commercial projects?
  - answer: Yes, you can access the free trial **[here](https://releases.aspose.com/)**.
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: You can seek support on the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**.
    question: How can I get support for Aspose.CAD for Java?
  - answer: Yes, you can get a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.
    question: Can I obtain a temporary license for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Aspose.CAD Java를 사용하여 DWG 파일에 이미지를 손쉽게 추가하기
url: /ko/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD Java를 사용하여 DWG 파일에 이미지를 손쉽게 추가하기

현대 Java 애플리케이션에서 **DWG에 이미지 추가**는 일반적인 요구 사항입니다—CAD 뷰어를 구축하거나, 도면 업데이트를 자동화하거나, 문서를 생성할 때도 마찬가지입니다. Aspose.CAD for Java는 전체 CAD 엔진 없이도 래스터 이미지를 DWG 도면에 직접 삽입할 수 있는 간단하고 고성능의 방법을 제공합니다. 이 튜토리얼에서는 DWG를 로드하고 결과를 PDF로 내보내는 전체 과정을 단계별로 안내하며, **import image into dwg**와 **convert dwg to pdf**를 하나의 워크플로우에서 수행하는 방법도 다룹니다.

## 빠른 답변
- **필요한 라이브러리는 무엇인가요?** Aspose.CAD for Java  
- **PDF로도 내보낼 수 있나요?** Yes – use `PdfOptions` with `CadRasterizationOptions`  
- **개발에 라이선스가 필요합니까?** A free trial works for testing; a commercial license is required for production  
- **지원되는 Java 버전은 무엇인가요?** Java 8 and higher  
- **구현에 얼마나 걸리나요?** About 10‑15 minutes for a basic image import  

## “add image to dwg”란 무엇인가요?

DWG 파일에 이미지를 추가한다는 것은 래스터 이미지(PNG, JPEG 등)를 **CadRasterImage** 엔터티로 도면의 모델 공간에 삽입하는 것을 의미합니다. 삽입된 이미지는 위치를 지정하고, 스케일을 조정하며, 필요에 따라 다른 CAD 객체와 마찬가지로 클리핑할 수 있습니다. 이 엔터티는 도면의 객체 테이블에 저장되며 표준 CAD 뷰어에 표시됩니다.

## DWG에 이미지를 추가하기 위해 Aspose.CAD for Java를 사용하는 이유

타사 CAD 소프트웨어를 설치하지 않아도 DWG 파일에 래스터 그래픽을 삽입할 수 있으며, API를 통해 삽입 지점, 스케일 벡터, 클리핑 경계에 대해 픽셀 단위의 정밀 제어가 가능합니다. Aspose.CAD는 최대 2 GB 크기의 파일을 처리하고, **50개 이상의 입력 및 출력 포맷**을 지원하며, Windows, Linux, macOS에서 실행되어 Java 기반 백엔드에 CAD 조작을 통합할 수 있습니다.

## 사전 요구 사항
- **Aspose.CAD for Java** – 공식 사이트에서 최신 JAR을 **[here](https://releases.aspose.com/cad/java/)** 에서 다운로드하십시오.  
- **Java Development Kit** – JDK 8 이상, 선호하는 IDE(IntelliJ IDEA, Eclipse, VS Code 등)와 함께 사용합니다.  
- 프로덕션 사용을 위한 유효한 **Aspose.CAD license** (체험판은 실험에 사용할 수 있습니다).

## 패키지 가져오기
다음 import 문은 이미지 조작 및 PDF 변환에 사용되는 필수 Aspose.CAD 클래스를 가져옵니다.
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## 단계별 가이드

### 단계 1: DWG 파일 로드
먼저, DWG 도면이 들어 있는 폴더를 지정하고 `Image.load`를 사용하여 로드합니다.
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### 단계 2: 래스터 이미지 정의 설정
`CadRasterImageDef` 클래스는 도면에 삽입될 외부 래스터 이미지 리소스를 정의합니다.
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### 단계 3: 삽입 지점 및 스케일 벡터 설정
삽입 지점은 이미지의 왼쪽 아래 모서리가 나타날 위치를 결정합니다. **U** 및 **V** 벡터는 각각 가로와 세로 스케일을 제어합니다.
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### 단계 4: CadRasterImage 객체 생성
`CadRasterImage` 엔터티는 DWG 모델 공간에 배치된 래스터 이미지를 나타냅니다.
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### 단계 5: 모델 공간에 이미지 추가
래스터 이미지를 `*Model_Space` 블록에 삽입한 후, 정의가 저장되도록 도면의 객체 컬렉션을 업데이트합니다.
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

### 단계 6: PDF 내보내기 옵션 구성 (선택 사항)
`PdfOptions`는 CAD 도면을 PDF 파일로 저장하기 위한 설정을 지정합니다. `CadRasterizationOptions`는 PDF 변환 중 CAD 콘텐츠가 어떻게 래스터화되는지를 정의합니다.
```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

### 단계 7: 결과 PDF 저장
마지막으로, 수정된 도면을 PDF 파일로 내보냅니다. 동일한 `image` 인스턴스를 사용하므로 PDF에 새로 추가된 래스터 이미지가 반영됩니다.
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

이 단계들을 따르면 **add image to dwg** 파일을 빠르게 추가하고 필요할 때 **save dwg as pdf**도 할 수 있어, 가장 일반적인 **dwg file operations**를 하나의 간결한 루틴으로 처리할 수 있습니다.

## 일반적인 문제 및 해결책
- **Image not appearing** – 이미지 파일 경로(`road-sign-custom.png`)가 올바른지, 이미지 크기가 `CadRasterImageDef`에 전달된 값과 일치하는지 확인하십시오.  
- **Incorrect scaling** – U 및 V 벡터를 조정하십시오; 이들은 픽셀당 도면 단위를 나타냅니다.  
- **PDF looks blank** – `CadRasterizationOptions.setDrawType`이 `UseObjectColor` 또는 다른 적절한 모드로 설정되어 있는지 확인하십시오.  

## 자주 묻는 질문

**Q: Aspose.CAD for Java가 모든 Java 개발 환경과 호환되나요?**  
A: 예, Aspose.CAD for Java는 JDK 8+를 지원하는 모든 IDE(IntelliJ IDEA, Eclipse, VS Code 등)와 함께 사용할 수 있습니다.

**Q: Aspose.CAD for Java를 상업 프로젝트에 사용할 수 있나요?**  
A: 예, Aspose.CAD for Java를 상업 프로젝트에 사용할 수 있습니다. 라이선스 상세 정보는 **[here](https://purchase.aspose.com/buy)** 를 방문하십시오.

**Q: Aspose.CAD for Java의 무료 체험판이 있나요?**  
A: 예, 무료 체험판은 **[here](https://releases.aspose.com/)** 에서 이용할 수 있습니다.

**Q: Aspose.CAD for Java에 대한 지원을 어떻게 받을 수 있나요?**  
A: **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** 에서 지원을 받을 수 있습니다.

**Q: Aspose.CAD for Java의 임시 라이선스를 받을 수 있나요?**  
A: 예, 임시 라이선스는 **[here](https://purchase.aspose.com/temporary-license/)** 에서 받을 수 있습니다.

---

**마지막 업데이트:** 2026-05-20  
**테스트 환경:** Aspose.CAD for Java 24.11  
**작성자:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 관련 튜토리얼

- [Aspose.CAD for Java를 사용하여 DWG를 PDF 또는 래스터로 내보내기](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Aspose.CAD for Java를 사용하여 DWG 파일에 사용자 정의 속성 추가](/cad/java/additional-features/add-custom-properties/)
- [CAD를 PNG로 저장 – Aspose.CAD for Java를 사용하여 CAD 도면을 래스터 이미지 포맷으로 변환](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}