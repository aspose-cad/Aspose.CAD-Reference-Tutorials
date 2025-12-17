---
date: 2025-12-10
description: Tìm hiểu cách chuyển đổi CAD sang PDF bằng Aspose.CAD cho Java, đồng
  thời thiết lập kích thước canvas, tự động điều chỉnh tỷ lệ bố cục và xuất ra TIFF.
linktitle: Convert CAD to PDF – Set Canvas Size & Mode
second_title: Aspose.CAD Java API
title: Chuyển CAD sang PDF – Thiết lập kích thước và chế độ canvas (Java)
url: /vi/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Đặt Kích Thước Canvas và Chế Độ

## Giới thiệu

Bạn đang muốn **chuyển đổi CAD sang PDF** đồng thời có toàn quyền kiểm soát kích thước canvas và chế độ render? Hướng dẫn toàn diện này sẽ chỉ cho bạn các bước chính xác để đặt kích thước canvas trong Java, bật tự động thu phóng bố cục, và sau đó xuất kết quả sang cả định dạng PDF và TIFF bằng Aspose.CAD. Dù bạn đang tinh chỉnh một pipeline sản xuất hay thử nghiệm một prototype, bạn sẽ tìm thấy các hướng dẫn rõ ràng, có thể thực hiện ngay tại đây.

## Câu trả lời nhanh
- **“chuyển đổi CAD sang PDF” có nghĩa là gì?** Chuyển đổi bản vẽ CAD (ví dụ: DXF, DWG) thành tài liệu PDF có thể xem trên bất kỳ nền tảng nào.  
- **Tôi có thể xuất sang TIFF không?** Có — sử dụng `TiffOptions` để tạo ảnh raster độ phân giải cao.  
- **Tuỳ chọn nào điều khiển kích thước canvas trong Java?** `CadRasterizationOptions.setPageWidth/Height`.  
- **Tự động thu phóng bố cục là gì?** Một cờ (`setAutomaticLayoutsScaling(true)`) giữ nguyên tỷ lệ bố cục gốc khi kích thước canvas thay đổi.  
- **Có cần giấy phép cho Aspose.CAD không?** Cần một giấy phép tạm thời hoặc vĩnh viễn cho việc sử dụng trong môi trường sản xuất.

## **chuyển đổi CAD sang PDF** là gì?

Chuyển đổi CAD sang PDF có nghĩa là lấy các bản vẽ kỹ thuật dựa trên vector và render chúng thành các trang PDF, giữ nguyên các đường nét, lớp và hình học đồng thời làm cho tệp tin có thể truy cập được trên mọi thiết bị.

## Tại sao phải **đặt kích thước canvas java**?

Việc đặt kích thước canvas trong Java cho phép bạn xác định độ phân giải đầu ra và kích thước trang, đảm bảo rằng PDF hoặc TIFF tạo ra đáp ứng yêu cầu in ấn hoặc hiển thị của bạn. Nó cũng cho phép bạn kiểm soát hành vi thu phóng, điều này rất quan trọng đối với các bản vẽ định dạng lớn.

## Các yêu cầu trước

