---
date: 2025-12-22
description: Aspose.CAD for Java를 사용하여 DWG 파일을 로드하고 언더레이 정보를 추출하는 방법을 배우세요 – 언더레이
  플래그를 다루는 단계별 가이드.
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: DWG 파일 로드 및 언더레이 플래그 액세스 – Aspose.CAD for Java
url: /ko/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG 파일 로드 및 Underlay 플래그 접근 – Aspose.CAD for Java

현대 CAD 워크플로에서 **DWG 파일 로드**를 빠르게 수행하고 underlay 세부 정보를 추출하는 것은 일반적인 요구 사항입니다. 뷰어를 구축하거나 배치 처리를 자동화하거나 GIS 통합을 위한 메타데이터를 추출하든, Aspose.CAD for Java는 깔끔한 코드‑우선 방식을 제공합니다. 이 튜토리얼에서는 **DWG 파일 로드** 단계, 엔티티 반복, 그리고 많은 개발자가 간과하는 underlay 플래그 읽는 정확한 절차를 안내합니다.

## 빠른 답변
- **DWG를 열기 위한 기본 클래스는 무엇인가요?** `com.aspose.cad.Image.load()`는 `CadImage`를 반환합니다.
- **underlay 정보를 보유하는 객체는 무엇인가요?** `CadUnderlay`(또는 `CadDgnUnderlay`와 같은 파생 타입).
- **개발에 라이선스가 필요합니까?** 무료 체험판으로 테스트가 가능하며, 프로덕션에서는 상용 라이선스가 필요합니다.
- **루프에서 여러 DWG 파일을 처리할 수 있나요?** 예 – load‑and‑iterate 패턴을 반복하면 됩니다.
- **이 접근 방식이 Java 11+와 호환되나요?** 물론입니다. Aspose.CAD는 Java 8부터 최신 LTS 릴리스까지 지원합니다.

## Aspose.CAD에서 “DWG 파일 로드”란 무엇인가요?
`Image.load()`은 바이너리 DWG 내용을 읽어 메모리 내 `CadImage` 객체를 생성합니다. 이후 DWG 파일 포맷을 직접 다루지 않고도 레이어, 블록, underlay 엔티티를 탐색할 수 있습니다.

## DWG에서 underlay 플래그를 추출하는 이유는?
Underlay 플래그는 외부 참조(예: DGN 또는 PDF underlay)가 도면 내에서 어떻게 위치하고, 스케일링 및 회전되는지를 알려줍니다. 이러한 값을 알면 다음을 수행할 수 있습니다:
- 맞춤형 뷰어에서 정확한 시각 레이아웃을 재구성합니다.
- underlay를 네이티브 CAD 엔티티로 변환하여 추가 편집이 가능합니다.
- 규정 준수 또는 문서화를 위해 underlay 메타데이터를 포함한 보고서를 생성합니다.

## 전제 조건
- **Aspose.CAD 라이브러리** – [releases](https://releases.aspose.com/cad/java/) 페이지에서 다운로드합니다.
- **Java Development Kit** – JDK 8 이상.
- **DWG 파일이 들어 있는 폴더**. 코드에서 `"Your Document Directory"`를 실제 경로로 교체하십시오.

## 네임스페이스 가져오기

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.CadUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.UnderlayFlags;
```

## 단계별 가이드

### 단계 1: 리소스 디렉터리 설정
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```
DWG 파일이 위치한 경로를 정의합니다. 전용 폴더를 사용하면 샘플이 깔끔하고 이식성이 유지됩니다.

### 단계 2: DWG 파일 로드
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
여기서는 **DWG 파일 로드** `BlockRefDgn.dwg`를 `CadImage` 인스턴스로 불러와 검토 준비를 합니다.

### 단계 3: DWG 엔티티 반복
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
루프는 모든 엔티티(선, 원, 블록, underlay)를 순회하여 필요한 항목을 선택할 수 있게 합니다.

### 단계 4: CadDgnUnderlay 엔티티 식별
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
`CadDgnUnderlay` 객체에만 우리가 찾는 underlay 플래그가 포함되어 있으므로 해당 객체만 필터링합니다.

### 단계 5: Underlay 정보 접근
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
`CadUnderlay`를 확보하면 경로, 이름, 삽입점, 회전, 스케일 팩터 및 가시성, 클리핑, 기타 렌더링 옵션을 나타내는 `UnderlayFlags` 열거형을 읽을 수 있습니다.

## 일반적인 문제 및 팁
- **Null underlay 경로** – DWG가 실제로 외부 파일을 참조하는지 확인하십시오; 그렇지 않으면 경로가 비어 있습니다.
- **지원되지 않는 underlay 유형** – Aspose.CAD는 현재 DGN underlay만 지원하며, PDF underlay는 아직 API를 통해 제공되지 않습니다.
- **라이선스 예외** – 유효한 라이선스 없이 코드를 실행하면 내보낸 이미지에 워터마크가 추가됩니다.

## 자주 묻는 질문

**Q: Aspose.CAD for Java를 다른 CAD 파일 형식과 함께 사용할 수 있나요?**  
A: Aspose.CAD는 주로 DWG 형식에 초점을 맞추지만, DXF, DWF 및 기타 CAD 형식도 지원합니다.

**Q: Aspose.CAD for Java에 대한 체험판이 있나요?**  
A: 예, [here](https://releases.aspose.com/)에서 무료 체험판으로 기능을 살펴볼 수 있습니다.

**Q: Aspose.CAD for Java에 대한 지원이나 도움을 어떻게 받을 수 있나요?**  
A: 커뮤니티 지원 및 토론을 위해 [Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)을 방문하십시오.

**Q: Aspose.CAD for Java에 대한 임시 라이선스가 있나요?**  
A: 예, [here](https://purchase.aspose.com/temporary-license/)에서 임시 라이선스를 받을 수 있습니다.

**Q: Aspose.CAD for Java에 대한 포괄적인 문서는 어디서 찾을 수 있나요?**  
A: 자세한 정보는 [documentation](https://reference.aspose.com/cad/java/)을 참고하십시오.

---

**마지막 업데이트:** 2025-12-22  
**테스트 환경:** Aspose.CAD 24.12 for Java  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}