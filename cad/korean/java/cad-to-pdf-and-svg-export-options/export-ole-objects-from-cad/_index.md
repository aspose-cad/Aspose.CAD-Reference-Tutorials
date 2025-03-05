---
title: Java용 Aspose.CAD를 사용하여 CAD에서 OLE 개체 내보내기
linktitle: CAD에서 OLE 개체 내보내기
second_title: Aspose.CAD 자바 API
description: Java용 Aspose.CAD의 잠재력을 활용해 보세요. CAD 파일에서 OLE 개체를 쉽게 내보낼 수 있습니다. 원활한 CAD 데이터 관리를 위해 지금 다운로드하세요.
type: docs
weight: 10
url: /ko/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
---
## 소개

역동적인 CAD(Computer-Aided Design) 세계에서는 OLE(Object Linking and Embedding) 개체를 효율적으로 관리하고 추출하는 것이 중요합니다. Aspose.CAD for Java는 CAD 파일에서 OLE 개체를 내보내기 위한 강력한 솔루션을 제공합니다. 이 단계별 가이드는 프로세스를 안내하여 이 도구의 잠재력을 최대한 활용하도록 보장합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

- Java 환경: 컴퓨터에 Java 개발 환경이 설정되어 있는지 확인하세요.
-  Aspose.CAD for Java: Aspose.CAD for Java 라이브러리를 다운로드하고 설치하세요. 도서관은 다음에서 찾으실 수 있습니다.[다운로드 링크](https://releases.aspose.com/cad/java/).
- CAD 파일: 내보낼 OLE 개체가 포함된 CAD 파일을 준비합니다.

## 네임스페이스 가져오기

시작하려면 필요한 네임스페이스를 Java 프로젝트로 가져옵니다. 이러한 네임스페이스는 Aspose.CAD를 사용하여 CAD 파일 작업에 필요한 필수 클래스와 기능을 제공합니다.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

이제 CAD에서 OLE 객체를 내보내는 과정을 여러 단계로 나누어 보겠습니다.

## 1단계: 문서 디렉터리 설정

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

"문서 디렉토리"를 CAD 파일이 포함된 디렉토리 경로로 바꾸십시오.

## 2단계: CAD 파일 이름 정의

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

 처리하려는 CAD 파일의 이름을 지정하십시오.`files` 정렬.

## 3단계: PNG 내보내기 옵션 설정

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

벡터 래스터화 및 레이아웃 설정을 포함한 PNG 내보내기 옵션을 구성합니다.

## 4단계: CAD 파일 반복

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

지정된 각 CAD 파일을 반복하고 Aspose.CAD를 사용하여 로드한 다음 OLE 개체를 PNG 이미지로 저장합니다.

## 결론

이러한 간단하면서도 강력한 단계를 통해 Aspose.CAD for Java를 사용하여 CAD 파일에서 OLE 개체를 원활하게 내보낼 수 있습니다. 이 다용도 도구를 사용하면 개발자가 CAD 데이터를 효율적으로 관리할 수 있어 CAD 응용 프로그램 개발에 새로운 가능성이 열립니다.

## FAQ

### Q1: Aspose.CAD는 모든 CAD 파일 형식과 호환됩니까?

 A1: Aspose.CAD는 DWG, DXF, DGN을 포함한 다양한 CAD 형식을 지원합니다. 다음을 참조하세요.[선적 서류 비치](https://reference.aspose.com/cad/java/) 전체 목록을 보려면.

### Q2: OLE 개체에 대한 내보내기 설정을 사용자 지정할 수 있습니까?

A2: 예, Aspose.CAD는 내보내기 설정을 사용자 정의하기 위한 광범위한 옵션을 제공하므로 특정 요구 사항에 맞게 출력을 조정할 수 있습니다.

### Q3: Aspose.CAD에 대한 무료 평가판이 있습니까?

 A3: 예, 다음에서 무료 평가판을 받아 Aspose.CAD의 기능을 탐색할 수 있습니다.[여기](https://releases.aspose.com/).

### Q4: Aspose.CAD에 대한 커뮤니티 지원은 어디서 받을 수 있나요?

 A4: Aspose.CAD 커뮤니티에 가입하세요.[법정](https://forum.aspose.com/c/cad/19) 도움을 구하고 경험을 공유합니다.

### Q5: Aspose.CAD 라이선스는 어떻게 구매할 수 있나요?

A5: 다음을 방문하세요.[구매 페이지](https://purchase.aspose.com/buy) 귀하의 개발 요구에 맞는 라이센스를 취득하십시오.