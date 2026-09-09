---
date: 2026-09-09
description: Tìm hiểu cách cắt khối trong CAD, chuyển đổi DXF sang PDF và lưu CAD
  dưới dạng PDF bằng Aspose.CAD for .NET. Thực hiện theo hướng dẫn từng bước.
keywords:
- how to clip block
- convert dxf to pdf
- save cad as pdf
- create pdf from cad
- load cad image
lastmod: 2026-09-09
linktitle: Hỗ trợ cắt khối trong CAD
og_description: Tìm hiểu cách cắt khối trong CAD, chuyển đổi DXF sang PDF và lưu CAD
  dưới dạng PDF với Aspose.CAD for .NET. Hướng dẫn nhanh cho nhà phát triển.
og_image_alt: Screenshot of block clipping in a CAD drawing using Aspose.CAD for .NET
og_title: Cách cắt khối trong CAD bằng Aspose.CAD for .NET
schemas:
- author: Aspose
  dateModified: '2026-09-09'
  description: Learn how to clip block in CAD, convert DXF to PDF and save CAD as
    PDF using Aspose.CAD for .NET. Follow this step‑by‑step guide.
  headline: How to clip block in CAD using Aspose.CAD for .NET
  type: TechArticle
- description: Learn how to clip block in CAD, convert DXF to PDF and save CAD as
    PDF using Aspose.CAD for .NET. Follow this step‑by‑step guide.
  name: How to clip block in CAD using Aspose.CAD for .NET
  steps:
  - name: define the document directory
    text: Replace “Your Document Directory” with the actual path to your CAD documents.
  - name: specify input and output files
    text: Adjust the file names as per your project requirements.
  - name: load CAD image
    text: The `Image` class **loads CAD image** from the specified input file, enabling
      you to apply clipping before any rendering.
  - name: configure rasterization options
    text: Customize rasterization options according to your rendering needs, such
      as setting the output resolution or background color.
  - name: save as PDF
    text: Save the processed CAD image as a PDF file, effectively **saving CAD as
      PDF** while the block remains clipped.
  type: HowTo
- questions:
  - answer: No, clipping is applied only during rasterization; vector exports retain
      the original geometry.
    question: Does block clipping affect vector export formats like SVG?
  - answer: The library can process files up to **2 GB** on a 64‑bit process without
      full memory loading.
    question: What is the maximum file size Aspose.CAD can handle when clipping?
  - answer: Yes—iterate through `image.Blocks` and assign a `BlockClippingInfo` to
      each target block before saving.
    question: Can I clip multiple blocks in one operation?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD clipping
- Aspose.CAD
- .NET CAD processing
- PDF conversion
title: Cách cắt khối trong CAD bằng Aspose.CAD for .NET
url: /vi/net/layout-and-object-handling/supporting-block-clipping-in-cad/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách cắt khối trong CAD bằng Aspose.CAD cho .NET

## Giới thiệu

Trong hướng dẫn toàn diện này, bạn sẽ học **cách cắt khối** trong bản vẽ CAD, chuyển DXF sang PDF và lưu CAD dưới dạng PDF—tất cả đều với Aspose.CAD cho .NET. Việc cắt khối cho phép bạn ẩn hoặc hiển thị các phần của một khối mà không thay đổi hình học gốc, một kỹ thuật giúp tăng tốc độ render và giảm kích thước tệp.

## Câu trả lời nhanh
- **Block clipping làm gì?** Nó ẩn hình học đã chọn bên trong một khối dựa trên ranh giới cắt.  
- **Thư viện nào hỗ trợ tính năng này?** Aspose.CAD cho .NET cung cấp API tích hợp cho block clipping.  
- **Tôi có cần giấy phép không?** Cần có giấy phép tạm thời hoặc vĩnh viễn để sử dụng trong môi trường sản xuất.  
- **Tôi có thể chuyển DXF sang PDF không?** Có—sử dụng cùng các tùy chọn rasterization và gọi `Save` với định dạng PDF.  
- **Các phiên bản .NET nào được hỗ trợ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Block clipping là gì?

`Block clipping` là một tính năng CAD định nghĩa vùng cắt cho một thực thể khối, khiến các hình học nằm ngoài vùng này bị bỏ qua trong quá trình rasterization. Điều này cải thiện hiệu suất khi chỉ cần hiển thị một phần của khối lớn.

## Tại sao nên sử dụng block clipping trong CAD?

Aspose.CAD hỗ trợ **hơn 50** định dạng CAD và BIM và có thể xử lý các tệp lên tới **2 GB** mà không cần tải toàn bộ tệp vào bộ nhớ. Sử dụng block clipping giảm diện tích render lên tới **70 %**, giúp tăng tốc chuyển đổi PDF và giảm tiêu thụ bộ nhớ trên các công việc phía máy chủ.

## Yêu cầu trước

- Kiến thức cơ bản về ngôn ngữ lập trình C#.  
- Visual Studio đã được cài đặt trên máy của bạn.  
- Thư viện Aspose.CAD cho .NET. Bạn có thể tải xuống từ [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).  
- Một tệp CAD mẫu để thử nghiệm. Bạn có thể sử dụng tệp DXF được cung cấp.

## Nhập không gian tên

Trong dự án C# của bạn, hãy chắc chắn nhập các không gian tên cần thiết để làm việc với Aspose.CAD:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

Bây giờ, chúng ta sẽ phân tích mã mẫu thành nhiều bước:

## Cách cắt khối trong CAD?

