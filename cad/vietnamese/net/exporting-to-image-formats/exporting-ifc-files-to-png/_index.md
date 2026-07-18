---
date: 2026-07-18
description: Cách xuất CAD sang PNG bằng Aspose.CAD cho .NET. Chuyển đổi tệp IFC thành
  ảnh PNG chất lượng cao một cách nhanh chóng và đáng tin cậy.
keywords:
- how to export cad to png
- Aspose.CAD IFC conversion
- CAD to PNG .NET
lastmod: 2026-07-18
linktitle: Xuất tệp IFC sang PNG
og_description: Cách xuất CAD sang PNG bằng Aspose.CAD cho .NET. Tìm hiểu quy trình
  chuyển đổi tệp IFC sang ảnh PNG từng bước mà không cần viết mã.
og_image_alt: Guide showing IFC to PNG conversion with Aspose.CAD for .NET
og_title: Cách xuất CAD sang PNG – Hướng dẫn Aspose.CAD .NET
schemas:
- author: Aspose
  dateModified: '2026-07-18'
  description: How to export CAD to PNG using Aspose.CAD for .NET. Convert IFC files
    to high‑quality PNG images quickly and reliably.
  headline: How to Export CAD to PNG – Exporting IFC Files with Aspose.CAD
  type: TechArticle
