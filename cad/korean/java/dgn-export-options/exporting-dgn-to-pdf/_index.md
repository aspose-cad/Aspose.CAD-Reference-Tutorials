---
date: 2026-05-04
description: Aspose.CAD for Java를 사용하여 DGN을 AutoCAD PDF로 내보내 CAD PDF 파일을 변환하는 방법을
  배워보세요. 맞춤형 PDF 크기와 옵션을 제공하는 단계별 가이드.
keywords:
- convert cad pdf
- how to export dgn
- customize pdf size
- aspose cad download
- set pdf options
linktitle: AutoCAD 형식의 DGN을 PDF로 내보내기
second_title: Aspose.CAD Java API
title: CAD PDF 변환 – Aspose.CAD for Java를 사용한 DGN에서 AutoCAD PDF로 손쉬운 내보내기
url: /ko/java/dgn-export-options/exporting-dgn-to-pdf/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD PDF 변환: Aspose.CAD for Java를 사용한 DGN에서 AutoCAD PDF 내보내기

## 소개

DGN 소스에서 직접 **convert CAD PDF** 파일을 변환해야 한다면, 올바른 곳에 오셨습니다. 이 튜토리얼에서는 Aspose.CAD for Java를 사용하여 DGN 파일을 AutoCAD 호환 PDF로 내보내는 방법을 단계별로 안내합니다. 사용자 정의 페이지 크기 설정, 특정 레이아웃 선택, PDF 출력 미세 조정 방법을 확인할 수 있으며, 모두 프로젝트에 바로 적용할 수 있는 명확한 단계별 코드와 함께 제공합니다.

## 빠른 답변
- **What does “convert CAD PDF” mean?** CAD 소스 파일(DGN 등)을 벡터 데이터와 레이아웃 정확성을 유지하는 PDF로 변환하는 것을 의미합니다.  
- **Which library handles the conversion?** Aspose.CAD for Java는 이 작업을 위한 신뢰할 수 있는 라이선스‑무료 체험판을 제공합니다.  
- **Do I need a license for development?** 무료 체험판은 테스트에 사용할 수 있으며, 상용 사용을 위해서는 상업용 라이선스가 필요합니다.  
- **Can I customize the PDF size?** 예 – `CadRasterizationOptions`를 사용하면 페이지 너비, 높이 및 스케일을 설정할 수 있습니다.  
- **How many lines of code are required?** PDF를 로드, 구성 및 저장하는 데 20줄 미만의 Java 코드가 필요합니다.

## “convert CAD PDF”란 무엇인가요?
CAD PDF 변환은 원본 CAD 도면(예: DGN)을 가져와 원래의 벡터 그래픽, 레이어 및 레이아웃 정보를 유지하는 PDF를 생성하는 것을 의미합니다. 생성된 PDF는 CAD 소프트웨어 없이도 모든 장치에서 볼 수 있어 공유, 인쇄 또는 보관에 이상적입니다.

## CAD PDF 변환에 Aspose.CAD for Java를 사용하는 이유
- **Full format support** – DGN, DWG, DXF 등 다양한 형식을 지원합니다.  
- **No external dependencies** – 순수 Java이며, 네이티브 DLL이 필요 없습니다.  
- **Fine‑grained control** – 내보낼 레이아웃 선택, 사용자 정의 페이지 크기 설정, 래스터화 품질 제어가 가능합니다.  
- **Scalable for batch jobs** – 루프에서 수십 개의 파일을 로드하고 저장할 수 있어 오버헤드가 최소화됩니다.

## 사전 요구 사항
시작하기 전에 다음 항목을 준비하십시오:

- **Aspose.CAD Library** – [여기](https://releases.aspose.com/cad/java/)에서 다운로드하십시오.  
- **Document Directory** – 입력 DGN 파일과 출력 PDF가 저장될 로컬 폴더입니다.

## 패키지 가져오기
Java 프로젝트에서 Aspose.CAD 기능에 접근하기 위해 필요한 패키지를 가져옵니다:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

이제 예제 코드를 여러 단계로 나눠 살펴보겠습니다:

## 단계 1: 파일 경로 정의 (dgn 내보내기 방법)

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

`"Your Document Directory"`를 파일이 위치한 실제 경로로 교체하십시오.

## 단계 2: DGN 이미지 로드

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Aspose.CAD를 사용하여 DGN 파일을 로드합니다.

## 단계 3: PDF 내보내기 옵션 설정 (PDF 크기 맞춤, 옵션 설정)

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Export specific views
options.setVectorRasterizationOptions(vectorOptions);
```

여기서는 페이지 크기, 자동 스케일링 및 최종 PDF에 포함할 특정 DGN 레이아웃(뷰)을 포함한 PDF 내보내기 옵션을 정의합니다.

## 단계 4: PDF 파일 저장

```java
objImage.save(outFile, options);
```

내보낸 PDF 파일을 저장합니다. `save` 메서드는 이전 단계에서 구성한 모든 옵션을 적용합니다.

추가로 변환하려는 DGN 파일에 대해 이 단계를 반복하십시오. 축하합니다! Aspose.CAD for Java를 사용하여 DGN 파일을 AutoCAD 형식 PDF로 내보내 **convert CAD PDF**를 성공적으로 수행했습니다.

## 일반적인 문제 및 해결책
| 문제 | 발생 원인 | 해결 방법 |
|-------|----------------|-----|
| **File not found** | `dataDir` 경로가 올바르지 않음 | 폴더 경로를 다시 확인하고 DGN 파일이 존재하는지 확인하십시오. |
| **Blank pages in PDF** | `AutomaticLayoutsScaling`이 `false`로 설정되었거나 레이아웃 ID가 누락됨 | `setAutomaticLayoutsScaling(true)`를 유지하고 레이아웃 이름(`"1","2",…`)을 확인하십시오. |
| **Low‑resolution output** | 기본 래스터화 DPI가 낮음 | `vectorOptions.setResolution(300);`을 사용하여 품질을 높이세요(`setVectorRasterizationOptions` 전에 추가). |
| **License exception** | 프로덕션 환경에서 유효한 라이선스 없이 실행 | Aspose 문서에 설명된 대로 임시 또는 구매한 라이선스를 적용하십시오. |

## 자주 묻는 질문 (추가)

**Q: 다중 레이아웃 DGN 파일에서 단일 레이아웃만 내보낼 수 있나요?**  
A: 예 – `vectorOptions.setLayouts(new String[] { "2" });`에 원하는 레이아웃 ID를 지정하면 됩니다.

**Q: 결과 PDF에 폰트를 포함시킬 수 있나요?**  
A: 벡터 데이터가 래스터화될 때 Aspose.CAD가 필요한 폰트를 자동으로 포함합니다; 필요하면 `PdfOptions`를 통해 폰트 포함을 제어할 수도 있습니다.

**Q: 여러 DGN 파일을 배치로 처리하려면 어떻게 해야 하나요?**  
A: 파일 이름 목록을 순회하는 `for` 루프 안에 단계를 넣고 각 반복에서 동일한 `PdfOptions` 인스턴스를 재사용하면 됩니다.

**Q: 라이브러리가 비밀번호로 보호된 PDF를 지원하나요?**  
A: 예 – `options.setPassword("yourPassword");`를 사용해 `PdfOptions` 객체에 비밀번호를 설정할 수 있습니다.

**Q: 더 많은 예제를 어디서 찾을 수 있나요?**  
A: 공식 Aspose.CAD 문서와 샘플 저장소에 다양한 추가 시나리오가 포함되어 있습니다.

## FAQ (원본)

### Q1: Aspose.CAD가 모든 CAD 파일 형식과 호환되나요?
A1: 예, Aspose.CAD는 다양한 CAD 형식을 지원하여 여러 파일 유형을 처리할 수 있는 다재다능함을 제공합니다.

### Q2: PDF 내보내기 설정을 맞춤화할 수 있나요?
A2: 물론입니다. 튜토리얼에 표시된 대로 페이지 크기와 레이아웃 등 옵션을 요구 사항에 맞게 조정할 수 있습니다.

### Q3: 추가 지원이나 도움을 어디서 받을 수 있나요?
A3: 커뮤니티 지원 및 토론을 위해 [Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)을 방문하십시오.

### Q4: 무료 체험판이 있나요?
A4: 예, 무료 체험판은 [여기](https://releases.aspose.com/)에서 이용할 수 있습니다.

### Q5: 임시 라이선스를 어떻게 얻을 수 있나요?
A5: 임시 라이선스는 [여기](https://purchase.aspose.com/temporary-license/)에서 받으세요.

## 결론

이 튜토리얼에서는 Aspose.CAD for Java를 활용하여 **convert CAD PDF** 파일을 변환하는 방법을 살펴보았습니다. 몇 줄의 코드만으로 DGN 도면을 로드하고 PDF 내보내기 옵션을 미세 조정하여 공유 또는 보관에 적합한 고품질 PDF를 생성할 수 있습니다. 프로젝트 요구에 맞게 다양한 페이지 크기, 레이아웃 또는 배치 처리를 자유롭게 실험해 보세요.

---

**마지막 업데이트:** 2026-05-04  
**테스트 환경:** Aspose.CAD for Java 24.12  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}