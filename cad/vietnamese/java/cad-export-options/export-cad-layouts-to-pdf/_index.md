---
date: 2025-12-21
description: Tìm hiểu cách xuất bố cục CAD sang PDF bằng Aspose.CAD cho Java – một
  cách nhanh chóng, đáng tin cậy để tạo PDF từ các tệp CAD.
linktitle: Export CAD Layouts to PDF
second_title: Aspose.CAD Java API
title: Cách xuất bố cục CAD sang PDF bằng Aspose.CAD cho Java
url: /vi/java/cad-export-options/export-cad-layouts-to-pdf/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách xuất bố cục CAD sang PDF bằng Aspose.CAD cho Java

## Giới thiệu

Trong hướng dẫn này, chúng tôi sẽ chỉ cho bạn **cách xuất bố cục CAD** sang PDF bằng Aspose.CAD cho Java. Dù bạn đang làm việc với DWG, DXF hay các định dạng CAD khác, hướng dẫn này sẽ dẫn bạn qua một quy trình lập trình sạch sẽ để tạo PDF từ các tệp CAD một cách nhanh chóng và đáng tin cậy.

## Câu trả lời nhanh
- **Thư viện này làm gì?** Nó chuyển đổi bản vẽ CAD (DWG, DXF, DWF, v.v.) sang PDF, hình ảnh raster và các định dạng khác.  
- **Ngôn ngữ nào được sử dụng?** Java – mã chạy trên bất kỳ nền tảng tương thích JVM nào.  
- **Có cần giấy phép không?** Có bản dùng thử miễn phí; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Tôi có thể chuyển đổi DWG sang PDF trong Java không?** Có – cùng một API hỗ trợ chuyển đổi **dwg to pdf java**.  
- **Các bước chính là gì?** Tải tệp CAD, thiết lập tùy chọn rasterization, cấu hình tùy chọn PDF và lưu kết quả.

## Yêu cầu trước

Trước khi bắt đầu tutorial, hãy chắc chắn rằng bạn đã chuẩn bị các yêu cầu sau:

- Aspose.CAD cho Java: Đảm bảo bạn đã cài đặt thư viện. Bạn có thể tải xuống từ trang web Aspose [tại đây](https://releases.aspose.com/cad/java/).

- Môi trường phát triển Java: Đảm bảo bạn đã thiết lập môi trường phát triển Java trên máy tính của mình.

Bây giờ mọi thứ đã sẵn sàng, hãy bắt đầu tutorial.

## “how to export cad” là gì?

Xuất CAD có nghĩa là chuyển đổi dữ liệu bản vẽ CAD gốc (như DWG, DXF hoặc DWF) sang một định dạng dễ đọc hơn như PDF. Quá trình này rất cần thiết để chia sẻ thiết kế với các bên liên quan có thể không cài đặt phần mềm CAD.

## Tại sao nên dùng Aspose.CAD cho Java để xuất CAD sang PDF?

- **Độ trung thực cao** – đồ họa vector được bảo toàn, và các tùy chọn rasterization cho phép bạn tinh chỉnh chất lượng.  
- **Không phụ thuộc bên ngoài** – thuần Java, không cần DLL native hay thành phần COM.  
- **Hỗ trợ đa định dạng** – bạn cũng có thể **generate pdf from cad** cho các tệp được tạo trong DWG, DWF hoặc các định dạng khác.  
- **Mở rộng cho công việc batch** – lý tưởng cho tự động hoá phía server, pipeline CI, hoặc tiện ích desktop.

## Nhập không gian tên

Trong mã Java của bạn, bắt đầu bằng cách nhập các không gian tên cần thiết. Các import này cung cấp quyền truy cập vào các lớp và phương thức cần thiết để làm việc với Aspose.CAD cho Java.

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

## Bước 1: Tải tệp CAD

Bắt đầu bằng cách tải tệp CAD vào ứng dụng Java của bạn bằng phương thức `Image.load`. Thay `"conic_pyramid.dxf"` bằng đường dẫn tới tệp CAD của bạn.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

## Bước 2: Thiết lập tùy chọn rasterization

Tạo một thể hiện của `CadRasterizationOptions` để định nghĩa cách các thực thể CAD sẽ được raster hóa. Điều chỉnh các tham số như chiều rộng trang, chiều cao trang và tỉ lệ bố cục theo yêu cầu của bạn.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(false);
rasterizationOptions.setContentAsBitmap(true);
rasterizationOptions.setLayouts(new String[]{"Model"});
```

## Bước 3: Thiết lập tùy chọn PDF

Tạo một thể hiện của `PdfOptions` và liên kết nó với các tùy chọn rasterization. Ngoài ra, thiết lập các tùy chọn đồ họa cho việc xuất PDF, chẳng hạn như chế độ làm mịn, gợi ý render văn bản và chế độ nội suy.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.getGraphicsOptions().setSmoothingMode(SmoothingMode.HighQuality);
rasterizationOptions.getGraphicsOptions().setTextRenderingHint(TextRenderingHint.AntiAliasGridFit);
rasterizationOptions.getGraphicsOptions().setInterpolationMode(InterpolationMode.HighQualityBicubic);
```

## Bước 4: Xuất sang PDF

Cuối cùng, xuất các bố cục CAD sang tệp PDF bằng phương thức `save` của đối tượng `cadImage`.

```java
cadImage.save(dataDir + "CADLayoutsToPDF_out_.pdf", pdfOptions);
```

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|------------|----------|
| **PDF đầu ra trống** | Các tùy chọn rasterization không được thiết lập đúng (ví dụ: tên layout không khớp) | Kiểm tra `rasterizationOptions.setLayouts()` để đảm bảo khớp với tên layout trong tệp CAD của bạn. |
| **Hình ảnh độ phân giải thấp** | `PageWidth`/`PageHeight` quá nhỏ | Tăng kích thước trang hoặc đặt DPI cao hơn qua `rasterizationOptions.setResolution()`. |
| **Phiên bản CAD không được hỗ trợ** | Các phiên bản DWG/DXF cũ có thể cần bản Aspose.CAD mới hơn | Tải xuống phiên bản thư viện mới nhất từ trang Aspose. |

## Câu hỏi thường gặp

### Q1: Tôi có thể dùng Aspose.CAD cho Java với các định dạng tệp CAD khác không?

A1: Có, Aspose.CAD hỗ trợ nhiều định dạng CAD, bao gồm DWG, DXF, DWF và hơn thế nữa. Xem tài liệu [tại đây](https://reference.aspose.com/cad/java/) để biết danh sách đầy đủ.

### Q2: Có bản dùng thử miễn phí cho Aspose.CAD cho Java không?

A2: Có, bạn có thể khám phá các tính năng của Aspose.CAD với bản dùng thử miễn phí [tại đây](https://releases.aspose.com/).

### Q3: Làm sao tôi có thể nhận hỗ trợ cho Aspose.CAD cho Java?

A3: Truy cập diễn đàn Aspose.CAD [tại đây](https://forum.aspose.com/c/cad/19) để nhận hỗ trợ cộng đồng. Đối với hỗ trợ cao cấp, hãy cân nhắc mua giấy phép [tại đây](https://purchase.aspose.com/buy).

### Q4: Sự khác nhau giữa việc tự động và thủ công trong việc điều chỉnh tỉ lệ layout là gì?

A4: Điều chỉnh tỉ lệ layout tự động sẽ thay đổi kích thước layout dựa trên kích thước trang đã chỉ định, trong khi điều chỉnh thủ công cho phép bạn đặt giá trị tỉ lệ tùy chỉnh.

### Q5: Tôi có thể tùy chỉnh giao diện của các tệp PDF đã xuất không?

A5: Có, bạn có thể tùy chỉnh các tùy chọn đồ họa trong mã để kiểm soát chất lượng và giao diện của PDF xuất ra.

### Q6: Aspose.CAD có hỗ trợ chuyển đổi **dwg to pdf java** trực tiếp không?

A6: Chắc chắn. Các tùy chọn rasterization và PDF giống nhau hoạt động cho tệp DWG, cho phép chuyển đổi **dwg to pdf java** một cách liền mạch.

### Q7: Có cách nào để **generate pdf from cad** mà không raster hóa thành bitmap không?

A7: Bằng cách đặt `rasterizationOptions.setContentAsBitmap(false)`, bạn có thể giữ dữ liệu vector khi có thể, tạo ra một PDF dựa trên vector thực sự.

---

**Cập nhật lần cuối:** 2025-12-21  
**Kiểm tra với:** Aspose.CAD cho Java 24.10  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}