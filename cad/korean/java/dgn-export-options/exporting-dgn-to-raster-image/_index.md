---
date: 2026-01-10
description: Aspose.CAD for Java를 사용하여 DGN 파일에서 JPEG를 만드는 방법을 배워보세요. 이 단계별 튜토리얼은 DGN을
  JPEG로 효율적으로 변환하는 방법을 보여줍니다.
linktitle: Exporting DGN in AutoCAD Format to Raster Image Format
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java를 사용하여 DGN에서 JPEG 만들기
url: /ko/java/dgn-export-options/exporting-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java를 사용하여 DGN에서 JPEG 만들기

## 소개

이 포괄적인 가이드에서는 몇 줄의 Java 코드만으로 **DGN에서 JPEG 만들기**를 수행합니다. 배치 변환 도구를 구축하든 CAD 도면을 웹 친화적인 이미지로 표시하든, DGN을 JPEG로 변환하는 것은 많은 엔지니어링 및 디자인 워크플로우에서 일반적인 요구 사항입니다. Aspose.CAD 라이브러리 설정부터 최종 래스터 이미지 저장까지 모든 단계를 안내하므로 바로 자신의 애플리케이션에 솔루션을 통합할 수 있습니다.

## 빠른 답변
- **필요한 라이브러리는?** Aspose.CAD for Java  
- **다른 CAD 형식을 JPEG로 변환할 수 있나요?** 예, Aspose.CAD는 많은 형식을 지원합니다 (보조 키워드 *convert cad to jpeg* 참고).  
- **프로덕션에 라이선스가 필요합니까?** 비체험용으로는 상업용 라이선스가 필요합니다  
- **지원되는 Java 버전은?** Java 8 이상  
- **일반적인 변환은 얼마나 걸리나요?** 표준 크기 도면은 보통 1초 미만입니다  

## “DGN에서 JPEG 만들기”란 무엇인가요?

DGN 파일에서 JPEG를 만든다는 것은 벡터 기반 DGN 도면을 픽셀 기반 이미지(JPEG)로 래스터화하는 것을 의미합니다. 이 과정은 시각적 정확성을 유지하면서도 브라우저, 이메일, 보고서 등에서 CAD 소프트웨어 없이 표시할 수 있는 가벼운 파일을 생성합니다.

## 왜 DGN을 JPEG로 변환하나요?

- **쉬운 공유:** JPEG는 모든 기기에서 보편적으로 볼 수 있습니다.  
- **성능:** 래스터 이미지는 웹 페이지에서 벡터 CAD 파일보다 빠르게 로드됩니다.  
- **호환성:** 많은 하위 도구(예: 보고 엔진)에서는 래스터 형식만 지원합니다.  

## 사전 요구 사항

시작하기 전에 다음이 준비되어 있는지 확인하십시오:

1. **Aspose.CAD 라이브러리** – 공식 사이트 **[여기](https://releases.aspose.com/cad/java/)**에서 다운로드하십시오.  
2. **Java Development Kit (JDK)** – 머신에 Java 8 이상이 설치되어 있어야 합니다.  
3. **IDE** – IntelliJ IDEA 또는 Eclipse와 같은 Java 호환 IDE를 사용하십시오.  

## 패키지 가져오기

Java 클래스에 필요한 import를 추가하십시오:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## 단계별 가이드

### 단계 1: DGN 파일 로드

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

*설명:* `Image.load` 메서드는 소스 DGN 파일을 읽고 이후 래스터화할 수 있는 `DgnImage` 객체를 반환합니다.

### 단계 2: JpegOptions 객체 생성

```java
ImageOptionsBase options = new JpegOptions();
```

*설명:* `JpegOptions`는 Aspose.CAD에 출력 형식이 JPEG임을 알려줍니다. 또한 래스터화 설정을 첨부할 수 있게 합니다.

### 단계 3: 래스터화 설정 구성

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

*설명:* 이 옵션들은 결과 이미지의 크기를 정의하고 스케일링 동작을 제어합니다. 목표 해상도에 맞게 `PageWidth`와 `PageHeight`를 조정하십시오.

### 단계 4: 변환된 이미지 저장

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

*설명:* `save` 메서드는 래스터화된 JPEG를 지정된 출력 스트림에 기록합니다. 이 단계가 끝나면 바로 사용할 수 있는 JPEG 파일이 생성됩니다.

> **프로 팁:** 변환 코드를 try‑with‑resources 블록으로 감싸면 스트림이 자동으로 닫히도록 할 수 있습니다.

## 일반적인 사용 사례

- **CAD 파일 브라우저용 썸네일 생성**.  
- **PDF 보고서 또는 HTML 페이지에 도면 삽입**.  
- **디자인 아카이브의 자동 배치 처리**.  

## 문제 해결 및 일반적인 함정

| 문제 | 원인 | 해결 방법 |
|-------|-------|-----|
| 빈 화면 또는 흰색 출력 이미지 | 잘못된 래스터화 옵션(예: 페이지 크기와 맞지 않게 `NoScaling`을 true로 설정) | `PageWidth`/`PageHeight`를 조정하거나 `NoScaling`을 false로 설정 |
| 대용량 DGN 파일에 대한 메모리 부족 오류 | 스트리밍 없이 매우 큰 파일을 로드함 | JVM 힙(`-Xmx`)을 늘리거나 파일을 작은 청크로 처리 |
| JPEG 품질이 충분하지 않음 | 기본 JPEG 품질이 낮음 | 저장하기 전에 `((JpegOptions)options).setQuality(100);`를 사용 |

## 자주 묻는 질문

### Q1: Aspose.CAD for Java를 다른 CAD 파일 형식과 함께 사용할 수 있나요?

A1: 예, Aspose.CAD는 다양한 형식을 지원하므로 **CAD를 JPEG로 변환** 및 기타 많은 래스터 또는 벡터 출력이 가능합니다.

### Q2: Aspose.CAD for Java에 대한 무료 체험이 있나요?

A2: 예, 무료 체험은 **[여기](https://releases.aspose.com/)**에서 이용할 수 있습니다.

### Q3: Aspose.CAD for Java 문서는 어디에서 찾을 수 있나요?

A3: 문서는 **[여기](https://reference.aspose.com/cad/java/)**에서 확인하십시오.

### Q4: Aspose.CAD for Java에 대한 지원은 어떻게 받을 수 있나요?

A4: 지원 포럼은 **[여기](https://forum.aspose.com/c/cad/19)**에서 방문하십시오.

### Q5: Aspose.CAD for Java 라이선스는 어디서 구매할 수 있나요?

A5: 라이선스는 **[여기](https://purchase.aspose.com/buy)**에서 구매할 수 있습니다.

## 결론

이제 Aspose.CAD for Java를 사용하여 **DGN에서 JPEG 만들기** 방법을 배웠습니다. 위 단계들을 따라 하면 데스크톱 도구, 웹 서비스 또는 자동 파이프라인 등 모든 Java 애플리케이션에 DGN‑to‑JPEG 변환을 원활히 통합할 수 있습니다.

---

**마지막 업데이트:** 2026-01-10  
**테스트 환경:** Aspose.CAD for Java 24.11 (작성 시 최신 버전)  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}