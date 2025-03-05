---
title: Xuất DGN sang PDF trong Aspose.CAD cho .NET
linktitle: Xuất DGN sang PDF
second_title: Aspose.CAD .NET - Định dạng tệp CAD và BIM
description: Tìm hiểu cách xuất tệp DGN sang PDF dễ dàng với Aspose.CAD cho .NET. Hướng dẫn từng bước để thao tác liền mạch với tệp CAD.
type: docs
weight: 12
url: /vi/net/cad-export-formats/export-dgn-to-pdf/
---
## Giới thiệu

Trong thế giới phát triển .NET, Aspose.CAD là một thư viện mạnh mẽ hỗ trợ thao tác và chuyển đổi các tệp CAD. Một nhiệm vụ phổ biến mà các nhà phát triển thường gặp là xuất tệp DGN sang định dạng PDF. Trong hướng dẫn này, chúng ta sẽ hướng dẫn từng bước quy trình bằng cách sử dụng Aspose.CAD cho .NET.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có những điều sau:

- Kiến thức làm việc về C# và .NET framework.
-  Đã cài đặt thư viện Aspose.CAD cho .NET. Bạn có thể tải nó xuống[đây](https://releases.aspose.com/cad/net/).
- Ví dụ: tệp DGN mẫu, "Nikon_D90_Camera.dgn" cho hướng dẫn này.

## Nhập không gian tên

Trong dự án C# của bạn, hãy bắt đầu bằng cách nhập các vùng tên cần thiết:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Bước 1: Tải tệp DGN

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage cadImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Mã của bạn ở đây...
}
```

## Bước 2: Định cấu hình tùy chọn Rasterization

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Bước 3: Tạo tùy chọn PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Bước 4: Lưu dưới dạng PDF

```csharp
cadImage.Save(MyDir + "ExportDGNToPdf_out.pdf", pdfOptions);
```

## Phần kết luận

Chúc mừng! Bạn đã xuất thành công tệp DGN sang PDF bằng Aspose.CAD cho .NET. Hướng dẫn này bao gồm các bước thiết yếu, từ tải tệp DGN đến định cấu hình các tùy chọn tạo điểm ảnh và lưu kết quả đầu ra dưới dạng PDF.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.CAD cho .NET mà không cần có kiến thức về CAD trước không?

A1: Chắc chắn rồi! Aspose.CAD đơn giản hóa các tác vụ CAD phức tạp, giúp các nhà phát triển có nền tảng đa dạng có thể truy cập được.

### Câu hỏi 2: Tôi có thể tìm thêm ví dụ và tài liệu về Aspose.CAD ở đâu?

 A2: Khám phá[tài liệu](https://reference.aspose.com/cad/net/) để có hướng dẫn và ví dụ toàn diện.

### Câu 3: Aspose.CAD có bản dùng thử miễn phí không?

A3: Có, bạn có thể dùng thử miễn phí[đây](https://releases.aspose.com/).

### Câu hỏi 4: Làm cách nào tôi có thể nhận được giấy phép tạm thời cho Aspose.CAD?

 A4: Xin giấy phép tạm thời[đây](https://purchase.aspose.com/temporary-license/).

### Câu 5: Cần trợ giúp hoặc có thắc mắc?

A5: Tham quan[Diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để hỗ trợ cộng đồng.