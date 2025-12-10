---
date: 2025-12-10
description: Tìm hiểu cách tạo PDF từ CAD bằng Aspose.CAD cho Java với tùy chỉnh bút
  vẽ. Hướng dẫn từng bước này cho thấy cách xuất CAD sang PDF một cách hiệu quả.
linktitle: Pen Support in Export
second_title: Aspose.CAD Java API
title: Cách tạo PDF từ CAD với hỗ trợ bút khi xuất
url: /vi/java/advanced-cad-features/pen-support-in-export/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hỗ trợ bút trong xuất

## Giới thiệu

Trong thế giới chuyển đổi CAD nhanh chóng, các nhà phát triển thường cần **create PDF from CAD** các tệp trong khi giữ nguyên độ trung thực hình ảnh. Aspose.CAD for Java làm cho việc này trở nên đơn giản, cung cấp các tùy chọn phong phú như tùy chỉnh bút cho phép bạn tinh chỉnh kiểu đường trong quá trình xuất. Trong hướng dẫn này, chúng tôi sẽ đi qua một ví dụ thực tế, toàn diện, cho thấy cách **export CAD to PDF** với các cài đặt bút tùy chỉnh, để bạn có thể tạo ra các PDF hoàn thiện trực tiếp từ bản vẽ DXF.

## Câu trả lời nhanh
- **“create PDF from CAD” có nghĩa là gì?** Chuyển đổi bản vẽ CAD (ví dụ, DXF) thành tài liệu PDF trong khi vẫn giữ chất lượng vector.  
- **Thư viện nào xử lý tùy chỉnh bút?** Aspose.CAD for Java’s `PenOptions` class.  
- **Tôi có thể sử dụng điều này cho các định dạng khác không?** Có – cùng một cài đặt bút áp dụng cho PNG, BMP, TIFF, v.v.  
- **Tôi có cần giấy phép không?** A valid Aspose.CAD license is required for production use.  
- **Phiên bản Java tối thiểu là gì?** Java 8 or higher.

## “create PDF from CAD” là gì?
Tạo PDF từ CAD có nghĩa là raster hóa hoặc render vector một bản vẽ CAD thành tệp PDF. Điều này cho phép chia sẻ, in ấn và lưu trữ thiết kế kỹ thuật một cách dễ dàng mà không cần phần mềm CAD ở phía người nhận.

## Tại sao nên sử dụng hỗ trợ bút khi xuất CAD sang PDF?
Hỗ trợ bút cho phép bạn kiểm soát các đầu nét, nối và độ dày, giúp bạn có khả năng phù hợp với thương hiệu công ty hoặc tiêu chuẩn bản vẽ kỹ thuật. Nó đặc biệt hữu ích khi việc render đường mặc định không đáp ứng yêu cầu hình ảnh của bạn.

## Yêu cầu trước

