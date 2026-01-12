---
date: 2026-01-12
description: Tìm hiểu cách xuất CAD sang PDF trong khi ghi đè việc phát hiện trang
  mã tự động trong các tệp DWG bằng Aspose.CAD cho Java. Xử lý mã hóa và CIF/MIF bị
  hỏng.
linktitle: Override Automatic Code Page Detection in DWG Files
second_title: Aspose.CAD Java API
title: Xuất CAD sang PDF – Ghi đè phát hiện trang mã tự động trong tệp DWG bằng Java
url: /vi/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xuất CAD sang PDF – Ghi đè Phát hiện Trang mã Tự động trong Tệp DWG bằng Java

## Giới thiệu

Trong hướng dẫn toàn diện này, bạn sẽ khám phá **cách xuất CAD sang PDF** đồng thời ghi đè phát hiện trang mã tự động có thể làm hỏng văn bản trong các tệp DWG. Aspose.CAD for Java cung cấp khả năng kiểm soát chi tiết đối với mã hoá, cho phép bạn khôi phục dữ liệu CIF/MIF bị lỗi và tạo ra đầu ra PDF đáng tin cậy. Dù bạn đang xây dựng một bộ chuyển đổi hàng loạt hay tích hợp xử lý CAD vào một ứng dụng Java lớn hơn, các bước dưới đây sẽ hướng dẫn bạn qua toàn bộ quy trình.

## Câu trả lời nhanh
- **Ý nghĩa của “override code page” là gì?** Nó buộc Aspose.CAD sử dụng một bảng mã ký tự cụ thể thay vì đoán.
- **Tôi có thể xuất DWG trực tiếp sang PDF không?** Có – sau khi đặt đúng trang mã, bạn có thể lưu hình ảnh CAD dưới dạng PDF.
- **Bảng mã nào phù hợp cho văn bản tiếng Nhật?** `CodePages.Japanese` và `MifCodePages.Japanese` là lựa chọn đúng.
- **Tôi có cần giấy phép cho việc sử dụng trong môi trường sản xuất không?** Cần một giấy phép thương mại; giấy phép tạm thời có sẵn cho mục đích thử nghiệm.
- **Phiên bản Aspose.CAD nào được yêu cầu?** Bất kỳ phiên bản gần đây nào hỗ trợ `LoadOptions` và `PdfOptions`.

## “Xuất CAD sang PDF” là gì?
Xuất CAD sang PDF chuyển đổi các bản vẽ CAD dựa trên vector thành định dạng tài liệu cố định, được hỗ trợ rộng rãi. PDF kết quả giữ nguyên các đường nét, lớp và văn bản đồng thời giúp bản vẽ dễ dàng chia sẻ, in ấn hoặc nhúng vào các ứng dụng khác.

## Tại sao cần ghi đè phát hiện trang mã tự động?
Các tệp DWG thường lưu trữ văn bản bằng các trang mã kế thừa. Việc tự động phát hiện của Aspose.CAD có thể hiểu sai các byte này, dẫn đến ký tự bị rối. Bằng cách chỉ định thủ công trang mã, bạn đảm bảo văn bản hiển thị đúng như mong muốn trong PDF xuất ra, đặc biệt với các script không phải Latin như tiếng Nhật, Cyrillic hoặc Arabic.

## Yêu cầu trước
- **Môi trường phát triển Java** – JDK 8+ và IDE yêu thích của bạn.
- **Aspose.CAD for Java** – Tải thư viện từ trang chính thức [đây](https://releases.aspose.com/cad/java/).
- **Tệp DWG mẫu** – Sử dụng `SimpleEntities.dwg` được cung cấp hoặc bất kỳ tệp DWG nào bạn cần chuyển đổi.

## Nhập gói
Trong dự án Java của bạn, nhập các lớp Aspose.CAD cần thiết:

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## Hướng dẫn từng bước

### Bước 1: Thiết lập dự án Java
Tạo một dự án Maven hoặc Gradle mới và thêm JAR Aspose.CAD vào classpath. Bước này đảm bảo IDE có thể giải quyết các lớp đã nhập.

### Bước 2: Tải tệp DWG với Trang mã được chỉ định
Cho Aspose.CAD biết mã hoá nào sẽ sử dụng và liệu có nên cố gắng khôi phục dữ liệu CIF/MIF bị lỗi hay không.

```java
String SourceDir = "Your Document Directory";
String dwgPathToFile = SourceDir + "SimpleEntites.dwg";
LoadOptions opts = new LoadOptions();
opts.setSpecifiedEncoding(CodePages.Japanese);
opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
opts.setRecoverMalformedCifMif(false);
CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);
```

### Bước 3: Xuất hình ảnh CAD sang PDF
Với trang mã đúng đã được áp dụng, bạn có thể xuất bản vẽ một cách an toàn. Đối tượng `PdfOptions` cho phép bạn tinh chỉnh đầu ra PDF (nén, rasterization, v.v.).

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### Bước 4: Xác minh thành công
Một thông báo console đơn giản xác nhận quá trình đã hoàn thành mà không có ngoại lệ.

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

Bạn có thể lặp lại các bước này cho nhiều tệp DWG, điều chỉnh đường dẫn nguồn và tên đầu ra tùy ý.

## Các vấn đề thường gặp & Giải pháp
- **Ký tự rác vẫn xuất hiện:** Kiểm tra lại `specifiedEncoding` có khớp với trang mã gốc của DWG không. Thử một enum `CodePages` khác nếu cần.
- **`NullPointerException` tại `cadImage.save`:** Đảm bảo tệp DWG được tải đúng; kiểm tra đường dẫn và quyền truy cập tệp.
- **Kích thước PDF quá lớn:** Bật nén trong `PdfOptions` (ví dụ, `pdfOptions.setCompress(true)`).

## Câu hỏi thường gặp

**Q1: Aspose.CAD có tương thích với mọi phiên bản tệp DWG không?**  
A1: Aspose.CAD hỗ trợ một loạt các phiên bản DWG, bao gồm AutoCAD 2018 và các bản phát hành trước đó.

**Q2: Tôi có thể sử dụng Aspose.CAD cho các dự án thương mại không?**  
A2: Có, cần có giấy phép thương mại cho việc sử dụng trong môi trường sản xuất. Bạn có thể nhận giấy phép [đây](https://purchase.aspose.com/buy).

**Q3: Có bất kỳ hạn chế nào trong phiên bản dùng thử miễn phí không?**  
A3: Bản dùng thử có giới hạn về kích thước và tính năng; tham khảo tài liệu chính thức để biết chi tiết.

**Q4: Làm sao tôi có thể nhận hỗ trợ cho Aspose.CAD?**  
A4: Truy cập cộng đồng [diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để được trợ giúp và thảo luận.

**Q5: Có giấy phép tạm thời cho mục đích thử nghiệm không?**  
A5: Có, bạn có thể yêu cầu giấy phép tạm thời [đây](https://purchase.aspose.com/temporary-license/).

---

**Cập nhật lần cuối:** 2026-01-12  
**Đã kiểm tra với:** Aspose.CAD for Java 24.11 (phiên bản mới nhất tại thời điểm viết)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}