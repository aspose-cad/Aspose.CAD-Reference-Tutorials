---
title: Xuất DGN nhúng sang PDF bằng Aspose.CAD cho Java
linktitle: Xuất DGN nhúng
second_title: API Java Aspose.CAD
description: Khám phá hướng dẫn từng bước về cách xuất tệp DGN được nhúng sang PDF bằng Aspose.CAD cho Java. Nâng cao các ứng dụng Java của bạn bằng thao tác liền mạch với tệp CAD.
type: docs
weight: 11
url: /vi/java/dgn-export-options/export-embedded-dgn/
---
## Giới thiệu

Chào mừng bạn đến với hướng dẫn toàn diện này về cách xuất tệp DGN nhúng bằng Aspose.CAD cho Java. Aspose.CAD là một thư viện mạnh mẽ cho phép các nhà phát triển Java làm việc liền mạch với các tệp CAD. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn quy trình xuất tệp DGN được nhúng sang PDF bằng hướng dẫn từng bước. Cho dù bạn là nhà phát triển dày dạn kinh nghiệm hay mới bắt đầu, hướng dẫn này sẽ giúp bạn khai thác các khả năng của Aspose.CAD để nâng cao các ứng dụng Java của bạn.

## Điều kiện tiên quyết

Trước khi chúng ta đi sâu vào hướng dẫn, hãy đảm bảo bạn có các điều kiện tiên quyết sau:
- Môi trường phát triển Java: Đảm bảo rằng bạn đã thiết lập môi trường phát triển Java trên máy của mình.
-  Aspose.CAD cho Java: Tải xuống và cài đặt thư viện Aspose.CAD cho Java từ[đây](https://releases.aspose.com/cad/java/).

## Gói nhập khẩu

Để bắt đầu, bạn cần nhập các gói cần thiết vào dự án Java của mình. Thêm các câu lệnh nhập sau vào mã của bạn:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Bây giờ, hãy chia mã ví dụ thành nhiều bước:

## Bước 1: Thiết lập đường dẫn đầu vào và đầu ra

Xác định đường dẫn thư mục nơi chứa tài liệu của bạn và chỉ định tên tệp DWG đầu vào.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

## Bước 2: Tải tệp DWG

 Tải tệp DWG vào một`Image` đối tượng sử dụng Aspose.CAD.

```java
Image objImage = Image.load(fileName);
```

## Bước 3: Định cấu hình tùy chọn Rasterization

Định cấu hình các tùy chọn tạo điểm ảnh, chẳng hạn như bố cục sẽ được đưa vào khi xuất.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

## Bước 4: Định cấu hình tùy chọn PDF

Thiết lập các tùy chọn PDF, bao gồm các tùy chọn rasterization vector.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Bước 5: Lưu tệp PDF

Lưu tệp PDF với các tùy chọn đã định cấu hình.
```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Phần kết luận

Chúc mừng! Bạn đã xuất thành công tệp DGN được nhúng sang PDF bằng Aspose.CAD cho Java. Hướng dẫn này bao gồm các bước cần thiết để tích hợp Aspose.CAD vào ứng dụng Java của bạn để thao tác tệp CAD hiệu quả.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.CAD cho Java trong một dự án thương mại không?

 Câu trả lời 1: Có, Aspose.CAD cho Java là một thư viện thương mại. Bạn có thể lấy giấy phép từ[đây](https://purchase.aspose.com/buy).

### Câu hỏi 2: Có bản dùng thử miễn phí không?

 Câu trả lời 2: Có, bạn có thể truy cập bản dùng thử miễn phí Aspose.CAD cho Java[đây](https://releases.aspose.com/).

### Câu hỏi 3: Làm cách nào tôi có thể nhận được hỗ trợ cho Aspose.CAD cho Java?

Câu trả lời 3: Bạn có thể tìm kiếm sự hỗ trợ từ cộng đồng Aspose.CAD trên[diễn đàn](https://forum.aspose.com/c/cad/19).

### Câu hỏi 4: Nếu tôi cần giấy phép tạm thời thì sao?

 A4: Bạn có thể xin giấy phép tạm thời[đây](https://purchase.aspose.com/temporary-license/).

### Câu 5: Tôi có thể tìm tài liệu ở đâu?

 A5: Tài liệu có sẵn[đây](https://reference.aspose.com/cad/java/).