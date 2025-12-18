---
date: 2025-12-18
description: Khám phá cách xuất DWG sang PDF hoặc hình ảnh raster trong Java bằng
  Aspose.CAD. Hướng dẫn từng bước này đảm bảo độ chính xác, hiệu quả và việc chuyển
  đổi file DWG một cách dễ dàng.
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: Xuất DWG sang PDF hoặc Raster bằng Aspose.CAD cho Java
url: /vi/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xuất DWG sang PDF hoặc Raster bằng Aspose.CAD cho Java

## Giới thiệu

Trong thế giới năng động của thiết kế hỗ trợ máy tính (CAD), việc xử lý bản vẽ một cách hiệu quả là rất quan trọng. Với **Aspose.CAD for Java** bạn có thể **export dwg to pdf** — hoặc hình raster — chỉ với vài dòng mã. Hướng dẫn này sẽ đưa bạn qua toàn bộ quy trình, từ việc tải tệp DWG đến tạo ra một PDF chất lượng cao, đồng thời nêu bật lý do tại sao Aspose.CAD Java là thư viện được lựa chọn cho các nhiệm vụ chuyển đổi CAD.

## Câu trả lời nhanh
- **Mục tiêu của hướng dẫn này là gì?** Xuất các tệp DWG sang PDF hoặc hình raster bằng Aspose.CAD cho Java.  
- **Tôi có cần giấy phép không?** Có một giấy phép tạm thời miễn phí để đánh giá; giấy phép đầy đủ cần thiết cho môi trường sản xuất.  
- **Phiên bản Java nào được hỗ trợ?** Bất kỳ môi trường chạy Java 8+ nào cũng hoạt động với API Aspose.CAD Java mới nhất.  
- **Tôi có thể chuyển đổi DWG sang các định dạng hình ảnh khác không?** Có – các tùy chọn rasterization tương tự cho phép xuất ra PNG, JPEG, BMP, v.v.  
- **Quá trình chuyển đổi mất bao lâu?** Thông thường dưới một giây cho các bản vẽ tiêu chuẩn; các tệp lớn hơn có thể mất vài giây.

## Export dwg to pdf là gì?

Xuất DWG sang PDF có nghĩa là chuyển đổi bản vẽ AutoCAD gốc thành tài liệu PDF di động, không phụ thuộc vào thiết bị. PDF tạo ra giữ nguyên dữ liệu vector, các lớp và tỷ lệ, làm cho nó lý tưởng cho việc chia sẻ, in ấn hoặc lưu trữ.

## Tại sao nên sử dụng Aspose.CAD Java cho việc chuyển đổi này?
- **Không phụ thuộc bên ngoài** – thuần Java, không có DLL gốc.  
- **Xử lý đơn vị chính xác** – tự động tôn trọng đơn vị mét hoặc inch.  
- **Đầu ra raster chất lượng cao** – điều chỉnh DPI và kích thước trang một cách tinh tế.  
- **Hỗ trợ PDF đầy đủ** – tạo PDF giữ vector mà không cần thư viện bổ sung.

## Yêu cầu trước

Trước khi bắt đầu với mã, hãy chắc chắn rằng bạn có:

- Kiến thức cơ bản về lập trình Java.  
- Thư viện Aspose.CAD cho Java đã được cài đặt. Nếu bạn chưa tải xuống, hãy lấy nó **[here](https://releases.aspose.com/cad/java/)**.  
- Một tệp DWG để thử nghiệm – mẫu **Bottom_plate.dwg** được sử dụng trong hướng dẫn này.

## Nhập các không gian tên

Trong dự án Java của bạn, nhập các lớp cần thiết để bắt đầu quá trình chuyển đổi:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Hướng dẫn từng bước

### Bước 1: Tải tệp DWG

Đầu tiên, tải bản vẽ DWG của bạn bằng lớp `Image`. Điều này tạo ra một biểu diễn trong bộ nhớ mà Aspose.CAD có thể làm việc.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Bước 2: Xác định loại đơn vị

Hiểu được bản vẽ sử dụng đơn vị mét hay inch là cần thiết để tỷ lệ đúng. Phương thức trợ giúp `IsMetric` (cài đặt được bỏ qua để ngắn gọn) trả về một giá trị boolean.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Bước 3: Đặt tùy chọn rasterization

Dựa trên hệ thống đơn vị, cấu hình kích thước trang, tỷ lệ và loại đơn vị mục tiêu. Các tùy chọn này quyết định cách DWG được raster hóa trước khi được đưa vào PDF.

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

### Bước 4: Cấu hình tùy chọn PDF

Tạo một thể hiện `PdfOptions` và gắn các cài đặt rasterization. Điều này cho Aspose.CAD biết cách nhúng nội dung raster vào PDF cuối cùng.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Bước 5: Lưu dưới dạng PDF

Cuối cùng, xuất bản vẽ ra tệp PDF. Phương thức `save` nhận đường dẫn đầu ra và `PdfOptions` đã cấu hình.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Khi mã hoàn thành, bạn sẽ thấy **Saved.pdf** trong thư mục `DWGDrawings` của mình, sẵn sàng để phân phối hoặc lưu trữ.

## Các vấn đề thường gặp & Mẹo

- **Kích thước trang không đúng** – Kiểm tra lại logic chuyển đổi đơn vị; hệ số không khớp có thể tạo ra các trang quá lớn.  
- **Thiếu phông chữ hoặc độ dày đường** – Đảm bảo DWG tham chiếu bất kỳ tài nguyên bên ngoài nào trước khi chuyển đổi.  
- **Hiệu năng với bản vẽ lớn** – Tăng cài đặt `DPI` trong `CadRasterizationOptions` chỉ khi cần chất lượng cao hơn; DPI thấp hơn sẽ tăng tốc xử lý.

## Câu hỏi thường gặp

**Q: Tôi có thể sử dụng Aspose.CAD cho Java với các framework Java khác không?**  
A: Có, Aspose.CAD cho Java tích hợp liền mạch với các framework Java phổ biến như Spring, Jakarta EE và Android.

**Q: Có giấy phép tạm thời cho Aspose.CAD cho Java không?**  
A: Có, bạn có thể nhận giấy phép tạm thời **[here](https://purchase.aspose.com/temporary-license/)**.

**Q: Tôi có thể tìm hỗ trợ cho Aspose.CAD cho Java ở đâu?**  
A: Truy cập **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** để được cộng đồng và kỹ sư Aspose hỗ trợ.

**Q: Làm thế nào để mua giấy phép cho Aspose.CAD cho Java?**  
A: Bạn có thể mua giấy phép **[here](https://purchase.aspose.com/buy)**.

**Q: Aspose.CAD cho Java hỗ trợ những đơn vị nào?**  
A: Aspose.CAD cho Java hỗ trợ cả đơn vị mét và inch, tự động phát hiện hệ thống đơn vị của bản vẽ.

**Q: Tôi có thể chuyển đổi DWG sang các định dạng hình ảnh khác (ví dụ: PNG, JPEG) bằng cùng API không?**  
A: Chắc chắn. Thay `PdfOptions` bằng các tùy chọn hình ảnh raster thích hợp (ví dụ: `PngOptions`) và tái sử dụng cùng `CadRasterizationOptions`.

## Kết luận

Hướng dẫn này đã trình bày cách **export dwg to pdf** và hình raster bằng Aspose.CAD cho Java. Bằng cách làm theo hướng dẫn từng bước, bạn có thể tích hợp chuyển đổi CAD đáng tin cậy vào bất kỳ ứng dụng Java nào, dù bạn cần PDF cho tài liệu hoặc hình raster cho hiển thị trên web.

---

**Cập nhật lần cuối:** 2025-12-18  
**Đã kiểm tra với:** Aspose.CAD for Java 24.10  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}