`Lớp `Image` tải bản vẽ CAD vào bộ nhớ, và `BlockClippingInfo` định nghĩa đa giác cắt cho một khối. Tải bản vẽ CAD của bạn bằng `new Image("input.dxf")`, tạo một đối tượng `BlockClippingInfo` xác định đa giác cắt, gán nó cho khối mục tiêu qua `image.Blocks["BlockName"].ClippingInfo = clippingInfo`, và cuối cùng rasterize hoặc lưu ảnh. Quy trình này cắt khối trong một lần duy nhất và hoạt động cho cả nguồn DXF và DWG.

### Bước 1: xác định thư mục tài liệu

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
```

Thay thế “Your Document Directory” bằng đường dẫn thực tế tới các tài liệu CAD của bạn.

### Bước 2: chỉ định tệp đầu vào và đầu ra

```csharp
string inputFile = MyDir + "SLS-CW-CD-CE001-R01_blockClip.dxf";
string outputFile = MyDir + "SLS-CW-CD-CE001-R01_blockClip.pdf";
```

Điều chỉnh tên tệp theo yêu cầu dự án của bạn.

### Bước 3: tải ảnh CAD

```csharp
using (CadImage cadImage = (CadImage)Image.Load(inputFile))
{
```

Lớp `Image` **tải ảnh CAD** từ tệp đầu vào đã chỉ định, cho phép bạn áp dụng cắt trước khi render bất kỳ.

### Bước 4: cấu hình tùy chọn rasterization

```csharp
var rasterizationOptions = new CadRasterizationOptions
{
    BackgroundColor = Aspose.CAD.Color.White,
    DrawType = CadDrawTypeMode.UseObjectColor,
    PageWidth = 1200,
    PageHeight = 1600,
    Margins = new Margins
    {
        Top = 5,
        Right = 30,
        Bottom = 5,
        Left = 30
    },
    Layouts = new string[] { "Model" }
};
```

Tùy chỉnh các tùy chọn rasterization theo nhu cầu render của bạn, chẳng hạn đặt độ phân giải đầu ra hoặc màu nền.

### Bước 5: lưu dưới dạng PDF

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outputFile, pdfOptions);
```

Lưu ảnh CAD đã xử lý dưới dạng tệp PDF, thực tế **lưu CAD dưới dạng PDF** trong khi khối vẫn được cắt.

## Kết luận

Chúc mừng! Bạn đã triển khai thành công block clipping trong CAD bằng Aspose.CAD cho .NET, và giờ bạn biết cách **chuyển DXF sang PDF**, **lưu CAD dưới dạng PDF**, và **tải ảnh CAD** để xử lý tiếp theo. Những kỹ thuật này cung cấp cho bạn khả năng kiểm soát chi tiết hiệu suất render và chất lượng đầu ra.

## Câu hỏi thường gặp

### Q1: Tôi có thể sử dụng Aspose.CAD cho .NET với các ngôn ngữ lập trình khác không?

A1: Aspose.CAD chủ yếu được thiết kế cho các ứng dụng .NET. Nếu bạn làm việc với các ngôn ngữ khác, hãy cân nhắc khám phá Aspose.CAD cho Java.

### Q2: Có các tùy chọn cấp phép nào cho Aspose.CAD không?

A2: Có, bạn có thể khám phá các tùy chọn cấp phép và mua hàng tại [Aspose.CAD licensing page](https://purchase.aspose.com/buy).

### Q3: Có bản dùng thử miễn phí cho Aspose.CAD cho .NET không?

A3: Có, bạn có thể truy cập bản dùng thử miễn phí tại [Aspose product releases page](https://releases.aspose.com/).

### Q4: Làm sao tôi có thể nhận hỗ trợ cho Aspose.CAD?

A4: Truy cập [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) để nhận hỗ trợ cộng đồng và thảo luận.

### Q5: Tôi có thể sử dụng Aspose.CAD mà không có giấy phép vĩnh viễn không?

A5: Có, bạn có thể nhận giấy phép tạm thời tại [temporary license request page](https://purchase.aspose.com/temporary-license/).

**Q: Việc cắt khối có ảnh hưởng đến các định dạng xuất vector như SVG không?**  
A: Không, việc cắt chỉ được áp dụng trong quá trình rasterization; các xuất vector vẫn giữ nguyên hình học gốc.

**Q: Kích thước tệp tối đa mà Aspose.CAD có thể xử lý khi cắt khối là bao nhiêu?**  
A: Thư viện có thể xử lý các tệp lên tới **2 GB** trên quy trình 64‑bit mà không cần tải toàn bộ vào bộ nhớ.

**Q: Tôi có thể cắt nhiều khối trong một thao tác không?**  
A: Có—lặp qua `image.Blocks` và gán một `BlockClippingInfo` cho mỗi khối mục tiêu trước khi lưu.

---

**Cập nhật lần cuối:** 2026-09-09  
**Kiểm tra với:** Aspose.CAD 24.11 cho .NET  
**Tác giả:** Aspose

## Hướng dẫn liên quan

- [Cách chuyển đổi và xuất bản vẽ CAD sang PDF với Aspose.CAD cho .NET – Hướng dẫn](/cad/net/advanced-export-techniques/exporting-cad-drawings-to-pdf/)
- [Ví dụ Aspose CAD: Chuyển đổi bố cục sang ảnh raster trong .NET](/cad/net/cad-drawing-manipulation/convert-layouts-to-raster-image/)
- [Tạo PDF từ bố cục DXF cụ thể – Hướng dẫn Aspose.CAD](/cad/net/export-techniques/exporting-dxf-specific-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}