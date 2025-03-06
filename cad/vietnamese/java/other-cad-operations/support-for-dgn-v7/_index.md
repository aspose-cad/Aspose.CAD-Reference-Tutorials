---
title: Hướng dẫn chuyển đổi DGN sang PDF - Aspose.CAD cho Java
linktitle: Hỗ trợ cho DGN V7
second_title: API Java Aspose.CAD
description: Dễ dàng chuyển đổi tệp DGN sang PDF bằng Aspose.CAD cho Java. Hãy làm theo hướng dẫn từng bước của chúng tôi để tích hợp liền mạch và quy trình làm việc hiệu quả.
weight: 11
url: /vi/java/other-cad-operations/support-for-dgn-v7/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hướng dẫn chuyển đổi DGN sang PDF - Aspose.CAD cho Java

## Giới thiệu

Trong thế giới năng động của CAD (Thiết kế hỗ trợ máy tính), việc chuyển đổi hiệu quả các tệp DGN (Thiết kế) sang PDF (Định dạng tài liệu di động) là một yêu cầu quan trọng. Aspose.CAD cho Java nổi lên như một giải pháp mạnh mẽ, cung cấp khả năng tích hợp liền mạch và mạnh mẽ. Hướng dẫn từng bước này nhằm mục đích hướng dẫn bạn quy trình xuất tệp DGN sang PDF bằng Aspose.CAD cho Java, đảm bảo quy trình làm việc suôn sẻ và hiệu quả.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:
-  Thư viện Aspose.CAD cho Java: Tải xuống và cài đặt thư viện từ[Trang tải xuống Aspose.CAD cho Java](https://releases.aspose.com/cad/java/).
- Môi trường phát triển Java: Đảm bảo bạn đã thiết lập môi trường phát triển Java trên máy của mình.

## Gói nhập khẩu

Bắt đầu bằng cách nhập các gói cần thiết vào dự án Java của bạn:

## Bước 1: Nhập các gói cần thiết

Trong dự án Java của bạn, hãy nhập các gói cần thiết cho Aspose.CAD for Java.
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.cadobjects.DgnImage;
import com.aspose.cad.imageoptions.PdfOptions;
import java.awt.Color;
```

## Bước 2: Đặt đường dẫn tệp

Xác định đường dẫn cho tệp DGN đầu vào của bạn và tệp PDF đầu ra.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

## Bước 3: Tải hình ảnh DGN

Tải hình ảnh DGN bằng thư viện Aspose.CAD.

```java
DgnImage objImage = (DgnImage)Image.load(fileName);
```

## Bước 4: Định cấu hình tùy chọn xuất PDF

Thiết lập các tùy chọn để xuất sang PDF, bao gồm kích thước trang, chia tỷ lệ bố cục tự động, màu nền và bố cục cụ thể để xuất.

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setBackgroundColor(Color.getBlack());
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); //chỉ xuất 4 lượt xem (1,2,3 và 9)
options.setVectorRasterizationOptions(vectorOptions);
```

## Bước 5: Lưu tệp PDF

Lưu hình ảnh DGN dưới dạng tệp PDF với các tùy chọn được chỉ định.

```java
objImage.save(outFile, options);
```

Lặp lại các bước này cho các tệp DGN khác nhau, điều chỉnh đường dẫn và tùy chọn tệp nếu cần.

## Phần kết luận

Với Aspose.CAD cho Java, việc chuyển đổi tệp DGN sang PDF trở thành một quá trình đơn giản. Hướng dẫn này trang bị cho bạn kiến thức để tích hợp liền mạch thư viện vào các dự án Java của bạn, tạo điều kiện chuyển đổi tệp CAD hiệu quả.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.CAD cho Java với các định dạng tệp CAD khác không?

Câu trả lời 1: Có, Aspose.CAD hỗ trợ nhiều định dạng CAD khác nhau, cung cấp chức năng linh hoạt ngoài khả năng chuyển đổi DGN sang PDF.

### Câu hỏi 2: Giấy phép tạm thời có sẵn cho Aspose.CAD cho Java không?

 A2: Có, bạn có thể xin giấy phép tạm thời[đây](https://purchase.aspose.com/temporary-license/) cho mục đích thử nghiệm.

### Câu hỏi 3: Làm cách nào tôi có thể tìm kiếm hỗ trợ hoặc đặt câu hỏi về Aspose.CAD cho Java?

 A3: Tham quan[Diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19)để kết nối với cộng đồng và tìm kiếm sự giúp đỡ.

### Câu hỏi 4: Tôi có thể xuất những bố cục nào khi chuyển đổi DGN sang PDF?

 A4: Bạn có thể chỉ định bố cục để xuất bằng cách tùy chỉnh`setLayouts` mảng trong mã.

### Câu hỏi 5: Tôi có thể tìm tài liệu toàn diện về Aspose.CAD cho Java ở đâu?

 A5: Hãy tham khảo[Aspose.CAD cho tài liệu Java](https://reference.aspose.com/cad/java/) để biết thông tin chi tiết.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
