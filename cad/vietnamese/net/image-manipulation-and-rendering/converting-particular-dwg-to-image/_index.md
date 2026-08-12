---
date: 2026-08-12
description: Trích xuất văn bản từ DWG và chuyển đổi DWG cụ thể sang hình ảnh trong
  C# bằng Aspose.CAD cho .NET. Học từng bước với các đoạn mã mẫu.
keywords:
- extract text from dwg
- convert specific dwg to image
- Aspose.CAD .NET
lastmod: 2026-08-12
linktitle: Chuyển đổi DWG cụ thể sang hình ảnh trong C#
og_description: Trích xuất văn bản từ DWG và chuyển đổi DWG cụ thể sang hình ảnh trong
  C# với Aspose.CAD. Tham khảo hướng dẫn ngắn gọn này để triển khai nhanh chóng.
og_image_alt: Guide showing DWG to image conversion and text extraction using Aspose.CAD
  in C#
og_title: Trích xuất văn bản từ DWG và chuyển đổi DWG cụ thể sang hình ảnh trong C#
schemas:
- author: Aspose
  dateModified: '2026-08-12'
  description: Extract text from DWG and convert specific DWG to image in C# using
    Aspose.CAD for .NET. Learn step‑by‑step with code snippets.
  headline: Extract text from DWG and convert specific DWG to image in C#
  type: TechArticle
