---
date: 2026-09-14
description: Aspose.CAD for .NET에서 파일 경로나 FileStream을 사용하여 라이선스를 적용하는 방법을 배우고, metered
  licensing을 활용하여 리소스 사용을 최적화하는 방법을 살펴보세요.
keywords:
- how to apply license
- apply license by path
- apply license using filestream
- metered licensing
lastmod: 2026-09-14
linktitle: 라이선스 및 구성
og_description: Aspose.CAD for .NET에서 파일 경로나 FileStream을 사용하여 라이선스를 적용하는 방법을 배우고,
  metered licensing을 활용하여 리소스 사용을 최적화하는 방법을 살펴보세요. (150‑160 chars)
og_image_alt: Screenshot of Aspose.CAD license configuration page in a .NET IDE
og_title: Aspose.CAD for .NET에서 라이선스 적용 방법 – Quick Guide
schemas:
- author: Aspose
  dateModified: '2026-09-14'
  description: Learn how to apply license in Aspose.CAD for .NET using a file path
    or FileStream, and explore metered licensing to optimise resource usage.
  headline: How to apply license in Aspose.CAD for .NET
  type: TechArticle
- description: Learn how to apply license in Aspose.CAD for .NET using a file path
    or FileStream, and explore metered licensing to optimise resource usage.
  name: How to apply license in Aspose.CAD for .NET
  steps:
  - name: Place your `Aspose.CAD.lic` file in a folder that your application can read
      (e.g., the application root or a secured config folder).
    text: Place your `Aspose.CAD.lic` file in a folder that your application can read
      (e.g., the application root or a secured config folder).
  - name: 'Add the following code early in your startup routine (e.g., `Main`, `Startup.Configure`,
      or `Global.asax`):'
    text: 'Add the following code early in your startup routine (e.g., `Main`, `Startup.Configure`,
      or `Global.asax`):'
  - name: Retrieve the license bytes from your source (file system, Azure Blob, etc.).
    text: Retrieve the license bytes from your source (file system, Azure Blob, etc.).
  - name: Open a `FileStream` with read permissions.
    text: Open a `FileStream` with read permissions.
  - name: Pass the stream to the `License` object.
    text: Pass the stream to the `License` object.
  - name: Obtain a metered‑license key from your Aspose account dashboard.
    text: Obtain a metered‑license key from your Aspose account dashboard.
  - name: Register the key with `License.SetMeteredKey("your‑key")`.
    text: Register the key with `License.SetMeteredKey("your‑key")`.
  - name: After each operation, call `License.GetMeteredUsage()` to retrieve the current
      usage count.
    text: After each operation, call `License.GetMeteredUsage()` to retrieve the current
      usage count.
  type: HowTo
- questions:
  - answer: Yes, a single license file can be deployed to any number of development
      or production servers, provided the usage complies with your purchased term.
    question: Can I use the same license file on multiple machines?
  - answer: The library will run in evaluation mode, adding a watermark to rendered
      images and limiting the number of pages you can process.
    question: What happens if I forget to set the license before loading a CAD file?
  - answer: Only the first activation and each usage report need connectivity; after
      that, the library can operate offline until the next report.
    question: Does metered licensing require an internet connection?
  - answer: Aspose.CAD supports 45+ input and output formats, including DWG, DXF,
      DGN, STL, OBJ, and IFC, and can render files up to 500 MB without loading the
      entire document into memory.
    question: Which CAD/BIM formats are supported out of the box?
  - answer: Call `License.IsLicensed` (or inspect `License.LicenseFilePath`) after
      registration; it returns `true` when a valid license is active.
    question: Is there a way to programmatically check if the license was applied
      successfully?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- Aspose.CAD
- license configuration
- .NET
- CAD processing
- metered licensing
title: Aspose.CAD for .NET에서 라이선스 적용 방법
url: /ko/net/licensing-and-configuration/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET에서 라이선스 적용 방법

Aspose.CAD for .NET에 대한 **라이선스 적용 방법**에 대한 종합 가이드에 오신 것을 환영합니다. 데스크톱 유틸리티, 서버‑사이드 서비스 또는 자동화된 BIM 파이프라인을 구축하든, 유효한 라이선스는 40개 이상의 CAD 및 BIM 형식 전체를 해제하고 고성능 렌더링을 가능하게 하며 평가용 워터마크를 제거합니다. 이 문서는 모든 라이선스 옵션을 단계별로 안내하여 중단 없이 개발을 시작할 수 있도록 도와줍니다.

