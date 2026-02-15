---
date: 2026-02-15
description: Tìm hiểu cách thiết lập kích thước trang PDF và chuyển đổi CAD sang PDF
  bằng Aspose.CAD cho Java, với việc tự động thu phóng bố cục và xuất ra TIFF.
linktitle: Set PDF Page Size – Convert CAD to PDF
second_title: Aspose.CAD Java API
title: Đặt kích thước trang PDF – Chuyển CAD sang PDF (Java)
url: /vi/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

24.12" keep.

"**Author:** Aspose" keep.

Then closing shortcodes unchanged.

Also final backtop button shortcode unchanged.

Now produce final content with all translations.

Be careful to preserve markdown formatting exactly.

Let's craft translation.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Đặt Kích Thước Canvas và Chế Độ

## Giới thiệu

Nếu bạn cần **đặt kích thước trang PDF** khi chuyển đổi bản vẽ CAD sang PDF, bạn đã đến đúng nơi. Trong hướng dẫn này, chúng tôi sẽ chỉ cho bạn cách sử dụng Aspose.CAD for Java để xác định kích thước canvas chính xác, bật tính năng tự động điều chỉnh tỷ lệ bố cục, và sau đó xuất kết quả ra cả PDF và TIFF. Dù bạn đang chuẩn bị sơ đồ kỹ thuật để in hoặc tạo ảnh thu nhỏ cho một bộ sưu tập web, việc kiểm soát kích thước trang và độ phân giải đầu ra là rất quan trọng.

## Câu trả lời nhanh
- **convert CAD to PDF** có nghĩa là gì?  
  Chuyển đổi một bản vẽ CAD (ví dụ: DXF, DWG) thành tài liệu PDF có thể xem trên bất kỳ nền tảng nào.  
- **Tôi có thể xuất ra TIFF không?**  
  Có — sử dụng `TiffOptions` để tạo ảnh raster độ phân giải cao.  
- **Tùy chọn nào kiểm soát kích thước canvas trong Java?**  
  `CadRasterizationOptions.setPageWidth/Height`.  
- **Tự động điều chỉnh tỷ lệ bố cục là gì?**  
  Một cờ (`setAutomaticLayoutsScaling(true)`) giữ nguyên tỉ lệ bố cục gốc khi kích thước canvas thay đổi.  
- **Tôi có cần giấy phép cho Aspose.CAD không?**  
  Cần một giấy phép tạm thời hoặc vĩnh viễn cho việc sử dụng trong môi trường sản xuất.

## Cách Đặt Kích Thước Trang PDF Khi Chuyển Đổi CAD sang PDF (Java)

Việc đặt kích thước trang PDF (hoặc kích thước canvas) cho phép bạn xác định kích thước cuối cùng của tài liệu, điều này đặc biệt hữu ích khi bạn phải **thay đổi kích thước PDF** để phù hợp với tiêu chuẩn in ấn hoặc yêu cầu giao diện người dùng. Dưới đây chúng tôi sẽ hướng dẫn từng bước, giải thích *tại sao* mỗi dòng mã lại cần thiết.

## **convert CAD to PDF** là gì?

Chuyển đổi CAD sang PDF có nghĩa là lấy các bản vẽ kỹ thuật dựa trên vector và render chúng thành các trang PDF, giữ nguyên các đường nét, lớp và hình học đồng thời làm cho tệp tin có thể truy cập được trên mọi thiết bị.

## Tại sao phải đặt kích thước canvas **java**?

Đặt kích thước canvas trong Java cho phép bạn xác định độ phân giải đầu ra và kích thước trang, đảm bảo PDF hoặc TIFF tạo ra đáp ứng yêu cầu in ấn hoặc hiển thị của bạn. Nó cũng cung cấp khả năng kiểm soát hành vi scaling, điều này rất quan trọng đối với các bản vẽ định dạng lớn.

## Yêu cầu trước

Trước khi bắt đầu hướng dẫn, hãy chắc chắn rằng bạn đã chuẩn bị các yêu cầu sau:

- Aspose.CAD for Java: Đảm bảo bạn đã cài đặt thư viện Aspose.CAD trong môi trường Java. Bạn có thể tải xuống nó [tại đây](https://releases.aspose.com/cad/java/).
- Thư mục tài liệu: Tạo một thư mục để lưu trữ các tệp CAD của bạn. Thư mục này sẽ được tham chiếu trong các bước của hướng dẫn.

Bây giờ, hãy bắt đầu với hướng dẫn từng bước.

## Nhập Namespace

Trong bước này, chúng ta sẽ nhập các namespace cần thiết để khởi động dự án Aspose.CAD của bạn.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Bước 1: Nhập Các Lớp Aspose.CAD

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

Trong đoạn mã này, chúng ta thiết lập đường dẫn tới thư mục tài nguyên và tải một tệp DXF bằng lớp `Image` của Aspose.CAD.

## Bước 2: Đặt Thuộc Tính **CadRasterizationOptions** (đặt kích thước canvas java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Ở đây, chúng ta tạo một thể hiện của `CadRasterizationOptions` và cấu hình các thuộc tính như chiều rộng trang, chiều cao trang và **tự động điều chỉnh tỷ lệ bố cục**. Đây là phần cốt lõi của **cấu hình chế độ canvas** cho quá trình chuyển đổi của bạn.

## Bước 3: Tạo PdfOptions và Đặt VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Bây giờ, chúng ta tạo một thể hiện `PdfOptions` và đặt thuộc tính `VectorRasterizationOptions` của nó thành `CadRasterizationOptions` đã cấu hình trước đó.

## Bước 4: Xuất ra PDF (convert cad to pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Cuối cùng, chúng ta lưu ảnh CAD thành tệp PDF bằng các tùy chọn đã chỉ định, hoàn thành quá trình **convert CAD to PDF**.

## Bước 5: Tạo TiffOptions và Đặt VectorRasterizationOptions (export cad to tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Trong bước này, chúng ta thiết lập một thể hiện `TiffOptions` và cấu hình thuộc tính `VectorRasterizationOptions` của nó.

## Bước 6: Xuất ra TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Cuối cùng, chúng ta lưu ảnh CAD thành tệp TIFF bằng các tùy chọn đã chỉ định, minh họa cách **export CAD to TIFF** sau khi đã cấu hình kích thước canvas.

## Các Vấn Đề Thường Gặp và Giải Pháp

| Vấn đề | Nguyên nhân | Cách khắc phục |
|-------|-------------|----------------|
| PDF đầu ra bị trắng | `setNoScaling(true)` vô hiệu hoá việc render cho một số bản vẽ | Xóa `setNoScaling(true)` hoặc đặt nó thành `false`. |
| Độ phân giải TIFF trông thấp | Chiều rộng/chiều cao trang quá nhỏ | Tăng giá trị `setPageWidth` / `setPageHeight`. |
| Bố cục bị biến dạng | Tự động điều chỉnh tỷ lệ bố cục bị tắt | Đảm bảo `setAutomaticLayoutsScaling(true)` được bật. |

## Tại sao phải điều chỉnh kích thước Canvas và DPI?

Thay đổi kích thước canvas ảnh hưởng trực tiếp đến độ phân giải raster của đầu ra. Nếu bạn cần **tăng độ phân giải TIFF**, chỉ cần tăng các giá trị `setPageWidth` / `setPageHeight` hoặc gọi `rasterizationOptions.setResolution(300)` trước khi tạo `TiffOptions`. Điều này sẽ cho bạn những ảnh raster chất lượng cao, phù hợp cho việc in ấn hoặc kiểm tra chi tiết.

## Câu Hỏi Thường Gặp

### Q1: Tôi có thể sử dụng Aspose.CAD for Java với các framework Java khác không?

**A1:** Có, Aspose.CAD được thiết kế để tích hợp liền mạch với nhiều framework Java khác nhau.

### Q2: Có giấy phép tạm thời cho Aspose.CAD không?

**A2:** Có. Bạn có thể lấy giấy phép tạm thời [tại đây](https://purchase.aspose.com/temporary-license/).

### Q3: Tôi có thể nhận hỗ trợ cộng đồng cho Aspose.CAD ở đâu?

**A3:** Truy cập [diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để nhận hỗ trợ và thảo luận từ cộng đồng.

### Q4: Tôi có thể dùng thử Aspose.CAD miễn phí không?

**A4:** Chắc chắn! Nhận bản dùng thử miễn phí [tại đây](https://releases.aspose.com/).

### Q5: Làm thế nào để mua Aspose.CAD for Java?

**A5:** Mua sản phẩm [tại đây](https://purchase.aspose.com/buy).

**Câu hỏi bổ sung**

**Hỏi:** Kích thước canvas có ảnh hưởng đến chất lượng vector trong PDF không?  
**Đáp:** Không. Kích thước canvas chỉ kiểm soát kích thước trang; dữ liệu vector vẫn độc lập với độ phân giải, đảm bảo hiển thị sắc nét ở bất kỳ mức phóng nào.

**Hỏi:** Tôi có thể đặt DPI khác cho đầu ra TIFF không?  
**Đáp:** Có. Điều chỉnh `rasterizationOptions.setResolution(dpiValue)` trước khi tạo `TiffOptions`.

**Hỏi:** Làm sao **thay đổi kích thước PDF** cho một PDF đã tồn tại mà không cần render lại CAD?  
**Đáp:** Sử dụng Aspose.PDF để tải PDF đã tạo và gọi `pdf.getPages().setPageSize(PageSize.A4)` hoặc kích thước tùy chỉnh khác.

**Hỏi:** Cách tốt nhất để **convert dxf to pdf** mà vẫn giữ nguyên các lớp là gì?  
**Đáp:** Giữ `setAutomaticLayoutsScaling(true)` và tránh `setNoScaling(true)`; cách này duy trì độ hiển thị của các lớp và độ chính xác bố cục.

## Kết luận

Chúc mừng! Bạn đã thành công **convert CAD to PDF** và **export CAD to TIFF** đồng thời **đặt kích thước canvas java**, kích hoạt **tự động điều chỉnh tỷ lệ bố cục**, và học cách **cấu hình chế độ canvas** cho các đầu ra chất lượng cao. Hướng dẫn này cung cấp nền tảng vững chắc cho các dự án chuyển đổi CAD của bạn. Khám phá thêm tính năng và khả năng trong [tài liệu Aspose.CAD](https://reference.aspose.com/cad/java/).

**Last Updated:** 2026-02-15  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}