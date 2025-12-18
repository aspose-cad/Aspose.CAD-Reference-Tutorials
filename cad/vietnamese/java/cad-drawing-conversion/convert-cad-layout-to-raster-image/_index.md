---
date: 2025-12-18
description: Tìm hiểu cách chuyển đổi DWG sang PNG và các định dạng ảnh raster khác
  với Aspose.CAD cho Java. Xuất CAD dưới dạng PNG với kết quả chất lượng cao.
linktitle: Convert CAD Layout to Raster Image Format
second_title: Aspose.CAD Java API
title: Chuyển đổi DWG sang PNG và các định dạng raster khác bằng Aspose.CAD cho Java
url: /vi/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Chuyển đổi DWG sang PNG và Các Định dạng Raster Khác Sử dụng Aspose.CAD cho Java

## Giới thiệu

Việc chuyển đổi DWG sang PNG (hoặc các định dạng ảnh raster khác) là một nhu cầu phổ biến khi bạn cần chia sẻ bản vẽ CAD với đồng nghiệp không có trình xem CAD, nhúng thiết kế vào tài liệu, hoặc tạo thumbnail cho các bộ sưu tập web. Aspose.CAD cho Java giúp quá trình chuyển đổi này trở nên đơn giản, bất kể bạn đang làm việc với một file bản vẽ đầy đủ hay chỉ một layout cụ thể. Trong hướng dẫn này, chúng ta sẽ đi qua các bước **chuyển đổi một layout CAD sang ảnh raster** — kỹ thuật bạn có thể áp dụng để tạo ra PNG, JPEG, TIFF hoặc PDF.

## Câu trả lời nhanh
- **Thư viện nào xử lý DWG sang PNG?** Aspose.CAD for Java  
- **Các định dạng nào có thể xuất?** PNG, JPEG, TIFF, PDF, BMP, và hơn nữa  
- **Tôi có cần giấy phép để thử nghiệm không?** Bản dùng thử miễn phí hoạt động cho phát triển; cần giấy phép cho môi trường sản xuất  
- **Tôi có thể chọn một layout cụ thể không?** Có, sử dụng `setLayouts` để chỉ định “Model”, “Layout1”, v.v.  
- **Có thể xuất hình ảnh độ phân giải cao không?** Chắc chắn—điều chỉnh `setPageWidth` và `setPageHeight` để kiểm soát DPI  

## Convert dwg to png là gì?

Cụm từ “convert dwg to png” mô tả quá trình lấy một file DWG dựa trên vector (định dạng gốc của nhiều ứng dụng CAD) và raster hoá nó thành một ảnh PNG dựa trên pixel. Ảnh raster rất phù hợp cho hiển thị trên web, chia sẻ qua email và tích hợp vào phần mềm không phải CAD.

## Tại sao xuất CAD dưới dạng PNG (hoặc các định dạng raster khác)?

- **Tương thích toàn cầu:** PNG và JPEG được hầu hết mọi trình xem ảnh và trình duyệt hỗ trợ.  
- **Tải nhanh:** Hình raster tải ngay lập tức so với việc mở một file DWG nặng.  
- **Dễ nhúng:** Chèn PNG trực tiếp vào Word, PowerPoint hoặc HTML mà không cần plugin bổ sung.  
- **Hiển thị nhất quán:** Bạn kiểm soát độ phân giải, nền và layout, đảm bảo mọi bên liên quan nhìn thấy cùng một hình ảnh.  

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn có:

1. **Môi trường phát triển Java** – JDK 8 hoặc mới hơn đã được cài đặt và cấu hình.  
2. **Aspose.CAD cho Java** – Tải JAR mới nhất từ [tài liệu Aspose.CAD cho Java](https://reference.aspose.com/cad/java/).  

## Nhập không gian tên

Đầu tiên, nhập các lớp bạn sẽ cần. Những import này cho phép bạn truy cập vào việc tải ảnh, tùy chọn rasterization và cài đặt xuất TIFF/PNG.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

> **Mẹo:** Nếu bạn dự định xuất sang PNG thay vì TIFF, thay thế `TiffOptions` bằng `PngOptions` (tìm trong `com.aspose.cad.imageoptions.PngOptions`).

## Hướng dẫn từng bước

### Bước 1: Thiết lập thư mục tài nguyên

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

Thay `"Your Document Directory"` bằng đường dẫn tuyệt đối nơi chứa các file CAD của bạn.

### Bước 2: Tải file CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

Bạn có thể tải bất kỳ định dạng được hỗ trợ nào (DWG, DXF, DGN, v.v.). Đây là phần **how to convert cad** — chỉ cần chỉ tới file và để Aspose xử lý việc phân tích.

### Bước 3: Cấu hình tùy chọn rasterization

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

- `setPageWidth` / `setPageHeight` kiểm soát độ phân giải đầu ra (giá trị lớn hơn = DPI cao hơn).  
- `setLayouts` cho phép bạn **convert cad to raster** cho các layout cụ thể; bỏ qua nó để raster hoá toàn bộ bản vẽ.

### Bước 4: Đặt tùy chọn hình ảnh

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

Nếu bạn muốn PNG, khởi tạo `PngOptions` thay vì `TiffOptions`. Đây là nơi bạn **export cad as png**.

### Bước 5: Lưu hình ảnh kết quả

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

Thay đổi phần mở rộng file thành `.png` (và đối tượng options thành `PngOptions`) để **save CAD as JPEG/PNG**.

> **Cạm bẫy thường gặp:** Quên đồng bộ phần mở rộng file với lớp options sẽ gây ra `UnsupportedFormatException`. Luôn giữ chúng nhất quán.

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Giải pháp |
|-------|----------|
| **Ảnh đầu ra trắng** | Kiểm tra lại tên layout trong `setLayouts` phải khớp chính xác với tên trong file CAD nguồn. |
| **PNG độ phân giải thấp** | Tăng `setPageWidth` / `setPageHeight` hoặc đặt `setResolution` trong tùy chọn rasterization. |
| **Phiên bản DWG không được hỗ trợ** | Đảm bảo bạn đang dùng phiên bản Aspose.CAD mới nhất; các phiên bản cũ có thể không hỗ trợ các bản DWG mới. |
| **Lỗi bộ nhớ khi xử lý file lớn** | Xử lý từng trang một hoặc tăng heap JVM (`-Xmx2g`). |

## Câu hỏi thường gặp

**Q: Aspose.CAD có tương thích với các định dạng file CAD khác nhau không?**  
A: Có, nó hỗ trợ DWG, DXF, DGN và nhiều định dạng khác.

**Q: Tôi có thể tùy chỉnh độ phân giải của ảnh raster đầu ra không?**  
A: Chắc chắn. Điều chỉnh `setPageWidth`, `setPageHeight` hoặc `setResolution` trong `CadRasterizationOptions`.

**Q: Làm sao để chuyển đổi nhiều layout CAD trong một lần chạy?**  
A: Cung cấp một mảng chứa tất cả tên layout cho `setLayouts`, ví dụ `new String[]{"Model","Layout1","Layout2"}`.

**Q: Có định dạng xuất nào ngoài TIFF được hỗ trợ không?**  
A: Có — PNG, JPEG, BMP, PDF và các định dạng khác có sẵn qua các lớp `*Options` tương ứng.

**Q: Tôi có thể nhận hỗ trợ hoặc chia sẻ kinh nghiệm với Aspose.CAD ở đâu?**  
A: Truy cập [diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để được cộng đồng hỗ trợ và nhận trợ giúp chính thức.

## Kết luận

Bằng cách thực hiện các bước trên, bạn có thể **convert DWG to PNG**, **export CAD as PNG**, **save CAD as JPEG**, hoặc tạo ra bất kỳ định dạng raster nào bạn cần. Aspose.CAD cho Java thực hiện phần công việc nặng, cho phép bạn tập trung vào việc tích hợp hình ảnh chất lượng cao vào ứng dụng, tài liệu hoặc cổng thông tin web của mình.

---

**Last Updated:** 2025-12-18  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}