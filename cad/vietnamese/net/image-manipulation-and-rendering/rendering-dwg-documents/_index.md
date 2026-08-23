---
date: 2026-08-23
description: Tìm hiểu cách tạo viewport dwg c# bằng Aspose.CAD. Hướng dẫn này bao
  gồm loading một tệp DWG, cấu hình rasterization, defining một viewport và saving
  kết quả dưới dạng PDF.
keywords:
- create viewport dwg c#
- render dwg c#
- aspose.cad .net
lastmod: 2026-08-23
linktitle: Kết xuất tài liệu DWG trong C#
og_description: Tìm hiểu cách tạo viewport dwg c# bằng Aspose.CAD trong .NET. Hướng
  dẫn step‑by‑step này cho thấy loading, rasterizing, defining viewports và saving
  sang PDF.
og_image_alt: Guide showing how to create viewport dwg c# with Aspose.CAD in .NET
og_title: Cách tạo viewport dwg c# với Aspose.CAD cho .NET
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Learn how to create viewport dwg c# using Aspose.CAD. This guide covers
    loading a DWG file, configuring rasterization, defining a viewport, and saving
    the result as PDF.
  headline: How to create viewport dwg c# with Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: Load the DWG file with `CadImage.Load`.
    question: What is the first step?
  - answer: '`Viewport` inside `CadRasterizationOptions`.'
    question: Which class defines the view area?
  - answer: Yes, using `PdfOptions` after rasterization.
    question: Can I output to PDF?
  - answer: A commercial license is required; a free trial works for evaluation.
    question: Do I need a license for production?
  - answer: Absolutely – Aspose.CAD works with .NET Framework, .NET Core, and .NET 5/6.
    question: Is .NET Core supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- create viewport dwg c#
- Aspose.CAD
- C# CAD rendering
- DWG to PDF
- CAD viewports
title: Cách tạo viewport dwg c# với Aspose.CAD cho .NET
url: /vi/net/image-manipulation-and-rendering/rendering-dwg-documents/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Kết xuất tài liệu DWG trong C# – hướng dẫn tạo viewport dwg c# tutorial

## Giới thiệu

Trong hướng dẫn toàn diện này, bạn sẽ học cách **create viewport dwg c#** với Aspose.CAD và chuyển đổi tệp DWG sang PDF. Cho dù bạn cần trích xuất một bố cục cụ thể, tạo một tờ in có thể in được, hoặc nhúng một chế độ xem CAD vào báo cáo, việc kiểm soát viewport mang lại cho bạn khả năng điều khiển việc kết xuất một cách chính xác. Aspose.CAD hỗ trợ **20+ CAD formats** và có thể xử lý các tệp có hàng ngàn thực thể mà không cần tải toàn bộ tài liệu vào bộ nhớ, làm cho nó lý tưởng cho các ứng dụng .NET hiệu suất cao.

## Câu trả lời nhanh
- **Bước đầu tiên là gì?** Load the DWG file with `CadImage.Load`.
- **Lớp nào định nghĩa khu vực xem?** `Viewport` inside `CadRasterizationOptions`.
- **Tôi có thể xuất ra PDF không?** Yes, using `PdfOptions` after rasterization.
- **Tôi có cần giấy phép cho môi trường sản xuất không?** A commercial license is required; a free trial works for evaluation.
- **.NET Core có được hỗ trợ không?** Absolutely – Aspose.CAD works with .NET Framework, .NET Core, and .NET 5/6.

## Yêu cầu trước

Before diving into the code, make sure you have:

- Kiến thức cơ bản về lập trình C#.
- Visual Studio (bất kỳ phiên bản gần đây nào) đã được cài đặt.
- Thư viện Aspose.CAD đã được thêm vào dự án của bạn. Bạn có thể tải xuống từ [Aspose.CAD download page](https://releases.aspose.com/cad/net/).
- Một tệp DWG mẫu như **Bottom_plate.dwg** để thực hành.

## Nhập không gian tên

Add the required `using` directives at the top of your C# file so the compiler can locate the Aspose.CAD types.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

Bây giờ môi trường đã sẵn sàng, chúng ta sẽ đi qua việc triển khai từng bước.

## Cách tạo viewport dwg c#?

Để tạo một viewport tùy chỉnh, đầu tiên tải tệp DWG vào một đối tượng `CadImage`, sau đó cấu hình `CadRasterizationOptions` với bố cục và tỷ lệ mong muốn. Xác định vùng bạn muốn hiển thị, khởi tạo một `CadVportTableObject` với trung tâm, chiều cao và tỷ lệ khung hình đã tính, thay thế viewport hiện hoạt, thiết lập các tùy chọn PDF nếu cần, và cuối cùng lưu kết quả.

## Bước 1: tải tệp dwg

`CadImage.Load` tải một tệp DWG vào một đối tượng `CadImage`, đại diện cho bản vẽ CAD trong bộ nhớ.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading the DWG file goes here.
}
```

## Bước 2: cấu hình tùy chọn rasterization

`CadRasterizationOptions` chỉ định cách raster hóa bản vẽ CAD, bao gồm việc chọn bố cục, tỷ lệ và kích thước đầu ra.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
// Additional rasterization configurations can be added here.
```

