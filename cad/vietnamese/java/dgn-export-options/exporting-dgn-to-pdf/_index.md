---
date: 2026-05-04
description: Tìm hiểu cách chuyển đổi tệp CAD PDF bằng cách xuất DGN sang PDF AutoCAD
  sử dụng Aspose.CAD cho Java. Hướng dẫn từng bước với kích thước PDF có thể tùy chỉnh
  và các tùy chọn.
keywords:
- convert cad pdf
- how to export dgn
- customize pdf size
- aspose cad download
- set pdf options
linktitle: Xuất DGN ở định dạng AutoCAD sang PDF
second_title: Aspose.CAD Java API
title: Chuyển đổi CAD PDF – Xuất PDF DGN sang AutoCAD một cách dễ dàng với Aspose.CAD
  cho Java
url: /vi/java/dgn-export-options/exporting-dgn-to-pdf/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chuyển Đổi CAD PDF: Xuất DGN sang PDF AutoCAD Dễ Dàng với Aspose.CAD cho Java

## Giới Thiệu

Nếu bạn cần **convert CAD PDF** trực tiếp từ các nguồn DGN, bạn đã đến đúng nơi. Trong hướng dẫn này, chúng tôi sẽ chỉ cho bạn cách sử dụng Aspose.CAD cho Java để xuất các tệp DGN thành PDF tương thích với AutoCAD. Bạn sẽ thấy cách đặt kích thước trang tùy chỉnh, chọn các bố cục cụ thể và tinh chỉnh đầu ra PDF — tất cả đều bằng mã rõ ràng, từng bước mà bạn có thể sao chép vào dự án của mình.

## Câu Trả Lời Nhanh
- **What does “convert CAD PDF” mean?** Nó đề cập đến việc chuyển đổi các tệp nguồn CAD (như DGN) thành PDF giữ nguyên dữ liệu vector và độ chính xác của bố cục.  
- **Which library handles the conversion?** Aspose.CAD for Java cung cấp bản dùng thử đáng tin cậy, không cần giấy phép cho nhiệm vụ này.  
- **Do I need a license for development?** Bản dùng thử miễn phí đủ cho việc thử nghiệm; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Can I customize the PDF size?** Có – `CadRasterizationOptions` cho phép bạn đặt chiều rộng, chiều cao và tỉ lệ trang.  
- **How many lines of code are required?** Ít hơn 20 dòng mã Java để tải, cấu hình và lưu PDF.

## “Chuyển Đổi CAD PDF” là gì?
Chuyển đổi CAD PDF có nghĩa là lấy một bản vẽ CAD gốc (ví dụ, DGN) và tạo ra một PDF giữ nguyên đồ họa vector, lớp và thông tin bố cục ban đầu. PDF kết quả có thể được xem trên bất kỳ thiết bị nào mà không cần phần mềm CAD, rất thích hợp để chia sẻ, in ấn hoặc lưu trữ.

## Tại sao nên dùng Aspose.CAD cho Java để chuyển đổi CAD PDF?
- **Full format support** – DGN, DWG, DXF và nhiều định dạng khác.  
- **No external dependencies** – thuần Java, không có DLL gốc.  
- **Fine‑grained control** – bạn có thể chọn các bố cục để xuất, đặt kích thước trang tùy chỉnh và kiểm soát chất lượng rasterization.  
- **Scalable for batch jobs** – tải và lưu hàng chục tệp trong một vòng lặp với chi phí tối thiểu.

## Yêu Cầu Trước
Trước khi bắt đầu, hãy chắc chắn bạn có những thứ sau:

- **Aspose.CAD Library** – tải xuống tại [here](https://releases.aspose.com/cad/java/).  
- **Document Directory** – một thư mục trên máy của bạn nơi các tệp DGN đầu vào và các PDF đầu ra sẽ được lưu.

## Nhập Gói

Trong dự án Java của bạn, nhập các gói cần thiết để truy cập các chức năng của Aspose.CAD:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Bây giờ, chúng ta sẽ phân tích mã ví dụ thành nhiều bước:

## Bước 1: Xác Định Đường Dẫn Tệp (cách xuất dgn)

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

Đảm bảo thay thế `"Your Document Directory"` bằng đường dẫn thực tế nơi các tệp của bạn được lưu.

## Bước 2: Tải Hình Ảnh DGN

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Tải tệp DGN bằng Aspose.CAD.

## Bước 3: Đặt Tùy Chọn Xuất PDF (tùy chỉnh kích thước pdf, thiết lập tùy chọn pdf)

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Export specific views
options.setVectorRasterizationOptions(vectorOptions);
```

Ở đây chúng ta định nghĩa các tùy chọn xuất PDF, bao gồm kích thước trang, tự động scaling, và các bố cục DGN (view) cụ thể mà bạn muốn bao gồm trong PDF cuối cùng.

## Bước 4: Lưu Tệp PDF

```java
objImage.save(outFile, options);
```

Lưu tệp PDF đã xuất. Phương thức `save` áp dụng tất cả các tùy chọn bạn đã cấu hình ở bước trước.

Lặp lại các bước này cho bất kỳ tệp DGN nào khác bạn muốn chuyển đổi. Xin chúc mừng! Bạn đã thành công **convert CAD PDF** bằng cách xuất các tệp DGN sang định dạng AutoCAD dưới dạng PDF bằng Aspose.CAD cho Java.

## Vấn Đề Thường Gặp và Giải Pháp
| Vấn Đề | Nguyên Nhân | Giải Pháp |
|-------|----------------|-----|
| **File not found** | Đường dẫn `dataDir` không đúng | Kiểm tra lại đường dẫn thư mục và đảm bảo tệp DGN tồn tại. |
| **Blank pages in PDF** | `AutomaticLayoutsScaling` được đặt thành `false` hoặc thiếu ID bố cục | Giữ `setAutomaticLayoutsScaling(true)` và xác minh tên bố cục (`"1","2",…`). |
| **Low‑resolution output** | DPI rasterization mặc định quá thấp | Sử dụng `vectorOptions.setResolution(300);` để tăng chất lượng (thêm trước `setVectorRasterizationOptions`). |
| **License exception** | Chạy mà không có giấy phép hợp lệ trong môi trường sản xuất | Áp dụng giấy phép tạm thời hoặc mua như mô tả trong tài liệu Aspose. |

## Câu Hỏi Thường Gặp (Bổ Sung)

**Q: Tôi có thể xuất chỉ một bố cục duy nhất từ tệp DGN đa‑bố cục không?**  
A: Có – chỉ định ID bố cục mong muốn trong `vectorOptions.setLayouts(new String[] { "2" });`.

**Q: Có thể nhúng phông chữ vào PDF kết quả không?**  
A: Aspose.CAD tự động nhúng các phông chữ cần thiết khi dữ liệu vector được rasterize; bạn cũng có thể kiểm soát việc nhúng phông chữ qua `PdfOptions` nếu cần.

**Q: Làm thế nào để xử lý nhiều tệp DGN trong một lô?**  
A: Đặt các bước trong một vòng lặp `for` duyệt qua danh sách tên tệp, sử dụng lại cùng một đối tượng `PdfOptions` cho mỗi lần lặp.

**Q: Thư viện có hỗ trợ PDF được bảo vệ bằng mật khẩu không?**  
A: Có – bạn có thể đặt mật khẩu cho đối tượng `PdfOptions` bằng `options.setPassword("yourPassword");`.

**Q: Tôi có thể tìm thêm ví dụ ở đâu?**  
A: Tài liệu chính thức của Aspose.CAD và kho mẫu chứa nhiều kịch bản bổ sung.

## Câu Hỏi Thường Gặp (Gốc)

### Q1: Aspose.CAD có tương thích với tất cả các định dạng tệp CAD không?

A1: Có, Aspose.CAD hỗ trợ một loạt các định dạng CAD, đảm bảo tính đa dạng trong việc xử lý các loại tệp khác nhau.

### Q2: Tôi có thể tùy chỉnh cài đặt xuất PDF không?

A2: Chắc chắn. Như đã trình bày trong hướng dẫn, bạn có thể điều chỉnh các tùy chọn như kích thước trang và bố cục để đáp ứng yêu cầu của mình.

### Q3: Tôi có thể tìm hỗ trợ hoặc trợ giúp bổ sung ở đâu?

A3: Truy cập [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) để nhận hỗ trợ cộng đồng và thảo luận.

### Q4: Có bản dùng thử miễn phí không?

A4: Có, bạn có thể truy cập bản dùng thử miễn phí [here](https://releases.aspose.com/).

### Q5: Làm thế nào để tôi có được giấy phép tạm thời?

A5: Nhận giấy phép tạm thời [here](https://purchase.aspose.com/temporary-license/).

## Kết Luận

Trong hướng dẫn này, chúng tôi đã khám phá cách **convert CAD PDF** bằng cách tận dụng Aspose.CAD cho Java. Chỉ với vài dòng mã, bạn có thể tải bản vẽ DGN, tinh chỉnh các tùy chọn xuất PDF và tạo ra các PDF chất lượng cao, sẵn sàng để chia sẻ hoặc lưu trữ. Hãy tự do thử nghiệm với các kích thước trang, bố cục hoặc xử lý batch khác nhau để phù hợp với nhu cầu dự án của bạn.

---

**Last Updated:** 2026-05-04  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}