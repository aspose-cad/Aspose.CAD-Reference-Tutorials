---
title: Chuyển đổi DWG sang PDF tuân thủ - Hướng dẫn Aspose.CAD
linktitle: Chuyển đổi DWG sang PDF tuân thủ
second_title: Aspose.CAD .NET - Định dạng tệp CAD và BIM
description: Chuyển đổi DWG sang PDF tuân thủ bằng Aspose.CAD cho .NET. Thực hiện theo hướng dẫn của chúng tôi để được hướng dẫn từng bước.
type: docs
weight: 13
url: /vi/net/conversion-and-export/converting-dwg-to-compliance-pdf/
---
## Giới thiệu

Chào mừng bạn đến với hướng dẫn từng bước của chúng tôi về cách chuyển đổi tệp DWG sang PDF tuân thủ bằng Aspose.CAD cho .NET. Aspose.CAD là một API .NET mạnh mẽ cho phép các nhà phát triển làm việc với các định dạng tệp CAD một cách dễ dàng. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn quy trình chuyển đổi tệp DWG sang PDF tuân thủ bằng các ví dụ và giải thích chi tiết.

## Điều kiện tiên quyết

Trước khi chúng ta bắt đầu, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

-  Aspose.CAD cho .NET: Đảm bảo bạn đã tích hợp thư viện Aspose.CAD vào dự án .NET của mình. Bạn có thể tải nó xuống[đây](https://releases.aspose.com/cad/net/).

- Môi trường phát triển: Đã cài đặt môi trường phát triển .NET đang hoạt động và đảm bảo môi trường đó được cấu hình đúng.

- Tệp DWG mẫu: Tải xuống tệp DWG mẫu mà bạn muốn chuyển đổi sang PDF Tuân thủ.

## Nhập không gian tên

Trong dự án .NET của bạn, hãy nhập các vùng tên cần thiết để sử dụng các chức năng của Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

Bây giờ, hãy chia nhỏ quá trình chuyển đổi tệp DWG sang PDF tuân thủ thành nhiều bước.

## Bước 1: Tải tệp DWG

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

Aspose.CAD.Image cadImage = Aspose.CAD.Image.Load(sourceFilePath);
```

## Bước 2: Đặt tùy chọn Rasterization

 Tạo một thể hiện của`CadRasterizationOptions` và định cấu hình các thuộc tính của nó, chẳng hạn như màu nền, chiều rộng trang và chiều cao trang.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    BackgroundColor = Aspose.CAD.Color.White,
    PageWidth = 1600,
    PageHeight = 1600
};
```

## Bước 3: Tạo tùy chọn PDF

 Tạo một thể hiện của`PdfOptions` và thiết lập các tùy chọn rasterization vector.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions,
    CorePdfOptions = new PdfDocumentOptions { Compliance = PdfCompliance.PdfA1a }
};
```

## Bước 4: Lưu dưới dạng PDF (Tuân thủ A1a)

Lưu hình ảnh CAD dưới dạng PDF tuân thủ tuân thủ A1a.

```csharp
cadImage.Save(MyDir + "PDFA1_A.pdf", pdfOptions);
```

## Bước 5: Lưu dưới dạng PDF (Tuân thủ A1b)

Thay đổi loại tuân thủ thành A1b và lưu hình ảnh CAD dưới dạng PDF tuân thủ.

```csharp
pdfOptions.CorePdfOptions.Compliance = PdfCompliance.PdfA1b;
cadImage.Save(MyDir + "PDFA1_B.pdf", pdfOptions);
```

## Phần kết luận

Chúc mừng! Bạn đã chuyển đổi thành công tệp DWG sang PDF tuân thủ bằng Aspose.CAD cho .NET. Hướng dẫn này cung cấp hướng dẫn toàn diện cho các nhà phát triển muốn tích hợp khả năng chuyển đổi CAD vào ứng dụng của họ.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể chuyển đổi các định dạng CAD khác sang PDF tuân thủ bằng Aspose.CAD không?

Câu trả lời 1: Có, Aspose.CAD hỗ trợ nhiều định dạng CAD khác nhau, cho phép chuyển đổi sang PDF tuân thủ.

### Câu hỏi 2: Aspose.CAD có tương thích với .NET Core không?

Câu trả lời 2: Có, Aspose.CAD tương thích với cả .NET Framework và .NET Core.

### Câu 3: Có bất kỳ tùy chọn cấp phép nào cho Aspose.CAD không?

 Câu trả lời 3: Có, bạn có thể khám phá các tùy chọn cấp phép[đây](https://purchase.aspose.com/buy).

### Q4: Có bản dùng thử miễn phí không?

 A4: Có, bạn có thể dùng thử miễn phí[đây](https://releases.aspose.com/).

### Câu hỏi 5: Tôi có thể nhận hỗ trợ cho Aspose.CAD ở đâu?

A5: Tham quan[Diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) cho bất kỳ truy vấn liên quan đến hỗ trợ.