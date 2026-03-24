---
date: 2026-03-24
description: Tìm hiểu cách chuyển đổi dgn sang png và lưu cad dưới dạng jpeg bằng
  Aspose.CAD cho .NET – hướng dẫn nhanh về chuyển đổi CAD sang hình ảnh.
linktitle: Export DGN to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Cách chuyển đổi DGN sang PNG trong Aspose.CAD cho .NET
url: /vi/net/cad-export-formats/export-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chuyển đổi DGN sang PNG trong Aspose.CAD cho .NET

Trong phát triển .NET hiện đại, **convert dgn to png** là một yêu cầu phổ biến khi bạn cần hiển thị bản vẽ CAD trên web hoặc nhúng chúng vào báo cáo. Aspose.CAD cho .NET giúp việc chuyển đổi này trở nên đơn giản, cho phép bạn biến một tệp DGN thành hình ảnh raster chất lượng cao chỉ với vài dòng mã. Trong hướng dẫn này, chúng ta sẽ đi qua toàn bộ quy trình, từ thiết lập dự án đến lưu tệp PNG (hoặc JPEG) cuối cùng.

## Trả lời nhanh
- **Tôi có thể chuyển đổi DGN sang PNG bằng Aspose.CAD không?** Có – chỉ cần cấu hình các tùy chọn rasterization và chọn đầu ra PNG hoặc JPEG.  
- **Tôi có cần giấy phép cho môi trường sản xuất không?** Cần một giấy phép Aspose.CAD hợp lệ cho các triển khai không dùng bản thử nghiệm.  
- **Các phiên bản .NET nào được hỗ trợ?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.  
- **Các định dạng ảnh nào có sẵn?** PNG, JPEG, BMP, GIF, TIFF và hơn thế nữa.  
- **Xử lý ngoại lệ có cần thiết không?** Chắc chắn – bao bọc quá trình chuyển đổi trong try/catch để xử lý các vấn đề truy cập tệp.

## “convert dgn to png” là gì?
Chuyển đổi một tệp DGN (MicroStation) sang PNG có nghĩa là raster hóa dữ liệu CAD vector thành một hình ảnh dựa trên pixel. Điều này hữu ích cho việc tạo bản xem trước, nhúng bản vẽ trong email HTML, hoặc tạo thumbnail cho hệ thống quản lý tài liệu.

## Tại sao nên dùng Aspose.CAD cho việc chuyển đổi CAD sang ảnh?
- **Không phụ thuộc bên ngoài** – hoạt động hoàn toàn bằng mã quản lý.  
- **Độ trung thực cao** – giữ nguyên độ dày đường, lớp và màu sắc.  
- **Đầu ra linh hoạt** – chuyển đổi giữa PNG, JPEG, BMP, v.v. chỉ bằng cách thay đổi một tùy chọn.  
- **Tối ưu hiệu năng** – rasterization nhanh ngay cả với các bản vẽ lớn.

## Yêu cầu trước

Trước khi bắt đầu, hãy đảm bảo bạn đã:

- **Cài đặt Aspose.CAD cho .NET** trong dự án của mình. Bạn có thể tải xuống từ [website](https://reference.aspose.com/cad/net/).  
- Một tệp DGN mẫu (ví dụ: `Nikon_D90_Camera.dgn`) được đặt trong thư mục đã biết.

## Nhập không gian tên

Bắt đầu bằng cách thêm các câu lệnh `using` cần thiết để bạn có thể truy cập các lớp Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Bước 1: Tải tệp DGN

Tải tệp DGN nguồn vào một đối tượng `CadImage`. Đối tượng này đại diện cho bản vẽ CAD trong bộ nhớ và sẽ là nguồn cho quá trình rasterization.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Bước 2: Định nghĩa tùy chọn rasterization

Cấu hình cách bản vẽ CAD sẽ được raster hóa. Bạn có thể điều chỉnh kích thước ảnh, tỷ lệ và màu nền tại đây.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Bước 3: Chọn định dạng đầu ra (PNG hoặc JPEG)

Mặc dù hướng dẫn tập trung vào PNG, bạn cũng có thể **save cad as jpeg**. Tạo đối tượng tùy chọn ảnh phù hợp và gắn các cài đặt rasterization.

```csharp
ImageOptionsBase options = new JpegOptions();   // Change to PngOptions() for PNG output
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Mẹo chuyên nghiệp:** Để tạo tệp PNG, thay `new JpegOptions()` bằng `new PngOptions()`.

## Bước 4: Lưu ảnh raster

Cuối cùng, gọi `Save` trên thể hiện `CadImage`, cung cấp tên tệp mong muốn và đối tượng tùy chọn bạn đã cấu hình.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

Nếu bạn đã chuyển sang `PngOptions`, tệp sẽ được lưu dưới tên `ExportDGNToRasterImage_out.png`.

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|-------------|----------|
| **Hình ảnh đầu ra trắng** | `NoScaling` được đặt không đúng hoặc layout chưa được chọn | Đặt `AutomaticLayoutsScaling = true` hoặc chỉ định layout mong muốn. |
| **Thiếu bộ nhớ cho tệp lớn** | Tải DGN khổng lồ mà không dùng streaming | Sử dụng `Image.Load(sourceFilePath, new LoadOptions { LoadOnDemand = true })`. |
| **Phiên bản DGN không được hỗ trợ** | Các phiên bản MicroStation cũ | Đảm bảo bạn đang dùng phiên bản Aspose.CAD mới nhất hỗ trợ các định dạng legacy. |

## Câu hỏi thường gặp

**H: Tôi có thể xuất tệp DGN sang các định dạng khác ngoài JPEG không?**  
Đ: Có, Aspose.CAD cho .NET hỗ trợ PNG, BMP, GIF, TIFF và hơn thế nữa – chỉ cần thay đổi lớp tùy chọn (ví dụ, `new PngOptions()`).

**H: Tôi nên xử lý ngoại lệ như thế nào trong quá trình chuyển đổi?**  
Đ: Bao bọc mã chuyển đổi trong khối `try/catch` và ghi log `Aspose.CAD.CadException` để có thông tin lỗi chi tiết.

**H: Có phiên bản dùng thử cho Aspose.CAD cho .NET không?**  
Đ: Có, bạn có thể khám phá sản phẩm với bản dùng thử miễn phí. Truy cập [here](https://releases.aspose.com/) để biết thêm chi tiết.

**H: Tôi có thể tìm sự hỗ trợ hoặc thảo luận các vấn đề liên quan đến Aspose.CAD cho .NET ở đâu?**  
Đ: Ghé thăm [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) để nhận hỗ trợ cộng đồng và thảo luận.

**H: Làm sao để lấy giấy phép tạm thời cho Aspose.CAD cho .NET?**  
Đ: Truy cập [this link](https://purchase.aspose.com/temporary-license/) để nhận giấy phép tạm thời cho nhu cầu phát triển của bạn.

## Kết luận

Bạn đã học cách **convert dgn to png** (hoặc JPEG) bằng Aspose.CAD cho .NET. Bằng cách điều chỉnh các tùy chọn rasterization và thay đổi lớp tùy chọn ảnh, bạn có thể tùy biến đầu ra để đáp ứng bất kỳ yêu cầu dự án nào. Hãy thoải mái thử nghiệm với các kích thước trang, cài đặt DPI và định dạng tệp khác nhau để có được hình ảnh raster hoàn hảo cho ứng dụng của mình.

---

**Cập nhật lần cuối:** 2026-03-24  
**Đã kiểm tra với:** Aspose.CAD 24.11 cho .NET  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}