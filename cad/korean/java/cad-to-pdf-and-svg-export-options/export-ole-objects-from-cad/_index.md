---
date: 2026-01-04
description: Aspose.CAD for Java를 사용하여 **CAD를 PNG로 저장**하고 CAD 파일에서 OLE 객체를 손쉽게 내보내는
  방법을 배워보세요. 빠른 설정, 전체 코드 샘플, 그리고 모범 사례 팁을 제공합니다.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java로 CAD를 PNG로 저장하고 OLE 객체를 내보내기
url: /ko/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java를 사용하여 CAD를 PNG로 저장하고 OLE 객체 내보내기

## 소개

빠르게 변화하는 컴퓨터 지원 설계 (CAD) 분야에서 **CAD를 PNG로 저장**하면서 포함된 OLE(Object Linking and Embedding) 객체를 추출할 수 있다면 작업 흐름을 크게 간소화할 수 있습니다. 배치 변환 도구를 만들든, 웹 포털용 썸네일을 생성하든, 혹은 OLE 콘텐츠를 보관하든, Aspose.CAD for Java는 이를 프로그램matically 수행할 수 있는 깔끔한 방법을 제공합니다. 이 튜토리얼에서는 프로젝트 설정부터 각 OLE 객체를 PNG 이미지로 내보내는 전체 과정을 단계별로 안내합니다.

## 빠른 답변
- **Can I export OLE objects directly to PNG?** Yes – Aspose.CAD loads the CAD file and lets you rasterize each layout to PNG.  
- **What Java version is required?** Java 8 or later.  
- **Do I need a license for this feature?** A free trial works for evaluation; a license is required for production.  
- **Will vector data be preserved?** The PNG rasterization keeps visual fidelity, but the output is raster, not vector.  
- **Is batch processing supported?** Absolutely – iterate over an array of files as shown in the code sample.

## 사전 요구 사항

시작하기 전에 다음이 준비되어 있어야 합니다:

- **Java Development Kit (JDK)** – Java 8+가 설치되고 구성되어 있어야 합니다.  
- **Aspose.CAD for Java** – 최신 라이브러리를 [download link](https://releases.aspose.com/cad/java/)에서 다운로드하십시오.  
- **CAD source files** – 내보내고자 하는 OLE 객체가 포함된 DWG/DXF/DGN 파일이면 모두 가능합니다.

## 네임스페이스 가져오기

CAD 파일을 다루려면 핵심 Aspose.CAD 클래스를 가져와야 합니다. 아래와 같이 import 블록을 그대로 유지하십시오 – 튜토리얼 후반에 사용되는 클래스들을 제공합니다.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## CAD를 PNG로 저장하는 방법

아래는 **OLE 객체를 내보내고 CAD를 PNG로 저장하는** 방법을 단계별로 간결하게 정리한 가이드입니다. 각 단계마다 짧은 설명과 프로젝트에 복사해 넣어야 할 정확한 코드를 제공합니다.

### 단계 1: 문서 디렉터리 설정

CAD 도면이 저장된 폴더를 정의합니다. 플레이스홀더를 실제 머신의 경로로 교체하십시오.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### 단계 2: CAD 파일 이름 정의

처리하려는 모든 CAD 파일을 나열합니다. 필요에 따라 항목을 추가하면 됩니다.

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### 단계 3: PNG 내보내기 옵션 설정

래스터화 설정을 구성합니다. 여기서는 특정 레이아웃(`Layout1`)을 대상으로 하고 기본 PNG 옵션을 사용합니다.

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

### 단계 4: CAD 파일을 순회하며 PNG로 저장

각 CAD 파일을 로드하고, OLE 객체를 래스터화한 뒤, 출력 PNG 파일을 기록합니다. `_out.png` 접미사는 생성된 이미지를 식별하는 데 도움이 됩니다.

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

## 일반적인 문제 및 해결책

| 문제 | 발생 원인 | 해결 방법 |
|------|----------|----------|
| **`Image.load` throws `FileNotFoundException`** | `dataDir` 경로가 잘못되었거나 파일 이름에 오타가 있습니다. | 디렉터리 문자열을 다시 확인하고 파일 이름이 정확히 일치하는지(공백 포함) 확인하십시오. |
| **Output PNG is blank** | 레이아웃 이름이 원본 CAD 파일에 존재하지 않습니다. | `cadImage.getLayouts()`를 사용해 사용 가능한 레이아웃을 확인한 뒤 `rasterizationOptions.setLayouts(...)`를 업데이트하십시오. |
| **Large CAD files cause OutOfMemoryError** | 고해상도 이미지를 래스터화하면 힙 메모리를 많이 사용합니다. | JVM 힙을 늘리세요(`-Xmx2g`) 또는 `rasterizationOptions.setResolution(...)`로 래스터화 해상도를 낮추십시오. |

## FAQ

### Q1: Aspose.CAD가 모든 CAD 파일 형식과 호환되나요?

A1: Aspose.CAD는 DWG, DXF, DGN 등 다양한 CAD 형식을 지원합니다. 전체 목록은 [documentation](https://reference.aspose.com/cad/java/)을 참고하십시오.

### Q2: OLE 객체에 대한 내보내기 설정을 사용자 정의할 수 있나요?

A2: 예, Aspose.CAD는 내보내기 설정을 광범위하게 커스터마이징할 수 있는 옵션을 제공하므로 요구 사항에 맞게 출력을 조정할 수 있습니다.

### Q3: Aspose.CAD의 무료 체험판을 이용할 수 있나요?

A3: 예, [here](https://releases.aspose.com/)에서 무료 체험판을 받아 Aspose.CAD의 기능을 살펴볼 수 있습니다.

### Q4: Aspose.CAD 커뮤니티 지원은 어디서 받을 수 있나요?

A4: [forum](https://forum.aspose.com/c/cad/19)에서 Aspose.CAD 커뮤니티에 참여하여 도움을 요청하고 경험을 공유하십시오.

### Q5: Aspose.CAD 라이선스는 어떻게 구매하나요?

A5: 개발 요구에 맞는 라이선스를 구매하려면 [purchase page](https://purchase.aspose.com/buy)를 방문하십시오.

## 결론

이 다섯 단계만 따르면 **CAD를 PNG로 저장**하고 Java 코드 몇 줄만으로 모든 포함된 OLE 객체를 추출할 수 있습니다. 이 방법은 배치 변환, 자동 보고서 생성, 혹은 수동 내보내기 없이 CAD 콘텐츠의 래스터 이미지를 필요로 하는 모든 시나리오에 이상적입니다. 품질 및 성능 요구에 맞게 다양한 래스터화 옵션을 실험해 보세요.

---

**Last Updated:** 2026-01-04  
**Tested With:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}