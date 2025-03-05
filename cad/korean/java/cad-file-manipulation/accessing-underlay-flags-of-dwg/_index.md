---
title: Java용 Aspose.CAD를 사용하여 DWG의 언더레이 플래그에 액세스
linktitle: DWG의 언더레이 플래그에 액세스
second_title: Aspose.CAD 자바 API
description: Aspose.CAD for Java로 CAD 마법의 세계를 탐험해보세요! Java 애플리케이션에서 DWG 파일을 손쉽게 처리할 수 있습니다.
type: docs
weight: 11
url: /ko/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
---
## 소개

CAD(Computer-Aided Design) 영역에서는 정확성과 효율성이 가장 중요합니다. Aspose.CAD for Java는 강력한 동맹으로 등장하여 Java 애플리케이션과 CAD 기능 간의 원활한 연결을 제공합니다. 이 단계별 가이드에서는 DWG 파일을 처리하고 Java를 사용하여 귀중한 정보를 추출하는 데 중점을 두고 Aspose.CAD의 마법을 탐구합니다.

## 전제 조건

이 여정을 시작하기 전에 다음 사항이 준비되어 있는지 확인하세요.

-  Aspose.CAD 라이브러리: Aspose.CAD 라이브러리를 다운로드하여 설치합니다.[릴리스](https://releases.aspose.com/cad/java/) 페이지.

-  문서 디렉토리: DWG 도면이 저장되는 디렉토리를 생성합니다. 바꾸다`"Your Document Directory"` 실제 경로가 포함된 코드 조각에서

## 네임스페이스 가져오기

Aspose.CAD의 모든 기능을 활용하려면 필요한 네임스페이스를 가져와야 합니다.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.CadUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.UnderlayFlags;
```

이제 예제를 여러 단계로 나누어 보겠습니다.

## 1단계: 리소스 디렉터리 설정

```java
// 리소스 디렉터리의 경로입니다.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

 이 단계에서는 DWG 도면이 저장되는 디렉토리를 정의합니다. 바꾸다`"Your Document Directory"` 실제 경로와 함께.

## 2단계: DWG 파일 로드 및 CadImage로 변환

```java
// 입력 파일 이름 및 경로
String fileName = dataDir + "BlockRefDgn.dwg";

//기존 DWG 파일을 로드하고 CadImage로 변환합니다.
CadImage image = (CadImage)Image.load(fileName);
```

이 단계에서는 DWG 파일의 경로와 이름을 지정한 다음 이를 CadImage 객체로 로드합니다.

## 3단계: DWG 엔터티 반복

```java
// DWG 파일 내의 각 엔터티를 살펴보세요.
for(CadBaseEntity entity : image.getEntities())
```

이 루프는 DWG 파일 내의 각 엔터티를 반복하여 이를 분석하고 조작할 수 있게 해줍니다.

## 4단계: CadDgnUnderlay 유형 확인

```java
// 엔터티가 CadDgnUnderlay 유형인지 확인하세요.
if (entity instanceof CadDgnUnderlay)
```

이 조건문은 CadDgnUnderlay 유형의 엔터티를 구체적으로 처리하도록 보장합니다.

## 5단계: 언더레이 정보에 액세스

```java
// 다양한 언더레이 플래그에 액세스
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (추가 언더레이 속성)
break;
```

여기서는 CadUnderlay 객체의 다양한 속성에 액세스하여 언더레이 경로, 이름, 삽입점, 회전 각도 및 축척 비율과 같은 중요한 정보를 추출합니다.

## 결론

이 튜토리얼에서는 Java 기능에 대한 Aspose.CAD의 표면만 살펴봤습니다. 이러한 단계를 완료하면 이제 Java 애플리케이션에서 CAD 조작의 잠재력을 활용할 수 있습니다.

## FAQ

### Q1: Aspose.CAD for Java를 다른 CAD 파일 형식과 함께 사용할 수 있습니까?

A1: Aspose.CAD는 주로 DWG 형식에 중점을 두고 있지만 DXF, DWF 및 기타 CAD 형식도 지원합니다.

### Q2: Aspose.CAD for Java에 사용할 수 있는 평가판이 있습니까?

 A2: 예, 무료 평가판을 통해 기능을 탐색할 수 있습니다.[여기](https://releases.aspose.com/).

### Q3: Aspose.CAD for Java에 대한 지원을 받거나 도움을 받으려면 어떻게 해야 합니까?

 A3: 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 커뮤니티 지원 및 토론을 위해.

### Q4: Aspose.CAD for Java에 임시 라이선스를 사용할 수 있나요?

 A4: 예, 임시 라이센스를 얻을 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).

### Q5: Aspose.CAD for Java에 대한 종합 문서는 어디서 찾을 수 있나요?

 A5: 다음을 참조하세요.[선적 서류 비치](https://reference.aspose.com/cad/java/) 자세한 정보를 보려면.