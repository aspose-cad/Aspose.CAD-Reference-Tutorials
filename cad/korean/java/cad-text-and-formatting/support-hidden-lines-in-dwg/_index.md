---
date: 2026-01-02
description: 이 단계별 튜토리얼에서 Aspose.CAD for Java를 사용하여 DWG를 PDF로 내보내고, 숨은 선을 활성화하며, DWG를
  PDF로 변환하는 방법을 배워보세요.
linktitle: Export DWG as PDF with Hidden Lines Using Java
second_title: Aspose.CAD Java API
title: 숨겨진 선을 포함한 DWG를 PDF로 내보내기 – Aspose.CAD for Java
url: /ko/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG를 숨은 선으로 PDF로 내보내기 – Aspose.CAD for Java

## 소개

이 튜토리얼에서는 Aspose.CAD for Java를 사용하여 숨은 선을 보존하면서 **export DWG as PDF** 하는 방법을 배웁니다. **convert DWG to PDF**가 필요하거나, **dwg to pdf tutorial** 스타일 가이드를 만들거나, 혹은 숨은 선 지원과 함께 **save DWG as PDF**만 필요하든, 단계별로 안내해 드립니다. 끝까지 진행하면 Java 프로젝트에 바로 적용할 수 있는 사용 가능한 솔루션을 얻게 됩니다.

## 빠른 답변
- **이 튜토리얼은 무엇을 다루나요?** Aspose.CAD for Java를 사용하여 DWG를 PDF로 내보낼 때 숨은 선 렌더링을 활성화합니다.  
- **주요 작업은 무엇인가요?** `export dwg as pdf`.  
- **라이선스가 필요합니까?** 무료 체험으로 테스트할 수 있으며, 프로덕션에서는 상용 라이선스가 필요합니다.  
- **전제 조건은 무엇인가요?** Java 개발 환경, Aspose.CAD for Java 라이브러리, 그리고 DWG 파일.  
- **구현에 얼마나 걸리나요?** 기본 설정에 약 10‑15분 정도 소요됩니다.

## “export dwg as pdf”란 무엇인가요?

DWG 파일을 PDF로 내보내면 벡터 기반 CAD 도면을 포터블 문서 형식으로 변환하면서 레이어, 라인 타입 및 선택적 숨은 선 렌더링을 보존합니다. 이를 통해 CAD 소프트웨어가 없는 이해관계자와도 CAD 설계를 쉽게 공유할 수 있습니다.

## 내보낼 때 숨은 선을 활성화하는 이유는?

숨은 선은 복잡한 3D 모델을 2‑D 페이지에 보다 명확하게 표시하여 보이는 가장자리만 강조합니다. 이는 가독성을 향상시키며 엔지니어링 문서에 종종 필요합니다.

## 전제 조건

1. **Aspose.CAD for Java** – 공식 사이트에서 라이브러리를 다운로드하세요 [여기](https://releases.aspose.com/cad/java/).  
2. **DWG files** – 소스 DWG 도면을 알려진 디렉터리에 저장해 두세요.  
3. **Java development environment** – JDK 8 이상 및 선호하는 IDE(Eclipse, IntelliJ 등).  

이제 설정이 완료되었으니, 코드로 들어가 보겠습니다.

## 네임스페이스 가져오기

필요한 클래스를 가져와 CAD 이미지와 PDF 옵션을 사용할 수 있도록 합니다.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## 단계 1: 프로젝트 설정

Java 프로젝트를 생성하고 Aspose.CAD JAR를 빌드 경로에 추가합니다. 그런 다음 DWG 파일이 있는 디렉터리를 정의합니다.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **Pro tip:** 절대 경로를 사용하거나 프로젝트의 리소스 폴더를 기준으로 상대 경로를 구성하세요.

## 단계 2: DWG 파일 로드

소스 DWG 파일을 `CadImage` 객체에 로드하여 조작할 수 있게 합니다.

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## 단계 3: 래스터화 옵션 구성

포함할 레이어를 선택하고 페이지 크기를 원본 도면에 맞게 설정합니다. 여기서 레이아웃을 지정하여 숨은 선 렌더링을 활성화합니다.

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## 단계 4: PDF 옵션 설정

Aspose.CAD에 벡터 데이터를 PDF로 래스터화하도록 지시하고, 숨은 선을 숨기기 위해 “Model” 레이아웃을 사용합니다.

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## 단계 5: 결과 저장

마지막으로 DWG를 PDF 파일로 내보냅니다. 설정한 레이아웃에 따라 숨은 선이 올바르게 처리됩니다.

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **Common Pitfall:** 레이아웃을 `"Model"`로 설정하지 않으면 숨은 선을 포함한 모든 선이 PDF에서 실선으로 표시됩니다.

## 결론

이제 Aspose.CAD for Java를 사용하여 숨은 선 지원과 함께 **export DWG as PDF** 하는 완전하고 프로덕션 준비된 방법을 갖추었습니다. 이 접근 방식은 배치 처리 도구, 웹 서비스 또는 데스크톱 애플리케이션에 통합하여 CAD‑to‑PDF 변환을 자동화할 수 있습니다.

## 자주 묻는 질문

### Q1: Aspose.CAD for Java를 다른 CAD 파일 형식과 함께 사용할 수 있나요?
A1: 예, Aspose.CAD는 DWG, DXF, DWF 등 다양한 CAD 형식을 지원합니다.

### Q2: Aspose.CAD for Java에 대한 무료 체험이 있나요?
A2: 예, 무료 체험은 [여기](https://releases.aspose.com/)에서 확인할 수 있습니다.

### Q3: Aspose.CAD for Java에 대한 지원을 어떻게 받을 수 있나요?
A3: 커뮤니티 지원을 위해 Aspose.CAD 포럼을 [여기](https://forum.aspose.com/c/cad/19)에서 방문하세요.

### Q4: Aspose.CAD for Java에 대한 자세한 문서는 어디서 찾을 수 있나요?
A4: 문서는 [여기](https://reference.aspose.com/cad/java/)에서 확인하세요.

### Q5: Aspose.CAD for Java에 대한 임시 라이선스를 구매할 수 있나요?
A5: 예, 임시 라이선스는 [여기](https://purchase.aspose.com/temporary-license/)에서 얻을 수 있습니다.

### Q6: 이 방법은 헤드리스 서버 환경에서 DWG를 PDF로 변환하는 데도 작동하나요?
A6: 물론입니다. 코드가 Aspose.CAD API만 사용하기 때문에 UI 의존성이 없으며 서버‑사이드 자동화에 적합합니다.

---

**마지막 업데이트:** 2026-01-02  
**테스트 환경:** Aspose.CAD for Java 24.12  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}