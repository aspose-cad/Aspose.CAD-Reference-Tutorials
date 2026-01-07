---
date: 2026-01-07
description: Tìm hiểu cách xuất CAD sang PDF và chuyển đổi DGN sang PDF bằng Aspose.CAD
  cho Java. Hướng dẫn chi tiết từng bước cho các nhà phát triển Java.
linktitle: Export Embedded DGN
second_title: Aspose.CAD Java API
title: Xuất CAD sang PDF – Xuất DGN nhúng với Aspose.CAD cho Java
url: /vi/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xuất CAD sang PDF – Xuất DGN nhúng với Aspose.CAD cho Java

## Giới thiệu

Trong hướng dẫn này, bạn sẽ khám phá **cách xuất CAD sang PDF** bằng cách chuyển đổi tệp DGN nhúng thành tài liệu PDF chất lượng cao với Aspose.CAD cho Java. Aspose.CAD là một thư viện mạnh mẽ cung cấp cho các nhà phát triển Java toàn quyền kiểm soát việc xử lý tệp CAD, dù bạn cần **chuyển đổi DGN sang PDF**, **chuyển đổi DWG sang PDF**, hay chỉ đơn giản là hiển thị bản vẽ CAD dưới các định dạng khác. Hãy làm theo hướng dẫn từng bước dưới đây, và bạn sẽ có thể tích hợp tính năng này vào ứng dụng của mình trong vài phút.

## Câu trả lời nhanh
- **“Xuất CAD sang PDF” có nghĩa là gì?** Nó chuyển đổi các bản vẽ CAD (DWG, DGN, v.v.) thành tệp PDF đồng thời giữ nguyên chất lượng vector.  
- **Thư viện nào được sử dụng?** Aspose.CAD cho Java.  
- **Có cần giấy phép không?** Cần giấy phép cho môi trường sản xuất; có bản dùng thử miễn phí.  
- **Các yêu cầu trước chính là gì?** Môi trường phát triển Java và JAR Aspose.CAD cho Java.  
- **Có thể tùy chỉnh đầu ra không?** Có – bạn có thể chọn layout, thiết lập tùy chọn rasterization và kiểm soát các cài đặt PDF.

## “Xuất CAD sang PDF” là gì?
Xuất CAD sang PDF có nghĩa là lấy một tệp CAD gốc (như DWG hoặc DGN) và tạo ra một tài liệu PDF phản ánh trung thực hình học gốc. PDF có thể được xem trên bất kỳ nền tảng nào mà không cần phần mềm CAD, rất phù hợp để chia sẻ, in ấn hoặc lưu trữ.

## Tại sao nên dùng Aspose.CAD cho Java để chuyển đổi DGN sang PDF?
- **Không phụ thuộc bên ngoài** – hoạt động hoàn toàn trong Java.  
- **Giữ nguyên dữ liệu vector** – PDF luôn sắc nét ở mọi mức phóng đại.  
- **Kiểm soát chi tiết** – chọn layout cụ thể, thiết lập DPI rasterization và nhúng phông chữ.  
- **Sẵn sàng cho doanh nghiệp** – hỗ trợ tệp lớn, xử lý hàng loạt và các tùy chọn cấp phép.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn đã có:

- **Môi trường phát triển Java** – JDK 8 trở lên đã được cài đặt và cấu hình.  
- **Aspose.CAD cho Java** – tải JAR mới nhất từ [đây](https://releases.aspose.com/cad/java/).  

## Nhập các gói

Để bắt đầu, bạn cần nhập các lớp cần thiết vào dự án Java của mình. Thêm các câu lệnh import sau vào tệp nguồn:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Cách xuất DGN sang PDF bằng Aspose.CAD cho Java?

Dưới đây là hướng dẫn chi tiết, có đánh số, cho thấy cách chuyển đổi một tệp DGN nhúng (được lưu trong DWG) thành PDF.

### Bước 1: Thiết lập đường dẫn đầu vào và đầu ra

Xác định thư mục chứa tệp nguồn và chỉ định DWG chứa DGN nhúng.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### Bước 2: Tải tệp DWG

Tải tệp DWG vào đối tượng `Image`. Aspose.CAD sẽ tự động phát hiện dữ liệu DGN nhúng.

```java
Image objImage = Image.load(fileName);
```

### Bước 3: Cấu hình tùy chọn rasterization

Chọn layout(s) bạn muốn đưa vào PDF. Trong ví dụ này, chúng ta chỉ xuất layout **Model**.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### Bước 4: Cấu hình tùy chọn PDF

Gắn các cài đặt rasterization vào tùy chọn xuất PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Bước 5: Lưu tệp PDF

Cuối cùng, ghi PDF ra đĩa bằng các tùy chọn đã cấu hình.

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Chuyển đổi DWG sang PDF – một mẹo bổ sung

Nếu tệp nguồn của bạn là DWG thuần (không có DGN nhúng), bạn có thể tái sử dụng cùng một đoạn mã – chỉ cần thay đổi `fileName` để trỏ tới DWG bạn muốn chuyển đổi. Các tùy chọn rasterization và PDF vẫn giữ nguyên, cho bạn một quy trình **chuyển đổi DWG sang PDF** nhất quán.

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|------------|----------|
| **PDF trống** | Tên layout không khớp | Kiểm tra lại tên layout truyền vào `setLayouts` có khớp chính xác (phân biệt chữ hoa/thường) với layout trong tệp nguồn. |
| **Lỗi giấy phép** | Sử dụng bản dùng thử mà không có giấy phép | Áp dụng giấy phép Aspose.CAD hợp lệ trước khi tải hình ảnh (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |
| **Không tìm thấy tệp** | Đường dẫn `dataDir` sai | Sử dụng đường dẫn tuyệt đối hoặc đảm bảo đường dẫn tương đối đúng so với thư mục làm việc của dự án. |
| **Đồ họa độ phân giải thấp** | DPI rasterization mặc định quá thấp | Đặt `rasterizationOptions.setPageWidth/Height` hoặc `setResolution` để tăng DPI. |

## Câu hỏi thường gặp

**H: Tôi có thể dùng Aspose.CAD cho Java trong dự án thương mại không?**  
Đ: Có, Aspose.CAD cho Java là thư viện thương mại. Bạn có thể mua giấy phép từ [đây](https://purchase.aspose.com/buy).

**H: Có bản dùng thử miễn phí không?**  
Đ: Có, bạn có thể truy cập bản dùng thử miễn phí của Aspose.CAD cho Java [tại đây](https://releases.aspose.com/).

**H: Làm sao để nhận hỗ trợ cho Aspose.CAD cho Java?**  
Đ: Bạn có thể tìm kiếm hỗ trợ từ cộng đồng Aspose.CAD trên [diễn đàn](https://forum.aspose.com/c/cad/19).

**H: Nếu tôi cần giấy phép tạm thời thì sao?**  
Đ: Bạn có thể lấy giấy phép tạm thời [tại đây](https://purchase.aspose.com/temporary-license/).

**H: Tài liệu hướng dẫn nằm ở đâu?**  
Đ: Tài liệu có sẵn [tại đây](https://reference.aspose.com/cad/java/).

## Kết luận

Bạn đã học cách **xuất CAD sang PDF**, cụ thể là **chuyển đổi DGN sang PDF** và thậm chí **chuyển đổi DWG sang PDF** bằng Aspose.CAD cho Java. Bằng cách làm theo các bước trên, bạn có thể tích hợp chuyển đổi CAD‑to‑PDF liền mạch vào bất kỳ giải pháp dựa trên Java nào, cung cấp PDF chất lượng cao cho người dùng mà không cần phần mềm CAD bổ sung.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Cập nhật lần cuối:** 2026-01-07  
**Kiểm tra với:** Aspose.CAD cho Java 24.12  
**Tác giả:** Aspose