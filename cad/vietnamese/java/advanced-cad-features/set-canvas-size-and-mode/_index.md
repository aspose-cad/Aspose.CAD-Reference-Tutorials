---
title: Đặt kích thước và chế độ canvas
linktitle: Đặt kích thước và chế độ canvas
second_title: API Java Aspose.CAD
description: Khám phá sức mạnh của Aspose.CAD cho Java với hướng dẫn từng bước của chúng tôi về cách đặt kích thước và chế độ canvas. Dễ dàng chuyển đổi tệp CAD sang định dạng PDF và TIFF.
type: docs
weight: 16
url: /vi/java/advanced-cad-features/set-canvas-size-and-mode/
---
## Giới thiệu

Bạn đang muốn khai thác sức mạnh của Aspose.CAD cho Java để nâng cao quá trình chuyển đổi CAD của mình? Hướng dẫn toàn diện này sẽ hướng dẫn bạn các bước cài đặt kích thước và chế độ canvas bằng Aspose.CAD cho Java. Cho dù bạn là nhà phát triển dày dạn kinh nghiệm hay chỉ mới bắt đầu, hướng dẫn này sẽ cung cấp cho bạn thông tin chi tiết bạn cần.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

-  Aspose.CAD cho Java: Đảm bảo rằng bạn đã cài đặt thư viện Aspose.CAD trong môi trường Java của mình. Bạn có thể tải nó xuống[đây](https://releases.aspose.com/cad/java/).

- Thư mục tài liệu: Thiết lập thư mục tài liệu để lưu trữ các tệp CAD của bạn. Thư mục này sẽ được tham chiếu trong các bước hướng dẫn.

Bây giờ, hãy bắt đầu với hướng dẫn từng bước.

## Nhập không gian tên

Trong bước này, chúng tôi sẽ nhập các vùng tên cần thiết để khởi động dự án Aspose.CAD của bạn.
```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Bước 1: Nhập các lớp Aspose.CAD

```java
// Đường dẫn đến thư mục tài nguyên.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

 Trong đoạn mã này, chúng tôi thiết lập đường dẫn đến thư mục tài nguyên và tải tệp DXF bằng Aspose.CAD`Image` lớp học.

## Bước 2: Đặt thuộc tính CadRasterizationOptions

```java
// Tạo một phiên bản CadRasterizationOptions và đặt các thuộc tính khác nhau của nó
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

 Ở đây, chúng ta tạo một thể hiện của`CadRasterizationOptions` và định cấu hình các thuộc tính như chiều rộng trang, chiều cao trang và tùy chọn chia tỷ lệ.

## Bước 3: Tạo PdfOptions và đặt VectorRasterizationOptions

```java
// Tạo một phiên bản của PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Đặt thuộc tính VectorRasterizationOptions
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

 Bây giờ, chúng ta tạo ra một`PdfOptions` ví dụ và thiết lập nó`VectorRasterizationOptions` thuộc tính được cấu hình trước đó`CadRasterizationOptions`.

## Bước 4: Xuất sang PDF

```java
// Xuất CAD sang PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Cuối cùng, chúng tôi lưu hình ảnh CAD vào tệp PDF bằng các tùy chọn đã chỉ định.

## Bước 5: Tạo TiffOptions và đặt VectorRasterizationOptions

```java
// Tạo một phiên bản của TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Đặt thuộc tính VectorRasterizationOptions
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Ở bước này, chúng ta thiết lập một`TiffOptions` dụ và cấu hình nó`VectorRasterizationOptions` tài sản.

## Bước 6: Xuất sang TIFF

```java
// Xuất CAD sang TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Cuối cùng, chúng tôi lưu hình ảnh CAD vào tệp TIFF bằng các tùy chọn đã chỉ định.

## Phần kết luận

 Chúc mừng! Bạn đã đặt thành công kích thước và chế độ canvas bằng Aspose.CAD cho Java. Hướng dẫn này cung cấp nền tảng vững chắc cho các dự án chuyển đổi CAD của bạn. Khám phá thêm các tính năng và khả năng trong[Tài liệu Aspose.CAD](https://reference.aspose.com/cad/java/).

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.CAD cho Java với các khung Java khác không?

Câu trả lời 1: Có, Aspose.CAD được thiết kế để tích hợp liền mạch với nhiều khung công tác Java khác nhau.

### Câu hỏi 2: Aspose.CAD có giấy phép tạm thời không?

 A2: Có, bạn có thể xin giấy phép tạm thời[đây](https://purchase.aspose.com/temporary-license/).

### Câu 3: Tôi có thể nhận hỗ trợ cộng đồng cho Aspose.CAD ở đâu?

 A3: Tham quan[Diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để được cộng đồng hỗ trợ và thảo luận.

### Q4: Tôi có thể dùng thử Aspose.CAD miễn phí không?

 A4: Chắc chắn rồi! Nhận bản dùng thử miễn phí[đây](https://releases.aspose.com/).

### Câu hỏi 5: Làm cách nào để mua Aspose.CAD cho Java?

 A5: Mua sản phẩm[đây](https://purchase.aspose.com/buy).