- questions:
  - answer: No, Aspose.CAD for .NET is specifically designed for Windows environments.
    question: Can I use Aspose.CAD for .NET on macOS or Linux?
  - answer: Yes, you can obtain a temporary license from [here](https://purchase.aspose.com/temporary-license/)
      for evaluation.
    question: Is a temporary license available for testing purposes?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and discussions.
    question: How can I get support for Aspose.CAD?
  - answer: Refer to the [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for detailed information and examples.
    question: Where can I find comprehensive documentation?
  - answer: Check the documentation or seek assistance on the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).
    question: What if I encounter issues during installation?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- export cad
- Aspose.CAD
- IFC to PNG
- .NET image conversion
title: Cách xuất CAD sang PNG – Xuất tệp IFC với Aspose.CAD
url: /vi/net/exporting-to-image-formats/exporting-ifc-files-to-png/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách Xuất CAD sang PNG – Xuất Tệp IFC với Aspose.CAD

## Giới thiệu

Nếu bạn cần **how to export cad to png**, Aspose.CAD cho .NET cung cấp một cách đáng tin cậy, không cần viết mã để chuyển các mô hình IFC (Industry Foundation Classes) thành các hình ảnh raster PNG sắc nét. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn toàn bộ quy trình — từ cài đặt thư viện đến lưu PNG cuối cùng — để bạn có thể tích hợp việc chuyển đổi này vào bất kỳ ứng dụng .NET nào một cách tự tin.

## Câu trả lời nhanh
- **Thư viện nào xử lý việc chuyển đổi?** Aspose.CAD cho .NET.
- **Định dạng nguồn được hỗ trợ?** Tệp IFC (Industry Foundation Classes).
- **Định dạng ảnh mục tiêu?** PNG, với khả năng kiểm soát đầy đủ kích thước và độ phân giải.
- **Phiên bản .NET tối thiểu?** .NET Framework 4.5+ hoặc .NET Core 3.1+.
- **Yêu cầu giấy phép?** Giấy phép Aspose.CAD hợp lệ cho việc sử dụng trong môi trường sản xuất.

## “how to export cad to png” là gì?

Cụm từ này đề cập đến quá trình chuyển đổi các định dạng tệp dựa trên CAD, chẳng hạn như IFC, thành các hình ảnh Portable Network Graphics (PNG) raster. Việc chuyển đổi này cho phép dễ dàng xem, chia sẻ và nhúng các hình ảnh CAD trong các trang web, tài liệu hoặc báo cáo, cung cấp một định dạng nhẹ, được hỗ trợ rộng rãi và giữ nguyên độ trung thực hình ảnh mà không cần các trình xem CAD chuyên dụng.

## Tại sao nên sử dụng Aspose.CAD cho việc chuyển đổi này?

Aspose.CAD hỗ trợ **hơn 50** định dạng CAD và BIM và có thể xử lý các mô hình IFC hàng trăm trang mà không cần tải toàn bộ tệp vào bộ nhớ. Nó cung cấp các chuyển đổi nhanh chóng, tiết kiệm bộ nhớ trên phần cứng máy chủ tiêu chuẩn, tự động xử lý các lớp, độ dày đường và ánh xạ màu trong khi cung cấp nhiều tùy chọn cấu hình cho chất lượng và kích thước đầu ra.

## Yêu cầu trước

### 1. Cài đặt Aspose.CAD
Đảm bảo rằng bạn đã cài đặt Aspose.CAD cho .NET. Bạn có thể tải xuống từ trang phát hành [here](https://releases.aspose.com/cad/net/).

### 2. Thư mục tài liệu
Tạo một thư mục được chỉ định cho tài liệu của bạn. Trong ví dụ được cung cấp, biến `MyDir` đại diện cho thư mục tài liệu.

## Nhập không gian tên
Khi các yêu cầu trước đã sẵn sàng, hãy nhập các không gian tên cần thiết để làm việc với Aspose.CAD trong dự án .NET của bạn.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.CAD.FileFormats.Ifc;
```

## Cách xuất CAD sang PNG?

`IfcImage` đại diện cho một hình ảnh CAD IFC có thể được raster hóa thành các định dạng raster như PNG. Tải tệp IFC của bạn bằng `new IfcImage("source.ifc")`, cấu hình raster hóa qua `RasterizationOptions`, đặt các cài đặt đặc thù cho PNG bằng `PngOptions`, và cuối cùng gọi `Save(outputPath, pngOptions)`. Quy trình đầu‑cuối này chuyển đổi mô hình CAD thành một PNG độ phân giải cao chỉ trong vài dòng mã, tự động xử lý các lớp, màu và độ dày đường.

## Bước 1: Tải tệp IFC
Lớp `IfcImage` tải một mô hình IFC và chuẩn bị nó cho việc raster hóa.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "example.ifc";
using (IfcImage cadImage = (IfcImage)Image.Load(sourceFilePath))
{
```

Trong bước này, chúng tôi khởi tạo đối tượng `IfcImage` của Aspose.CAD và tải tệp IFC vào đó.

## Bước 2: Đặt tùy chọn raster hóa
Lớp `RasterizationOptions` xác định cách dữ liệu vector được chuyển đổi thành hình ảnh raster, bao gồm chiều rộng trang, chiều cao và màu nền.

```csharp
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
   
    rasterizationOptions.PageWidth = 100;
    rasterizationOptions.PageHeight = 100;
```

Xác định các tùy chọn raster hóa để cấu hình chiều rộng và chiều cao trang cho đầu ra PNG.

## Bước 3: Đặt tùy chọn PNG
Lớp `PngOptions` chứa các cài đặt đặc thù cho đầu ra PNG, chẳng hạn mức nén và độ sâu màu.

```csharp
    PngOptions pngOptions = new PngOptions();
    pngOptions.VectorRasterizationOptions = rasterizationOptions;
```

Tạo các tùy chọn PNG và liên kết với các tùy chọn raster hóa đã định nghĩa trước đó.

## Bước 4: Chỉ định đường dẫn đầu ra
Đường dẫn đầu ra xác định nơi tệp PNG được tạo sẽ được lưu.

```csharp
    // Set output path as well
    string outPath = sourceFilePath + ".png";
    cadImage.Save(outPath, pngOptions);
}
```

Xác định đường dẫn đầu ra cho tệp PNG, đảm bảo nó có cùng tên với tệp nguồn và có phần mở rộng ".png". Cuối cùng, lưu hình ảnh đã chuyển đổi.

## Các vấn đề thường gặp và giải pháp
- **Thiếu phông chữ hoặc kiểu đường:** Đảm bảo IFC nguồn tham chiếu tất cả các tài nguyên cần thiết; Aspose.CAD sẽ nhúng các tài sản thiếu khi có thể.
- **Tệp lớn gây tăng đột biến bộ nhớ:** Sử dụng thuộc tính `MemoryLimit` trên `RasterizationOptions` để giới hạn việc sử dụng bộ nhớ.
- **Màu không chính xác:** Xác minh rằng các định nghĩa màu trong IFC nguồn tuân thủ schema IFC; Aspose.CAD tôn trọng việc ánh xạ màu tiêu chuẩn.

## Câu hỏi thường gặp

**Q: Có thể sử dụng Aspose.CAD cho .NET trên macOS hoặc Linux không?**  
A: Không, Aspose.CAD cho .NET được thiết kế đặc biệt cho môi trường Windows.

**Q: Có giấy phép tạm thời để thử nghiệm không?**  
A: Có, bạn có thể lấy giấy phép tạm thời từ [here](https://purchase.aspose.com/temporary-license/) để đánh giá.

**Q: Làm sao để nhận hỗ trợ cho Aspose.CAD?**  
A: Truy cập [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) để được cộng đồng hỗ trợ và thảo luận.

**Q: Tôi có thể tìm tài liệu chi tiết ở đâu?**  
A: Tham khảo [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) để có thông tin chi tiết và các ví dụ.

**Q: Nếu gặp vấn đề trong quá trình cài đặt thì sao?**  
A: Kiểm tra tài liệu hoặc tìm trợ giúp trên [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

---

**Cập nhật lần cuối:** 2026-07-18  
**Đã kiểm tra với:** Aspose.CAD 24.11 cho .NET  
**Tác giả:** Aspose

## Hướng dẫn liên quan

- [Chuyển đổi bản vẽ CAD sang hình ảnh raster trong Aspose.CAD cho .NET](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [Chuyển đổi STL sang PNG dễ dàng với Aspose.CAD cho .NET](/cad/net/stl-file-export/exporting-stl-files-to-png/)
- [Xuất bố cục CAD sang các định dạng hình ảnh raster trong Aspose.CAD cho .NET](/cad/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}