---
date: 2026-10-14
description: Tìm hiểu cách thư viện Java CAD Aspose.CAD cho Java có thể xuất DWG sang
  PDF hoặc hình ảnh raster một cách nhanh chóng và chính xác.
keywords:
- export dwg pdf
- high quality pdf
- dwg to pdf tutorial
- aspose cad java
- java cad library
lastmod: 2026-10-14
linktitle: Xuất DWG PDF và hình ảnh raster
og_description: Xuất DWG PDF nhanh chóng với Aspose.CAD cho Java. Tìm hiểu chuyển
  đổi PDF chất lượng cao, các tùy chọn raster và giấy phép trong hướng dẫn từng bước
  này.
og_image_alt: Tutorial showing Java code to convert DWG drawings to PDF and raster
  formats with Aspose.CAD
og_title: Xuất DWG PDF và hình ảnh raster bằng thư viện Java CAD Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-14'
  description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  headline: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  type: TechArticle
- description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  name: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  steps:
  - name: Load the DWG file
    text: First, load your DWG drawing using the `Image` class. This creates an in‑memory
      representation that Aspose.CAD can work with.
  - name: Determine unit type
    text: Understanding whether the drawing uses metric or imperial units is essential
      for correct scaling. The helper method `IsMetric` (implementation omitted for
      brevity) returns a boolean flag.
  - name: Set rasterization options
    text: The `CadRasterizationOptions` class defines rasterization parameters such
      as DPI, page size, and unit conversion. Based on the unit system, configure
      page size, scaling, and the target unit type. These options drive how the DWG
      is rasterized before being wrapped into a PDF.
  - name: Configure PDF options (pdf options cad)
    text: The `PdfOptions` class specifies PDF‑specific settings, including compression
      and metadata. Create a `PdfOptions` instance and attach the rasterization settings.
      This tells Aspose.CAD how to embed the rasterized content into the final PDF.
  - name: Save as PDF
    text: The `save` method writes the image to the given file path using the supplied
      options. Finally, export the drawing to a PDF file. The `save` method takes
      the output path and the configured `PdfOptions`. When the code finishes, you’ll
      find **Saved.pdf** in your `DWGDrawings` folder, ready for distribu
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java seamlessly integrates with popular Java frameworks
      such as Spring, Jakarta EE, and Android.
    question: Can I use Aspose.CAD for Java with other Java frameworks?
  - answer: Yes, you can obtain a temporary license **[obtain a temporary license](https://purchase.aspose.com/temporary-license/)**.
    question: Is a temporary license available for Aspose.CAD for Java?
  - answer: Visit the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** for
      assistance from the community and Aspose engineers.
    question: Where can I find support for Aspose.CAD for Java?
  - answer: You can purchase a license **[purchase a license](https://purchase.aspose.com/buy)**.
    question: How can I purchase a license for Aspose.CAD for Java?
  - answer: Aspose.CAD for Java supports both metric and imperial units, automatically
      detecting the drawing’s unit system.
    question: What units does Aspose.CAD for Java support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- export dwg
- aspose.cad
- java cad conversion
title: Xuất DWG PDF và hình ảnh raster bằng thư viện Java CAD Aspose.CAD
url: /vi/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xuất DWG PDF và hình ảnh raster bằng thư viện Java CAD Aspose.CAD

## Giới thiệu

Việc xuất DWG sang PDF là một yêu cầu thường gặp đối với kỹ sư, kiến trúc sư và bất kỳ ai cần chia sẻ bản vẽ CAD mà không tiết lộ định dạng tệp gốc. Với **Aspose.CAD for Java**, bạn có thể **export dwg pdf** — hoặc hình ảnh raster — chỉ với vài dòng mã Java, giữ nguyên độ chính xác vector và bố cục. Hướng dẫn này sẽ chỉ cho bạn cách tải tệp DWG, cấu hình raster hóa và lưu kết quả dưới dạng PDF hoặc hình ảnh chất lượng cao. Bạn cũng sẽ thấy tại sao Aspose.CAD là thư viện Java CAD được ưa chuộng cho việc chuyển đổi đáng tin cậy, đa nền tảng.  

Để có hướng dẫn tập trung chỉ về chuyển đổi PDF, xem [Export DWG to PDF tutorial](/java/cad-drawing-conversion/export-dwg-to-pdf/).

## Câu trả lời nhanh
- **Hướng dẫn này đề cập đến gì?** Exporting DWG files to PDF or raster images using Aspose.CAD for Java.  
- **Tôi có cần giấy phép không?** A free temporary license is available for evaluation; a full license is required for production.  
- **Phiên bản Java nào được hỗ trợ?** Any Java 8+ runtime works with the latest Aspose.CAD Java API.  
- **Tôi có thể chuyển đổi DWG sang các định dạng hình ảnh khác không?** Yes – the same rasterization options let you output PNG, JPEG, BMP, etc.  
- **Quá trình chuyển đổi mất bao lâu?** Typically under a second for standard drawings; larger files may take a few seconds.

## Tại sao thư viện Java CAD là lựa chọn tốt nhất cho việc chuyển đổi DWG?

Aspose.CAD for Java là lựa chọn tốt nhất vì nó cung cấp một triển khai thuần Java không cần DLL gốc, tự động phát hiện đơn vị mét hoặc inch, cung cấp đầu ra raster lên tới 1200 DPI, và tạo PDF giữ nguyên vector mà không cần phụ thuộc bên ngoài. Thư viện cũng cung cấp mô hình cấp phép linh hoạt cho phép bạn bắt đầu với giấy phép tạm thời và mở rộng lên quy mô doanh nghiệp.

## “export dwg to pdf” là gì?

`Export dwg pdf` là quá trình chuyển đổi tệp bản vẽ DWG gốc thành tài liệu PDF trong khi giữ nguyên dữ liệu vector, lớp và tỷ lệ. Việc chuyển đổi này tạo ra một tệp độc lập với thiết bị, có thể xem trên bất kỳ nền tảng nào mà không cần AutoCAD. Vì PDF giữ thông tin vector, văn bản vẫn có thể tìm kiếm và đồ họa luôn sắc nét ở mọi mức phóng đại, làm cho nó lý tưởng cho tài liệu, đánh giá của khách hàng và lưu trữ lưu trữ.

## Tại sao sử dụng Aspose.CAD Java cho việc chuyển đổi này?

Bạn nên sử dụng Aspose.CAD Java vì thư viện này xử lý chuyển đổi đơn vị, raster hóa và nhúng PDF nội bộ, loại bỏ nhu cầu sử dụng công cụ bên thứ ba hoặc các pipeline dòng lệnh phức tạp. API của nó được thiết kế cho các nhà phát triển: một đối tượng `Image` duy nhất đại diện cho bản vẽ, và một vài đối tượng cấu hình cho phép bạn tinh chỉnh DPI, kích thước trang và nén. Kết quả là đầu ra nhất quán, có thể lặp lại trên các môi trường Windows, Linux và macOS.

## Yêu cầu trước

- Kiến thức cơ bản về lập trình Java.  
- Thư viện Aspose.CAD for Java đã được cài đặt. Nếu bạn chưa tải xuống, hãy tải **[download Aspose.CAD for Java](https://releases.aspose.com/cad/java/)**.  
- Một tệp DWG để thử nghiệm – mẫu **Bottom_plate.dwg** được sử dụng trong hướng dẫn này.  

## Nhập không gian tên

Trong dự án Java của bạn, nhập các lớp cần thiết để bắt đầu chuyển đổi:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Hướng dẫn từng bước

### Bước 1: Tải tệp DWG

Đầu tiên, tải bản vẽ DWG của bạn bằng lớp `Image`. Điều này tạo ra một đại diện trong bộ nhớ mà Aspose.CAD có thể làm việc.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Bước 2: Xác định loại đơn vị

Hiểu xem bản vẽ sử dụng đơn vị mét hay inch là cần thiết để tỷ lệ chính xác. Phương thức trợ giúp `IsMetric` (cài đặt được bỏ qua để ngắn gọn) trả về một cờ boolean.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Bước 3: Đặt tùy chọn raster hóa

Lớp `CadRasterizationOptions` định nghĩa các tham số raster hóa như DPI, kích thước trang và chuyển đổi đơn vị. Dựa trên hệ thống đơn vị, cấu hình kích thước trang, tỷ lệ và loại đơn vị mục tiêu. Những tùy chọn này quyết định cách DWG được raster hóa trước khi được đóng gói vào PDF.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### Bước 4: Cấu hình tùy chọn PDF (pdf options cad)

Lớp `PdfOptions` chỉ định các cài đặt đặc thù cho PDF, bao gồm nén và siêu dữ liệu. Tạo một thể hiện `PdfOptions` và gắn các cài đặt raster hóa. Điều này cho Aspose.CAD biết cách nhúng nội dung raster vào PDF cuối cùng.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Bước 5: Lưu dưới dạng PDF

Phương thức `save` ghi hình ảnh vào đường dẫn tệp được chỉ định bằng các tùy chọn đã cung cấp. Cuối cùng, xuất bản vẽ ra tệp PDF. Phương thức `save` nhận đường dẫn đầu ra và `PdfOptions` đã cấu hình.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Khi mã hoàn thành, bạn sẽ thấy **Saved.pdf** trong thư mục `DWGDrawings` của mình, sẵn sàng để phân phối hoặc lưu trữ.

## Cách chuyển đổi hình ảnh raster DWG bằng thư viện Java CAD?

Bạn có thể chuyển đổi DWG sang các định dạng raster bằng cách thay thế `PdfOptions` bằng một lớp tùy chọn raster như `PngOptions` hoặc `JpegOptions`. Tái sử dụng cùng một thể hiện `CadRasterizationOptions`, điều chỉnh định dạng đầu ra và gọi phương thức `save` với đối tượng tùy chọn mới. Cách tiếp cận này cho phép bạn tạo các tệp PNG, JPEG, BMP hoặc TIFF chỉ với một dòng thay đổi, giữ cho quy trình làm việc nhất quán.

## Cách tạo PDF DWG bằng tùy chọn PDF CAD?

Ví dụ trên đã **generates pdf dwg** đầu ra. Để tinh chỉnh kích thước PDF, bật nén bằng cách gọi `pdfOptions.setCompress(true)`. Bạn cũng có thể nhúng siêu dữ liệu tùy chỉnh, đặt phiên bản PDF, hoặc thêm bảo vệ bằng mật khẩu thông qua các thuộc tính `PdfOptions` bổ sung. Những điều chỉnh này cho phép bạn kiểm soát hoàn toàn PDF cuối cùng mà không rời khỏi mã Java.

## Các vấn đề thường gặp & mẹo

- **Kích thước trang không đúng** – Double‑check the unit conversion logic; mismatched coefficients can produce oversized pages.  
- **Thiếu phông chữ hoặc độ dày đường** – Ensure the DWG references any external resources before conversion.  
- **Hiệu suất trên bản vẽ lớn** – Increase the `DPI` setting in `CadRasterizationOptions` only when higher quality is required; lower DPI speeds up processing.  
- **Vấn đề giấy phép** – For evaluation you can use a **temporary license Aspose**; a full license is required for production deployments.

## Câu hỏi thường gặp

**Q: Tôi có thể sử dụng Aspose.CAD for Java với các framework Java khác không?**  
A: Có, Aspose.CAD for Java tích hợp liền mạch với các framework Java phổ biến như Spring, Jakarta EE và Android.

**Q: Có giấy phép tạm thời cho Aspose.CAD for Java không?**  
A: Có, bạn có thể nhận giấy phép tạm thời **[obtain a temporary license](https://purchase.aspose.com/temporary-license/)**.

**Q: Tôi có thể tìm hỗ trợ cho Aspose.CAD for Java ở đâu?**  
A: Truy cập **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** để nhận trợ giúp từ cộng đồng và các kỹ sư Aspose.

**Q: Làm thế nào tôi có thể mua giấy phép cho Aspose.CAD for Java?**  
A: Bạn có thể mua giấy phép **[purchase a license](https://purchase.aspose.com/buy)**.

**Q: Aspose.CAD for Java hỗ trợ những đơn vị nào?**  
A: Aspose.CAD for Java hỗ trợ cả đơn vị mét và inch, tự động phát hiện hệ thống đơn vị của bản vẽ.

**Q: Tôi có thể chuyển đổi DWG sang các định dạng hình ảnh khác (ví dụ: PNG, JPEG) bằng cùng API không?**  
A: Chắc chắn. Thay thế `PdfOptions` bằng các tùy chọn hình ảnh raster phù hợp (ví dụ: `PngOptions`) và tái sử dụng cùng `CadRasterizationOptions`.

## Kết luận

Hướng dẫn này đã trình bày cách **export dwg pdf** và hình ảnh raster bằng **java cad library** Aspose.CAD for Java. Bằng cách làm theo hướng dẫn từng bước, bạn có thể tích hợp chuyển đổi CAD đáng tin cậy vào bất kỳ ứng dụng Java nào, dù bạn cần PDF cho tài liệu hoặc hình ảnh raster cho hiển thị web. Tính thuần Java của thư viện, đầu ra chất lượng cao và mô hình cấp phép linh hoạt khiến nó trở thành lựa chọn vững chắc cho cả tiện ích nhỏ và quy trình doanh nghiệp quy mô lớn.

---

**Cập nhật lần cuối:** 2026-10-14  
**Kiểm tra với:** Aspose.CAD for Java 24.10  
**Tác giả:** Aspose

## Hướng dẫn liên quan

- [Xuất DWG sang PDF: Bố cục cụ thể sử dụng Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Xuất DWG sang PDF trong Java – Đặt kích thước trang PDF với Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Xuất DWG sang PDF với các đường ẩn – Aspose.CAD for Java](/cad/java/cad-text-and-formatting/support-hidden-lines-in-dwg/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}