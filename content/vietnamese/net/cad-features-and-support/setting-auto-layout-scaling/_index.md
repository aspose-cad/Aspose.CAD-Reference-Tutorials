---
title: Đặt tỷ lệ bố cục tự động trong Aspose.CAD cho .NET
linktitle: Cài đặt tự động chia tỷ lệ bố cục
second_title: Aspose.CAD .NET - Định dạng tệp CAD và BIM
description: Nâng cao kết xuất CAD với Aspose.CAD cho .NET. Tìm hiểu cách thiết lập Tự động chia tỷ lệ bố cục để hiển thị tệp chính xác và có khả năng thích ứng.
type: docs
weight: 14
url: /vi/net/cad-features-and-support/setting-auto-layout-scaling/
---
Trong lĩnh vực phát triển .NET năng động, việc tối ưu hóa hiển thị các tệp Thiết kế hỗ trợ máy tính (CAD) là một khía cạnh quan trọng trong việc tạo ra các ứng dụng hiệu quả và hấp dẫn về mặt hình ảnh. Aspose.CAD cho .NET trao quyền cho các nhà phát triển nâng cao khả năng xử lý CAD của họ và trong hướng dẫn này, chúng tôi sẽ tập trung vào việc thiết lập Auto Layout Scaling bằng Aspose.CAD cho .NET.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

1.  Thư viện Aspose.CAD cho .NET: Tải xuống và cài đặt thư viện Aspose.CAD cho .NET từ[trang tải xuống](https://releases.aspose.com/cad/net/).

2. Môi trường phát triển: Có môi trường phát triển hoạt động với Visual Studio hoặc bất kỳ công cụ phát triển .NET nào khác được cài đặt.

3. Tệp CAD mẫu: Chuẩn bị tệp CAD mẫu ở định dạng DXF để thử nghiệm. Bạn có thể tìm thấy một cái cho mục đích thử nghiệm hoặc sử dụng cái của riêng bạn.

## Nhập không gian tên

Bắt đầu bằng cách nhập các vùng tên cần thiết vào dự án .NET của bạn để truy cập các chức năng do Aspose.CAD cung cấp.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Bước 1: Tải tệp CAD

Tải tệp CAD vào ứng dụng của bạn bằng thư viện Aspose.CAD.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Mã của bạn ở đây
}
```

## Bước 2: Định cấu hình tùy chọn Rasterization

 Tạo một thể hiện của`CadRasterizationOptions` và định cấu hình các thuộc tính của nó để tùy chỉnh quá trình rasterization.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

## Bước 3: Kích hoạt tính năng tự động chia tỷ lệ bố cục

 Bật Tự động chia tỷ lệ bố cục bằng cách đặt`AutomaticLayoutsScaling` thuộc tính thành đúng.

```csharp
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## Bước 4: Tạo tùy chọn PDF

 Tạo một thể hiện của`PdfOptions` để chỉ định định dạng đầu ra và thiết lập`VectorRasterizationOptions` thuộc tính được cấu hình trước đó`CadRasterizationOptions`.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Bước 5: Lưu kết quả

Xác định đường dẫn đầu ra và lưu tệp CAD với các cài đặt được áp dụng vào tệp PDF.

```csharp
MyDir = MyDir + "result_out.pdf";
image.Save(MyDir, pdfOptions);
```

## Phần kết luận

Chúc mừng! Bạn đã thiết lập thành công Tự động chia tỷ lệ bố cục bằng Aspose.CAD cho .NET. Sự tối ưu hóa này đảm bảo rằng các tệp CAD của bạn được hiển thị với độ chính xác và khả năng thích ứng, giúp ứng dụng của bạn trở nên linh hoạt hơn.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể áp dụng Auto Layout Scaling cho các định dạng tệp khác ngoài DXF không?

Câu trả lời 1: Có, Aspose.CAD for .NET hỗ trợ nhiều định dạng CAD khác nhau cho Auto Layout Scaling.

### Câu hỏi 2: Làm cách nào để xử lý lỗi trong quá trình kết xuất?

Câu trả lời 2: Bạn có thể triển khai cơ chế xử lý lỗi bằng cách sử dụng khối thử bắt để quản lý các ngoại lệ.

### Câu hỏi 3: Có giới hạn nào về kích thước tệp mà Aspose.CAD dành cho .NET có thể xử lý không?

Câu trả lời 3: Aspose.CAD được thiết kế để xử lý các tệp lớn nhưng hiệu suất có thể thay đổi tùy theo thông số kỹ thuật hệ thống của bạn.

### Q4: Tôi có thể tùy chỉnh thêm bản PDF đầu ra không?

Trả lời 4: Hoàn toàn có thể, Aspose.CAD cung cấp nhiều tùy chọn để tùy chỉnh đầu ra, bao gồm cài đặt màu sắc và cấu hình lớp.

### Câu hỏi 5: Tôi có thể tìm thêm tài nguyên và hỗ trợ cho Aspose.CAD ở đâu?

 A5: Khám phá[Diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để được cộng đồng hỗ trợ và tham khảo[tài liệu](https://reference.aspose.com/cad/net/) để biết thông tin chi tiết.