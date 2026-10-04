---
date: 2026-10-04
description: Tìm hiểu cách nhanh chóng chuyển đổi dwg sang png và xuất cad dưới dạng
  png hoặc các định dạng raster khác bằng Aspose.CAD for Java. Nhận kết quả chất lượng
  cao nhanh chóng.
keywords:
- convert dwg to png
- dwg to raster image
- convert cad to pdf
- export cad as png
- convert dwg to jpeg
lastmod: 2026-10-04
linktitle: Chuyển đổi bố cục CAD sang định dạng ảnh raster
og_description: Chuyển đổi DWG sang PNG nhanh chóng với Aspose.CAD for Java. Tìm hiểu
  từng bước cách xuất CAD dưới dạng PNG, JPEG, TIFF và hơn nữa.
og_image_alt: 'Developer guide: Convert DWG to PNG and other raster formats using
  Aspose.CAD for Java'
og_title: Chuyển đổi DWG sang PNG và các định dạng raster khác bằng Aspose.CAD for
  Java
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  headline: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  name: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  steps:
  - name: set up the resource directory
    text: Replace `"Your Document Directory"` with the absolute path where your CAD
      files reside. This directory will be used for both input and output files.
  - name: load the CAD file
    text: '`Image.load` parses the source file and creates an in‑memory representation
      that you can rasterize. You can load any supported format (DWG, DXF, DGN, etc.)
      – this is the **how to convert cad** part.'
  - name: configure rasterization options
    text: '`CadRasterizationOptions` defines how the vector data is turned into pixels.
      `setPageWidth` and `setPageHeight` control output resolution (larger values
      = higher DPI). `setLayouts` lets you **convert CAD to raster** for specific
      layouts; omit it to rasterize the whole drawing.'
  - name: set image options
    text: '`TiffOptions` (or `PngOptions` for PNG) tells Aspose which raster format
      to generate and lets you fine‑tune compression, color depth, and other format‑specific
      settings. Choose the options class that matches your desired output.'
  - name: save the resultant image
    text: Call `save` on the `Image` instance, passing the output file name and the
      options object. Change the file extension to `.png` (and use `PngOptions`) to
      **save CAD as PNG**. The same pattern works for JPEG, BMP, or PDF. > **Common
      pitfall:** Forgetting to match the file extension with the options cla
  type: HowTo
- questions:
  - answer: Yes, it supports over 30 CAD and raster formats, including DWG, DXF, DGN,
      and SVG.
    question: Is Aspose.CAD compatible with different CAD file formats?
  - answer: Absolutely. Adjust `setPageWidth`, `setPageHeight`, or `setResolution`
      in `CadRasterizationOptions` to achieve the desired DPI.
    question: Can I customize the resolution of the output raster image?
  - answer: Provide an array with all layout names to `setLayouts`, e.g., `new String[]{"Model","Layout1","Layout2"}`.
    question: How can I convert multiple CAD layouts in a single run?
  - answer: Yes—PNG, JPEG, BMP, PDF, and more are available via their respective `*Options`
      classes.
    question: Are there output formats besides TIFF supported?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and official assistance.
    question: Where can I get help or share my experience with Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg
- Aspose.CAD
- Java raster conversion
- CAD image processing
title: Chuyển đổi DWG sang PNG và các định dạng raster khác bằng Aspose.CAD for Java
url: /vi/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chuyển DWG sang PNG và các định dạng raster khác bằng Aspose.CAD cho Java

## Giới thiệu

`Aspose.CAD for Java` là một thư viện cho phép chuyển đổi CAD sang ảnh raster như PNG, JPEG và TIFF một cách lập trình. Chuyển DWG sang PNG (hoặc các định dạng raster khác) là nhu cầu phổ biến khi bạn cần chia sẻ bản vẽ CAD với đồng nghiệp không có trình xem CAD, nhúng thiết kế vào tài liệu, hoặc tạo thumbnail cho các bộ sưu tập web. Trong hướng dẫn này, bạn sẽ học cách chuyển dwg sang png nhanh chóng và đáng tin cậy, dù bạn đang làm việc với một tệp bản vẽ đầy đủ hoặc chỉ một layout cụ thể. Bạn cũng có thể cần **convert CAD to raster** cho bản xem trước web, công cụ báo cáo, hoặc ứng dụng di động.

## Câu trả lời nhanh
- **Thư viện nào xử lý DWG sang PNG?** Aspose.CAD for Java cung cấp động cơ chuyển đổi.  
- **Tôi có thể xuất các định dạng raster nào?** PNG, JPEG, TIFF, PDF, BMP và hơn 30 định dạng khác.  
- **Tôi có cần giấy phép để thử nghiệm không?** Bản dùng thử miễn phí hoạt động cho phát triển; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Tôi có thể chọn một layout cụ thể không?** Có – sử dụng `setLayouts` để chỉ định “Model”, “Layout1”, v.v.  
- **Có thể xuất đầu ra độ phân giải cao không?** Chắc chắn – điều chỉnh `setPageWidth` và `setPageHeight` (hoặc `setResolution`) để kiểm soát DPI.

## “convert dwg to png” là gì?

Chuyển dwg sang png có nghĩa là biến một bản vẽ vector DWG thành một hình ảnh PNG dựa trên pixel mà bất kỳ trình xem ảnh tiêu chuẩn nào cũng có thể hiển thị. Quá trình này raster hoá các thực thể vector, giữ nguyên độ dày đường, màu sắc và lớp trong khi chuyển chúng thành bitmap có độ phân giải cố định. Kết quả rất phù hợp để nhúng vào PDF, tài liệu Word, hoặc trang web nơi hỗ trợ vector hạn chế.

## Tại sao xuất CAD dưới dạng PNG (hoặc các định dạng raster khác)?

Xuất CAD dưới dạng PNG mang lại cho bạn khả năng tương thích toàn cầu, tải nhanh và dễ dàng nhúng trên mọi nền tảng chính. Ảnh raster tải ngay lập tức so với việc mở tệp DWG nặng, và việc nén không mất dữ liệu của PNG đảm bảo độ trung thực hình ảnh. Bằng cách kiểm soát độ phân giải, màu nền và layout, bạn đảm bảo mọi bên liên quan nhìn thấy cùng một giao diện, dù tệp được xem trên máy tính để bàn, thiết bị di động, hay trong trình duyệt.

## Các trường hợp sử dụng phổ biến

| Kịch bản | Lý do đầu ra raster hữu ích |
|----------|------------------------------|
| **Tài liệu dự án** | Nhúng PNG vào PDF hoặc tài liệu Word giúp tránh yêu cầu phần mềm CAD cho người xem. |
| **Cổng thông tin web** | Các thumbnail tạo từ tệp DWG tải ngay và cải thiện trải nghiệm người dùng. |
| **Ứng dụng di động** | Ảnh raster hiển thị đúng trên các thiết bị không có trình xem CAD. |
| **Báo cáo tự động** | Chuyển hàng loạt nhiều layout sang PNG/JPEG để đưa vào biểu đồ hoặc bảng điều khiển. |

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn bạn có:

1. **Môi trường phát triển Java** – JDK 8 hoặc mới hơn đã được cài đặt và cấu hình.  
2. **Aspose.CAD for Java** – Tải JAR mới nhất từ [tài liệu Aspose.CAD for Java](https://reference.aspose.com/cad/java/).  

## Nhập không gian tên

`com.aspose.cad.Image` là lớp cốt lõi đại diện cho bất kỳ tệp CAD nào trong bộ nhớ. `com.aspose.cad.imageoptions.*` cung cấp các đối tượng tùy chọn cho mỗi định dạng raster. Nhập các lớp bạn cần để tải bản vẽ, cấu hình raster hoá và lưu kết quả.

> **Mẹo chuyên nghiệp:** Nếu bạn dự định **export CAD as PNG** thay vì TIFF, hãy thay thế `TiffOptions` bằng `PngOptions` (tìm trong `com.aspose.cad.imageoptions.PngOptions`).

## Hướng dẫn từng bước

### Bước 1: thiết lập thư mục tài nguyên

Thay thế `"Your Document Directory"` bằng đường dẫn tuyệt đối nơi các tệp CAD của bạn nằm. Thư mục này sẽ được sử dụng cho cả tệp đầu vào và đầu ra.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

### Bước 2: tải tệp CAD

`Image.load` phân tích tệp nguồn và tạo một biểu diễn trong bộ nhớ mà bạn có thể raster hoá. Bạn có thể tải bất kỳ định dạng hỗ trợ nào (DWG, DXF, DGN, v.v.) – đây là phần **how to convert cad**.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

### Bước 3: cấu hình tùy chọn raster hoá

`CadRasterizationOptions` xác định cách dữ liệu vector được chuyển thành pixel. `setPageWidth` và `setPageHeight` kiểm soát độ phân giải đầu ra (giá trị lớn hơn = DPI cao hơn). `setLayouts` cho phép bạn **convert CAD to raster** cho các layout cụ thể; bỏ qua để raster hoá toàn bộ bản vẽ.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Bước 4: thiết lập tùy chọn hình ảnh

`TiffOptions` (hoặc `PngOptions` cho PNG) cho Aspose biết định dạng raster nào sẽ tạo và cho phép bạn tinh chỉnh nén, độ sâu màu và các cài đặt riêng cho định dạng. Chọn lớp tùy chọn phù hợp với đầu ra mong muốn.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

### Bước 5: lưu ảnh kết quả

Gọi `save` trên đối tượng `Image`, truyền tên tệp đầu ra và đối tượng tùy chọn. Thay đổi phần mở rộng tệp thành `.png` (và sử dụng `PngOptions`) để **save CAD as PNG**. Mẫu tương tự hoạt động cho JPEG, BMP hoặc PDF.

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

> **Cạm bẫy thường gặp:** Quên khớp phần mở rộng tệp với lớp tùy chọn sẽ gây ra `UnsupportedFormatException`. Luôn giữ chúng đồng nhất.

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Giải pháp |
|--------|-----------|
| **Ảnh đầu ra trắng** | Kiểm tra rằng tên layout trong `setLayouts` hoàn toàn khớp với trong tệp CAD nguồn. |
| **PNG độ phân giải thấp** | Tăng `setPageWidth` / `setPageHeight` hoặc đặt `setResolution` trong tùy chọn raster hoá. |
| **Phiên bản DWG không được hỗ trợ** | Đảm bảo bạn đang dùng phiên bản Aspose.CAD mới nhất; các bản cũ có thể không hỗ trợ các phiên bản DWG mới. |
| **Lỗi bộ nhớ khi xử lý tệp lớn** | Xử lý các trang từng cái một hoặc tăng heap JVM (`-Xmx2g`). |

## Câu hỏi thường gặp

**Q: Aspose.CAD có tương thích với các định dạng tệp CAD khác nhau không?**  
A: Có, nó hỗ trợ hơn 30 định dạng CAD và raster, bao gồm DWG, DXF, DGN và SVG.

**Q: Tôi có thể tùy chỉnh độ phân giải của ảnh raster đầu ra không?**  
A: Chắc chắn. Điều chỉnh `setPageWidth`, `setPageHeight` hoặc `setResolution` trong `CadRasterizationOptions` để đạt DPI mong muốn.

**Q: Làm thế nào để chuyển đổi nhiều layout CAD trong một lần chạy?**  
A: Cung cấp một mảng chứa tất cả tên layout cho `setLayouts`, ví dụ `new String[]{"Model","Layout1","Layout2"}`.

**Q: Có định dạng đầu ra nào khác ngoài TIFF được hỗ trợ không?**  
A: Có—PNG, JPEG, BMP, PDF và nhiều định dạng khác có sẵn qua các lớp `*Options` tương ứng.

**Q: Tôi có thể nhận hỗ trợ hoặc chia sẻ kinh nghiệm với Aspose.CAD ở đâu?**  
A: Truy cập [diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để nhận hỗ trợ cộng đồng và trợ giúp chính thức.

## Kết luận

Bằng cách thực hiện các bước này, bạn có thể **convert DWG to PNG**, **export CAD as PNG**, **save CAD as JPEG**, hoặc tạo bất kỳ định dạng raster nào khác mà bạn cần. Aspose.CAD cho Java thực hiện phần công việc nặng, cho phép bạn tập trung vào việc tích hợp hình ảnh chất lượng cao vào ứng dụng, tài liệu hoặc cổng web của mình. Hỗ trợ hơn 30 định dạng và khả năng render các bản vẽ hàng trăm trang mà không cần tải toàn bộ tệp vào bộ nhớ khiến thư viện này là lựa chọn mạnh mẽ cho raster hoá CAD cấp doanh nghiệp.

---

**Last Updated:** 2026-10-04  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

```bash
java -jar aspose-cad.jar -i input.dwg -o output.png -w 1200 -h 1200
```

## Hướng dẫn liên quan

- [Nhanh chóng xuất DWG sang PDF hoặc Raster bằng thư viện java cad Aspose.CAD cho Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Chuyển DWG sang BMP với Aspose.CAD cho Java](/cad/java/cad-export-options/export-to-bmp/)
- [Xuất DWG sang PDF: Layout cụ thể bằng Aspose.CAD cho Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}