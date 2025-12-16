---
date: 2025-12-13
description: Aspose.CAD를 사용하여 Java에서 CAD를 JPEG로 저장하는 방법, 여러 레이어를 추가하는 방법, 그리고 정밀한
  이미지 변환을 위해 CAD 치수를 조정하는 방법을 배워보세요.
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: Java에서 레이어 지원을 포함한 CAD를 JPEG로 저장
url: /ko/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Save CAD as JPEG with Layer Support in Java

## Introduction

이 튜토리얼에서는 **CAD를 JPEG로 저장**하면서 Aspose.CAD for Java의 레이어 지원을 최대한 활용하는 방법을 알아봅니다. 레이어를 사용하면 도면의 특정 부분만 분리하여 필요한 부분만 쉽게 내보낼 수 있습니다. 환경 설정부터 선택한 레이어만 포함된 JPEG를 내보내는 과정까지 단계별로 안내합니다.

## Quick Answers
- **“save CAD as JPEG”가 의미하는 것은?** CAD 도면을 래스터 JPEG 이미지로 변환하는 것입니다.
- **선택한 레이어만 포함할 수 있나요?** 예 – `setLayers` 메서드를 사용하여 렌더링할 레이어를 지정합니다.
- **이미지 크기는 어떻게 변경하나요?** `CadRasterizationOptions`의 `setPageWidth`와 `setPageHeight`를 조정합니다.
- **Java 전용 솔루션인가요?** 예제는 Aspose.CAD for Java를 사용하지만, 동일한 개념을 다른 언어에도 적용할 수 있습니다.
- **라이선스가 필요합니까?** 테스트용 무료 체험판을 사용할 수 있으며, 실제 운영 환경에서는 상용 라이선스가 필요합니다.

## Prerequisites

시작하기 전에 다음 항목을 준비하세요:

1. **Aspose.CAD for Java Library** – [website](https://releases.aspose.com/cad/java/)에서 다운로드합니다. 설치 가이드를 따라 JAR 파일을 프로젝트 클래스패스에 추가하세요.  
2. **Java Development Environment** – 최신 JDK(8 이상)가 설치되어 있어야 합니다.

이제 환경 설정이 완료되었으니, 선택적 레이어 렌더링을 통해 **CAD를 JPEG로 저장**하는 코드를 살펴보겠습니다.

## Import Namespaces

필요한 Aspose.CAD 클래스와 표준 Java 유틸리티를 import합니다:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## Step‑by‑Step Guide

### Step 1: Set Up File Paths

소스 DWF 파일이 위치한 경로와 출력 JPEG가 저장될 경로를 정의합니다.

```java
String dataDir = "Your Document Directory" + "DWFDrawings/";
String srcFile = dataDir + "for_layers_test.dwf";
String outFile = dataDir + "for_layers_test.jpg";
```

### Step 2: Load the DWF Image

Aspose.CAD의 `Image.load` 메서드를 사용해 CAD 도면을 읽어옵니다.

```java
Image image = Image.load(srcFile);
```

### Step 3: Configure Rasterization Options (Adjust CAD Dimensions)

`CadRasterizationOptions` 인스턴스를 생성하고 원하는 출력 크기를 설정합니다. 이 값을 변경하면 최종 JPEG의 **CAD 차원**을 조정할 수 있습니다.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Step 4: Specify Layers (Add Multiple Layers)

여러 레이어를 렌더링하려면 리스트에 레이어 이름을 추가하면 됩니다. 여기서는 “LayerA”라는 단일 레이어로 시작합니다.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*Pro tip:* **여러 레이어를 추가**하려면 `Arrays.asList` 호출을 확장하여 `Arrays.asList("LayerA", "LayerB", "LayerC")`와 같이 작성합니다.

### Step 5: Configure JPEG Options (Java Convert CAD Image)

래스터화 설정을 JPEG 출력 형식에 연결합니다.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Step 6: Export to JPG (Save CAD as JPEG)

마지막으로 이미지를 디스크에 저장합니다. 이 단계에서는 **선택한 레이어만 포함된 CAD 도면을 JPEG 파일**로 저장합니다.

```java
image.save(outFile, jpegOptions);
```

위 단계를 따라 하면 **CAD를 JPEG로 저장**하면서 어떤 레이어가 표시될지 제어하고 이미지 크기도 맞춤 설정할 수 있습니다.

## Common Issues and Solutions

| Issue | Solution |
|-------|----------|
| **Layers not appearing** | 레이어 이름이 DWF 파일에 저장된 이름과 정확히 일치하는지(대소문자 구분) 확인하세요. |
| **Output image is blank** | `setPageWidth`와 `setPageHeight`가 도면 범위에 충분히 큰지 확인하세요. |
| **License exception** | 테스트용 체험 라이선스를 사용하고, 실제 운영 환경에서는 정식 라이선스를 구매하세요. |

## Frequently Asked Questions

**Q: Can I add multiple layers to the rasterization options?**  
A: Absolutely. Extend the `stringList` with additional layer names, e.g., `Arrays.asList("LayerA", "LayerB")`.

**Q: Is Aspose.CAD compatible with other CAD formats?**  
A: Yes, it supports DWG, DXF, DWF, and many more formats.

**Q: How can I change the output image dimensions?**  
A: Modify `setPageWidth` and `setPageHeight` in the `CadRasterizationOptions` instance.

**Q: Where can I purchase a license for Aspose.CAD?**  
A: You can explore licensing options [here](https://purchase.aspose.com/buy).

**Q: Where can I get community support?**  
A: Join the Aspose.CAD community on the [forum](https://forum.aspose.com/c/cad/19) for assistance and discussions.

---

**Last Updated:** 2025-12-13  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}