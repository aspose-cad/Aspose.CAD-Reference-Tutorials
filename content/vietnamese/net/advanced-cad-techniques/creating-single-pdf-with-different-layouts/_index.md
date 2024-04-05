---
title: Tạo một tệp PDF với các bố cục khác nhau - Hướng dẫn Aspose.CAD
linktitle: Tạo một tệp PDF với các bố cục khác nhau
second_title: Aspose.CAD .NET - Định dạng tệp CAD và BIM
description: Tạo một tệp PDF với các bố cục khác nhau bằng Aspose.CAD cho .NET. Hãy làm theo hướng dẫn từng bước của chúng tôi để tích hợp liền mạch và tạo PDF hiệu quả.
type: docs
weight: 13
url: /vi/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
---
## Giới thiệu

Bạn đang muốn tạo một tài liệu PDF từ bản vẽ CAD với các bố cục khác nhau bằng Aspose.CAD cho .NET? Hướng dẫn từng bước này sẽ hướng dẫn bạn thực hiện quy trình, giúp bạn đạt được sự tích hợp liền mạch và tạo PDF hiệu quả. Aspose.CAD cho .NET cung cấp các tính năng mạnh mẽ để thao tác các bản vẽ CAD theo chương trình và trong hướng dẫn này, chúng tôi sẽ tập trung vào việc tạo một tệp PDF duy nhất với các bố cục khác nhau.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có các điều kiện tiên quyết sau:

-  Aspose.CAD cho .NET: Đảm bảo bạn đã cài đặt Aspose.CAD cho .NET. Bạn có thể tải nó xuống từ[đây](https://releases.aspose.com/cad/net/).

- Môi trường phát triển: Thiết lập môi trường phát triển .NET và có hiểu biết cơ bản về lập trình C#.

## Nhập không gian tên

Trong dự án C# của bạn, hãy bao gồm các vùng tên cần thiết để tận dụng các chức năng của Aspose.CAD cho .NET:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Bước 1: Tải hình ảnh CAD

```csharp
// Đường dẫn đến thư mục tài liệu.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // Mã của bạn cho Bước 1 ở đây
}
```

## Bước 2: Tùy chỉnh tùy chọn Rasterization

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// Kích thước tùy chỉnh cho một số bố cục
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

## Bước 3: Xác định các tùy chọn PDF

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

## Bước 4: Lưu dưới dạng PDF

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

Bây giờ bạn đã tạo thành công một tài liệu PDF với các bố cục khác nhau bằng Aspose.CAD cho .NET. Vui lòng khám phá thêm các tính năng và tùy chỉnh mã theo yêu cầu cụ thể của bạn.

## Phần kết luận

Trong hướng dẫn này, chúng tôi đã đề cập đến quá trình tạo một tệp PDF từ bản vẽ CAD với các bố cục khác nhau bằng Aspose.CAD cho .NET. Thư viện mạnh mẽ này đơn giản hóa các tác vụ thao tác CAD và mang lại sự linh hoạt cho nhiều tình huống khác nhau.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.CAD cho .NET với các định dạng CAD khác không?

Câu trả lời 1: Có, Aspose.CAD cho .NET hỗ trợ nhiều định dạng CAD khác nhau như DWG, DXF, DGN, v.v.

### Q2: Có bản dùng thử miễn phí không?

 Câu trả lời 2: Có, bạn có thể khám phá bản dùng thử miễn phí[đây](https://releases.aspose.com/).

### Câu 3: Làm cách nào tôi có thể nhận được hỗ trợ cho Aspose.CAD cho .NET?

 A3: Tham quan[Diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để hỗ trợ cộng đồng.

### Q4: Tôi có thể tìm tài liệu chi tiết ở đâu?

 A4: Tham khảo tài liệu[đây](https://reference.aspose.com/cad/net/).

### Câu hỏi 5: Tôi có thể mua giấy phép Aspose.CAD cho .NET không?

 A5: Có, bạn có thể mua giấy phép[đây](https://purchase.aspose.com/buy).