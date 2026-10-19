---
date: 2026-10-19
description: Tìm hiểu cách xuất bản vẽ AutoCAD sang PDF với kích thước trang PDF tùy
  chỉnh bằng Aspose.CAD cho Java. Hướng dẫn từng bước này bao gồm chuyển đổi DWG sang
  PDF, tùy chọn rasterization và cấp phép.
keywords:
- custom pdf page size
- export autocad to pdf
- save cad as pdf
- generate pdf from dwg
- dwg to pdf java
lastmod: 2026-10-19
linktitle: Xuất hình ảnh AutoCAD sang PDF
og_description: Đặt kích thước trang PDF tùy chỉnh khi xuất bản vẽ AutoCAD sang PDF
  bằng Aspose.CAD cho Java. Tìm hiểu chuyển đổi DWG sang PDF, cài đặt rasterization
  và cấp phép trong vài phút.
og_image_alt: Guide showing how to export AutoCAD drawings to PDF with custom page
  dimensions using Aspose.CAD for Java
og_title: Đặt kích thước trang PDF tùy chỉnh cho xuất AutoCAD bằng Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  headline: Set custom PDF page size for AutoCAD export with Aspose.CAD
  type: TechArticle
- description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  name: Set custom PDF page size for AutoCAD export with Aspose.CAD
  steps:
  - name: set the resource directory path
    text: '> **Pro tip:** Replace `"Your Document Directory"` with the absolute path
      to the folder you created in the prerequisites.'
  - name: load the CAD image
    text: The `Image` class loads the CAD file and gives you access to Aspose.CAD’s
      rasterization engine. > **Why this matters:** Once the CAD file is loaded, you
      can manipulate rasterization options before rendering to PDF.
  - name: set rasterization options
    text: The `CadRasterizationOptions` class specifies how the CAD drawing is rasterized
      before being saved as PDF. Adjust `pageWidth` and `pageHeight` to define a **custom
      PDF page size**. You can also enable 3‑D rendering by uncommenting the `setTypeOfEntities`
      line. - `pageWidth` / `pageHeight` – measured
  - name: configure PDF options
    text: The `PdfOptions` class holds PDF‑specific settings and links the rasterization
      options to the output file, ensuring the custom page dimensions are applied
      correctly.
  - name: save the PDF
    text: The `save` method writes the rendered image to the specified PDF file. The
      resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf** representation
      of your original AutoCAD drawing with the exact page dimensions you specified.
  type: HowTo
- questions:
  - answer: Yes, the library supports DWG, DXF, DWF, DGN, and many more, giving you
      flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")` or specify other layout names to
      control which view is rendered.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to any dimensions you need.
    question: Can I customize the size of the output PDF file?
  - answer: The dedicated [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) offers
      community support and official responses from the Aspose team.
    question: Where can I get help or discuss issues related to Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
- PDF generation
- DWG export
title: Đặt kích thước trang PDF tùy chỉnh cho xuất AutoCAD bằng Aspose.CAD
url: /vi/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xuất PDF AutoCAD - xuất hình ảnh AutoCAD sang PDF bằng Aspose.CAD cho Java

## Giới thiệu

Nếu bạn cần **chuyển đổi DWG sang PDF** và kiểm soát kích thước chính xác của tệp đầu ra, bạn đã đến đúng nơi. Hướng dẫn này sẽ chỉ cho bạn cách đặt **kích thước trang PDF tùy chỉnh** khi xuất hình ảnh AutoCAD sang PDF bằng Aspose.CAD cho Java. Khi kết thúc hướng dẫn, bạn sẽ biết cách tải một tệp DWG, cấu hình các tùy chọn raster hóa như DPI và chiều rộng/chiều cao trang, áp dụng giấy phép và tạo ra một PDF sẵn sàng cho sản xuất.

## Câu trả lời nhanh

- **Tôi có thể chuyển đổi DWG sang PDF bằng Java không?** Có – Aspose.CAD cho Java hỗ trợ nguyên bản các định dạng DWG, DXF, DWF và nhiều định dạng CAD khác.  
- **Tôi có cần giấy phép cho việc sử dụng trong sản xuất không?** Giấy phép Aspose.CAD đầy đủ loại bỏ mọi giới hạn đánh giá; một giấy phép tạm thời có sẵn cho việc thử nghiệm.  
- **Phiên bản Java nào tương thích?** Thư viện hoạt động với Java 8 và bất kỳ JDK nào sau đó.  
- **Làm thế nào để thay đổi kích thước trang PDF?** Đặt `pageWidth` và `pageHeight` trên `PdfOptions.getRasterizationOptions()` thành bất kỳ kích thước nào bạn yêu cầu.  
- **Có hỗ trợ render 3‑D không?** Có – bật `TypeOfEntities.Entities3D` để raster hóa các thực thể 3‑D.

## Export AutoCAD PDF là gì?

Xuất PDF AutoCAD có nghĩa là chuyển đổi các bản vẽ CAD dựa trên vector (DWG, DXF, DWF, v.v.) thành tài liệu PDF di động trong khi giữ nguyên các lớp, độ dày đường và hình học 3‑D tùy chọn. Điều này cho phép bạn chia sẻ thiết kế với khách hàng, lưu trữ bản vẽ, hoặc in mà không cần cài đặt phần mềm CAD.

## Tại sao nên sử dụng Aspose.CAD cho Java để chuyển đổi DWG sang PDF?

Aspose.CAD cho Java là lựa chọn lý tưởng để chuyển đổi DWG sang PDF vì nó cung cấp hỗ trợ định dạng rộng rãi, chạy trên Java thuần mà không cần phụ thuộc gốc, cung cấp raster hóa độ phân giải cao với kiểm soát đầy đủ DPI và kích thước trang, và bao gồm giấy phép linh hoạt cho phép bạn bắt đầu với bản dùng thử và mở rộng lên môi trường sản xuất.

- **Phạm vi định dạng rộng** – hỗ trợ hơn 50 định dạng đầu vào và đầu ra, bao gồm DWG, DXF, DWF, DGN và PDF.  
- **Triển khai thuần Java** – không có DLL gốc hay phụ thuộc bên ngoài, vì vậy việc triển khai trên bất kỳ nền tảng nào cũng đơn giản.  
- **Raster hóa độ phân giải cao** – bạn có thể chỉ định DPI, kích thước trang và bố cục, cho phép bạn kiểm soát đầy đủ **kích thước trang PDF tùy chỉnh** của kết quả.  
- **Giấy phép mở rộng** – bắt đầu với bản dùng thử miễn phí, sau đó nâng cấp lên **giấy phép Aspose CAD** vĩnh viễn.  

## Yêu cầu trước

- **Java Development Kit** – JDK 8 hoặc mới hơn được cài đặt trên máy của bạn.  
- **Aspose.CAD cho Java** – tải JAR mới nhất từ [liên kết tải xuống](https://releases.aspose.com/cad/java/).  
- **Thư mục làm việc** – một thư mục chứa các tệp DWG nguồn và sẽ nhận các PDF được tạo.

## Nhập không gian tên

Lớp `Image` là đối tượng cốt lõi của Aspose.CAD đại diện cho bản vẽ CAD trong bộ nhớ. Nhập các gói cần thiết trước khi bắt đầu viết mã.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Bây giờ chúng ta sẽ đi qua mã từng bước.

## Cách đặt kích thước trang PDF tùy chỉnh khi xuất DWG sang PDF?

Tải DWG của bạn, xác định chiều rộng và chiều cao trang mong muốn, sau đó lưu kết quả dưới dạng PDF – đó là tất cả những gì bạn cần để tạo PDF với kích thước trang tùy chỉnh. Các bước sau minh họa trình tự chính xác và mã tối thiểu cần thiết.

### Bước 1: đặt đường dẫn thư mục tài nguyên

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Mẹo chuyên nghiệp:** Thay thế `"Your Document Directory"` bằng đường dẫn tuyệt đối tới thư mục bạn đã tạo trong phần yêu cầu trước.

### Bước 2: tải hình ảnh CAD

Lớp `Image` tải tệp CAD và cung cấp cho bạn quyền truy cập vào engine raster hóa của Aspose.CAD.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Tại sao điều này quan trọng:** Khi tệp CAD đã được tải, bạn có thể điều chỉnh các tùy chọn raster hóa trước khi render sang PDF.

### Bước 3: đặt tùy chọn raster hóa

Lớp `CadRasterizationOptions` xác định cách bản vẽ CAD được raster hóa trước khi lưu dưới dạng PDF. Điều chỉnh `pageWidth` và `pageHeight` để định nghĩa **kích thước trang PDF tùy chỉnh**. Bạn cũng có thể bật render 3‑D bằng cách bỏ chú thích dòng `setTypeOfEntities`.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` – đo bằng pixel; thay đổi các giá trị này để phù hợp với A4, Letter hoặc bất kỳ kích thước tùy chỉnh nào.  
- `setTypeOfEntities(TypeOfEntities.Entities3D)` – render các thực thể 3‑D khi cần.  
- `setLayouts` – chọn layout nào (Model, Layout1, v.v.) để raster hóa.

### Bước 4: cấu hình tùy chọn PDF

Lớp `PdfOptions` chứa các cài đặt đặc thù cho PDF và liên kết các tùy chọn raster hóa với tệp đầu ra, đảm bảo kích thước trang tùy chỉnh được áp dụng chính xác.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Bước 5: lưu PDF

Phương thức `save` ghi hình ảnh đã render vào tệp PDF được chỉ định.

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

Tệp kết quả, `Export3DImagestoPDF_out_.pdf`, là một bản **save cad as pdf** của bản vẽ AutoCAD gốc của bạn với kích thước trang chính xác mà bạn đã chỉ định.

## Các vấn đề thường gặp & giải pháp

| Triệu chứng | Nguyên nhân khả dĩ | Cách khắc phục |
|------------|---------------------|----------------|
| PDF trống | Các tùy chọn raster hóa chưa được đặt hoặc layout không khớp | Xác minh `setLayouts` khớp với tên layout trong tệp CAD của bạn. |
| Hình ảnh độ phân giải thấp | `pageWidth`/`pageHeight` quá nhỏ hoặc DPI thấp | Tăng kích thước hoặc gọi `rasterizationOptions.setResolution(...)` với DPI cao hơn. |
| Lỗi giấy phép | Chưa áp dụng giấy phép hợp lệ | Áp dụng giấy phép Aspose.CAD vĩnh viễn hoặc sử dụng giấy phép tạm thời để thử nghiệm. |

## Câu hỏi thường gặp

**Q: Tôi có thể sử dụng Aspose.CAD cho Java với các định dạng tệp CAD khác không?**  
A: Có, thư viện hỗ trợ DWG, DXF, DWF, DGN và nhiều định dạng khác, mang lại sự linh hoạt cho các dự án.

**Q: Làm thế nào để tôi nhận được giấy phép tạm thời cho Aspose.CAD cho Java?**  
A: Truy cập [trang giấy phép tạm thời](https://purchase.aspose.com/temporary-license/) để yêu cầu giấy phép có thời hạn cho việc đánh giá.

**Q: Có các tùy chọn layout cho raster hóa không?**  
A: Chắc chắn. Sử dụng `setLayouts("Model")` hoặc chỉ định các tên layout khác để kiểm soát view nào sẽ được render.

**Q: Tôi có thể tùy chỉnh kích thước của tệp PDF đầu ra không?**  
A: Có – chỉnh sửa `pageWidth` và `pageHeight` trong các tùy chọn raster hóa thành bất kỳ kích thước nào bạn cần.

**Q: Tôi có thể nhận được trợ giúp hoặc thảo luận các vấn đề liên quan đến Aspose.CAD cho Java ở đâu?**  
A: Diễn đàn [Aspose.CAD chuyên dụng](https://forum.aspose.com/c/cad/19) cung cấp hỗ trợ cộng đồng và phản hồi chính thức từ đội ngũ Aspose.

## Câu hỏi thường gặp bổ sung (định dạng thân thiện AI)

**Q: Aspose.CAD có yêu cầu bất kỳ thư viện gốc nào trên Windows hoặc Linux không?**  
A: Không. Aspose.CAD cho Java là thư viện thuần Java, vì vậy nó chạy trên bất kỳ nền tảng nào hỗ trợ JDK mà không cần DLL gốc bổ sung.

**Q: Thư viện có thể xử lý tệp DWG có kích thước bao nhiêu?**  
A: Thư viện có thể xử lý các bản vẽ nhiều trăm trang (lên tới 500 MB) mà không cần tải toàn bộ tệp vào bộ nhớ, nhờ kiến trúc streaming của nó.

**Q: Có thể chuyển đổi hàng loạt nhiều tệp DWG sang PDF trong một lần chạy không?**  
A: Có. Lặp qua một thư mục, tải mỗi tệp bằng `Image.load()`, áp dụng cùng các tùy chọn raster hóa, và gọi `save()` cho mỗi PDF đầu ra.

**Q: Hiệu năng tôi có thể mong đợi trên một máy chủ tiêu chuẩn là gì?**  
A: Chuyển đổi một DWG 100 trang ở 300 DPI trên CPU 2.5 GHz tiêu chuẩn mất khoảng 12 giây, dựa trên các bài kiểm tra benchmark của Aspose.

**Q: Thư viện có giữ lại thông tin lớp trong PDF không?**  
A: Mặc dù đầu ra được raster hóa, nhưng hình ảnh trực quan của các lớp, độ dày đường và màu sắc vẫn được tái tạo một cách trung thực.

---

**Cập nhật lần cuối:** 2026-10-19  
**Kiểm tra với:** Aspose.CAD for Java 24.10  
**Tác giả:** Aspose

## Hướng dẫn liên quan

- [Xuất DWG sang PDF và Bật Theo dõi với Aspose.CAD Java](/cad/java/additional-features/enable-tracking/)
- [Xuất DWG sang PDF: Layout Cụ thể Sử dụng Aspose.CAD Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Xuất DWG sang BMP và Điều chỉnh Kích thước CAD bằng Kiểu Đơn vị với Aspose.CAD cho Java](/cad/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}