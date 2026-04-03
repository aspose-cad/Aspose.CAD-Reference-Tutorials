---
date: 2026-04-03
description: Tìm hiểu cách hiển thị các tệp CAD và chuyển đổi DWG sang PNG bằng Aspose.CAD
  cho .NET. Hướng dẫn từng bước để lưu CAD dưới dạng hình ảnh.
keywords:
- how to render cad
- convert dwg to png
- export cad to png
- save cad as image
- load dwg in .net
linktitle: Kết xuất màu trong tệp CAD
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Cách hiển thị tệp CAD với màu sắc – Hướng dẫn Aspose.CAD
url: /vi/net/conversion-and-export/rendering-colors-in-cad-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách Render Các Tệp CAD Với Màu Sắc – Hướng Dẫn Aspose.CAD

## Giới thiệu

Bạn đang gặp khó khăn **cách render CAD** với màu sắc sống động bằng .NET? Trong hướng dẫn chi tiết, từng bước này chúng tôi sẽ chỉ cho bạn cách render màu trong các tệp CAD, chuyển DWG sang PNG, và lưu bản vẽ CAD dưới dạng hình ảnh chất lượng cao bằng thư viện Aspose.CAD.

## Câu trả lời nhanh
- **Thư viện nào tốt nhất để render màu CAD?** Aspose.CAD for .NET  
- **Tôi có thể chuyển DWG sang PNG trong một bước không?** Có – rasterize DWG và lưu dưới dạng PNG.  
- **Tôi có cần giấy phép cho việc sử dụng trong môi trường sản xuất không?** Giấy phép tạm thời hoạt động cho việc thử nghiệm; giấy phép đầy đủ cần thiết cho môi trường sản xuất.  
- **Các phiên bản .NET nào được hỗ trợ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.  
- **Quá trình có đủ nhanh cho chuyển đổi hàng loạt không?** Việc render được thực hiện trong bộ nhớ và phù hợp cho các thao tác bulk.

## Render Màu Trong Các Tệp CAD là gì?
Render màu nghĩa là lấy thông tin vector lưu trong bản vẽ CAD (DWG, DXF, v.v.) và rasterize nó thành ảnh bitmap trong khi giữ nguyên màu gốc của các đối tượng. Điều này rất cần thiết khi bạn muốn chia sẻ hình ảnh CAD với những người không có phần mềm CAD.

## Tại sao nên dùng Aspose.CAD để chuyển DWG sang PNG?
- **Không phụ thuộc bên ngoài** – hoạt động hoàn toàn offline.  
- **Độ trung thực cao** – màu đối tượng, độ dày đường và lớp được giữ nguyên.  
- **API đơn giản** – một dòng code để tải, cấu hình và lưu.  
- **Đa nền tảng** – hoạt động trên Windows, Linux và macOS .NET runtimes.

## Yêu cầu trước

