---
date: 2026-07-04
description: Tìm hiểu cách đặt kích thước trang PDF và xuất PDF từ hình ảnh CAD 3D
  bằng Aspose.CAD cho .NET – hướng dẫn chi tiết từng bước để chuyển đổi DWG sang PDF
  và lưu CAD dưới dạng PDF.
keywords:
- set pdf page size
- export pdf from cad
- convert dwg to pdf
- save cad as pdf
- cad to pdf tutorial
linktitle: Xuất hình ảnh 3D sang PDF
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  headline: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  type: TechArticle
- description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  name: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  steps:
  - name: Load the CAD Image
    text: '`Image` class represents a CAD drawing loaded into memory, ready for rasterization.'
  - name: Configure Rasterization Options (Save CAD as PDF)
    text: '`RasterizationOptions` class defines how the CAD data is rasterized, including
      page size, DPI, and whether 3‑D entities are rendered.'
  - name: Set PDF Options (Create PDF from CAD)
    text: '`PdfOptions` class holds the output format settings and links the rasterization
      options to PDF generation.'
  - name: Save as PDF (Generate PDF from 3D Model)
    text: '`Save` method on the `Image` object writes the rasterized content to the
      specified PDF file, producing a ready‑to‑share document.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports more than 50 input and output formats, including
      DWG, DXF, DGN, STL, and IFC, ensuring flexibility for any project.
    question: Is Aspose.CAD compatible with all CAD file formats?
  - answer: Absolutely. Set `PageWidth` and `PageHeight` in `RasterizationOptions`
      to any size in points, inches, or millimetres before calling `Save`.
    question: Can I customize the page dimensions when exporting to PDF?
  - answer: Yes, you can obtain temporary licenses for Aspose.CAD by visiting [Temporary
      License](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for Aspose.CAD?
  - answer: Head to the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for
      expert help and peer‑to‑peer advice.
    question: Where can I find additional support or community discussions?
  - answer: Yes, you can explore the features of Aspose.CAD by accessing the [free
      trial](https://releases.aspose.com/).
    question: Is there a free trial version of Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Đặt kích thước trang PDF – Xuất hình ảnh 3D sang PDF với Aspose.CAD
url: /vi/net/3d-image-export/exporting-3d-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xuất hình ảnh 3D sang PDF - Hướng dẫn Aspose.CAD

## Giới thiệu

Nếu bạn cần **đặt kích thước trang PDF** khi chuyển đổi bản vẽ CAD 3‑D sang PDF, bạn đã đến đúng nơi. Bài hướng dẫn này sẽ chỉ cho bạn, từng bước, cách tải tệp CAD, cấu hình các tùy chọn rasterization—bao gồm kích thước trang tùy chỉnh—và tạo ra một PDF chất lượng cao bằng Aspose.CAD cho .NET. Khi kết thúc, bạn sẽ có thể **xuất PDF từ CAD**, **lưu CAD dưới dạng PDF**, và kiểm soát mọi chi tiết bố cục mà không cần cài đặt AutoCAD.

## Câu trả lời nhanh
- **“export PDF from CAD” có nghĩa là gì?** Nó chuyển đổi một bản vẽ CAD (DWG, DXF, DGN, v.v.) thành một tệp PDF có thể mở trên bất kỳ thiết bị nào.  
- **Thư viện nào thực hiện việc chuyển đổi?** Aspose.CAD cho .NET cung cấp rasterization và xuất PDF mà không cần phụ thuộc bên ngoài.  
- **Tôi có cần giấy phép không?** Cần có giấy phép tạm thời hoặc đầy đủ cho môi trường sản xuất; bản dùng thử miễn phí có sẵn.  
- **Tôi có thể đặt kích thước trang tùy chỉnh không?** Có — sử dụng `PageWidth` và `PageHeight` trong `RasterizationOptions`.  
- **Độ hình 3‑D có được giữ lại không?** Các thực thể 3‑D được rasterize; bật `TypeOfEntities.Entities3D` để hỗ trợ đầy đủ 3‑D.

## “export PDF” là gì trong ngữ cảnh CAD?

Xuất PDF từ CAD có nghĩa là lấy một bản vẽ CAD (DWG, DXF, DGN, v.v.) và chuyển đổi nó thành một tệp PDF có thể chứa đồ họa vector, các góc nhìn 3‑D rasterized, và thông tin bố cục trang chính xác, giúp dễ dàng chia sẻ với bất kỳ ai không có phần mềm CAD.

## Tại sao nên dùng Aspose.CAD để xuất PDF?

Aspose.CAD cho phép bạn **đặt kích thước trang PDF** và xuất PDF hoàn toàn bằng mã .NET quản lý. Nó hỗ trợ hơn 50 định dạng CAD, xử lý các tệp lên tới 2 GB mà không cần tải toàn bộ tài liệu vào bộ nhớ, và giữ nguyên độ dày đường, màu sắc, cũng như việc render thực thể 3‑D tùy chọn với DPI rasterization lên tới 1200. Thư viện chạy trên Windows, Linux và macOS, vì vậy các PDF được tạo ra hoạt động trên bất kỳ nền tảng nào.

## Yêu cầu trước

- **Aspose.CAD cho .NET** đã được cài đặt. Tải xuống từ [trang tải Aspose.CAD cho .NET](https://releases.aspose.com/cad/net/).  
- Một thư mục chứa các tệp CAD bạn muốn chuyển đổi (ví dụ, `C:\CAD\`).  
- .NET 6.0 hoặc mới hơn (hoặc .NET Framework 4.7.2).  

## Nhập không gian tên

Các câu lệnh `using` nhập các không gian tên của Aspose.CAD cần thiết để làm việc với rasterization và các tùy chọn PDF.  

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Hướng dẫn từng bước

### Cách đặt kích thước trang PDF khi xuất CAD sang PDF?

Tải tệp CAD của bạn, cấu hình kích thước trang trong `RasterizationOptions`, gắn các tùy chọn đó vào một thể hiện `PdfOptions`, và gọi `Save`. Quy trình bốn bước này cho phép bạn kiểm soát hoàn toàn kích thước và chất lượng đầu ra trong khi giữ mã ngắn gọn.

### Bước 1: Tải hình ảnh CAD

Lớp `Image` đại diện cho bản vẽ CAD được tải vào bộ nhớ, sẵn sàng cho rasterization.  

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD image goes here
}
```

### Bước 2: Cấu hình tùy chọn Rasterization (Lưu CAD dưới dạng PDF)

Lớp `RasterizationOptions` định nghĩa cách dữ liệu CAD được rasterize, bao gồm kích thước trang, DPI và việc render thực thể 3‑D.  

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

### Bước 3: Đặt tùy chọn PDF (Tạo PDF từ CAD)

Lớp `PdfOptions` chứa các cài đặt định dạng đầu ra và liên kết các tùy chọn rasterization với việc tạo PDF.  

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Bước 4: Lưu dưới dạng PDF (Tạo PDF từ mô hình 3D)

Phương thức `Save` trên đối tượng `Image` ghi nội dung rasterized vào tệp PDF được chỉ định, tạo ra một tài liệu sẵn sàng chia sẻ.  

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|------------|----------|
| **PDF đầu ra trống** | Tên layout sai hoặc thiếu layout `Model`. | Kiểm tra `rasterizationOptions.Layouts` khớp với một layout có trong tệp CAD. |
| **Độ phân giải thấp** | DPI rasterization mặc định quá thấp. | Đặt `rasterizationOptions.Resolution = 300;` trước khi lưu. |
| **Thực thể 3‑D không hiển thị** | `TypeOfEntities` bị comment. | Bỏ comment `rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;`. |
| **Lỗi giấy phép** | Sử dụng bản dùng thử mà không có giấy phép. | Áp dụng giấy phép tạm thời hoặc vĩnh viễn bằng `License license = new License(); license.SetLicense("Aspose.CAD.lic");`. |

## Câu hỏi thường gặp

**H: Aspose.CAD có tương thích với tất cả các định dạng tệp CAD không?**  
Đ: Có, Aspose.CAD hỗ trợ hơn 50 định dạng đầu vào và đầu ra, bao gồm DWG, DXF, DGN, STL và IFC, đảm bảo tính linh hoạt cho bất kỳ dự án nào.

**H: Tôi có thể tùy chỉnh kích thước trang khi xuất sang PDF không?**  
Đ: Chắc chắn. Đặt `PageWidth` và `PageHeight` trong `RasterizationOptions` thành bất kỳ kích thước nào bằng điểm, inch hoặc milimet khi gọi `Save`.

**H: Có giấy phép tạm thời cho Aspose.CAD không?**  
Đ: Có, bạn có thể lấy giấy phép tạm thời cho Aspose.CAD bằng cách truy cập [Temporary License](https://purchase.aspose.com/temporary-license/).

**H: Tôi có thể tìm hỗ trợ bổ sung hoặc thảo luận cộng đồng ở đâu?**  
Đ: Đến [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) để nhận trợ giúp từ chuyên gia và lời khuyên từ cộng đồng.

**H: Có phiên bản dùng thử miễn phí của Aspose.CAD không?**  
Đ: Có, bạn có thể khám phá các tính năng của Aspose.CAD bằng cách truy cập [free trial](https://releases.aspose.com/).

## Kết luận

Bạn giờ đã có một phương pháp hoàn chỉnh, sẵn sàng cho sản xuất để **đặt kích thước trang PDF** và **xuất PDF từ hình ảnh CAD 3D** bằng Aspose.CAD cho .NET. Bằng cách điều chỉnh các tùy chọn rasterization, bạn có thể tinh chỉnh độ phân giải, bố cục trang và việc render thực thể 3‑D để đáp ứng bất kỳ yêu cầu tài liệu nào. Hãy thử các thiết lập DPI và kích thước trang khác nhau để đạt được cân bằng hoàn hảo giữa kích thước tệp và độ trung thực hình ảnh.

{{< blocks/products/products-backtop-button >}}

## Hướng dẫn liên quan

- [Xuất các layout cụ thể sang PDF - Hướng dẫn Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Xuất DWG sang PDF hoặc hình raster - Hướng dẫn Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Xuất DGN sang PDF trong Aspose.CAD cho .NET](/cad/net/cad-export-formats/export-dgn-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

--- 

**Last Updated:** 2026-07-04  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose