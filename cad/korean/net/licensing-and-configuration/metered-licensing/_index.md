---
date: 2026-09-19
description: Aspose CAD 메터드 라이선싱을 .NET에 구현하여 .NET 애플리케이션의 리소스 사용량을 효율적으로 모니터링하는 방법을
  배웁니다. 단계별 가이드를 따라하세요.
keywords:
- aspose cad metered licensing
- monitor resource usage .net
- aspose cad licensing
lastmod: 2026-09-19
linktitle: 메터드 라이선싱
og_description: Aspose CAD 메터드 라이선싱을 .NET에 구현하여 .NET 애플리케이션의 리소스 사용량을 효율적으로 모니터링하는
  방법을 배웁니다. 단계별 가이드를 따라하세요.
og_image_alt: Guide to Aspose CAD metered licensing for .NET developers
og_title: Aspose CAD 메터드 라이선싱을 .NET에서 사용하는 방법
schemas:
- author: Aspose
  dateModified: '2026-09-19'
  description: Learn how to implement Aspose CAD metered licensing in .NET to monitor
    resource usage .NET applications efficiently. Follow our step‑by‑step guide.
  headline: How to use Aspose CAD metered licensing in .NET
  type: TechArticle
- description: Learn how to implement Aspose CAD metered licensing in .NET to monitor
    resource usage .NET applications efficiently. Follow our step‑by‑step guide.
  name: How to use Aspose CAD metered licensing in .NET
  steps:
  - name: '**Aspose.CAD installed** – download the latest package from the [Aspose.CAD
      website](https://releases.aspose.com/cad/net/).'
    text: '**Aspose.CAD installed** – download the latest package from the [Aspose.CAD
      website](https://releases.aspose.com/cad/net/).'
  - name: '**Public and private keys** – obtain them from the [Aspose.CAD purchase
      page](https://purchase.aspose.com/buy).'
    text: '**Public and private keys** – obtain them from the [Aspose.CAD purchase
      page](https://purchase.aspose.com/buy).'
  - name: '**Basic .NET knowledge** – the guide assumes you are comfortable with C#
      projects targeting .NET 6 or later.'
    text: '**Basic .NET knowledge** – the guide assumes you are comfortable with C#
      projects targeting .NET 6 or later.'
  type: HowTo
- questions:
  - answer: Yes, the free trial version available from the [free trial version](https://releases.aspose.com/)
      supports metered licensing.
    question: Can I use metered licensing with a free trial?
  - answer: Monitoring before and after each major operation gives the most accurate
      insight, but you can also poll at regular intervals for long‑running services.
    question: How often should I check consumption quantities?
  - answer: Yes, the same public/private key pair can be reused across multiple projects
      and environments.
    question: Are metered keys reusable?
  - answer: The library will throw a licensing exception. You can either purchase
      additional credits or contact support via the [Aspose.CAD support](https://forum.aspose.com/c/cad/19)
      forum.
    question: What happens if I exceed my metered limit?
  - answer: Absolutely – explore [temporary licensing options](https://purchase.aspose.com/temporary-license/)
      for limited‑duration needs.
    question: Can I temporarily license Aspose.CAD for a short‑term project?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- aspose cad
- metered licensing
- .net resource monitoring
title: Aspose CAD 메터드 라이선싱을 .NET에서 사용하는 방법
url: /ko/net/licensing-and-configuration/metered-licensing/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose CAD 메터링 라이선스 (.NET)

## 소개

Aspose CAD 메터링 라이선스를 사용하면 .NET 애플리케이션이 소비하는 CAD/BIM API 호출 수를 제어할 수 있어 정확한 청구와 사용 인사이트를 제공합니다. 이 라이선스 모델을 통합하면 제한을 하드코딩하지 않고도 **.NET** 애플리케이션의 리소스 사용량을 **모니터링**할 수 있어 확장성과 비용 관리가 간편해집니다. 아래 가이드는 네임스페이스 가져오기부터 처리 전후 소비량 확인까지 모든 단계를 안내합니다.

## 빠른 답변
- **Metered 라이선스란?** 사전 정의된 크레딧을 각 API 호출이 소비하는 사용량 기반 모델입니다.  
- **시험 라이선스가 필요합니까?** 예 – 무료 체험은 메터링 키와 함께 작동합니다.  
- **소비량을 어떻게 확인할 수 있나요?** `License.GetConsumptionQuantity()` 메서드를 작업 전후에 호출합니다.  
- **스레드 안전합니까?** 예, 라이선스 엔진은 동시 .NET 작업을 위해 설계되었습니다.  
- **같은 키를 재사용할 수 있나요?** 물론입니다 – 동일한 공개/비공개 키 쌍을 프로젝트 간에 공유할 수 있습니다.

## Aspose CAD 메터링 라이선스란?

Aspose CAD 메터링 라이선스는 Aspose.CAD for .NET 라이브러리에서 발생하는 각 API 호출을 추적하는 사용량 기반 라이선스 방식입니다. 개발자는 영구 좌석을 구매하는 대신 실제로 소비한 리소스에 대해서만 비용을 지불할 수 있습니다.

## Aspose CAD와 메터링 라이선스를 사용하는 이유

메터링 라이선스를 사용하면 실제 API 사용량에만 비용을 부과하므로 비용을 정확히 제어할 수 있습니다. 선불 좌석 구매가 필요 없으며 워크로드에 따라 자동으로 확장되므로 사용량이 변동하는 간헐적 또는 클라우드 기반 처리에 이상적입니다.

## 전제 조건

1. **Aspose.CAD 설치** – 최신 패키지는 [Aspose.CAD 웹사이트](https://releases.aspose.com/cad/net/)에서 다운로드하십시오.  
2. **공개 및 비공개 키** – [Aspose.CAD 구매 페이지](https://purchase.aspose.com/buy)에서 얻으세요.  
3. **기본 .NET 지식** – 이 가이드는 .NET 6 이상을 대상으로 하는 C# 프로젝트에 익숙하다고 가정합니다.

## 네임스페이스 가져오기

필요한 `using` 지시문을 C# 파일 상단에 추가하여 컴파일러가 Aspose.CAD 클래스를 찾을 수 있게 합니다.

```csharp
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.License;
```

`License` 네임스페이스에는 메터링 라이선스에 필요한 클래스가 포함되어 있습니다.

## 메터링 키를 설정하는 방법?

`SetMeteredKey`는 공개 및 비공개 메터링 라이선스 키를 Aspose.CAD 엔진에 등록합니다. 애플리케이션 시작 시 한 번 이 메서드를 호출하고 Aspose에서 받은 키를 전달하십시오. 이렇게 하면 이후 모든 API 호출이 메터링 계정에 따라 추적됩니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## API 호출 전 소비량을 가져오는 방법?

`GetConsumptionQuantity`는 현재 시점까지 라이브러리가 소비한 총 크레딧 수를 반환합니다. CAD 작업을 수행하기 전에 이 값을 캡처하여 기준선을 설정하십시오. 처리 후 값과 비교하면 특정 작업이 정확히 얼마나 많은 크레딧을 사용했는지 알 수 있습니다.

```csharp
//ExStart:MeteredLicensing
// Access the setMeteredKey property and pass public and private keys as parameters
Aspose.CAD.Metered.SetMeteredKey("PublicKey", "PrivateKey");
```

## Aspose.CAD로 CAD 데이터를 처리하는 방법?

`CadImage`는 로드된 CAD 파일을 나타내며 렌더링 또는 변환 메서드를 제공합니다. 메터링 키를 설정한 후 CAD 파일을 `CadImage` 인스턴스로 로드하십시오. 그런 다음 래스터 형식으로 렌더링하거나 다른 CAD 유형으로 변환하거나 메타데이터를 추출할 수 있으며, 모든 작업이 메터링 할당량에 포함됩니다.

```csharp
// Get metered data amount before calling API
decimal amountbefore = Aspose.CAD.Metered.GetConsumptionQuantity();
// Display information
Console.WriteLine("Amount Consumed Before: " + amountbefore.ToString());
```

## API 호출 후 소비량을 가져오는 방법?

처리 후 다시 `GetConsumptionQuantity`를 호출하면 업데이트된 크레딧 총합을 얻을 수 있습니다. 이전에 기록한 기준선 값을 빼면 최근 작업이 소비한 크레딧 수를 계산할 수 있습니다. 이 정보는 사용 패턴을 모니터링하고 비용을 낮추도록 코드를 최적화하는 데 도움이 됩니다.

```csharp
// Do processing
//Aspose.CAD.FileFormats.Cad.CadImage image = (Aspose.CAD.FileFormats.Cad.CadImage)Aspose.CAD.Image.load("BlockRefDgn.dwg");
```

## 일반적인 문제 및 해결 방법

- **License가 설정되지 않은 오류:** `SetMeteredKey`가 모든 Aspose.CAD API 사용 전에 호출되었는지 확인하십시오.  
- **예상치 못한 높은 소비:** 루프에서 대량 파일을 의도치 않게 로드하고 있지는 않은지 확인하십시오; 각 로드는 별도 호출로 계산됩니다.  
- **스레드 안전성 문제:** 라이선스 엔진은 스레드 안전하지만 `SetMeteredKey`를 동시에 여러 번 호출하지 않도록 하세요.

## 자주 묻는 질문

**Q: 무료 체험으로 메터링 라이선스를 사용할 수 있나요?**  
A: 예, [무료 체험 버전](https://releases.aspose.com/)에서 제공되는 무료 체험은 메터링 라이선스를 지원합니다.

**Q: 소비량을 얼마나 자주 확인해야 하나요?**  
A: 각 주요 작업 전후에 모니터링하면 가장 정확한 인사이트를 얻을 수 있지만, 장기 실행 서비스의 경우 정기적으로 폴링해도 됩니다.

**Q: 메터링 키를 재사용할 수 있나요?**  
A: 예, 동일한 공개/비공개 키 쌍을 여러 프로젝트와 환경에서 재사용할 수 있습니다.

**Q: 메터링 한도를 초과하면 어떻게 되나요?**  
A: 라이브러리가 라이선스 예외를 발생시킵니다. 추가 크레딧을 구매하거나 [Aspose.CAD 지원](https://forum.aspose.com/c/cad/19) 포럼을 통해 지원팀에 연락할 수 있습니다.

**Q: 단기 프로젝트를 위해 Aspose.CAD를 임시 라이선스할 수 있나요?**  
A: 물론입니다 – 제한된 기간 요구에 맞는 [임시 라이선스 옵션](https://purchase.aspose.com/temporary-license/)을 확인하세요.

---

**마지막 업데이트:** 2026-09-19  
**테스트 환경:** Aspose.CAD 24.11 for .NET  
**작성자:** Aspose  






```csharp
// Get metered data amount after calling API
decimal amountafter = Aspose.CAD.Metered.GetConsumptionQuantity();
// Display information
Console.WriteLine("Amount Consumed After: " + amountafter.ToString());
//ExEnd:MeteredLicensing 
```

## 관련 튜토리얼

- [Aspose.CAD for .NET에서 라이선스 적용 – 단계별 튜토리얼](/cad/net/)
- [Aspose.CAD for .NET으로 CAD 도면을 PDF로 변환 및 내보내는 방법 – 튜토리얼](/cad/net/advanced-export-techniques/exporting-cad-drawings-to-pdf/)
- [Aspose.CAD for .NET에서 CAD를 PNG로 변환](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}