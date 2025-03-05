---
title: Đặt màu nền và màu vẽ trong Aspose.CAD cho .NET
linktitle: Đặt màu nền và màu vẽ
second_title: Aspose.CAD .NET - Định dạng tệp CAD và BIM
description: Làm chủ Aspose.CAD cho .NET. Đặt màu nền và màu vẽ dễ dàng. Thực hiện theo hướng dẫn từng bước của chúng tôi.
type: docs
weight: 15
url: /vi/net/cad-features-and-support/setting-background-and-drawing-colors/
---
## Giới thiệu

Trong thế giới phát triển .NET năng động, Aspose.CAD nổi lên như một công cụ mạnh mẽ để xử lý các tệp Thiết kế hỗ trợ máy tính (CAD). Nếu bạn mong muốn nâng cao kỹ năng thao tác các bản vẽ CAD của mình thì hướng dẫn này chính là cánh cổng dành cho bạn. Chúng tôi sẽ đi sâu vào sự phức tạp của việc thiết lập nền và vẽ màu bằng Aspose.CAD cho .NET, cung cấp cho bạn hướng dẫn từng bước để đảm bảo sự rõ ràng và hiệu quả.

## Điều kiện tiên quyết

Trước khi chúng ta bắt đầu cuộc hành trình này, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

- Hiểu biết cơ bản về phát triển .NET.
-  Cài đặt Aspose.CAD cho .NET. Nếu bạn chưa làm điều này, bạn có thể tải xuống[đây](https://releases.aspose.com/cad/net/).
- Một tệp CAD mẫu để thử nghiệm. Bạn có thể tìm thấy một trong thư mục tài liệu của bạn.

## Nhập không gian tên

Trong dự án .NET của bạn, hãy bắt đầu bằng cách nhập các vùng tên cần thiết:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Bước 1: Tải tệp CAD

Bắt đầu bằng cách tải tệp CAD mà bạn muốn làm việc bằng đoạn mã sau:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Mã của bạn để xử lý thêm ở đây
}
```

## Bước 2: Định cấu hình tùy chọn Rasterization

 Tạo một thể hiện của`CadRasterizationOptions` và đặt các thuộc tính của nó để thiết lập màu nền và màu vẽ:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.BackgroundColor = Color.Beige;
rasterizationOptions.DrawType = CadDrawTypeMode.UseDrawColor;
rasterizationOptions.DrawColor = Color.Blue;
```

## Bước 3: Xuất sang PDF

 Tạo một thể hiện của`PdfOptions` và thiết lập`VectorRasterizationOptions` tài sản:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;

// Xuất CAD sang PDF
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## Bước 4: Xuất sang TIFF

 Tạo một thể hiện của`TiffOptions` và thiết lập`VectorRasterizationOptions` tài sản:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;

// Xuất CAD sang TIFF
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Phần kết luận

Chúc mừng! Bạn đã học thành công cách đặt nền và màu vẽ trong Aspose.CAD cho .NET. Hướng dẫn này trang bị cho bạn những kỹ năng để thao tác các tệp CAD một cách dễ dàng.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.CAD cho .NET với bất kỳ loại tệp CAD nào không?

Câu trả lời 1: Có, Aspose.CAD hỗ trợ nhiều định dạng CAD khác nhau, bao gồm DWG, DXF và DGN.

### Câu hỏi 2: Aspose.CAD có bản dùng thử miễn phí cho .NET không?

 Câu trả lời 2: Có, bạn có thể khám phá bản dùng thử miễn phí[đây](https://releases.aspose.com/).

### Câu hỏi 3: Tôi có thể tìm tài liệu chi tiết về Aspose.CAD cho .NET ở đâu?

 A3: Tham khảo tài liệu[đây](https://reference.aspose.com/cad/net/).

### Câu hỏi 4: Làm cách nào tôi có thể nhận được giấy phép tạm thời cho Aspose.CAD?

 A4: Có thể xin giấy phép tạm thời[đây](https://purchase.aspose.com/temporary-license/).

### Q5: Cần hỗ trợ hoặc muốn kết nối với cộng đồng?

 A5: Truy cập diễn đàn hỗ trợ[đây](https://forum.aspose.com/c/cad/19).
