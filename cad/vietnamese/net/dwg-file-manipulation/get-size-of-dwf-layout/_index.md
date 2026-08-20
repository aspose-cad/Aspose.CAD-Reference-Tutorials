---
date: 2026-04-06
description: Tìm hiểu cách chuyển đổi DWF sang JPG trong C# bằng Aspose.CAD và khám
  phá cách trích xuất kích thước bố cục DWF từ các tệp DWG.
keywords:
- convert dwf to jpg
- how to extract dwf
- convert dwg to jpg
linktitle: Làm việc với tệp DWG trong C# - Lấy kích thước của bố cục DWF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Chuyển đổi DWF sang JPG trong C# – Lấy kích thước bố cục DWF từ DWG
url: /vi/net/dwg-file-manipulation/get-size-of-dwf-layout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chuyển đổi DWF sang JPG trong C# – Lấy kích thước bố cục DWF từ DWG

## Giới thiệu

Nếu bạn cần **convert DWF to JPG** đồng thời xác định kích thước bố cục chính xác, bạn đã đến đúng nơi. Trong hướng dẫn này, chúng tôi sẽ trình bày một ví dụ hoàn chỉnh, từ đầu đến cuối, sử dụng Aspose.CAD cho .NET để mở tệp DWF được tạo từ DWG, đọc kích thước của mỗi bố cục, và lưu bố cục dưới dạng hình ảnh JPG chất lượng cao. Khi kết thúc, bạn sẽ không chỉ biết cách trích xuất thông tin bố cục DWF mà còn có một đoạn mã có thể tái sử dụng trong bất kỳ dự án C# nào.

## Câu trả lời nhanh
- **Ý nghĩa của “convert DWF to JPG” là gì?** Nó có nghĩa là raster hóa một bố cục DWF vector thành một hình ảnh bitmap JPEG.  
- **Tại sao phải đọc kích thước bố cục trước?** Biết kích thước chính xác cho phép bạn đặt kích thước trang đúng, tránh kết quả bị kéo dài hoặc cắt.  
- **Thư viện nào xử lý việc này?** Aspose.CAD cho .NET cung cấp hỗ trợ đầy đủ cho DWG, DWF và chuyển đổi ảnh raster.  
- **Tôi có cần giấy phép không?** Giấy phép tạm thời hoạt động cho việc đánh giá; giấy phép đầy đủ cần thiết cho môi trường sản xuất.  
- **Các phiên bản .NET nào được hỗ trợ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## “convert DWF to JPG” là gì và tại sao nó quan trọng?

Chuyển đổi tệp DWF (Design Web Format) sang JPG tạo ra một hình ảnh di động có thể hiển thị trong trình duyệt, nhúng vào báo cáo, hoặc chia sẻ với các bên liên quan không có phần mềm CAD. Việc chuyển đổi cũng cho phép bạn linh hoạt thao tác với hình ảnh (thay đổi kích thước, nén, thêm watermark) bằng các công cụ xử lý ảnh tiêu chuẩn.

## Tại sao cần trích xuất kích thước bố cục DWF?

Một tệp DWF có thể chứa nhiều bố cục, mỗi bố cục có hệ tọa độ và đơn vị riêng (inch, milimet, v.v.). Việc trích xuất kích thước bố cục cho phép bạn:

1. Giữ tỷ lệ khung hình gốc khi raster hóa.  
2. Chọn DPI phù hợp cho đầu ra độ phân giải cao.  
3. Tự động xử lý hàng loạt nhiều bố cục mà không cần điều chỉnh thủ công.

## Yêu cầu trước

Để thực hiện hướng dẫn này một cách suôn sẻ, hãy chắc chắn rằng bạn đã chuẩn bị các yêu cầu sau:

- Aspose.CAD cho .NET: Đảm bảo bạn đã cài đặt Aspose.CAD cho .NET. Bạn có thể tải xuống từ [trang tải Aspose.CAD cho .NET](https://releases.aspose.com/cad/net/).

Có sẵn thư viện có nghĩa là bạn có thể tập trung vào mã thay vì phải tìm kiếm các phụ thuộc.

## Nhập không gian tên

Trước khi bắt đầu viết mã, hãy nhập các không gian tên cần thiết. Chúng cung cấp các lớp chúng ta sẽ dùng để làm việc với tệp CAD, tùy chọn raster hóa và I/O tệp.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Bước 1: Thiết lập môi trường của bạn

Tạo một dự án console hoặc class‑library C# mới, thêm tham chiếu tới **Aspose.CAD.dll**, và đảm bảo dự án nhắm tới phiên bản .NET tương thích.

## Bước 2: Xác định đường dẫn tệp (cách trích xuất DWF)

Xác định vị trí tệp DWF nguồn và nơi các tệp JPG được tạo sẽ được ghi.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

> **Mẹo chuyên nghiệp:** Sử dụng `Path.Combine(MyDir, "blocks_and_tables.dwf")` để xử lý đường dẫn an toàn hơn trên các hệ điều hành khác nhau.

## Bước 3: Tải ảnh DWF

Tải tệp DWF vào đối tượng `Aspose.CAD.Image`. Chúng ta ép kiểu nó thành `DwfImage` vì cần truy cập các thuộc tính riêng của trang.

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Code for further steps will go here
}
```

## Bước 4: Duyệt qua các trang

Một DWF có thể chứa nhiều trang (bố cục). Lặp qua từng trang để chúng ta có thể xử lý chúng riêng biệt.

```csharp
foreach (var page in image.Pages)
{
    // Code for further steps will go here
}
```

## Bước 5: Lấy thông tin bố cục

Bên trong vòng lặp, lấy tên bố cục. Tên này sẽ được dùng cả để ghi log và đặt tên cho tệp JPG đầu ra.

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## Bước 6: Thiết lập tùy chọn JPG

Tạo một thể hiện `JpegOptions` và cấu hình các tùy chọn raster hóa. Thuộc tính `Layouts` cho Aspose.CAD biết nên render bố cục nào.

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Code for further steps will go here
}
```

