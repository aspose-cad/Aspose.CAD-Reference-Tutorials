---
date: 2026-06-09
description: Tìm hiểu cách chuyển đổi DXF sang WMF với Aspose.CAD cho Java, bao gồm
  bản dùng thử miễn phí, hỗ trợ Java 8+, và tùy chọn xuất PDF. Hướng dẫn chi tiết
  từng bước kèm ví dụ mã.
keywords:
- convert dxf to wmf
- aspose cad java
- aspose free trial
- aspose cad conversion
- export dxf pdf
linktitle: Xuất DXF sang định dạng WMF bằng Java
schemas:
- author: Aspose
  dateModified: '2026-06-09'
  description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  headline: Convert DXF to WMF Using Aspose.CAD in Java
  type: TechArticle
- description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  name: Convert DXF to WMF Using Aspose.CAD in Java
  steps:
  - name: Load DXF Drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: Configure Rasterization Options
    text: CadRasterizationOptions specifies page size, resolution, and background
      for rasterizing the CAD drawing.
  - name: Save as WMF
    text: ImageSaveOptions with SaveFormat.WMF tells Aspose.CAD to write the output
      as a Windows Metafile.
  - name: Dispose of Resources
    text: Calling image.close() releases native resources used by the Aspose.CAD Image
      object.
  - name: Optional – Export to PDF
    text: PdfOptions configures PDF‑specific settings when saving the image as a PDF
      document. > **Pro tip:** You can reuse the same `CadRasterizationOptions` object
      for PDF export by passing it to a `PdfOptions` instance, saving you a few lines
      of setup.
  type: HowTo
- questions:
  - answer: Yes. Load the file in a try‑with‑resources block and dispose of the `Image`
      object promptly. Adjust `CadRasterizationOptions.setPageWidth/Height` to a reasonable
      size to keep memory usage low.
    question: Can I convert large DXF files (hundreds of MB) without running out of
      memory?
  - answer: WMF is a flat vector format, so layer hierarchy is flattened, but line
      styles, colors, and hatch patterns are preserved.
    question: Does the WMF output retain layer information?
  - answer: Use `rasterizationOptions.setResolution(300);` to define DPI before saving.
    question: Is it possible to set a custom DPI for the WMF?
  - answer: Absolutely. Loop through a directory, load each file, and apply the same
      rasterization and save logic.
    question: Can I batch‑convert multiple DXF files in one run?
  - answer: Aspose.CAD for Java supports Java 8 and later, including Java 11, 17,
      and newer LTS releases.
    question: What versions of Java are supported?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Chuyển đổi DXF sang WMF bằng Aspose.CAD trong Java
url: /vi/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chuyển đổi DXF sang WMF bằng Aspose.CAD trong Java

## Giới thiệu

Trong hướng dẫn này, bạn sẽ khám phá cách **chuyển đổi DXF sang WMF** bằng Aspose.CAD cho Java. Cho dù bạn cần nhúng bản vẽ CAD vào báo cáo dựa trên Windows, tạo đồ họa vector nhẹ cho tài liệu Office, hoặc tự động hoá chuyển đổi hàng loạt, việc chuyển đổi DXF sang WMF là một yêu cầu thường gặp trong các quy trình kỹ thuật và báo cáo. Chúng tôi sẽ hướng dẫn cách tải bản vẽ DXF, cấu hình các tùy chọn rasterization, lưu kết quả dưới dạng WMF, và tùy chọn xuất cùng bản vẽ sang PDF.

## Câu trả lời nhanh
- **Tôi có thể chuyển đổi DXF sang WMF với bản dùng thử miễn phí không?** Có – Aspose cung cấp bản dùng thử đầy đủ chức năng trong 30 ngày.  
- **Phiên bản Java nào được yêu cầu?** Java 8 hoặc mới hơn.  
- **Tôi có cần giấy phép để chạy mã không?** Cần giấy phép cho môi trường sản xuất; bản dùng thử hoạt động cho phát triển và kiểm thử.  
- **Quá trình chuyển đổi có mất dữ liệu không?** Dữ liệu vector được giữ nguyên; các tùy chọn rasterization cho phép bạn kiểm soát độ phân giải.  
- **Tôi cũng có thể xuất cùng bản vẽ sang PDF không?** Chắc chắn – xem bước “Export to PDF” bên dưới.

