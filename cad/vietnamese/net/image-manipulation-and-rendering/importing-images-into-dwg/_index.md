---
date: 2026-08-17
description: Tìm hiểu cách thêm image vào file dwg bằng C# và Aspose.CAD cho .NET.
  Hướng dẫn này sẽ chỉ cho bạn cách importing images, setting insertion points và
  exporting to PDF.
keywords:
- add image to dwg
- convert dwg to pdf
- set insertion point dwg
- embed png in dwg
- save dwg as pdf
lastmod: 2026-08-17
linktitle: Importing Images vào file DWG bằng C#
og_description: Tìm hiểu cách thêm image vào file dwg bằng C#. Hướng dẫn này bao gồm
  importing images, setting insertion points và converting dwg to pdf với Aspose.CAD.
og_image_alt: Guide showing C# code to embed an image into a DWG file using Aspose.CAD
og_title: Cách thêm image vào file dwg bằng C# sử dụng Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  headline: How to add image to dwg files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  name: How to add image to dwg files with C# using Aspose.CAD
  steps:
  - name: set up your document directory
    text: Prepare the folder that contains the source DWG and the image you want to
      embed.
  - name: load the dwg file
    text: The `CadImage` class represents a DWG drawing and provides access to its
      entities, layers, and metadata.
  - name: define the image properties
    text: Create an `Image` object that points to the raster file (e.g., PNG) and
      specify its format.
  - name: set insertion point dwg and vectors
    text: Specify where the image should appear inside the drawing and how it should
      be scaled. The insertion point is defined by a 2‑D coordinate, while the vectors
      control width and height.
  - name: create and configure the raster image
    text: Instantiate a `RasterImage` object, assign the image data, and set any additional
      rendering options.
  - name: add image to dwg file
    text: Insert the configured raster image into the DWG’s entities collection so
      it becomes part of the drawing.
  - name: save as pdf (export dwg to pdf)
    text: After embedding the image you can **convert dwg to pdf** or **save dwg as
      pdf** with a single call. This is useful for sharing the drawing with stakeholders
      who don’t have CAD software.
  type: HowTo