## Bước 3: xác định vùng vẽ

`Point` xác định tọa độ X và Y của góc trên‑trái của vùng cần render.

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## Bước 4: tạo một viewport mới

`CadVportTableObject` đại diện cho một đối tượng viewport kiểm soát khu vực hiển thị và tỷ lệ khung hình của bản vẽ đã render.

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## Bước 5: thay thế viewport hiện hoạt

Vòng lặp thay thế viewport hiện hoạt bằng viewport mới tạo để áp dụng các cài đặt hiển thị tùy chỉnh.

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## Bước 6: cấu hình tùy chọn PDF

`PdfOptions` cấu hình các tham số đầu ra PDF như nén và siêu dữ liệu.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Bước 7: lưu dwg đã render dưới dạng PDF

`image.Save` ghi hình ảnh đã render vào tệp bằng các tùy chọn định dạng đã chỉ định.

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## Tại sao nên sử dụng viewport tùy chỉnh khi render DWG?

Viewport tùy chỉnh cho phép bạn cô lập một bố cục hoặc vùng cụ thể, giảm kích thước tệp và cải thiện tốc độ render. Aspose.CAD có thể render một DWG 300 trang trong vòng dưới 2 giây khi sử dụng viewport tập trung, so với việc render toàn bộ bản vẽ có thể mất vài giây lâu hơn.

## Các vấn đề thường gặp và giải pháp

- **Blank output** – Đảm bảo các tọa độ viewport nằm trong phạm vi của bản vẽ; sử dụng `CadImage.Size` để kiểm tra giới hạn.
- **Missing layers** – Đặt `CadRasterizationOptions.Layouts` thành tên bố cục đúng; nếu không, bố cục mặc định có thể trống.
- **Performance slowdown** – Tắt anti‑aliasing trong `CadRasterizationOptions` nếu bạn chỉ cần một bản xem trước nhanh.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.CAD với các định dạng tệp CAD khác không?

A1: Có, Aspose.CAD hỗ trợ nhiều định dạng, bao gồm DWG, DXF, DWF và hơn 20 loại CAD khác.

### Câu hỏi 2: Aspose.CAD có tương thích với .NET Core không?

A2: Có, Aspose.CAD hoạt động với .NET Framework, .NET Core và các phiên bản .NET mới nhất.

### Câu hỏi 3: Làm thế nào tôi có thể xử lý các bố cục khác nhau trong tệp DWG?

A3: Xác định bố cục mong muốn bằng cách sử dụng thuộc tính `Layouts` của `CadRasterizationOptions` trước khi render.

### Câu hỏi 4: Có lưu ý nào về giấy phép khi sử dụng Aspose.CAD không?

A4: Để biết chi tiết về giấy phép, truy cập [Aspose.CAD licensing page](https://purchase.aspose.com/buy).

### Câu hỏi 5: Tôi có thể tìm hỗ trợ bổ sung ở đâu?

A5: Truy cập [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) để nhận trợ giúp và thảo luận từ cộng đồng.

### Câu hỏi 6: Tôi có thể render trực tiếp sang PNG thay vì PDF không?

A6: Có, thay đổi `PdfOptions` thành `PngOptions` và gọi `image.Save("output.png", pngOptions)`.

### Câu hỏi 7: Làm thế nào để nhúng hình ảnh đã render vào ứng dụng Windows Forms?

A7: Tải hình ảnh đã lưu vào điều khiển `PictureBox` bằng cách sử dụng `Image.FromFile("output.png")`.

## Kết luận

Bây giờ bạn đã biết cách **create viewport dwg c#** và render một tệp DWG sang PDF (hoặc các định dạng raster khác) bằng Aspose.CAD. Bằng cách thành thạo việc thao tác viewport, bạn sẽ có khả năng kiểm soát chi tiết đầu ra hình ảnh, điều này rất quan trọng để tạo ra các bản vẽ kỹ thuật chính xác, báo cáo hoặc hình thu nhỏ. Khám phá các cài đặt rasterization bổ sung, thử nghiệm với các định dạng đầu ra khác nhau, và tích hợp mã vào các dịch vụ .NET lớn hơn hoặc tiện ích desktop.

---

**Cập nhật lần cuối:** 2026-08-23  
**Được kiểm tra với:** Aspose.CAD 24.11 for .NET  
**Tác giả:** Aspose

## Hướng dẫn liên quan

- [Cách Đặt Viewport khi Chuyển Đổi DWG sang PDF với Tọa Độ trong C# - Hướng dẫn Aspose.CAD](/cad/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/)
- [Học Cách Đặt Tùy Chọn Rasterization CAD – Xuất Bố Cục Cụ Thể sang PDF với Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Cách chuyển DWG sang PDF và Hình Ảnh Raster bằng Aspose.CAD cho .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}