## Bước 7: Xác định kích thước trang (convert dwg to jpg)

Tính chiều rộng và chiều cao của bố cục bằng các đơn vị gốc của nó. Thông tin này rất quan trọng để đặt kích thước trang raster một cách chính xác.

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Code for further steps will go here
```

## Bước 8: Thiết lập kích thước trang

Chuyển đổi các đơn vị gốc (inch hoặc millimeter) sang pixel bằng các phương thức trợ giúp do Aspose.CAD cung cấp. Nếu loại đơn vị không phải là hai loại trên, chúng ta sẽ sử dụng giá trị thô.

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## Bước 9: Lưu tệp JPG

Cuối cùng, gắn các tùy chọn raster hóa vào tùy chọn JPEG và lưu hình ảnh ra đĩa.

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

Khi vòng lặp kết thúc, bạn sẽ có một tệp JPG cho mỗi bố cục, mỗi tệp có kích thước chính xác khớp với kích thước gốc của DWF.

## Vấn đề thường gặp và giải pháp

| Triệu chứng | Nguyên nhân khả dĩ | Cách khắc phục |
|------------|---------------------|----------------|
| Kết quả JPG trống | `options.Layouts` chưa được đặt đúng | Xác minh tên bố cục khớp với `page.Name`. |
| Hình ảnh bị biến dạng | Chuyển đổi DPI sai | Sử dụng `CommonHelper.DPI = 300` (hoặc DPI mục tiêu) trước khi chuyển đổi. |
| Không tìm thấy tệp | Đường dẫn `MyDir` không đúng | Sử dụng đường dẫn tuyệt đối hoặc `Path.Combine`. |
| Ngoại lệ giấy phép | Chưa áp dụng giấy phép | Tải giấy phép tạm thời hoặc vĩnh viễn trước khi gọi `Image.Load`. |

## Câu hỏi thường gặp

### Q1: Aspose.CAD có tương thích với các định dạng tệp DWG mới nhất không?
A1: Aspose.CAD hỗ trợ nhiều định dạng tệp DWG, bao gồm các phiên bản mới nhất. Tham khảo [tài liệu](https://reference.aspose.com/cad/net/) để biết chi tiết tương thích.

### Q2: Tôi có thể sử dụng Aspose.CAD cho cả dự án thương mại và cá nhân không?
A2: Có, Aspose.CAD cung cấp các tùy chọn giấy phép linh hoạt cho cả mục đích thương mại và cá nhân. Truy cập [trang mua hàng](https://purchase.aspose.com/buy) để biết thêm chi tiết.

### Q3: Làm sao tôi có thể lấy giấy phép tạm thời cho Aspose.CAD?
A3: Bạn có thể nhận giấy phép tạm thời từ [đây](https://purchase.aspose.com/temporary-license/) để đánh giá.

### Q4: Tôi có thể tìm hỗ trợ cho Aspose.CAD ở đâu?
A4: Đối với bất kỳ câu hỏi hoặc hỗ trợ nào, hãy truy cập [diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q5: Có bản dùng thử miễn phí cho Aspose.CAD không?
A5: Có, bạn có thể truy cập phiên bản dùng thử miễn phí của Aspose.CAD [tại đây](https://releases.aspose.com/).

### Q6: Làm sao tôi chuyển đổi tệp DWG trực tiếp sang JPG mà không cần trích xuất DWF trước?
A6: Bạn có thể tải tệp DWG bằng `Aspose.CAD.Image.Load` và sử dụng cùng quy trình raster hóa; chỉ cần đặt `options.Layouts` thành tên bố cục mong muốn từ DWG.

### Q7: Việc chuyển đổi có giữ nguyên chất lượng vector không?
A7: Khi đã raster hóa thành JPG, hình ảnh trở thành bitmap, vì vậy khả năng mở rộng vector bị mất. Để mở rộng không mất chất lượng, hãy cân nhắc xuất sang PNG hoặc SVG.

---

**Cập nhật lần cuối:** 2026-04-06  
**Kiểm tra với:** Aspose.CAD 24.11 for .NET  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}