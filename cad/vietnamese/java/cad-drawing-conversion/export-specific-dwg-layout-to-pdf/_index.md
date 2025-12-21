---
date: 2025-12-21
description: Tìm hiểu cách chuyển đổi DWG sang PDF bằng cách xuất một bố cục DWG cụ
  thể sang PDF sử dụng Aspose.CAD cho Java. Hãy làm theo hướng dẫn từng bước chuyển
  đổi DWG sang PDF này để tối ưu quy trình làm việc CAD của bạn.
linktitle: Export Specific DWG Layout to PDF
second_title: Aspose.CAD Java API
title: Chuyển đổi DWG sang PDF – Xuất bố cục với Aspose.CAD cho Java
url: /vi/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chuyển DWG sang PDF – Xuất Bố Cục Cụ Thể Sử Dụng Aspose.CAD cho Java

## Giới thiệu

Trong thế giới năng động của Computer‑Aided Design (CAD), **convert DWG to PDF** là một yêu cầu thường xuyên khi chia sẻ bản vẽ với khách hàng, nhà thầu hoặc các bên liên quan không chuyên môn. Aspose.CAD cho Java giúp quá trình chuyển đổi này trở nên nhẹ nhàng, và thậm chí cho phép bạn chọn một bố cục duy nhất từ tệp DWG có nhiều bố cục. Trong hướng dẫn này, chúng ta sẽ đi qua **how to export DWG**‑specific layouts to PDF, để bạn có thể cung cấp chính xác những gì dự án cần mà không có các trang thừa hoặc cắt thủ công.

## Câu trả lời nhanh
- **What does “convert DWG to PDF” mean?** Nó chuyển đổi bản vẽ DWG thành tài liệu PDF, giữ nguyên dữ liệu vector và độ chính xác của bố cục.  
- **Which library handles the conversion?** Aspose.CAD cho Java cung cấp một API sẵn sàng sử dụng.  
- **Do I need a license for production?** Có, cần có giấy phép thương mại; bản dùng thử miễn phí hoạt động cho mục đích đánh giá.  
- **Can I choose a single layout?** Chắc chắn – đặt thuộc tính `Layouts` thành tên bố cục mong muốn.  
- **What Java version is supported?** Java 8 và các phiên bản sau đều tương thích hoàn toàn.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn có:

- **Java Development Environment** – JDK 8+ và IDE yêu thích của bạn.  
- **Aspose.CAD Library** – Tải JAR mới nhất từ trang chính thức **[here](https://releases.aspose.com/cad/java/)**.  
- **DWG File** – Một bản vẽ chứa ít nhất một bố cục (ví dụ: *visualization_-_conference_room.dwg*).  

## Tại sao xuất một Bố Cục DWG cụ thể sang PDF?

Nhiều tệp DWG chứa nhiều không gian giấy (layouts). Xuất toàn bộ tệp có thể tạo ra một PDF cồng kềnh với các trang không mong muốn. Việc chọn một bố cục duy nhất:

- Giảm kích thước tệp.  
- Tập trung sự chú ý của người xem vào tờ bản vẽ liên quan.  
- Phù hợp với tiêu chuẩn tài liệu dự án.  

## Hướng dẫn từng bước

### Bước 1: Thiết lập môi trường dự án

Tạo một dự án Java mới (Maven, Gradle, hoặc IDE thuần) và thêm JAR Aspose.CAD vào classpath. Bạn có thể tải nó **[here](https://releases.aspose.com/cad/java/)**.

### Bước 2: Nhập các gói cần thiết

Thêm các namespace Aspose.CAD cần thiết vào lớp Java của bạn.

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

### Bước 3: Tải tệp DWG

Chỉ đến tệp DWG bạn muốn chuyển đổi và tải nó vào một đối tượng `Image`.

```java
String srcFile = dataDir + "visualization_-_conference_room.dwg";
Image image = Image.load(srcFile);
```

### Bước 4: Cấu hình tùy chọn rasterization

Xác định kích thước trang và, quan trọng nhất, bố cục bạn muốn xuất.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
// Specify desired layout name
rasterizationOptions.setLayouts(new String[] {"Layout1"});
```

### Bước 5: Đặt tùy chọn xuất PDF

Liên kết các cài đặt rasterization với trình xuất PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Bước 6: Xuất DWG sang PDF

Lưu kết quả dưới dạng tệp PDF. Kết quả sẽ chỉ chứa **Layout1**, đạt được một thao tác **convert DWG to PDF** sạch sẽ.

```java
image.save(dataDir + "ExportSpecificLayoutToPDF_out_.pdf", pdfOptions);
```

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân | Cách khắc phục |
|-------|-------------|----------------|
| **Layout not found** | Tên bố cục bị viết sai hoặc không tồn tại trong DWG. | Sử dụng `image.getLayoutNames()` để liệt kê các bố cục có sẵn, sau đó chọn đúng tên. |
| **Low resolution PDF** | `PageWidth`/`PageHeight` quá nhỏ. | Tăng kích thước (ví dụ, 2000 × 2000) hoặc đặt `rasterizationOptions.setResolution(300);`. |
| **License exception** | Chạy mà không có giấy phép hợp lệ trong môi trường không dùng thử. | Áp dụng giấy phép Aspose.CAD trước khi tải hình ảnh: `License license = new License(); license.setLicense("Aspose.CAD.lic");`. |

## Câu hỏi thường gặp

**Q1: Can I use Aspose.CAD for Java with other Java‑based CAD libraries?**  
A: Aspose.CAD cho Java là một thư viện độc lập nhưng có thể được tích hợp với các thư viện Java‑based khác để mở rộng chức năng.

**Q2: Are there any licensing options for Aspose.CAD?**  
A: Có, bạn có thể khám phá các tùy chọn giấy phép và chi tiết mua hàng **[here](https://purchase.aspose.com/buy)**.

**Q3: How can I obtain a temporary license for Aspose.CAD?**  
A: Truy cập **[this link](https://purchase.aspose.com/temporary-license/)** để yêu cầu giấy phép tạm thời.

**Q4: Where can I find support for Aspose.CAD?**  
A: Đối với bất kỳ câu hỏi hoặc hỗ trợ nào, hãy truy cập **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**.

**Q5: Is there a free trial available for Aspose.CAD?**  
A: Có, bạn có thể truy cập bản dùng thử miễn phí **[here](https://releases.aspose.com/)**.

## Kết luận

Bằng cách làm theo **dwg to pdf tutorial** này, bạn đã có một cách đáng tin cậy để **convert DWG to PDF** đồng thời tập trung vào một bố cục duy nhất. Cách tiếp cận này giúp tiết kiệm không gian lưu trữ, tăng tốc chia sẻ tài liệu và giữ cho quy trình CAD của bạn gọn gàng. Hãy thoải mái thử nghiệm các cài đặt rasterization khác nhau hoặc kết hợp nhiều bố cục vào một PDF duy nhất khi dự án của bạn phát triển.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Cập nhật lần cuối:** 2025-12-21  
**Kiểm tra với:** Aspose.CAD for Java 24.12  
**Tác giả:** Aspose