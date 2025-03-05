---
title: Xuất bố cục CAD sang PDF bằng Aspose.CAD cho Java
linktitle: Xuất bố cục CAD sang PDF
second_title: API Java Aspose.CAD
description: Khám phá Aspose.CAD cho Java để dễ dàng xuất bố cục CAD sang PDF. Hiệu quả, đáng tin cậy và thân thiện với nhà phát triển.
type: docs
weight: 11
url: /vi/java/cad-export-options/export-cad-layouts-to-pdf/
---
## Giới thiệu

Trong lĩnh vực thiết kế có sự hỗ trợ của máy tính (CAD) ngày càng phát triển, Aspose.CAD cho Java nổi bật như một công cụ mạnh mẽ để thao tác và chuyển đổi các tệp CAD. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn quy trình xuất bố cục CAD sang PDF bằng Aspose.CAD cho Java. Cho dù bạn là nhà phát triển dày dạn kinh nghiệm hay chỉ mới bước chân vào thế giới CAD, hướng dẫn từng bước này sẽ giúp bạn khai thác toàn bộ tiềm năng của thư viện Java linh hoạt này.

## Điều kiện tiên quyết

Trước khi chúng ta đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

-  Aspose.CAD cho Java: Đảm bảo rằng bạn đã cài đặt thư viện. Bạn có thể tải xuống từ trang web Aspose[đây](https://releases.aspose.com/cad/java/).

- Môi trường phát triển Java: Đảm bảo bạn đã thiết lập môi trường phát triển Java trên máy của mình.

Bây giờ bạn đã thiết lập xong mọi thứ, hãy bắt đầu với phần hướng dẫn.

## Nhập không gian tên

Trong mã Java của bạn, hãy bắt đầu bằng cách nhập các vùng tên cần thiết. Những lần nhập này cung cấp quyền truy cập vào các lớp và phương thức cần thiết để làm việc với Aspose.CAD cho Java.

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//nhập com.aspose.cad.imageoptions.TypeOfEntities;
```

## Bước 1: Tải tệp CAD

 Bắt đầu bằng cách tải tệp CAD vào ứng dụng Java của bạn bằng cách sử dụng`Image.load` phương pháp. Thay thế`"conic_pyramid.dxf"` với đường dẫn đến tệp CAD của bạn.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

## Bước 2: Đặt tùy chọn Rasterization

 Tạo một thể hiện của`CadRasterizationOptions` để xác định cách thức phân loại các thực thể CAD. Điều chỉnh các tham số như chiều rộng trang, chiều cao trang và tỷ lệ bố cục theo yêu cầu của bạn.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(false);
rasterizationOptions.setContentAsBitmap(true);
rasterizationOptions.setLayouts(new String[]{"Model"});
```

## Bước 3: Đặt tùy chọn PDF

 Tạo một thể hiện của`PdfOptions` và liên kết nó với các tùy chọn rasterization. Ngoài ra, hãy đặt các tùy chọn đồ họa để xuất PDF, chẳng hạn như chế độ làm mịn, gợi ý hiển thị văn bản và chế độ nội suy.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.getGraphicsOptions().setSmoothingMode(SmoothingMode.HighQuality);
rasterizationOptions.getGraphicsOptions().setTextRenderingHint(TextRenderingHint.AntiAliasGridFit);
rasterizationOptions.getGraphicsOptions().setInterpolationMode(InterpolationMode.HighQualityBicubic);
```

## Bước 4: Xuất sang PDF

 Cuối cùng, xuất bố cục CAD sang tệp PDF bằng cách sử dụng`save` phương pháp của`cadImage` sự vật.

```java
cadImage.save(dataDir + "CADLayoutsToPDF_out_.pdf", pdfOptions);
```

Chúc mừng! Bạn đã xuất thành công bố cục CAD sang PDF bằng Aspose.CAD cho Java. Vui lòng khám phá các tính năng và chức năng bổ sung do Aspose.CAD cung cấp để nâng cao trải nghiệm thao tác tệp CAD của bạn.

## Phần kết luận

Trong hướng dẫn này, chúng tôi đã hướng dẫn quy trình xuất bố cục CAD sang PDF bằng Aspose.CAD cho Java. Với các tính năng mạnh mẽ và API dễ sử dụng, Aspose.CAD trao quyền cho các nhà phát triển làm việc hiệu quả với các tệp CAD trong ứng dụng Java của họ.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.CAD cho Java với các định dạng tệp CAD khác không?

 Câu trả lời 1: Có, Aspose.CAD hỗ trợ nhiều định dạng CAD khác nhau, bao gồm DWG, DXF, DWF, v.v. Kiểm tra tài liệu[đây](https://reference.aspose.com/cad/java/) để có danh sách đầy đủ.

### Câu hỏi 2: Có bản dùng thử miễn phí cho Aspose.CAD cho Java không?

 Câu trả lời 2: Có, bạn có thể khám phá các tính năng của Aspose.CAD bằng bản dùng thử miễn phí[đây](https://releases.aspose.com/).

### Câu hỏi 3: Làm cách nào tôi có thể nhận được hỗ trợ cho Aspose.CAD cho Java?

 A3: Truy cập diễn đàn Aspose.CAD[đây](https://forum.aspose.com/c/cad/19) để hỗ trợ cộng đồng. Để được hỗ trợ cao cấp, hãy cân nhắc việc mua giấy phép[đây](https://purchase.aspose.com/buy).

### Câu hỏi 4: Sự khác biệt giữa chia tỷ lệ bố cục tự động và thủ công là gì?

Câu trả lời 4: Tự động chia tỷ lệ bố cục sẽ điều chỉnh kích thước bố cục dựa trên kích thước trang được chỉ định, trong khi chia tỷ lệ thủ công cho phép bạn đặt các giá trị chia tỷ lệ tùy chỉnh.

### Câu hỏi 5: Tôi có thể tùy chỉnh hình thức của tệp PDF đã xuất không?

Câu trả lời 5: Có, bạn có thể tùy chỉnh các tùy chọn đồ họa trong mã để kiểm soát chất lượng và hình thức của tệp PDF đã xuất.