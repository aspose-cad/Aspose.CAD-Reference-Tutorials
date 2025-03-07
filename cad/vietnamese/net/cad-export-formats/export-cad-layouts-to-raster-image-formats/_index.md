---
title: Xuất bố cục CAD sang định dạng hình ảnh raster trong Aspose.CAD cho .NET
linktitle: Xuất bố cục CAD sang định dạng hình ảnh raster
second_title: Aspose.CAD .NET - Định dạng tệp CAD và BIM
description: Tìm hiểu cách xuất bố cục CAD sang hình ảnh raster bằng Aspose.CAD cho .NET. Hãy làm theo hướng dẫn từng bước của chúng tôi để chuyển đổi liền mạch.
weight: 10
url: /vi/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xuất bố cục CAD sang định dạng hình ảnh raster trong Aspose.CAD cho .NET

## Giới thiệu

Bạn đang tìm cách chuyển đổi hiệu quả bố cục CAD sang định dạng hình ảnh raster bằng Aspose.CAD cho .NET? Hướng dẫn từng bước này sẽ hướng dẫn bạn thực hiện quy trình, cung cấp hướng dẫn chi tiết và đoạn mã để thực hiện công việc một cách liền mạch. Cho dù bạn là nhà phát triển dày dạn kinh nghiệm hay người mới làm quen với Aspose.CAD, hướng dẫn này sẽ đáp ứng mọi cấp độ chuyên môn.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có những điều sau:

- Aspose.CAD for .NET Library: Đảm bảo rằng bạn đã cài đặt thư viện Aspose.CAD. Nếu không, bạn có thể tải xuống từ[Trang web Aspose.CAD](https://releases.aspose.com/cad/net/).

- Tệp bản vẽ CAD: Chuẩn bị tệp bản vẽ CAD (ví dụ: conic_pyramid.dxf) mà bạn muốn chuyển đổi sang định dạng hình ảnh raster.

## Nhập không gian tên

Trong dự án .NET của bạn, hãy nhập các vùng tên cần thiết để tận dụng các chức năng của Aspose.CAD. Bao gồm các không gian tên sau vào đầu mã của bạn:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Bước 1: Tải bản vẽ CAD

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Tải bản vẽ CAD trong phiên bản của Hình ảnh
using (var image = Image.Load(sourceFilePath))
{
    // Mã của bạn để tải bản vẽ CAD có ở đây
}
```

## Bước 2: Tạo CadRasterizationOptions

```csharp
// Tạo một phiên bản của CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

## Bước 3: Chỉ định lớp

```csharp
// Thêm tên lớp vào danh sách lớp của CadRasterizationOptions
rasterizationOptions.Layers = new string[] { "LayerA" };
```

## Bước 4: Tạo JpegOptions

```csharp
// Tạo một phiên bản của JpegOptions (hoặc bất kỳ ImageOptions nào cho các định dạng raster)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## Bước 5: Xuất sang định dạng Jpeg

```csharp
// Xuất từng lớp sang định dạng Jpeg
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

## Bước bổ sung: Chuyển đổi tất cả các lớp

Nếu bạn muốn chuyển đổi tất cả các lớp, hãy sử dụng phương pháp sau:

```csharp
ConvertAllLayersToRasterImageFormats();
```

Phương pháp này lặp lại trên tất cả các lớp trong bản vẽ CAD, xuất từng lớp sang một tệp Jpeg riêng biệt.

## Phần kết luận

Chúc mừng! Bạn đã học thành công cách xuất bố cục CAD sang định dạng hình ảnh raster bằng Aspose.CAD cho .NET. Hướng dẫn này cung cấp hướng dẫn toàn diện cho các nhà phát triển đang tìm kiếm các giải pháp hiệu quả và đáng tin cậy để chuyển đổi CAD.

## Câu hỏi thường gặp

### Q1: Tôi có thể sử dụng các định dạng hình ảnh khác để xuất không?

 A1: Có, bạn có thể. Đơn giản chỉ cần thay thế`JpegOptions` với các tùy chọn của định dạng mong muốn, chẳng hạn như`PngOptions` hoặc`BmpOptions`.

### Q2: Có phiên bản dùng thử không?

 Câu trả lời 2: Có, bạn có thể khám phá chức năng của Aspose.CAD bằng cách tải xuống phiên bản dùng thử[đây](https://releases.aspose.com/).

### Câu 3: Làm cách nào tôi có thể nhận được hỗ trợ cho Aspose.CAD?

 A3: Truy cập Aspose.CAD[diễn đàn](https://forum.aspose.com/c/cad/19) để được hỗ trợ cộng đồng hoặc cân nhắc mua giấy phép để được hỗ trợ tận tình.

### Câu hỏi 4: Có giấy phép tạm thời không?

 A4: Có, bạn có thể xin giấy phép tạm thời[đây](https://purchase.aspose.com/temporary-license/).

### Câu 5: Tôi có thể tìm tài liệu ở đâu?

 A5: Tham khảo tài liệu chi tiết[đây](https://reference.aspose.com/cad/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