## “Chuyển đổi DXF sang WMF” là gì?

Chuyển đổi DXF sang WMF có nghĩa là lấy một tệp Drawing Exchange Format (DXF) — một định dạng CAD được sử dụng rộng rãi — và biến nó thành Windows Metafile (WMF). WMF là định dạng hình ảnh vector tích hợp mượt mà với Microsoft Office, các ứng dụng Windows và nhiều công cụ báo cáo.

## Tại sao nên sử dụng Aspose.CAD cho Java?

Aspose.CAD cho Java cung cấp một engine thuần Java, không cần DLL gốc, chuyển đổi các tệp CAD với **hơn 99 % độ trung thực vector**, bảo toàn các lớp, màu sắc, kiểu đường và mẫu hatch. Nó hỗ trợ **hơn 50 định dạng đầu vào và đầu ra** — bao gồm DXF, DWG, DGN, PDF, PNG, SVG và WMF — đồng thời cho phép bạn tinh chỉnh kích thước trang, DPI và màu nền thông qua các tùy chọn rasterization tích hợp. Cùng một API còn xử lý xuất PDF, PNG và SVG, loại bỏ nhu cầu sử dụng nhiều thư viện.

### Lợi thế chính
- **Không phụ thuộc bên ngoài** – thuần Java, hoạt động trên mọi hệ điều hành chạy Java.  
- **Kết xuất độ chính xác cao** – giữ nguyên độ dày đường, màu sắc và chi tiết hatch.  
- **Rasterization tích hợp** – kiểm soát kích thước trang, độ phân giải và nền.  
- **Chuyển đổi một cửa** – cùng các lớp có thể xuất ra WMF, PDF, PNG, SVG, v.v.

## Yêu cầu trước

- **Aspose.CAD cho Java** đã được tích hợp vào dự án của bạn. Tải xuống từ trang chính thức: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- **Thư mục tài liệu** nơi lưu các tệp DXF của bạn (ví dụ, `Your Document Directory/DXFDrawings/`).  

## Nhập không gian tên

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

### Làm thế nào để chuyển đổi DXF sang WMF trong Java?

Tải tệp DXF của bạn bằng `Image.load("yourFile.dxf")`, cấu hình `CadRasterizationOptions` cho kích thước trang và DPI mong muốn, sau đó gọi `image.save("output.wmf", new ImageSaveOptions(SaveFormat.WMF))`. Mô hình ba bước này thực hiện chuyển đổi hoàn chỉnh trong khi giữ nguyên chất lượng vector và chỉ cần vài dòng mã.

#### Bước 1: Tải bản vẽ DXF

`Image.load` đọc tệp DXF vào một đối tượng Aspose.CAD Image.  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### Bước 2: Cấu hình tùy chọn rasterization

`CadRasterizationOptions` chỉ định kích thước trang, độ phân giải và nền cho quá trình rasterize bản vẽ CAD.  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### Bước 3: Lưu dưới dạng WMF

`ImageSaveOptions` với `SaveFormat.WMF` chỉ cho Aspose.CAD ghi đầu ra dưới dạng Windows Metafile.  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### Bước 4: Giải phóng tài nguyên

Gọi `image.close()` giải phóng các tài nguyên gốc được Aspose.CAD Image sử dụng.  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### Bước 5: Tùy chọn – Xuất sang PDF

`PdfOptions` cấu hình các thiết lập đặc thù cho PDF khi lưu hình ảnh dưới dạng tài liệu PDF.  
```java
finally
{
  cadImage.dispose();
}
```

> **Pro tip:** Bạn có thể tái sử dụng cùng một đối tượng `CadRasterizationOptions` cho việc xuất PDF bằng cách truyền nó vào một thể hiện `PdfOptions`, giúp giảm bớt một vài dòng cấu hình.

## Làm thế nào để xuất DXF sang PDF bằng Aspose CAD Java?

