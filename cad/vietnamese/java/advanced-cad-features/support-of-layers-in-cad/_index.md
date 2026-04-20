---
date: 2026-02-17
description: Tìm hiểu cách lưu DWG thành JPEG trong Java bằng Aspose.CAD, thêm nhiều
  lớp và điều chỉnh kích thước CAD để chuyển đổi hình ảnh một cách chính xác.
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: Lưu DWG dưới dạng JPEG với hỗ trợ lớp trong Java
url: /vi/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lưu DWG dưới dạng JPEG với Hỗ trợ Lớp trong Java

## Giới thiệu

Trong hướng dẫn này, bạn sẽ khám phá cách **lưu DWG dưới dạng JPEG** đồng thời tận dụng tối đa tính năng hỗ trợ lớp trong Aspose.CAD cho Java. Các lớp cho phép bạn cô lập các phần cụ thể của bản vẽ, giúp dễ dàng xuất ra chỉ những gì bạn cần. Chúng tôi sẽ hướng dẫn từng bước, từ việc thiết lập môi trường đến xuất JPEG chỉ bao gồm các lớp bạn chọn.

## Trả lời nhanh
- **“Lưu DWG dưới dạng JPEG” có nghĩa là gì?** Nó chuyển đổi bản vẽ DWG (hoặc CAD khác) thành ảnh raster JPEG.  
- **Tôi có thể chỉ bao gồm các lớp đã chọn không?** Có – sử dụng phương thức `setLayers` để chỉ định các lớp cần render.  
- **Làm sao thay đổi kích thước ảnh?** Điều chỉnh `setPageWidth` và `setPageHeight` trong `CadRasterizationOptions`.  
- **Đây có phải là giải pháp chỉ dành cho Java không?** Ví dụ sử dụng Aspose.CAD cho Java, nhưng cùng khái niệm áp dụng cho các ngôn ngữ khác.  
- **Có cần giấy phép không?** Bản dùng thử miễn phí đủ cho việc thử nghiệm; giấy phép thương mại cần thiết cho môi trường sản xuất.

## “Lưu DWG dưới dạng JPEG” là gì?
Lưu DWG dưới dạng JPEG có nghĩa là raster hoá một tệp CAD dựa trên vector (DWG, DWF, DXF, v.v.) thành một bitmap JPEG tiêu chuẩn. Điều này hữu ích khi bạn cần nhúng bản vẽ CAD vào các trang web, email hoặc báo cáo chỉ hỗ trợ ảnh raster.

## Tại sao nên chuyển đổi JPEG có nhận thức lớp?
- **Tập trung vào dữ liệu liên quan:** Xuất chỉ các lớp bạn cần, giảm kích thước tệp và giảm nhiễu thị giác.  
- **Giữ nguyên ý định thiết kế:** Các lớp bảo tồn việc nhóm logic các đối tượng, cho phép bạn tái sử dụng cùng một tệp nguồn cho các đầu ra khác nhau.  
- **Kiểm soát hoàn toàn kích thước:** Bằng cách điều chỉnh các tùy chọn raster hoá, bạn có thể tạo ra ảnh độ phân giải cao phù hợp với yêu cầu xuất bản của mình.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn bạn đã có:

