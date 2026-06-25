---
date: 2026-02-15
description: Tìm hiểu cách thiết lập kích thước trang tùy chỉnh và tạo PDF từ CAD
  bằng Aspose.CAD cho Java. Hướng dẫn chi tiết này bao gồm việc xuất CAD sang PDF
  với Auto Layout Scaling.
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: Đặt kích thước trang tùy chỉnh – PDF từ CAD với tự động tỷ lệ bố cục
url: /vi/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Đặt Kích Thước Trang Tùy Chỉnh – Tạo PDF từ CAD với Tự Động Điều Chỉnh Bố Cục

## Giới thiệu

Nếu bạn cần **đặt kích thước trang tùy chỉnh** khi **tạo PDF từ CAD** một cách nhanh chóng và với tỷ lệ hoàn hảo, Aspose.CAD for Java sẽ hỗ trợ bạn. Tự Động Điều Chỉnh Bố Cục (Auto Layout Scaling) tự động điều chỉnh kích thước bố cục sao cho PDF kết quả trông chính xác như mong muốn, bất kể kích thước trang CAD gốc. Trong hướng dẫn này, chúng ta sẽ đi qua toàn bộ quy trình — từ tải tệp DXF đến xuất PDF — đồng thời nhấn mạnh khả năng **export CAD to PDF** của thư viện và chỉ ra cách bạn cũng có thể **convert DWG to PDF** hoặc **increase PDF resolution** khi cần.

## Câu trả lời nhanh
- **Auto Layout Scaling làm gì?** Nó tự động thay đổi kích thước bố cục CAD để vừa với kích thước trang mục tiêu khi raster hóa.  
- **Tôi có thể chuyển đổi những định dạng nào?** Bất kỳ định dạng nào được Aspose.CAD hỗ trợ (ví dụ: DXF, DWG, DWF) đều có thể chuyển đổi sang PDF.  
- **Tôi có cần giấy phép cho môi trường sản xuất không?** Có, cần giấy phép thương mại cho việc sử dụng không phải ở chế độ đánh giá.  
- **Quá trình chuyển đổi mất bao lâu?** Thông thường dưới một giây cho các tệp tiêu chuẩn trên phần cứng hiện đại.  
- **Tôi có thể thay đổi kích thước trang không?** Có, bạn có thể đặt kích thước trang tùy chỉnh qua `CadRasterizationOptions`.

## “Create PDF from CAD” là gì?

Tạo PDF từ CAD có nghĩa là lấy một bản vẽ kỹ thuật dựa trên vector (DXF, DWG, v.v.) và raster hóa nó thành tài liệu PDF. PDF giữ nguyên độ trung thực hình ảnh của bản vẽ gốc đồng thời có thể xem trên bất kỳ nền tảng nào.

## Tại sao nên sử dụng Auto Layout Scaling?

- **Đầu ra nhất quán:** Đảm bảo mọi bố cục lấp đầy trang PDF mà không cần tính toán kích thước thủ công.  
- **Tiết kiệm thời gian:** Loại bỏ nhu cầu điều chỉnh tỷ lệ cho từng bản vẽ một cách thủ công.  
- **Chất lượng cao:** Giữ nguyên độ dày đường và độ chính xác hình học trong quá trình chuyển đổi.  
- **Linh hoạt:** Hoạt động cho **convert dxf to pdf**, **convert dwg to pdf**, và ngay cả khi bạn cần **increase PDF resolution** cho các tệp sẵn sàng in.

## Yêu cầu trước

