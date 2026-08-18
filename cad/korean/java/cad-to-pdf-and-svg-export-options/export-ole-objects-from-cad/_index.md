---
date: 2026-03-02
description: Java용 Aspose.CAD의 잠재력을 활용하세요. OLE 객체를 손쉽게 내보내고 **CAD를 PNG로 저장**하세요. 원활한
  CAD 데이터 관리를 위해 지금 다운로드하세요.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: CAD를 PNG로 저장 – Aspose.CAD for Java를 사용하여 OLE 객체 내보내기
url: /ko/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD를 PNG로 저장 – Aspose.CAD for Java를 사용하여 OLE 객체 내보내기

## 소개

동적인 컴퓨터 지원 설계(CAD) 세계에서 OLE(Object Linking and Embedding) 객체를 효율적으로 관리하고 추출하는 것—그리고 **CAD를 PNG로 저장**할 수 있는 능력—은 보고서 작성, 웹 미리보기 또는 보관과 같은 하위 워크플로에 필수적입니다. Aspose.CAD for Java는 강력한 코드‑우선 솔루션을 제공하여 OLE 객체를 내보내고 CAD 도면을 고품질 PNG 이미지로 변환하는 작업을 몇 줄의 코드만으로 수행할 수 있게 합니다.

## 빠른 답변
- **Aspose.CAD는 무엇을 하나요?** CAD 파일(DWG, DXF, DGN 등)을 네이티브 CAD 소프트웨어 없이 읽고, 조작하고, 변환합니다.  
- **CAD를 PNG로 저장할 수 있나요?** 예—`PngOptions`와 `CadRasterizationOptions`를 함께 사용하여 모든 레이아웃을 래스터화합니다.  
- **OLE 객체를 어떻게 내보내나요?** `Image.load`로 CAD 파일을 로드하고 OLE가 포함된 각 레이아웃을 PNG로 저장합니다.  
- **라이선스가 필요한가요?** 무료 체험판을 제공하며, 상업용 라이선스를 구매하면 평가 제한이 해제됩니다.  
- **필요한 Java 버전은?** Java 8 이상을 완전히 지원합니다.

## **CAD를 PNG로 저장**이란 무엇인가요?
CAD를 PNG로 저장한다는 것은 벡터 기반 CAD 도면을 픽셀 기반 PNG 이미지로 래스터화하는 것을 의미합니다. 이 변환은 웹 페이지, 모바일 앱 또는 문서와 같이 가볍고 모든 환경에서 볼 수 있는 형식이 필요할 때 유용합니다.

## 왜 Aspose.CAD for Java를 사용하여 **CAD를 PNG로 변환**해야 할까요?
- **CAD 설치가 필요 없음** – 라이브러리가 Java만으로 완전히 동작합니다.  
- **레이아웃 정확도 유지** – 특정 레이아웃을 선택하고 DPI를 제어하며 선 품질을 유지할 수 있습니다.  
- **배치 처리** – 간단한 루프로 여러 파일을 순회합니다.  
- **OLE 객체 내보내기** – DWG/DXF 파일에 포함된 OLE 콘텐츠가 자동으로 PNG 출력에 렌더링됩니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 준비되어 있는지 확인하십시오:

- **Java 환경** – 머신에 Java 개발 환경이 설정되어 있는지 확인하십시오.  
- **Aspose.CAD for Java** – Aspose.CAD for Java 라이브러리를 다운로드하고 설치하십시오. 라이브러리는 [download link](https://releases.aspose.com/cad/java/)에서 찾을 수 있습니다.  
- **CAD 파일** – 내보내려는 OLE 객체가 포함된 CAD 파일을 준비하십시오.

## 네임스페이스 가져오기

시작하려면 Java 프로젝트에 필요한 네임스페이스를 가져오십시오. 이러한 네임스페이스는 Aspose.CAD를 사용하여 CAD 파일을 작업하는 데 필요한 핵심 클래스와 기능을 제공합니다.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

이제 CAD에서 OLE 객체를 내보내는 과정을 여러 단계로 나누어 살펴보겠습니다:

## **CAD를 PNG로 저장**하고 OLE 객체를 내보내는 방법

### 1단계: 문서 디렉터리 설정

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

`"Your Document Directory"`를 CAD 파일이 들어 있는 디렉터리 경로로 교체하십시오.

### 2단계: CAD 파일 이름 정의

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

`files` 배열에 처리하려는 CAD 파일 이름을 지정하십시오.

### 3단계: PNG 내보내기 옵션 설정

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

벡터 래스터화 및 레이아웃 설정을 포함한 PNG 내보내기 옵션을 구성합니다. 이러한 옵션을 통해 원하는 품질로 **CAD를 PNG로 변환**할 수 있습니다.

### 4단계: CAD 파일 순회

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

지정된 각 CAD 파일을 순회하면서 Aspose.CAD로 로드하고 OLE 객체를 PNG 이미지로 저장합니다. 이 루프는 **DWG를 PNG로 대량 변환**하는 간단한 방법을 보여줍니다.

## 일반적인 문제 및 해결책

| 문제 | 원인 | 해결책 |
|-------|-------|----------|
| **빈 PNG 출력** | 레이아웃 이름 불일치 | `\"Layout1\"` 레이아웃 이름이 원본 DWG에 존재하는지 확인하십시오. |
| **OLE 그래픽 누락** | OLE 객체가 다른 레이아웃에 저장됨 | `rasterizationOptions.setLayouts(...)`에 모든 관련 레이아웃을 포함하십시오. |
| **대용량 파일에서 메모리 부족 오류** | 높은 DPI 설정 | `rasterizationOptions.setResolution(...)`으로 DPI를 낮추거나 파일을 하나씩 처리하십시오. |

## 자주 묻는 질문

**Q: Aspose.CAD가 모든 CAD 파일 형식과 호환되나요?**  
A: Aspose.CAD는 DWG, DXF, DGN 등을 포함한 다양한 CAD 형식을 지원합니다. 전체 목록은 [documentation](https://reference.aspose.com/cad/java/)을 참조하십시오.

**Q: OLE 객체의 내보내기 설정을 맞춤화할 수 있나요?**  
A: 예, Aspose.CAD는 내보내기 설정을 맞춤화할 수 있는 다양한 옵션을 제공하여 요구 사항에 맞게 출력을 조정할 수 있습니다.

**Q: Aspose.CAD의 무료 체험판이 있나요?**  
A: 예, [here](https://releases.aspose.com/)에서 무료 체험판을 받아 Aspose.CAD의 기능을 확인할 수 있습니다.

**Q: Aspose.CAD 커뮤니티 지원은 어디서 받을 수 있나요?**  
A: 도움을 받거나 경험을 공유하려면 [forum](https://forum.aspose.com/c/cad/19)에서 Aspose.CAD 커뮤니티에 참여하십시오.

**Q: Aspose.CAD 라이선스는 어떻게 구매하나요?**  
A: 개발 요구에 맞는 라이선스를 구매하려면 [purchase page](https://purchase.aspose.com/buy)를 방문하십시오.

## 결론

이와 같이 간단하면서도 강력한 단계들을 통해 Aspose.CAD for Java를 사용하여 CAD 파일에서 OLE 객체를 내보내면서 **CAD를 PNG로 저장**할 수 있습니다. 이 다재다능한 도구는 개발자가 CAD 데이터를 효율적으로 관리하도록 지원하여 CAD 애플리케이션 개발 및 하위 이미지 기반 워크플로에 새로운 가능성을 열어줍니다.

---

**마지막 업데이트:** 2026-03-02  
**테스트 환경:** Aspose.CAD for Java 24.12  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}