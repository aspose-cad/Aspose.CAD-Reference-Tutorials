---
date: 2026-07-18
description: Aspose CAD 변환을 사용하면 IFC를 PNG로, IGES를 PDF로 손쉽게 내보낼 수 있습니다. Aspose.CAD
  for .NET을 사용하여 CAD 파일을 몇 분 만에 변환하는 방법을 단계별로 알아보세요.
keywords:
- aspose cad conversion
- export cad to png
- convert iges to pdf
lastmod: 2026-07-18
linktitle: 이미지 형식으로 내보내기
og_description: Aspose CAD 변환을 통해 IFC를 PNG로, IGES를 PDF로 빠르게 내보낼 수 있습니다. Aspose.CAD
  for .NET으로 원활한 CAD 파일 처리를 위한 가이드를 확인하세요.
og_image_alt: Guide showing Aspose CAD conversion from CAD files to PNG and PDF
og_title: 'Aspose CAD 변환: 이미지 형식으로 내보내기'
schemas:
- author: Aspose
  dateModified: '2026-07-18'
  description: Aspose CAD conversion lets you effortlessly export IFC to PNG and IGES
    to PDF. Learn step‑by‑step how to convert CAD files with Aspose.CAD for .NET in
    minutes.
  headline: 'Aspose CAD Conversion: Exporting to Image Formats'
  type: TechArticle
- questions:
  - answer: Yes, iterate over a folder with `foreach (var file in Directory.GetFiles(path,
      "*.ifc")) { var img = new Image(file); img.Save(Path.ChangeExtension(file, ".png"),
      ImageFormat.Png); }`. The `Directory.GetFiles` method returns the names of files
      (including their paths) that match a specified pattern in a directory.
    question: Can I convert multiple CAD files in one batch?
  - answer: Layer visibility is respected; you can toggle layers via `LoadOptions`
      before saving, ensuring only selected layers appear in the output.
    question: Does Aspose.CAD preserve layer information in the exported image?
  - answer: The library comfortably processes files up to **2 GB**; larger files should
      be split or streamed using `LoadOptions.MemoryLimit`.
    question: What is the maximum file size Aspose.CAD can handle?
  - answer: Yes—by saving as `ImageFormat.Pdf` the output retains vector data, allowing
      infinite scaling without quality loss.
    question: Is there support for converting CAD to vector‑based PDFs?
  - answer: A single Aspose.CAD license covers all supported .NET runtimes (Framework,
      Core, and .NET 5+).
    question: Do I need a separate license for each .NET platform?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- aspose cad
- cad conversion
- export cad to png
- iges to pdf
- ifc to png
title: 'Aspose CAD 변환: 이미지 형식으로 내보내기'
url: /ko/net/exporting-to-image-formats/
weight: 39
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose CAD 변환: 이미지 형식으로 내보내기

현대 엔지니어링 및 디자인 워크플로에서 **aspose cad conversion**은 복잡한 CAD 및 BIM 파일을 보편적으로 볼 수 있는 이미지 형식으로 변환하는 데 필수적입니다. IFC 모델의 빠른 미리보기를 공유하거나 IGES 도면에서 인쇄 가능한 PDF를 생성해야 할 경우, 이 튜토리얼은 Aspose.CAD for .NET을 사용하여 정확한 단계별 과정을 안내합니다. PNG, PDF 및 기타 래스터 형식으로 내보낼 때도 기하학, 색상 및 레이어를 그대로 유지하는 방법을 확인할 수 있습니다.

## 빠른 답변
- **Aspose.CAD가 내보낼 수 있는 형식은 무엇인가요?** PNG, JPEG, PDF, TIFF 등을 포함한 20가지 이상의 이미지 유형에 대해 30개 이상의 CAD/BIM 형식을 지원합니다.  
- **개발에 라이선스가 필요합니까?** 평가용 무료 체험판을 사용할 수 있지만, 실제 운영을 위해서는 상용 라이선스가 필요합니다.  
- **지원되는 .NET 버전은 무엇입니까?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.  
- **대용량 파일을 처리할 수 있습니까?** 예 – Aspose.CAD는 전체 문서를 메모리에 로드하지 않고도 2 GB까지 파일을 처리합니다.  
- **추가 소프트웨어가 필요합니까?** 외부 CAD 도구가 필요하지 않으며, 라이브러리가 모든 변환을 내부적으로 수행합니다.

## Aspose CAD 변환이란?
`Image` 클래스는 메모리에 로드된 CAD 문서를 나타내며 다양한 형식으로 저장하는 메서드를 제공합니다. Aspose CAD 변환은 Aspose.CAD for .NET을 사용하여 CAD/BIM 파일을 다른 형식으로 변환합니다. `Image`로 소스를 로드하고 대상 형식을 선택한 뒤 `Save`를 호출합니다. 이 두 단계 패턴은 레이어, 라인 두께 및 텍스처를 보존하여 원본 디자인 의도를 유지합니다.

## IFC 파일을 PNG로 내보내는 방법?
`Image` 클래스는 메모리에 로드된 CAD 문서를 나타내며 다양한 형식으로 저장하는 메서드를 제공합니다. `new Image("model.ifc")`로 IFC 파일을 로드하고 `image.Save("model.png", ImageFormat.Png)`를 호출합니다. Aspose.CAD는 3‑D 기하학을 읽어 래스터 이미지로 평면화하고 색 깊이와 투명성을 유지하는 고해상도 PNG를 작성합니다. 배치 처리를 위해 폴더를 순회하며 각 파일을 저장할 수 있습니다.

