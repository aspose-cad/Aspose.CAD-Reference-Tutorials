---
date: 2026-02-17
description: Học cách chuyển đổi DWG sang PNG và xuất CAD dưới dạng PNG hoặc các định
  dạng raster khác bằng Aspose.CAD cho Java. Nhận kết quả chất lượng cao nhanh chóng.
linktitle: Convert CAD Layout to Raster Image Format
second_title: Aspose.CAD Java API
title: Chuyển đổi DWG sang PNG và các định dạng raster khác bằng Aspose.CAD cho Java
url: /vi/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

 translation.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chuyển đổi DWG sang PNG và các Định dạng Raster Khác bằng Aspose.CAD cho Java

## Giới thiệu

Việc chuyển đổi DWG sang PNG (hoặc các định dạng ảnh raster khác) là một nhu cầu phổ biến khi bạn cần chia sẻ bản vẽ CAD với đồng nghiệp không có trình xem CAD, nhúng thiết kế vào tài liệu, hoặc tạo thumbnail cho các bộ sưu tập web. **Trong hướng dẫn này bạn sẽ học cách chuyển đổi dwg sang png một cách nhanh chóng và đáng tin cậy**, dù bạn đang làm việc với một tệp bản vẽ đầy đủ hay chỉ một layout cụ thể. Bạn cũng có thể cần **chuyển đổi CAD sang raster** cho các bản xem trước trên web, công cụ báo cáo, hoặc ứng dụng di động. Aspose.CAD cho Java giúp quá trình chuyển đổi này trở nên đơn giản và cho phép bạn kiểm soát hoàn toàn độ phân giải, lựa chọn layout và định dạng đầu ra.

## Câu trả lời nhanh
- **Thư viện nào xử lý DWG sang PNG?** Aspose.CAD cho Java  
- **Những định dạng nào có thể xuất?** PNG, JPEG, TIFF, PDF, BMP và nhiều hơn nữa  
- **Có cần giấy phép để thử nghiệm không?** Bản dùng thử miễn phí hoạt động cho phát triển; cần giấy phép cho môi trường sản xuất  
- **Có thể chọn một layout cụ thể không?** Có, dùng `setLayouts` để chỉ định “Model”, “Layout1”, v.v.  
- **Có thể xuất ra độ phân giải cao không?** Chắc chắn—điều chỉnh `setPageWidth` và `setPageHeight` để kiểm soát DPI  

## “convert dwg to png” là gì?

Cụm từ “convert dwg to png” mô tả quá trình lấy một tệp DWG dựa trên vector (định dạng gốc của nhiều ứng dụng CAD) và raster hoá nó thành một ảnh PNG dựa trên pixel. Ảnh raster rất phù hợp cho hiển thị trên web, chia sẻ qua email và tích hợp vào phần mềm không phải CAD.

## Tại sao xuất CAD dưới dạng PNG (hoặc các định dạng raster khác)?

- **Tương thích toàn cầu:** PNG và JPEG được hỗ trợ bởi hầu hết các trình xem ảnh và trình duyệt.  
- **Tải nhanh:** Ảnh raster tải ngay lập tức so với việc mở một tệp DWG nặng.  
- **Dễ nhúng:** Chèn PNG trực tiếp vào Word, PowerPoint hoặc HTML mà không cần plugin bổ sung.  
- **Hiển thị đồng nhất:** Bạn kiểm soát độ phân giải, nền và layout, đảm bảo mọi người đều nhìn thấy cùng một hình ảnh.  

## Các trường hợp sử dụng phổ biến

| Kịch bản | Lý do raster giúp ích |
|----------|------------------------|
| **Tài liệu dự án** | Nhúng PNG vào PDF hoặc Word tránh yêu cầu phần mềm CAD cho người xem. |
| **Cổng thông tin web** | Thumbnail tạo từ tệp DWG tải ngay và cải thiện trải nghiệm người dùng. |
| **Ứng dụng di động** | Ảnh raster hiển thị đúng trên các thiết bị không có trình xem CAD. |
| **Báo cáo tự động** | Chuyển đổi hàng loạt nhiều layout sang PNG/JPEG để đưa vào biểu đồ hoặc bảng điều khiển. |

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn đã có:

1. **Môi trường phát triển Java** – JDK 8 trở lên đã được cài đặt và cấu hình.  
2. **Aspose.CAD cho Java** – Tải JAR mới nhất từ [tài liệu Aspose.CAD cho Java](https://reference.aspose.com/cad/java/).  

## Nhập không gian tên

Đầu tiên, nhập các lớp cần thiết. Những import này cho phép bạn tải ảnh, tùy chọn raster hoá và cài đặt xuất TIFF/PNG.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

> **Mẹo chuyên nghiệp:** Nếu bạn muốn **xuất CAD dưới dạng PNG** thay vì TIFF, thay `TiffOptions` bằng `PngOptions` (tìm trong `com.aspose.cad.imageoptions.PngOptions`).

## Hướng dẫn từng bước

### Bước 1: Thiết lập thư mục tài nguyên

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

Thay `"Your Document Directory"` bằng đường dẫn tuyệt đối nơi lưu trữ các tệp CAD của bạn.

### Bước 2: Tải tệp CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

Bạn có thể tải bất kỳ định dạng hỗ trợ nào (DWG, DXF, DGN, v.v.). Đây là phần **cách chuyển đổi cad**—chỉ cần chỉ tới tệp và để Aspose xử lý việc phân tích.

### Bước 3: Cấu hình tùy chọn raster hoá

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

- `setPageWidth` / `setPageHeight` kiểm soát độ phân giải đầu ra (giá trị lớn hơn = DPI cao hơn).  
- `setLayouts` cho phép bạn **chuyển đổi CAD sang raster** cho các layout cụ thể; bỏ qua nó để raster hoá toàn bộ bản vẽ.

### Bước 4: Đặt tùy chọn ảnh

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

Nếu bạn muốn PNG, khởi tạo `PngOptions` thay vì `TiffOptions`. Đây là nơi bạn **xuất CAD dưới dạng PNG**.

### Bước 5: Lưu ảnh kết quả

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

Thay đổi phần mở rộng tệp thành `.png` (và đối tượng options thành `PngOptions`) để **lưu CAD dưới dạng JPEG/PNG**.

> **Sai lầm thường gặp:** Quên đồng bộ phần mở rộng tệp với lớp options sẽ gây ra `UnsupportedFormatException`. Luôn giữ chúng nhất quán.

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Giải pháp |
|-------|----------|
| **Ảnh đầu ra trắng** | Kiểm tra tên layout trong `setLayouts` có khớp chính xác với tên trong tệp CAD nguồn không. |
| **PNG độ phân giải thấp** | Tăng `setPageWidth` / `setPageHeight` hoặc đặt `setResolution` trên tùy chọn raster hoá. |
| **Phiên bản DWG không được hỗ trợ** | Đảm bảo bạn đang dùng phiên bản Aspose.CAD mới nhất; các phiên bản cũ có thể không hỗ trợ DWG mới. |
| **Lỗi bộ nhớ với tệp lớn** | Xử lý từng trang một hoặc tăng heap JVM (`-Xmx2g`). |

## Câu hỏi thường gặp

**H: Aspose.CAD có tương thích với các định dạng tệp CAD khác nhau không?**  
Đ: Có, nó hỗ trợ DWG, DXF, DGN và nhiều định dạng khác.

**H: Tôi có thể tùy chỉnh độ phân giải của ảnh raster đầu ra không?**  
Đ: Chắc chắn. Điều chỉnh `setPageWidth`, `setPageHeight`, hoặc `setResolution` trong `CadRasterizationOptions`.

**H: Làm sao để chuyển đổi nhiều layout CAD trong một lần chạy?**  
Đ: Cung cấp một mảng chứa tất cả tên layout cho `setLayouts`, ví dụ `new String[]{"Model","Layout1","Layout2"}`.

**H: Có định dạng đầu ra nào khác ngoài TIFF không?**  
Đ: Có—PNG, JPEG, BMP, PDF và nhiều hơn nữa thông qua các lớp `*Options` tương ứng.

**H: Tôi có thể nhận hỗ trợ hoặc chia sẻ kinh nghiệm với Aspose.CAD ở đâu?**  
Đ: Truy cập [diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để nhận hỗ trợ cộng đồng và trợ giúp chính thức.

## Kết luận

Bằng cách làm theo các bước trên, bạn có thể **chuyển đổi DWG sang PNG**, **xuất CAD dưới dạng PNG**, **lưu CAD dưới dạng JPEG**, hoặc tạo bất kỳ định dạng raster nào khác mà bạn cần. Aspose.CAD cho Java thực hiện phần công việc nặng, cho phép bạn tập trung vào việc tích hợp các ảnh chất lượng cao vào ứng dụng, tài liệu hoặc cổng thông tin web của mình.

---

**Cập nhật lần cuối:** 2026-02-17  
**Đã kiểm tra với:** Aspose.CAD cho Java 24.12  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}