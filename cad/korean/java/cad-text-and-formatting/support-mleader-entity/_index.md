---
title: Java용 Aspose.CAD를 사용하여 DWG 형식용 MLeader 엔터티 지원
linktitle: Java를 사용한 DWG 형식용 MLeader 엔터티 지원
second_title: Aspose.CAD 자바 API
description: DWG 형식의 MLeader 엔터티 지원에 대한 단계별 튜토리얼을 통해 Java용 Aspose.CAD의 강력한 기능을 활용하세요.
weight: 12
url: /ko/java/cad-text-and-formatting/support-mleader-entity/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java용 Aspose.CAD를 사용하여 DWG 형식용 MLeader 엔터티 지원

## 소개

Java를 사용한 CAD(컴퓨터 지원 설계) 영역에서 DWG 형식의 MLeader 엔터티에 대한 지원을 이해하고 구현하는 것은 귀중한 기술입니다. Aspose.CAD for Java는 강력한 도구와 기능 세트를 제공하여 이러한 작업을 위한 강력한 솔루션을 제공합니다. 이 튜토리얼은 Aspose.CAD와 함께 Java를 사용하여 DWG 파일 내에서 MLeader 엔터티를 지원하는 프로세스를 안내합니다.

## 전제 조건

튜토리얼을 자세히 살펴보기 전에 다음 전제 조건이 충족되었는지 확인하세요.

1. Java 개발 환경: 시스템에 Java 개발 환경이 설정되어 있는지 확인하십시오.

2.  Aspose.CAD 라이브러리: 다음에서 Java용 Aspose.CAD 라이브러리를 다운로드하고 설치합니다.[다운로드 링크](https://releases.aspose.com/cad/java/).

## 네임스페이스 가져오기

Java 프로젝트에서 Aspose.CAD의 기능을 효과적으로 활용하는 데 필요한 네임스페이스를 가져옵니다. 코드에 다음 줄을 포함합니다.

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

이제 코드를 Aspose.CAD와 함께 Java를 사용하여 DWG 형식용 MLeader 엔터티를 지원하는 단계별 가이드로 나누어 보겠습니다.

## 1. DWG 파일 로드 및 CadImage 액세스

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

## 2. MLeader 엔터티 유효성 검사

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### 3. MLeader 스타일 및 속성 확인

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

## 4. MLeader 컨텍스트 데이터에 액세스

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

## 5. 컨텍스트 속성 검증

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(), "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

## 6. MLeader 노드 및 지시선에 액세스

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

## 7. 추가 MLeader 속성 검증

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

## 8. 텍스트 속성 확인

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

## 9. 추가 MLeader 속성

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## 결론

축하해요! Java 및 Aspose.CAD를 사용하여 DWG 형식에 대한 MLeader 엔터티 지원에 대한 포괄적인 가이드를 성공적으로 탐색했습니다. 이 기능은 고급 CAD 조작을 가능하게 하고 Java 개발 툴킷을 향상시킵니다.

## FAQ

### Q1: Aspose.CAD for Java를 다른 CAD 형식과 함께 사용할 수 있나요?

A1: 예, Aspose.CAD는 DWG 이외의 다양한 CAD 형식을 지원하여 프로젝트에 다양성을 제공합니다.

### Q2: Aspose.CAD for Java에 대한 자세한 문서는 어디서 찾을 수 있나요?

 A2: 다음을 참조하세요.[선적 서류 비치](https://reference.aspose.com/cad/java/) Aspose.CAD의 기능에 대한 심층적인 통찰력을 얻으려면

### Q3: 무료 평가판이 제공됩니까?

 A3: 예.[무료 시험판](https://releases.aspose.com/).

### Q4: Aspose.CAD에 대한 임시 라이선스를 어떻게 얻을 수 있나요?

A4: 다음을 통해 임시 면허를 취득하세요.[이 링크](https://purchase.aspose.com/temporary-license/).

### 질문 5: 지역사회 지원 및 도움을 어디서 구할 수 있나요?

A5: 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 커뮤니티에 연결하고 도움을 받으려면
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
