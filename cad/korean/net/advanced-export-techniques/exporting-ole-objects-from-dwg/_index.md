---
description: Aspose.CAD for .NET을 사용하여 DWG를 PNG로 변환하고 DWG 파일에서 OLE 객체를 추출하는 방법을 배우세요
  – 빠르고 코드 중심의 가이드.
linktitle: Exporting OLE Objects from DWG Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DWG를 PNG로 변환 및 OLE 객체 내보내기 - Aspose.CAD 튜토리얼
url: /ko/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
weight: 12
---

2026-03-13" keep date.

"**Tested With:** Aspose.CAD 24.11 for .NET" keep.

"**Author:** Aspose" keep.

Then closing shortcodes.

Then backtop button shortcode.

Make sure to keep all shortcodes exactly.

Now produce final content.

Let's craft translation.

Be careful with markdown formatting: keep spaces.

Let's write.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG 파일에서 OLE 개체 내보내기 - Aspose.CAD 튜토리얼

## 소개

DWG 파일에서 **convert DWG to PNG**를 수행하면서 포함된 OLE 개체를 추출해야 한다면, 여기가 바로 정답입니다. Aspose.CAD for .NET은 이 두 단계 과정을 간단하게 만들어 주며, 몇 줄의 C# 코드만으로 추출 및 래스터화를 자동화할 수 있습니다. 다음 몇 분 동안 환경 설정부터 추출된 OLE 데이터를 포함한 PNG로 DWG를 저장하는 전체 워크플로우를 살펴보겠습니다.

## 빠른 답변
- **이 튜토리얼은 무엇을 다루나요?** Aspose.CAD for .NET을 사용하여 DWG를 PNG로 변환하고 OLE 개체를 추출합니다.  
- **라이선스가 필요합니까?** 개발 단계에서는 무료 체험판으로 충분하지만, 운영 환경에서는 상용 라이선스가 필요합니다.  
- **지원되는 .NET 버전은?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **여러 DWG 파일을 한 번에 처리할 수 있나요?** 예 – 샘플 코드는 파일 이름 배열을 순회합니다.  
- **추가 예제는 어디서 찾을 수 있나요?** 아래 공식 Aspose.CAD 문서 및 포럼 링크를 확인하세요.

## **convert DWG to PNG**란 무엇인가요?
DWG(AutoCAD 도면)를 PNG 이미지로 변환하면 벡터 데이터를 래스터화하여 웹 페이지, 보고서 또는 DWG를 기본적으로 지원하지 않는 다른 애플리케이션에서 쉽게 볼 수 있습니다. OLE 개체가 포함된 경우, 변환 과정에서 이를 별도 자산으로 추출하여 저장할 수 있습니다.

## CAD 파일에서 OLE 개체를 추출해야 하는 이유
많은 DWG 도면에는 스프레드시트, 차트 또는 기타 Office 문서가 OLE 개체 형태로 삽입됩니다. 이를 추출하면 원본 데이터를 재사용하거나 보고서를 자동화하고, 임베디드 정보를 잃지 않으면서 최신 형식으로 마이그레이션할 수 있습니다.

## 전제 조건

- Aspose.CAD for .NET Library: 라이브러리가 설치되어 있는지 확인하세요. [Aspose.CAD for .NET 다운로드 페이지](https://releases.aspose.com/cad/net/)에서 다운로드할 수 있습니다.
- Document Directory: DWG 파일이 저장된 디렉터리를 설정합니다. 제공된 코드 스니펫의 `"Your Document Directory"`를 실제 경로로 교체하세요.

## 네임스페이스 가져오기

.NET 프로젝트에서 필요한 네임스페이스를 가져옵니다:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## 단계별 가이드

### 단계 1: 문서 디렉터리 설정

```csharp
string MyDir = "Your Document Directory";
```

`"Your Document Directory"`를 DWG 파일이 위치한 경로로 교체합니다.

### 단계 2: 처리할 DWG 파일 목록 만들기

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### 단계 3: PNG 변환을 위한 내보내기 옵션 구성

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

원하는 출력 해상도에 맞게 `CadRasterizationOptions`(예: `PageWidth`, `PageHeight`, `BackgroundColor`)를 조정할 수 있습니다.

### 단계 4: 각 DWG를 순회하며 변환 수행

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

이 루프 동안 라이브러리는 각 도면에 포함된 **OLE 개체를 자동으로 추출**하고 생성된 PNG에 포함합니다. 원시 OLE 스트림이 필요하면 `cadImage.OleObjects` 컬렉션에 접근하면 되며, 이는 **how to extract ole** 데이터를 프로그래밍 방식으로 얻는 편리한 방법입니다.

## 일반적인 문제 및 해결 방법

- **Missing layout name** – 예제에 사용된 `"Layout1"` 레이아웃이 원본 DWG에 존재하는지 확인하세요. 없을 경우 래스터라이저가 기본 모델 공간으로 대체됩니다.  
- **Large files cause memory pressure** – 파일을 하나씩 처리하고 `using` 구문을 사용해 `CadImage` 객체를 즉시 해제하세요.  
- **Unexpected colors** – 투명도가 필요하면 `rasterizationOptions.BackgroundColor`를 도면 배경색과 일치하도록 설정하세요.

## 자주 묻는 질문

### Q1: Aspose.CAD for .NET이 초급 및 고급 CAD 파일 모두에 적합한가요?
A1: 예, Aspose.CAD for .NET은 다양한 CAD 파일을 지원하며 초급부터 고급까지 모든 변형을 처리할 수 있습니다.

### Q2: 레이아웃별로 내보내기 옵션을 맞춤 설정할 수 있나요?
A2: 물론입니다! 튜토리얼에 표시된 대로 레이아웃별로 내보내기 옵션을 조정하여 필요에 맞게 구성할 수 있습니다.

### Q3: Aspose.CAD for .NET에 대한 자세한 문서는 어디서 찾을 수 있나요?
A3: 자세한 정보와 예제는 [Aspose.CAD for .NET documentation](https://reference.aspose.com/cad/net/)을 참고하세요.

### Q4: 무료 체험판을 이용할 수 있나요?
A4: 예, 무료 체험판으로 Aspose.CAD for .NET의 기능을 체험할 수 있습니다. 시작하려면 [this link](https://releases.aspose.com/)를 방문하세요.

### Q5: 지원을 받거나 커뮤니티와 연결하려면 어떻게 해야 하나요?
A5: 지원 및 커뮤니티 활동은 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)에서 확인할 수 있습니다.

### Q6: PNG로 변환하지 않고 CAD 파일에서 **OLE를 추출**하려면 어떻게 해야 하나요?
A6: DWG를 로드한 뒤 `CadImage.OleObjects` 컬렉션을 사용하면 각 `OleObject`를 순회하면서 원시 데이터를 파일로 저장할 수 있습니다.

## 결론

이제 Aspose.CAD for .NET을 활용해 **DWG를 PNG로 변환**하면서 **OLE 개체를 원활히 추출**하는 방법을 확인했습니다. 이 접근 방식은 시간을 절약하고 수동 복사‑붙여넣기 단계를 없애며 자동화 파이프라인에 깔끔하게 통합됩니다. 다른 래스터 형식(JPEG, BMP)으로 실험하거나 Aspose가 제공하는 풍부한 CAD 조작 기능을 탐색해 보세요.

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}