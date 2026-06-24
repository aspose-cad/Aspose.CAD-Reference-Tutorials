---
date: 2026-03-02
description: Mở khóa tiềm năng của Aspose.CAD cho Java. Dễ dàng xuất các đối tượng
  OLE và **lưu CAD dưới dạng PNG**. Tải ngay để quản lý dữ liệu CAD một cách liền
  mạch.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: Lưu CAD dưới dạng PNG – Xuất đối tượng OLE bằng Aspose.CAD cho Java
url: /vi/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lưu CAD dưới dạng PNG – Xuất Đối tượng OLE bằng Aspose.CAD cho Java

## Giới thiệu

Trong thế giới năng động của Thiết kế Hỗ trợ Máy tính (CAD), việc quản lý và trích xuất các đối tượng OLE (Object Linking and Embedding) một cách hiệu quả—và có khả năng **save CAD as PNG**—là rất quan trọng cho các quy trình downstream như báo cáo, xem trước trên web, hoặc lưu trữ. Aspose.CAD cho Java cung cấp một giải pháp mạnh mẽ, dựa trên mã, cho phép bạn vừa xuất các đối tượng OLE vừa chuyển đổi bản vẽ CAD thành các hình ảnh PNG chất lượng cao chỉ trong vài dòng mã.

## Câu trả lời nhanh
- **Aspose.CAD làm gì?** Nó đọc, thao tác và chuyển đổi các tệp CAD (DWG, DXF, DGN, v.v.) mà không cần phần mềm CAD gốc.  
- **Có thể lưu CAD dưới dạng PNG không?** Có — sử dụng `PngOptions` cùng với `CadRasterizationOptions` để raster hoá bất kỳ layout nào.  
- **Cách xuất các đối tượng OLE?** Tải tệp CAD bằng `Image.load` và lưu mỗi layout chứa OLE dưới dạng PNG.  
- **Có cần giấy phép không?** Có bản dùng thử miễn phí; giấy phép thương mại sẽ loại bỏ các giới hạn đánh giá.  
- **Yêu cầu phiên bản Java nào?** Java 8 hoặc cao hơn được hỗ trợ đầy đủ.

## save CAD as PNG là gì?
Lưu CAD dưới dạng PNG có nghĩa là raster hoá các bản vẽ CAD dựa trên vector thành hình ảnh PNG dựa trên pixel. Việc chuyển đổi này hữu ích khi bạn cần một định dạng nhẹ, có thể xem được trên mọi nền tảng cho các trang web, ứng dụng di động hoặc tài liệu.

## Tại sao nên dùng Aspose.CAD cho Java để **convert CAD to PNG**?
- **Không cần cài đặt CAD** – thư viện hoạt động hoàn toàn trong Java.  
- **Giữ nguyên độ chính xác layout** – bạn có thể chọn các layout cụ thể, kiểm soát DPI và duy trì chất lượng đường nét.  
- **Xử lý hàng loạt** – lặp qua nhiều tệp bằng một vòng lặp đơn giản.  
- **Xuất đối tượng OLE** – nội dung OLE nhúng trong các tệp DWG/DXF sẽ tự động được render vào đầu ra PNG.

## Yêu cầu trước

Trước khi bắt đầu tutorial, hãy chắc chắn rằng bạn đã chuẩn bị các yêu cầu sau:

