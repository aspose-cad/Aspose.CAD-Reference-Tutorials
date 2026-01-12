---
date: 2026-01-12
description: Aspose.CAD for Java를 사용하여 DWG 파일에서 자동 코드 페이지 감지를 무시하고 CAD를 PDF로 내보내는
  방법을 배웁니다. 인코딩 및 잘못된 CIF/MIF를 처리합니다.
linktitle: Override Automatic Code Page Detection in DWG Files
second_title: Aspose.CAD Java API
title: CAD를 PDF로 내보내기 – Java로 DWG 파일의 자동 코드 페이지 감지를 무시하기
url: /ko/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD를 PDF로 내보내기 – DWG 파일에서 자동 코드 페이지 감지를 Java로 무시하기

## 소개

이 포괄적인 가이드에서는 DWG 파일에서 텍스트를 손상시킬 수 있는 자동 코드 페이지 감지를 무시하면서 **CAD를 PDF로 내보내는 방법**을 알아볼 수 있습니다. Aspose.CAD for Java는 인코딩에 대한 세밀한 제어를 제공하여 잘못된 CIF/MIF 데이터를 복구하고 신뢰할 수 있는 PDF 출력을 생성합니다. 배치 변환기를 구축하든 더 큰 Java 애플리케이션에 CAD 처리를 통합하든, 아래 단계가 전체 워크플로우를 안내합니다.

## 빠른 답변
- **“override code page”가 무엇을 의미하나요?** Aspose.CAD가 추측하는 대신 특정 문자 인코딩을 사용하도록 강제합니다.
- **DWG를 직접 PDF로 내보낼 수 있나요?** 예 – 올바른 코드 페이지를 설정한 후 CAD 이미지를 PDF로 저장할 수 있습니다.
- **일본어 텍스트에 어떤 인코딩이 작동하나요?** `CodePages.Japanese`와 `MifCodePages.Japanese`가 적절한 선택입니다.
- **프로덕션 사용에 라이선스가 필요합니까?** 상업용 라이선스가 필요하며, 테스트용 임시 라이선스를 사용할 수 있습니다.
- **필요한 Aspose.CAD 버전은 무엇인가요?** `LoadOptions`와 `PdfOptions`를 지원하는 최신 버전이면 됩니다.

## “CAD를 PDF로 내보내기”란 무엇인가요?
CAD를 PDF로 내보내면 벡터 기반 CAD 도면을 널리 지원되는 고정 레이아웃 문서 형식으로 변환합니다. 생성된 PDF는 선 작업, 레이어 및 텍스트를 보존하면서 도면을 쉽게 공유, 인쇄 또는 다른 애플리케이션에 삽입할 수 있게 합니다.

## 왜 자동 코드 페이지 감지를 무시해야 할까요?
DWG 파일은 종종 레거시 코드 페이지를 사용해 텍스트를 저장합니다. Aspose.CAD의 자동 감지는 이러한 바이트를 오해하여 깨진 문자를 초래할 수 있습니다. 코드 페이지를 수동으로 지정하면 특히 일본어, 키릴 문자, 아라비아어와 같은 비라틴 스크립트에서도 텍스트가 내보낸 PDF에 정확히 표시됩니다.

## 전제 조건
- **Java 개발 환경** – JDK 8 이상 및 선호하는 IDE.
- **Aspose.CAD for Java** – 공식 사이트에서 라이브러리를 다운로드하세요 [여기](https://releases.aspose.com/cad/java/).
- **DWG 샘플 파일** – 제공된 `SimpleEntities.dwg` 또는 변환하려는 DWG 파일을 사용하세요.

## 패키지 가져오기
Java 프로젝트에서 필요한 Aspose.CAD 클래스를 가져옵니다:

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## 단계별 가이드

### 1단계: Java 프로젝트 설정
새 Maven 또는 Gradle 프로젝트를 만들고 Aspose.CAD JAR를 클래스패스에 추가하세요. 이 단계는 IDE가 가져온 클래스를 해결할 수 있도록 보장합니다.

### 2단계: 지정된 코드 페이지로 DWG 파일 로드
Aspose.CAD에 사용할 인코딩과 손상된 CIF/MIF 데이터를 복구할지 여부를 알려줍니다.

```java
String SourceDir = "Your Document Directory";
String dwgPathToFile = SourceDir + "SimpleEntites.dwg";
LoadOptions opts = new LoadOptions();
opts.setSpecifiedEncoding(CodePages.Japanese);
opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
opts.setRecoverMalformedCifMif(false);
CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);
```

### 3단계: CAD 이미지를 PDF로 내보내기
올바른 코드 페이지가 적용되면 도면을 안전하게 내보낼 수 있습니다. `PdfOptions` 객체를 사용하면 PDF 출력(압축, 래스터화 등)을 세밀하게 조정할 수 있습니다.

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### 4단계: 성공 확인
간단한 콘솔 메시지가 예외 없이 프로세스가 완료되었음을 확인합니다.

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

필요에 따라 소스 경로와 출력 이름을 조정하여 여러 DWG 파일에 대해 이 단계를 반복할 수 있습니다.

## 일반적인 문제 및 해결책
- **여전히 깨진 문자가 나타남:** `specifiedEncoding`이 원본 DWG의 코드 페이지와 일치하는지 다시 확인하세요. 필요하면 다른 `CodePages` 열거형을 사용하십시오.
- **`cadImage.save`에서 `NullPointerException` 발생:** DWG 파일이 올바르게 로드되는지 확인하고, 경로와 파일 권한을 검증하세요.
- **PDF 크기가 큼:** `PdfOptions`에서 압축을 활성화하세요(예: `pdfOptions.setCompress(true)`).

## 자주 묻는 질문

**Q1: Aspose.CAD가 모든 버전의 DWG 파일과 호환되나요?**  
A1: Aspose.CAD는 AutoCAD 2018 및 이전 릴리스를 포함한 다양한 DWG 버전을 지원합니다.

**Q2: Aspose.CAD를 상업 프로젝트에 사용할 수 있나요?**  
A2: 예, 프로덕션 사용을 위해 상업용 라이선스가 필요합니다. 라이선스는 [여기](https://purchase.aspose.com/buy)에서 얻을 수 있습니다.

**Q3: 무료 체험 버전에 제한이 있나요?**  
A3: 체험판은 크기 및 기능 제한을 두고 있으며, 자세한 내용은 공식 문서를 참조하십시오.

**Q4: Aspose.CAD 지원을 어떻게 받을 수 있나요?**  
A4: 커뮤니티 [Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)에서 도움과 토론을 받을 수 있습니다.

**Q5: 테스트용 임시 라이선스를 받을 수 있나요?**  
A5: 예, 임시 라이선스는 [여기](https://purchase.aspose.com/temporary-license/)에서 요청할 수 있습니다.

---

**마지막 업데이트:** 2026-01-12  
**테스트 환경:** Aspose.CAD for Java 24.11 (작성 시 최신 버전)  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}