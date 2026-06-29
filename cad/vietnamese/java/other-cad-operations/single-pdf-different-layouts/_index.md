---
date: 2026-06-29
description: Tìm hiểu cách tạo PDF từ DWG và tùy chỉnh bố cục PDF bằng Aspose.CAD
  for Java. Tích hợp dễ dàng cho các nhà phát triển Java.
keywords:
- create pdf from dwg
- convert cad to pdf
- pdf different page sizes
- export dwg to pdf
- customize pdf layout
linktitle: PDF đơn với các bố cục khác nhau
schemas:
- author: Aspose
  dateModified: '2026-06-29'
  description: Learn how to create PDF from DWG and customize PDF layout using Aspose.CAD
    for Java. Easy integration for Java developers.
  headline: Create PDF from DWG with Aspose.CAD for Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD for Java integrates seamlessly with libraries such as
      Apache POI, Jackson, or Spring Boot.
    question: Can I use Aspose.CAD for Java with other Java libraries?
  - answer: Absolutely! You can access a free trial version [here](https://releases.aspose.com/).
    question: Is there a trial version available?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and discussions.
    question: Where can I find additional support?
  - answer: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license?
  - answer: Purchase the full version of Aspose.CAD for Java [here](https://purchase.aspose.com/buy).
    question: Where can I purchase the full version?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Tạo PDF từ DWG với Aspose.CAD for Java
url: /vi/java/other-cad-operations/single-pdf-different-layouts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tạo PDF từ DWG với Aspose.CAD cho Java

## Giới thiệu

Trong hướng dẫn này, bạn sẽ **tạo PDF từ DWG** và áp dụng một số bố cục kích thước trang khác nhau bằng Aspose.CAD cho Java. Cho dù bạn cần tạo bản vẽ xây dựng, sơ đồ kỹ thuật, hay PDF sẵn sàng cho marketing, các bước dưới đây sẽ chỉ cho bạn cách chuyển đổi bản vẽ CAD sang PDF, tùy chỉnh kích thước của mỗi bố cục, và tạo một tài liệu đa trang duy nhất — tất cả mà không rời khỏi môi trường Java.

## Câu trả lời nhanh
- **Nội dung hướng dẫn?** Chuyển đổi bản vẽ DWG thành một PDF duy nhất với nhiều kích thước trang.  
- **Thư viện cần thiết?** Aspose.CAD cho Java (phiên bản mới nhất).  
- **Có cần giấy phép không?** Bản dùng thử miễn phí đủ cho phát triển; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Có thể xuất sang định dạng khác không?** Có – API cũng hỗ trợ xuất sang PNG, JPEG và SVG.  
- **Java 8 có đủ không?** Thư viện hoạt động với Java 8 và các runtime mới hơn.

## “Tạo PDF từ DWG” là gì?

**Tạo PDF từ DWG** có nghĩa là chuyển đổi tệp AutoCAD DWG gốc thành tài liệu PDF trong khi giữ nguyên độ chính xác vector, các lớp và độ dày đường, đồng thời cho phép tùy chỉnh bố cục. Aspose.CAD thực hiện quá trình chuyển đổi này hoàn toàn trong bộ nhớ, vì vậy không cần phần mềm CAD bên ngoài, và PDF kết quả có thể được chỉnh sửa hoặc in trực tiếp.

## Tại sao tùy chỉnh bố cục PDF từ DWG?

Aspose.CAD hỗ trợ **hơn 30 định dạng CAD** và có thể tạo PDF lên tới **500 MB** mà không cần tải toàn bộ tệp vào bộ nhớ. Bằng cách định nghĩa kích thước trang riêng cho mỗi bố cục, bạn có thể tạo ra các tờ in phù hợp với tiêu chuẩn ISO, ANSI hoặc kích thước tùy chỉnh – một lợi ích định lượng giúp tiết kiệm thời gian và loại bỏ việc xử lý thủ công sau khi chuyển đổi.

## Yêu cầu trước

Trước khi bắt đầu, hãy đảm bảo bạn đã chuẩn bị các yêu cầu sau:
- Môi trường Java: Đảm bảo bạn đã cài đặt Java trên máy.  
- Thư viện Aspose.CAD: Tải xuống và cài đặt thư viện Aspose.CAD cho Java từ [liên kết tải xuống](https://releases.aspose.com/cad/java/).  
- Thư mục tài liệu: Tạo một thư mục cho các bản vẽ DWG của bạn.

## Nhập gói

Class `CadImage` là đối tượng cốt lõi của Aspose.CAD đại diện cho bản vẽ CAD trong bộ nhớ. Nhập các namespace cần thiết trước khi bắt đầu:

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## Bước 1: Tải bản vẽ CAD

`CadImage` tải tệp DWG và cung cấp quyền truy cập vào dữ liệu vector. Bắt đầu bằng cách tải bản vẽ CAD của bạn vào một đối tượng `CadImage`:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## Bước 2: Cấu hình tùy chọn raster hoá

`RasterizationOptions` xác định cách các vector CAD được raster hoá trước khi đưa vào PDF. Thiết lập các tùy chọn raster hoá cho hình ảnh CAD:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## Bước 3: Tùy chỉnh kích thước trang bố cục

`PdfOptions` cho phép bạn chỉ định kích thước trang riêng cho mỗi bố cục trong DWG. Định nghĩa kích thước tùy chỉnh cho một số bố cục trong bản vẽ CAD:

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## Bước 4: Đặt tùy chọn PDF

`PdfOptions` là container kết hợp các cài đặt raster hoá và định nghĩa bố cục. Cấu hình các tùy chọn PDF, bao gồm các cài đặt raster hoá:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Bước 5: Lưu dưới dạng PDF

`PdfSaveOptions` hoàn thiện quá trình chuyển đổi và ghi tệp đầu ra. Lưu hình ảnh CAD đã xử lý dưới dạng PDF:

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

Chúc mừng! Bạn đã thành công **tạo PDF từ DWG** với các kích thước trang khác nhau bằng Aspose.CAD cho Java.

## Các vấn đề thường gặp và giải pháp

- **Trang trắng trong PDF đầu ra** – Đảm bảo các giá trị `PageSize` khớp với kích thước bố cục thực tế trong tệp DWG.  
- **Lỗi hết bộ nhớ khi xử lý bản vẽ lớn** – Sử dụng `CadImage.load(..., LoadOptions)` với `LoadOptions.setLoadMode(LoadMode.Memory)` để stream tệp thay vì tải toàn bộ.  
- **Tỷ lệ không đúng** – Điều chỉnh `RasterizationOptions.setPageWidth` và `setPageHeight` để phù hợp với DPI mong muốn.

## Câu hỏi thường gặp

**H: Tôi có thể sử dụng Aspose.CAD cho Java cùng với các thư viện Java khác không?**  
Đ: Có, Aspose.CAD cho Java tích hợp liền mạch với các thư viện như Apache POI, Jackson, hoặc Spring Boot.

**H: Có phiên bản dùng thử không?**  
Đ: Chắc chắn! Bạn có thể truy cập phiên bản dùng thử miễn phí [tại đây](https://releases.aspose.com/).

**H: Tôi có thể tìm hỗ trợ bổ sung ở đâu?**  
Đ: Truy cập [diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để nhận hỗ trợ cộng đồng và thảo luận.

**H: Làm sao để lấy giấy phép tạm thời?**  
Đ: Bạn có thể lấy giấy phép tạm thời [tại đây](https://purchase.aspose.com/temporary-license/).

**H: Tôi có thể mua phiên bản đầy đủ ở đâu?**  
Đ: Mua phiên bản đầy đủ của Aspose.CAD cho Java [tại đây](https://purchase.aspose.com/buy).

---

**Cập nhật lần cuối:** 2026-06-29  
**Được kiểm tra với:** Aspose.CAD for Java 24.10  
**Tác giả:** Aspose

## Hướng dẫn liên quan

- [Xuất DWG sang PDF hoặc Raster bằng Aspose.CAD cho Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Xuất bố cục CAD sang PDF với Aspose.CAD cho Java](/cad/java/cad-export-options/export-cad-layouts-to-pdf/)
- [Xuất bố cục DWG cụ thể sang PDF bằng Aspose.CAD cho Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}