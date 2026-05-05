---
date: 2026-04-06
description: C#와 Aspose.CAD를 사용하여 DWG를 PDF로 변환하고 사용자 지정 텍스트를 추가하는 방법을 배웁니다. 이 단계별
  가이드는 DWG에서 PDF를 생성하고, 텍스트 엔터티를 삽입하며, DWG 텍스트 폰트를 변경하는 내용을 다룹니다.
keywords:
- convert dwg to pdf
- generate pdf from dwg
- insert text entity
- change dwg text font
- aspose cad dwg pdf
linktitle: C#에서 DWG 파일에 텍스트 추가하기
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DWG를 PDF로 변환하고 C#에서 텍스트 추가 – Aspose.CAD 튜토리얼
url: /ko/net/dwg-file-manipulation/adding-text-to-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG를 PDF로 변환하고 C#에서 텍스트 추가 – Aspose.CAD 튜토리얼

## 소개

CAD와 .NET 개발이 빠르게 변화하는 세계에서, **DWG를 PDF로 변환**하면서 사용자 정의 주석을 삽입하는 것은 흔한 요구사항입니다. 클라이언트를 위한 인쇄 가능한 도면을 생성하거나 DWG에 직접 동적 메모를 삽입해야 할 경우, Aspose.CAD는 작업을 간단하게 해줍니다. 이 튜토리얼에서는 **DWG를 PDF로 변환**, **텍스트 엔터티 추가**, 그리고 C#을 사용하여 **DWG 텍스트 폰트 변경** 방법을 배웁니다.

## 빠른 답변
- **DWG를 PDF로 변환하기에 가장 적합한 라이브러리는 무엇인가요?** Aspose.CAD for .NET  
- **변환 중에 사용자 정의 텍스트를 추가할 수 있나요?** 예 – `CadText` 엔터티를 생성하고 저장하기 전에 추가합니다.  
- **프로덕션 사용을 위해 라이선스가 필요합니까?** 상업용 라이선스가 필요하며, 무료 체험판을 사용할 수 있습니다.  
- **지원되는 .NET 버전은 무엇인가요?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **텍스트 폰트를 변경할 수 있나요?** 예, `StyleType` 및 `TextHeight`와 같은 `CadText` 속성을 조정합니다.

## ‘DWG를 PDF로 변환’이란 무엇인가요?

DWG 파일을 PDF로 변환하면 벡터 기반 CAD 도면을 널리 공유할 수 있는 장치 독립적인 문서로 바꿉니다. PDF는 원래의 기하학 및 레이어를 유지하면서 주석, 텍스트 또는 기타 메타데이터를 삽입할 수 있게 합니다. Aspose.CAD는 래스터화와 벡터 렌더링을 자동으로 처리하므로 서버에 별도의 CAD 소프트웨어가 필요하지 않습니다.

## 변환 전에 DWG에 텍스트를 추가하는 이유는?

텍스트를 DWG에 직접 삽입하면 배치, 스타일 및 레이어 할당을 완전히 제어할 수 있습니다. 파일을 나중에 PDF로 변환하면 텍스트가 정확히 배치한 위치에 표시되어 설계 의도를 유지하고 PDF 편집기에서 후처리할 필요가 없습니다.

## 전제 조건

시작하기 전에 다음을 확인하십시오:

