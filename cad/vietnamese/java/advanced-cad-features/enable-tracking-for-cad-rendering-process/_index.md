---
date: 2025-12-07
description: Học cách đặt kích thước trang PDF khi chuyển CAD sang PDF bằng Aspose.CAD
  cho Java. Thực hiện theo hướng dẫn từng bước này để bật theo dõi, chuyển CAD sang
  PDF và lưu CAD dưới dạng PDF một cách hiệu quả.
language: vi
linktitle: Set PDF Page Size – Enable Tracking for CAD Rendering
second_title: Aspose.CAD Java API
title: Cách thiết lập kích thước trang PDF và bật theo dõi cho quá trình render CAD
url: /java/advanced-cad-features/enable-tracking-for-cad-rendering-process/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Kích hoạt Theo dõi cho Quy trình Render CAD

## Giới thiệu

Trong hướng dẫn này, bạn sẽ học cách **đặt kích thước trang PDF** khi **chuyển đổi CAD sang PDF** bằng **Aspose.CAD for Java**. Bằng cách bật theo dõi, bạn sẽ có được cái nhìn toàn diện về quy trình render, giúp việc gỡ lỗi và tối ưu chuyển đổi từ các tệp CAD (như DXF) sang PDF trở nên dễ dàng hơn. Dù bạn cần **lưu CAD dưới dạng PDF**, tạo PDF từ DXF, hay chỉ đơn giản kiểm soát kích thước đầu ra, các bước dưới đây sẽ hướng dẫn bạn toàn bộ quá trình.

## Câu trả lời nhanh
- **“set PDF page size” làm gì?** Nó xác định chiều rộng và chiều cao của trang PDF kết quả trong quá trình render CAD.  
- **Tại sao cần bật theo dõi?** Theo dõi ghi lại mỗi giai đoạn của quá trình chuyển đổi, giúp bạn phát hiện các nút thắt hiệu năng hoặc lỗi.  
- **Tôi có cần giấy phép không?** Bản dùng thử miễn phí đủ cho việc đánh giá; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Các định dạng CAD nào được hỗ trợ?** DWG, DXF, DGN và nhiều định dạng khác – xem tài liệu Aspose.CAD để biết danh sách đầy đủ.  
- **Tôi có thể thay đổi kích thước trang ngay lập tức không?** Có – chỉ cần điều chỉnh các giá trị `PageWidth` và `PageHeight` trong `CadRasterizationOptions`.

## “set PDF page size” trong render CAD là gì?

Việc đặt kích thước trang PDF cho rasterizer biết canvas cần lớn bao nhiêu khi dữ liệu CAD vector được raster hoá thành một trang PDF. Điều này rất quan trọng để duy trì độ trung thực hình ảnh, đặc biệt với các bản vẽ kỹ thuật chi tiết.

## Tại sao cần bật theo dõi cho render CAD?

Bật theo dõi cung cấp một nhật ký chi tiết của mỗi bước — từ tải tệp nguồn đến ghi file PDF đầu ra. Nó giúp bạn:

- Chẩn đoán lý do một bản vẽ cụ thể có thể render không đúng.  
- Đo thời gian thực hiện mỗi giai đoạn, hữu ích cho việc tinh chỉnh hiệu năng.  
- Xác nhận rằng kích thước trang bạn đã cấu hình thực sự được áp dụng.

## Yêu cầu trước

Trước khi thiết lập theo dõi, hãy đảm bảo bạn đã có các yêu cầu sau:

1. **Môi trường phát triển Java** – Java 8 trở lên đã được cài đặt trên máy tính.  
2. **Thư viện Aspose.CAD** – Tải và tích hợp thư viện Aspose.CAD vào dự án Java của bạn. Bạn có thể tìm liên kết tải về [tại đây](https://releases.aspose.com/cad/java/).  
3. **Thư mục Tài liệu** – Chuẩn bị một thư mục để lưu trữ các tệp CAD và các PDF được tạo.

## Nhập không gian tên

Trong dự án Java, nhập các không gian tên cần thiết để tận dụng các chức năng của Aspose.CAD. Thêm các dòng sau vào đầu mã nguồn của bạn:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;

import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Đặt Đường dẫn Thư mục Tài nguyên

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Thay thế `"Your Document Directory"` bằng đường dẫn thực tế tới thư mục tài liệu của bạn.

## Tải tệp CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

Xác định đường dẫn tới tệp CAD của bạn, đảm bảo nó nằm trong thư mục tài liệu đã chỉ định.

## Đặt tùy chọn xuất PDF

```java
OutputStream stream = new FileOutputStream(dataDir + "conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
```

Tạo một luồng đầu ra và thiết lập các tùy chọn PDF cho quá trình chuyển đổi.

## Cấu hình CadRasterizationOptions (Set PDF Page Size)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

Ở đây chúng ta **đặt kích thước trang PDF** bằng cách định nghĩa `PageWidth` và `PageHeight`. Điều chỉnh các giá trị này để phù hợp với kích thước yêu cầu cho bản vẽ kỹ thuật của bạn. Bước này ảnh hưởng trực tiếp đến cách nội dung CAD được thu phóng và render trong PDF cuối cùng.

## Lưu tệp PDF

```java
image.save(stream, pdfOptions);
```

Lưu file PDF đã render với các tùy chọn đã chỉ định.

## Xác nhận việc bật theo dõi

```java
System.out.println("Tracking enabled successfully for CAD rendering process.");
```

Xác nhận rằng việc theo dõi đã được bật thành công cho quy trình render CAD.

## Các vấn đề thường gặp & Khắc phục

| Triệu chứng | Nguyên nhân có thể | Cách khắc phục |
|------------|--------------------|----------------|
| Trang PDF xuất hiện trắng | `PageWidth`/`PageHeight` được đặt thành 0 | Đảm bảo cung cấp các kích thước khác 0. |
| File đầu ra bị hỏng | Luồng đầu ra chưa được đóng | Gọi `stream.close()` sau `image.save(...)`. |
| Các lớp bị thiếu trong PDF | Tệp CAD sử dụng các thực thể không được hỗ trợ | Kiểm tra xem định dạng tệp có được Aspose.CAD hỗ trợ đầy đủ không. |

## Câu hỏi thường gặp

### Q1: Aspose.CAD có tương thích với tất cả các định dạng tệp CAD không?

A1: Aspose.CAD hỗ trợ một loạt các định dạng CAD, bao gồm DWG, DXF, DGN và nhiều hơn nữa. Tham khảo [tài liệu](https://reference.aspose.com/cad/java/) để biết danh sách chi tiết.

### Q2: Tôi có thể tùy chỉnh kích thước đầu ra của file PDF không?

A2: Chắc chắn! Điều chỉnh các tham số `PageWidth` và `PageHeight` trong `CadRasterizationOptions` để phù hợp với kích thước mong muốn.

### Q3: Có bản dùng thử miễn phí cho Aspose.CAD for Java không?

A3: Có, bạn có thể khám phá các tính năng của Aspose.CAD bằng cách lấy bản dùng thử miễn phí [tại đây](https://releases.aspose.com/).

### Q4: Làm sao tôi có thể nhận hỗ trợ cộng đồng cho các câu hỏi liên quan đến Aspose.CAD?

A4: Truy cập [diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để giao lưu với cộng đồng và nhận trợ giúp.

### Q5: Có giấy phép tạm thời cho Aspose.CAD không?

A5: Có, nếu bạn cần giấy phép tạm thời, bạn có thể mua [tại đây](https://purchase.aspose.com/temporary-license/).

## Kết luận

Chúc mừng! Bạn đã học cách **đặt kích thước trang PDF** và bật theo dõi cho quá trình render CAD bằng **Aspose.CAD for Java**. Hướng dẫn này giúp bạn **chuyển đổi CAD sang PDF**, **lưu CAD dưới dạng PDF**, và tạo PDF từ DXF với kiểm soát đầy đủ kích thước trang và nhật ký thực thi chi tiết. Hãy thử nghiệm với các kích thước trang khác nhau và khám phá thêm các tùy chọn rasterization để phù hợp với quy trình kỹ thuật của bạn.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Cập nhật lần cuối:** 2025-12-07  
**Kiểm tra với:** Aspose.CAD for Java 24.12 (phiên bản mới nhất tại thời điểm viết)  
**Tác giả:** Aspose  

---