---
date: 2026-01-07
description: Aspose.CAD for Java를 사용하여 CAD를 PDF로 내보내고 DGN을 PDF로 변환하는 방법을 배웁니다. Java
  개발자를 위한 단계별 가이드.
linktitle: Export Embedded DGN
second_title: Aspose.CAD Java API
title: CAD를 PDF로 내보내기 – Aspose.CAD for Java로 내장 DGN 내보내기
url: /ko/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD를 PDF로 내보내기 – Aspose.CAD for Java를 사용한 임베디드 DGN 내보내기

## 소개

이 튜토리얼에서는 **how to export CAD to PDF**를 배우게 되며, 임베디드 DGN 파일을 고품질 PDF 문서로 변환하는 방법을 Aspose.CAD for Java를 사용해 살펴봅니다. Aspose.CAD는 Java 개발자에게 CAD 파일 조작에 대한 완전한 제어를 제공하는 강력한 라이브러리로, **convert DGN to PDF**, **convert DWG to PDF**가 필요하거나 CAD 도면을 다른 형식으로 렌더링하려는 경우에 적합합니다. 아래 단계별 가이드를 따라 하면 몇 분 안에 이 기능을 애플리케이션에 통합할 수 있습니다.

## 빠른 답변
- **What does “export CAD to PDF” mean?** CAD 도면(DWG, DGN 등)을 벡터 품질을 유지하면서 PDF 파일로 변환합니다.  
- **Which library is used?** Aspose.CAD for Java.  
- **Do I need a license?** 프로덕션에서는 라이선스가 필요하며, 무료 체험판을 사용할 수 있습니다.  
- **What are the main prerequisites?** Java 개발 환경 및 Aspose.CAD for Java JAR.  
- **Can I customize the output?** 예 – 레이아웃 선택, 래스터화 옵션 설정, PDF 설정 제어가 가능합니다.

## “export CAD to PDF”란?
CAD를 PDF로 내보낸다는 것은 DWG 또는 DGN과 같은 네이티브 CAD 파일을 원본 기하학을 충실히 재현하는 PDF 문서로 생성하는 것을 의미합니다. PDF는 CAD 소프트웨어 없이도 모든 플랫폼에서 열 수 있어 공유, 인쇄 또는 보관에 이상적입니다.

## 왜 Aspose.CAD for Java를 사용하여 DGN을 PDF로 변환합니까?
- **No external dependencies** – 순수 Java에서 동작합니다.  
- **Preserves vector data** – PDF는 어떤 확대 수준에서도 선명합니다.  
- **Fine‑grained control** – 특정 레이아웃 선택, 래스터화 DPI 설정, 글꼴 포함이 가능합니다.  
- **Enterprise‑ready** – 대용량 파일, 배치 처리 및 다양한 라이선스 옵션을 지원합니다.

## 전제 조건

시작하기 전에 다음 항목을 준비하십시오:

- **Java Development Environment** – JDK 8 이상이 설치되고 구성되어 있어야 합니다.  
- **Aspose.CAD for Java** – 최신 JAR를 [here](https://releases.aspose.com/cad/java/)에서 다운로드하십시오.

## 패키지 가져오기

프로젝트에서 필요한 클래스를 가져와야 합니다. 소스 파일에 다음 import 구문을 추가하십시오:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Aspose.CAD for Java를 사용하여 DGN을 PDF로 내보내는 방법은?

아래는 DWG 내부에 포함된 임베디드 DGN 파일을 PDF로 변환하는 정확한 단계별 워크스루입니다.

### 단계 1: 입력 및 출력 경로 설정

소스 파일이 위치한 디렉터리를 정의하고, 임베디드 DGN을 포함하고 있는 DWG를 지정하십시오.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### 단계 2: DWG 파일 로드

DWG 파일을 `Image` 객체로 로드합니다. Aspose.CAD는 임베디드 DGN 데이터를 자동으로 감지합니다.

```java
Image objImage = Image.load(fileName);
```

### 단계 3: 래스터화 옵션 구성

PDF에 포함할 레이아웃을 선택합니다. 이 예제에서는 **Model** 레이아웃만 내보냅니다.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### 단계 4: PDF 옵션 구성

래스터화 설정을 PDF 내보내기 옵션에 연결합니다.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 단계 5: PDF 파일 저장

구성된 옵션을 사용하여 PDF를 디스크에 기록합니다.

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## DWG를 PDF로 변환 – 추가 팁

소스 파일이 임베디드 DGN이 없는 일반 DWG인 경우에도 동일한 코드를 재사용할 수 있습니다 – `fileName`을 변환하려는 DWG 파일을 가리키도록 변경하면 됩니다. 래스터화 및 PDF 옵션은 동일하게 유지되어 일관된 **convert DWG to PDF** 워크플로를 제공합니다.

## 일반적인 문제 및 해결책

| Issue | Reason | Solution |
|-------|--------|----------|
| **Blank PDF output** | 레이아웃 이름 불일치 | `setLayouts`에 전달된 레이아웃 이름이 소스 파일의 레이아웃과 정확히 일치하는지(대소문자 구분) 확인하십시오. |
| **License exception** | 라이선스 없이 체험판 사용 | 이미지 로드 전에 유효한 Aspose.CAD 라이선스를 적용하십시오 (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |
| **File not found** | `dataDir` 경로 오류 | 절대 경로를 사용하거나 프로젝트 작업 디렉터리를 기준으로 상대 경로가 올바른지 확인하십시오. |
| **Low‑resolution graphics** | 기본 래스터화 DPI가 낮음 | `rasterizationOptions.setPageWidth/Height` 또는 `setResolution`을 설정하여 DPI를 높이십시오. |

## 자주 묻는 질문

**Q: Aspose.CAD for Java를 상업 프로젝트에 사용할 수 있나요?**  
A: 예, Aspose.CAD for Java는 상업용 라이브러리이며, [here](https://purchase.aspose.com/buy)에서 라이선스를 구매할 수 있습니다.

**Q: 무료 체험판을 제공하나요?**  
A: 예, Aspose.CAD for Java의 무료 체험판은 [here](https://releases.aspose.com/)에서 이용할 수 있습니다.

**Q: Aspose.CAD for Java에 대한 지원은 어떻게 받나요?**  
A: Aspose.CAD 커뮤니티 포럼([forum](https://forum.aspose.com/c/cad/19))에서 지원을 받을 수 있습니다.

**Q: 임시 라이선스가 필요하면 어떻게 하나요?**  
A: 임시 라이선스는 [here](https://purchase.aspose.com/temporary-license/)에서 얻을 수 있습니다.

**Q: 문서는 어디서 찾을 수 있나요?**  
A: 문서는 [here](https://reference.aspose.com/cad/java/)에서 확인할 수 있습니다.

## 결론

이제 **export CAD to PDF**를 수행하는 방법, 특히 Aspose.CAD for Java를 사용해 **convert DGN to PDF** 및 **convert DWG to PDF**하는 방법을 배웠습니다. 위 단계들을 따르면 Java 기반 솔루션에 원활한 CAD‑to‑PDF 변환 기능을 통합하여 추가 CAD 소프트웨어 없이도 사용자에게 고품질 PDF를 제공할 수 있습니다.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**마지막 업데이트:** 2026-01-07  
**테스트 환경:** Aspose.CAD for Java 24.12  
**작성자:** Aspose