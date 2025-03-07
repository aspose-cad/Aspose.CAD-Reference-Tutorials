---
title: Hỗ trợ DGN V7 trong Aspose.CAD cho .NET
linktitle: Hỗ trợ cho DGN V7
second_title: Aspose.CAD .NET - Định dạng tệp CAD và BIM
description: Khám phá Aspose.CAD để biết sự hỗ trợ liền mạch của .NET cho DGN V7. Chuyển đổi tệp DGN thành hình ảnh raster dễ dàng với hướng dẫn từng bước.
weight: 19
url: /vi/net/cad-features-and-support/support-for-dgn-v7/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hỗ trợ DGN V7 trong Aspose.CAD cho .NET

## Giới thiệu

Trong lĩnh vực phát triển .NET, Aspose.CAD nổi bật như một thư viện mạnh mẽ để xử lý các tệp Thiết kế hỗ trợ máy tính (CAD). Hướng dẫn này đi sâu vào một tính năng cụ thể của Aspose.CAD cho .NET—hỗ trợ cho các tệp DGN V7. DGN, viết tắt của Design, là định dạng tệp được sử dụng rộng rãi trong miền CAD. Aspose.CAD đơn giản hóa quá trình làm việc với các tệp DGN V7, mang đến cho các nhà phát triển trải nghiệm liền mạch.

## Điều kiện tiên quyết

Trước khi chúng ta đi sâu vào triển khai, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

-  Aspose.CAD cho .NET: Đảm bảo bạn đã cài đặt thư viện Aspose.CAD. Bạn có thể tải nó xuống từ[trang mạng](https://releases.aspose.com/cad/net/).

- Môi trường phát triển: Thiết lập môi trường phát triển .NET đang hoạt động, bao gồm Visual Studio hoặc bất kỳ IDE ưa thích nào khác.

Bây giờ chúng ta đã sắp xếp các điều kiện tiên quyết, hãy khám phá cách tận dụng sự hỗ trợ cho DGN V7 trong Aspose.CAD cho .NET.

## Nhập không gian tên

Bắt đầu bằng cách nhập các không gian tên cần thiết để truy cập chức năng của Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Bước 1: Tải tệp DGN

 Bắt đầu bằng cách tải tệp DGN hiện có dưới dạng`CadImage` Thay thế`"Your Document Directory"` Và`"Nikon_D90_Camera.dgn"` với đường dẫn thư mục và tên file thích hợp.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Mã cho các bước tiếp theo ở đây ...
}
```

## Bước 2: Định cấu hình tùy chọn Rasterization

 Tạo một`CadRasterizationOptions` đối tượng để xác định và thiết lập các thuộc tính khác nhau liên quan đến rasterization.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    PageWidth = 600,
    PageHeight = 300,
    NoScaling = true,
    AutomaticLayoutsScaling = false
};
```

## Bước 3: Đặt tùy chọn Rasterization Vector

 Tạo một`JpegOptions` object khi chúng tôi dự định chuyển đổi tệp DGN thành JPEG. Gán cái đã tạo trước đó`CadRasterizationOptions` phản đối nó.

```csharp
ImageOptionsBase options = new JpegOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## Bước 4: Lưu hình ảnh đã được Rasterized

 Gọi`Save` phương pháp của`CadImage` class để xuất tệp DGN thành hình ảnh raster, trong trường hợp này là JPEG.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpeg", options);
```

Sau khi hoàn thành các bước này, tệp DGN sẽ được xuất thành công sang hình ảnh raster.

## Phần kết luận

Trong hướng dẫn này, chúng tôi đã khám phá sự hỗ trợ liền mạch cho DGN V7 trong Aspose.CAD cho .NET. Bằng cách làm theo hướng dẫn từng bước, các nhà phát triển có thể dễ dàng chuyển đổi tệp DGN thành hình ảnh raster, mở rộng khả năng của các ứng dụng .NET của họ.

## Câu hỏi thường gặp

### Câu hỏi 1: Aspose.CAD có tương thích với thông số kỹ thuật DGN V7 mới nhất không?

Câu trả lời 1: Có, Aspose.CAD được thiết kế để xử lý liền mạch các tệp DGN V7, đảm bảo khả năng tương thích với các thông số kỹ thuật mới nhất.

### Câu hỏi 2: Tôi có thể tùy chỉnh các tùy chọn tạo điểm ảnh để chuyển đổi tệp DGN không?

 A2: Chắc chắn rồi. Hướng dẫn trình bày cách tạo và cấu hình`CadRasterizationOptions` để điều chỉnh quá trình chuyển đổi.

### Câu hỏi 3: Có định dạng đầu ra nào khác được hỗ trợ ngoài JPEG không?

Câu trả lời 3: Có, Aspose.CAD hỗ trợ nhiều định dạng đầu ra khác nhau. Bạn có thể khám phá tài liệu để có danh sách đầy đủ.

### Câu hỏi 4: Làm cách nào tôi có thể nhận được hỗ trợ cho các truy vấn liên quan đến Aspose.CAD?

 A4: Tham quan[Diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để được cộng đồng hỗ trợ và thảo luận.

### Câu hỏi 5: Có bản dùng thử miễn phí Aspose.CAD cho .NET không?

 Câu trả lời 5: Có, bạn có thể truy cập bản dùng thử miễn phí[đây](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
