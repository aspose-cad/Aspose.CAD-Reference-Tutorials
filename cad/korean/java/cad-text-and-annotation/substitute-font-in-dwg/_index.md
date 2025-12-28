---
date: 2025-12-28
description: Aspose.CAD for Java를 사용하여 DWG 파일을 Java 프로젝트에 로드하고 기본 글꼴 이름을 설정하는 방법을
  배워보세요. 완벽한 CAD 시각화를 위한 단계별 가이드.
linktitle: Substitute Font in DWG
second_title: Aspose.CAD Java API
title: Java에서 DWG 파일을 로드하고 Aspose.CAD로 글꼴을 교체하는 방법
url: /ko/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java에서 DWG 파일을 로드하고 Aspose.CAD로 글꼴 교체하기

## 소개

**Java** 애플리케이션에서 **DWG 파일을 로드**하고 도면에 세련된 모습을 부여하려면 글꼴을 교체하는 것이 빠른 해결책입니다. Aspose.CAD for Java를 사용하면 기본 텍스트 스타일을 시스템에 설치된 任意의 글꼴로 교체할 수 있어 모든 주석이 기대한 대로 표시됩니다. 이 튜토리얼에서는 DWG 파일을 Java에서 로드하고 `setPrimaryFontName` 메서드를 사용해 글꼴을 변경하는 전체 과정을 단계별로 안내합니다.

## 빠른 답변
- **필요한 라이브러리는?** Aspose.CAD for Java.  
- **Java에서 DWG 파일을 로드할 수 있나요?** 예, DWG 경로에 `Image.load()`를 호출하면 됩니다.  
- **어떤 메서드가 글꼴을 변경하나요?** `setPrimaryFontName`.  
- **프로덕션에 라이선스가 필요합니까?** 예, 상용 라이선스가 필요합니다.  
- **배치 처리도 가능한가요?** 물론입니다 – 동일한 코드를 사용해 여러 파일을 반복 처리할 수 있습니다.

## “load dwg file java”란?

Java 환경에서 DWG 파일을 로드한다는 것은 이진 CAD 데이터를 Aspose.CAD가 조작할 수 있는 `Image` 객체로 읽어들이는 것을 의미합니다. 파일이 로드되면 레이어, 스타일, 텍스트 엔터티 등에 대해 완전한 프로그래밍 접근이 가능합니다.

## DWG 파일에서 글꼴을 교체하는 이유

- **일관성:** 로컬 글꼴 설정에 관계없이 모든 협업자가 동일한 서체를 보게 됩니다.  
- **가독성:** 기본 CAD 글꼴은 화면에서 읽기 어려운 경우가 많으며, Arial과 같은 깔끔한 글꼴로 교체하면 가독성이 향상됩니다.  
- **브랜딩:** 기술 도면을 기업 스타일 가이드에 맞출 수 있습니다.

## 사전 요구 사항

