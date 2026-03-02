---
date: 2026-03-02
description: Tìm hiểu cách tạo một tệp PDF duy nhất với các bố cục khác nhau bằng
  Aspise.CAD cho .NET – chuyển đổi CAD sang PDF, xuất DWG sang PDF và lưu CAD dưới
  dạng PDF một cách hiệu quả.
linktitle: Creating Single PDF with Different Layouts
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Cách tạo một tệp PDF duy nhất với các bố cục khác nhau - Hướng dẫn Aspose.CAD
url: /vi/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách tạo PDF đơn với các Bố cục Khác nhau - Hướng dẫn Aspose.CAD

## Giới thiệu

Nếu bạn cần **tạo PDF đơn** chứa nhiều bố cục CAD, bạn đã đến đúng nơi. Trong hướng dẫn này, chúng tôi sẽ trình bày các bước chính xác để chuyển đổi bản vẽ CAD thành một tài liệu PDF, xử lý nhiều bố cục trong quá trình. Bạn sẽ thấy cách Aspose.CAD cho .NET giúp dễ dàng **chuyển đổi CAD sang PDF**, **xuất DWG sang PDF**, và **lưu CAD dưới dạng PDF** chỉ với vài dòng mã C#.

## Câu trả lời nhanh
- **Nội dung của hướng dẫn này là gì?** Tạo một PDF bao gồm nhiều bố cục CAD.  
- **Thư viện nào được sử dụng?** Aspose.CAD cho .NET.  
- **Tôi có cần giấy phép không?** Bản dùng thử miễn phí đủ cho việc đánh giá; cần giấy phép cho môi trường sản xuất.  
- **Các định dạng CAD được hỗ trợ?** DWG, DXF, DGN và nhiều định dạng khác.  
- **Thời gian thực hiện điển hình?** Khoảng 10‑15 phút cho một chuyển đổi cơ bản.

## “Tạo PDF đơn” trong ngữ cảnh CAD là gì?

Tạo một PDF đơn có nghĩa là lấy một tệp nguồn CAD có thể chứa nhiều định nghĩa bố cục (paper spaces) và hợp nhất mỗi bố cục thành các trang riêng biệt của một tài liệu PDF. Điều này đặc biệt hữu ích cho bản vẽ kiến trúc, sơ đồ kỹ thuật, hoặc bất kỳ trường hợp nào khách hàng mong muốn một gói PDF hợp nhất.

## Tại sao nên sử dụng Aspose.CAD cho nhiệm vụ này?

- **Không phụ thuộc vào bên ngoài** – thuần .NET, không cần cài đặt AutoCAD.  
- **Kiểm soát đầy đủ quá trình raster hóa** – bạn có thể đặt kích thước trang, DPI và kích thước bố cục tùy chỉnh.  
- **Kết xuất độ trung thực cao** – dữ liệu vector được giữ lại khi có thể, đảm bảo đầu ra sắc nét.  
- **Sẵn sàng cho xử lý batch** – cùng một đoạn mã có thể được đặt trong vòng lặp để tự động xử lý nhiều bản vẽ.

## Yêu cầu trước

