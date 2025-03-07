---
title: Xuất bố cục cụ thể sang PDF - Hướng dẫn Aspose.CAD
linktitle: Xuất bố cục cụ thể sang PDF
second_title: Aspose.CAD .NET - Định dạng tệp CAD và BIM
description: Tìm hiểu cách xuất bố cục cụ thể sang PDF bằng Aspose.CAD cho .NET. Hướng dẫn từng bước để tích hợp liền mạch.
weight: 13
url: /vi/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xuất bố cục cụ thể sang PDF - Hướng dẫn Aspose.CAD

## Giới thiệu

Chào mừng bạn đến với hướng dẫn từng bước của chúng tôi về cách xuất bố cục cụ thể sang PDF bằng Aspose.CAD cho .NET. Aspose.CAD là một thư viện mạnh mẽ cho phép các nhà phát triển làm việc liền mạch với các định dạng tệp CAD. Trong hướng dẫn này, chúng tôi sẽ tập trung vào việc xuất các bố cục cụ thể từ tệp DWG sang PDF bằng Aspose.CAD trong môi trường .NET.

## Điều kiện tiên quyết

Trước khi chúng ta đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

-  Aspose.CAD for .NET Library: Đảm bảo rằng bạn đã cài đặt thư viện Aspose.CAD. Bạn có thể tải nó xuống[đây](https://releases.aspose.com/cad/net/).

- Môi trường phát triển: Thiết lập môi trường phát triển .NET, chẳng hạn như Visual Studio.

## Nhập không gian tên

Trong dự án .NET của bạn, hãy nhập các vùng tên cần thiết cho Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Bước 1: Tải tệp DWG

```csharp
// Đường dẫn đến thư mục tài liệu.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // Mã của bạn cho các bước tiếp theo sẽ có ở đây.
}
```

## Bước 2: Đặt tùy chọn CadRasterization

```csharp
// Tạo một phiên bản CadRasterizationOptions và đặt các thuộc tính khác nhau của nó
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

## Bước 3: Chỉ định tên bố cục

```csharp
// Chỉ định tên bố cục mong muốn
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

## Bước 4: Tạo PdfOptions

```csharp
// Tạo một phiên bản của PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// Đặt thuộc tính VectorRasterizationOptions
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Bước 5: Xuất sang PDF

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// Xuất DWG sang PDF
image.Save(MyDir, pdfOptions);
```

## Bước 6: Hiển thị thông báo thành công

```csharp
// Hiển thị thông báo thành công
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## Phần kết luận

Chúc mừng! Bạn đã học thành công cách xuất các bố cục cụ thể sang PDF bằng Aspose.CAD cho .NET. Hướng dẫn này cung cấp hướng dẫn chi tiết, đảm bảo bạn có thể tích hợp chức năng này vào dự án của mình một cách dễ dàng.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể xuất nhiều bố cục cùng lúc không?

 A1: Có, chỉ cần sửa đổi`Layouts` mảng ở Bước 3 để bao gồm tên của tất cả các bố cục mong muốn.

### Câu hỏi 2: Aspose.CAD có tương thích với các định dạng tệp CAD khác không?

Câu trả lời 2: Có, Aspose.CAD hỗ trợ nhiều định dạng CAD khác nhau, bao gồm DWG, DXF, DWF, v.v.

### Câu hỏi 3: Làm cách nào để điều chỉnh cài đặt đầu ra PDF?

 A3: Khám phá các thuộc tính của`CadRasterizationOptions` ở Bước 2 để biết các tùy chọn tùy chỉnh.

### Câu hỏi 4: Tôi có thể tìm thêm tài liệu Aspose.CAD ở đâu?

 A4: Tham quan[tài liệu](https://reference.aspose.com/cad/net/) để biết thông tin chuyên sâu.

### Câu 5: Có bản dùng thử miễn phí không?

 Câu trả lời 5: Có, bạn có thể truy cập bản dùng thử miễn phí[đây](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
