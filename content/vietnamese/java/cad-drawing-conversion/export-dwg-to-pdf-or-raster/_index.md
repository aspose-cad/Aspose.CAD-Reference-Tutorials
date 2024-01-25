---
title: Xuất DWG sang PDF hoặc Raster bằng Aspose.CAD cho Java
linktitle: Xuất DWG sang PDF hoặc Raster
second_title: API Java Aspose.CAD
description: Khám phá quy trình liền mạch xuất tệp DWG sang PDF hoặc hình ảnh raster trong Java bằng Aspose.CAD. Hướng dẫn từng bước này đảm bảo độ chính xác và hiệu quả.
type: docs
weight: 13
url: /vi/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
---
## Giới thiệu

Trong thế giới năng động của thiết kế có sự hỗ trợ của máy tính (CAD), việc xử lý hiệu quả các bản vẽ là rất quan trọng. Aspose.CAD cho Java cung cấp một giải pháp mạnh mẽ để xuất tệp DWG sang PDF hoặc hình ảnh raster. Hướng dẫn này sẽ hướng dẫn bạn trong suốt quy trình, đảm bảo bạn khai thác toàn bộ tiềm năng của Aspose.CAD cho Java.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có những điều sau:

- Hiểu biết cơ bản về lập trình Java.
-  Đã cài đặt thư viện Aspose.CAD cho Java. Nếu không thì tải về[đây](https://releases.aspose.com/cad/java/).
- Một tệp DWG cho mục đích thử nghiệm. Bạn có thể sử dụng tệp "Bottom_plate.dwg" được cung cấp.

## Nhập không gian tên

Trong dự án Java của bạn, hãy nhập các vùng tên cần thiết để bắt đầu quá trình:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Bước 1: Tải tệp DWG

 Bắt đầu bằng cách tải tệp DWG của bạn bằng Aspose.CAD's`Image` lớp học:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## Bước 2: Xác định loại đơn vị

Tiếp theo, kiểm tra loại đơn vị của tệp DWG được tải:

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

## Bước 3: Đặt tùy chọn rasterization

Dựa trên loại đơn vị, hãy định cấu hình các tùy chọn tạo điểm ảnh:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Đơn vị hệ mét
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // đơn vị hoàng gia
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

## Bước 4: Định cấu hình tùy chọn PDF

Thiết lập tùy chọn xuất PDF:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## Bước 5: Lưu dưới dạng PDF

Cuối cùng, lưu tệp DWG dưới dạng PDF:

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Và bạn có nó rồi đấy! Bạn đã xuất thành công tệp DWG sang PDF bằng Aspose.CAD cho Java.

## Phần kết luận

Hướng dẫn này cung cấp hướng dẫn từng bước về cách tận dụng Aspose.CAD cho Java để xuất tệp DWG sang PDF hoặc hình ảnh raster. Thư viện này đơn giản hóa quy trình, cho phép bạn xử lý hiệu quả các bản vẽ CAD trong các ứng dụng Java của mình.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.CAD cho Java với các khung Java khác không?

Câu trả lời 1: Có, Aspose.CAD dành cho Java tích hợp liền mạch với các khung công tác Java phổ biến.

### Câu hỏi 2: Giấy phép tạm thời có sẵn cho Aspose.CAD cho Java không?

 A2: Có, bạn có thể xin giấy phép tạm thời[đây](https://purchase.aspose.com/temporary-license/).

### Câu hỏi 3: Tôi có thể tìm hỗ trợ cho Aspose.CAD cho Java ở đâu?

 A3: Tham quan[Diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để được sự giúp đỡ từ cộng đồng.

### Câu hỏi 4: Làm cách nào tôi có thể mua giấy phép Aspose.CAD cho Java?

 A4: Bạn có thể mua giấy phép[đây](https://purchase.aspose.com/buy).

### Câu hỏi 5: Aspose.CAD cho Java hỗ trợ những đơn vị nào?

Câu trả lời 5: Aspose.CAD cho Java hỗ trợ cả đơn vị hệ mét và hệ đo lường Anh.