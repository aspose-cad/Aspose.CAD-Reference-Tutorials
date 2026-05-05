---
date: 2026-01-22
description: Tìm hiểu cách tạo PDF từ bản vẽ CAD, chuyển đổi DWG sang PDF và tùy chỉnh
  kích thước trang PDF bằng Aspose.CAD cho Java.
linktitle: Single PDF with Different Layouts
second_title: Aspose.CAD Java API
title: Cách tạo PDF từ bản vẽ CAD bằng Aspose.CAD cho Java
url: /vi/java/other-cad-operations/single-pdf-different-layouts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách Tạo PDF Từ Bản Vẽ CAD Bằng Aspose.CAD cho Java

## Giới thiệu

Trong hướng dẫn này, bạn sẽ khám phá **cách tạo PDF từ bản vẽ CAD** bằng thư viện Aspose.CAD cho Java. Dù bạn cần **chuyển đổi DWG sang PDF**, xuất một tệp CAD phức tạp, hay áp dụng **kích thước trang PDF tùy chỉnh**, các bước dưới đây sẽ hướng dẫn bạn qua một giải pháp lập trình sạch sẽ. Hãy cùng đi qua quy trình, để bạn có thể tạo một tệp PDF duy nhất chứa nhiều trang layout—tất cả chỉ với vài dòng mã Java.

## Câu trả lời nhanh
- **Aspose.CAD làm gì?** Nó cho phép các nhà phát triển Java tải, thao tác và xuất bản vẽ CAD sang các định dạng như PDF.
- **Tôi có thể xuất nhiều layout vào một PDF không?** Có, bằng cách tùy chỉnh kích thước trang layout trước khi lưu.
- **Các định dạng CAD nào được hỗ trợ?** DWG, DXF, DWF, DGN và nhiều hơn nữa.
- **Có cần giấy phép cho môi trường sản xuất không?** Giấy phép tạm thời hoạt động cho việc thử nghiệm; giấy phép đầy đủ cần thiết cho sử dụng thương mại.
- **Yêu cầu phiên bản Java nào?** Java 8 hoặc mới hơn.

## “Tạo PDF từ CAD” là gì?
Tạo PDF từ CAD có nghĩa là raster hoá các bản vẽ CAD dựa trên vector thành một tài liệu bố cục cố định (PDFốc.
- **Kiy chọn raster hoá như DPI, kích thước trang và lựa chọn layout.
- **Xử lý hàng loạt** – xử lý nhiều bản vẽ trong một lần chạy.
- **Chuyển đổi chính xác** – giữ nguyên độ dày đường, màu sắc và lớp.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn bạn có:

- **Môi trường Java** – JDK 8 hoặc mới hơn đã được cài đặt.
- **Thư viện Aspose.CAD** – Tải và cài đặt thư viện Aspose.CAD cho Java từ [liên kết tải xuống](https://releases.aspose.com/cad/java/).
- **Thư mục tài liệu** – Một thư mục chứa các bản vẽ DWG (hoặc CAD khác) mà bạn muốn chuyển đổi.

## Nhập gói

Trong dự án Java của bạn, nhập các lớp cần thiết:

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## Hướng dẫn từng bước

### Bước 1: Tải bản vẽ CAD

Đầu tiên, tải tệp CAD nguồn (ví dụ: DWG) vào một đối tượng `CadImage`. Đây là điểm khởi đầu cho bất kỳ hoạt động **xuất CAD sang PDF** nào.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

### Bước 2: Cấu hình tùy chọn raster hoá

Xác định cách dữ liệu CAD sẽ được raster hoá. Ở đây chúng ta đặt chiều rộng và chiều cao trang cơ bản sẽ được sử dụng cho các layout không có kích thước tùy chỉnh.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

### Bước 3: Tùy chỉnh kích thước trang Layout

Nếu bạn cần **kích thước trang PDF tùy chỉnh**, hãy thêm các mục cho mỗi layout bạn muốn xuất hiện trong PDF cuối cùng. Điều này cho phép bạn **chuyển đổi DWG sang PDF** với các kích thước khác nhau cho từng layout.

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

### Bước 4: Đặt tùy chọn PDF

Kết hợp các cài đặt raster hoá với các tùy chọn đặc thù cho PDF. Thuộc tính `VectorRasterizationOptions` thông báo cho Aspose.CAD sử dụng các kích thước layout mà chúng ta vừa định nghĩa.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Bước 5: Lưu dưới dạng PDF

Cuối cùng, xuất bản vẽ CAD ra một tệp PDF duy nhất chứa tất cả các layout đã chỉ định. Bước này **lưu CAD dưới dạng PDF** trong một lần gọi.

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

> **Mẹo chuyên nghiệp:** Tái sử dụng cùng một đối tượng `PdfOptions` nếu bạn cần xuất nhiều bản vẽ trong một batch – nó giảm tải việc tạo đối tượng mới.

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Giải pháp |
|-------|----------|
| **Các trang trống trong PDF đầu ra** | Kiểm tra rằng tên layout (`"ANSI C Plot"`, `"8.5 x 11 Plot"`) khớp chính xác với những gì được định nghĩa trong tệp CAD. |
| **Đầu ra có độ phân giải thấp** | Tăng DPI bằng cách gọi `rasterizationOptions.setResolution(300);` trước khi lưu. |
| **Giấy phép chưa được áp dụng** | Tải giấy phép tạm thời hoặc đầy đủ trước bất kỳ lời gọi Aspose.CAD nào: `License license = new License(); license.setLicense("Aspose.CAD.lic");` |

## Câu hỏi thường gặp

### Q1: Tôi có thể dùng Aspose.CAD cho Java cùng với các thư viện Java khác không?

A1: Có, Aspose.CAD cho Java được thiết kế để tích hợp liền mạch với các thư viện Java khác, cung cấp chức năng phong phú.

### Q2: Có phiên bản dùng thử không?

A2: Chắc chắn! Bạn có thể truy cập phiên bản dùng thử miễn phí [tại đây](https://releases.aspose.com/).

### Q3: Tôi có thể tìm hỗ trợ bổ sung ở đâu?

A3: Tham khảo [diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để nhận hỗ trợ cộng đồng và thảo luận.

### Q4: Làm sao để lấy giấy phép tạm thời?

A4: Bạn có thể nhận giấy phép tạm thời [tại đây](https://purchase.aspose.com/temporary-license/).

### Q5: Tôi mua phiên bản đầy đủ ở đâu?

A5: Mua phiên bản đầy đủ của Aspose.CAD cho Java [tại đây](https://purchase.aspose.com/buy).

---

**Cập nhật lần cuối:** 2026-01-22  
**Đã kiểm tra với:** Aspose.CAD cho Java 24.12  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}