---
date: 2025-12-09
description: Tìm hiểu cách tạo PDF từ các tệp DWG bằng Aspose.CAD cho Java. Chuyển
  đổi DWG sang PDF một cách dễ dàng với hỗ trợ lưới.
linktitle: Mesh Support in CAD
second_title: Aspose.CAD Java API
title: Tạo PDF từ DWG bằng Aspose.CAD cho Java
url: /vi/java/advanced-cad-features/mesh-support-in-cad/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tạo PDF từ DWG bằng Aspose.CAD cho Java

## Giới thiệu

Trong tutorial này, bạn sẽ học **cách tạo PDF từ DWG** bằng cách sử dụng Aspose.CAD cho Java. Hỗ trợ mesh của thư viện cho phép bạn chuyển đổi các bản vẽ CAD phức tạp—bao gồm cả những bản có mesh 3‑D—trực tiếp sang PDF mà không mất chi tiết. Dù bạn cần **chuyển đổi DWG sang PDF** cho việc báo cáo, lưu trữ, hay xử lý tiếp theo, các bước dưới đây sẽ hướng dẫn bạn một giải pháp đáng tin cậy, sẵn sàng cho môi trường sản xuất.

## Câu trả lời nhanh
- **Nội dung tutorial:** Chuyển đổi một tệp DWG có chứa mesh sang PDF bằng Aspose.CAD cho Java.  
- **Tôi có cần giấy phép không?** Giấy phép tạm thời hoạt động cho việc thử nghiệm; giấy phép đầy đủ cần thiết cho sử dụng thương mại.  
- **Phiên bản Java nào được hỗ trợ?** Java 8 hoặc mới hơn.  
- **Tôi có thể xuất sang các định dạng khác không?** Có – Aspose.CAD cũng hỗ trợ PNG, JPEG, BMP và các định dạng khác.  
- **Quá trình chuyển đổi mất bao lâu?** Thông thường dưới một giây cho các bản vẽ kích thước tiêu chuẩn.

## Cách tạo PDF từ DWG?

Ở dưới đây, bạn sẽ tìm thấy hướng dẫn ngắn gọn, từng bước, dẫn bạn qua toàn bộ quá trình — từ thiết lập dự án đến lưu PDF cuối cùng.

## Yêu cầu trước