- Aspose.CAD cho .NET: Đảm bảo bạn đã cài đặt Aspose.CAD cho .NET. Bạn có thể tải xuống từ [here](https://releases.aspose.com/cad/net/).  
- Môi trường phát triển: Thiết lập môi trường phát triển .NET và có kiến thức cơ bản về lập trình C#.

## Nhập các Namespace

Trong dự án C# của bạn, bao gồm các namespace cần thiết để tận dụng các chức năng của Aspose.CAD cho .NET:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Hướng dẫn từng bước

### Bước 1: Tải hình ảnh CAD

Đầu tiên, tải tệp CAD nguồn (ví dụ, một bản vẽ DWG). Lớp `CadImage` cung cấp quyền truy cập vào tất cả các bố cục trong tệp.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // Your code for Step 1 goes here
}
```

### Bước 2: Tùy chỉnh tùy chọn raster hóa

Xác định cách mỗi bố cục sẽ được raster hóa. Bạn có thể đặt kích thước trang mặc định và sau đó ghi đè cho các bố cục cụ thể bằng cách sử dụng `LayoutPageSizes`.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// Custom sizes for several layouts
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

> **Mẹo chuyên nghiệp:** Điều chỉnh DPI (`rasterizationOptions.Resolution`) nếu bạn cần đầu ra độ phân giải cao hơn cho các bản vẽ chi tiết.

### Bước 3: Định nghĩa tùy chọn PDF

Đặt các cài đặt raster hóa vào trong một đối tượng `PdfOptions`. Điều này cho Aspose.CAD biết sẽ render dữ liệu CAD trực tiếp vào luồng PDF.

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

### Bước 4: Lưu dưới dạng PDF

Cuối cùng, gọi `Save` trên thể hiện `CadImage`, truyền tên tệp PDF đích và các tùy chọn đã chuẩn bị. Thư viện sẽ tạo một PDF đơn chứa một trang cho mỗi bố cục bạn đã cấu hình.

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

Sau lệnh này, bạn sẽ có một PDF kết hợp các bố cục “ANSI C Plot” và “8.5 x 11 Plot” thành một tài liệu thống nhất.

## Các khó khăn thường gặp & khắc phục

| Issue | Reason | Fix |
|-------|--------|-----|
| Bố cục bị thiếu trong PDF | `LayoutPageSizes` chưa được định nghĩa cho tên bố cục | Xác minh tên bố cục chính xác trong tệp CAD (phân biệt chữ hoa/thường). |
| Đầu ra chất lượng thấp | DPI mặc định là 96 | Đặt `rasterizationOptions.Resolution = 300` (hoặc cao hơn) trước khi lưu. |
| Không tìm thấy tệp | Đường dẫn `MyDir` sai | Sử dụng `Path.Combine` để xây dựng đường dẫn độc lập nền tảng. |

## Câu hỏi thường gặp

### Q1: Tôi có thể dùng Aspose.CAD cho .NET với các định dạng CAD khác không?

**A1:** Có, Aspose.CAD cho .NET hỗ trợ nhiều định dạng CAD như DWG, DXF, DGN và các định dạng khác.

### Q2: Có bản dùng thử miễn phí không?

**A2:** Có, bạn có thể khám phá bản dùng thử miễn phí [here](https://releases.aspose.com/).

### Q3: Làm sao tôi có thể nhận hỗ trợ cho Aspose.CAD cho .NET?

**A3:** Truy cập [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) để nhận hỗ trợ cộng đồng.

### Q4: Tôi có thể tìm tài liệu chi tiết ở đâu?

**A4:** Tham khảo tài liệu [here](https://reference.aspose.com/cad/net/).

### Q5: Tôi có thể mua giấy phép cho Aspose.CAD cho .NET không?

**A5:** Có, bạn có thể mua giấy phép [here](https://purchase.aspose.com/buy).

**Additional Q&A**

**Q:** Làm thế nào để **xuất DWG sang PDF** với kích thước trang tùy chỉnh?  
**A:** Sử dụng `CadRasterizationOptions.LayoutPageSizes` để ánh xạ mỗi bố cục DWG tới kích thước trang PDF mong muốn, như đã trình bày ở Bước 2.

**Q:** Có thể **lưu CAD dưới dạng PDF** mà không raster hóa dữ liệu vector không?  
**A:** Aspose.CAD luôn raster hóa khi tạo PDF, nhưng bạn có thể tăng DPI để giữ độ trung thực hình ảnh.

## Kết luận

Trong hướng dẫn này, chúng tôi đã trình bày cách **tạo PDF đơn** từ các bản vẽ CAD có nhiều bố cục, sử dụng Aspose.CAD cho .NET. Giờ bạn đã có các khối xây dựng để **chuyển đổi CAD sang PDF**, **xuất DWG sang PDF**, và **lưu CAD dưới dạng PDF** trong một quy trình tự động duy nhất. Hãy thử nghiệm các cài đặt raster hóa khác nhau để đáp ứng yêu cầu chất lượng của dự án, và tích hợp mã này vào các pipeline xử lý batch lớn hơn khi cần.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Cập nhật lần cuối:** 2026-03-02  
**Đã kiểm tra với:** Aspose.CAD cho .NET 24.11  
**Tác giả:** Aspose