---
date: 2025-12-10
description: Tìm hiểu cách tạo PDF từ CAD bằng Aspose.CAD cho Java với tính năng Auto
  Layout Scaling. Hướng dẫn từng bước này sẽ chỉ cho bạn cách xuất CAD sang PDF một
  cách hiệu quả và đáng tin cậy.
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: Tạo PDF từ CAD – Tự động điều chỉnh tỷ lệ bố cục với Aspose.CAD Java
url: /vi/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tạo PDF từ CAD Layout Scaling với Aspose.CAD Java

## Giới thiệu

Nếu bạn cần **create PDF from CAD** nhanh chóng và với tỷ lệ hoàn hảo, Aspose.CAD for Java sẽ hỗ trợ bạn. Auto Layout Scaling tự động điều chỉnh kích thước bố cục sao cho PDF kết quả trông chính xác như mong muốn, bất kể kích thước trang CAD gốc. Trong hướng dẫn này, chúng ta sẽ đi qua toàn bộ quy trình — từ tải tệp DXF đến xuất PDF — đồng thời nhấn mạnh khả năng **export CAD to PDF** của thư viện.

## Câu trả lời nhanh
- **Auto Layout Scaling làm gì?** Nó tự động thay đổi kích thước bố cục CAD để vừa với kích thước trang đích khi raster hóa.  
- **ôi có thể chuyển đổi định dạng nào?** Bất kỳ định dạng nào được Aspose.CAD hỗ trợ (ví dụ: DXF, DWG, DWF) đều có thể chuyển sang PDF.  
- **Tôi có cần giấy phép cho môi trường sản xuất không?** Có, cần giấy phép thương mại cho việc sử dụng không phải đánh giá.  
- **Quá trình chuyển đổi mất bao lâu?** Thông thường dưới một giây cho các tệp tiêu chuẩn trên phần cứng hiện đại.  
- **Tôi có thể thay đổi kích thước trang không?** Có, bạn có thể đặt kích thước trang tùy chỉnh qua `CadRasterizationOptions`.

## “create PDF from CAD” là gì?
Tạo PDF từ CAD có nghĩa là lấy một bản vẽ kỹ thuật dựa trên vector (DXF, DWG, v.v.) và raster hóa nó thành tài liệu PDF. PDF giữ nguyên độ trung thực hình ảnh của bản vẽ gốc đồng thời có thể xem trên bất kỳ nền tảng nào.

## Tại sao nên sử dụng Auto Layout Scaling?
- **Đầu ra nhất quán:** Đảm bảo mọi bố cục lấp đầy trang PDF mà không cần tính toán kích thước thủ công.  
- **Tiết kiệm thời gian:** Loại bỏ nhu cầu điều chỉnh tỷ lệ cho từng bản vẽ một cách thủ công.  
- **Chất lượng cao:** Giữ nguyên độ dày đường và độ chính xác hình học trong quá trình chuyển đổi.

## Yêu cầu trước

