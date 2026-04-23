---
date: 2026-03-21
description: Aspose.CAD for .NET를 사용하여 DWG에서 PDF를 생성하고 DWG의 일부로 DGN을 내보내는 방법을 배웁니다.
  이 가이드는 또한 DWG를 PDF로 변환하고 PDF 옵션을 설정하는 방법을 보여줍니다.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DWG에서 PDF 만들기 및 DGN을 DWG의 일부로 내보내기 – Aspose.CAD for .NET
url: /ko/net/cad-export-formats/export-dgn-as-part-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG에서 PDF 생성 및 DGN을 DWG의 일부로 내보내기 – Aspose.CAD for .NET

## 소개

DWG 파일에서 **PDF를 생성**하면서 DGN 디자인을 DWG의 일부로 포함해야 할 경우, Aspose.CAD for .NET을 사용하면 간단합니다. 이 튜토리얼에서는 전체 워크플로우를 단계별로 안내합니다: DWG 로드, 포함된 DGN 언더레이 찾기, 래스터화 옵션 구성, 최종적으로 결과를 PDF 문서로 내보내기. 배치 변환 도구, 보고 엔진, 혹은 CAD‑BIM 통합 서비스를 구축하든, 아래 단계는 견고하고 프로덕션 준비가 된 기반을 제공합니다.

## 빠른 답변
- **DWG → PDF 변환을 담당하는 라이브러리는?** Aspose.CAD for .NET  
- **PDF를 생성하면서 DGN 언더레이를 내보낼 수 있나요?** 예 – 언더레이는 `CadDgnUnderlay`를 통해 접근합니다.  
- **PDF 옵션을 설정하는 메서드는?** `PdfOptions`와 `CadRasterizationOptions`.  
- **상업적 사용에 라이선스가 필요합니까?** 예, 유효한 Aspose.CAD 라이선스가 필요합니다.  
- **지원되는 .NET 버전은?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## “DWG에서 PDF 생성”이란?

DWG 파일에서 PDF를 생성한다는 것은 벡터 도면을 래스터 또는 벡터 기반 PDF 문서로 렌더링하는 것을 의미합니다. 이 과정은 CAD 소프트웨어가 없는 이해관계자와 도면을 공유하거나, 아카이브하거나, 인쇄 가능한 보고서를 생성할 때 유용합니다. Aspose.CAD는 DWG 엔티티 파싱 작업을 처리하고 `PdfOptions`를 통해 출력에 대한 세밀한 제어를 제공함으로써 작업을 단순화합니다.

## 왜 DGN을 DWG의 일부로 내보내나요?

DGN 언더레이는 종종 MicroStation 프로젝트의 참조 기하학을 나타냅니다. DGN을 DWG와 함께 내보내면 원래 설계 컨텍스트를 보존하게 되어, 이후 사용자가 전체 도면 세트를 확인할 수 있습니다. 이는 DWG와 DGN 파일이 동시에 존재하는 다학제 프로젝트에서 특히 유용합니다.

## 전제 조건