- **Môi trường Java** – Đảm bảo bạn đã cài đặt môi trường phát triển Java trên máy.  
- **Aspose.CAD cho Java** – Tải và cài đặt thư viện Aspose.CAD cho Java. Bạn có thể tìm thư viện tại [download link](https://releases.aspose.com/cad/java/).  
- **Tệp CAD** – Chuẩn bị các tệp CAD chứa các đối tượng OLE mà bạn muốn xuất.

## Nhập không gian tên

Để bắt đầu, nhập các không gian tên cần thiết vào dự án Java của bạn. Các không gian tên này cung cấp các lớp và chức năng thiết yếu để làm việc với tệp CAD bằng Aspose.CAD.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Bây giờ, chúng ta sẽ phân tích quy trình xuất các đối tượng OLE từ CAD thành các bước:

## Cách **save CAD as PNG** và xuất các đối tượng OLE

### Bước 1: Đặt Thư mục Tài liệu của Bạn

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

Đảm bảo thay thế `"Your Document Directory"` bằng đường dẫn tới thư mục chứa các tệp CAD của bạn.

### Bước 2: Xác định Tên Tệp CAD

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

Xác định tên các tệp CAD mà bạn muốn xử lý trong mảng `files`.

### Bước 3: Đặt Các Tùy chọn Xuất PNG

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

Cấu hình các tùy chọn xuất PNG, bao gồm raster hoá vector và cài đặt layout. Những tùy chọn này cho phép bạn **convert CAD to PNG** với chất lượng mong muốn.

### Bước 4: Lặp qua Các Tệp CAD

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

Lặp qua mỗi tệp CAD được chỉ định, tải nó bằng Aspose.CAD và lưu các đối tượng OLE dưới dạng hình ảnh PNG. Vòng lặp này minh họa cách đơn giản để **convert DWG to PNG** hàng loạt.

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|-------------|-----------|
| **Blank PNG output** | Không khớp tên layout | Xác nhận rằng tên layout (`"Layout1"`) tồn tại trong DWG nguồn. |
| **Missing OLE graphics** | Các đối tượng OLE được lưu trong một layout khác | Bao gồm tất cả các layout liên quan trong `rasterizationOptions.setLayouts(...)`. |
| **Out‑of‑memory error on large files** | Cài đặt DPI cao | Giảm DPI bằng `rasterizationOptions.setResolution(...)` hoặc xử lý các tệp từng cái một. |

## Câu hỏi thường gặp

**Q: Aspose.CAD có tương thích với tất cả các định dạng tệp CAD không?**  
A: Aspose.CAD hỗ trợ nhiều định dạng CAD, bao gồm DWG, DXF và DGN. Tham khảo [documentation](https://reference.aspose.com/cad/java/) để biết danh sách đầy đủ.

**Q: Tôi có thể tùy chỉnh cài đặt xuất cho các đối tượng OLE không?**  
A: Có, Aspose.CAD cung cấp nhiều tùy chọn để tùy chỉnh cài đặt xuất, cho phép bạn điều chỉnh đầu ra theo yêu cầu cụ thể.

**Q: Có bản dùng thử miễn phí cho Aspose.CAD không?**  
A: Có, bạn có thể khám phá các khả năng của Aspose.CAD bằng cách nhận bản dùng thử miễn phí từ [here](https://releases.aspose.com/).

**Q: Tôi có thể nhận hỗ trợ cộng đồng cho Aspose.CAD ở đâu?**  
A: Tham gia cộng đồng Aspose.CAD tại [forum](https://forum.aspose.com/c/cad/19) để nhận trợ giúp và chia sẻ kinh nghiệm.

**Q: Làm thế nào để mua giấy phép cho Aspose.CAD?**  
A: Truy cập [purchase page](https://purchase.aspose.com/buy) để mua giấy phép phù hợp với nhu cầu phát triển của bạn.

## Kết luận

Với những bước đơn giản nhưng mạnh mẽ này, bạn có thể dễ dàng **save CAD as PNG** đồng thời xuất các đối tượng OLE từ các tệp CAD bằng Aspose.CAD cho Java. Công cụ đa năng này giúp các nhà phát triển quản lý dữ liệu CAD một cách hiệu quả, mở ra những khả năng mới trong phát triển ứng dụng CAD và các quy trình downstream dựa trên hình ảnh.

---

**Cập nhật lần cuối:** 2026-03-02  
**Kiểm tra với:** Aspose.CAD for Java 24.12  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}