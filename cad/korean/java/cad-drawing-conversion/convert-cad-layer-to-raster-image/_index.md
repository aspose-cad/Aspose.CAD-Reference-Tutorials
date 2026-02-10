---
date: 2025-12-18
description: Aspose CAD Java 튜토리얼을 수행하여 CAD 레이어를 손쉽게 래스터 이미지로 변환하는 방법을 배워보세요. 원활한
  문서 시각화를 위해 단계별 가이드를 따라가세요.
linktitle: Convert CAD Layer to Raster Image Format
second_title: Aspose.CAD Java API
title: Aspose CAD Java 튜토리얼 – CAD 레이어를 래스터 이미지 형식으로 변환
url: /ko/java/cad-drawing-conversion/convert-cad-layer-to-raster-image/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose CAD Java 튜토리얼: CAD 레이어를 래스터 이미지 형식으로 변환

## 소개

컴퓨터 지원 설계(CAD) 분야에서 개별 CAD 레이어를 래스터 이미지 형식으로 변환하는 것은 손쉬운 공유, 인쇄 또는 추가 이미지 처리를 위해 필수적입니다. 이 **aspose cad java tutorial**에서는 **Aspose.CAD for Java**를 활용하여 특정 레이어를 추출하고 JPEG(또는 다른 래스터 형식)로 저장하는 방법을 보여줍니다. 이 가이드를 끝까지 읽으면 레이어 수준 변환이 왜 중요한지, 래스터화 옵션을 어떻게 구성하는지, 몇 줄의 코드만으로 결과를 내보내는 방법을 이해하게 됩니다.

## 빠른 답변
- **이 튜토리얼은 무엇을 다루나요?** Aspose.CAD for Java를 사용하여 선택한 CAD 레이어를 래스터 이미지로 변환합니다.  
- **지원되는 형식은 무엇인가요?** Aspose에서 지원하는 모든 래스터 형식(JPEG, PNG, BMP 등)입니다.  
- **라이선스가 필요합니까?** 개발용으로는 무료 체험판을 사용할 수 있지만, 운영 환경에서는 라이선스가 필요합니다.  
- **전제 조건은 무엇인가요?** Java 개발 환경 및 Aspose.CAD Java 라이브러리.  
- **구현에 얼마나 걸리나요?** 기본 변환의 경우 대략 10–15분 정도 소요됩니다.

## 전제 조건

코드에 들어가기 전에 다음 항목을 준비하십시오:

- **Java Development Environment** – JDK 8 이상이 설치되고 구성되어 있어야 합니다.  
- **Aspose.CAD Library** – [download link](https://releases.aspose.com/cad/java/)에서 Java용 Aspose.CAD 라이브러리를 다운로드하고 설치하십시오.

## 네임스페이스 가져오기

이 단계에서는 CAD 파일 작업에 필요한 클래스를 가져옵니다.

### Aspose.CAD 클래스 가져오기

Java 소스 파일에 필요한 Aspose.CAD import 구문을 포함합니다:

```java
import com.aspose.cad.Image;


import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## CAD 레이어를 래스터 이미지 형식으로 변환

아래는 전체 단계별 프로세스입니다. 각 단계는 코드 블록 전에 쉬운 설명으로 제공되어 어떤 작업이 이루어지는지 정확히 알 수 있습니다.

### 1단계: CAD 파일 설정

먼저 CAD 파일을 지정하고 `Image` 객체에 로드합니다.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### 2단계: 래스터화 옵션 구성

`CadRasterizationOptions` 인스턴스를 생성하여 출력 이미지 크기와 품질을 정의합니다.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
```

### 3단계: CAD 레이어 지정

래스터화하려는 레이어 이름을 추가합니다. 이 예제에서는 기본 레이어 `"0"`을 내보냅니다.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("0"));
rasterizationOptions.setLayers(stringList);
```

### 4단계: JPEG 옵션 설정

`JpegOptions` 객체(또는 다른 래스터 이미지 옵션)를 생성하고 이를 래스터화 설정에 연결합니다.

```java
JpegOptions options = new JpegOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

### 5단계: JPEG로 내보내기

마지막으로 래스터화된 레이어를 JPEG 파일로 저장합니다.

```java
image.save(dataDir + "CADLayersToRasterImageFormats_out_.jpg", options);
```

추가 레이어에 대해 위 단계를 반복하거나 래스터화 매개변수(해상도, 배경색 등)를 조정하여 특정 요구 사항을 충족시킬 수 있습니다.

## 이 접근 방식을 사용하는 이유

- **Selective Export** – 필요한 레이어만 렌더링하여 파일 크기와 처리 시간을 줄입니다.  
- **Format Flexibility** – 핵심 로직을 변경하지 않고 `JpegOptions`를 `PngOptions`, `BmpOptions` 등으로 전환할 수 있습니다.  
- **High‑Quality Rendering** – Aspose.CAD는 원본 CAD 파일과 동일하게 선 굵기, 색상 및 텍스트를 정확히 보존합니다.

## 일반적인 문제 및 해결 방법

| 증상 | 가능한 원인 | 해결 방법 |
|---------|--------------|-----|
| 빈 이미지 출력 | 레이어가 지정되지 않았거나 레이어 이름이 잘못됨 | CAD 파일에 레이어 이름이 존재하는지 확인하고, `image.getLayers()`를 사용하여 레이어 목록을 확인하십시오. |
| 해상도 낮음 | 기본 DPI가 낮음 | 저장하기 전에 `rasterizationOptions.setResolution(300);`(또는 더 높은 값)으로 설정하십시오. |
| 지원되지 않는 CAD 형식 | 구버전 Aspose.CAD 사용 | 최신 Aspose.CAD for Java 릴리스로 업데이트하십시오. |

## 자주 묻는 질문

**Q: Aspose.CAD for Java를 다른 프로그래밍 언어와 함께 사용할 수 있나요?**  
A: Aspose.CAD는 주로 Java를 지원하지만 .NET, C++, 기타 언어 버전도 제공됩니다.

**Q: 추가 지원이나 도움을 어디서 찾을 수 있나요?**  
A: 문의 사항이나 도움이 필요하면 [Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)을 방문하십시오.

**Q: 무료 체험판을 이용할 수 있나요?**  
A: 예, [여기](https://releases.aspose.com/)에서 무료 체험판을 받아 Aspose.CAD를 체험할 수 있습니다.

**Q: Aspose.CAD 임시 라이선스를 어떻게 얻을 수 있나요?**  
A: [이 링크](https://purchase.aspose.com/temporary-license/)에서 임시 라이선스를 획득하십시오.

**Q: Aspose.CAD for Java에 대한 특정 시스템 요구 사항이 있나요?**  
A: 호환 가능한 Java 개발 환경을 갖추고 있는지 확인하십시오; 자세한 요구 사항은 문서를 참고하십시오.

---

**마지막 업데이트:** 2025-12-18  
**테스트 환경:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**작성자:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