- questions:
  - answer: Aspose.CAD supports DWG releases from AutoCAD 2000 up to the latest 2024
      version, covering over 90 % of files created in the field.
    question: Is Aspose.CAD compatible with all versions of DWG files?
  - answer: Yes – you can change resolution, image format, anti‑aliasing, and background
      color to suit PNG, JPEG, or PDF targets.
    question: Can I customize the rasterization options for different outputs?
  - answer: Explore the comprehensive [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for more code samples and API details.
    question: Where can I find additional examples and documentation?
  - answer: Absolutely – you can download a trial version on the **[Aspose trial download
      page](https://releases.aspose.com/)** and evaluate all features without restrictions
      for 30 days.
    question: Is there a free trial available for Aspose.CAD?
  - answer: Join the active [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where developers share solutions and the Aspose team answers questions.
    question: How can I get support or connect with the community?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- extract text from dwg
- Aspose.CAD
- C# CAD processing
title: Trích xuất văn bản từ DWG và chuyển đổi DWG cụ thể sang hình ảnh trong C#
url: /vi/net/image-manipulation-and-rendering/converting-particular-dwg-to-image/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chuyển đổi DWG cụ thể sang hình ảnh trong C# - Hướng dẫn Aspose.CAD

## Giới thiệu

Trong các ứng dụng kỹ thuật hiện đại, bạn thường cần **trích xuất văn bản từ tệp DWG** và **chuyển đổi DWG cụ thể sang định dạng hình ảnh** để báo cáo hoặc trực quan hoá. Aspose.CAD cho .NET cung cấp cho bạn một API đầy đủ tính năng, xử lý cả hai nhiệm vụ mà không cần phần mềm CAD bên ngoài. Trong hướng dẫn này, bạn sẽ học cách tải DWG, lọc các thực thể văn bản, raster hoá bản vẽ, và cuối cùng lưu kết quả dưới dạng hình ảnh PDF — tất cả bằng mã C# sạch sẽ.

## Câu trả lời nhanh
- **Bước đầu tiên là gì?** Tải tệp DWG bằng `new CadImage("file.dwg")`.  
- **Lớp nào lọc văn bản?** Sử dụng `CadEntityFilter` để chọn các thực thể `Text`.  
- **Làm thế nào để xác định kích thước hình ảnh?** Đặt `Width` và `Height` trên `CadRasterizationOptions`.  
- **Định dạng đầu ra nào được sử dụng?** Ví dụ lưu dưới dạng PDF, trong đó nhúng hình ảnh raster.  
- **Tôi có cần giấy phép cho môi trường sản xuất không?** Có – giấy phép thương mại Aspose.CAD loại bỏ các giới hạn đánh giá.

## Cách trích xuất văn bản từ dwg?

Tải DWG, áp dụng bộ lọc chỉ chọn các thực thể văn bản, sau đó đọc thuộc tính `TextString` của mỗi thực thể. Cách tiếp cận này trả về mọi đoạn chú thích, nhãn hoặc văn bản kích thước có trong bản vẽ, cho phép bạn tái sử dụng chúng cho việc tìm kiếm, lập chỉ mục hoặc báo cáo.

## Tại sao chuyển đổi dwg cụ thể sang hình ảnh?

Chuyển đổi DWG sang hình ảnh raster cho phép bạn nhúng bản vẽ vào tài liệu, trang web hoặc ứng dụng di động không thể hiển thị định dạng CAD gốc. Aspose.CAD xử lý **hơn 50+ định dạng CAD** và có thể raster hoá các bản vẽ có hàng trăm trang trong khi sử dụng dưới 200 MB bộ nhớ, điều này làm cho nó phù hợp với các kịch bản máy chủ có lưu lượng cao.

## Yêu cầu trước

- Visual Studio (bất kỳ phiên bản mới nào) để biên dịch và chạy các dự án C#.  
- Aspose.CAD cho .NET – đảm bảo bạn đã cài đặt thư viện. Bạn có thể tìm liên kết tải xuống trên **[trang tải xuống Aspose.CAD cho .NET](https://releases.aspose.com/cad/net/)**.  
- Một tệp DWG bạn muốn làm việc; tệp mẫu *visualization_-_conference_room.dwg* được sử dụng trong các đoạn mã.

## Nhập không gian tên

Các không gian tên sau cung cấp cho bạn quyền truy cập vào các lớp CAD cốt lõi, tùy chọn raster hoá và các công cụ hỗ trợ xuất PDF:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Bước 1: tải tệp dwg

Tạo một thể hiện `CadImage` bằng cách truyền đường dẫn tới tệp DWG của bạn. Đối tượng `CadImage` đại diện cho toàn bộ bản vẽ trong bộ nhớ và cung cấp quyền truy cập vào các lớp, thực thể và siêu dữ liệu của nó.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
var cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath);
```

## Bước 2: lọc các thực thể

`CadEntityFilter` cho phép bạn chọn chỉ những thực thể bạn cần. Trong hướng dẫn này, chúng tôi cấu hình nó để giữ lại các đối tượng **text**, loại bỏ các đường, vòng tròn và các hình học khác mà bạn không muốn trong hình ảnh cuối cùng.

```csharp
CadBaseEntity[] entities = cadImage.Entities;
List<CadBaseEntity> filteredEntities = new List<CadBaseEntity>();

foreach (CadBaseEntity baseEntity in entities)
{
    // Selection or filtration of entities
    if (baseEntity.TypeName == CadEntityTypeName.TEXT)
    {
        filteredEntities.Add(baseEntity);
    }
}

cadImage.Entities = filteredEntities.ToArray();
```

## Bước 3: đặt tùy chọn raster hoá

`CadRasterizationOptions` điều khiển cách bản vẽ được chuyển thành bitmap. Bạn có thể xác định kích thước đầu ra, màu nền và độ phân giải (DPI). Định nghĩa sau đây giới thiệu lớp:

Lớp `CadRasterizationOptions` chỉ định kích thước hình ảnh, độ phân giải và cài đặt render cho việc chuyển đổi bản vẽ CAD sang định dạng raster.  

Đặt chiều rộng, chiều cao và màu nền mong muốn trước khi truyền các tùy chọn cho bộ xuất PDF.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## Bước 4: đặt tùy chọn PDF

`PdfOptions` gộp các cài đặt raster hoá với các tính năng đặc thù của PDF như nén. Định nghĩa cho lớp này xuất hiện đầu tiên:

`PdfOptions` bao gồm các tham số tạo PDF, bao gồm các tùy chọn raster hoá quyết định cách dữ liệu CAD được render trong tài liệu PDF.  

Gán thể hiện `CadRasterizationOptions` đã tạo trước đó vào thuộc tính `VectorRasterizationOptions`.

```csharp
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Bước 5: lưu dưới dạng PDF

Cuối cùng, gọi phương thức `Save` trên đối tượng `CadImage`, truyền tên tệp đích và `PdfOptions` đã cấu hình. PDF sẽ chứa một hình ảnh chất lượng cao của bản vẽ đã lọc.

```csharp
string outFile = MyDir + "result_out_generated.pdf";
cadImage.Save(outFile, pdfOptions);
```

## Các vấn đề thường gặp và khắc phục

- **Thiếu văn bản sau khi lọc** – Đảm bảo DWG thực sự chứa các thực thể `Text`; một số bản vẽ lưu chú thích dưới dạng `MText`. Điều chỉnh bộ lọc để bao gồm `MText` nếu cần.  
- **Hình ảnh đầu ra trống** – Kiểm tra DPI raster hoá đủ cao (300 DPI là giá trị mặc định an toàn) và màu nền không được đặt là trong suốt khi xem PDF.  
- **Lỗi hết bộ nhớ khi xử lý tệp lớn** – Sử dụng overload `LoadOptions` cho phép streaming, giúp ngăn toàn bộ tệp được tải vào bộ nhớ cùng một lúc.

## Câu hỏi thường gặp

**Q: Aspose.CAD có tương thích với mọi phiên bản tệp DWG không?**  
A: Aspose.CAD hỗ trợ các phiên bản DWG từ AutoCAD 2000 đến phiên bản mới nhất 2024, bao phủ hơn 90 % các tệp được tạo trong lĩnh vực này.

**Q: Tôi có thể tùy chỉnh các tùy chọn raster hoá cho các đầu ra khác nhau không?**  
A: Có – bạn có thể thay đổi độ phân giải, định dạng hình ảnh, khử răng cưa và màu nền để phù hợp với mục tiêu PNG, JPEG hoặc PDF.

**Q: Tôi có thể tìm các ví dụ và tài liệu bổ sung ở đâu?**  
A: Khám phá tài liệu toàn diện [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) để xem thêm mẫu mã và chi tiết API.

**Q: Có bản dùng thử miễn phí cho Aspose.CAD không?**  
A: Chắc chắn – bạn có thể tải phiên bản dùng thử trên **[trang tải xuống dùng thử Aspose](https://releases.aspose.com/)** và đánh giá tất cả tính năng không giới hạn trong 30 ngày.

**Q: Làm thế nào để tôi nhận được hỗ trợ hoặc kết nối với cộng đồng?**  
A: Tham gia diễn đàn [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) năng động, nơi các nhà phát triển chia sẻ giải pháp và đội ngũ Aspose trả lời các câu hỏi.

---

**Cập nhật lần cuối:** 2026-08-12  
**Kiểm tra với:** Aspose.CAD 24.11 for .NET  
**Tác giả:** Aspose

## Hướng dẫn liên quan

- [Tìm kiếm văn bản trong tệp DWG bằng C# - Hướng dẫn Aspose.CAD](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [Chuyển đổi bản vẽ CAD sang hình ảnh Raster trong Aspose.CAD cho .NET](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [Kết xuất tài liệu DWG trong C# - Hướng dẫn Aspose.CAD](/cad/net/image-manipulation-and-rendering/rendering-dwg-documents/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}