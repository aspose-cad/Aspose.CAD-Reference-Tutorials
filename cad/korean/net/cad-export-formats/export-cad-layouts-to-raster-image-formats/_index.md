---
date: 2026-03-21
description: Aspose.CAD for .NET를 사용하여 dxf를 png 및 기타 래스터 형식으로 변환하는 방법을 배우세요. 원활한 CAD
  레이어 내보내기를 위한 단계별 가이드를 따라보세요.
linktitle: Export CAD Layouts to Raster Image Formats
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Aspose.CAD for .NET를 사용하여 DXF를 PNG로 변환
url: /ko/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET에서 CAD 레이아웃을 래스터 이미지 형식으로 내보내기

## 소개

Aspose.CAD for .NET을 사용하여 **convert dxf to png** 및 기타 래스터 이미지 형식을 효율적으로 변환하고 싶으신가요? 이 단계별 가이드는 과정을 자세히 안내하고, 작업을 원활하게 수행할 수 있도록 상세한 설명과 코드 스니펫을 제공합니다. 숙련된 개발자이든 Aspose.CAD를 처음 접하는 개발자이든, 이 튜토리얼은 모든 수준의 전문성을 만족합니다.

### 빠른 답변
- **변환을 담당하는 라이브러리는?** Aspose.CAD for .NET  
- **기본 지원 형식은?** JPEG, PNG, BMP, TIFF 래스터 이미지  
- **특정 CAD 레이어를 내보낼 수 있나요?** 예 – `CadRasterizationOptions.Layers`를 사용하여 개별 레이어를 지정합니다  
- **프로덕션에 라이선스가 필요합니까?** 비체험용으로는 유효한 Aspose.CAD 라이선스가 필요합니다  
- **지원되는 .NET 버전은?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7  

## **convert dxf to png**란?

DXF(Drawing Exchange Format) 파일을 PNG로 변환한다는 것은 벡터 기반 CAD 데이터를 픽셀 기반 이미지로 래스터화한다는 의미입니다. 이는 웹 페이지, 보고서 또는 래스터 그래픽만 지원하는 환경에 CAD 도면을 삽입해야 할 때 유용합니다.

## CAD 레이어를 별도로 내보내는 이유는?

CAD 레이어를 개별적으로 내보내면 시각적 출력에 대한 세밀한 제어가 가능하고, 각 이미지의 파일 크기를 줄이며, 레이어별 스타일링이나 후처리를 적용할 수 있습니다. 특히 대형 엔지니어링 도면에서 특정 레이어만 특정 청중에게 보여줄 때 매우 편리합니다.

## 사전 요구 사항

튜토리얼을 시작하기 전에 다음 항목을 준비하십시오:

- **Aspose.CAD for .NET 라이브러리** – [Aspose.CAD 웹사이트](https://releases.aspose.com/cad/net/)에서 다운로드합니다.  
- **CAD 도면 파일** – 래스터 형식으로 변환하려는 DXF 파일(예: `conic_pyramid.dxf`).  

## 네임스페이스 가져오기

.NET 프로젝트에서 Aspose.CAD 기능을 활용하려면 필요한 네임스페이스를 가져와야 합니다. 코드 시작 부분에 다음 네임스페이스를 포함하십시오:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## **convert dxf to png** 단계별 가이드

### 1단계: CAD 도면 로드

DXF 파일을 `Image` 객체에 로드합니다. 이 객체는 메모리 내 전체 CAD 도면을 나타냅니다.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Load a CAD drawing in an instance of Image
using (var image = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD drawing goes here
}
```

### 2단계: `CadRasterizationOptions` 생성

출력 차원 및 해상도와 같은 래스터화 설정을 구성합니다. 이 옵션들은 벡터 데이터가 어떻게 래스터화될지를 제어합니다.

```csharp
// Create an instance of CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

### 3단계: 레이어 지정 (CAD 레이어 내보내기)

특정 레이어만 필요하다면 여기에서 이름을 나열하십시오. 이는 **export cad layers**를 개별적으로 수행하는 예시입니다.

```csharp
// Add the layer name to the CadRasterizationOptions's layer list
rasterizationOptions.Layers = new string[] { "LayerA" };
```

### 4단계: 이미지 형식 선택 – CAD를 PNG(또는 JPEG)로 저장

이미지 형식에 맞는 옵션 객체를 생성합니다. **save cad as png**을 원한다면 `JpegOptions` 대신 `PngOptions`로 교체하십시오.

```csharp
// Create an instance of JpegOptions (or any ImageOptions for raster formats)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

> **프로 팁:** PNG 파일을 생성하려면 `JpegOptions` 대신 `new PngOptions()`를 인스턴스화하면 됩니다.

### 5단계: JPEG(또는 PNG) 형식으로 내보내기

마지막으로 래스터화된 이미지를 디스크에 저장합니다. 파일 확장자가 출력 형식을 결정합니다.

```csharp
// Export each layer to Jpeg format
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

`JpegOptions`를 `PngOptions`로 교체하면 동일한 코드가 **convert dxf to png**를 수행하고 `.png` 파일을 생성합니다.

### 추가 단계: 모든 레이어 변환

도면의 모든 레이어에 대해 **convert cad to raster**가 필요하다면 아래 헬퍼 메서드를 호출하십시오. 이 메서드는 모든 레이어를 순회하며 각각을 별도 이미지로 저장합니다.

```csharp
ConvertAllLayersToRasterImageFormats();
```

> *참고:* `ConvertAllLayersToRasterImageFormats` 구현은 전체 Aspose.CAD 샘플 스위트의 일부이며 레이어 배치 처리 예시를 보여줍니다.

## 일반적인 문제 및 해결 방법

| 증상 | 가능한 원인 | 해결 방법 |
|------|------------|----------|
| 이미지가 빈 화면 또는 흰색 | 래스터화 옵션이 설정되지 않음(예: `PageWidth`/`PageHeight` = 0) | `PageWidth`와 `PageHeight`에 양수 값을 지정하십시오 |
| 레이어가 누락됨 | `Layers` 배열에 잘못된 레이어 이름 지정 | CAD 파일에서 정확한 레이어 이름을 확인하십시오(대소문자 구분) |
| PNG 품질 저하 | 기본 DPI가 낮음 | `rasterizationOptions.Resolution = 300;`으로 설정하여 품질을 높이십시오 |

## 자주 묻는 질문 (Original)

### Q1: 다른 이미지 형식으로 내보낼 수 있나요?

A1: 예, 가능합니다. `JpegOptions`를 원하는 형식의 옵션(`PngOptions`, `BmpOptions` 등)으로 교체하면 됩니다.

### Q2: 체험판 버전이 있나요?

A2: 예, 체험판 버전을 [여기](https://releases.aspose.com/)에서 다운로드하여 Aspose.CAD 기능을 확인할 수 있습니다.

### Q3: Aspose.CAD 지원을 어떻게 받을 수 있나요?

A3: 커뮤니티 지원은 Aspose.CAD [포럼](https://forum.aspose.com/c/cad/19)에서 받거나, 전용 지원을 위해 라이선스를 구매하십시오.

### Q4: 임시 라이선스를 제공하나요?

A4: 예, 임시 라이선스는 [여기](https://purchase.aspose.com/temporary-license/)에서 얻을 수 있습니다.

### Q5: 문서는 어디서 찾을 수 있나요?

A5: 자세한 문서는 [여기](https://reference.aspose.com/cad/net/)에서 확인하십시오.

## 추가 FAQ

**Q: 한 번에 모든 레이어를 내보낼 수 있나요?**  
A: 예, 위에 표시된 `ConvertAllLayersToRasterImageFormats` 메서드를 사용하면 됩니다.

**Q: Aspose.CAD가 SVG와 같은 벡터 형식을 지원하나요?**  
A: 주로 래스터 형식을 대상으로 하지만, 벡터 데이터를 유지하는 PDF로 내보낼 수 있습니다.

**Q: 내보낸 PNG의 배경 색을 어떻게 제어하나요?**  
A: 저장하기 전에 `rasterizationOptions.BackgroundColor`를 원하는 `Color`로 설정하십시오.

**Q: 전체 도면이 아니라 단일 레이아웃만 내보낼 수 있나요?**  
A: 예, `rasterizationOptions.Layouts`를 설정하여 래스터화할 레이아웃 이름을 지정하면 됩니다.

## 결론

이제 **convert dxf to png**, **export cad layers**, **save cad as png** 또는 JPEG를 Aspose.CAD for .NET을 사용해 수행하는 방법을 익혔습니다. `CadRasterizationOptions`를 조정하고 이미지 형식 옵션을 교체하면 거의 모든 래스터 출력 요구에 맞게 변환을 맞춤 설정할 수 있습니다. Aspose.CAD API의 다른 형식 옵션을 탐색하여 CAD‑to‑raster 워크플로우를 확장해 보세요.

---

**마지막 업데이트:** 2026-03-21  
**테스트 환경:** Aspose.CAD for .NET 24.11 (작성 시 최신 버전)  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}