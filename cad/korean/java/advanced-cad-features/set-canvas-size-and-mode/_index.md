---
date: 2025-12-10
description: Aspose.CAD for Java를 사용하여 캔버스 크기 설정, 자동 레이아웃 스케일링 및 TIFF 내보내기를 수행하면서
  CAD를 PDF로 변환하는 방법을 배웁니다.
linktitle: Convert CAD to PDF – Set Canvas Size & Mode
second_title: Aspose.CAD Java API
title: CAD를 PDF로 변환 – 캔버스 크기 및 모드 설정 (Java)
url: /ko/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 캔버스 크기 및 모드 설정

## 소개

전체 캔버스 크기더링 모드를 완벽히 제어하면서 **CAD를 PDF로 변환**하고 싶으신가요? 이 포괄적인 가이드는 Java에서 캔버스 크기를 설정하고 자동 레이아웃 스케일링을 활성화한 뒤, Aspose.CAD를 사용해 결과물을 PDF와 TIFF 형식 단계를 안내합니다. 프로덕션 파이프라인을 다듬거나 프로토타입을 실험하든, 여기서 명확하고 실행 가능한 지침을 찾을 수 있습니다.

## 빠른 답변
- **“convert CAD to PDF”는 무엇을 의미합니까?** CAD 도면(예: DXF, DWG)을 모든 플랫폼에서 볼 수 있는 PDF 문서로 변환하는 것입니다.  
- **TIFF로도 내보낼 수 있나요?** 예—`TiffOptions`를 사용해 고해상도 래스터 이미지를 생성합니다.  
- **Java에서 캔버스 크기를 제어하는 옵션은 무엇입니까?** `CadRasterizationOptions.setPageWidth/Height`.  
- **자동 레이아웃 스케일링이란?** 캔버스 크기가 변경될 때 원본 레이아웃 비율을 유지하는 플래그(`setAutomaticLayoutsScaling(true)`).  
- **Aspose.CAD 라이선스가 필요합니까?** 프로덕션 사용을 위해 임시 또는 영구 라이선스가 필요합니다.

## **convert CAD to PDF**란 무엇입니까?

CAD를 PDF로 변환한다는 것은 벡터 기반 엔지니어링 도면을 PDF 페이지로 렌더링하여 선 작업, 레이어 및 기하학을 보존하면서 파일을 보편적으로 접근 가능하게 만드는 것을 의미합니다.

## 왜 캔버스 크기를 **java**에서 설정해야 합니까?

Java에서 캔버스 크기를 설정하면 출력 해상도와 페이지 치수를 정의할 수 있어, 결과 PDF 또는 TIFF가 인쇄 또는 디스플레이 요구 사항에 정확히 맞도록 보장합니다. 또한 스케일링 동작을 제어할 수 있어 대형 도면에 필수적입니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건을 준비하십시오:

- Aspose.CAD for Java: Java 환경에 Aspose.CAD 라이브러리가 설치되어 있는지 확인하십시오. [여기](https://releases.aspose.com/cad/java/)에서 다운로드할 수 있습니다.

- 문서 디렉터리: CAD 파일을 저장할 문서 디렉터리를 설정하십시오. 이 디렉터리는 튜토리얼 단계에서 참조됩니다.

이제 단계별 가이드를 시작해 보겠습니다.

## 네임스페이스 가져오기

이 단계에서는 Aspose.CAD 프로젝트를 시작하기 위해 필요한 네임스페이스를 가져옵니다.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## 단계 1: Aspose.CAD 클래스 가져오기

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

이 코드 스니펫에서는 리소스 디렉터리 경로를 설정하고 Aspose.CAD의 `Image` 클래스를 사용해 DXF 파일을 로드합니다.

## 단계 2: **CadRasterizationOptions** 속성 설정 (set canvas size java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

여기서는 `CadRasterizationOptions` 인스턴스를 생성하고 페이지 너비, 페이지 높이 및 **자동 레이아웃 스케일링**과 같은 속성을 구성합니다. 이는 변환을 위한 **캔버스 모드 구성**의 핵심입니다.

## 단계 3: PdfOptions 생성 및 VectorRasterizationOptions 설정

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

이제 `PdfOptions` 인스턴스를 생성하고, 앞서 구성한 `CadRasterizationOptions`를 `VectorRasterizationOptions` 속성에 할당합니다.

## 단계 4: PDF로 내보내기 (convert cad to pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

마지막으로 지정된 옵션을 사용해 CAD 이미지를 PDF 파일로 저장하여 **convert CAD to PDF** 프로세스를 완료합니다.

## 단계 5: TiffOptions 생성 및 VectorRasterizationOptions 설정 (export cad to tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

이 단계에서는 `TiffOptions` 인스턴스를 설정하고 해당 `VectorRasterizationOptions` 속성을 구성합니다.

## 단계 6: TIFF로 내보내기

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

마지막으로 지정된 옵션을 사용해 CAD 이미지를 TIFF 파일로 저장하며, 캔버스 크기를 구성한 후 **CAD를 TIFF로 내보내는** 방법을 보여줍니다.

## 일반적인 문제 및 해결책

| 문제 | 원인 | 해결책 |
|------|------|--------|
| 출력 PDF가 빈 페이지로 표시됨 | `setNoScaling(true)`가 일부 도면의 렌더링을 비활성화 | `setNoScaling(true)`를 제거하거나 `false`로 설정합니다. |
| TIFF 해상도가 낮게 보임 | 페이지 너비/높이가 너무 작음 | `setPageWidth` / `setPageHeight` 값을 증가시킵니다. |
| 레이아웃이 왜곡됨 | 자동 레이아웃 스케일링이 비활성화됨 | `setAutomaticLayoutsScaling(true)`가 활성화되어 있는지 확인합니다. |

## 결론

축하합니다! 이제 **CAD를 PDF로 변환**하고 **CAD를 TIFF로 내보내기**를 성공적으로 수행했으며, **java에서 캔버스 크기 설정**, **자동 레이아웃 스케일링 활성화**, 그리고 고품질 출력을 위한 **캔버스 모드 구성** 방법을 익혔습니다. 이 튜토리얼은 CAD 변환 프로젝트의 견고한 기반을 제공합니다. 더 많은 기능과 가능성은 [Aspose.CAD documentation](https://reference.aspose.com/cad/java/)에서 확인해 보세요.

## FAQ

### Q1: Aspose.CAD for Java를 다른 Java 프레임워크와 함께 사용할 수 있나요?

A1: 예, Aspose.CAD는 다양한 Java 프레임워크와 원활하게 통합되도록 설계되었습니다.

### Q2: Aspose.CAD에 대한 임시 라이선스를 제공하나요?

A2: 예, [여기](https://purchase.aspose.com/temporary-license/)에서 임시 라이선스를 받을 수 있습니다.

### Q3: Aspose.CAD에 대한 커뮤니티 지원은 어디서 받을 수 있나요?

A3: 커뮤니티 지원 및 토론은 [Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)에서 확인하십시오.

### Q4: Aspose.CAD를 무료로 체험할 수 있나요?

A4: 물론입니다! [여기](https://releases.aspose.com/)에서 무료 체험을 받으세요.

### Q5: Aspose.CAD for Java를 어떻게 구매하나요?

A5: 제품은 [여기](https://purchase.aspose.com/buy)에서 구매할 수 있습니다.

**추가 Q&A**

**Q: 캔버스 크기가 PDF의 벡터 품질에 영향을 미칩니까?**  
**A:** 아니요. 캔버스 크기는 페이지 치수를 제어할 뿐이며, 벡터 데이터는 해상도에 독립적이어서 어떤 확대 수준에서도 선명하게 렌더링됩니다.

**Q: TIFF 출력에 다른 DPI를 설정할 수 있나요?**  
**A:** 예. `TiffOptions`를 만들기 전에 `rasterizationOptions.setResolution(dpiValue)`를 조정하면 됩니다.

---

**Last Updated:** 2025-12-10  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}