- questions:
  - answer: The core library is .NET‑specific, but Aspose offers equivalent APIs for
      Java, Python and other platforms.
    question: Can I use Aspose.CAD for .NET with other programming languages?
  - answer: Yes, you can explore a free trial on the [Aspose free trial page](https://releases.aspose.com/).
    question: Is a free trial available for Aspose.CAD?
  - answer: The documentation is available in the [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/).
    question: Where can I find detailed documentation for Aspose.CAD?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to get a temporary license.
    question: How do I obtain a temporary license for Aspose.CAD?
  - answer: Yes, you can seek support and engage with the community in the [Aspose.CAD
      community forum](https://forum.aspose.com/c/cad/19).
    question: Are there community forums for Aspose.CAD support?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD
- Aspose.CAD
- C# image processing
- DWG manipulation
title: Cách thêm image vào file dwg bằng C# sử dụng Aspose.CAD
url: /vi/net/image-manipulation-and-rendering/importing-images-into-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách thêm hình ảnh vào tệp dwg bằng C# sử dụng Aspose.CAD

## Giới thiệu

Thêm một hình ảnh vào tệp DWG là yêu cầu thường gặp khi bạn cần làm phong phú bản vẽ CAD bằng logo, ảnh hoặc đồ họa raster. Trong hướng dẫn này, bạn sẽ học cách **thêm hình ảnh vào dwg** một cách lập trình bằng C# và Aspose.CAD cho .NET, sau đó tùy chọn chuyển đổi kết quả sang PDF. Các bước được chia nhỏ để bạn có thể sao chép‑dán từng phần vào dự án của mình.

## Câu trả lời nhanh
- **Thư viện nào thực hiện công việc?** Aspose.CAD cho .NET.  
- **Có thể nhúng tệp PNG không?** Có – PNG, JPEG, BMP và các định dạng raster khác được hỗ trợ.  
- **Cần giấy phép cho việc phát triển không?** Bản dùng thử miễn phí đủ cho việc thử nghiệm; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Xuất PDF có được hỗ trợ không?** Hoàn toàn – bạn có thể chuyển đổi DWG đã cập nhật sang PDF chỉ bằng một dòng lệnh.  
- **Các phiên bản .NET nào tương thích?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## DWG là gì?

DWG là định dạng nhị phân gốc của các bản vẽ Autodesk AutoCAD, lưu trữ hình học vector, lớp và siêu dữ liệu. Định dạng này được sử dụng rộng rãi trong kiến trúc, kỹ thuật và xây dựng, và Aspose.CAD có thể đọc và ghi DWG mà không cần cài đặt AutoCAD.

## Tại sao thêm hình ảnh vào dwg với Aspose.CAD?

Aspose.CAD hỗ trợ **hơn 50 định dạng đầu vào và đầu ra**, có thể xử lý các tệp lớn hơn 500 MB mà không tải toàn bộ tài liệu vào bộ nhớ, và cung cấp API xác định hoạt động tốt trong môi trường server không giao diện. Điều này giúp xử lý hàng loạt bản vẽ DWG nhanh chóng và đáng tin cậy.

## Yêu cầu trước
- Kiến thức cơ bản về lập trình C#.  
- Aspose.CAD cho .NET đã được cài đặt. Bạn có thể tải xuống từ [trang tải Aspose.CAD cho .NET](https://releases.aspose.com/cad/net/). Bạn cũng có thể khám phá các sản phẩm Aspose khác trên [trang phát hành Aspose](https://releases.aspose.com/).  
- Môi trường phát triển như Visual Studio 2022 hoặc mới hơn.

## Cách thêm hình ảnh vào dwg bằng Aspose.CAD?

Tải DWG mục tiêu, tạo đối tượng hình ảnh raster mô tả bức ảnh muốn nhúng, đặt điểm chèn và vector tỉ lệ, sau đó gắn hình ảnh vào bản vẽ. Cuối cùng, lưu DWG đã chỉnh sửa hoặc xuất trực tiếp sang PDF. Toàn bộ quy trình chỉ cần một vài lời gọi API và chạy dưới một giây cho các bản vẽ 2 trang điển hình.

### Nhập không gian tên
Bao gồm các không gian tên cung cấp các lớp CAD cần thiết.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

### Bước 1: thiết lập thư mục tài liệu của bạn
Chuẩn bị thư mục chứa DWG nguồn và hình ảnh muốn nhúng.

```csharp
string MyDir = "Your Document Directory";
```

### Bước 2: tải tệp dwg
Lớp `CadImage` đại diện cho bản vẽ DWG và cung cấp quyền truy cập vào các thực thể, lớp và siêu dữ liệu của nó.

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

### Bước 3: xác định thuộc tính hình ảnh
Tạo một đối tượng `Image` trỏ tới tệp raster (ví dụ: PNG) và chỉ định định dạng của nó.

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

### Bước 4: đặt điểm chèn và vector cho dwg
Xác định vị trí hình ảnh sẽ xuất hiện trong bản vẽ và cách nó sẽ được thu phóng. Điểm chèn được định nghĩa bằng tọa độ 2‑D, trong khi các vector điều khiển chiều rộng và chiều cao.

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Bước 5: tạo và cấu hình hình ảnh raster
Khởi tạo một đối tượng `RasterImage`, gán dữ liệu hình ảnh và thiết lập các tùy chọn render bổ sung nếu cần.

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

### Bước 6: thêm hình ảnh vào tệp dwg
Chèn hình ảnh raster đã cấu hình vào bộ sưu tập thực thể của DWG để nó trở thành một phần của bản vẽ.

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

### Bước 7: lưu dưới dạng pdf (xuất dwg sang pdf)
Sau khi nhúng hình ảnh, bạn có thể **chuyển đổi dwg sang pdf** hoặc **lưu dwg dưới dạng pdf** chỉ bằng một lời gọi. Điều này hữu ích khi chia sẻ bản vẽ với những người không có phần mềm CAD.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;

cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
cadImage1.Save(MyDir + "export2.pdf", pdfOptions);
```

## Cách chuyển đổi dwg sang pdf sau khi nhúng hình ảnh?

Gọi phương thức `Save` trên đối tượng `CadImage`, truyền `SaveFormat.Pdf` và tùy chọn một đối tượng `PdfOptions` để kiểm soát kích thước trang, rasterization và siêu dữ liệu. Aspose.CAD giữ nguyên hình ảnh raster đã nhúng, các lớp và độ dày đường, tạo ra bản PDF trung thực có thể mở bằng bất kỳ trình xem nào. Việc chuyển đổi này chỉ cần một dòng mã.

## Các vấn đề thường gặp và giải pháp
- **Hình ảnh xuất hiện ở vị trí sai** – kiểm tra lại tọa độ điểm chèn và các vector hướng; chúng tính tương đối so với gốc của bản vẽ.  
- **Hình ảnh lớn gây tăng đột biến bộ nhớ** – sử dụng tùy chọn `Resize` trên hình raster trước khi chèn, hoặc làm việc với bản sao có độ phân giải thấp hơn.  
- **Xuất PDF mất chất lượng vector** – đảm bảo bạn lưu với `PdfOptions` giữ lại dữ liệu vector; hình raster luôn được nhúng nguyên trạng.

## Câu hỏi thường gặp

**Q: Tôi có thể dùng Aspose.CAD cho .NET với các ngôn ngữ lập trình khác không?**  
A: Thư viện lõi chỉ dành cho .NET, nhưng Aspose cung cấp API tương đương cho Java, Python và các nền tảng khác.

**Q: Có bản dùng thử miễn phí cho Aspose.CAD không?**  
A: Có, bạn có thể khám phá bản dùng thử miễn phí trên [trang dùng thử miễn phí của Aspose](https://releases.aspose.com/).

**Q: Tôi có thể tìm tài liệu chi tiết cho Aspose.CAD ở đâu?**  
A: Tài liệu có sẵn trong [tham khảo API .NET của Aspose.CAD](https://reference.aspose.com/cad/net/).

**Q: Làm sao để lấy giấy phép tạm thời cho Aspose.CAD?**  
A: Truy cập [trang giấy phép tạm thời](https://purchase.aspose.com/temporary-license/) để nhận giấy phép tạm thời.

**Q: Có diễn đàn cộng đồng nào hỗ trợ Aspose.CAD không?**  
A: Có, bạn có thể tìm kiếm hỗ trợ và tham gia cộng đồng tại [diễn đàn cộng đồng Aspose.CAD](https://forum.aspose.com/c/cad/19).

---

**Cập nhật lần cuối:** 2026-08-17  
**Đã kiểm tra với:** Aspose.CAD 24.11 cho .NET  
**Tác giả:** Aspose

## Hướng dẫn liên quan

- [Exporting DWG to PDF or Raster Images - Aspose.CAD Guide](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Exporting DWG to DXF Format in C# - Aspose.CAD Tutorial](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)
- [Exporting Specific Layouts to PDF - Aspose.CAD Guide](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}