---
title: Thêm hình mờ vào bản vẽ CAD - Hướng dẫn Aspose.CAD
linktitle: Thêm hình mờ vào bản vẽ CAD
second_title: Aspose.CAD .NET - Định dạng tệp CAD và BIM
description: Nâng cao bản vẽ CAD của bạn bằng hình mờ chuyên nghiệp bằng Aspose.CAD cho .NET. Hãy làm theo hướng dẫn từng bước của chúng tôi để có các thiết kế được cá nhân hóa và hấp dẫn.
weight: 11
url: /vi/net/plt-and-watermarking/adding-watermarks-to-cad-drawings/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Thêm hình mờ vào bản vẽ CAD - Hướng dẫn Aspose.CAD

## Giới thiệu

Bạn đang muốn nâng cao bản vẽ CAD của mình bằng cách thêm hình mờ chuyên nghiệp? Aspose.CAD cho .NET cung cấp một giải pháp mạnh mẽ để tích hợp liền mạch hình mờ vào tệp CAD của bạn. Trong hướng dẫn từng bước này, chúng tôi sẽ hướng dẫn bạn quy trình thêm hình mờ bằng Aspose.CAD, đảm bảo bản vẽ của bạn không chỉ truyền tải thông tin quan trọng mà còn mang dấu ấn độc đáo của bạn.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có những điều sau:
-  Aspose.CAD cho .NET: Đảm bảo bạn đã cài đặt thư viện Aspose.CAD. Bạn có thể tải nó xuống[đây](https://releases.aspose.com/cad/net/).
- Thư mục tài liệu của bạn: Thiết lập một thư mục để lưu trữ các bản vẽ CAD của bạn.
Bây giờ, hãy bắt đầu thêm hình mờ vào bản vẽ CAD của bạn!

## Nhập không gian tên

Bắt đầu bằng cách nhập các vùng tên cần thiết vào dự án .NET của bạn:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Bước 1: Tải bản vẽ CAD

```csharp
// Đường dẫn đến thư mục tài liệu.
string MyDir = "Your Document Directory";
using (CadImage cadImage = (CadImage)Image.Load(MyDir + "Drawing11.dwg")) {
```

## Bước 2: Thêm Hình mờ dưới dạng MTEXT

```csharp
// Thêm MTEXT mới
CadMText watermark = new CadMText();
watermark.Text = "Watermark message";
watermark.InitialTextHeight = 40;
watermark.InsertionPoint = new Cad3DPoint(300, 40);
watermark.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(watermark);
```

## Bước 3: Hoặc Thêm Watermark dưới dạng văn bản

```csharp
// Ngoài ra, hãy thêm một thực thể đơn giản hơn như Văn bản
CadText text = new CadText();
text.DefaultValue = "Watermark text";
text.TextHeight = 40;
text.FirstAlignment = new Cad3DPoint(300, 40);
text.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(text);
```

## Bước 4: Xuất sang PDF

```csharp
// Xuất bản vẽ CAD có hình mờ sang PDF
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.Layouts = new[] { "Model" };
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "AddWatermark_out.pdf", pdfOptions);
```

Lặp lại các bước này cho các bản vẽ khác nhau và bạn sẽ có các tệp CAD có hình mờ trông chuyên nghiệp ngay lập tức!

## Phần kết luận

Chúc mừng! Bạn đã học thành công cách thêm hình mờ vào bản vẽ CAD của mình bằng Aspose.CAD cho .NET. Quy trình đơn giản nhưng mạnh mẽ này cho phép bạn cá nhân hóa thiết kế của mình trong khi vẫn duy trì tính toàn vẹn của bản vẽ kỹ thuật.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể tùy chỉnh hình thức của hình mờ không?

Trả lời 1: Có, bạn có thể tùy chỉnh văn bản, phông chữ, kích thước và vị trí của hình mờ theo sở thích của mình.

### Câu hỏi 2: Aspose.CAD có tương thích với các định dạng tệp CAD khác nhau không?

Câu trả lời 2: Aspose.CAD hỗ trợ nhiều định dạng tệp CAD khác nhau, bao gồm DWG và DXF, đảm bảo khả năng tương thích rộng rãi.

### Câu hỏi 3: Tôi có thể thêm nhiều hình mờ vào một bản vẽ CAD không?

A3: Chắc chắn rồi! Bạn có thể thêm bao nhiêu hình mờ nếu cần, mang lại sự linh hoạt cho các trường hợp sử dụng khác nhau.

### Câu hỏi 4: Aspose.CAD có cung cấp bản dùng thử miễn phí không?

Câu trả lời 4: Có, bạn có thể khám phá các tính năng của Aspose.CAD bằng bản dùng thử miễn phí. Hiểu rồi[đây](https://releases.aspose.com/).

### Câu hỏi 5: Tôi có thể tìm hỗ trợ cho Aspose.CAD ở đâu?

 Câu trả lời 5: Nếu có bất kỳ thắc mắc hoặc trợ giúp nào, hãy truy cập[Diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
