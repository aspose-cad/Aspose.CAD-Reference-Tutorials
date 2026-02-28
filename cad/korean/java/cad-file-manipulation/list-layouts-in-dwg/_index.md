---
date: 2026-02-28
description: Aspose.CAD for Java를 사용하여 DWG 파일을 읽는 방법을 배우고 DWG 파일의 레이아웃을 손쉽게 나열하십시오.
  강력한 CAD 기능을 Java 애플리케이션에 통합하세요.
linktitle: List Layouts in DWG
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java를 사용하여 DWG를 읽고 DWG의 레이아웃을 나열하는 방법
url: /ko/java/cad-file-manipulation/list-layouts-in-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java를 사용하여 DWG를 읽고 DWG에서 레이아웃 목록을 가져오는 방법

## 소개

프로그래밍 방식으로 **DWG 파일을 읽는 방법**을 찾고 있다면, Aspose.CAD for Java는 깨끗하고 크로스‑플랫폼 API를 제공하여 도면을 로드하고 파일 내부의 모든 레이아웃 이름과 같은 필요한 정보를 추출할 수 있습니다. 이 단계별 튜토리얼에서는 **DWG를 읽고** DWG(또는 DXF) 파일에 포함된 모든 레이아웃을 나열하는 방법을 보여드리며, CAD 데이터를 다루는 모든 Java 애플리케이션에 이 기능을 통합할 수 있습니다.

## 빠른 답변
- **필요한 라이브러리는?** Aspose.CAD for Java.  
- **DWG 파일을 모든 OS에서 읽을 수 있나요?** 예 – Java는 크로스‑플랫폼이므로 **Linux에서 dwg를 읽는 것**도 Windows와 동일하게 쉽습니다.  
- **샘플을 실행하려면 라이선스가 필요합니까?** 평가용 무료 체험판을 사용할 수 있으며, 프로덕션에서는 라이선스가 필요합니다.  
- **지원되는 CAD 포맷은?** DWG, DXF, DWF 등 여러 포맷.  
- **코드가 Java 8+와 호환되나요?** 전적으로 호환됩니다.

## Java에서 “DWG를 읽는 방법”이란?

DWG 파일을 읽는다는 것은 바이너리 CAD 데이터를 객체 모델로 로드하여 쿼리할 수 있게 하는 것을 의미합니다. Aspose.CAD는 복잡한 DWG 구조를 간단한 Java 클래스 뒤에 추상화하여, 필요한 정보(예: 레이아웃 이름)에 집중할 수 있게 합니다.

## DWG 파일에서 레이아웃을 나열하는 이유

DWG에는 여러 레이아웃(페이퍼 스페이스, 모델 스페이스, 사용자 정의 시트)이 포함될 수 있습니다. 레이아웃 이름을 알면 다음과 같은 작업이 가능합니다:

- 레이아웃별 보고서 생성.  
- 특정 레이아웃을 이미지 또는 PDF로 내보내기.  
- 도면의 배치 처리 자동화.  

## 사전 요구 사항

코드 작성을 시작하기 전에 다음이 준비되어 있는지 확인하십시오:

- **Aspose.CAD for Java 라이브러리** – 최신 JAR 파일을 [웹사이트](https://releases.aspose.com/cad/java/)에서 다운로드합니다.  
- **Java 개발 환경** – JDK 8 이상 및 원하는 IDE 또는 빌드 도구.

## 네임스페이스 가져오기

Java 소스 파일에서 필요한 Aspose.CAD 클래스를 가져옵니다:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadLayoutDictionary;
import com.aspose.cad.fileformats.cad.cadobjects.CadLayout;
```

## 1단계: 문서 디렉터리 설정

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

**“Your Document Directory”**를 CAD 파일이 위치한 절대 경로로 교체하십시오. Linux에서는 `/home/user/cad/`와 같은 경로를 사용할 수 있습니다.

## 2단계: DWG 파일 로드

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image image = Image.load(sourceFilePath);
CadImage cadImage = (CadImage)image;
```

`Image.load` 메서드는 파일 형식을 자동으로 감지하므로 **DWG**와 **DXF** 파일 모두에 동일한 코드를 사용할 수 있습니다.

## 3단계: 레이아웃 가져오기 및 이름 출력

```java
CadLayoutDictionary layouts = cadImage.getLayouts();
for (CadLayout layout : layouts.getValues())
{
    System.out.println("Layout " + layout.getLayoutName());
}
```

루프는 각 레이아웃 객체를 순회하면서 이름을 콘솔에 출력합니다 – **DWG를 읽고** 레이아웃 정보를 추출했는지 확인하는 간단한 방법입니다.

## Linux에서 DWG를 PDF로 변환하는 방법

특정 레이아웃을 PDF로 변환해야 할 경우, Aspose.CAD는 레이아웃을 이미지로 렌더링할 수 있으며, 이후 Aspose.PDF(또는 다른 PDF 라이브러리)를 사용해 해당 이미지를 PDF 문서에 삽입할 수 있습니다. 변환 코드는 순수 Java API이므로 Linux에서도 동일하게 동작합니다.

## 흔히 발생하는 문제 및 팁

- **잘못된 파일 경로** – `dataDir`이 OS에 맞는 구분자(`/` 또는 `\\`)로 끝나는지 확인하십시오.  
- **지원되지 않는 DWG 버전** – 최신 Aspose.CAD 버전을 사용하십시오; 오래된 DWG 버전은 변환이 필요할 수 있습니다.  
- **메모리 사용량** – 대형 도면은 많은 메모리를 소모합니다. 사용이 끝난 후 `CadImage` 객체를 해제하십시오: `cadImage.dispose();`.  
- **헤드리스 서버에서 실행** – UI 구성 요소가 필요 없으므로 그래픽 환경이 없는 Linux 서버에서도 코드가 정상 작동합니다.

## 결론

축하합니다! 이제 Aspose.CAD for Java를 사용하여 **DWG를 읽고** 레이아웃을 나열하는 방법을 알게 되었습니다. 이 기술은 특정 레이아웃을 이미지, PDF로 내보내거나 Linux에서 DWG를 PDF로 변환하는 등 보다 고급 CAD 자동화의 기반이 됩니다. 자세한 내용은 공식 [문서](https://reference.aspose.com/cad/java/)를 참고하십시오.

## 자주 묻는 질문

**Q1: Aspose.CAD for Java를 다른 CAD 파일 포맷과 함께 사용할 수 있나요?**  
A1: 예, Aspose.CAD는 DWG, DXF, DWF 등 다양한 CAD 포맷을 지원합니다.

**Q2: Aspose.CAD for Java의 무료 체험판을 제공하나요?**  
A2: 예, [여기](https://releases.aspose.com/)에서 무료 체험판을 받을 수 있습니다.

**Q3: Aspose.CAD for Java에 대한 커뮤니티 지원은 어디서 받을 수 있나요?**  
A3: 커뮤니티 지원은 [Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)에서 확인하십시오.

**Q4: Aspose.CAD for Java 라이선스는 어떻게 구매하나요?**  
A4: [구매 페이지](https://purchase.aspose.com/buy)에서 라이선스를 구매할 수 있습니다.

**Q5: 테스트 용도로 임시 라이선스를 사용할 수 있나요?**  
A5: 예, 임시 라이선스는 [여기](https://purchase.aspose.com/temporary-license/)에서 받을 수 있습니다.

**추가 질문**

**Q: 이 방법이 Linux에서 DWG 파일을 읽는 데도 작동하나요?**  
A: 전적으로 작동합니다. 솔루션이 순수 Java이므로 호환 가능한 JDK가 설치된 모든 OS에서 실행됩니다.

**Q: 전체 도면을 메모리에 로드하지 않고 DWG 파일을 읽을 수 있나요?**  
A: Aspose.CAD는 도면을 메모리에 로드합니다. 매우 큰 파일의 경우 향후 릴리스에서 제공될 수 있는 스트리밍 API나 별도 스레드 처리를 고려하십시오.

**Q: 레이아웃을 이름으로 필터링할 수 있나요?**  
A: 예 – `CadLayoutDictionary`를 가져온 뒤 `layout.getLayoutName().equalsIgnoreCase("MyLayout")`와 같이 이름을 확인한 후 처리하면 됩니다.

---

**최종 업데이트:** 2026-02-28  
**테스트 환경:** Aspose.CAD for Java 24.11  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}