- **Môi trường phát triển Java** – một JDK hoạt động (phiên bản 8 hoặc mới hơn) và một IDE hoặc công cụ xây dựng mà bạn lựa chọn.  
- **Thư viện Aspose.CAD** – tải JAR mới nhất từ trang chính thức [here](https://releases.aspose.com/cad/java/).  
- **Một tệp DXF mẫu** – cho hướng dẫn này chúng ta sẽ sử dụng `conic_pyramid.dxf`.

Bây giờ chúng ta đã sẵn sàng, hãy đi sâu vào mã.

## Nhập không gian tên

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.PenOptions;
import com.aspose.cad.internal.imaging.LineCap;
```

## Bước 1: Xác định Thư mục Tài liệu của Bạn

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

> **Mẹo chuyên nghiệp:** Thay thế `"Your Document Directory"` bằng đường dẫn tuyệt đối nơi chứa các tệp DXF của bạn.

## Bước 2: Tải tệp CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

Phương thức `Image.load` đọc tệp DXF và tạo một đối tượng `CadImage` mà chúng ta có thể thao tác.

## Bước 3: Cấu hình tùy chọn raster hóa

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImage.getWidth() * 100);
rasterizationOptions.setPageHeight(cadImage.getHeight() * 100);
```

Điều chỉnh kích thước trang để kiểm soát độ phân giải của PDF kết quả. Nhân với 100 cho ra đầu ra độ phân giải cao, phù hợp cho việc in ấn.

## Bước 4: Tùy chỉnh tùy chọn bút

```java
PenOptions penOts = new PenOptions();
penOts.setStartCap(LineCap.Flat);
penOts.setEndCap(LineCap.Flat);
```

Ở đây chúng ta đặt cả đầu bắt đầu và đầu kết thúc của bút thành `Flat`. Bạn có thể thử nghiệm các giá trị `LineCap` khác (ví dụ, `Round`, `Square`) để đạt hiệu ứng hình ảnh khác nhau.

## Bước 5: Cấu hình tùy chọn xuất PDF

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Đối tượng `PdfOptions` liên kết các cài đặt raster hóa với quá trình xuất PDF.

## Bước 6: Lưu PDF đã xuất

```java
cadImage.save((dataDir + "9LHATT-A56_generated.pdf"), pdfOptions);
```

Chạy dòng lệnh này sẽ ghi một tệp PDF có tên `9LHATT-A56_generated.pdf` vào thư mục `dataDir` của bạn, hoàn chỉnh với kiểu bút tùy chỉnh mà bạn đã định nghĩa.

## Các trường hợp sử dụng phổ biến

- **Tài liệu kỹ thuật** – nhúng các bản vẽ kỹ thuật chính xác vào sổ tay PDF.  
- **Báo cáo tự động** – tạo PDF từ dữ liệu CAD ngay lập tức trong các dịch vụ web.  
- **Kiểm soát chất lượng** – áp dụng các đầu nét tùy chỉnh để làm nổi bật các đường đo lường hoặc dung sai.

## Khắc phục sự cố & Mẹo

- **Đường dẫn tệp không đúng** – đảm bảo `dataDir` kết thúc bằng dấu phân cách thư mục (`/` hoặc `\\`).  
- **Thiếu giấy phép** – nếu không có giấy phép hợp lệ, thư viện sẽ chạy ở chế độ đánh giá, có thể thêm watermark.  
- **Kiểu đường không mong muốn** – kiểm tra lại rằng `PenOptions` đã được đặt trước khi gọi `save`; nếu không sẽ sử dụng mặc định.

## Câu hỏi thường gặp

### Q1: Tôi có thể tùy chỉnh tùy chọn bút cho các định dạng khác ngoài PDF không?

A1: Có, việc tùy chỉnh bút được trình bày trong hướng dẫn này áp dụng cho nhiều định dạng ảnh khác nhau, bao gồm PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF và WMF.

### Q2: Làm thế nào để tôi xử lý các đầu nét bắt đầu và kết thúc khác nhau cho bút?

A2: Sử dụng lớp `PenOptions` để đặt các đầu nét bắt đầu và kết thúc mong muốn, cung cấp tính linh hoạt trong việc định nghĩa giao diện của các đường.

### Q3: Nếu tôi không chỉ định tùy chọn bút thì sao?

A3: Nếu không đặt rõ ràng các tùy chọn bút, hệ thống sẽ sử dụng các bút mặc định, có thể khác nhau trong các ngữ cảnh khác nhau.

### Q4: Có những lưu ý đặc biệt nào cho các tùy chọn raster hóa không?

A4: Điều chỉnh chiều rộng và chiều cao trang trong các tùy chọn raster hóa để kiểm soát kích thước của hình ảnh xuất ra.

### Q5: Tôi có thể tìm hỗ trợ bổ sung hoặc các cuộc thảo luận cộng đồng ở đâu?

A5: Khám phá diễn đàn cộng đồng Aspose.CAD tại [here](https://forum.aspose.com/c/cad/19) để được hỗ trợ và thảo luận.

---

**Last Updated:** 2025-12-10  
**Tested With:** Aspose.CAD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}