- **Java Development Kit (JDK)** – 최신 버전(8 이상 권장).  
- **Aspose.CAD for Java** – [웹사이트](https://releases.aspose.com/cad/java/)에서 다운로드.  
- **샘플 DWG 파일** – 수정하려는 도면(테스트용으로 任意의 DWG 또는 DXF 파일 사용 가능).

## 네임스페이스 가져오기

Java 프로젝트에서 Aspose.CAD와 작업하기 위해 필요한 클래스를 가져옵니다. 이 임포트 구문을 통해 이미지 로드, CAD 전용 객체 및 스타일 조작에 접근할 수 있습니다.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## 글꼴 교체 단계별 가이드

### 단계 1: DWG 파일 로드 (load dwg file java)

먼저 DWG(또는 DXF) 파일 위치를 지정하고 `CadImage` 객체에 로드합니다.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **팁:** DWG 파일을 직접 다룰 경우 `srcFile` 변수의 확장자를 `.dxf`에서 `.dwg`로 바꾸면 됩니다.

### 단계 2: 스타일 테이블을 순회하며 기본 글꼴 이름 설정

각 CAD 도면에는 스타일 객체 컬렉션이 포함됩니다. 이를 순회하면서 `setPrimaryFontName` 메서드(**기본 글꼴 이름을 설정**하는 API 호출)를 사용해 글꼴을 교체합니다.

```java
for(Object style : cadImage.getStyles())
{
    // Set the font name
    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
}
```

`"Arial"`을 코드가 실행되는 머신에 설치된 任意의 글꼴 이름으로 바꿀 수 있습니다.

### 단계 3: 수정된 도면 저장

글꼴을 업데이트한 뒤 변경 사항을 새 DWG 파일에 저장하거나 원본을 덮어씁니다.

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

저장된 파일은 지정한 글꼴을 사용하게 되며, 모든 텍스트 주석이 해당 서체로 렌더링됩니다.

## 일반적인 문제와 해결책

| Issue | Solution |
|-------|----------|
| **Font not applied** | 호스트 OS에 글꼴이 설치되어 있는지, 철자가 정확히 일치하는지 확인합니다. |
| **`Image.load` throws an exception** | 파일 경로가 올바른지, 지원되는 DWG/DXF 형식인지 확인합니다. |
| **Performance slowdown on large files** | 별도 스레드에서 처리하거나 배치 작업으로 UI 차단을 방지합니다. |

## FAQ

### Q1: DWG 파일에서 글꼴 교체를 되돌릴 수 있나요?

A1: 예, 원본 DWG 파일을 다시 로드하거나 CAD 소프트웨어 내의 실행 취소 기능을 사용하면 됩니다.

### Q2: Aspose.CAD for Java에서 글꼴 교체에 제한이 있나요?

A2: 글꼴 교체 기능은 시스템에 설치된 글꼴에 따라 달라집니다. 원하는 글꼴이 접근 가능하도록 설치하거나 DWG 파일에 포함시키는 방안을 고려하세요.

### Q3: 교체 과정에서 글꼴 크기를 조정하려면 어떻게 하나요?

A3: Aspose.CAD의 스타일 속성에 접근해 폰트 크기를 원하는 값으로 수정하면 됩니다.

### Q4: 배치 프로세스에서 글꼴 교체를 자동화할 수 있나요?

A4: 예, Aspose.CAD for Java는 배치 처리를 지원합니다. 스크립트나 프로그램을 작성해 여러 DWG 파일에 대해 글꼴 교체를 자동화할 수 있습니다.

### Q5: Aspose.CAD for Java는 최신 CAD 파일 형식을 지원하나요?

A5: 예, Aspose.CAD for Java는 정기적으로 업데이트되어 최신 CAD 파일 형식을 지원합니다. 구체적인 형식 지원 여부는 릴리즈 노트를 확인하세요.

## 자주 묻는 질문

**Q: `setPrimaryFontName` 메서드는 텍스트 엔터티에만 영향을 주나요?**  
A: 스타일 테이블의 기본 글꼴을 업데이트하므로 해당 스타일을 참조하는 모든 텍스트 객체에 영향을 미칩니다.

**Q: 시스템에 설치되지 않은 사용자 정의 글꼴을 사용할 수 있나요?**  
A: Aspose.CAD는 운영 체제의 글꼴 레지스트리를 사용합니다. 사용자 정의 글꼴을 사용하려면 코드를 실행하는 머신에 해당 글꼴을 설치해야 합니다.

**Q: 특정 레이어에만 글꼴을 변경할 수 있나요?**  
A: 예, `setPrimaryFontName`을 호출하기 전에 레이어 이름으로 스타일을 필터링하면 됩니다.

**Q: DWG 2022 파일을 처리하려면 어떤 버전의 Aspose.CAD가 필요하나요?**  
A: 2025년 현재 최신 릴리스가 DWG 2022를 완벽히 지원합니다. 형식 지원 여부는 항상 최신 릴리즈 노트를 확인하세요.

**Q: 개발 환경에서 라이선스를 어떻게 처리하나요?**  
A: 테스트용으로 임시 평가 라이선스를 사용하고, 프로덕션에서는 `License.setLicense("Aspose.Total.Java.lic");`를 통해 구매한 라이선스 파일을 임베드합니다.

---

**마지막 업데이트:** 2025-12-28  
**테스트 환경:** Aspose.CAD for Java 24.11  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}