- **Aspose.CAD 라이브러리** – [download link](https://releases.aspose.com/cad/net/)에서 다운로드하십시오.  
- **작동하는 .NET 환경** (Visual Studio 2022, .NET 6 또는 호환 가능한 버전).  
- **테스트 파일용 폴더** – 가이드 전체에서 `MyDir`이라고 부릅니다.

이제 단계별로 과정을 살펴보겠습니다.

## 네임스페이스 가져오기

필요한 `using` 문을 추가하여 Aspose.CAD 클래스를 사용할 수 있게 합니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
using Aspose.CAD.ImageOptions;
```

## 1단계: DWG 파일 로드

소스 DWG 파일을 `Image` 객체에 로드합니다. 이 객체를 통해 기본 CAD 엔터티에 접근할 수 있습니다.

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Subsequent steps will be performed inside this block
}
```

## 2단계: CadText 객체 생성 (텍스트 엔터티 삽입)

`CadText` 클래스는 DWG에서 단일 텍스트 라인을 나타냅니다. 여기서 스타일, 값, 색상, 레이어 및 위치를 설정합니다. `StyleType` 또는 `TextHeight`를 조정하여 **DWG 텍스트 폰트를 변경**할 수 있습니다.

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";          // Font/style – change to alter DWG text font
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;                    // 256 = ByLayer (you can use a specific ACI color)
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;                 // Height influences visual size
cadText.ScaleX = 0.0;
```

## 3단계: 텍스트 엔터티를 모델 스페이스에 추가

DWG 모델 스페이스는 대부분의 도면 엔터티를 포함합니다. `CadText`를 `*Model_Space` 블록에 추가하면 텍스트가 도면의 일부가 됩니다.

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## 4단계: PDF 옵션 구성 (DWG에서 PDF 생성)

DWG가 PDF로 렌더링되는 방식을 제어하는 래스터화 옵션을 설정합니다. 페이지 크기, 그리기 유형 및 레이아웃을 조정할 수 있습니다.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## 5단계: 수정된 DWG를 PDF로 저장

마지막으로 수정된 도면을 내보냅니다. 결과 PDF에는 새로 삽입된 텍스트가 포함됩니다.

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

> **Pro tip:** 고해상도 PDF가 필요하면 `PageHeight`와 `PageWidth`를 비례적으로 늘리세요.

## 일반적인 문제 및 해결책

| 문제 | 원인 | 해결책 |
|-------|--------|-----|
| PDF에 텍스트가 표시되지 않음 | 잘못된 레이어 또는 색상 ID | `LayerName`이 존재하고 `ColorId`가 눈에 보이는 색상(예: 흰색은 7)으로 설정되어 있는지 확인하십시오. |
| 텍스트가 잘못 배치됨 | 잘못된 정렬 좌표 | 도면 단위에 대한 `FirstAlignment.X/Y` 값을 확인하십시오. |
| PDF가 빈 페이지임 | 래스터화 옵션이 설정되지 않음 | `DrawType`을 `UseObjectColor` 또는 `UseObjectLineWeight`로 설정하십시오. |

## 자주 묻는 질문 (기존)

### Q1: Aspose.CAD가 모든 버전의 DWG 파일과 호환됩니까?
A1: Aspose.CAD는 다양한 DWG 파일 버전을 지원하여 여러 CAD 소프트웨어와의 호환성을 보장합니다.

### Q2: Aspose.CAD를 사용하여 단일 DWG 파일에 여러 텍스트 엔터티를 추가할 수 있나요?
A2: 예, 튜토리얼에 설명된 절차를 반복하면 DWG 파일에 여러 텍스트 엔터티를 추가할 수 있습니다.

### Q3: Aspose.CAD에서 텍스트 폰트와 스타일을 어떻게 변경할 수 있나요?
A3: `CadText` 객체의 속성을 DWG 파일에 추가하기 전에 조정하여 텍스트 폰트와 스타일을 변경할 수 있습니다.

### Q4: 상업 프로젝트에서 Aspose.CAD를 사용할 때 라이선스 고려 사항이 있나요?
A5: 예, Aspose.CAD 라이선스 조건을 준수해야 합니다. 자세한 내용은 [Aspose.CAD Purchase](https://purchase.aspose.com/buy) 를 참조하십시오.

### Q5: Aspose.CAD 관련 문의나 토론을 어디에서 할 수 있나요?
A5: 커뮤니티와 연결하고 지원을 받으려면 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 를 방문하십시오.

## 추가 FAQ

**Q: 텍스트를 추가하지 않고 DWG에서 PDF를 생성하려면 어떻게 해야 하나요?**  
A: `CadText` 생성 단계를 건너뛰고 `image.Save(...)` 호출 전에 `PdfOptions`를 직접 구성하십시오.

**Q: 프로그래밍으로 텍스트 색상을 변경할 수 있나요?**  
A: 예, `cadText.ColorId`를 특정 ACI 색상 번호(예: 빨강은 1)로 설정하십시오.

**Q: 다중 행 텍스트를 삽입할 수 있나요?**  
A: 다중 행 텍스트 블록에는 `CadMText`를 사용하십시오; 접근 방식은 `CadText`와 유사합니다.

**Q: Aspose.CAD가 여러 DWG 파일의 배치 변환을 지원하나요?**  
A: 물론입니다 – DWG 파일이 있는 디렉터리를 순회하면서 동일한 단계를 적용하고 각각을 PDF로 저장하면 됩니다.

## 결론

이제 C#과 Aspose.CAD를 사용하여 **DWG를 PDF로 변환**, **사용자 정의 텍스트 추가**, 그리고 **텍스트 모양 맞춤**을 할 수 있는 완전하고 프로덕션 준비된 워크플로우를 갖추었습니다. 이 기술은 자동 도면 생성, 보고 파이프라인, 또는 실시간으로 CAD 파일을 강화해야 하는 모든 상황에 이상적입니다.

---

**마지막 업데이트:** 2026-04-06  
**테스트 대상:** Aspose.CAD 24.11 for .NET  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}