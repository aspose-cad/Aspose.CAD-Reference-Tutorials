---
date: 2026-05-04
description: Aspose.CAD를 사용하여 Java에서 dxf를 dwg로 변환하고 기본 글꼴을 설정하는 방법을 배워보세요. 완벽한 CAD
  시각화를 위한 단계별 가이드.
keywords:
- convert dxf to dwg
- set primary font
- change dwg text style
- how to substitute font
- aspose cad licensing
linktitle: DWG에서 글꼴 교체
second_title: Aspose.CAD Java API
title: DXF를 DWG로 변환하고 DWG에서 글꼴을 변경하기 Aspose.CAD Java
url: /ko/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG 파일을 Java에서 로드하고 Aspose.CAD로 글꼴 교체하는 방법

## 소개

Java 애플리케이션에서 **convert dxf to dwg**가 필요하고 도면을 깔끔하게 만들고 싶다면, 글꼴을 교체하는 것이 빠른 해결책입니다. Aspose.CAD for Java를 사용하면 기본 텍스트 스타일을 시스템에 설치된 任意의 글꼴로 교체할 수 있어, 모든 주석이 기대한 대로 정확히 표시됩니다. 이 튜토리얼에서는 Java에서 DWG 파일을 로드하고 `setPrimaryFontName` 메서드를 사용해 글꼴을 변경하는 전체 과정을 단계별로 안내합니다.

## 빠른 답변
- **필요한 라이브러리는 무엇인가요?** Aspose.CAD for Java.  
- **Java에서 DWG 파일을 로드할 수 있나요?** Yes, simply call `Image.load()` on the DWG path.  
- **어떤 메서드가 글꼴을 변경하나요?** `setPrimaryFontName`.  
- **프로덕션에 라이선스가 필요합니까?** Yes, a commercial license is required.  
- **배치 처리가 가능한가요?** Absolutely – loop through multiple files with the same code.

## **convert dxf to dwg**란 무엇인가요?

“Convert dxf to dwg”는 DXF(Drawing Exchange Format) 파일을 많은 CAD 애플리케이션에서 사용하는 기본 DWG 형식으로 변환하는 것을 의미합니다. 변환을 통해 널리 지원되는 DXF 도면을 DWG 워크플로우로 가져온 다음, Aspose.CAD를 사용해 글꼴 교체와 같은 고급 스타일링을 적용할 수 있습니다.

## DWG 파일에서 글꼴을 교체하는 이유는?

- **일관성:** 모든 협업자가 로컬 글꼴 설정에 관계없이 동일한 서체를 보도록 보장합니다.  
- **가독성:** 일부 기본 CAD 글꼴은 화면에서 읽기 어려우며, Arial과 같은 깔끔한 글꼴로 교체하면 명확성이 향상됩니다.  
- **브랜딩:** 기술 도면을 기업 스타일 가이드와 일치시킵니다.

## 일반적인 사용 사례

| 시나리오 | 중요한 이유 |
|----------|----------------|
| **레거시 DXF 도면의 배치 변환** | 한 번에 DWG로 변환하고 기업 글꼴을 적용할 수 있습니다. |
| **클라이언트 프레젠테이션용 도면 준비** | 일관되고 가독성 높은 글꼴이 문서를 전문적으로 보이게 합니다. |
| **자동화된 CAD 파이프라인** | 글꼴 교체를 포함하면 수동 후처리 단계를 없앨 수 있습니다. |

## 전제 조건

- **Java Development Kit (JDK)** – 최신 버전(8 이상 권장) 중 하나.  
- **Aspose.CAD for Java** – [website](https://releases.aspose.com/cad/java/)에서 다운로드합니다.  
- **Sample DWG/DXF file** – 수정하려는 도면(테스트용으로 任意의 DWG 또는 DXF 파일을 사용할 수 있음).

## 네임스페이스 가져오기

Java 프로젝트에서 Aspose.CAD와 작업하기 위해 필요한 클래스를 가져옵니다. 이러한 import는 이미지 로드, CAD 전용 객체 및 스타일 조작에 접근할 수 있게 해줍니다.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## 글꼴 교체 단계별 가이드

### 1단계: DWG 파일 로드 (load dwg file java)

먼저, API가 DWG(또는 DXF) 파일이 위치한 경로를 가리키도록 하고 `CadImage` 객체에 로드합니다.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **팁:** DWG 파일을 직접 작업하는 경우 `srcFile` 변수에서 `.dxf` 확장자를 `.dwg`로 교체하세요.

### 2단계: 스타일 테이블을 순회하고 기본 글꼴 이름 설정

각 CAD 도면에는 스타일 객체 컬렉션이 포함되어 있습니다. 이를 순회하면서 `setPrimaryFontName` 메서드(**기본 글꼴 이름을 설정**하는 API 호출)를 사용해 글꼴을 교체합니다.

```java
for(Object style : cadImage.getStyles())
{
    // Set the font name
    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
}
```

`"Arial"`을 코드가 실행되는 머신에 설치된 任意의 글꼴로 변경할 수 있습니다.

### 3단계: 수정된 도면 저장

글꼴을 업데이트한 후, 변경 사항을 새로운 DWG 파일에 저장하거나 원본을 덮어씁니다.

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

저장된 파일은 이제 지정한 글꼴을 사용하며, 모든 텍스트 주석이 해당 서체로 렌더링됩니다.

## 일반적인 문제 및 해결책

| 문제 | 해결책 |
|-------|----------|
| **글꼴이 적용되지 않음** | 글꼴이 호스트 OS에 설치되어 있는지, 철자가 정확히 일치하는지 확인하십시오. |
| **`Image.load` 예외 발생** | 파일 경로가 올바른지, 파일이 지원되는 DWG/DXF 형식인지 확인하십시오. |
| **대용량 파일에서 성능 저하** | 파일을 별도 스레드에서 처리하거나 배치하여 UI 차단을 방지하십시오. |

## 자주 묻는 질문

**Q: `setPrimaryFontName` 메서드는 텍스트 엔터티에만 영향을 줍니까?**  
A: 스타일 테이블의 기본 글꼴을 업데이트하며, 해당 스타일을 참조하는 모든 텍스트 객체에 영향을 미칩니다.

**Q: 시스템에 설치되지 않은 사용자 정의 글꼴을 사용할 수 있나요?**  
A: Aspose.CAD는 운영 체제의 글꼴 레지스트리를 사용합니다. 사용자 정의 글꼴을 사용하려면 코드를 실행하는 머신에 해당 글꼴을 설치하십시오.

**Q: 단일 레이어에만 글꼴을 변경할 수 있나요?**  
A: 예, `setPrimaryFontName`을 호출하기 전에 레이어 이름으로 스타일을 필터링할 수 있습니다.

**Q: DWG 2022 파일에 필요한 Aspose.CAD 버전은 무엇인가요?**  
A: 2025년 현재 최신 릴리스가 DWG 2022를 완전히 지원합니다. 특정 형식 지원 여부는 릴리스 노트를 항상 확인하십시오.

**Q: 개발 환경에서 라이선스를 어떻게 처리하나요?**  
A: 테스트용으로 임시 평가 라이선스를 사용하십시오. 프로덕션에서는 `License.setLicense("Aspose.Total.Java.lic");`를 사용해 구매한 라이선스 파일을 삽입합니다.

---

**마지막 업데이트:** 2026-05-04  
**테스트 환경:** Aspose.CAD for Java 24.11  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}