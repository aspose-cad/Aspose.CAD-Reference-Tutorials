---
title: Xuất STL sang PNG bằng Aspose.CAD cho Java
linktitle: Xuất STL sang PNG
second_title: API Java Aspose.CAD
description: Khám phá quy trình xuất tệp STL sang PNG trong Java một cách liền mạch với Aspose.CAD. Đơn giản hóa quy trình làm việc của bạn và nâng cao các dự án Java của bạn một cách dễ dàng.
weight: 20
url: /vi/java/cad-export-options/export-stl-to-png/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xuất STL sang PNG bằng Aspose.CAD cho Java

## Giới thiệu

Bạn đang muốn xuất tệp STL sang PNG bằng Java? Aspose.CAD cho Java chính là giải pháp bạn cần! Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn từng bước thực hiện quy trình. Là một người viết SEO thành thạo, tôi sẽ đảm bảo nội dung không chỉ mang tính thông tin mà còn được tối ưu hóa cho các công cụ tìm kiếm.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

- Bộ công cụ phát triển Java (JDK) được cài đặt trên máy của bạn.
-  Đã tải xuống thư viện Aspose.CAD cho Java. Bạn có thể lấy nó[đây](https://releases.aspose.com/cad/java/).
-  Giấy phép hợp lệ hoặc giấy phép tạm thời từ[đây](https://purchase.aspose.com/temporary-license/).

## Nhập không gian tên

Trong dự án Java của bạn, hãy nhập các không gian tên cần thiết:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Bây giờ, hãy chia ví dụ thành nhiều bước.

## Bước 1: Thiết lập dự án của bạn

Tạo một dự án Java mới và thêm thư viện Aspose.CAD cho Java vào các phần phụ thuộc của dự án của bạn.

## Bước 2: Chỉ định tệp STL của bạn

Xác định đường dẫn đến tệp STL của bạn. Ví dụ:

```java
String dataDir = "Your Document Directory" + "ExportingSTL/";
String fileName = dataDir + "example.stl";
```

## Bước 3: Tải tệp STL

 Tải tệp STL bằng cách sử dụng`Image.load` phương pháp:

```java
CadImage cadImage = (CadImage)Image.load(fileName);
```

## Bước 4: Định cấu hình tùy chọn Rasterization

Thiết lập các tùy chọn rasterization cho vectorization:

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

## Bước 5: Định cấu hình tùy chọn PNG

Chỉ định các tùy chọn để xuất PNG:

```java
PngOptions pngOptions = new PngOptions();
// Bỏ ghi chú dòng bên dưới nếu bạn muốn đặt tùy chọn rasterization vector
// pngOptions.setVectorRasterizationOptions(vectorOptions);
```

## Bước 6: Lưu dưới dạng PNG

Lưu hình ảnh CAD dưới dạng tệp PNG:

```java
String outPath = dataDir + "galeon.stl.png";
cadImage.save(outPath, pngOptions);
```

Chúc mừng! Bạn đã xuất thành công tệp STL sang PNG bằng Aspose.CAD cho Java.

## Phần kết luận

Trong hướng dẫn này, chúng tôi đã khám phá cách tận dụng Aspose.CAD cho Java để xuất tệp STL sang PNG một cách dễ dàng. Thư viện mạnh mẽ này đơn giản hóa các tác vụ phức tạp, biến nó thành tài sản quý giá cho các dự án Java của bạn.

## Câu hỏi thường gặp

### Câu hỏi 1: Aspose.CAD cho Java có tương thích với tất cả các phiên bản tệp STL không?

Câu trả lời 1: Aspose.CAD cho Java hỗ trợ nhiều phiên bản tệp STL khác nhau, đảm bảo khả năng tương thích với hầu hết các định dạng phổ biến.

### Câu hỏi 2: Tôi có thể sử dụng Aspose.CAD cho Java trong một dự án thương mại không?

 A2: Có, bạn có thể. Đơn giản chỉ cần có được giấy phép hợp lệ từ[đây](https://purchase.aspose.com/buy).

### Câu hỏi 3: Tôi có cần giấy phép tạm thời để dùng thử miễn phí không?

 Câu trả lời 3: Không, giấy phép tạm thời không cần thiết để dùng thử miễn phí. Bạn có thể bắt đầu ngay với phiên bản dùng thử[đây](https://releases.aspose.com/).

### Câu hỏi 4: Tôi có thể tìm thêm hỗ trợ hoặc đặt câu hỏi ở đâu?

 A4: Truy cập diễn đàn Aspose.CAD[đây](https://forum.aspose.com/c/cad/19) cho bất kỳ hỗ trợ hoặc truy vấn.

### Câu hỏi 5: Có tài liệu đầy đủ nào không?

 A5: Có, tài liệu có thể được tìm thấy[đây](https://reference.aspose.com/cad/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
