---
title: .NET용 Aspose.CAD를 사용하면 STL에서 PNG로 쉽게 변환할 수 있습니다.
linktitle: STL 파일을 PNG로 내보내기
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: .NET용 Aspose.CAD를 사용하여 STL 파일을 PNG로 쉽게 변환할 수 있습니다. 원활한 통합을 위한 단계별 가이드를 따르세요. 지금 다운로드하세요!
type: docs
weight: 10
url: /ko/net/stl-file-export/exporting-stl-files-to-png/
---
## 소개
CAD(컴퓨터 지원 설계)의 역동적인 세계에서는 효율적인 파일 변환이 매우 중요합니다. .NET용 Aspose.CAD는 STL 파일을 PNG로 내보내는 프로세스를 단순화하여 개발자에게 필요한 유연성과 기능을 제공하는 강력한 도구 키트입니다. 이 튜토리얼은 Aspose.CAD를 사용하여 STL에서 PNG로 원활하게 전환하는 과정을 단계별로 안내합니다.
## 전제 조건
튜토리얼을 시작하기 전에 다음 사항이 준비되어 있는지 확인하세요.
1.  .NET용 Aspose.CAD: Aspose.CAD 라이브러리를 다운로드하여 설치하세요. 당신은 그것을 찾을 수 있습니다[여기](https://releases.aspose.com/cad/net/).
2. 개발 환경: 선호하는 .NET 개발 환경을 설정합니다.
3. STL 파일: 변환할 STL 파일을 준비합니다. 이 튜토리얼에서는 "galeon.stl"이라는 예제 파일을 사용합니다.
## 네임스페이스 가져오기
프로세스를 시작하려면 .NET 애플리케이션에 필요한 네임스페이스를 가져옵니다. 이렇게 하면 STL에서 PNG로 변환하는 데 필요한 클래스와 메서드에 액세스할 수 있습니다.
```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```
## 1단계: 디렉터리 및 소스 파일 경로 정의
```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "galeon.stl";
```
"Your Document Directory"를 STL 파일이 있는 실제 디렉토리 경로로 바꾸십시오.
## 2단계: CAD 이미지 로드
```csharp
using (var cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // 이 블록 내에서 추가 단계가 실행됩니다.
}
```
이 단계에서는 STL 파일을 CAD 이미지로 로드하여 이를 조작하고 내보낼 수 있습니다.
## 3단계: 래스터화 옵션 설정
```csharp
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 100;
rasterizationOptions.PageHeight = 100;
```
기본 설정과 요구 사항에 따라 페이지 너비와 높이를 조정합니다. 이러한 설정은 내보낸 PNG의 크기를 결정합니다.
## 4단계: PNG 옵션 구성
```csharp
PngOptions pngOptions = new PngOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
```
이전 단계에서 정의한 래스터화 설정을 통합하여 PNG 옵션을 만듭니다.
## 5단계: PNG 파일 저장
```csharp
string outPath = sourceFilePath + ".png";
cadImage.Save(outPath, pngOptions);
```
PNG 파일의 출력 경로를 지정하고 제공된 옵션을 사용하여 CAD 이미지를 PNG 형식으로 저장합니다.
특정 사용 사례에 필요에 따라 이 단계를 반복하면 Aspose.CAD for .NET을 사용하여 STL 파일을 PNG로 성공적으로 내보낼 수 있습니다.
## 결론
.NET용 Aspose.CAD는 STL 파일을 PNG로 변환하는 복잡한 작업을 단순화하여 개발자에게 안정적인 툴킷을 제공합니다. 이 단계별 가이드를 따르면 이 기능을 애플리케이션에 원활하게 통합할 수 있습니다.
## 자주 묻는 질문
### Q: 내보낸 PNG의 크기를 사용자 정의할 수 있습니까?
 전적으로! 3단계에서`PageWidth` 그리고`PageHeight` 특정 요구 사항을 충족하는 값.
### Q: 테스트 목적으로 임시 라이센스를 사용할 수 있습니까?
 네, 임시 면허를 취득하실 수 있습니다[여기](https://purchase.aspose.com/temporary-license/) 테스트 및 평가를 위해.
### Q: 추가 지원이나 커뮤니티 토론은 어디서 찾을 수 있나요?
 방문하다[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 지원 및 협력 토론을 위해.
### Q: 변환이 지원되는 다른 파일 형식이 있습니까?
 네, Aspose.CAD는 STL 이외의 다양한 CAD 형식을 지원합니다. 다음을 참조하세요.[선적 서류 비치](https://reference.aspose.com/cad/net/) 포괄적인 목록을 보려면
### Q: 여러 STL 파일을 일괄 처리할 수 있나요?
틀림없이! 여러 STL 파일을 일괄 처리하기 위해 제공된 단계를 기반으로 루프를 구현합니다.