---
title: Xuất DGN sang hình ảnh raster trong Aspose.CAD cho .NET
linktitle: Xuất DGN sang hình ảnh raster
second_title: Aspose.CAD .NET - Định dạng tệp CAD và BIM
description: Chuyển đổi DGN sang hình ảnh raster dễ dàng bằng Aspose.CAD cho .NET. Khám phá hướng dẫn từng bước và giải phóng sức mạnh của .NET trong thao tác tệp CAD.
weight: 13
url: /vi/net/cad-export-formats/export-dgn-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xuất DGN sang hình ảnh raster trong Aspose.CAD cho .NET

## Giới thiệu

Trong lĩnh vực phát triển .NET năng động, Aspose.CAD nổi lên như một công cụ mạnh mẽ để xử lý các tệp Thiết kế hỗ trợ máy tính (CAD). Hướng dẫn này đi sâu vào quá trình xuất tệp DGN sang hình ảnh raster bằng Aspose.CAD cho .NET. Nếu bạn muốn chuyển đổi các tệp DGN của mình thành các hình ảnh raster hấp dẫn về mặt trực quan một cách liền mạch thì bạn đã đến đúng nơi.

## Điều kiện tiên quyết

Trước khi chúng ta bắt đầu cuộc hành trình này, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

-  Aspose.CAD cho .NET: Đảm bảo bạn đã cài đặt thư viện Aspose.CAD trong dự án .NET của mình. Bạn có thể tìm thấy thư viện và tài liệu liên quan trên[trang mạng](https://reference.aspose.com/cad/net/).

- Tệp DGN mẫu: Chuẩn bị sẵn tệp DGN để chuyển đổi. Trong ví dụ của chúng tôi, chúng tôi sẽ sử dụng "Nikon_D90_Camera.dgn."

Bây giờ chúng ta hãy đi sâu vào hướng dẫn từng bước.

## Nhập không gian tên

Trong dự án .NET của bạn, hãy bắt đầu bằng cách nhập các vùng tên cần thiết cho Aspose.CAD. Bước này cho phép bạn truy cập các lớp và phương thức cần thiết để chuyển đổi hình ảnh DGN sang raster.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Bước 1: Tải tệp DGN

 Bắt đầu bằng cách tải tệp DGN vào một`CadImage` sự vật. Điều này tạo nền tảng cho các hoạt động tiếp theo.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Mã của bạn để xử lý thêm ở đây
}
```

## Bước 2: Xác định các tùy chọn Rasterization

 Tạo một`CadRasterizationOptions` đối tượng và đặt các thuộc tính khác nhau để tùy chỉnh quá trình rasterization theo yêu cầu của bạn.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Bước 3: Tạo đối tượng JpegOptions

 Vì mục tiêu của chúng tôi là chuyển đổi tệp DGN thành JPEG, hãy tạo một`JpegOptions` đối tượng và gán được xác định trước đó`CadRasterizationOptions` đến nó.

```csharp
ImageOptionsBase options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## Bước 4: Lưu hình ảnh raster

 Sử dụng`Save` phương pháp của`CadImage` class để xuất tệp DGN sang hình ảnh raster ở định dạng mong muốn, trong trường hợp này là JPEG.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

## Phần kết luận

Chúc mừng! Bạn đã điều hướng thành công qua các bước để xuất tệp DGN sang hình ảnh raster bằng Aspose.CAD cho .NET. Hướng dẫn này đã trang bị cho bạn kiến thức cần thiết để tích hợp chức năng này vào các dự án .NET của bạn một cách dễ dàng.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể xuất tệp DGN sang các định dạng khác ngoài JPEG không?

Câu trả lời 1: Có, Aspose.CAD for .NET hỗ trợ nhiều định dạng đầu ra khác nhau. Bạn có thể sửa đổi các tùy chọn cho phù hợp ở Bước 3.

### Q2 Làm cách nào để xử lý các trường hợp ngoại lệ trong quá trình chuyển đổi?

Câu trả lời 2: Đảm bảo bạn có cách xử lý ngoại lệ thích hợp, như được minh họa trong mã được cung cấp, để giải quyết các vấn đề tiềm ẩn.

### Câu hỏi 3: Có phiên bản dùng thử cho Aspose.CAD cho .NET không?

 Câu trả lời 3: Có, bạn có thể khám phá sản phẩm bằng bản dùng thử miễn phí. Thăm nom[đây](https://releases.aspose.com/) để biết thêm thông tin.

### Câu hỏi 4: Tôi có thể tìm kiếm trợ giúp hoặc thảo luận các vấn đề liên quan đến Aspose.CAD cho .NET ở đâu?

 A4: Đi tới[Diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để được cộng đồng hỗ trợ và thảo luận.

### Câu hỏi 5: Làm cách nào để có được giấy phép tạm thời cho Aspose.CAD cho .NET?

 A5: Thăm quan[liên kết này](https://purchase.aspose.com/temporary-license/)để có được giấy phép tạm thời cho nhu cầu phát triển của bạn.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