1. **Thư viện Aspose.CAD cho Java** – tải về từ [website](https://releases.aspose.com/cad/java/). Thực hiện hướng dẫn cài đặt để thêm các tệp JAR vào classpath của dự án.  
2. **Môi trường phát triển Java** – JDK mới (phiên bản 8 trở lên) đã được cài đặt trên máy tính của bạn.

Sau khi đã sẵn sàng, chúng ta sẽ khám phá mã cần thiết để **lưu DWG dưới dạng JPEG** với việc render lớp chọn lọc.

## Nhập không gian tên

Bắt đầu bằng cách nhập các lớp Aspose.CAD cần thiết và các tiện ích chuẩn của Java:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## Hướng dẫn từng bước

### Bước 1: Thiết lập đường dẫn tệp

Xác định vị trí tệp DWF nguồn và nơi sẽ ghi tệp JPEG đầu ra.

```java
String dataDir = "Your Document Directory" + "DWFDrawings/";
String srcFile = dataDir + "for_layers_test.dwf";
String outFile = dataDir + "for_layers_test.jpg";
```

### Bước 2: Tải ảnh DWF

Sử dụng phương thức `Image.load` của Aspose.CAD để đọc bản vẽ CAD.

```java
Image image = Image.load(srcFile);
```

### Bước 3: Cấu hình tùy chọn raster hoá (Điều chỉnh kích thước CAD)

Tạo một thể hiện `CadRasterizationOptions` và đặt kích thước đầu ra mong muốn. Thay đổi các giá trị này cho phép bạn **điều chỉnh kích thước CAD** cho JPEG cuối cùng.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Bước 4: Chỉ định các lớp (Thêm nhiều lớp)

Nếu muốn render hơn một lớp, chỉ cần thêm tên chúng vào danh sách. Ở đây chúng ta bắt đầu với một lớp duy nhất có tên “LayerA”.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*Mẹo chuyên nghiệp:* Để **thêm nhiều lớp**, mở rộng lời gọi `Arrays.asList`, ví dụ `Arrays.asList("LayerA", "LayerB", "LayerC")`. Điều này cho phép bạn **chọn các lớp CAD cụ thể** cho quá trình chuyển đổi.

### Bước 5: Cấu hình tùy chọn JPEG (Java Chuyển đổi Ảnh CAD)

Liên kết các cài đặt raster hoá với định dạng đầu ra JPEG.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Bước 6: Xuất ra JPG (Lưu DWG dưới dạng JPEG)

Cuối cùng, ghi ảnh ra đĩa. Bước này **lưu bản vẽ CAD dưới dạng tệp JPEG** chỉ chứa các lớp đã chọn.

```java
image.save(outFile, jpegOptions);
```

Bằng cách thực hiện các bước trên, bạn đã thành công **lưu DWG dưới dạng JPEG** đồng thời kiểm soát các lớp xuất hiện và tùy chỉnh kích thước ảnh.

## Cách chuyển đổi DWF sang JPEG với lựa chọn lớp

Mặc dù ví dụ sử dụng nguồn DWF, cùng quy trình raster hoá hoạt động cho bất kỳ định dạng CAD nào được hỗ trợ (DWG, DXF, DGN, v.v.). Chỉ cần thay đổi phần mở rộng tệp trong `srcFile` và thư viện sẽ tự động thực hiện **chuyển đổi DWF sang JPEG** (hoặc định dạng khác).

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Giải pháp |
|-------|----------|
| **Các lớp không hiển thị** | Kiểm tra xem tên lớp có khớp chính xác với những gì được lưu trong tệp DWF không (phân biệt chữ hoa/thường). |
| **Ảnh đầu ra trắng** | Đảm bảo `setPageWidth` và `setPageHeight` đủ lớn cho phạm vi của bản vẽ. |
| **Ngoại lệ giấy phép** | Sử dụng giấy phép dùng thử để thử nghiệm; mua giấy phép đầy đủ cho môi trường sản xuất. |

## Câu hỏi thường gặp

**H: Tôi có thể thêm nhiều lớp vào tùy chọn raster hoá không?**  
Đ: Chắc chắn. Mở rộng `stringList` với các tên lớp bổ sung, ví dụ `Arrays.asList("LayerA", "LayerB")`.

**H: Aspose.CAD có tương thích với các định dạng CAD khác không?**  
Đ: Có, nó hỗ trợ DWG, DXF, DWF và nhiều định dạng khác.

**H: Làm sao thay đổi kích thước ảnh đầu ra?**  
Đ: Sửa `setPageWidth` và `setPageHeight` trong thể hiện `CadRasterizationOptions`.

**H: Tôi có thể mua giấy phép cho Aspose.CAD ở đâu?**  
Đ: Bạn có thể khám phá các tùy chọn mua giấy phép [tại đây](https://purchase.aspose.com/buy).

**H: Tôi có thể nhận hỗ trợ cộng đồng ở đâu?**  
Đ: Tham gia cộng đồng Aspose.CAD trên [diễn đàn](https://forum.aspose.com/c/cad/19) để được trợ giúp và thảo luận.

---

**Cập nhật lần cuối:** 2026-02-17  
**Đã kiểm tra với:** Aspose.CAD cho Java 24.11  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}