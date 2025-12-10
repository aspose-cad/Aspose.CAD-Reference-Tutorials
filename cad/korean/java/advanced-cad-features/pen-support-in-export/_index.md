---
date: 2025-12-10
description: Aspose.CAD for Java를 사용하여 펜 맞춤 설정으로 CAD에서 PDF를 만드는 방법을 배워보세요. 이 단계별 가이드는
  CAD를 PDF로 효율적으로 내보내는 방법을 보여줍니다.
linktitle: Pen Support in Export
second_title: Aspose.CAD Java API
title: CAD에서 펜 지원을 사용해 PDF 만들기 (내보내기)
url: /ko/java/advanced-cad-features/pen-support-in-export/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 내보내기에서 펜 지원

## 소개

빠르게 변화하는 CAD 변환 세계에서 개발자는 시각적 충실도를 유지하면서 **CAD에서 PDF 만들기**가 필요합니다. Aspose.CAD for Java는 이를 간단하게 해주며, 내보내기 과정에서 선 스타일을 미세 조정할 수 있는 펜 사용자 정의와 같은 풍부한 옵션을 제공합니다. 이 가이드에서는 **CAD를 PDF로 내보내기**와 사용자 정의 펜 설정을 보여주는 완전한 실습 예제를 단계별로 살펴보며, DXF 도면에서 바로 고품질 PDF를 생성할 수 있습니다.

## 빠른 답변
- **“CAD에서 PDF 만들기”는 무엇을 의미하나요?** CAD 도면(예: DXF)을 벡터 품질을 유지한 채 PDF 문서로 변환하는 것입니다.  
- **펜 사용자 정의를 담당하는 라이브러리는 무엇인가요?** Aspose.CAD for Java의 `PenOptions` 클래스.  
- **다른 형식에도 사용할 수 있나요?** 네 – 동일한 펜 설정이 PNG, BMP, TIFF 등에도 적용됩니다.  
- **라이선스가 필요합니까?** 프로덕션 사용을 위해서는 유효한 Aspose.CAD 라이선스가 필요합니다.  
- **최소 Java 버전은 무엇인가요?** Java 8 이상.

## “CAD에서 PDF 만들기”란 무엇인가요?
CAD에서 PDF를 만든다는 것은 CAD 도면을 PDF 파일로 래스터화하거나 벡터 렌더링하는 것을 의미합니다. 이를 통해 수신자가 CAD 소프트웨어 없이도 엔지니어링 설계를 쉽게 공유·인쇄·보관할 수 있습니다.

## CAD를 PDF로 내보낼 때 펜 지원을 사용하는 이유는?
펜 지원을 사용하면 선 캡, 조인 및 두께를 제어할 수 있어 기업 브랜드나 기술 도면 표준에 맞출 수 있습니다. 기본 선 렌더링이 시각적 요구를 충족하지 못할 때 특히 유용합니다.

## 전제 조건

- **Java Development Environment** – JDK(8 이상)와 원하는 IDE 또는 빌드 도구가 설치된 환경.  
- **Aspose.CAD Library** – 공식 사이트에서 최신 JAR를 [여기](https://releases.aspose.com/cad/java/)에서 다운로드하십시오.  
- **샘플 DXF 파일** – 이 튜토리얼에서는 `conic_pyramid.dxf`를 사용합니다.

이제 준비가 되었으니 코드로 들어가 보겠습니다.

## 네임스페이스 가져오기

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.PenOptions;
import com.aspose.cad.internal.imaging.LineCap;
```

## 단계 1: 문서 디렉터리 정의

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

> **프로 팁:** `"Your Document Directory"`를 DXF 파일이 위치한 절대 경로로 교체하십시오.

## 단계 2: CAD 파일 로드

```java
String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

`Image.load` 메서드는 DXF 파일을 읽어 `CadImage` 객체를 생성하며, 이를 통해 조작할 수 있습니다.

## 단계 3: 래스터화 옵션 구성

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImage.getWidth() * 100);
rasterizationOptions.setPageHeight(cadImage.getHeight() * 100);
```

페이지 크기를 조정하여 결과 PDF의 해상도를 제어합니다. 100을 곱하면 인쇄에 적합한 고해상도 출력이 됩니다.

## 단계 4: 펜 옵션 사용자 정의

```java
PenOptions penOts = new PenOptions();
penOts.setStartCap(LineCap.Flat);
penOts.setEndCap(LineCap.Flat);
```

여기서는 펜의 시작 캡과 끝 캡을 모두 `Flat`으로 설정합니다. `LineCap`의 다른 값(`Round`, `Square` 등)을 실험하여 다양한 시각 효과를 얻을 수 있습니다.

## 단계 5: PDF 내보내기 옵션 구성

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

`PdfOptions` 객체는 래스터화 설정을 PDF 내보내기 프로세스와 연결합니다.

## 단계 6: 내보낸 PDF 저장

```java
cadImage.save((dataDir + "9LHATT-A56_generated.pdf"), pdfOptions);
```

이 코드를 실행하면 `9LHATT-A56_generated.pdf`라는 파일이 `dataDir` 폴더에 저장되며, 정의한 사용자 정의 펜 스타일이 적용됩니다.

## 일반적인 사용 사례

- **기술 문서** – 정밀한 엔지니어링 도면을 PDF 매뉴얼에 삽입.  
- **자동 보고** – 웹 서비스에서 CAD 데이터를 실시간으로 PDF로 생성.  
- **품질 관리** – 측정선이나 공차를 강조하기 위해 사용자 정의 선 캡 적용.

## 문제 해결 및 팁

- **잘못된 파일 경로** – `dataDir`이 파일 구분자(`/` 또는 `\\`)로 끝나는지 확인하십시오.  
- **라이선스 누락** – 유효한 라이선스가 없으면 라이브러리가 평가 모드로 실행되어 워터마크가 추가될 수 있습니다.  
- **예상치 못한 선 스타일** – `save`를 호출하기 전에 `PenOptions`가 설정되어 있는지 다시 확인하십시오; 그렇지 않으면 기본값이 사용됩니다.

## 자주 묻는 질문

### Q1: PDF 외의 형식에도 펜 옵션을 사용자 정의할 수 있나요?

A1: 네, 이 튜토리얼에서 보여준 펜 사용자 정의는 PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF, WMF 등 다양한 이미지 형식에 적용할 수 있습니다.

### Q2: 펜의 시작 캡과 끝 캡을 다르게 지정하려면 어떻게 해야 하나요?

A2: `PenOptions` 클래스를 활용하여 원하는 시작 캡과 끝 캡을 설정하면 선의 외관을 유연하게 정의할 수 있습니다.

### Q3: 펜 옵션을 지정하지 않으면 어떻게 되나요?

A3: 펜 옵션을 명시적으로 설정하지 않으면 시스템은 기본 펜을 사용하며, 상황에 따라 다르게 적용될 수 있습니다.

### Q4: 래스터화 옵션에 대한 특별한 고려사항이 있나요?

A4: 래스터화 옵션에서 페이지 너비와 높이를 조정하면 내보낸 이미지의 크기를 제어할 수 있습니다.

### Q5: 추가 지원이나 커뮤니티 토론을 어디서 찾을 수 있나요?

A5: 지원 및 토론을 위해 Aspose.CAD 커뮤니티 포럼을 [여기](https://forum.aspose.com/c/cad/19)에서 확인하십시오.

---

**Last Updated:** 2025-12-10  
**Tested With:** Aspose.CAD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}