1. **Aspose.CAD for Java Library** – tải phiên bản mới nhất từ [download page](https://releases.aspose.com/cad/java/).  
2. **Thư mục tài nguyên** – tạo một thư mục trên máy của bạn để lưu các tệp CAD; thay thế `"Your Document Directory"` trong mã bằng đường dẫn đó.  
3. **Tệp CAD mẫu** – trong hướng dẫn này chúng ta sẽ sử dụng `conic_pyramid.dxf`, được bao gồm trong bộ dữ liệu mẫu của Aspose.

## Nhập không gian tên

Đầu tiên, nhập các lớp cần thiết. Điều này cho phép chúng ta truy cập các tính năng tải ảnh, raster hóa và xuất PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Bước 1: Tải tệp CAD

Tải tệp nguồn là bước đầu tiên trong **how to export CAD** sang tài liệu PDF.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

## Bước 2: Tạo tùy chọn Rasterization

Xác định kích thước trang đích. Bạn cũng có thể dùng khối này để **set CAD page size** thủ công nếu muốn bố cục tùy chỉnh.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

## Bước 3: Đặt Auto Layout Scaling

Bật tính năng tự động điều chỉnh tỷ lệ. Đây là cốt lõi của **how to set scaling** cho quá trình chuyển đổi CAD‑to‑PDF.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

## Bước 4: Tạo tùy chọn PDF

Liên kết các cài đặt rasterization với tùy chọn xuất PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Bước 5: Xuất ra PDF

Cu cùng, lưu hình ảnh đã render dưới dạng tệp PDF. Bước này hoàn thành quy trình **convert DXF to PDF**.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Lặp lại các bước trên cho bất kỳ tệp CAD bổ sung nào bạn cần xử lý.

## Các vấn đề thường gặp & Khắc phục

| Triệu chứng | Nguyên nhân có thể | Cách khắc phục |
|------------|---------------------|----------------|
| Blank PDF output | Rasterization options not set or file path incorrect | Verify `srcFile` path and ensure `setPageWidth/Height` are non‑zero |
| Distorted scaling | `setAutomaticLayoutsScaling` left as `false` | Enable automatic scaling or manually calculate scaling factor |
| Missing layers | Source DXF contains unsupported entities | Check the Aspose.CAD release notes for supported entity types |

## Câu hỏi thường gặp

### Q1: Aspose.CAD cho Java có tương thích với tất cả các định dạng tệp CAD không?

**A1:** Aspose.CAD for Java hỗ trợ nhiều định dạng CAD, bao gồm DWG, DXF và DWF.

### Q2: Tôi có thể tùy chỉnh thêm các tùy chọn scaling không?

**A2:** Có, lớp `CadRasterizationOptions` cung cấp nhiều thuộc tính để tinh chỉnh scaling và các cài đặt khác.

### Q3: Tôi có thể tìm tài liệu bổ sung cho Aspose.CAD for Java ở đâu?

**A3:** Tham khảo [documentation](https://reference.aspose.com/cad/java/) để biết thông tin chi tiết và các ví dụ.

### Q4: Có bản dùng thử miễn phí cho Aspose.CAD for Java không?

**A4:** Có, bạn có thể khám phá [free trial](https://releasespose.com/) để trải nghiệm các khả năng của Aspose.CAD for Java.

### Q5: Làm sao để tôi nhận được hỗ trợ hoặc tham gia thảo luận về Aspose.CAD for Java?

**A5:** Truy cập [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) để kết nối với cộng đồng và nhận hỗ trợ.

**Các câu hỏi chung bổ sung**

**Q: Làm thế nào để chuyển đổi tệp DWG sang PDF thay vì DXF?**  
**A:** Mã vẫn hoạt động; chỉ cần thay đổi phần mở rộng tệp trong `srcFile` thành `.dwg`.

**Q: Tôi có thể đặt DPI tùy chỉnh cho PDF có độ phân giải cao hơn không?**  
**A:** Có, sử dụng `rasterizationOptions.setResolution(300);` (hoặc bất kỳ DPI nào bạn cần).

**Q: Có thể nhúng phông chữ vào PDF được tạo không?**  
**A:** Aspose.CAD raster hóa bản vẽ, vì vậy phông chữ được render dưới dạng vector; không cần nhúng phông chữ riêng.

## Kết luận

Bằng cách làm theo hướng dẫn này, bạn đã biết cách **create PDF from CAD** bằng Aspose.CAD for Java với Auto Layout Scaling. Quy trình này giúp đơn giản hoá **export CAD to PDF**, đảm bảo tỷ lệ nhất quán và tiết kiệm thời gian phát triển. Hãy thử nghiệm với các kích thước trang, độ phân giải và định dạng CAD khác nhau để đáp ứng nhu cầu dự án của bạn.

---

**Last Updated:** 2025-12-10  
**Tested With:** Aspose.CAD for Java 24.12 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}