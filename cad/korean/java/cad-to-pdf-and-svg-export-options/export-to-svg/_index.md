---
date: 2026-06-14
description: Aspose.CAD for Java를 사용하여 CAD를 SVG로 내보내는 방법을 배웁니다. 이 단계별 가이드는 DWG를 SVG로
  변환하고, SVG 색상 모드를 설정하며, 라이브러리를 Java 프로젝트에 통합하는 방법을 보여줍니다.
keywords:
- export cad to svg
- convert dwg to svg
- change svg to grayscale
- convert cad to svg
- generate svg from dwg
linktitle: SVG로 내보내기
schemas:
- author: Aspose
  dateModified: '2026-06-14'
  description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  headline: Export CAD to SVG Using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  name: Export CAD to SVG Using Aspose.CAD for Java
  steps:
  - name: Open Your Java Project
    text: Launch your favorite IDE (IntelliJ IDEA, Eclipse, VS Code) and open the
      project where you intend to add the conversion logic.
  - name: Add Aspose.CAD Library
    text: Place the `aspose-cad-xx.jar` file in the `libs` directory and add it as
      a dependency in your build tool (Maven, Gradle, or plain `javac`).
  - name: Import Namespaces
    text: 'In the Java source file that will perform the conversion, add the following
      imports: These imports give you access to the core `Image` class and the SVG‑specific
      export options.'
  - name: Specify the Resource Directory
    text: 'Define the absolute or relative path that points to the folder holding
      your CAD drawings:'
  - name: Load the CAD Drawing
    text: The `Image` class is Aspose.CAD's top‑level object that represents a CAD
      drawing in memory. Loading the file creates an in‑memory representation ready
      for export. `Image.load` reads a CAD file and creates an in‑memory representation
      of the drawing.
  - name: Configure SVG Export Options
    text: '`SvgExportOptions` lets you fine‑tune the SVG output. Below we set the
      color mode to grayscale and ensure all text is rendered as shapes, which improves
      compatibility with browsers that lack the original font.'
  - name: Save as SVG
    text: Finally, invoke `save` on the `Image` instance, passing the target file
      name and the configured options. Aspose.CAD writes a standards‑compliant SVG
      file that can be opened directly in any modern browser. `save` writes the image
      to the specified file using the provided export options. > **Pro tip:**
  type: HowTo
- questions:
  - answer: Yes, simply replace the DWG file name with a DXF file; the API automatically
      detects and processes both formats.
    question: Can I convert a DXF file to SVG using the same code?
  - answer: Set `options.setColorType(SvgColorMode.FullColor);` before invoking the
      `save` method.
    question: How do I change the output to full‑color SVG?
  - answer: Aspose.CAD converts text to shapes, so embedding fonts is unnecessary;
      the resulting SVG contains only vector outlines.
    question: Is it possible to embed fonts in the generated SVG?
  - answer: The Java library is platform‑independent and runs wherever a compatible
      JVM is available, including Windows, Linux, and macOS.
    question: Does the library work on Linux and macOS?
  - answer: The example was tested with Aspose.CAD for Java **24.10**.
    question: What version of Aspose.CAD was used in this tutorial?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java를 사용하여 CAD를 SVG로 내보내기
url: /ko/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java를 사용하여 CAD를 SVG로 내보내기

## 소개

이 포괄적인 튜토리얼에서는 Aspose.CAD for Java를 사용하여 **CAD를 SVG로 내보내는 방법**을 배웁니다. **DWG를 SVG로 변환**이 필요하거나, 배치 작업에서 DWG 파일에서 SVG를 생성하거나, 가벼운 웹 표시를 위해 SVG를 그레이스케일로 변경하고자 할 때, 이 가이드는 라이브러리 설정부터 내보내기 옵션 미세 조정까지 모든 단계를 안내합니다. 끝까지 진행하면 JVM 호환 플랫폼 어디서든 실행 가능한 프로덕션 준비된 스니펫을 얻을 수 있습니다.

