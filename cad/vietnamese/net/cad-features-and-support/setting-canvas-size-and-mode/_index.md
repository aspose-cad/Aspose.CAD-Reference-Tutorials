---
date: 2026-03-29
description: Tìm hiểu cách tạo PDF từ CAD, thiết lập kích thước canvas và xuất CAD
  sang PDF hoặc TIFF bằng Aspose.CAD cho .NET trong hướng dẫn từng bước này.
linktitle: Setting Canvas Size and Mode
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 'Cách tạo PDF từ CAD: Đặt kích thước canvas và chế độ trong Aspose.CAD cho
  .NET'
url: /vi/net/cad-features-and-support/setting-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cài đặt kích thước canvas và chế độ trong Aspose.CAD cho .NET

## Giới thiệu

Sẵn sàng **tạo PDF từ CAD** với việc kiểm soát kích thước đầu ra? Trong hướng dẫn này, chúng ta sẽ hướng dẫn cách cài đặt kích thước canvas và chế độ, tải tệp CAD, và xuất ra PDF hoặc TIFF bằng Aspose.CAD cho .NET. Cho dù bạn cần **chuyển đổi DXF sang PDF**, tạo bản vẽ độ phân giải cao, hoặc chỉ đơn giản điều chỉnh khu vực raster hóa, các bước dưới đây sẽ cung cấp cho bạn một giải pháp vững chắc, sẵn sàng cho sản xuất.

## Câu trả lời nhanh
- **“create PDF from CAD” có nghĩa là gì?** Chuyển đổi bản vẽ CAD (ví dụ: DXF, DWG) thành tài liệu PDF giữ nguyên chi tiết vector và raster.  
- **Tùy chọn nào kiểm soát kích thước đầu ra?** `CadRasterizationOptions.PageWidth` và `PageHeight` (canvas size).  
- **Tôi có thể xuất ra TIFF không?** Có – sử dụng `TiffOptions` với cùng các cài đặt rasterization.  
- **Tôi có cần giấy phép cho môi trường sản xuất không?** Cần một giấy phép thương mại; bản dùng thử miễn phí có sẵn.  
- **Các phiên bản .NET được hỗ trợ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## “create PDF from CAD” là gì

Tạo PDF từ CAD có nghĩa là render bản vẽ CAD thành định dạng hướng trang (PDF) có thể xem, in hoặc chia sẻ mà không cần phần mềm CAD. Aspose.CAD thực hiện các công việc nặng, cho phép bạn định nghĩa kích thước canvas, tỷ lệ và định dạng đầu ra.

## Tại sao cần đặt kích thước canvas khi tạo PDF từ CAD?

Việc đặt kích thước canvas cho phép bạn kiểm soát chính xác độ phân giải và kích thước của PDF hoặc TIFF kết quả. Điều này đặc biệt hữu ích khi:
- Chuẩn bị bản vẽ để in trên các kích thước giấy cụ thể.  
- Tạo ảnh thu nhỏ hoặc hình ảnh độ phân giải cao cho xem trước trên web.  
- Đảm bảo bố cục nhất quán trên nhiều tài liệu.

## Yêu cầu trước