## IGES 파일을 PDF로 내보내는 방법?
`Image` 클래스는 메모리에 로드된 CAD 문서를 나타내며 다양한 형식으로 저장하는 메서드를 제공합니다. IGES 파일에서 `Image` 인스턴스를 생성하고 `image.Save("drawing.pdf", ImageFormat.Pdf)`를 호출합니다. 변환은 벡터 정보, 라인 스타일 및 주석을 보존하여 세부 사항 손실 없이 모든 뷰어에서 열 수 있는 PDF를 생성합니다. 인쇄용 PDF를 위해 DPI를 높이고 싶다면 선택적 `Resolution` 속성을 사용하십시오.

## .NET에서 Aspose.CAD를 사용하는 이유
Aspose.CAD는 **30개 이상의 입력 형식**(IFC, IGES, DWG, DWF, STL 등)과 **20개 이상의 이미지 유형**을 출력할 수 있습니다. 일반 서버에서 수백 페이지 도면을 5 초 이내에 처리하며, 완전 오프라인으로 동작해 네이티브 CAD 설치가 전혀 필요 없습니다. 이러한 정량적 이점은 기업 및 프리랜서 개발자 모두에게 비용 효율적이고 고성능인 선택이 됩니다.

## 일반적인 함정 및 전문가 팁
`LoadOptions` 클래스는 메모리 제한 설정이나 레이어 지정 등 CAD 파일 로드 방식을 사용자 정의할 수 있게 해줍니다.  
`FontSettings` 객체는 변환 중에 사용되는 글꼴 대체 및 임베딩 규칙을 정의합니다.  

- **Pitfall:** 기본 DPI를 무시하면 저해상도 이미지가 생성됩니다.  
  **Pro tip:** 인쇄 품질 PNG를 위해 `image.DpiX`와 `image.DpiY`를 300으로 설정하십시오.  
- **Pitfall:** 대용량 IGES 파일은 메모리 제한을 초과할 수 있습니다.  
  **Pro tip:** `LoadOptions`와 `MemoryLimit`을 사용해 파일을 청크 단위로 스트리밍하십시오.  
- **Pitfall:** IFC 모델에 글꼴이 없으면 자리 표시자 텍스트가 표시됩니다.  
  **Pro tip:** 변환 전에 `FontSettings` 객체를 사용해 필요한 글꼴을 임베드하십시오.

## 이미지 형식 내보내기 튜토리얼
### [IFC 파일을 PNG로 내보내기 - Aspose.CAD 튜토리얼](./exporting-ifc-files-to-png/)
Aspose.CAD for .NET을 탐색하여 원활한 IFC → PNG 변환을 구현하십시오. 효율적인 CAD 파일 처리를 위해 지금 다운로드하세요.
### [IGES 파일을 PDF로 내보내기 - Aspose.CAD 가이드](./exporting-iges-files-to-pdf/)
Aspose.CAD for .NET을 사용해 IGES 파일을 PDF로 손쉽게 내보내는 방법을 배워보세요. 정확한 CAD 파일 조작을 위한 단계별 가이드를 따라가십시오.

## 자주 묻는 질문

**Q: 여러 CAD 파일을 한 번에 배치 처리할 수 있나요?**  
A: 예, 다음과 같이 폴더를 순회하면 됩니다. `foreach (var file in Directory.GetFiles(path, "*.ifc")) { var img = new Image(file); img.Save(Path.ChangeExtension(file, ".png"), ImageFormat.Png); }`.  
`Directory.GetFiles` 메서드는 지정된 패턴에 일치하는 파일(경로 포함)의 이름을 반환합니다.

**Q: Aspose.CAD가 내보낸 이미지에서 레이어 정보를 보존합니까?**  
A: 레이어 가시성이 유지됩니다; 저장하기 전에 `LoadOptions`를 통해 레이어를 토글하면 선택된 레이어만 출력에 포함됩니다.

**Q: Aspose.CAD가 처리할 수 있는 최대 파일 크기는 얼마입니까?**  
A: 라이브러리는 **2 GB**까지의 파일을 편안하게 처리합니다; 더 큰 파일은 `LoadOptions.MemoryLimit`을 사용해 분할하거나 스트리밍해야 합니다.

**Q: CAD를 벡터 기반 PDF로 변환하는 기능이 있습니까?**  
A: 예—`ImageFormat.Pdf`로 저장하면 출력이 벡터 데이터를 유지하므로 품질 손실 없이 무한히 확대할 수 있습니다.

**Q: 각 .NET 플랫폼마다 별도의 라이선스가 필요합니까?**  
A: 단일 Aspose.CAD 라이선스로 모든 지원 .NET 런타임(Framework, Core, .NET 5+)을 커버합니다.

**마지막 업데이트:** 2026-07-18  
**테스트 환경:** Aspose.CAD 24.12 for .NET  
**작성자:** Aspose

## 관련 튜토리얼

- [IFC 파일을 PNG로 내보내기 - Aspose.CAD 튜토리얼](/cad/net/exporting-to-image-formats/exporting-ifc-files-to-png/)
- [IGES 파일을 PDF로 내보내기 - Aspose.CAD 가이드](/cad/net/exporting-to-image-formats/exporting-iges-files-to-pdf/)
- [Aspose.CAD for .NET에서 CAD 레이아웃을 래스터 이미지 형식으로 내보내기](/cad/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}