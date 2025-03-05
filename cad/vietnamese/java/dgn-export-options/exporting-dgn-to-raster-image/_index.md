---
title: Chuyển đổi Java DGN sang JPEG với Hướng dẫn Aspose.CAD
linktitle: Xuất DGN ở định dạng AutoCAD sang định dạng hình ảnh raster
second_title: API Java Aspose.CAD
description: Tìm hiểu cách xuất tệp DGN sang hình ảnh JPEG trong Java bằng Aspose.CAD. Hướng dẫn từng bước này sẽ hướng dẫn bạn thực hiện quy trình một cách dễ dàng.
type: docs
weight: 13
url: /vi/java/dgn-export-options/exporting-dgn-to-raster-image/
---
## Giới thiệu

Chào mừng bạn đến với hướng dẫn toàn diện này về cách xuất tệp DGN (Thiết kế) sang Định dạng Hình ảnh Raster bằng Aspose.CAD cho Java. Aspose.CAD là một thư viện mạnh mẽ cho phép các nhà phát triển Java làm việc liền mạch với các tệp CAD. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn quy trình chuyển đổi tệp DGN thành hình ảnh JPEG, cung cấp cho bạn hướng dẫn từng bước và ví dụ về mã.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:
1.  Thư viện Aspose.CAD: Đảm bảo bạn đã cài đặt thư viện Aspose.CAD cho Java. Bạn có thể tải nó xuống[đây](https://releases.aspose.com/cad/java/).
2. Bộ công cụ phát triển Java (JDK): Đảm bảo bạn đã cài đặt Java trên máy của mình.
3. Môi trường phát triển tích hợp (IDE): Sử dụng IDE tương thích với Java như IntelliJ hoặc Eclipse.

## Gói nhập khẩu

Trong dự án Java của bạn, hãy nhập các gói cần thiết cho Aspose.CAD. Thêm các dòng sau vào mã của bạn:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## Bước 1: Tải tệp DGN

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## Bước 2: Tạo đối tượng JpegOptions

```java
ImageOptionsBase options = new JpegOptions();
```

## Bước 3: Chỉ định các tùy chọn Rasterization

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## Bước 4: Lưu hình ảnh đã chuyển đổi

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

Lặp lại các bước này cho các tệp DGN cụ thể của bạn, điều chỉnh đường dẫn tệp cho phù hợp.

## Phần kết luận

Chúc mừng! Bạn đã học thành công cách xuất tệp DGN sang Định dạng hình ảnh Raster bằng Aspose.CAD cho Java. Hướng dẫn này đã trang bị cho bạn kiến thức để kết hợp chức năng này vào các ứng dụng Java của bạn.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.CAD cho Java với các định dạng tệp CAD khác không?

Câu trả lời 1: Có, Aspose.CAD hỗ trợ nhiều định dạng CAD khác nhau, cung cấp giải pháp linh hoạt cho các nhà phát triển Java.

### Câu hỏi 2: Có bản dùng thử miễn phí cho Aspose.CAD cho Java không?

 Câu trả lời 2: Có, bạn có thể truy cập bản dùng thử miễn phí[đây](https://releases.aspose.com/).

### Câu hỏi 3: Tôi có thể tìm tài liệu về Aspose.CAD cho Java ở đâu?

 A3: Tham khảo tài liệu[đây](https://reference.aspose.com/cad/java/).

### Câu hỏi 4: Làm cách nào tôi có thể nhận được hỗ trợ cho Aspose.CAD cho Java?

 A4: Truy cập diễn đàn hỗ trợ[đây](https://forum.aspose.com/c/cad/19).

### Câu hỏi 5: Tôi có thể mua giấy phép Aspose.CAD cho Java ở đâu?

 A5: Bạn có thể mua giấy phép[đây](https://purchase.aspose.com/buy).