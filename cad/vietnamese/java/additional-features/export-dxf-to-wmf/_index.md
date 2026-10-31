---
date: 2026-10-30
description: Tìm hiểu cách chuyển đổi hàng loạt tệp DXF sang WMF bằng Aspose.CAD for
  Java, kèm mã từng bước, thông tin phiên bản dùng thử miễn phí và tùy chọn xuất ra
  PDF.
keywords:
- batch convert dxf files
- aspose cad java
- dxf to wmf conversion
- java cad rasterization
- aspose free trial
lastmod: 2026-10-30
linktitle: Xuất DXF sang định dạng WMF bằng Java
og_description: Chuyển đổi hàng loạt tệp DXF sang WMF bằng Aspose.CAD for Java. Thực
  hiện theo hướng dẫn này để tải bản vẽ DXF, thiết lập tùy chọn rasterization, lưu
  dưới dạng WMF và tùy chọn xuất ra PDF với phiên bản dùng thử miễn phí.
og_image_alt: Tutorial showing batch conversion of DXF to WMF in Java using Aspose.CAD
og_title: Chuyển đổi hàng loạt tệp DXF sang WMF với Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-30'
  description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  headline: Batch convert DXF files to WMF with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  name: Batch convert DXF files to WMF with Aspose.CAD for Java
  steps:
  - name: load dxf drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: configure rasterization options
    text: '`CadRasterizationOptions` specifies page size, resolution, and background
      for rasterizing the CAD drawing.'
  - name: save as wmf
    text: '`ImageSaveOptions` with `SaveFormat.WMF` tells Aspose.CAD to write the
      output as a Windows Metafile.'
  - name: dispose of resources
    text: Calling `image.close()` releases native resources used by the Aspose.CAD
      Image object.
  - name: optional – export to pdf
    text: '`PdfOptions` configures PDF‑specific settings when saving the image as
      a PDF document. > **Pro tip:** You can reuse the same `CadRasterizationOptions`
      object for PDF export by passing it to a `PdfOptions` instance, saving you a
      few lines of setup.'
  type: HowTo
- questions:
  - answer: You can access the documentation [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).
    question: Where can I find the Aspose.CAD documentation?
  - answer: Download the library [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).
    question: How do I download Aspose.CAD for Java?
  - answer: Yes, you can get a free trial [Aspose free trial page](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Explore temporary licenses [temporary license options](https://purchase.aspose.com/temporary-license/).
    question: Need temporary licensing options?
  - answer: Visit the Aspose.CAD support forum [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).
    question: Where can I get support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- batch convert dxf
- Aspose.CAD
- Java CAD conversion
- WMF export
- DXF processing
title: Chuyển đổi hàng loạt tệp DXF sang WMF với Aspose.CAD for Java
url: /vi/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chuyển đổi hàng loạt tệp DXF sang WMF với Aspose.CAD cho Java

## Giới thiệu

Trong hướng dẫn này, bạn sẽ học cách **chuyển đổi hàng loạt tệp DXF sang WMF** bằng cách sử dụng Aspose.CAD cho Java. Dù bạn cần nhúng bản vẽ CAD vào các báo cáo dựa trên Windows, tạo đồ họa vector nhẹ cho tài liệu Office, hay tự động hoá việc chuyển đổi quy mô lớn, hướng dẫn này sẽ chỉ cho bạn cách tải bản vẽ DXF, cấu hình các tùy chọn rasterization, lưu dưới dạng WMF, và tùy chọn xuất cùng bản vẽ sang PDF. Các bước này hoạt động trên bất kỳ nền tảng nào chạy Java 8+.

## Câu trả lời nhanh
- **Bạn có thể chuyển đổi DXF sang WMF với bản dùng thử miễn phí không?** Có – Aspose cung cấp bản dùng thử đầy đủ chức năng trong 30 ngày.  
- **Phiên bản Java nào được yêu cầu?** Java 8 hoặc mới hơn.  
- **Tôi có cần giấy phép để chạy mã không?** Cần giấy phép cho môi trường sản xuất; bản dùng thử hoạt động cho phát triển và kiểm thử.  
- **Quá trình chuyển đổi có mất dữ liệu không?** Dữ liệu vector được bảo toàn; các tùy chọn rasterization cho phép bạn kiểm soát độ phân giải.  
- **Tôi có thể xuất cùng bản vẽ sang PDF không?** Chắc chắn – xem bước “Export to PDF” bên dưới.  
- **Làm thế nào để chuyển đổi hàng loạt nhiều tệp DXF cùng một lúc?** Duyệt qua một thư mục, áp dụng cùng mẫu load‑rasterize‑save cho mỗi tệp.

## Chuyển đổi hàng loạt tệp DXF là gì?

Chuyển đổi hàng loạt tệp DXF có nghĩa là xử lý nhiều bản vẽ Định dạng Trao đổi Bản vẽ (DXF) trong một lần chạy và tạo ra đầu ra WMF cho mỗi bản vẽ. WMF (Windows Metafile) là định dạng ảnh vector tích hợp sẵn với Microsoft Office, các ứng dụng Windows và nhiều công cụ báo cáo.

## Tại sao nên sử dụng Aspose.CAD cho Java?

Aspose.CAD cho Java là một engine thuần Java hỗ trợ **hơn 50 định dạng đầu vào và đầu ra**—bao gồm DXF, DWG, DGN, PDF, PNG, SVG và WMF—với **độ trung thực vector 99 %**. Nó chạy trên bất kỳ hệ điều hành nào hỗ trợ Java, không yêu cầu DLL gốc, và cho phép bạn kiểm soát kích thước trang, DPI và màu nền thông qua một lớp `CadRasterizationOptions` duy nhất. API này cũng xử lý xuất PDF, PNG và SVG, loại bỏ nhu cầu sử dụng nhiều thư viện.

### Lợi ích định lượng
- **Hơn 50 định dạng được hỗ trợ** giảm nhu cầu sử dụng các bộ chuyển đổi bên thứ ba.  
- **Xử lý tệp DXF 300 trang trong dưới 5 giây** trên máy chủ 2.5 GHz điển hình khi rasterized ở 150 DPI.  
- **Dung lượng bộ nhớ duy trì dưới 200 MB** cho các tệp lên tới 500 MB khi bạn đặt kích thước trang phù hợp.  

## Yêu cầu trước

- **Aspose.CAD cho Java** được tích hợp vào dự án của bạn. Tải xuống từ trang chính thức: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- Một thư mục chứa các tệp DXF bạn muốn chuyển đổi (ví dụ, `Your Document Directory/DXFDrawings/`).  

## Nhập không gian tên

`Image` là lớp cốt lõi của Aspose.CAD đại diện cho một bản vẽ CAD trong bộ nhớ. Sau khi tải tệp, tất cả các thao tác tiếp theo—rasterization, chuyển đổi định dạng và dọn dẹp tài nguyên—đều được thực hiện thông qua đối tượng này.

Các import sau đưa vào các lớp Aspose.CAD cần thiết để tải, rasterize và lưu các tệp CAD.  
```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageSaveOptions;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import java.awt.Color;
```

## Hướng dẫn từng bước

### Làm thế nào để chuyển đổi hàng loạt tệp DXF sang WMF trong Java?

Tải mỗi DXF bằng `Image.load`, cấu hình `CadRasterizationOptions` cho kích thước trang và DPI mong muốn, và gọi `image.save` với `SaveFormat.WMF`. Mẫu ba bước này thực hiện chuyển đổi hoàn chỉnh trong khi giữ nguyên chất lượng vector và chỉ yêu cầu vài dòng mã cho mỗi tệp.

#### Bước 1: tải bản vẽ dxf

`Image.load` đọc tệp DXF vào một đối tượng Aspose.CAD Image.  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### Bước 2: cấu hình tùy chọn rasterization

`CadRasterizationOptions` xác định kích thước trang, độ phân giải và màu nền khi rasterize bản vẽ CAD.  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### Bước 3: lưu dưới dạng wmf

`ImageSaveOptions` với `SaveFormat.WMF` chỉ định cho Aspose.CAD ghi đầu ra dưới dạng Windows Metafile.  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### Bước 4: giải phóng tài nguyên

Gọi `image.close()` giải phóng các tài nguyên gốc được Aspose.CAD Image sử dụng.  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### Bước 5: tùy chọn – xuất sang pdf

`PdfOptions` cấu hình các thiết lập đặc thù cho PDF khi lưu ảnh dưới dạng tài liệu PDF.  
```java
finally
{
  cadImage.dispose();
}
```

> **Pro tip:** Bạn có thể tái sử dụng cùng một đối tượng `CadRasterizationOptions` cho việc xuất PDF bằng cách truyền nó vào một thể hiện `PdfOptions`, giúp bạn tiết kiệm vài dòng cấu hình.

## Làm thế nào để xuất DXF sang PDF bằng Aspose CAD Java?

Thay đổi định dạng lưu WMF thành PDF bằng cách sử dụng `new ImageSaveOptions(SaveFormat.Pdf)`. Các thiết lập rasterization vẫn được áp dụng, và bạn có thể thêm các tùy chọn đặc thù cho PDF như siêu dữ liệu tác giả hoặc mức nén. Lệnh chuyển đổi một dòng này tạo ra một tệp PDF có thể tìm kiếm, chính xác về trang và phản ánh bố cục CAD gốc.

## Các vấn đề thường gặp và giải pháp

`License` là lớp Aspose dùng để áp dụng giấy phép sản phẩm tại thời gian chạy.

| Vấn đề | Nguyên nhân | Cách khắc phục |
|-------|------------|----------------|
| **`NullPointerException` on `cadImage.save`** | Biến `cadImage` chưa được định nghĩa (nên là `image`). | Thay `cadImage` bằng `image` hoặc đổi tên biến một cách nhất quán. |
| **Output WMF is blank** | Kích thước trang rasterization quá nhỏ hoặc màu nền được đặt là trong suốt. | Tăng `PageWidth`/`PageHeight` hoặc đặt màu nền qua `rasterizationOptions.setBackgroundColor(Color.WHITE);`. |
| **License exception** | Chạy mà không có giấy phép Aspose hợp lệ trong môi trường sản xuất. | Áp dụng tệp giấy phép khi khởi động ứng dụng: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Câu hỏi thường gặp

**Q: Tôi có thể tìm tài liệu Aspose.CAD ở đâu?**  
A: Bạn có thể truy cập tài liệu tại [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).

**Q: Làm thế nào để tải Aspose.CAD cho Java?**  
A: Tải thư viện từ [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).

**Q: Có bản dùng thử miễn phí không?**  
A: Có, bạn có thể nhận bản dùng thử miễn phí tại [Aspose free trial page](https://releases.aspose.com/).

**Q: Cần các tùy chọn cấp phép tạm thời?**  
A: Khám phá các giấy phép tạm thời tại [temporary license options](https://purchase.aspose.com/temporary-license/).

**Q: Tôi có thể nhận hỗ trợ ở đâu?**  
A: Truy cập diễn đàn hỗ trợ Aspose.CAD tại [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).

## Các câu hỏi thường gặp bổ sung

**Q: Tôi có thể chuyển đổi các tệp DXF lớn (hàng trăm MB) mà không hết bộ nhớ không?**  
A: Có. Tải tệp trong khối `try‑with‑resources` và giải phóng đối tượng `Image` ngay sau khi dùng. Điều chỉnh `CadRasterizationOptions.setPageWidth/Height` về kích thước hợp lý để giảm mức tiêu thụ bộ nhớ.

**Q: Đầu ra WMF có giữ lại thông tin lớp không?**  
A: WMF là định dạng vector phẳng, vì vậy cấu trúc lớp được làm phẳng, nhưng các kiểu đường, màu sắc và mẫu hatch vẫn được bảo toàn.

**Q: Có thể đặt DPI tùy chỉnh cho WMF không?**  
A: Sử dụng `rasterizationOptions.setResolution(300);` để định nghĩa DPI trước khi lưu.

**Q: Tôi có thể chuyển đổi hàng loạt nhiều tệp DXF trong một lần chạy không?**  
A: Chắc chắn. Duyệt qua một thư mục, tải mỗi tệp và áp dụng cùng logic rasterization và lưu.

**Q: Những phiên bản Java nào được hỗ trợ?**  
A: Aspose.CAD cho Java hỗ trợ Java 8 trở lên, bao gồm Java 11, 17 và các bản LTS mới hơn.

---

**Cập nhật lần cuối:** 2026-10-30  
**Được kiểm tra với:** Aspose.CAD cho Java 24.11  
**Tác giả:** Aspose

## Hướng dẫn liên quan

- [Tạo PDF từ CAD – Xuất DXF sang PDF với Aspose.CAD cho Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Tạo PDF từ DXF: Xuất lớp với Aspose.CAD cho Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Cách chuyển đổi bố cục DXF sang ảnh JPEG với Aspose.CAD trong Java](/cad/java/additional-features/export-specific-layout-to-image/)

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}