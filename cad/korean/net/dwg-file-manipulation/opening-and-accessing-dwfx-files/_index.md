---
date: 2026-04-09
description: Aspose.CAD for .NET를 사용하여 C#에서 DWFX 파일을 로드하고 CAD를 PDF로 변환하는 방법을 배워보세요.
  원활한 통합을 위한 단계별 가이드.
keywords:
- load dwfx file c#
- c# convert cad to pdf
- aspose.cad dwfx
linktitle: C#에서 DWFX 파일 열기 및 액세스
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Aspose.CAD 가이드를 사용하여 C#에서 DWFX 파일 로드하는 방법
url: /ko/net/dwg-file-manipulation/opening-and-accessing-dwfx-files/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWFX 파일을 C#에서 Aspose.CAD로 로드하는 방법 가이드

## 소개

DWFX 파일을 **C#에서 로드**하고 PDF로 변환해야 한다면, 바로 이곳이 정답입니다. 이 튜토리얼에서는 Aspose.CAD for .NET을 사용해 DWFX 도면을 열고, 래스터화 옵션을 설정한 뒤, 최종적으로 **c# convert CAD to PDF** 하는 정확한 단계를 차례대로 안내합니다. 데스크톱 유틸리티든 웹 서비스든 접근 방식은 동일하며, Aspose.CAD가 지원하는 모든 .NET 버전에서 작동합니다.

## 빠른 답변
- **필요한 라이브러리는?** Aspose.CAD for .NET  
- **DWFX를 PDF로 변환할 수 있나요?** 예 – `CadRasterizationOptions`를 설정하고 `PdfOptions`를 사용하면 됩니다.  
- **지원되는 .NET 버전은?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **테스트용 라이선스가 필요합니까?** 개발 단계에서는 무료 체험판으로 가능하지만, 운영 환경에서는 영구 라이선스가 필요합니다.  
- **코드 실행 시간은 얼마나 걸리나요?** 일반적인 DWFX 파일은 최신 CPU에서 1초 미만에 로드 및 변환됩니다.

## DWFX 파일이란?

DWFX(Design Web Format XPS)는 CAD 도면을 XML 기반으로 표현한 형식으로, 브라우저 및 다양한 뷰어에서 렌더링할 수 있습니다. 벡터 데이터를 저장하므로 상세 손실 없이 고품질 PDF 변환에 이상적입니다.

## C#에서 DWFX 파일을 로드하기 위해 Aspose.CAD를 사용하는 이유

* **전체 형식 지원** – Aspose.CAD는 DWFX를 포함해 수십 가지 CAD 형식을 이해합니다.  
* **외부 종속성 없음** – 순수 .NET 구현으로 AutoCAD 등 네이티브 구성 요소가 필요 없습니다.  
* **간편한 래스터‑벡터 변환** – 몇 줄의 코드만으로 래스터 이미지와 벡터 PDF를 자유롭게 전환할 수 있습니다.  

## 사전 요구 사항

코드 작성을 시작하기 전에 다음을 준비하세요:

1. **Aspose.CAD for .NET**이 설치되어 있어야 합니다. [여기](https://releases.aspose.com/cad/net/)에서 다운로드할 수 있습니다.  
2. DWFX 파일이 들어 있는 폴더와 출력 파일을 저장할 폴더의 전체 경로를 확인하세요.

## C#에서 DWFX 파일을 로드하는 방법

아래는 단계별 가이드입니다. 각 단계마다 간단한 설명과 복사해서 사용할 수 있는 정확한 코드 블록이 제공됩니다.

### 네임스페이스 가져오기

```csharp
using Aspose.CAD.ImageOptions;
using System;
```

이 네임스페이스들은 CAD 파일 로드와 래스터화 및 PDF 출력에 필요한 `Image` 클래스와 옵션들을 제공합니다.

### 단계 1: 소스 및 출력 디렉터리 설정

```csharp
string SourceDir = "Your Document Directory";
string OutputDir = "Your Document Directory";
```

`"Your Document Directory"`를 DWFX 파일이 위치한 경로와 PDF를 저장할 경로로 교체하세요.

### 단계 2: DWFX 파일 로드

```csharp
using (Image cadDrawing = Image.Load(SourceDir + "Tyrannosaurus.dwfx"))
```

`Image.Load`는 DWFX 파일을 Aspose.CAD가 처리할 수 있는 `Image` 객체로 읽어들입니다. `"Tyrannosaurus.dwfx"`를 실제 도면 파일명으로 바꾸세요.

### 단계 3: 래스터화 옵션 구성

```csharp
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = cadDrawing.Size.Width;
rasterizationOptions.PageHeight = cadDrawing.Size.Height;
```

래스터화 옵션은 결과 페이지의 크기를 정의합니다. 원본 도면 크기를 사용하면 정확한 비율을 유지할 수 있습니다.

### 단계 4: PDF로 저장 (c# convert CAD to PDF)

```csharp
PdfOptions CADf = new PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
cadDrawing.Save(OutputDir + "OpenDwfxFile_out.pdf", CADf);
```

여기서 **c# convert CAD to PDF**를 수행합니다. 래스터화 설정을 `PdfOptions` 객체에 연결하고 `Save`를 호출하면 됩니다. 출력 파일은 지정한 폴더에 저장됩니다.

### 단계 5: 성공 메시지 표시

```csharp
Console.WriteLine("OpenDwfxFile executed successfully");
```

간단한 콘솔 메시지를 통해 변환이 오류 없이 완료되었음을 알릴 수 있습니다.

## 일반적인 문제 및 팁

* **파일을 찾을 수 없음** – `SourceDir` 경로를 다시 확인하고 파일 이름이 정확히 일치하는지(대소문자 포함) 확인하세요.  
* **빈 PDF** – DWFX 파일에 실제 벡터 데이터가 포함되어 있는지 확인하세요; 일부 내보내기 도구는 빈 도면을 생성할 수 있습니다.  
* **성능** – 매우 큰 도면의 경우 `PageWidth`/`PageHeight`를 줄이거나 `CadRasterizationOptions`에서 `Resolution`을 낮추는 것을 고려하세요.

## 자주 묻는 질문

### Q1: Aspose.CAD for .NET이 모든 DWFX 파일과 호환되나요?

A1: Aspose.CAD for .NET은 DWFX를 포함한 다양한 CAD 형식을 지원합니다. 다만 특정 호환성 세부 사항은 문서를 확인하는 것이 좋습니다.

### Q2: Aspose.CAD for .NET 문서는 어디서 찾을 수 있나요?

A2: 문서는 [여기](https://reference.aspose.com/cad/net/)에서 확인할 수 있습니다.

### Q3: 구매 전에 Aspose.CAD for .NET을 체험해볼 수 있나요?

A3: 예, 무료 체험 버전을 [여기](https://releases.aspose.com/)에서 다운로드할 수 있습니다.

### Q4: Aspose.CAD for .NET 임시 라이선스를 어떻게 얻나요?

A4: 임시 라이선스는 [여기](https://purchase.aspose.com/temporary-license/)에서 발급받을 수 있습니다.

### Q5: 지원이 필요하거나 추가 질문이 있나요?

A5: 도움을 원하시면 [Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)에서 문의하세요.

### Q6: 여러 DWFX 파일을 일괄 처리할 수 있나요?

A6: 물론 가능합니다. 디렉터리의 파일들을 순회하는 `foreach` 루프 안에 로드 및 저장 로직을 넣으면 됩니다.

### Q7: 변환 시 레이어와 색상이 유지되나요?

A7: 원본 DWFX에 레이어와 색상 정보가 포함되어 있다면 PDF에서도 해당 벡터 정보가 보존됩니다.

---

**Last Updated:** 2026-04-09  
**Tested With:** Aspose.CAD for .NET 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}