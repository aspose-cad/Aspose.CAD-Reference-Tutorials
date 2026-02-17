---
date: 2026-02-17
description: Aspose.CAD를 사용하여 Java에서 DWG를 JPEG로 저장하는 방법을 배우고, 여러 레이어를 추가하며, 정밀한 이미지
  변환을 위해 CAD 치수를 조정하세요.
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: Java에서 레이어 지원을 포함한 DWG를 JPEG로 저장
url: /ko/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java에서 레이어 지원으로 DWG를 JPEG로 저장하기

## 소개

이 튜토리얼에서는 **DWG를 JPEG로 저장**하면서 Aspose.CAD for Java의 레이어 지원을 최대한 활용하는 방법을 알아봅니다. 레이어를 사용하면 도면의 특정 부분만 분리하여 필요한 부분만 쉽게 내보낼 수 있습니다. 환경 설정부터 선택한 레이어만 포함된 JPEG 내보내기까지 단계별로 진행합니다.

## 빠른 답변
- **“DWG를 JPEG로 저장”이란 무엇인가요?** DWG(또는 기타 CAD) 도면을 래스터 JPEG 이미지로 변환하는 것입니다.  
- **선택한 레이어만 포함할 수 있나요?** 예 – `setLayers` 메서드를 사용해 렌더링할 레이어를 지정합니다.  
- **이미지 크기를 어떻게 변경하나요?** `CadRasterizationOptions`의 `setPageWidth`와 `setPageHeight`를 조정합니다.  
- **Java 전용 솔루션인가요?** 예제는 Aspose.CAD for Java를 사용하지만 동일한 개념을 다른 언어에도 적용할 수 있습니다.  
- **라이선스가 필요합니까?** 테스트용 무료 체험판을 사용할 수 있으며, 실제 운영 환경에서는 상용 라이선스가 필요합니다.

## “DWG를 JPEG로 저장”이란?
DWG를 JPEG로 저장한다는 것은 벡터 기반 CAD 파일(DWG, DWF, DXF 등)을 표준 JPEG 비트맵으로 래스터화한다는 의미입니다. 웹 페이지, 이메일, 보고서 등 래스터 이미지만 지원하는 환경에 CAD 도면을 삽입해야 할 때 유용합니다.

## 레이어 인식 JPEG 변환을 사용하는 이유
- **관련 데이터에 집중:** 필요한 레이어만 내보내 파일 크기와 시각적 혼란을 줄입니다.  
- **디자인 의도 유지:** 레이어는 객체의 논리적 그룹화를 보존하므로 동일한 소스 파일을 다양한 출력에 재사용할 수 있습니다.  
- **차원에 대한 완전한 제어:** 래스터화 옵션을 조정해 출판 요구에 맞는 고해상도 이미지를 생성할 수 있습니다.

## 사전 요구 사항

시작하기 전에 다음을 준비하십시오:

1. **Aspose.CAD for Java 라이브러리** – [웹사이트](https://releases.aspose.com/cad/java/)에서 다운로드합니다. 설치 가이드를 따라 JAR 파일을 프로젝트 클래스패스에 추가합니다.  
2. **Java 개발 환경** – 최신 JDK(8 이상)가 설치되어 있어야 합니다.

이제 준비가 되었으니, 선택적 레이어 렌더링을 통해 **DWG를 JPEG로 저장**하는 코드를 살펴보겠습니다.

## 네임스페이스 가져오기

필요한 Aspose.CAD 클래스와 표준 Java 유틸리티를 가져옵니다:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## 단계별 가이드

### 단계 1: 파일 경로 설정

소스 DWF 파일이 위치한 경로와 출력 JPEG가 저장될 경로를 정의합니다.

```java
String dataDir = "Your Document Directory" + "DWFDrawings/";
String srcFile = dataDir + "for_layers_test.dwf";
String outFile = dataDir + "for_layers_test.jpg";
```

### 단계 2: DWF 이미지 로드

Aspose.CAD의 `Image.load` 메서드를 사용해 CAD 도면을 읽어옵니다.

```java
Image image = Image.load(srcFile);
```

### 단계 3: 래스터화 옵션 구성 (CAD 차원 조정)

`CadRasterizationOptions` 인스턴스를 생성하고 원하는 출력 크기를 설정합니다. 이 값을 변경하면 최종 JPEG의 **CAD 차원**을 조정할 수 있습니다.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### 단계 4: 레이어 지정 (다중 레이어 추가)

여러 레이어를 렌더링하려면 이름을 리스트에 추가하면 됩니다. 여기서는 “LayerA”라는 단일 레이어로 시작합니다.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*팁:* **다중 레이어를 추가**하려면 `Arrays.asList` 호출을 확장하여 `Arrays.asList("LayerA", "LayerB", "LayerC")`와 같이 작성합니다. 이렇게 하면 변환 시 **특정 CAD 레이어**를 선택할 수 있습니다.

### 단계 5: JPEG 옵션 구성 (Java에서 CAD 이미지 변환)

래스터화 설정을 JPEG 출력 형식에 연결합니다.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 단계 6: JPG로 내보내기 (DWG를 JPEG로 저장)

마지막으로 이미지를 디스크에 기록합니다. 이 단계는 **선택한 레이어만 포함한 JPEG** 파일로 CAD 도면을 저장합니다.

```java
image.save(outFile, jpegOptions);
```

위 단계를 따라 하면 **DWG를 JPEG로 저장**하면서 어떤 레이어가 표시될지 제어하고 이미지 차원도 맞춤 설정할 수 있습니다.

## 레이어 선택으로 DWF를 JPEG로 변환하는 방법

예제는 DWF 소스를 사용하지만, 동일한 래스터화 파이프라인은 지원되는 모든 CAD 형식(DWG, DXF, DGN 등)에서 작동합니다. `srcFile`의 파일 확장자를 변경하기만 하면 라이브러리가 **DWF를 JPEG로 변환**(또는 다른 형식) 작업을 자동으로 처리합니다.

## 일반적인 문제와 해결책

| 문제 | 해결책 |
|-------|----------|
| **레이어가 표시되지 않음** | 레이어 이름이 DWF 파일에 저장된 이름과 정확히 일치하는지(대소문자 구분) 확인합니다. |
| **출력 이미지가 빈 화면** | `setPageWidth`와 `setPageHeight`가 도면 범위에 충분히 큰지 확인합니다. |
| **라이선스 예외** | 테스트용으로는 체험 라이선스를 사용하고, 실제 운영 환경에서는 정식 라이선스를 구입합니다. |

## 자주 묻는 질문

**Q: 래스터화 옵션에 여러 레이어를 추가할 수 있나요?**  
A: 물론입니다. `stringList`에 `Arrays.asList("LayerA", "LayerB")`와 같이 추가 레이어 이름을 넣으면 됩니다.

**Q: Aspose.CAD가 다른 CAD 형식과 호환되나요?**  
A: 예, DWG, DXF, DWF 등 다양한 형식을 지원합니다.

**Q: 출력 이미지 차원을 어떻게 변경하나요?**  
A: `CadRasterizationOptions` 인스턴스의 `setPageWidth`와 `setPageHeight`를 수정하면 됩니다.

**Q: Aspose.CAD 라이선스는 어디서 구매하나요?**  
A: [여기](https://purchase.aspose.com/buy)에서 라이선스 옵션을 확인할 수 있습니다.

**Q: 커뮤니티 지원은 어디서 받을 수 있나요?**  
A: [포럼](https://forum.aspose.com/c/cad/19)에서 Aspose.CAD 커뮤니티에 참여해 도움을 받을 수 있습니다.

---

**마지막 업데이트:** 2026-02-17  
**테스트 환경:** Aspose.CAD for Java 24.11  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}