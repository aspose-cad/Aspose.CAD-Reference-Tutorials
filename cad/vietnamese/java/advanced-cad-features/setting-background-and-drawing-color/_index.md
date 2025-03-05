---
title: Đặt nền và màu vẽ bằng Aspose.CAD cho Java
linktitle: Đặt nền và màu vẽ
second_title: API Java Aspose.CAD
description: Dễ dàng chuyển đổi tệp CAD sang PDF và TIFF bằng Aspose.CAD cho Java. Đặt màu nền và màu vẽ tùy chỉnh để có kết quả trực quan ấn tượng.
type: docs
weight: 15
url: /vi/java/advanced-cad-features/setting-background-and-drawing-color/
---
## Giới thiệu

Trong thế giới năng động của Thiết kế có sự hỗ trợ của máy tính (CAD), việc chuyển đổi tệp hiệu quả là rất quan trọng để cộng tác và liên lạc liền mạch. Aspose.CAD cho Java nổi lên như một công cụ mạnh mẽ, cung cấp khả năng mạnh mẽ để chuyển đổi tệp CAD sang định dạng PDF và TIFF. Trong hướng dẫn này, chúng tôi sẽ đi sâu vào quy trình thiết lập nền và vẽ màu bằng Aspose.CAD cho Java, cung cấp cho bạn hướng dẫn từng bước để có kết quả tối ưu.

## Điều kiện tiên quyết

Trước khi chúng ta bắt đầu cuộc hành trình này, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

-  Thư viện Aspose.CAD cho Java: Đảm bảo bạn đã cài đặt thư viện Aspose.CAD cho Java. Bạn có thể tải nó xuống[đây](https://releases.aspose.com/cad/java/).

-  Thư mục Tài liệu: Có một thư mục dành riêng cho các tệp CAD của bạn. Thay thế`"Your Document Directory" + "CADConversion/"` với đường dẫn đến thư mục của bạn.

Bây giờ, hãy đi sâu vào quá trình.

## Nhập không gian tên

Đảm bảo bạn nhập các không gian tên cần thiết để tận dụng các chức năng của Aspose.CAD cho Java. Trong ví dụ của chúng tôi, chúng tôi sử dụng như sau:

```java
import java.awt.Color;
import java.awt.Image;

import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Bước 1: Tải tệp CAD

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image objImage = Image.load(srcFile);
```

## Bước 2: Đặt nền và màu vẽ

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setBackgroundColor(com.aspose.cad.Color.getBeige());
rasterizationOptions.setDrawType(CadDrawTypeMode.UseDrawColor);
rasterizationOptions.setBackgroundColor(com.aspose.cad.Color.getBlue());
```

## Bước 3: Tạo PDF và lưu

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

## Bước 4: Tạo TIFF và lưu

```java
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Hãy thực hiện chăm chỉ các bước sau để đạt được kết quả tối ưu khi chuyển đổi CAD sang PDF và TIFF bằng Aspose.CAD cho Java.

## Phần kết luận

Aspose.CAD cho Java trao quyền cho các nhà phát triển một bộ công cụ linh hoạt để thao tác với tệp CAD. Bằng cách nắm vững sự phức tạp của việc thiết lập nền và màu vẽ, bạn nâng cao khả năng tạo ra các chuyển đổi chính xác và hấp dẫn về mặt hình ảnh.

## Câu hỏi thường gặp

### Câu hỏi 1: Aspose.CAD cho Java có phù hợp để chuyển đổi hàng loạt không?

A1: Chắc chắn rồi! Aspose.CAD cho Java vượt trội trong việc chuyển đổi hàng loạt, mang lại hiệu quả và độ chính xác.

### Câu hỏi 2: Tôi có thể tùy chỉnh màu nền trong các tệp được tạo không?

Câu trả lời 2: Có, hướng dẫn này trình bày cách đặt màu nền tùy chỉnh cho cả đầu ra PDF và TIFF.

### Câu hỏi 3: Tôi có thể tìm tài liệu toàn diện về Aspose.CAD cho Java ở đâu?

 A3: Hãy tham khảo[tài liệu](https://reference.aspose.com/cad/java/) để biết những hiểu biết sâu sắc và ví dụ.

### Q4: Có bản dùng thử miễn phí không?

 Câu trả lời 4: Có, hãy khám phá các tính năng với[dùng thử miễn phí](https://releases.aspose.com/).

### Câu hỏi 5: Làm cách nào tôi có thể nhận được hỗ trợ cho Aspose.CAD cho Java?

A5: Tham quan[Diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để tìm kiếm sự hỗ trợ và tham gia với cộng đồng.