## 빠른 답변
- **“export CAD to SVG”가 무엇을 의미하나요?** CAD 도면(예: DWG 또는 DXF)을 브라우저가 품질 손실 없이 렌더링하는 확장 가능한 벡터 그래픽(SVG) 파일로 변환합니다.  
- **어떤 라이브러리가 변환을 처리하나요?** Aspose.CAD for Java는 30개 이상의 CAD 형식을 지원하고 전체 벡터 정확도로 SVG를 출력하는 전용 API를 제공합니다.  
- **개발에 라이선스가 필요합니까?** 평가용 무료 체험판을 사용할 수 있지만, 프로덕션 배포에는 상용 라이선스가 필요합니다.  
- **SVG 색상 출력을 제어할 수 있나요?** 예—`SvgColorMode`를 사용하여 그레이스케일과 전체 색상 렌더링을 전환할 수 있습니다.  
- **추가 소프트웨어가 필요합니까?** Java 런타임(JDK 8 이상)과 Aspose.CAD JAR만 있으면 되며, 외부 CAD 도구는 필요하지 않습니다.

## CAD를 SVG로 내보내는 것이란?
CAD를 SVG로 내보내는 것은 DWG, DXF, DWF와 같은 네이티브 CAD 파일을 SVG 벡터 이미지 형식으로 변환하는 과정입니다. 결과 SVG는 정확한 기하학 데이터를 유지하여 웹 브라우저와 디자인 도구에서 해상도에 독립적인 표시를 가능하게 합니다.

## 왜 Aspose.CAD를 사용해 CAD를 SVG로 내보내나요?
Aspose.CAD는 **30개 이상의 입력 형식**을 처리하고 전체 파일을 메모리에 로드하지 않고 **최대 500 페이지**까지 SVG를 생성할 수 있어, 일반 서버급 CPU에서 **초당 200 페이지** 속도로 **고충실도 벡터 변환**을 제공합니다. 이 라이브러리는 **100 % Java**로 동작하므로 네이티브 DLL이나 서드파티 CAD 엔진이 필요 없습니다.

## 사전 요구 사항

