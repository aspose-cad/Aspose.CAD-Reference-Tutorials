---
title: Chuyển đổi bố cục thành hình ảnh raster trong Aspose.CAD cho .NET
linktitle: Chuyển đổi bố cục thành hình ảnh raster
second_title: Aspose.CAD .NET - Định dạng tệp CAD và BIM
description: Dễ dàng chuyển đổi bố cục CAD thành hình ảnh raster bằng Aspose.CAD cho .NET. Nâng cao sự phát triển của bạn với khả năng thao tác CAD mạnh mẽ.
weight: 12
url: /vi/net/cad-drawing-manipulation/convert-layouts-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chuyển đổi bố cục thành hình ảnh raster trong Aspose.CAD cho .NET

## Giới thiệu

Bạn đang muốn chuyển đổi bố cục thành hình ảnh raster một cách dễ dàng trong các ứng dụng .NET của mình? Đừng tìm đâu xa! Hướng dẫn từng bước này sẽ hướng dẫn bạn qua quy trình sử dụng Aspose.CAD cho .NET, một thư viện mạnh mẽ giúp đơn giản hóa các tác vụ Thiết kế có sự hỗ trợ của Máy tính (CAD).

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

- Aspose.CAD for .NET Library: Tải xuống và cài đặt thư viện từ[Trang tải xuống Aspose.CAD cho .NET](https://releases.aspose.com/cad/net/).

- Môi trường phát triển: Đảm bảo bạn đã thiết lập môi trường phát triển .NET đang hoạt động trên máy của mình.

- Tài liệu cần chuyển đổi: Chuẩn bị tài liệu CAD có chứa bố cục bạn muốn chuyển đổi thành hình ảnh raster.

- Thư mục tài liệu của bạn: Thay thế phần giữ chỗ "Thư mục tài liệu của bạn" trong mã bằng đường dẫn đến thư mục tài liệu của bạn.

## Nhập không gian tên

Trước tiên, hãy nhập các không gian tên cần thiết để làm cho các chức năng Aspose.CAD có thể truy cập được trong mã của bạn.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Bước 1: Tải tài liệu CAD

Bắt đầu bằng cách tải tài liệu CAD bằng thư viện Aspose.CAD.

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image image = Image.Load(sourceFilePath))
{
    //Mã của bạn cho các bước tiếp theo sẽ có ở đây
}
```

## Bước 2: Định cấu hình tùy chọn Rasterization

 Tạo một thể hiện của`CadRasterizationOptions` để đặt chiều rộng, chiều cao của trang và chỉ định bố cục bạn muốn chuyển đổi.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
rasterizationOptions.Layouts = new string[] { "Model", "Layout1" };
```

## Bước 3: Thiết lập TiffOptions cho hình ảnh kết quả

 Tạo một thể hiện của`TiffOptions`để xác định định dạng của hình ảnh kết quả.

```csharp
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.VectorRasterizationOptions = rasterizationOptions;
```

## Bước 4: Lưu hình ảnh kết quả

Chỉ định đường dẫn đầu ra và lưu hình ảnh đã chuyển đổi.

```csharp
string outputFilePath = MyDir + "conic_pyramid_layoutstorasterimage_out.tiff";
image.Save(outputFilePath, options);
```

## Phần kết luận

Chúc mừng! Bạn đã chuyển đổi thành công bố cục CAD sang định dạng hình ảnh raster bằng Aspose.CAD cho .NET. Khả năng là rất lớn và hướng dẫn này đóng vai trò là điểm khởi đầu cho những nỗ lực liên quan đến CAD của bạn.

## Câu hỏi thường gặp

### Câu hỏi 1: Aspose.CAD có tương thích với tất cả các định dạng CAD không?

 Trả lời 1: Aspose.CAD hỗ trợ nhiều định dạng CAD, bao gồm DWG, DXF, DWF, STL, v.v. Kiểm tra[tài liệu](https://reference.aspose.com/cad/net/) để có danh sách đầy đủ.

### Câu hỏi 2: Làm cách nào tôi có thể nhận được giấy phép tạm thời cho Aspose.CAD?

 A2: Tham quan[trang giấy phép tạm thời](https://purchase.aspose.com/temporary-license/) để có được giấy phép tạm thời cho mục đích thử nghiệm và đánh giá.

### Câu hỏi 3: Tôi có thể tìm hỗ trợ cho Aspose.CAD ở đâu?

 Câu trả lời 3: Diễn đàn là nơi tuyệt vời để tìm kiếm sự trợ giúp. Tham quan[Diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để kết nối với cộng đồng và nhận trợ giúp.

### Q4: Tôi có thể dùng thử Aspose.CAD miễn phí không?

 A4: Chắc chắn rồi! Lấy của bạn[dùng thử miễn phí](https://releases.aspose.com/) để khám phá các tính năng và khả năng của Aspose.CAD.

### Câu hỏi 5: Tôi có thể mua giấy phép cho Aspose.CAD ở đâu?

 A5: Điều hướng đến[trang mua hàng](https://purchase.aspose.com/buy) để mua giấy phép và khai thác toàn bộ tiềm năng của Aspose.CAD.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