Xuất sang PDF tuân theo các bước tải và rasterize giống nhau; chỉ cần thay đổi định dạng lưu WMF thành PDF. Sử dụng `new ImageSaveOptions(SaveFormat.Pdf)` và tùy chọn thêm các thiết lập PDF như mức nén hoặc metadata tác giả. Lệnh một dòng này tạo ra một tệp PDF có thể tìm kiếm, trang chính xác, phản ánh bố cục CAD gốc.

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân | Cách khắc phục |
|-------|-------------|----------------|
| **`NullPointerException` on `cadImage.save`** | Biến `cadImage` chưa được định nghĩa (nên là `image`). | Thay `cadImage` bằng `image` hoặc đổi tên biến một cách nhất quán. |
| **Output WMF is blank** | Kích thước trang rasterization quá nhỏ hoặc màu nền được đặt là trong suốt. | Tăng `PageWidth`/`PageHeight` hoặc đặt màu nền qua `rasterizationOptions.setBackgroundColor(Color.WHITE);`. |
| **License exception** | Chạy mà không có giấy phép Aspose hợp lệ trong môi trường sản xuất. | Áp dụng tệp giấy phép khi khởi động ứng dụng: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Kết luận

Bạn đã có một quy trình hoàn chỉnh, sẵn sàng cho môi trường sản xuất để **chuyển đổi DXF sang WMF** bằng Aspose.CAD cho Java, với bước tùy chọn để **xuất cùng bản vẽ sang PDF**. Cách tiếp cận này cung cấp đầu ra vector chất lượng cao, tích hợp liền mạch với các công cụ báo cáo và tài liệu dựa trên Windows, đồng thời giữ cho codebase của bạn đơn giản và không phụ thuộc.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể tìm tài liệu Aspose.CAD ở đâu?
A1: Bạn có thể truy cập tài liệu [tại đây](https://reference.aspose.com/cad/java/).

### Câu hỏi 2: Làm thế nào để tải Aspose.CAD cho Java?
A2: Tải thư viện [tại đây](https://releases.aspose.com/cad/java/).

### Câu hỏi 3: Có bản dùng thử miễn phí không?
A3: Có, bạn có thể nhận bản dùng thử miễn phí [tại đây](https://releases.aspose.com/).

### Câu hỏi 4: Cần các tùy chọn cấp phép tạm thời?
A4: Khám phá các giấy phép tạm thời [tại đây](https://purchase.aspose.com/temporary-license/).

### Câu hỏi 5: Tôi có thể nhận hỗ trợ ở đâu?
A5: Tham khảo diễn đàn hỗ trợ Aspose.CAD [tại đây](https://forum.aspose.com/c/cad/19).

## Các câu hỏi thường gặp

**Q: Tôi có thể chuyển đổi các tệp DXF lớn (hàng trăm MB) mà không hết bộ nhớ không?**  
A: Có. Tải tệp trong khối `try‑with‑resources` và giải phóng đối tượng `Image` ngay sau khi dùng. Điều chỉnh `CadRasterizationOptions.setPageWidth/Height` về kích thước hợp lý để giảm tiêu thụ bộ nhớ.

**Q: Đầu ra WMF có giữ lại thông tin lớp không?**  
A: WMF là định dạng vector phẳng, vì vậy cấu trúc lớp được làm phẳng, nhưng các kiểu đường, màu sắc và mẫu hatch vẫn được bảo toàn.

**Q: Có thể đặt DPI tùy chỉnh cho WMF không?**  
A: Sử dụng `rasterizationOptions.setResolution(300);` để xác định DPI trước khi lưu.

**Q: Tôi có thể chuyển đổi hàng loạt nhiều tệp DXF trong một lần chạy không?**  
A: Hoàn toàn có thể. Duyệt qua một thư mục, tải từng tệp và áp dụng cùng logic rasterization và lưu.

**Q: Các phiên bản Java nào được hỗ trợ?**  
A: Aspose.CAD cho Java hỗ trợ Java 8 trở lên, bao gồm Java 11, 17 và các phiên bản LTS mới hơn.

---

**Cập nhật lần cuối:** 2026-06-09  
**Kiểm tra với:** Aspose.CAD for Java 24.11  
**Tác giả:** Aspose

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

## Hướng dẫn liên quan

- [Tạo PDF từ CAD – Xuất DXF sang PDF với Aspose.CAD cho Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Tạo PDF từ DXF: Xuất lớp với Aspose.CAD cho Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Cách chuyển đổi bố cục DXF sang ảnh JPEG với Aspose.CAD trong Java](/cad/java/additional-features/export-specific-layout-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}