Trước khi bắt đầu tutorial, hãy chắc chắn rằng bạn đã chuẩn bị các yêu- Aspose.CAD for Java: Đảm bảo bạn đã cài đặt thư viện Aspose.CAD trong môi trường Java. Bạn có thể tải về [tại đây](https://releases.aspose.com/cad/java/).

- Thư mục tài liệu: Tạo một thư mục để lưu trữ các tệp CAD. Thư mục này sẽ được tham chiếu trong các bước tutorial.

Bây giờ, chúng ta cùng bắt đầu với hướng dẫn chi tiết.

## Nhập các Namespace

Trong bước này, chúng ta sẽ nhập các namespace cần thiết để khởi động dự án Aspose.CAD của bạn.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Bước 1: Nhập các lớp Aspose.CAD

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

Trong đoạn mã này, chúng ta thiết lập đường dẫn tới thư mục tài nguyên và tải một tệp DXF bằng lớp `Image` của Aspose.CAD.

## Bước 2: Đặt các thuộc tính **CadRasterizationOptions** (đặt kích thước canvas java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Ở đây, chúng ta tạo một thể hiện của `CadRasterizationOptions` và cấu hình các thuộc tính như chiều rộng trang, chiều cao trang, và **tự động thu phóng bố cục**. Đây là phần cốt lõi của **cấu hình chế độ canvas** cho quá trình chuyển đổi của bạn.

## Bước 3: Tạo PdfOptions và Đặt VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Bây giờ, chúng ta tạo một thể hiện `PdfOptions` và đặt thuộc tính `VectorRasterizationOptions` của nó thành `CadRasterizationOptions` đã cấu hình trước đó.

## Bước 4: Xuất ra PDF (chuyển đổi cad sang pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Cuối cùng, chúng ta lưu ảnh CAD thành tệp PDF bằng các tùy chọn đã chỉ định, hoàn thành quy trình **chuyển đổi CAD sang PDF**.

## Bước 5: Tạo TiffOptions và Đặt VectorRasterizationOptions (xuất cad sang tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Trong bước này, chúng ta thiết lập một thể hiện `TiffOptions` và cấu hình thuộc tính `VectorRasterizationOptions` của nó.

## Bước 6: Xuất ra TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Cuối cùng, chúng ta lưu ảnh CAD thành tệp TIFF bằng các tùy chọn đã chỉ định, minh họa cách **xuất CAD sang TIFF** sau khi đã cấu hình kích thước canvas.

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân | Cách khắc phục |
|-------|-------------|----------------|
| PDF đầu ra trống | `setNoScaling(true)` vô hiệu hoá việc render cho một số bản vẽ | Xóa `setNoScaling(true)` hoặc đặt thành `false`. |
| Độ phân giải TIFF thấp | Chiều rộng/chiều cao trang quá nhỏ | Tăng giá trị `setPageWidth` / `setPageHeight`. |
| Bố cục bị biến dạng | Tự động thu phóng bố cục bị tắt | Đảm bảo `setAutomaticLayoutsScaling(true)` được bật. |

## Kết luận

Chúc mừng! Bạn đã thành công **chuyển đổi CAD sang PDF** và **xuất CAD sang TIFF** đồng thời **đặt kích thước canvas java**, kích hoạt **tự động thu phóng bố cục**, và học cách **cấu hình chế độ canvas** cho các đầu ra chất lượng cao. Tutorial này cung cấp nền tảng vững chắc cho các dự án chuyển đổi CAD của bạn. Khám phá thêm các tính năng và khả năng trong [tài liệu Aspose.CAD](https://reference.aspose.com/cad/java/).

## Câu hỏi thường gặp

### Q1: Tôi có thể dùng Aspose.CAD cho Java với các framework Java khác không?

A1: Có, Aspose.CAD được thiết kế để tích hợp liền mạch với nhiều framework Java.

### Q2: Có giấy phép tạm thời cho Aspose.CAD không?

A2: Có, bạn có thể nhận giấy phép tạm thời [tại đây](https://purchase.aspose.com/temporary-license/).

### Q3: Tôi có thể nhận hỗ trợ cộng đồng cho Aspose.CAD ở đâu?

A3: Truy cập [diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để nhận hỗ trợ và thảo luận cộng đồng.

### Q4: Tôi có thể dùng thử Aspose.CAD miễn phí không?

A4: Chắc chắn! Nhận bản dùng thử miễn phí [tại đây](https://releases.aspose.com/).

### Q5: Làm sao để mua Aspose.CAD cho Java?

A5: Mua sản phẩm [tại đây](https://purchase.aspose.com/buy).

**Câu hỏi & Trả lời bổ sung**

**Hỏi: Kích thước canvas có ảnh hưởng đến chất lượng vector trong PDF không?**  
Đáp: Không. Kích thước canvas chỉ điều khiển kích thước trang; dữ liệu vector vẫn độc lập với độ phân giải, đảm bảo hiển thị sắc nét ở bất kỳ mức thu phóng nào.

**Hỏi: Tôi có thể đặt DPI khác cho đầu ra TIFF không?**  
Đáp: Có. Điều chỉnh `rasterizationOptions.setResolution(dpiValue)` trước khi tạo `TiffOptions`.

---

**Cập nhật lần cuối:** 2025-12-10  
**Đã kiểm tra với:** Aspose.CAD for Java 24.12  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}