- Thư viện Aspose.CAD: Tải xuống và cài đặt thư viện Aspose.CAD từ [trang web Aspose.CAD](https://releases.aspose.com/cad/net/).
- Môi trường phát triển: Đảm bảo bạn có môi trường phát triển .NET được cài đặt trên máy.
- Tệp CAD mẫu: Trong hướng dẫn này, chúng ta sẽ sử dụng một tệp DXF mẫu. Bạn có thể tìm thấy nó trong [tài liệu Aspose.CAD](https://reference.aspose.com/cad/net/).

## Nhập không gian tên

First, import the namespaces required for CAD processing:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Cách tạo PDF từ CAD với kích thước canvas tùy chỉnh

### Bước 1: Tải tệp CAD

Chúng ta bắt đầu bằng cách **tải tệp CAD** (ví dụ: một DXF) vào đối tượng `Image`. Đây là thời điểm bạn **tải tệp CAD** vào bộ nhớ.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps will go here
}
```

### Bước 2: Tạo CadRasterizationOptions

Tạo một thể hiện `CadRasterizationOptions` và xác định kích thước canvas. Các thuộc tính `PageWidth` và `PageHeight` cho phép bạn **đặt kích thước canvas** theo đúng kích thước bạn cần.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

### Bước 3: Tạo PdfOptions (Xuất CAD sang PDF)

Liên kết các cài đặt rasterization với một đối tượng `PdfOptions`. Cấu hình này cho phép bạn **xuất CAD sang PDF** với canvas tùy chỉnh mà bạn đã định nghĩa.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Bước 4: Xuất ra PDF (Chuyển đổi DXF sang PDF)

Bây giờ lưu hình ảnh dưới dạng PDF. Bước này **tạo PDF từ CAD** bằng cách sử dụng các tùy chọn chúng ta đã thiết lập.

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

### Bước 5: Tạo TiffOptions (Xuất CAD sang TIFF)

Nếu bạn cũng cần một hình ảnh raster, hãy cấu hình `TiffOptions`. Các tùy chọn rasterization giống nhau được tái sử dụng, vì vậy **xuất CAD sang TIFF** sẽ tuân theo kích thước canvas.

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Bước 6: Xuất ra TIFF

Cuối cùng, lưu bản vẽ dưới dạng tệp TIFF.

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Các vấn đề thường gặp và giải pháp

- **Canvas bị cắt** – Kiểm tra rằng `AutomaticLayoutsScaling` được đặt thành `true` và `NoScaling` là `false` để bản vẽ được phóng to/thu nhỏ phù hợp với canvas.  
- **PDF độ phân giải thấp** – Tăng `PageWidth`/`PageHeight` hoặc đặt `Resolution` trên `CadRasterizationOptions`.  
- **Lỗi không tìm thấy tệp** – Đảm bảo `MyDir` trỏ tới một thư mục hợp lệ và tên tệp DXF khớp chính xác.

## Câu hỏi thường gặp

### Q1: Tôi có thể sử dụng Aspose.CAD với các thư viện .NET khác không?

A1: Có, Aspose.CAD tích hợp liền mạch với các thư viện .NET khác, cung cấp khả năng nâng cao cho việc xử lý CAD.

### Q2: Có bản dùng thử miễn phí cho Aspose.CAD không?

A2: Có, bạn có thể khám phá các tính năng của Aspose.CAD với bản dùng thử miễn phí. Truy cập [đây](https://releases.aspose.com/) để bắt đầu.

### Q3: Làm sao tôi có thể nhận hỗ trợ cho Aspose.CAD?

A3: Để được hỗ trợ và thảo luận, truy cập [diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q4: Tôi có thể tìm tài liệu đầy đủ cho Aspose.CAD ở đâu?

A4: Tham khảo [tài liệu Aspose.CAD](https://reference.aspose.com/cad/net/) để có thông tin chi tiết và các ví dụ.

### Q5: Làm thế nào để mua Aspose.CAD cho .NET?

A5: Để mua Aspose.CAD, truy cập [trang mua hàng](https://purchase.aspose.com/buy).

**Câu hỏi bổ sung**

**Q: Tôi có thể xuất một bản vẽ CAD đa trang thành một PDF duy nhất không?**  
A: Có. Đặt `PageCount` trong `CadRasterizationOptions` và thư viện sẽ nối các trang lại thành một PDF.

**Q: Kích thước canvas có ảnh hưởng đến chất lượng dữ liệu vector không?**  
A: Dữ liệu vector vẫn độc lập với độ phân giải; kích thước canvas chỉ ảnh hưởng đến các yếu tố rasterized và độ phân giải của hình ảnh.

---

**Cập nhật lần cuối:** 2026-03-29  
**Kiểm tra với:** Aspose.CAD 24.11 cho .NET  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}