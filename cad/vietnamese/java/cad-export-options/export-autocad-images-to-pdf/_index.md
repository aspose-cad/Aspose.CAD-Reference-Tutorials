---
date: 2025-12-19
description: Tìm hiểu cách xuất PDF từ AutoCAD bằng Aspose.CAD cho Java. Hướng dẫn
  từng bước này chỉ cho bạn cách chuyển DWG sang PDF, lưu CAD dưới dạng PDF và xử
  lý giấy phép.
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: Xuất PDF AutoCAD - Xuất hình ảnh AutoCAD sang PDF bằng Aspose.CAD cho Java
  Tutorial
url: /vi/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xuất PDF AutoCAD - Xuất Hình ảnh AutoCAD sang PDF với Aspose.CAD cho Java

## Giới thiệu

Bạn đang tìm cách **xuất PDF AutoCAD** một cách liền mạch bằng Java? Đừng lo lắng! Trong hướng dẫn này, chúng tôi sẽ chỉ cho bạn cách chuyển đổi hình ảnh AutoCAD sang PDF với Aspose.CAD cho Java, một thư viện mạnh mẽ giúp quá trình **chuyển DWG sang PDF** trở nên dễ dàng. Khi hoàn thành, bạn sẽ hiểu cách **lưu CAD dưới dạng PDF**, áp dụng các cài đặt rasterization tùy chỉnh, và làm việc với giấy phép Aspose.CAD cho môi trường sản xuất.

## Câu trả lời nhanh
- **Tôi có thể chuyển DWG sang PDF bằng Java không?** Có, Aspose.CAD cho Java hỗ trợ DWG, DXF và nhiều định dạng khác.  
- **Tôi có cần giấy phép không?** Một **giấy phép Aspose CAD** là bắt buộc để sử dụng không giới hạn; giấy phép tạm thời có sẵn cho việc đánh giá.  
- **Phiên bản Java nào được hỗ trợ?** Java 8+ (thư viện tương thích với mọi JDK hiện đại).  
- **Tôi có thể tùy chỉnh kích thước trang PDF không?** Chắc chắn – điều chỉnh `pageWidth` và `pageHeight` trong các tùy chọn rasterization.  
- **Rasterization 3‑D có khả thi không?** Có, bật `TypeOfEntities.Entities3D` để render đầy đủ 3‑D.

## **export autocad pdf** là gì?
Xuất PDF AutoCAD có nghĩa là chuyển đổi các bản vẽ CAD dựa trên vector (DWG, DXF, DWF, v.v.) thành tài liệu PDF di động trong khi vẫn giữ nguyên các lớp, độ dày đường, và tùy chọn hình học 3‑D. Điều này hữu ích để chia sẻ thiết kế với khách hàng, lưu trữ, hoặc in ấn mà không cần phần mềm CAD.

## Tại sao nên dùng Aspose.CAD cho Java để **export autocad pdf**?
- **Hỗ trợ đầy đủ định dạng** – hoạt động với DWG, DXF, DWF và nhiều hơn nữa.  
- **Không phụ thuộc bên ngoài** – thư viện thuần Java, không cần DLL gốc.  
- **Rasterization chất lượng cao** – kiểm soát DPI, kích thước trang và bố cục.  
- **Linh hoạt về giấy phép** – bắt đầu với bản dùng thử miễn phí, sau đó nâng cấp lên **giấy phép Aspose CAD** vĩnh viễn.  

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn bạn đã có:

- **Môi trường phát triển Java** – JDK 8 trở lên đã được cài đặt.  
- **Thư viện Aspose.CAD cho Java** – tải về từ [liên kết tải xuống](https://releases.aspose.com/cad/java/).  
- **Thư mục tài liệu** – một thư mục trên máy của bạn nơi lưu các tệp CAD nguồn và các PDF được tạo ra.

## Nhập không gian tên

Trong dự án Java của bạn, nhập các lớp cần thiết để làm việc với Aspose.CAD:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Bây giờ chúng ta sẽ đi qua mã từng bước.

## Hướng dẫn từng bước

### Bước 1: Đặt đường dẫn thư mục tài nguyên

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Mẹo:** Thay thế `"Your Document Directory"` bằng đường dẫn tuyệt đối tới thư mục bạn đã tạo ở phần yêu cầu trước.

### Bước 2: Tải hình ảnh CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Tại sao điều này quan trọng:** Việc tải tệp CAD vào đối tượng `Image` cho phép bạn truy cập đầy đủ vào engine rasterization của Aspose.CAD.

### Bước 3: Đặt tùy chọn rasterization

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- Điều chỉnh `pageWidth` và `pageHeight` để thay đổi kích thước PDF đầu ra.  
- Bỏ comment dòng `setTypeOfEntities` nếu bạn cần **java convert cad pdf** cho các thực thể 3‑D.  
- Lệnh `setLayouts` chọn layout nào (Model, Layout1, v.v.) sẽ được render.

### Bước 4: Cấu hình tùy chọn PDF

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Điều này liên kết các cài đặt rasterization với đầu ra PDF, đảm bảo dữ liệu vector được chuyển đổi đúng cách.

### Bước 5: Lưu PDF

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

Tệp kết quả, `Export3DImagestoPDF_out_.pdf`, là một bản **save cad as pdf** của bản vẽ AutoCAD gốc của bạn.

## Các vấn đề thường gặp & Giải pháp

| Symptom | Likely Cause | Fix |
|---------|--------------|-----|
| Blank PDF output | Rasterization options not set or layout mismatch | Verify `setLayouts` matches the layout name in your CAD file. |
| Low‑resolution image | `pageWidth`/`pageHeight` too small | Increase dimensions or set a higher DPI via `rasterizationOptions.setResolution(...)`. |
| License exception | No valid license applied | Apply an **Aspose CAD license** or use a temporary license for testing. |

## Câu hỏi thường gặp

### Q1: Tôi có thể dùng Aspose.CAD cho Java với các định dạng CAD khác không?
A1: Có, Aspose.CAD hỗ trợ nhiều định dạng bao gồm DWG, DWF, DGN và hơn thế nữa, mang lại sự linh hoạt cho dự án của bạn.

### Q2: Làm sao để lấy giấy phép tạm thời cho Aspose.CAD cho Java?
A2: Truy cập [đây](https://purchase.aspose.com/temporary-license/) để nhận giấy phép tạm thời cho mục đích đánh giá.

### Q3: Có tùy chọn layout nào cho rasterization không?
A3: Có, bạn có thể tùy chỉnh các layout (ví dụ: `"Model"`, `"Layout1"`) thông qua phương thức `setLayouts` để kiểm soát view sẽ được render.

### Q4: Tôi có thể tùy chỉnh kích thước file PDF đầu ra không?
A4: Chắc chắn! Điều chỉnh các tham số `pageWidth` và `pageHeight` trong rasterization options để phù hợp với kích thước mong muốn.

### Q5: Tôi có thể tìm kiếm trợ giúp hoặc thảo luận các vấn đề liên quan đến Aspose.CAD cho Java ở đâu?
A5: Hãy truy cập [diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để nhận hỗ trợ chuyên biệt và thảo luận cộng đồng.

---

**Last Updated:** 2025-12-19  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}