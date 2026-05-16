---
date: 2026-02-23
description: Tìm hiểu cách chuyển đổi DWFX sang PDF và lưu CAD dưới dạng PDF bằng
  Aspose.CAD cho Java. Hướng dẫn nhanh để mở tệp DWFX và tạo PDF.
linktitle: Open DWFX File
second_title: Aspose.CAD Java API
title: Chuyển đổi DWFX sang PDF với Aspose.CAD cho Java
url: /vi/java/cad-file-manipulation/open-dwfx-file/
weight: 10
---

 we keep markdown formatting.

Let's craft final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chuyển đổi DWFX sang PDF với Aspose.CAD cho Java

## Giới thiệu

Trong thế giới thiết kế nhanh chóng ngày nay, các nhà phát triển thường cần **convert DWFX to PDF** để các bản vẽ CAD có thể được chia sẻ với những người không chuyên. Aspose.CAD for Java làm cho nhiệm vụ này trở nên đơn giản, cho phép bạn mở tệp DWFX, raster hoá nó, và **save CAD as PDF** chỉ với vài dòng mã. Trong hướng dẫn này, chúng tôi sẽ đi qua toàn bộ quy trình — từ thiết lập môi trường đến xác minh PDF cuối cùng — để bạn có thể tự tin xử lý các tệp DWFX trong ứng dụng Java của mình.

## Câu trả lời nhanh
- **Mục đích chính của hướng dẫn này là gì?** Để chỉ cách chuyển đổi DWFX sang PDF bằng Aspose.CAD cho Java.  
- **Thư viện nào cần thiết?** Aspose.CAD cho Java (tải xuống từ trang chính thức của Aspose).  
- **Tôi có cần giấy phép không?** Bản dùng thử miễn phí hoạt động cho phát triển; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Có thể mở tệp DWFX trực tiếp không?** Có, sử dụng `Image.load` để mở tệp DWFX.  
- **Định dạng đầu ra của ví dụ là gì?** Một tệp PDF được lưu vào thư mục đầu ra đã chỉ định.

## DWFX chuyển đổi sang PDF là gì?

Chuyển đổi DWFX sang PDF có nghĩa là lấy một bản vẽ DWFX dựa trên vector — thường được sử dụng trong các sản phẩm của Autodesk — và render nó thành một tài liệu PDF di động, được hỗ trợ rộng rãi. Điều này cho phép xem, in và chia sẻ dễ dàng mà không cần phần mềm CAD ở phía người nhận.

## Tại sao nên sử dụng Aspose.CAD cho Java để **save CAD as PDF**?

- **Không phụ thuộc bên ngoài:** API thuần Java, không cần các engine CAD gốc.  
- **Render chất lượng cao:** Giữ nguyên độ dày đường, màu sắc và lớp.  
- **Thân thiện với xử lý batch:** Lý tưởng cho tự động hoá phía máy chủ hoặc dịch vụ đám mây.  
- **Đa nền tảng:** Hoạt động trên Windows, Linux và macOS.

## Yêu cầu trước

Trước khi chúng ta bắt đầu với mã, hãy chắc chắn rằng bạn có những thứ sau:

- **Thư viện Aspose.CAD cho Java** – Tải xuống từ [trang tải Aspose.CAD cho Java](https://releases.aspose.com/cad/java/).  
- **Môi trường phát triển Java** – JDK 8 trở lên, với IDE hoặc công cụ xây dựng yêu thích của bạn.  
- **Tệp DWFX** – Một tệp DWFX mẫu (ví dụ, `Tyrannosaurus.dwfx`) để thử chuyển đổi.

## Nhập các namespace

Đầu tiên, nhập các lớp chúng ta sẽ cần:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Cách chuyển đổi DWFX sang PDF bằng Aspose.CAD cho Java

Dưới đây là hướng dẫn từng bước. Mỗi bước bao gồm một giải thích ngắn gọn và sau đó là đoạn mã chính xác bạn sẽ chạy.

### Bước 1: Tải tệp DWFX  

```java
String SourceDir = Utils.getDataDir_DWFXDrawings();
String OutputDir = Utils.getDataDir_Output();
String filePath = SourceDir + "Tyrannosaurus.dwfx";

Image cadImageDwf = Image.load(filePath);
```

Phương thức `Image.load` đọc tệp DWFX vào bộ nhớ, cung cấp cho chúng ta một đối tượng `CadImage` sẵn sàng để raster hoá.

### Bước 2: Đặt tùy chọn raster hoá  

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImageDwf.getSize().getWidth());
rasterizationOptions.setPageHeight(cadImageDwf.getSize().getHeight());
```

Các tùy chọn này xác định kích thước trang đầu ra, đảm bảo PDF khớp với kích thước bản vẽ gốc.

### Bước 3: Cấu hình tùy chọn PDF  

```java
PdfOptions CADf = new PdfOptions();
CADf.setVectorRasterizationOptions(rasterizationOptions);
```

Ở đây chúng ta gắn các thiết lập raster hoá vào cấu hình xuất PDF.

### Bước 4: Lưu dưới dạng PDF  

```java
cadImageDwf.save(OutputDir + "OpenDwfxFile_out.pdf", CADf);
```

Gọi `save` sẽ ghi hình ảnh đã render vào tệp PDF trong thư mục đầu ra.

### Bước 5: Xác nhận thành công  

```java
System.out.println("OpenDwfxFile executed successfully");
```

Một thông báo console đơn giản xác nhận việc chuyển đổi đã hoàn thành mà không có lỗi.

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân có thể | Giải pháp |
|-------|-------------------|----------|
| **Blank PDF output** | Chiều rộng/chiều cao raster hoá được đặt thành 0 | Đảm bảo `cadImageDwf.getSize()` trả về kích thước hợp lệ trước khi đặt các tùy chọn. |
| **Out‑of‑memory error** | Tệp DWFX rất lớn | Tăng kích thước heap JVM (`-Xmx2g`) hoặc xử lý tệp theo các phần nhỏ hơn. |
| **Missing fonts** | Phông chữ không được nhúng trong DWFX nguồn | Cài đặt các phông chữ cần thiết trên máy chủ hoặc sử dụng `CadRasterizationOptions.setFontName` để chỉ định phông thay thế. |

## Câu hỏi thường gặp

### Q1: Tôi có thể sử dụng Aspose.CAD cho Java với các định dạng tệp CAD khác không?  
**A1:** Có, Aspose.CAD cho Java hỗ trợ nhiều định dạng CAD, cung cấp giải pháp đa năng cho các nhà phát triển.

### Q2: Có bản dùng thử miễn phí cho Aspose.CAD cho Java không?  
**A2:** Có, bạn có thể khám phá các khả năng của Aspose.CAD cho Java với bản dùng thử miễn phí. Truy cập [đây](https://releases.aspose.com/) để bắt đầu.

### Q3: Làm thế nào để tôi nhận được hỗ trợ cho Aspose.CAD cho Java?  
**A3:** Tham gia cộng đồng Aspose.CAD trên [diễn đàn hỗ trợ](https://forum.aspose.com/c/cad/19) để được trợ giúp và hợp tác.

### Q4: Có giấy phép tạm thời cho Aspose.CAD cho Java không?  
**A4:** Có, bạn có thể nhận giấy phép tạm thời cho Aspose.CAD cho Java. Truy cập [đây](https://purchase.aspose.com/temporary-license/) để biết thêm chi tiết.

### Q5: Tôi có thể tìm tài liệu cho Aspose.CAD cho Java ở đâu?  
**A5:** Tài liệu đầy đủ có sẵn [tại đây](https://reference.aspose.com/cad/java/).

---

**Cập nhật lần cuối:** 2026-02-23  
**Đã kiểm tra với:** Aspose.CAD for Java 24.11  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}