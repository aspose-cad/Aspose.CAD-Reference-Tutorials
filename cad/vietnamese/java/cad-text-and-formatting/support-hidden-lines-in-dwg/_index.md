---
date: 2026-01-02
description: Tìm hiểu cách xuất DWG sang PDF, bật các đường ẩn và chuyển đổi DWG sang
  PDF bằng Aspose.CAD cho Java trong hướng dẫn từng bước này.
linktitle: Export DWG as PDF with Hidden Lines Using Java
second_title: Aspose.CAD Java API
title: Xuất DWG sang PDF với các đường ẩn – Aspose.CAD cho Java
url: /vi/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xuất DWG thành PDF với Đường ẩn – Aspose.CAD cho Java

## Giới thiệu

Trong hướng dẫn này, bạn sẽ học cách **export DWG as PDF** trong khi giữ nguyên các đường ẩn bằng Aspose.CAD cho Java. Cho dù bạn cần **convert DWG to PDF**, tạo một hướng dẫn kiểu **dwg to pdf tutorial**, hoặc chỉ đơn giản **save DWG as PDF** có hỗ trợ đường ẩn, chúng tôi sẽ hướng dẫn bạn từng bước. Khi hoàn thành, bạn sẽ có một giải pháp sẵn sàng sử dụng mà bạn có thể tích hợp vào bất kỳ dự án Java nào.

## Câu trả lời nhanh
- **Mục tiêu của hướng dẫn này là gì?** Kích hoạt việc render đường ẩn khi xuất DWG sang PDF bằng Aspose.CAD cho Java.  
- **Hoạt động chính được thực hiện là gì?** `export dwg as pdf`.  
- **Tôi có cần giấy phép không?** Bản dùng thử miễn phí hoạt động cho việc thử nghiệm; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Các yêu cầu tiên quyết là gì?** Môi trường phát triển Java, thư viện Aspose.CAD cho Java, và các tệp DWG.  
- **Thời gian triển khai mất bao lâu?** Khoảng 10‑15 phút cho một cấu hình cơ bản.

## “export dwg as pdf” là gì?
Việc xuất một tệp DWG sang PDF chuyển đổi bản vẽ CAD dựa trên vector thành định dạng tài liệu di động trong khi giữ nguyên các lớp, kiểu đường và tùy chọn render đường ẩn. Điều này giúp dễ dàng chia sẻ thiết kế CAD với các bên liên quan có thể không có phần mềm CAD.

## Tại sao bật đường ẩn khi xuất?
Đường ẩn cung cấp một hình ảnh trực quan rõ ràng hơn cho các mô hình 3D phức tạp trên trang 2‑D, đảm bảo chỉ các cạnh hiển thị được nhấn mạnh. Điều này cải thiện khả năng đọc và thường được yêu cầu trong tài liệu kỹ thuật.

## Yêu cầu tiên quyết

1. **Aspose.CAD for Java** – tải thư viện từ trang chính thức [here](https://releases.aspose.com/cad/java/).  
2. **DWG files** – có các bản vẽ DWG nguồn được lưu trong một thư mục đã biết.  
3. **Java development environment** – JDK 8+ và IDE ưa thích của bạn (Eclipse, IntelliJ, v.v.).  

Bây giờ bạn đã sẵn sàng, hãy bắt đầu vào phần mã.

## Nhập các không gian tên

Bắt đầu bằng việc nhập các lớp cần thiết để bạn có thể làm việc với hình ảnh CAD và tùy chọn PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## Bước 1: Thiết lập dự án của bạn

Tạo một dự án Java và thêm tệp JAR Aspose.CAD vào đường dẫn biên dịch. Sau đó xác định thư mục chứa các tệp DWG của bạn.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **Mẹo chuyên nghiệp:** Sử dụng đường dẫn tuyệt đối hoặc cấu hình đường dẫn tương đối dựa trên thư mục tài nguyên của dự án.

## Bước 2: Tải tệp DWG

Tải tệp DWG nguồn vào một đối tượng `CadImage` để bạn có thể thao tác với nó.

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## Bước 3: Cấu hình tùy chọn rasterization

Chọn các lớp bạn muốn bao gồm và đặt kích thước trang sao cho khớp với bản vẽ gốc. Đây là nơi chúng ta bật render đường ẩn bằng cách chỉ định bố cục.

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## Bước 4: Đặt tùy chọn PDF

Yêu cầu Aspose.CAD raster hóa dữ liệu vector thành PDF, sử dụng bố cục “Model” để giữ các đường ẩn ở trạng thái ẩn.

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Bước 5: Lưu kết quả

Cuối cùng, xuất DWG thành tệp PDF. Các đường ẩn sẽ được tôn trọng theo bố cục bạn đã thiết lập.

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **Cạm bẫy phổ biến:** Quên đặt bố cục thành `"Model"` sẽ khiến tất cả các đường (kể cả đường ẩn) xuất hiện liền mạch trong PDF.

## Kết luận

Bạn đã có một phương pháp hoàn chỉnh, sẵn sàng cho sản xuất để **export dwg as pdf** với hỗ trợ đường ẩn bằng Aspose.CAD cho Java. Cách tiếp cận này có thể được tích hợp vào công cụ xử lý hàng loạt, dịch vụ web, hoặc ứng dụng desktop để tự động hoá việc chuyển đổi CAD sang PDF.

## Câu hỏi thường gặp

### Q1: Tôi có thể sử dụng Aspose.CAD cho Java với các định dạng tệp CAD khác không?
A1: Có, Aspose.CAD hỗ trợ nhiều định dạng CAD như DWG, DXF, DWF và nhiều hơn nữa.

### Q2: Có bản dùng thử miễn phí cho Aspose.CAD cho Java không?
A2: Có, bạn có thể tìm bản dùng thử miễn phí [here](https://releases.aspose.com/).

### Q3: Làm sao tôi có thể nhận hỗ trợ cho Aspose.CAD cho Java?
A3: Truy cập diễn đàn Aspose.CAD [here](https://forum.aspose.com/c/cad/19) để nhận hỗ trợ cộng đồng.

### Q4: Tôi có thể tìm tài liệu chi tiết cho Aspose.CAD cho Java ở đâu?
A4: Tham khảo tài liệu [here](https://reference.aspose.com/cad/java/).

### Q5: Tôi có thể mua giấy phép tạm thời cho Aspose.CAD cho Java không?
A5: Có, bạn có thể nhận giấy phép tạm thời [here](https://purchase.aspose.com/temporary-license/).

### Q6: Phương pháp này có hoạt động cho việc chuyển đổi DWG sang PDF trong môi trường server không giao diện (headless) không?
A6: Chắc chắn. Vì mã chỉ sử dụng API của Aspose.CAD, nên nó chạy mà không cần bất kỳ phụ thuộc UI nào, rất phù hợp cho tự động hoá phía server.

---

**Last Updated:** 2026-01-02  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}