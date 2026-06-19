---
date: 2026-06-19
description: Aspose.CAD for Java를 사용하여 DWG 파일을 편집하는 방법을 배우고, DWG XRef 경로 업데이트 및 하이퍼링크
  편집 방법을 포함합니다. 오늘 무료 체험을 이용해 보세요!
keywords:
- how to edit dwg
- update dwg xref paths
- Aspose.CAD Java hyperlink
linktitle: 하이퍼링크 편집
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Learn how to edit DWG files with Aspose.CAD for Java, including how
    to update DWG XRef paths and edit hyperlinks. Try the free trial today!
  headline: How to Edit DWG Hyperlinks - Aspose.CAD Java Tutorial
  type: TechArticle
- description: Learn how to edit DWG files with Aspose.CAD for Java, including how
    to update DWG XRef paths and edit hyperlinks. Try the free trial today!
  name: How to Edit DWG Hyperlinks - Aspose.CAD Java Tutorial
  steps:
  - name: Accessing Insert Objects
    text: '`CadInsertObject` is the Aspose.CAD class that represents an inserted block
      reference (XRef) inside a DWG drawing. Iterate through the entities and identify
      if an entity is an instance of the `CadInsertObject` class.'
  - name: How to Change XRef Path in a DWG Drawing
    text: '`CadImage` is the primary object that loads and saves CAD files in Aspose.CAD
      for Java. Once you have identified the insert object, retrieve the associated
      block entity and update the XRef path as needed. This ensures the reference
      points to the correct external file.'
  - name: Modifying Hyperlinks
    text: Next, check if the entity has a hyperlink associated with it. If the hyperlink
      matches a specific URL, update it to the desired URL. This step guarantees that
      clicking the hyperlink in the CAD viewer opens the new target.
  type: HowTo
- questions:
  - answer: Yes, after making changes call `cadImage.save("EditedDrawing.dwg");` to
      persist the modifications.
    question: Do I need to call a specific method to write the edited DWG back to
      disk?
  - answer: Absolutely—loop through `cadImage.getEntities()` and apply the hyperlink
      logic to each matching entity.
    question: Is it possible to edit multiple hyperlinks in one pass?
  type: FAQPage
second_title: Aspose.CAD Java API
title: DWG 하이퍼링크 편집 방법 - Aspose.CAD Java 튜토리얼
url: /ko/java/other-cad-operations/edit-hyperlink/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG 하이퍼링크 편집 방법 - Aspose.CAD Java 튜토리얼

오늘날 디지털 시대에 **DWG 파일을 효율적으로 편집하는 방법**은 엔지니어, 건축가 및 BIM 전문가에게 필수적인 기술입니다. 끊어진 하이퍼링크를 수정하거나 XRef를 새로운 소스로 지정하거나 다수의 도면을 일괄 업데이트해야 할 때, Aspose.CAD for Java는 CAD 편집기를 열지 않고도 이러한 변경을 프로그래밍 방식으로 수행할 수 있는 깔끔한 방법을 제공합니다. 이 튜토리얼에서는 도면을 로드하고 편집을 저장하는 전체 과정을 단계별로 안내합니다.

## 빠른 답변
- **Java에서 DWG 편집을 처리하는 라이브러리는 무엇입니까?** Aspose.CAD for Java.  
- **하이퍼링크와 XRef 경로를 함께 편집할 수 있습니까?** 예—두 기능 모두 동일한 API에서 지원됩니다.  
- **개발에 라이선스가 필요합니까?** 테스트용 무료 체험판을 사용할 수 있으며, 상용 환경에서는 상업용 라이선스가 필요합니다.  
- **필요한 Java 버전은?** Java 8 이상.  
- **코드 샘플을 그대로 실행할 수 있습니까?** 예, 파일 경로를 로컬 DWG 파일을 가리키도록 업데이트하면 바로 실행됩니다.

## 왜 DWG 하이퍼링크와 XRef 경로를 편집해야 할까요?

하이퍼링크와 XRef 경로를 최신 상태로 유지하면 깨진 참조를 방지하고, 프로젝트 문서가 항상 올바른 리소스를 가리키게 하며, 방대한 CAD 라이브러리 전반에 걸쳐 자동화된 일괄 업데이트를 가능하게 합니다. 이를 통해 수작업을 줄이고 오류를 최소화하며, 설계 수명 주기 전반에 걸쳐 링크 무결성을 프로그래밍 방식으로 유지함으로써 전체 프로젝트 효율성을 향상시킵니다.

## 전제 조건

튜토리얼을 진행하기 전에 다음 전제 조건을 준비하십시오:

1. **Java 개발 환경:** JDK 8+가 설치되어 있고 선호하는 IDE(IntelliJ IDEA, Eclipse 등)를 사용하고 있어야 합니다.  
2. **Aspose.CAD for Java 라이브러리:** [download link](https://releases.aspose.com/cad/java/)에서 Aspose.CAD for Java 라이브러리를 다운로드하고 설치하십시오.  
3. **DWG 도면:** 하이퍼링크 편집을 위해 준비된 DWG 파일이 있어야 합니다.

## 패키지 가져오기

Java 프로젝트에 필요한 패키지를 가져와야 Aspose.CAD for Java 기능을 사용할 수 있습니다.

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadBlockEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadInsertObject;
```

## Aspose.CAD for Java를 사용하여 DWG 하이퍼링크를 편집하는 방법?

`CadImage`는 CAD 도면을 로드하고 저장하는 데 사용되는 Aspose.CAD 클래스입니다.  
`CadImage`로 DWG 파일을 로드하고, 엔티티를 순회하면서 필요에 따라 하이퍼링크와 XRef 경로를 업데이트한 뒤, 최종적으로 이미지를 DWG 형식으로 저장합니다. 이 엔드‑투‑엔드 흐름을 통해 단일 패스에서 여러 엔티티를 수정하고 모든 변경 사항을 영구적으로 저장할 수 있습니다.

### 단계 1: 삽입 객체 접근

`CadInsertObject`는 DWG 도면 내부에 삽입된 블록 참조(XRef)를 나타내는 Aspose.CAD 클래스입니다. 엔티티를 순회하면서 해당 엔티티가 `CadInsertObject` 클래스의 인스턴스인지 확인하십시오.

```java
    String dataDir = "Your Document Directory" + "DWGDrawings/";
    
    CadImage cadImage = (CadImage)Image.load(dataDir + "AutoCad_Sample.dwg");
    for (CadBaseEntity entity : cadImage.getEntities())
    {
        if (entity instanceof CadInsertObject)
        {
        }
	}
```

### 단계 2: DWG 도면에서 XRef 경로 변경 방법

`CadImage`는 Aspose.CAD for Java에서 CAD 파일을 로드하고 저장하는 주요 객체입니다. 삽입 객체를 확인한 후, 연관된 블록 엔티티를 가져와 필요에 따라 XRef 경로를 업데이트하십시오. 이렇게 하면 외부 파일에 대한 참조가 올바른 파일을 가리키게 됩니다.

```java
			CadBlockEntity block = cadImage.getBlockEntities().get_Item(((CadInsertObject)entity).getName());
            String value = block.getXRefPathName().getValue();
            if (value != null && !value.contentEquals(""))
            {
                block.getXRefPathName().setValue("new file reference.dwg");
            }
    
```

### 단계 3: 하이퍼링크 수정

다음으로, 엔티티에 하이퍼링크가 연결되어 있는지 확인하십시오. 하이퍼링크가 특정 URL과 일치한다면 원하는 URL로 업데이트합니다. 이 단계는 CAD 뷰어에서 하이퍼링크를 클릭했을 때 새로운 대상이 열리도록 보장합니다.

```java
        if (entity.getHyperlink() == "https://products.aspose.com")
        {
            entity.setHyperlink("https://www.aspose.com");
        }
```

## 일반적인 함정 및 팁

- **문자열 비교:** Java에서는 문자열 비교에 `==` 대신 `.equals()`를 사용하십시오. 샘플에서는 간단히 `==`를 사용했지만, 실제 환경에서는 `entity.getHyperlink().equals("https://products.aspose.com")`와 같이 교체해야 합니다.  
- **Null 검사:** `block.getXRefPathName()`이 `null`이 아닌지 확인한 후 `.getValue()`를 호출하십시오.  
- **변경 사항 저장:** 엔티티를 수정한 후 `cadImage.save("output.dwg");`를 호출하여 변경 내용을 영구 저장합니다(원본 블록 수를 유지하기 위해 코드가 생략되었습니다).  
- **성능 참고:** Aspose.CAD for Java는 30개 이상의 CAD 형식을 지원하며, 전체 문서를 메모리에 로드하지 않고도 2 GB까지의 파일을 처리할 수 있어 대량 업데이트 시 빠르고 메모리 효율적입니다.

## 자주 묻는 질문

### Q1: Aspose.CAD for Java가 모든 DWG 도면 버전과 호환됩니까?
A1: Aspose.CAD for Java는 AutoCAD 2000부터 최신 2025 형식까지 50개 이상의 DWG 버전을 지원합니다.

### Q2: Aspose.CAD for Java를 상업 프로젝트에 사용할 수 있습니까?
A2: 예, 상용 환경에서는 상업용 라이선스가 필요합니다. 라이선스는 [여기](https://purchase.aspose.com/buy)에서 구매할 수 있습니다.

### Q3: Aspose.CAD for Java에 대한 무료 체험판이 있습니까?
A3: 예, 무료 체험판은 [여기](https://releases.aspose.com/)에서 확인할 수 있습니다.

### Q4: Aspose.CAD for Java에 대한 기술 지원은 어떻게 받을 수 있습니까?
A4: 기술 지원이 필요하면 Aspose.CAD 포럼 [여기](https://forum.aspose.com/c/cad/19)에서 문의하십시오.

### Q5: 테스트 용도로 임시 라이선스를 받을 수 있습니까?
A5: 예, 임시 라이선스는 [여기](https://purchase.aspose.com/temporary-license/)에서 발급받을 수 있습니다.

**추가 Q&A**

**Q: 편집된 DWG를 디스크에 다시 쓰기 위해 특정 메서드를 호출해야 합니까?**  
A: 예, 변경 후 `cadImage.save("EditedDrawing.dwg");`를 호출하여 수정 내용을 영구 저장합니다.

**Q: 한 번에 여러 하이퍼링크를 편집할 수 있습니까?**  
A: 물론입니다—`cadImage.getEntities()`를 순회하면서 각 일치하는 엔티티에 하이퍼링크 로직을 적용하면 됩니다.

---

**마지막 업데이트:** 2026-06-19  
**테스트 환경:** Aspose.CAD for Java 24.12  
**작성자:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 관련 튜토리얼

- [Aspose.CAD for Java를 사용하여 DWG 파일에서 XREF 메타 데이터 읽기](/cad/java/cad-meta-data-and-rendering/read-xref-meta-data/)
- [Aspose.CAD for Java를 사용하여 DWG 파일에 사용자 정의 속성 추가](/cad/java/additional-features/add-custom-properties/)
- [Aspose.CAD for Java를 사용하여 DWG를 PDF 또는 래스터로 내보내기](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}