---
date: 2026-01-10
description: 이 단계별 튜토리얼에서 Aspose.CAD for Java를 사용하여 DWG 파일을 읽고 멀티리더 DWG 엔터티를 만드는 방법을
  배워보세요.
linktitle: Support MLeader Entity for DWG Format with Java
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java로 DWG를 읽고 MLeader 지원하기
url: /ko/java/cad-text-and-formatting/support-mleader-entity/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG를 읽고 Aspose.CAD for Java로 MLeader 지원하기

## 소개

Java 애플리케이션에서 **DWG** 파일을 **읽고** **멀티리더 DWG** 엔터티를 다루어야 한다면, 바로 이곳이 정답입니다. Aspose.CAD for Java는 DWG 도면을 열고, MLeader 객체를 검사하며, 해당 속성을 검증할 수 있는 깔끔한 프로그래밍 방식을 제공하므로 별도의 CAD 워크스테이션이 필요하지 않습니다. 이번 튜토리얼에서는 DWG 파일 로드부터 멀티리더 데이터가 기대하는 스타일과 일치하는지 확인하는 전체 과정을 단계별로 안내합니다.

## 빠른 답변
- **“DWG를 읽는 방법”은 무엇을 의미하나요?** `Image.load()` 로 DWG를 로드하고 `CadImage` 로 캐스팅합니다.  
- **멀티리더 DWG 엔터티를 생성할 수 있나요?** 예 – CadMLeader API를 사용해 MLeader 객체를 추가, 편집 및 검증할 수 있습니다.  
- **필요한 라이브러리 버전은?** 최신 Aspose.CAD for Java 릴리스(2024+ 빌드)라면 모두 동작합니다.  
- **개발에 라이선스가 필요하나요?** 테스트용 임시 라이선스로 가능하지만, 운영 환경에서는 정식 라이선스가 필요합니다.  
- **코드가 크로스‑플랫폼인가요?** 물론입니다 – Java는 Windows, Linux, macOS에서 모두 실행됩니다.

## Aspose.CAD와 함께 “DWG를 읽는 방법”이란?

DWG 파일을 읽는다는 것은 바이너리 도면을 메모리 상의 `CadImage` 객체로 변환하는 것을 의미합니다. 이 객체를 얻으면 엔터티(선, 원, 텍스트, **MLeader** 객체 등)를 열거하고 속성을 검사할 수 있습니다.

## 왜 MLeader 엔터티를 지원해야 할까요?

MLeader(멀티리더) 객체는 리더 라인과 연결된 텍스트 또는 블록을 결합한 형태로, 엔지니어링 도면에서 주석을 달 때 필수적입니다. 이를 지원하면 다음을 할 수 있습니다:

- 주석이 회사 표준에 부합하는지 검증
- 텍스트를 추출해 후속 처리(예: BOM 생성) 수행
- 리더 스타일을 프로그래밍 방식으로 수정하거나 블록 내용을 교체

## 사전 준비

시작하기 전에 다음을 준비하세요:

1. **Java 개발 환경** – JDK 11 이상 및 선호하는 IDE(IntelliJ, Eclipse, VS Code)  
2. **Aspose.CAD for Java** – 최신 JAR 파일을 [다운로드 링크](https://releases.aspose.com/cad/java/)에서 받으세요  

## 네임스페이스 가져오기

DWG 엔터티와 래스터화 옵션을 사용하려면 Java 클래스에 다음 import 문을 추가합니다:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeader;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderContextData;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderLine;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderNode;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Aspose.CAD for Java로 DWG 파일 읽는 방법

### 단계 1: DWG 파일을 로드하고 `CadImage` 얻기

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

### 단계 2: 도면에 MLeader 엔터티가 포함되어 있는지 검증

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### 단계 3: MLeader 스타일 및 기본 속성 확인

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

### 단계 4: MLeader 컨텍스트 데이터에 접근 (멀티리더의 핵심)

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

### 단계 5: 컨텍스트‑레벨 속성 검증

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(),
    "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

### 단계 6: MLeader 노드와 리더 라인 작업

```java
CadMLeaderNode mleaderNode = context.getLeaderNode();
Assert.areEqual(mleaderNode.getLastLeaderLinePoint().getX(), 473, 1);

CadMLeaderLine leaderLine = mleaderNode.getLeaderLine();
Assert.areEqual(leaderLine.getBreakEndPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getBreakPointIndex().getValue()), Integer.toString(0));
Assert.areEqual(leaderLine.getBreakStartPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getLeaderLineIndex().getValue()), Integer.toString(0));
Assert.areEqual(Integer.toString(leaderLine.getLeaderPoints().size()), Integer.toString(4));
```

### 단계 7: 추가 MLeader 노드 속성 검증

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

### 단계 8: 텍스트‑관련 속성 확인

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

### 단계 9: 기타 MLeader 속성을 전체적으로 검토

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## 일반적인 문제와 해결책

| 문제 | 발생 원인 | 해결 방법 |
|------|----------|----------|
| `ClassCastException` 발생 시 캐스팅 오류 | 선택한 인덱스가 MLeader 객체가 아님 | 캐스팅 전에 `cadImage.getEntities()[i] instanceof CadMLeader` 를 확인 |
| 리더 라인 포인트가 `null` | 도면이 완전히 지원되지 않는 커스텀 리더 스타일 사용 | 최신 Aspose.CAD 버전을 사용하거나 테스트용으로 기본 스타일을 사용 |
| 숫자 값에 대한 Assertion 실패 | CAD 버전 간 미세한 반올림 차이 | 예제와 같이 `Assert.areEqual(..., delta)` 에 허용 오차를 조정 |

## 자주 묻는 질문

**Q: Aspose.CAD for Java를 다른 CAD 포맷과 함께 사용할 수 있나요?**  
A: 예, Aspose.CAD는 DWG 외에도 DXF, DWF, DGN 및 여러 래스터 포맷을 지원합니다.

**Q: Aspose.CAD for Java에 대한 자세한 문서는 어디서 찾을 수 있나요?**  
A: API 세부 정보와 코드 샘플은 공식 [문서](https://reference.aspose.com/cad/java/)를 참고하세요.

**Q: 무료 체험판을 제공하나요?**  
A: 물론입니다 – [무료 체험판](https://releases.aspose.com/) 페이지에서 다운로드할 수 있습니다.

**Q: 테스트용 임시 라이선스는 어떻게 얻나요?**  
A: [임시 라이선스 링크](https://purchase.aspose.com/temporary-license/)를 통해 발급받으세요.

**Q: 커뮤니티에 질문하고 싶다면 어디에 문의하면 되나요?**  
A: [Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)에서 질문과 해결책을 공유할 수 있습니다.

## 결론

이제 **DWG 파일을 읽는 방법**과 **Aspose.CAD for Java로 멀티리더 DWG 엔터티를 생성하는 방법**에 대한 전체 흐름을 이해하셨습니다. 위 단계들을 따라 하면 MLeader 스타일을 검증하고, 주석 데이터를 추출하며, DWG 처리를 Java 기반 워크플로에 손쉽게 통합할 수 있습니다.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**마지막 업데이트:** 2026-01-10  
**테스트 환경:** Aspose.CAD 24.11 for Java  
**작성자:** Aspose