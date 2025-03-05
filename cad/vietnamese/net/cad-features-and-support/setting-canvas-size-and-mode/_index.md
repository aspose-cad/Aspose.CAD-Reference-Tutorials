---
title: Đặt kích thước và chế độ Canvas trong Aspose.CAD cho .NET
linktitle: Đặt kích thước và chế độ canvas
second_title: Aspose.CAD .NET - Định dạng tệp CAD và BIM
description: Khám phá hướng dẫn từng bước về cách đặt kích thước và chế độ canvas trong Aspose.CAD cho .NET. Tối ưu hóa kết xuất CAD của bạn một cách dễ dàng bằng cách sử dụng hướng dẫn toàn diện này.
type: docs
weight: 16
url: /vi/net/cad-features-and-support/setting-canvas-size-and-mode/
---
## Giới thiệu

Bạn đã sẵn sàng khám phá toàn bộ tiềm năng của Aspose.CAD cho .NET và cách mạng hóa trải nghiệm kết xuất CAD của mình chưa? Trong hướng dẫn từng bước này, chúng ta sẽ đi sâu vào sự phức tạp của việc thiết lập kích thước và chế độ canvas bằng thư viện Aspose.CAD mạnh mẽ. Cho dù bạn là nhà phát triển dày dạn kinh nghiệm hay mới bắt đầu, hướng dẫn này sẽ hướng dẫn bạn qua quy trình, đảm bảo bạn khai thác các khả năng của Aspose.CAD một cách hiệu quả.

## Điều kiện tiên quyết

Trước khi chúng ta đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

-  Thư viện Aspose.CAD: Tải xuống và cài đặt thư viện Aspose.CAD từ[Trang web Aspose.CAD](https://releases.aspose.com/cad/net/).

- Môi trường phát triển: Đảm bảo bạn đã thiết lập môi trường phát triển .NET trên máy của mình.

-  Tệp CAD mẫu: Đối với hướng dẫn này, chúng tôi sẽ sử dụng tệp DXF mẫu. Bạn có thể tìm thấy một trong[Tài liệu Aspose.CAD](https://reference.aspose.com/cad/net/).

## Nhập không gian tên

Để bắt đầu, hãy nhập các vùng tên cần thiết vào đầu ứng dụng .NET của bạn:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Bước 1: Tải tệp CAD

Bắt đầu bằng cách tải tệp CAD bằng mã sau:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    //Mã của bạn cho các bước tiếp theo sẽ có ở đây
}
```

## Bước 2: Tạo CadRasterizationOptions

 Tạo một thể hiện của`CadRasterizationOptions` và thiết lập thuộc tính của nó:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

## Bước 3: Tạo PdfOptions

 Tạo một thể hiện của`PdfOptions` và thiết lập nó`VectorRasterizationOptions` tài sản:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Bước 4: Xuất sang PDF

Xuất tệp CAD sang PDF bằng các tùy chọn đã định cấu hình:

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## Bước 5: Tạo TiffOptions

 Tạo một thể hiện của`TiffOptions` và thiết lập nó`VectorRasterizationOptions` tài sản:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Bước 6: Xuất sang TIFF

Xuất tệp CAD sang TIFF bằng các tùy chọn đã định cấu hình:

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Phần kết luận

Chúc mừng! Bạn đã đặt thành công kích thước và chế độ canvas trong Aspose.CAD cho .NET. Tính năng mạnh mẽ này mở ra vô số khả năng kết xuất CAD. Thử nghiệm với các tùy chọn khác nhau và khám phá toàn bộ tiềm năng của Aspose.CAD trong các ứng dụng .NET của bạn.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.CAD với các thư viện .NET khác không?

Câu trả lời 1: Có, Aspose.CAD tích hợp liền mạch với các thư viện .NET khác, cung cấp các khả năng nâng cao để thao tác CAD.

### Câu hỏi 2: Aspose.CAD có bản dùng thử miễn phí không?

 Câu trả lời 2: Có, bạn có thể khám phá các tính năng của Aspose.CAD bằng bản dùng thử miễn phí. Thăm nom[đây](https://releases.aspose.com/) để bắt đầu.

### Câu 3: Làm cách nào tôi có thể nhận được hỗ trợ cho Aspose.CAD?

 A3: Để được hỗ trợ và thảo luận, hãy truy cập[Diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Câu hỏi 4: Tôi có thể tìm tài liệu toàn diện về Aspose.CAD ở đâu?

 A4: Hãy tham khảo[Tài liệu Aspose.CAD](https://reference.aspose.com/cad/net/) để biết thông tin chi tiết và ví dụ.

### Câu hỏi 5: Làm cách nào để mua Aspose.CAD cho .NET?

 A5: Để mua Aspose.CAD, hãy truy cập[trang mua hàng](https://purchase.aspose.com/buy).