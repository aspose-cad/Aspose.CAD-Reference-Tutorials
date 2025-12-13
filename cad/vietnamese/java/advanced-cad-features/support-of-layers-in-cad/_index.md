---
date: 2025-12-13
description: Tìm hiểu cách lưu CAD thành JPEG trong Java bằng Aspose.CAD, thêm nhiều
  lớp và điều chỉnh kích thước CAD để chuyển đổi hình ảnh một cách chính xác.
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: Lưu CAD dưới dạng JPEG với hỗ trợ lớp trong Java
url: /vi/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lưu CAD dưới dạng JPEG với Hỗ trợ Lớp trong Java

## Giới thiệu

Trong hướng dẫn này, bạn sẽ khám phá cách **lưu CAD dưới dạng JPEG** đồng thời tận dụng tối đa hỗ trợ lớp trong Aspose.CAD cho Java. Các lớp cho phép bạn cô lập các phần cụ thể của bản vẽ, giúp dễ dàng xuất chỉ những gì bạn cần. Chúng tôi sẽ hướng dẫn từng bước, từ thiết lập môi trường đến xuất JPEG chỉ bao gồm các lớp bạn chọn.

## Câu trả lời nhanh
- **“save CAD as JPEG” có nghĩa là gì?** Nó chuyển đổi bản vẽ CAD thành một hình ảnh raster JPEG.  
- **Tôi có thể chỉ bao gồm các lớp đã chọn không?** Có – sử dụng phương thức `setLayers` để chỉ định các lớp cần render.  
- **Làm thế nào để thay đổi kích thước hình ảnh?** Điều chỉnh `setPageWidth` và `setPageHeight` trong `CadRasterizationOptions`.  
- **Đây có phải là giải pháp chỉ dành cho Java không?** Ví dụ sử dụng Aspose.CAD cho Java, nhưng các khái niệm tương tự áp dụng cho các ngôn ngữ khác.  
- **Tôi có cần giấy phép không?** Bản dùng thử miễn phí hoạt động cho việc thử nghiệm; giấy phép thương mại cần thiết cho môi trường sản xuất.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn có những thứ sau:

1. **Aspose.CAD for Java Library** – tải xuống từ [website](https://releases.aspose.com/cad/java/). Thực hiện hướng dẫn cài đặt để thêm các tệp JAR vào classpath của dự án.  
2. **Java Development Environment** – một JDK mới (phiên bản 8 trở lên) được cài đặt trên máy của bạn.

Bây giờ chúng ta đã sẵn sàng, hãy khám phá mã cần thiết để **lưu CAD dưới dạng JPEG** với việc render lớp chọn lọc.

## Nhập các namespace

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

### Bước 3: Cấu hình tùy chọn rasterization (Điều chỉnh kích thước CAD)

Tạo một thể hiện `CadRasterizationOptions` và đặt kích thước đầu ra mong muốn. Thay đổi các giá trị này cho phép bạn **điều chỉnh kích thước CAD** cho JPEG cuối cùng.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Bước 4: Chỉ định các lớp (Thêm nhiều lớp)

Nếu bạn muốn render nhiều hơn một lớp, chỉ cần thêm tên của chúng vào danh sách. Ở đây chúng ta bắt đầu với một lớp duy nhất có tên “LayerA”.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*Mẹo chuyên nghiệp:* Để **thêm nhiều lớp**, mở rộng lời gọi `Arrays.asList`, ví dụ, `Arrays.asList("LayerA", "LayerB", "LayerC")`.

### Bước 5: Cấu hình tùy chọn JPEG (Java Convert CAD Image)

Liên kết các cài đặt rasterization với định dạng đầu ra JPEG.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Bước 6: Xuất ra JPG (Lưu CAD dưới dạng JPEG)

Cuối cùng, ghi hình ảnh ra đĩa. Bước này **lưu bản vẽ CAD dưới dạng tệp JPEG** chỉ chứa các lớp đã chọn.

```java
image.save(outFile, jpegOptions);
```

Bằng cách thực hiện các bước này, bạn đã thành công **lưu CAD dưới dạng JPEG** đồng thời kiểm soát các lớp hiển thị và tùy chỉnh kích thước hình ảnh.

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Giải pháp |
|-------|----------|
| **Layers not appearing** | Xác minh rằng tên lớp khớp chính xác với những gì được lưu trong tệp DWF (phân biệt chữ hoa‑thường). |
| **Output image is blank** | Đảm bảo `setPageWidth` và `setPageHeight` đủ lớn cho phạm vi của bản vẽ. |
| **License exception** | Sử dụng giấy phép dùng thử cho việc thử nghiệm; mua giấy phép đầy đủ cho môi trường sản xuất. |

## Câu hỏi thường gặp

**Q: Tôi có thể thêm nhiều lớp vào tùy chọn rasterization không?**  
A: Chắc chắn. Mở rộng `stringList` với các tên lớp bổ sung, ví dụ, `Arrays.asList("LayerA", "LayerB")`.

**Q: Aspose.CAD có tương thích với các định dạng CAD khác không?**  
A: Có, nó hỗ trợ DWG, DXF, DWF và nhiều định dạng khác.

**Q: Làm thế nào để thay đổi kích thước ảnh đầu ra?**  
A: Thay đổi `setPageWidth` và `setPageHeight` trong thể hiện `CadRasterizationOptions`.

**Q: Tôi có thể mua giấy phép cho Aspose.CAD ở đâu?**  
A: Bạn có thể khám phá các tùy chọn giấy phép [tại đây](https://purchase.aspose.com/buy).

**Q: Tôi có thể nhận hỗ trợ cộng đồng ở đâu?**  
A: Tham gia cộng đồng Aspose.CAD trên [forum](https://forum.aspose.com/c/cad/19) để được trợ giúp và thảo luận.

---

**Last Updated:** 2025-12-13  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}