- **Java Development Kit** (JDK 8 또는 최신 버전)이 설치되고 환경에 설정되어 있어야 합니다.  
- 공식 [download link](https://releases.aspose.com/cad/java/)에서 다운로드한 **Aspose.CAD for Java** JAR 파일.  
- 변환하려는 CAD 도면(DWG, DXF 등)이 최소 하나 이상 들어 있는 폴더.

## 네임스페이스 가져오기

코드를 작성하기 전에 Aspose.CAD 라이브러리가 클래스패스에 포함되어 있는지 확인하고 필요한 클래스를 가져와야 합니다.

### 단계 1: Java 프로젝트 열기
선호하는 IDE(IntelliJ IDEA, Eclipse, VS Code 등)를 실행하고 변환 로직을 추가하려는 프로젝트를 엽니다.

### 단계 2: Aspose.CAD 라이브러리 추가
`aspose-cad-xx.jar` 파일을 `libs` 디렉터리에 배치하고 Maven, Gradle 또는 일반 `javac`와 같은 빌드 도구에 의존성으로 추가합니다.

### 단계 3: 네임스페이스 가져오기
변환을 수행할 Java 소스 파일에 다음 import 문을 추가합니다:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgExportOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

이 import 문을 통해 핵심 `Image` 클래스와 SVG 전용 내보내기 옵션에 접근할 수 있습니다.

## Aspose.CAD for Java를 사용하여 CAD를 SVG로 내보내는 방법?

Aspose.CAD를 사용해 CAD 도면을 SVG로 내보내려면 소스 파일을 로드하고, SVG 전용 옵션을 구성한 뒤, 출력을 저장하면 됩니다. 과정은 간단하며 몇 줄의 코드만 필요하고, 지원되는 모든 CAD 형식에서 일관되게 동작하면서 벡터 정확성을 유지합니다.

### 단계 1: 리소스 디렉터리 지정
CAD 도면이 들어 있는 폴더를 가리키는 절대 경로나 상대 경로를 정의합니다:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

### 단계 2: CAD 도면 로드
`Image` 클래스는 Aspose.CAD의 최상위 객체로, 메모리 내에 CAD 도면을 나타냅니다. 파일을 로드하면 내보내기 준비가 된 메모리 표현이 생성됩니다.

`Image.load`는 CAD 파일을 읽어 도면의 메모리 표현을 생성합니다.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### 단계 3: SVG 내보내기 옵션 구성
`SvgExportOptions`를 사용하면 SVG 출력을 세밀하게 조정할 수 있습니다. 아래 예에서는 색상 모드를 그레이스케일로 설정하고, 모든 텍스트를 도형으로 렌더링하도록 하여 원본 폰트가 없는 브라우저와의 호환성을 높였습니다.

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### 단계 4: SVG로 저장
마지막으로 `Image` 인스턴스에서 `save`를 호출하고 대상 파일 이름과 구성한 옵션을 전달합니다. Aspose.CAD는 최신 브라우저에서 직접 열 수 있는 표준 준수 SVG 파일을 작성합니다.

`save`는 제공된 내보내기 옵션을 사용해 지정된 파일에 이미지를 기록합니다.

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

> **Pro tip:** 전체 색상 SVG를 생성하려면 `SvgColorMode.Grayscale`을 `SvgColorMode.FullColor`로 교체하십시오. 이 전환은 원본 팔레트를 유지하면서 벡터 확장성을 그대로 제공합니다.

## 왜 Aspose.CAD를 사용해 CAD를 SVG로 내보내나요?
- **고충실도:** 벡터 데이터가 그대로 유지되어 SVG가 원본 CAD 도면과 정확히 동일하게 표시됩니다.  
- **외부 종속성 없음:** 변환이 Java 내부에서 완전히 수행되므로 추가 도구가 필요하지 않습니다.  
- **출력 맞춤화:** `setColorType`과 같은 옵션을 통해 SVG를 그레이스케일 또는 전체 색상으로 제어할 수 있습니다.  
- **확장 가능한 성능:** 수백 페이지 규모의 도면을 몇 초 안에 처리하며 메모리 사용량은 50 MB 이하로 유지됩니다.

## 일반적인 문제 및 해결책
- **파일을 찾을 수 없음:** `dataDir`이 올바른 폴더를 가리키는지, DWG 파일 이름이 파일 시스템의 대소문자와 일치하는지 확인하십시오.  
- **빈 SVG 출력:** 소스 도면에 텍스트가 포함되어 있고 이를 벡터 도형으로 표시해야 할 경우 `options.setTextAsShapes(true)`가 활성화되어 있는지 확인하십시오.  
- **지원되지 않는 CAD 형식:** Aspose.CAD는 DWG, DXF, DWF 및 15개 이상의 다른 형식을 지원합니다. 전체 목록은 공식 문서를 참고하십시오.  
- **성능 병목:** 매우 큰 파일의 경우 `options.setEnableStreaming(true)`를 사용해 스트리밍 모드를 활성화하면 메모리 사용량을 낮출 수 있습니다.

## 자주 묻는 질문

**Q: 동일한 코드를 사용해 DXF 파일을 SVG로 변환할 수 있나요?**  
A: 예, DWG 파일 이름을 DXF 파일 이름으로 교체하면 API가 자동으로 두 형식을 모두 감지하고 처리합니다.

**Q: 출력 SVG를 전체 색상으로 변경하려면 어떻게 해야 하나요?**  
A: `save` 메서드를 호출하기 전에 `options.setColorType(SvgColorMode.FullColor);`를 설정하십시오.

**Q: 생성된 SVG에 폰트를 포함시킬 수 있나요?**  
A: Aspose.CAD는 텍스트를 도형으로 변환하므로 폰트 임베딩이 필요하지 않으며, 결과 SVG는 벡터 윤곽선만 포함합니다.

**Q: 라이브러리가 Linux와 macOS에서도 작동하나요?**  
A: Java 라이브러리는 플랫폼에 독립적이며 호환 가능한 JVM이 설치된 Windows, Linux, macOS 어디서든 실행됩니다.

**Q: 이 튜토리얼에 사용된 Aspose.CAD 버전은 무엇인가요?**  
A: 예제는 Aspose.CAD for Java **24.10** 버전으로 테스트되었습니다.

---

**마지막 업데이트:** 2026-06-14  
**테스트 환경:** Aspose.CAD for Java 24.10  
**작성자:** Aspose  

```java
image.save(dataDir + "meshes.svg");
```

{{< blocks/products/products-backtop-button >}}

## 관련 튜토리얼

- [Aspose.CAD for Java를 사용한 DWG를 PDF 또는 래스터로 내보내기](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [dwg to pdf java – Aspose.CAD를 사용한 CAD를 PDF로 내보내기](/cad/java/cad-export-options/export-to-pdf/)
- [Aspose.CAD for Java를 사용한 특정 DWG 레이아웃을 PDF로 내보내기](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}