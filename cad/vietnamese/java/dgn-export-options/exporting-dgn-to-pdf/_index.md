---
title: Xuất DGN sang AutoCAD PDF dễ dàng bằng Aspose.CAD cho Java
linktitle: Xuất DGN ở định dạng AutoCAD sang PDF
second_title: API Java Aspose.CAD
description: Khám phá hướng dẫn từng bước về cách xuất tệp DGN sang định dạng AutoCAD ở dạng PDF bằng Aspose.CAD cho Java. Nâng cao khả năng xử lý CAD của ứng dụng Java của bạn một cách dễ dàng.
weight: 12
url: /vi/java/dgn-export-options/exporting-dgn-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xuất DGN sang AutoCAD PDF dễ dàng bằng Aspose.CAD cho Java

## Giới thiệu

Chào mừng bạn đến với hướng dẫn toàn diện về cách sử dụng Aspose.CAD cho Java để xuất tệp DGN ở định dạng AutoCAD sang PDF. Nếu bạn đang tìm cách nâng cao khả năng xử lý các tệp CAD của ứng dụng Java thì Aspose.CAD là một lựa chọn tuyệt vời. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn từng bước trong quá trình xuất tệp DGN.


## Điều kiện tiên quyết
Trước khi chúng ta đi sâu vào hướng dẫn, hãy đảm bảo bạn có các điều kiện tiên quyết sau:
-  Thư viện Aspose.CAD: Đảm bảo rằng bạn đã cài đặt thư viện Aspose.CAD cho Java. Bạn có thể tải nó xuống[đây](https://releases.aspose.com/cad/java/).
- Thư mục Tài liệu: Thiết lập thư mục tài liệu nơi các tệp đầu vào và đầu ra của bạn sẽ được lưu trữ.

## Gói nhập khẩu

Trong dự án Java của bạn, hãy nhập các gói cần thiết để truy cập các chức năng của Aspose.CAD:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Bây giờ, hãy chia mã ví dụ thành nhiều bước:

## Bước 1: Xác định đường dẫn tệp

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

Đảm bảo thay thế "Thư mục tài liệu của bạn" bằng đường dẫn thực tế nơi chứa tệp của bạn.

## Bước 2: Tải hình ảnh DGN

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Tải tệp DGN bằng Aspose.CAD.

## Bước 3: Đặt tùy chọn xuất PDF

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Xuất các chế độ xem cụ thể
options.setVectorRasterizationOptions(vectorOptions);
```

Xác định các tùy chọn xuất PDF, bao gồm kích thước trang và tùy chọn bố cục.

## Bước 4: Lưu tệp PDF

```java
objImage.save(outFile, options);
```

Lưu tệp PDF đã xuất.

Lặp lại các bước này cho bất kỳ tệp DGN bổ sung nào mà bạn muốn chuyển đổi. Chúc mừng! Bạn đã xuất thành công tệp DGN sang định dạng AutoCAD ở dạng PDF bằng Aspose.CAD cho Java.

## Phần kết luận

Trong hướng dẫn này, chúng tôi đã khám phá cách tận dụng Aspose.CAD cho Java để nâng cao khả năng xử lý tệp CAD cho ứng dụng của bạn. Với các bước dễ thực hiện và ví dụ về mã, giờ đây bạn có thể xuất liền mạch các tệp DGN sang định dạng AutoCAD ở dạng PDF.

## Câu hỏi thường gặp

### Câu hỏi 1: Aspose.CAD có tương thích với tất cả các định dạng tệp CAD không?

Câu trả lời 1: Có, Aspose.CAD hỗ trợ nhiều định dạng CAD, đảm bảo tính linh hoạt trong việc xử lý nhiều loại tệp khác nhau.

### Câu hỏi 2: Tôi có thể tùy chỉnh cài đặt xuất PDF không?

A2: Chắc chắn rồi. Như được hiển thị trong hướng dẫn, bạn có thể điều chỉnh các tùy chọn như kích thước và bố cục trang cho phù hợp với yêu cầu của mình.

### Câu hỏi 3: Tôi có thể tìm thêm hỗ trợ hoặc hỗ trợ ở đâu?

 A3: Tham quan[Diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để được cộng đồng hỗ trợ và thảo luận.

### Q4: Có bản dùng thử miễn phí không?

 Câu trả lời 4: Có, bạn có thể truy cập bản dùng thử miễn phí[đây](https://releases.aspose.com/).

### Câu hỏi 5: Làm cách nào để có được giấy phép tạm thời?

 A5: Nhận giấy phép tạm thời[đây](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
