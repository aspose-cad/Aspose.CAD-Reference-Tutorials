---
title: Java용 Aspose.CAD를 사용하여 이미지를 DXF 형식으로 내보내기
linktitle: Java를 사용하여 이미지를 DXF 형식으로 내보내기
second_title: Aspose.CAD 자바 API
description: Aspose.CAD for Java를 사용하여 이미지를 DXF 형식으로 내보내는 원활한 프로세스를 살펴보세요. 단계별 가이드, FAQ 등.
weight: 15
url: /ko/java/additional-features/export-images-to-dxf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java용 Aspose.CAD를 사용하여 이미지를 DXF 형식으로 내보내기

## 소개

Aspose.CAD for Java를 사용하여 이미지를 DXF 형식으로 내보내는 방법에 대한 포괄적인 튜토리얼에 오신 것을 환영합니다. Aspose.CAD는 개발자가 프로그래밍 방식으로 CAD 도면을 작업할 수 있게 해주는 강력한 Java 라이브러리입니다. 이 튜토리얼에서는 이미지를 DXF 형식으로 내보내는 과정을 안내하고 이 작업을 수행하기 위한 다양한 단계와 기술을 보여줍니다.

## 전제 조건

시작하기 전에 다음 사항이 있는지 확인하세요.

- Java 프로그래밍에 대한 기본 이해.
-  Java 라이브러리용 Aspose.CAD가 설치되었습니다. 당신은 그것을 다운로드 할 수 있습니다[여기](https://releases.aspose.com/cad/java/).
- Aspose.CAD에 대한 유효한 라이센스 또는 임시 라이센스. 그것을 얻으십시오[여기](https://purchase.aspose.com/temporary-license/).
- 테스트용 DXF 형식의 일부 샘플 이미지.

## 네임스페이스 가져오기

Java 프로젝트에서 Aspose.CAD에 필요한 네임스페이스를 가져옵니다.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadconsts.CadEntityTypeName;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
import java.io.File;
import static java.lang.System.in;
```

## 1단계: 문서별로 새 글꼴 설정

```java
// 리소스 디렉터리의 경로입니다.
String dataDir = "Your Document Directory" + "DXFDrawings/";

File[] files = new File(dataDir).listFiles();
for (File file : files) {
    String extension = GetFileExtension(file);
    if (extension.equals(".dxf")) {
        CadImage cadImage = (CadImage)Image.load(file.getName());
        for (Object style : cadImage.getStyles()) {
            ((CadStyleTableObject)style).setPrimaryFontName("Broadway");
        }
        cadImage.save(file.getName() + "_font.dxf");
    }
}
```

## 2단계: 모든 "직선" 선 숨기기

```java
CadImage cadImageEntity = (CadImage)Image.load(file.getName());
for (CadBaseEntity entity : cadImageEntity.getEntities()) {
    if (entity.getTypeName() == CadEntityTypeName.LINE) {
        entity.setVisible((short)0);
    }
}
cadImageEntity.save(file.getName() + "_lines.dxf");
```

## 3단계: 텍스트 조작

```java
CadImage cadImageText = (CadImage)Image.load(file.getName());
for (CadBaseEntity entity : cadImageText.getEntities()) {
    if (entity.getTypeName() == CadEntityTypeName.TEXT) {
        ((CadText)entity).setDefaultValue("New text here!!! :)");
        break;
    }
}
cadImageText.save(file.getName() + "_text.dxf");
```

디렉터리의 각 DXF 파일에 대해 이 단계를 반복합니다.

## 결론

축하해요! Aspose.CAD for Java를 사용하여 이미지를 DXF 형식으로 내보내는 방법을 성공적으로 배웠습니다. 이 튜토리얼에서는 글꼴 설정, 선 숨기기, CAD 이미지 내 텍스트 조작 등 필수 단계를 다루었습니다.

## FAQ

### Q1: 라이선스 없이 Java용 Aspose.CAD를 사용할 수 있나요?

 A1: 사용 가능한 임시 라이센스로 사용할 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).

### Q2: Aspose.CAD 문서는 어디서 찾을 수 있나요?

 A2: 문서를 사용할 수 있습니다.[여기](https://reference.aspose.com/cad/java/).

### Q3: Aspose.CAD에 대한 지원은 어떻게 받나요?

 A3: 지원 포럼을 방문하세요.[여기](https://forum.aspose.com/c/cad/19).

### Q4: Java용 Aspose.CAD를 어디서 다운로드할 수 있나요?

 A4: 라이브러리 다운로드[여기](https://releases.aspose.com/cad/java/).

### Q5: 무료 평가판이 제공됩니까?

 A5: 예, 무료 평가판을 받을 수 있습니다.[여기](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
