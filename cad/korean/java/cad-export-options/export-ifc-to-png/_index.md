---
date: 2025-12-21
description: Aspose.CAD for Java를 사용하여 IFC를 PNG로 손쉽게 변환하세요. 단계별 튜토리얼을 따라보세요.
linktitle: Export IFC to PNG
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java를 사용하여 IFC를 PNG로 변환
url: /ko/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java를 사용하여 IFC를 PNG로 변환하기

## 소개

이 튜토리얼에서는 강력한 Aspose.CAD 라이브러리를 사용하여 **IFC를 PNG로 변환하는 방법**을 배웁니다. BIM 뷰어를 구축하거나, 건설 포털용 썸네일을 생성하거나, 문서 파이프라인을 자동화하는 경우 등, IFC(Industry Foundation Classes) 파일을 래스터 이미지로 변환하는 것은 일반적인 요구 사항입니다. 각 단계를 차근차근 살펴보고, 설정 뒤에 숨은 이유를 설명하며, 최상의 시각적 결과를 얻기 위한 팁을 제공합니다.

## 빠른 답변
- **필요한 라이브러리는?** Aspose.CAD for Java (무료 체험 제공).  
- **지원되는 IFC 버전?** 대부분의 IFC 2x3 및 IFC4 파일을 처리합니다.  
- **일반적인 변환 시간?** 표준 모델은 몇 초 정도이며 파일 크기에 따라 다릅니다.  
- **라이선스가 필요합니까?** 프로덕션 사용을 위해 임시 라이선스가 필요합니다.  
- **이미지 크기를 맞춤 설정할 수 있나요?** 예 – `CadRasterizationOptions`를 사용하여 너비와 높이를 설정합니다.

## “IFC를 PNG로 변환”이란 무엇인가요?
IFC를 PNG로 변환한다는 것은 3‑D 건물 모델(IFC)을 2‑D 비트맵 이미지(PNG)로 래스터화한다는 의미입니다. 이 과정은 기하학을 평면화하고 기본 시각 스타일을 적용하여, CAD 뷰어 없이도 브라우저, 보고서 또는 모바일 앱에서 표시할 수 있는 휴대용 이미지를 생성합니다.

## 왜 Aspose.CAD for Java를 사용하나요?
- **외부 CAD 소프트웨어 불필요** – 순수 Java API이며 모든 플랫폼에서 작동합니다.  
- **고품질 렌더링** – 선 굵기, 색상 및 레이어를 보존합니다.  
- **전체 제어** – 래스터화 옵션을 통해 해상도, 배경 등을 정의할 수 있습니다.  
- **간편한 라이선스** – 체험 및 임시 라이선스로 평가가 간편합니다.

## 전제 조건

시작하기 전에 다음이 준비되어 있는지 확인하세요:

- **Aspose.CAD 라이브러리** – [download link](https://releases.aspose.com/cad/java/)에서 다운로드하고 설치합니다.  
- **Java Development Kit (JDK)** – 버전 8 이상.  
- **IFC 파일이 들어 있는 폴더**.

## 네임스페이스 가져오기

Java 프로젝트에서 필요한 클래스를 가져옵니다:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## 단계별 가이드

### Step 1: IFC 파일 로드

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

여기서는 소스 IFC 파일을 `IfcImage` 객체에 로드합니다. Aspose.CAD는 IFC 구조를 자동으로 파싱하고 래스터화를 위해 준비합니다.

### Step 2: 벡터(래스터화) 옵션 설정

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

`CadRasterizationOptions`는 3‑D 기하학을 평면화하는 방식을 제어합니다. 원하는 PNG 해상도에 맞게 `PageWidth`와 `PageHeight`를 조정합니다. 값이 클수록 고해상도 이미지를 얻지만 메모리 사용량이 증가합니다.

### Step 3: PNG 내보내기 설정 구성

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

`PngOptions`는 Aspose.CAD에 PNG 파일을 출력하도록 지시하고 이전 단계에서 정의한 래스터화 설정을 연결합니다.

### Step 4: 이미지를 PNG로 저장

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

`save` 메서드는 래스터화된 이미지를 디스크에 저장합니다. 이 라인이 실행된 후에는 소스 IFC 파일과 같은 디렉터리에서 `example.png`를 찾을 수 있습니다.

## 일반적인 문제 및 해결책

| 문제 | 발생 원인 | 해결 방법 |
|------|----------|----------|
| **빈 PNG 출력** | 래스터화 옵션의 width/height가 0이거나 매우 작게 설정되었습니다. | `PageWidth`와 `PageHeight`가 양의 정수인지 확인하세요(예: 1500). |
| **레이어 또는 색상 누락** | 기본 뷰가 특정 레이어를 숨길 수 있습니다. | `vectorOptions.setRenderMode(CadRenderMode.Wireframe)`를 사용하거나 필요에 따라 API를 통해 레이어 가시성을 조정하세요. |
| **대용량 IFC 파일에서 메모리 부족 오류** | 매우 높은 해상도는 많은 RAM을 소비합니다. | 해상도를 낮추거나 모델을 섹션별로 처리하세요. |

## FAQ

### Q1: Aspose.CAD가 모든 버전의 IFC 파일과 호환되나요?
A1: Aspose.CAD는 다양한 버전의 IFC 파일을 지원합니다. 호환성 세부 사항은 [documentation](https://reference.aspose.com/cad/java/)을 참고하세요.

### Q2: 래스터화 옵션을 더 맞춤 설정할 수 있나요?
A2: 물론입니다! 고급 맞춤 옵션은 [documentation](https://reference.aspose.com/cad/java/)을 확인하세요.

### Q3: 체험 버전을 제공하나요?
A3: 예, 무료 체험 버전은 [here](https://releases.aspose.com/)에서 이용할 수 있습니다.

### Q4: Aspose.CAD의 임시 라이선스를 어떻게 얻을 수 있나요?
A4: [this link](https://purchase.aspose.com/temporary-license/)에서 임시 라이선스를 얻으세요.

### Q5: 어디에서 도움을 받거나 문제를 논의할 수 있나요?
A5: 커뮤니티 지원은 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)에서 확인하세요.

## 자주 묻는 질문 (추가)

**Q: 여러 IFC 파일을 배치로 변환할 수 있나요?**  
A: 예. 로드 및 저장 로직을 파일 경로 리스트를 순회하는 루프 안에 넣으세요.

**Q: PNG의 배경 색상을 어떻게 변경하나요?**  
A: `PngOptions`를 만들기 전에 `vectorOptions.setBackgroundColor(Color.getWhite())`(또는 원하는 `java.awt.Color`)를 설정하세요.

**Q: JPEG나 BMP와 같은 다른 래스터 형식으로 내보낼 수 있나요?**  
A: 물론입니다. `PngOptions`를 `JpegOptions` 또는 `BmpOptions`로 교체하고 형식별 설정을 조정하세요.

**Q: 변환 후 리소스를 해제해야 하나요?**  
A: 작업이 끝나면 `cadImage.dispose()`를 호출하여 네이티브 메모리를 해제하세요.

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}