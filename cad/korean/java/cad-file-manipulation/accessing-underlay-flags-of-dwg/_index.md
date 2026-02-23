---
date: 2026-02-23
description: Java용 Aspose.CAD DWG를 사용하여 DWG 파일을 로드하고 언더레이 플래그를 추출하는 방법을 배우세요 – 개발자를
  위한 단계별 가이드.
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: aspose cad dwg – DWG 로드 및 언더레이 플래그 접근 (Java)
url: /ko/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG 파일 로드 및 Underlay 플래그 접근 – Aspose.CAD for Java

현대 CAD 워크플로우에서 **aspose cad dwg**를 사용하면 DWG 파일을 빠르게 로드하고 일반 사용자에게 숨겨진 경우가 많은 underlay 세부 정보를 추출할 수 있습니다. Java DWG 뷰어를 구축하든, 배치 프로세스 dwg 파이프라인을 자동화하든, GIS 통합을 위한 메타데이터를 추출하든, Aspose.CAD for Java는 깔끔한 코드‑우선 방식을 제공합니다. 이 튜토리얼에서는 **DWG 파일을 로드**하고, 엔티티를 반복하며, 많은 개발자가 간과하는 underlay 플래그를 읽는 정확한 단계를 안내합니다.

## 빠른 답변
- **DWG를 열기 위한 주요 클래스는 무엇인가요?** `com.aspose.cad.Image.load()` 은 `CadImage` 를 반환합니다.  
- **Underlay 정보를 담고 있는 객체는 무엇인가요?** `CadUnderlay` (또는 `CadDgnUnderlay` 와 같은 파생 타입).  
- **개발에 라이선스가 필요합니까?** 테스트용 무료 체험판을 사용할 수 있으며, 프로덕션에서는 상용 라이선스가 필요합니다.  
- **루프에서 여러 DWG 파일을 처리할 수 있나요?** 예 – 로드‑및‑반복 패턴을 반복하면 됩니다.  
- **이 접근 방식이 Java 11+와 호환되나요?** 물론입니다. Aspose.CAD는 Java 8부터 최신 LTS 릴리스까지 지원합니다.

## aspose cad dwg – DWG 파일 로드 (Java)

`Image.load()`은 바이너리 DWG 내용을 읽어 메모리 내 `CadImage` 객체를 생성합니다. 여기서부터는 DWG 파일 포맷을 직접 다루지 않고도 레이어, 블록, underlay 엔티티를 탐색할 수 있습니다.

## 왜 DWG에서 underlay 플래그를 추출해야 할까요?

Underlay 플래그는 외부 참조(예: DGN 또는 PDF underlay)가 도면 내에서 어떻게 위치하고, 스케일링되며, 회전되는지를 알려줍니다. 이러한 값을 알면 다음을 수행할 수 있습니다.

- 맞춤형 **java dwg viewer**에서 정확한 시각 레이아웃을 재구성합니다.  
- underlay를 네이티브 CAD 엔티티로 변환하여 추가 편집이 가능하게 합니다.  
- 규정 준수 또는 문서화를 위해 underlay 메타데이터를 포함한 보고서를 생성합니다.  
- **Batch process dwg** 파일을 처리하고, 추출한 underlay 메타데이터를 데이터베이스에 저장하여 나중에 분석합니다.

## 사전 요구 사항
- **Aspose.CAD Library** – [releases](https://releases.aspose.com/cad/java/) 페이지에서 다운로드합니다.  
- **Java Development Kit** – JDK 8 이상.  
- **DWG 파일이 들어 있는 폴더**. 코드에서 `"Your Document Directory"` 를 실제 경로로 교체하세요.

## Import Namespaces

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.CadUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.UnderlayFlags;
```

## 단계별 가이드

### Step 1: Set the Resource Directory
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```
DWG 파일이 위치한 디렉터리를 정의합니다. 전용 폴더를 사용하면 샘플이 깔끔하고 이식성이 높아집니다.

### Step 2: Load the DWG File
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
여기서 **dwg 파일** `BlockRefDgn.dwg` 를 `CadImage` 인스턴스로 로드하여 검토할 준비를 합니다.

### Step 3: Iterate Through DWG Entities
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
루프는 모든 엔티티(선, 원, 블록, underlay)를 순회하므로 필요한 항목을 골라낼 수 있습니다.

### Step 4: Identify CadDgnUnderlay Entities
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
`CadDgnUnderlay` 객체만이 우리가 찾는 underlay 플래그를 포함하고 있으므로, 해당 객체만 필터링합니다.

### Step 5: Access Underlay Information
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
`CadUnderlay` 를 확보하면 경로, 이름, 삽입점, 회전, 스케일 팩터 및 가시성, 클리핑 등 렌더링 옵션을 나타내는 `UnderlayFlags` 열거형을 읽을 수 있습니다.

## 배치 프로세스에서 dwg 파일을 로드하는 방법

**batch process dwg** 파일이 필요하다면, 위 단계들을 `for` 루프로 감싸 `dataDir` 에 있는 모든 파일을 순회하면 됩니다. 동일한 `Image.load()` 호출이 각 파일에 적용되며, 추출한 플래그를 CSV 또는 데이터베이스에 저장해 후속 보고에 활용할 수 있습니다.

## 일반적인 문제 및 팁
- **Null underlay path** – DWG가 실제로 외부 파일을 참조하고 있는지 확인하세요. 그렇지 않으면 경로가 비어 있습니다.  
- **Unsupported underlay type** – 현재 Aspose.CAD는 DGN underlay만 지원하며, PDF underlay는 아직 API를 통해 제공되지 않습니다.  
- **License exceptions** – 유효한 라이선스 없이 코드를 실행하면 내보낸 이미지에 워터마크가 추가됩니다.  
- **Performance tip:** 배치 처리 시 단일 `Image` 인스턴스를 재사용하면 GC 부하를 줄일 수 있습니다.

## 자주 묻는 질문

**Q: Aspose.CAD for Java를 다른 CAD 파일 형식과 함께 사용할 수 있나요?**  
A: Aspose.CAD는 주로 DWG 형식에 초점을 맞추지만, DXF, DWF 및 기타 CAD 형식도 지원합니다.

**Q: Aspose.CAD for Java용 체험 버전이 있나요?**  
A: 예, [여기](https://releases.aspose.com/)에서 무료 체험판으로 기능을 살펴볼 수 있습니다.

**Q: Aspose.CAD for Java에 대한 지원이나 도움을 어떻게 받을 수 있나요?**  
A: 커뮤니티 지원 및 토론을 위해 [Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)을 방문하세요.

**Q: Aspose.CAD for Java용 임시 라이선스가 제공되나요?**  
A: 예, [여기](https://purchase.aspose.com/temporary-license/)에서 임시 라이선스를 얻을 수 있습니다.

**Q: Aspose.CAD for Java에 대한 포괄적인 문서는 어디서 찾을 수 있나요?**  
A: 자세한 내용은 [문서](https://reference.aspose.com/cad/java/)를 참고하세요.

**Last Updated:** 2026-02-23  
**Tested With:** Aspose.CAD 24.12 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}