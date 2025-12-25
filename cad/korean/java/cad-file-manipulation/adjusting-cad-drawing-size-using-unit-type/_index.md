---
date: 2025-12-25
description: Aspose.CAD for Java를 사용하여 DWG를 BMP로 내보내는 방법을 배웁니다. 이 단계별 가이드는 CAD 도면
  크기를 조정하고 CAD를 BMP로 효율적으로 변환하는 방법을 보여줍니다.
linktitle: Adjusting CAD Drawing Size Using Unit Type
second_title: Aspose.CAD Java API
title: DWG를 BMP로 내보내기 – 단위 유형을 사용하여 CAD 크기 조정 (Java)
url: /ko/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG를 BMP로 내보내기 – Aspose.CAD for Java를 사용한 단위 유형으로 CAD 도면 크기 조정

## 소개

**DWG를 BMP로 내보내기**가 필요할 때, 출력 크기와 측정 단위를 제어하는 ​​것은 후속 처리나 인쇄에 필수적입니다. 이 튜토리얼에서는 `UnitType` 속성을 사용하여 측정 단위를 정의하고, Aspose.CAD for Java로 CAD 도면 크기를 조정하고 CAD를 BMP로 변환하는 방법을 배웁니다. 단계는 쉬운 언어로 설명되므로 라이브러리를 처음 사용하는 경우에도 따라 할 수 있습니다.

## 빠른 답변
- **“DWG를 BMP로 내보내기”는 무엇을 의미하나요?** DWG 도면을 BMP 래스터 이미지로 변환하는 것입니다.  
- **출력 크기를 제어하는 속성은?** `CadRasterizationOptions.setUnitType()`이 단위(예: 센티미터)를 설정합니다.  
- **코드를 실행하려면 라이선스가 필요합니까?** 평가용 무료 체험이 가능하지만, 프로덕션에서는 라이선스가 필요합니다.  
- **다른 레이아웃을 선택할 수 있나요?** 예, `setLayouts()`를 사용하여 모델 또는 종이 공간 레이아웃을 지정할 수 있습니다.  
- **지원되는 출력 형식은?** BMP 외에도 옵션 클래스를 변경하면 PNG, JPEG, TIFF 등으로 내보낼 수 있습니다.

## **DWG를 BMP로 내보내기**란?

DWG를 BMP로 내보낸다는 것은 벡터 기반 DWG 파일을 비트맵 이미지(BMP)로 래스터화한다는 의미입니다. 이는 레거시 시스템, 이미지 처리 파이프라인 또는 간단한 디스플레이 상황에서 픽셀 단위의 정확한 표현이 필요할 때 유용합니다.

## **단위 유형**으로 CAD 도면 크기를 조정하는 이유는?

단위 유형을 설정하면 스케일링 팩터를 직접 계산하지 않고도 내보낸 이미지의 물리적 크기를 제어할 수 있습니다. 이렇게 하면 비트맵이 실제 측정값(예: 센티미터)과 일치하게 되어 엔지니어링 도면 및 인쇄 문서에 필수적입니다.

## 사전 요구 사항

튜토리얼을 시작하기 전에 다음 사전 요구 사항을 준비하십시오:

- **Java 개발 환경** – JDK(8 이상)와 IDE 또는 빌드 도구(Maven/Gradle)가 설치되어 있어야 합니다.  
- **Aspose.CAD for Java 라이브러리** – Aspose.CAD 라이브러리를 다운로드하여 Java 프로젝트에 통합합니다. 라이브러리는 [여기](https://releases.aspose.com/cad/java/)에서 얻을 수 있습니다.

## 네임스페이스 가져오기

Java 코드에서 Aspose.CAD 기능에 접근하려면 필요한 네임스페이스를 포함합니다. 다음 import 문을 추가하십시오:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

이제 단위 유형을 사용해 CAD 도면 크기를 조정하는 과정을 단계별로 살펴보겠습니다:

## 단계 1: 데이터 디렉터리 정의

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

CAD 파일이 위치한 디렉터리 경로를 설정합니다.

## 단계 2: CAD 도면 로드

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

Aspose.CAD의 `Image` 클래스를 사용해 CAD 도면을 로드합니다.

## 단계 3: BMP 옵션 생성

```java
BmpOptions bmpOptions = new BmpOptions();
```

CAD 레이아웃을 BMP 형식으로 내보내기 위해 `BmpOptions` 클래스를 인스턴스화합니다.

## 단계 4: 래스터화 옵션 구성

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

`CadRasterizationOptions` 인스턴스를 생성하고 이를 `BmpOptions`에 연결하여 벡터 래스터화를 수행합니다.

## 단계 5: 단위 유형 설정

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

CAD 도면에 원하는 단위 유형을 지정합니다. 이 예에서는 **Centimeter**를 설정했으며, 이는 **CAD 도면 크기 조정** 시 내보낸 이미지 크기에 직접 영향을 줍니다.

## 단계 6: 레이아웃 설정

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

내보내기 시 고려할 레이아웃을 정의합니다. 여기서는 **"Model"** 레이아웃을 선택했지만 필요에 따라 종이 공간 레이아웃으로 전환할 수 있습니다.

## 단계 7: BMP로 내보내기

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

마지막으로 수정된 CAD 도면을 BMP 형식으로 저장합니다. 이 단계가 **DWG를 BMP로 내보내기** 워크플로를 완료하며, 앞서 구성한 크기 조정이 유지됩니다.

## 일반적인 문제 및 해결책

| 문제 | 원인 | 해결 방법 |
|------|------|-----------|
| **출력 이미지가 너무 작음** | 단위 유형이 설정되지 않았거나 기본값(픽셀) 사용 | 원하는 측정값(예: `UnitType.Centimeter`)을 `setUnitType()`으로 지정합니다. |
| **잘못된 레이아웃이 내보내짐** | 레이아웃 이름 오타 | CAD 뷰어로 레이아웃 이름을 확인하고 `setLayouts()`에 정확한 문자열을 사용합니다. |
| **라이선스 예외 발생** | 프로덕션 환경에서 유효한 라이선스 없이 실행 | FAQ에 설명된 대로 임시 또는 영구 라이선스를 적용합니다. |

## 자주 묻는 질문 (확장)

**Q: Aspose.CAD for Java를 다른 프로그래밍 언어와 함께 사용할 수 있나요?**  
A: Aspose.CAD는 주로 Java를 지원하지만, .NET 등 다른 언어용 버전도 제공됩니다.

**Q: Aspose.CAD의 라이선스 옵션이 있나요?**  
A: 네, 라이선스 옵션을 확인하고 Aspose.CAD를 [여기](https://purchase.aspose.com/buy)에서 구매할 수 있습니다.

**Q: Aspose.CAD의 무료 체험이 가능한가요?**  
A: 물론입니다. 무료 체험은 [여기](https://releases.aspose.com/)에서 이용할 수 있습니다.

**Q: Aspose.CAD for Java에 대한 지원은 어떻게 받나요?**  
A: 포괄적인 지원을 위해 Aspose.CAD 포럼을 [여기](https://forum.aspose.com/c/cad/19)에서 방문하십시오.

**Q: Aspose.CAD의 임시 라이선스를 받을 수 있나요?**  
A: 예, 임시 라이선스는 [여기](https://purchase.aspose.com/temporary-license/)에서 얻을 수 있습니다.

---

**마지막 업데이트:** 2025-12-25  
**테스트 환경:** Aspose.CAD for Java 24.10  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}