- **Aspose.CAD for .NET** – [여기](https://releases.aspose.com/cad/net/)에서 다운로드하세요.  
- **개발 환경** – Visual Studio(최근 버전) 또는 선호하는 .NET IDE.  
- **기본 C# 지식** – C# 구문 및 .NET 프로젝트 구조에 익숙해야 합니다.

## 네임스페이스 가져오기

C# 소스 파일 상단에 필요한 `using` 지시문을 추가하세요:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 단계별 가이드

### 단계 1: 파일 경로 정의

입력 DWG 파일과 출력 PDF 이름을 설정합니다.

```csharp
// Input and Output file paths
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

### 단계 2: `PdfOptions` 인스턴스 생성 (PDF 옵션 설정)

`PdfOptions`를 사용하면 페이지 크기, 압축, 메타데이터 등 PDF 생성 방식을 제어할 수 있습니다.

```csharp
// Create an instance of PdfOptions class for exporting DWG to PDF
PdfOptions exportOptions = new PdfOptions();
```

### 단계 3: DWG 파일 로드

DWG를 `CadImage`로 로드하여 엔티티를 검사할 수 있습니다.

```csharp
// Load the existing DWG file as an image and convert it to CadImage type
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

### 단계 4: 엔티티 순회

도면의 모든 엔티티를 순회하여 DGN 언더레이를 찾습니다.

```csharp
// Iterate through each entity inside the DWG file
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

### 단계 5: 엔티티 유형 확인 (DGN 내보내기)

현재 엔티티가 DGN 언더레이인지 확인합니다.

```csharp
// Check if the entity is an image definition
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

### 단계 6: 언더레이 경로 가져오기

DGN 파일의 외부 참조 경로를 가져옵니다.

```csharp
// If it's an image definition, get the external reference to the object
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

### 단계 7: 래스터화 옵션 정의 (DWG를 PDF로 변환)

DWG가 PDF에 삽입되기 전에 어떻게 래스터화될지 구성합니다.

```csharp
// Define settings for CadRasterizationOptions object
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

### 단계 8: DWG를 PDF로 내보내기

마지막으로 렌더링된 이미지를 PDF 파일로 저장합니다.

```csharp
// Export the DWG to PDF by calling Save method
cadImage.Save(outPath, exportOptions);
```

## 일반적인 문제 및 해결책

| 문제 | 원인 | 해결 방법 |
|-------|--------|-----|
| **`Image.Load` throws “File not found”** | 경로가 잘못되었거나 파일이 없음. | 절대 경로를 사용하거나 DWG가 출력 폴더에 복사되었는지 확인하세요. |
| **Underlay path is empty** | DGN 언더레이가 포함되지 않았거나 참조가 깨짐. | DWG에 실제로 DGN 언더레이가 포함되어 있는지, 외부 DGN 파일에 접근 가능한지 확인하세요. |
| **PDF output is blank** | 래스터화 옵션이 크기 0으로 설정됨. | `PageWidth`/`PageHeight`를 조정하거나 `NoScaling = false`로 설정하세요. |
| **License exception** | 유효한 Aspose.CAD 라이선스 없이 실행. | 이미지 로드 전에 라이선스를 적용합니다: `License lic = new License(); lic.SetLicense("Aspose.CAD.lic");` |

## 자주 묻는 질문

### Q1: Aspose.CAD for .NET을 상업 프로젝트에 사용할 수 있나요?
A1: 예, 사용할 수 있습니다. 라이선스 옵션은 [여기](https://purchase.aspose.com/buy)에서 확인하세요.

### Q2: 처리할 수 있는 DWG 파일 크기에 제한이 있나요?
A2: Aspose.CAD는 대용량 DWG 파일을 지원하지만 하드웨어 제한이 적용될 수 있습니다.

### Q3: 체험판 버전이 있나요?
A3: 예, 무료 체험판은 [여기](https://releases.aspose.com/)에서 받을 수 있습니다.

### Q4: 임시 라이선스는 어떻게 얻나요?
A4: 임시 라이선스는 [여기](https://purchase.aspose.com/temporary-license/)에서 얻을 수 있습니다.

### Q5: 문제 발생 시 어디에서 도움을 받을 수 있나요?
A5: Aspose.CAD 포럼은 [여기](https://forum.aspose.com/c/cad/19)에서 방문해 지원을 받을 수 있습니다.

**Q: 추가 PDF 메타데이터(작성자, 제목 등)를 설정하려면?**  
A: `Save` 호출 전에 `exportOptions.Metadata` 속성을 사용합니다.

**Q: 여러 레이아웃을 별도의 PDF 페이지로 내보낼 수 있나요?**  
A: 예 – `CadRasterizationOptions`에서 `Layouts = new string[] { "Layout1", "Layout2" }`로 설정합니다.

**Q: Aspose.CAD가 DWG를 다른 이미지 형식으로 변환하는 것을 지원하나요?**  
A: 물론입니다. 해당 `Image.Save` 오버로드를 사용하여 PNG, JPEG, SVG 등으로 내보낼 수 있습니다.

---

**최종 업데이트:** 2026-03-21  
**테스트 환경:** Aspose.CAD 24.11 for .NET  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}