1. **Thư viện Aspose.CAD for Java** – tải phiên bản mới nhất từ [download page](https://releases.aspose.com/cad/java/).  
2. **Thư mục tài nguyên** – tạo một thư mục trên máy của bạn để lưu các tệp CAD; thay thế `"Your Document Directory"` trong mã bằng đường dẫn đó.  
3. **Tệp CAD mẫu** – trong hướng dẫn này chúng ta sẽ dùng `conic_pyramid.dxf`, được bao gồm trong bộ dữ liệu mẫu của Aspose.

## Nhập không gian tên

Đầu tiên, nhập các lớp cần thiết. Điều này cho phép chúng ta truy cập các tính năng tải ảnh, raster hóa và xuất PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Cách Đặt Kích Thước Trang Tùy Chỉnh cho PDF từ CAD

Trước khi đi vào mã từng bước, hãy hiểu tại sao việc đặt kích thước trang tùy chỉnh lại quan trọng. Khi bạn **đặt kích thước trang tùy chỉnh**, bạn kiểm soát kích thước vật lý của PDF kết quả (ví dụ: A4, Letter, hoặc một kích thước riêng). Điều này rất cần thiết trong quy trình kỹ thuật nơi các bản vẽ phải phù hợp với tiêu chuẩn tờ hoặc khi bạn cần nhúng PDF vào tài liệu lớn hơn.

### Bước 1: Tải tệp CAD

Tải tệp nguồn là bước đầu tiên trong **how to export CAD** sang tài liệu PDF.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Bước 2: Tạo tùy chọn raster hóa

Xác định kích thước trang mục tiêu. Bạn cũng có thể dùng khối này để **set CAD page size** một cách thủ công nếu muốn bố cục tùy chỉnh.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Bước 3: Đặt Auto Layout Scaling

Bật tính năng tự động điều chỉnh tỷ lệ. Đây là phần cốt lõi của **how to set scaling** cho quá trình chuyển đổi CAD‑to‑PDF.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

### Bước 4: Tạo tùy chọn PDF

Liên kết các cài đặt raster hóa với tùy chọn xuất PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Bước 5: Xuất ra PDF

Cuối cùng, lưu hình ảnh đã render dưới dạng tệp PDF. Bước này hoàn thành quy trình **convert dxf to pdf**.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Lặp lại các bước trên cho bất kỳ tệp CAD bổ sung nào bạn cần xử lý, dù chúng là **DWG**, **DWF**, hoặc các định dạng được hỗ trợ khác.

## Các trường hợp sử dụng phổ biến

| Kịch bản | Tại sao cần đặt kích thước trang tùy chỉnh? |
|----------|---------------------------------------------|
| **Nộp bản vẽ xây dựng** | Đảm bảo PDF khớp với kích thước tờ A1/A2 tiêu chuẩn yêu cầu bởi cơ quan quản lý. |
| **Nhúng vào sách hướng dẫn kỹ thuật** | Đảm bảo bản vẽ vừa với bố cục đã định trước của sách mà không cần tỷ lệ bổ sung. |
| **In chất lượng cao** | Cho phép tăng DPI (ví dụ: `rasterizationOptions.setResolution(300)`) trong khi giữ kích thước trang nhất quán. |

## Các vấn đề thường gặp & Khắc phục

| Triệu chứng | Nguyên nhân có thể | Cách khắc phục |
|------------|--------------------|----------------|
| PDF trống | Các tùy chọn rasterization chưa được đặt hoặc đường dẫn tệp sai | Kiểm tra lại đường dẫn `srcFile` và đảm bảo `setPageWidth/Height` khác 0 |
| Tỷ lệ bị biến dạng | `setAutomaticLayoutsScaling` để `false` | Bật tự động scaling hoặc tính toán tỷ lệ thủ công |
| Thiếu lớp | DXF nguồn chứa các thực thể không được hỗ trợ | Kiểm tra ghi chú phát hành Aspose.CAD để biết các loại thực thể được hỗ trợ |

## Câu hỏi thường gặp

**Q: Aspose.CAD for Java có tương thích với tất cả các định dạng tệp CAD không?**  
A: Aspose.CAD for Java hỗ trợ nhiều định dạng CAD, bao gồm DWG, DXF và DWF.

**Q: Tôi có thể tùy chỉnh thêm các tùy chọn scaling không?**  
A: Có, lớp `CadRasterizationOptions` cung cấp các thuộc tính để tinh chỉnh scaling, DPI và các cài đặt rasterization khác.

**Q: Tôi có thể tìm tài liệu bổ sung cho Aspose.CAD for Java ở đâu?**  
A: Tham khảo [documentation](https://reference.aspose.com/cad/java/) để có thông tin chi tiết và các ví dụ.

**Q: Có bản dùng thử miễn phí cho Aspose.CAD for Java không?**  
A: Có, bạn có thể khám phá [free trial](https://releases.aspose.com/) để trải nghiệm các khả năng của Aspose.CAD for Java.

**Q: Làm sao tôi có thể nhận hỗ trợ hoặc tham gia thảo luận về Aspose.CAD for Java?**  
A: Truy cập [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) để kết nối với cộng đồng và nhận hỗ trợ.

**Các câu hỏi chung bổ sung**

**Q: Làm sao tôi chuyển đổi tệp DWG sang PDF thay vì DXF?**  
A: Cùng một đoạn mã hoạt động; chỉ cần đổi phần mở rộng tệp trong `srcFile` thành `.dwg`.

**Q: Tôi có thể đặt DPI tùy chỉnh cho PDF độ phân giải cao không?**  
A: Có, sử dụng `rasterizationOptions.setResolution(300);` (hoặc bất kỳ DPI nào bạn cần).

**Q: Có thể nhúng phông chữ vào PDF được tạo không?**  
A: Aspose.CAD raster hóa bản vẽ, vì vậy phông chữ được render dưới dạng vector; không cần nhúng phông chữ riêng.

## Kết luận

Bằng cách làm theo hướng dẫn này, bạn đã biết cách **đặt kích thước trang tùy chỉnh** và **tạo PDF từ CAD** bằng Aspose.CAD for Java với Auto Layout Scaling. Quy trình này giúp đơn giản hoá **export CAD to PDF**, đảm bảo tỷ lệ nhất quán và tiết kiệm thời gian phát triển quý giá. Hãy thoải mái thử nghiệm với các kích thước trang, độ phân giải và định dạng CAD khác nhau để đáp ứng nhu cầu dự án, dù bạn đang **convert DWG to PDF**, **increase PDF resolution**, hoặc xây dựng một bộ xử lý **java CAD to PDF** hàng loạt.

---

**Last Updated:** 2026-02-15  
**Tested With:** Aspose.CAD for Java 24.12 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}