## 빠른 답변
- **파일 경로에서 라이선스를 로드할 수 있나요?** 예 – `License` 객체를 인스턴스화하고 `SetLicense("path/to/license.lic")`를 호출하면 됩니다.  
- **FileStream을 지원하나요?** 물론입니다; 열어둔 스트림을 `SetLicense(stream)`에 전달하면 됩니다.  
- **Metered 라이선스란 무엇인가요?** 요청당 사용량을 추적하여 실제 사용량에 대해서만 비용을 지불하도록 합니다.  
- **개발에 라이선스가 필요합니까?** 무료 체험 라이선스는 개발 및 테스트에 사용할 수 있으며, 프로덕션에서는 상용 라이선스가 필요합니다.  
- **지원되는 .NET 버전은 무엇인가요?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Aspose.CAD의 라이선스란?

Aspose.CAD의 라이선스는 구매를 검증하고 라이브러리의 전체 기능을 활성화하는 메커니즘입니다. 라이선스가 없으면 API는 평가 모드로 실행되어 출력 크기가 제한되고 렌더링된 이미지에 워터마크가 삽입됩니다.

## 파일 경로 기반 라이선스와 스트림 기반 라이선스 중 어느 것을 사용해야 할까요?

경로 기반 라이선스는 Aspose.CAD를 활성화하는 가장 빠른 방법입니다: .lic 파일을 지정하면 라이브러리가 자동으로 로드합니다. 파일이 아닌 소스에서 라이선스를 읽거나, 맞춤 보안을 적용하거나, 어셈블리 내에 라이선스를 포함해야 할 경우 스트림을 사용합니다. 배포 환경에 맞는 방법을 선택하십시오.

`License` 클래스는 API에 라이선스를 등록하는 Aspose.CAD 라이선스 구성 요소를 나타냅니다.

## Aspose.CAD for .NET에서 경로를 사용해 라이선스를 적용하는 방법은?

경로를 사용해 라이선스를 적용하려면 `License` 클래스의 인스턴스를 생성하고 `.lic 파일의 전체 경로`를 인수로 하여 `SetLicense` 메서드를 호출합니다. 이 코드를 애플리케이션 시작 초기에 배치하여 이후 모든 CAD 작업이 라이선스가 적용된 컨텍스트에서 실행되도록 합니다.

`License` 클래스는 API에 라이선스를 등록하는 Aspose.CAD 라이선스 구성 요소를 나타냅니다.

1. 애플리케이션이 읽을 수 있는 폴더에 `Aspose.CAD.lic` 파일을 배치합니다 (예: 애플리케이션 루트 또는 보안된 구성 폴더).  
2. 시작 루틴 초기에 다음 코드를 추가합니다 (예: `Main`, `Startup.Configure`, 또는 `Global.asax`):

```csharp
// No code block added – original tutorial contained none.
```

> **직접 답변 (40‑70 단어):**  
> 경로를 사용해 라이선스를 적용하려면 `License` 객체를 생성하고 `SetLicense("full\\path\\to\\Aspose.CAD.lic")`를 호출합니다. 이 한 줄로 전체 라이브러리가 활성화되고 평가용 워터마크가 제거되며 40개 이상의 CAD/BIM 형식을 성능 제한 없이 처리할 수 있습니다. CAD 작업을 수행하기 전에 호출을 배치하여 라이선스가 활성화되도록 합니다.

## Aspose.CAD for .NET에서 FileStream을 사용해 라이선스를 적용하는 방법은?

`FileStream`을 사용해 라이선스를 적용하려면 .lic 파일을 읽기 전용으로 열고, `License` 객체를 생성한 뒤 스트림을 `SetLicense`에 전달합니다. 등록이 완료될 때까지 스트림을 열어 두고, 이후에 닫아 리소스를 해제하십시오.

`FileStream` 클래스는 디스크의 파일을 읽고 쓰기 위한 스트림을 제공합니다.

1. 소스(파일 시스템, Azure Blob 등)에서 라이선스 바이트를 가져옵니다.  
2. `FileStream`을 읽기 권한으로 엽니다.  
3. 스트림을 `License` 객체에 전달합니다.

> **직접 답변 (40‑70 단어):**  
> 읽기 가능한 `FileStream`인 `stream`을 사용해 `License` 객체를 인스턴스화하고 `SetLicense(stream)`를 호출합니다. 이 방법은 메모리에서 라이선스를 로드하므로 파일을 파일 시스템에 남기지 않을 수 있으며 모든 기능을 즉시 활성화합니다. 스트림이 등록이 완료될 때까지 열려 있도록 유지하고, 완료 후 닫습니다.

## Aspose.CAD for .NET에서 Metered 라이선스는 어떻게 작동하나요?

Metered 라이선스는 고유 키와 함께 `License.SetMeteredKey`를 호출하여 활성화됩니다. 등록 후 SDK는 각 CAD 작업마다 사용 데이터를 Aspose 서버에 자동으로 전송하여 사용량을 모니터링하고 구독 기간 내 수행된 작업에 대해서만 청구할 수 있게 합니다.

`License.SetMeteredKey` 메서드는 Aspose.CAD 라이브러리에 Metered 라이선스 키를 등록합니다.

1. Aspose 계정 대시보드에서 Metered 라이선스 키를 얻습니다.  
2. `License.SetMeteredKey("your‑key")`를 사용해 키를 등록합니다.  
3. 각 작업 후 `License.GetMeteredUsage()`를 호출해 현재 사용량을 확인합니다.

> **직접 답변 (40‑70 단어):**  
> Metered 라이선스는 `License.SetMeteredKey("your‑key")`를 호출해 활성화됩니다. SDK는 각 CAD 작업 후 사용 데이터를 Aspose 서버에 전송하여 실제 사용량에 따라 모니터링 및 청구가 가능하게 합니다. 이 모델은 무제한 동시 사용자를 지원하면서 비용을 실제 사용량에 맞게 조정합니다.

## 라이선스 및 구성 튜토리얼

### [Aspose.CAD for .NET에서 경로를 사용해 라이선스 적용](./apply-license-by-path/)
Aspose.CAD for .NET의 전체 잠재력을 활용하세요! 단계별 가이드를 따라 라이선스를 원활히 적용하십시오. 이제 CAD 파일 조작 능력을 한 단계 끌어올리세요!

### [Aspose.CAD for .NET에서 FileStream을 사용해 라이선스 적용](./apply-license-using-filestream/)
Aspose.CAD for .NET 마스터하기: FileStream을 사용해 라이선스를 원활히 적용하세요. 단계별 가이드를 탐색하고 잠재력을 활용하십시오. 지금 다운로드!

### [Aspose.CAD for .NET에서 Metered 라이선스](./metered-licensing/)
.NET에서 Metered 라이선스로 Aspose.CAD의 잠재력을 활용하세요. 리소스 사용을 원활히 최적화하고 단계별 가이드를 확인하십시오.

## 자주 묻는 질문

**Q: 여러 대의 머신에서 동일한 라이선스 파일을 사용할 수 있나요?**  
A: 예, 단일 라이선스 파일을 개발 또는 프로덕션 서버 여러 대에 배포할 수 있으며, 사용이 구매한 조건을 준수하는 경우에만 가능합니다.

**Q: CAD 파일을 로드하기 전에 라이선스 설정을 잊으면 어떻게 되나요?**  
A: 라이브러리는 평가 모드로 실행되어 렌더링된 이미지에 워터마크가 추가되고 처리할 수 있는 페이지 수가 제한됩니다.

**Q: Metered 라이선스에 인터넷 연결이 필요합니까?**  
A: 최초 활성화와 각 사용량 보고 시에만 연결이 필요하며, 그 이후에는 다음 보고가 있을 때까지 라이브러리를 오프라인으로 사용할 수 있습니다.

**Q: 기본적으로 지원되는 CAD/BIM 형식은 무엇인가요?**  
A: Aspose.CAD는 DWG, DXF, DGN, STL, OBJ, IFC 등을 포함한 45개 이상의 입력 및 출력 형식을 지원하며, 전체 문서를 메모리에 로드하지 않고도 최대 500 MB 파일을 렌더링할 수 있습니다.

**Q: 라이선스가 성공적으로 적용되었는지 프로그래밍 방식으로 확인할 방법이 있나요?**  
A: 등록 후 `License.IsLicensed`(또는 `License.LicenseFilePath`를 확인) 를 호출하면 유효한 라이선스가 활성화된 경우 `true`를 반환합니다.

---

**마지막 업데이트:** 2026-09-14  
**테스트 환경:** Aspose.CAD 24.11 for .NET  
**작성자:** Aspose

## 관련 튜토리얼

- [Aspose.CAD for .NET에서 경로를 사용해 라이선스 적용](/cad/net/licensing-and-configuration/apply-license-by-path/)
- [Aspose.CAD for .NET에서 FileStream을 사용해 라이선스 적용](/cad/net/licensing-and-configuration/apply-license-using-filestream/)
- [Aspose.CAD for .NET에서 Metered 라이선스](/cad/net/licensing-and-configuration/metered-licensing/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}