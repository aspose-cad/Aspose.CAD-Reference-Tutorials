---
title: Xuất hình ảnh 3D sang PDF - Hướng dẫn Aspose.CAD
linktitle: Xuất hình ảnh 3D sang PDF
second_title: Aspose.CAD .NET - Định dạng tệp CAD và BIM
description: Dễ dàng chuyển đổi hình ảnh CAD 3D sang PDF bằng Aspose.CAD cho .NET. Hãy làm theo hướng dẫn từng bước của chúng tôi để xuất PDF liền mạch.
weight: 10
url: /vi/net/3d-image-export/exporting-3d-images-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xuất hình ảnh 3D sang PDF - Hướng dẫn Aspose.CAD

## Giới thiệu

Bạn đang muốn xuất hình ảnh 3D sang PDF một cách liền mạch bằng Aspose.CAD cho .NET? Hướng dẫn từng bước này sẽ hướng dẫn bạn thực hiện quy trình, đảm bảo rằng bạn khai thác sức mạnh của Aspose.CAD để dễ dàng chuyển đổi hình ảnh 3D sang định dạng PDF.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

-  Aspose.CAD cho .NET: Đảm bảo rằng bạn đã cài đặt thư viện Aspose.CAD cho .NET. Nếu không, bạn có thể tải xuống từ[Trang tải xuống Aspose.CAD cho .NET](https://releases.aspose.com/cad/net/).

- Thư mục Tài liệu: Thiết lập một thư mục lưu trữ các tệp CAD của bạn và ghi lại đường dẫn.

## Nhập không gian tên

Trong dự án .NET của bạn, hãy nhập các vùng tên cần thiết để làm việc với Aspose.CAD. Thêm các dòng sau vào đầu tệp mã của bạn:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Bước 1: Tải hình ảnh CAD

 Bắt đầu bằng cách tải hình ảnh CAD mà bạn muốn xuất sang PDF. Sử dụng`Load` phương pháp từ thư viện Aspose.CAD. Thay thế`"conic_pyramid.dxf"` với đường dẫn đến tệp CAD của bạn.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Mã của bạn để tải hình ảnh CAD ở đây
}
```

## Bước 2: Định cấu hình tùy chọn Rasterization

 Định cấu hình các tùy chọn rasterization cho hình ảnh CAD. Đặt các tham số như chiều rộng trang, chiều cao trang và bố cục. Bỏ ghi chú dòng liên quan đến`TypeOfEntities` nếu thực thể của bạn là 3D.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

## Bước 3: Đặt tùy chọn PDF

Tạo các tùy chọn PDF và liên kết chúng với các tùy chọn tạo điểm ảnh.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Bước 4: Lưu dưới dạng PDF

Lưu hình ảnh CAD dưới dạng tệp PDF bằng các tùy chọn đã định cấu hình. Chỉ định đường dẫn đầu ra cho tệp PDF.

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Phần kết luận

Chúc mừng! Bạn đã xuất thành công hình ảnh 3D sang PDF bằng Aspose.CAD cho .NET. Hướng dẫn đơn giản này đảm bảo rằng bạn dễ dàng chuyển đổi các tệp CAD của mình sang định dạng dễ tiếp cận hơn.

## Câu hỏi thường gặp

### Câu hỏi 1: Aspose.CAD có tương thích với tất cả các định dạng tệp CAD không?

Câu trả lời 1: Có, Aspose.CAD hỗ trợ nhiều định dạng CAD, đảm bảo tính linh hoạt trong việc xử lý nhiều loại tệp khác nhau.

### Câu hỏi 2: Tôi có thể tùy chỉnh kích thước trang khi xuất sang PDF không?

A2: Chắc chắn rồi. Hướng dẫn trình bày cách định cấu hình chiều rộng và chiều cao của trang theo yêu cầu của bạn.

### Câu hỏi 3: Aspose.CAD có giấy phép tạm thời không?

 Câu trả lời 3: Có, bạn có thể lấy giấy phép tạm thời cho Aspose.CAD bằng cách truy cập[Giấy phép tạm thời](https://purchase.aspose.com/temporary-license/).

### Câu hỏi 4: Tôi có thể tìm thêm hỗ trợ hoặc thảo luận cộng đồng ở đâu?

 A4: Đi đến[Diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để được hỗ trợ và gắn kết với cộng đồng.

### Câu hỏi 5: Có phiên bản dùng thử miễn phí của Aspose.CAD không?

 Câu trả lời 5: Có, bạn có thể khám phá các tính năng của Aspose.CAD bằng cách truy cập vào[dùng thử miễn phí](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