- Thư viện Aspose.CAD: Tải xuống và cài đặt thư viện Aspose.CAD từ [tại đây](https://releases.aspose.com/cad/net/).  
- Môi trường phát triển: Đảm bảo bạn đã thiết lập môi trường phát triển .NET.  
- Tệp CAD: Có một tệp CAD mẫu sẵn sàng để thử nghiệm. Bạn có thể dùng “test1.dwg” cho hướng dẫn này.

## Nhập các Namespace

Trong dự án .NET của bạn, nhập các namespace cần thiết để truy cập các chức năng của Aspose.CAD. Thêm các dòng sau vào đầu mã nguồn của bạn:

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Bước 1: Thiết lập Dự án của Bạn

Tạo một dự án .NET mới và thiết lập các thư mục cần thiết. Đảm bảo thư viện Aspose.CAD được tham chiếu trong dự án của bạn.

## Bước 2: Xác định Đường dẫn Tệp

Xác định đường dẫn cho tệp CAD đầu vào và tệp PNG đầu ra. Cập nhật các dòng sau trong mã của bạn:

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "test1.dwg";
string outputFile = MyDir + "test1.png";
```

## Bước 3: Tải Tệp CAD

Sử dụng đoạn mã sau để mở và tải tệp CAD:

```csharp
using (FileStream fs = new FileStream(inputFile, FileMode.Open))
{
    using (FileStream output = new FileStream(outputFile, FileMode.Create))
    {
        Image document = Image.Load(fs);
```

## Bước 4: Cấu hình tùy chọn Rasterization

Cấu hình các tùy chọn rasterization để tùy chỉnh quá trình render. Cập nhật các dòng sau:

```csharp
PngOptions saveOptions = new PngOptions();

CadRasterizationOptions options = new CadRasterizationOptions();
options.NoScaling = false;
options.PageHeight = document.Height * 10;
options.PageWidth = document.Width * 10;
options.DrawType = Aspose.CAD.FileFormats.Cad.CadDrawTypeMode.UseObjectColor;
saveOptions.VectorRasterizationOptions = options;
```

## Bước 5: Lưu Hình ảnh Đã Render

Lưu hình ảnh đã render bằng các tùy chọn đã chỉ định:

```csharp
document.Save(output, saveOptions);
```

## Tại sao điều này quan trọng

Lưu CAD dưới dạng hình ảnh (PNG, JPEG, v.v.) là yêu cầu phổ biến khi bạn cần nhúng bản vẽ vào báo cáo, trang web hoặc tệp đính kèm email. Bằng cách nắm vững **cách render CAD**, bạn loại bỏ nhu cầu sử dụng các trình xem bên thứ ba và đảm bảo đầu ra hình ảnh nhất quán trên mọi nền tảng.

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|------------|-----------|
| Hình ảnh trống | `NoScaling` được đặt thành `true` với kích thước bằng 0 | Đảm bảo `PageHeight` và `PageWidth` được tính dựa trên hình ảnh đã tải (như minh họa). |
| Màu sắc hiển thị sai | `DrawType` sai | Sử dụng `CadDrawTypeMode.UseObjectColor` để giữ màu gốc của đối tượng. |
| Không tìm thấy tệp | Đường dẫn `MyDir` không đúng | Kiểm tra đường dẫn thư mục kết thúc bằng dấu gạch chéo hoặc dùng `Path.Combine`. |
| Hết bộ nhớ khi xử lý tệp lớn | Render ở DPI rất cao | Giảm hệ số scaling (ví dụ, `*5` thay vì `*10`). |

## Kết luận

Chúc mừng! Bạn đã học thành công **cách render CAD**, chuyển DWG sang PNG, và **lưu CAD dưới dạng hình ảnh** bằng Aspose.CAD cho .NET. Kiến thức này cho phép bạn tích hợp việc render CAD trực tiếp vào ứng dụng, tự động tạo báo cáo, xem trước trên web, và nhiều hơn nữa.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể dùng Aspose.CAD miễn phí không?

A1: Aspose.CAD cung cấp phiên bản dùng thử miễn phí có sẵn [tại đây](https://releases.aspose.com/). Bạn có thể khám phá các tính năng trước khi mua.

### Câu hỏi 2: Tôi có thể tìm tài liệu chi tiết cho Aspose.CAD ở đâu?

A2: Tham khảo tài liệu [tại đây](https://reference.aspose.com/cad/net/) để biết thông tin chi tiết về các chức năng của Aspose.CAD.

### Câu hỏi 3: Làm sao để có giấy phép tạm thời cho Aspose.CAD?

A3: Lấy giấy phép tạm thời [tại đây](https://purchase.aspose.com/temporary-license/) cho mục đích thử nghiệm.

### Câu hỏi 4: Cần trợ giúp hoặc có câu hỏi?

A4: Truy cập cộng đồng Aspose.CAD [forum](https://forum.aspose.com/c/cad/19) để được hỗ trợ và thảo luận.

### Câu hỏi 5: Tôi có thể mua thư viện Aspose.CAD ở đâu?

A5: Mua Aspose.CAD [tại đây](https://purchase.aspose.com/buy) để mở khóa đầy đủ tính năng.

## Các Câu Hỏi Thường Gặp Bổ Sung

**H: Làm sao tôi có thể **chuyển DWG sang PNG** mà không mất độ dày đường?**  
A: Giữ nguyên scaling mặc định của `PageHeight` và `PageWidth` (ví dụ, nhân 10) và đặt `options.DrawType` thành `UseObjectColor`. Điều này bảo toàn độ dày đường và màu sắc.

**H: Có thể **xuất CAD sang PNG** trong một dịch vụ nền không?**  
A: Có. API Aspose.CAD an toàn với đa luồng cho các thao tác chỉ đọc, vì vậy bạn có thể tải và rasterize tệp trong một worker nền.

**H: Tôi có thể **tải DWG trong .NET** từ một mảng byte thay vì tệp không?**  
A: Hoàn toàn có thể. Sử dụng `Image.Load(byteArray)` thay vì `FileStream` và thực hiện các bước rasterization tương tự.

**H: Định dạng nào nên chọn để có chất lượng tốt nhất khi **lưu CAD dưới dạng hình ảnh**?**  
A: PNG cung cấp nén không mất dữ liệu và giữ nguyên độ trung thực màu, là lựa chọn lý tưởng cho bản vẽ kỹ thuật.

**H: Aspose.CAD có hỗ trợ các định dạng raster khác như JPEG hoặc BMP không?**  
A: Có – chỉ cần thay `PngOptions` bằng `JpegOptions` hoặc `BmpOptions` và điều chỉnh các cài đặt riêng cho định dạng.

**Last Updated:** 2026-04-03  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}