- **Môi trường phát triển Java:** JDK 8 hoặc mới hơn được cài đặt trên máy của bạn.  
- **Thư viện Aspose.CAD cho Java:** Tải JAR mới nhất từ [download link](https://releases.aspose.com/cad/java/).  
- **Tài liệu có Meshes:** Một tệp DWG chứa dữ liệu mesh (ví dụ, `meshes.dwg`).  

## Import Namespaces

Trong tệp nguồn Java của bạn, bao gồm các lớp Aspose.CAD cần thiết:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Bước 1: Thiết lập dự án

Tạo dự án Java mới (hoặc thêm vào dự án hiện có) và thêm JAR Aspose.CAD vào classpath của dự án. Xác định thư mục gốc sẽ chứa DWG nguồn và PDF được tạo.

## Bước 2: Xác định đường dẫn tệp

Chỉ định vị trí tệp DWG đầu vào và nơi PDF đầu ra sẽ được ghi.

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "meshes.dwg";
String outPath = dataDir + "meshes.pdf";
```

## Bước 3: Tải hình ảnh CAD

Tải tệp DWG vào đối tượng `CadImage` để Aspose.CAD có thể làm việc với cấu trúc nội bộ của nó.

```java
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## Bước 4: Cấu hình tùy chọn rasterization

Đặt các tùy chọn rasterization để kiểm soát kích thước và bố cục của các trang PDF được tạo. Mảng `Layouts` chỉ cho Aspose.CAD render không gian **Model**, bao gồm các thực thể mesh.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[] { "Model" });
```

## Bước 5: Đặt tùy chọn PDF

Gắn các cài đặt rasterization vào một thể hiện `PdfOptions`. Điều này cho thư viện biết sử dụng các tùy chọn đã định nghĩa trước khi tạo PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Bước 6: Lưu PDF

Cuối cùng, lưu hình ảnh CAD đã tải dưới dạng tệp PDF. Tài liệu kết quả sẽ chứa bản sao trung thực của DWG gốc, bao gồm mọi hình học mesh.

```java
cadImage.save(outPath, pdfOptions);
```

### Tại sao cách này hoạt động cho **chuyển đổi CAD sang PDF**

Aspose.CAD thực hiện rasterization dựa trên vector, giữ nguyên độ dày đường, màu sắc và chi tiết mesh 3‑D. Bằng cách cấu hình các tùy chọn rasterization, bạn kiểm soát độ phân giải và bố cục, đảm bảo rằng **bản vẽ CAD xuất** trông chính xác như mong muốn trong PDF.

## Các trường hợp sử dụng phổ biến

- **Báo cáo tự động:** Tạo báo cáo PDF từ bản vẽ kỹ thuật một cách nhanh chóng.  
- **Lưu trữ tài liệu:** Lưu các bản vẽ CAD dưới dạng PDF để bảo quản lâu dài.  
- **Dịch vụ web:** Cung cấp API nhận tải lên DWG và trả về PDF, hữu ích cho các nền tảng SaaS.  

## Mẹo khắc phục sự cố

- **Mesh bị thiếu trong đầu ra:** Kiểm tra thuộc tính `Layouts` có bao gồm `"Model"` không; mesh thường được lưu trong không gian model.  
- **Tỷ lệ không đúng:** Điều chỉnh `PageWidth` và `PageHeight` để khớp với đơn vị gốc của bản vẽ.  
- **Lỗi giấy phép:** Đảm bảo bạn đã gọi `License.setLicense()` với tệp giấy phép hợp lệ trước khi tải hình ảnh.

## Kết luận

Thông qua việc thực hiện các bước này, bạn có thể đáng tin cậy **chuyển đổi DWG sang PDF** và tận dụng tối đa hỗ trợ mesh của Aspose.CAD. Khả năng này đơn giản hoá quy trình làm việc cần xuất PDF chất lượng cao từ các bản vẽ CAD phức tạp, dù cho mục đích nội bộ hay tài liệu cho khách hàng.

## Câu hỏi thường gặp

### Q1: Aspose.CAD cho Java có phù hợp cho sử dụng thương mại không?

Aspose.CAD cho Java được thiết kế cho cả sử dụng cá nhân và thương mại. Bạn có thể tìm chi tiết giấy phép trên [trang mua hàng](https://purchasepose.com/buy).

### Q2: Làm sao để nhận giấy phép tạm thời cho mục đích thử nghiệm?

Nhận giấy phép tạm thời từ [đây](https://purchase.aspose.com/temporary-license/) để thử nghiệm và đánh giá.

### Q3: Tôi có thể tìm hỗ trợ cộng đồng cho Aspose.CAD cho Java ở đâu?

Truy cập diễn đàn dành riêng cho Aspose.CAD tại [https://forum.aspose.com/c/cad/19](https://forum.aspose.com/c/cad/19) để nhận hỗ trợ cộng đồng.

### Q4: Có các định dạng đầu ra khác ngoài PDF không?

Có, Aspose.CAD cho Java hỗ trợ nhiều định dạng đầu ra, bao gồm PNG, JPEG, BMP và các định dạng khác. Tham khảo tài liệu để biết chi tiết.

### Q5: Tôi có thể dùng thử Aspose.CAD cho Java miễn phí không?

Có, bạn có thể khám phá phiên bản dùng thử miễn phí của Aspose.CAD cho Java [tại đây](https://releases.aspose.com/).

---

**Cập nhật lần cuối:** 2025-12-09  
**Kiểm thử với:** Aspose.CAD cho Java 24.11  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}