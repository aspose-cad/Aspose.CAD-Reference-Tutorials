---
title: Thêm hình mờ vào bản vẽ CAD - Hướng dẫn Aspose.CAD cho Java
linktitle: Thêm hình mờ
second_title: API Java Aspose.CAD
description: Nâng cao bản vẽ CAD của bạn bằng hình mờ được cá nhân hóa bằng Aspose.CAD cho Java. Hãy làm theo hướng dẫn từng bước của chúng tôi để tích hợp liền mạch.
weight: 12
url: /vi/java/other-cad-operations/add-watermark/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Thêm hình mờ vào bản vẽ CAD - Hướng dẫn Aspose.CAD cho Java

## Giới thiệu

Chào mừng bạn đến với hướng dẫn toàn diện về cách thêm hình mờ vào bản vẽ CAD bằng Aspose.CAD cho Java. Trong hướng dẫn này, bạn sẽ tìm hiểu cách tích hợp hình mờ một cách hiệu quả, cải thiện tài liệu CAD của bạn bằng các thông điệp hoặc nhãn hiệu được cá nhân hóa. Aspose.CAD cho Java cung cấp một bộ tính năng mạnh mẽ, giúp quá trình thêm hình mờ trở nên đơn giản.

## Điều kiện tiên quyết

Trước khi chúng ta đi sâu vào hướng dẫn, hãy đảm bảo bạn có các điều kiện tiên quyết sau:

-  Aspose.CAD cho Java: Đảm bảo bạn đã cài đặt thư viện Aspose.CAD trong môi trường Java của mình. Bạn có thể tải nó xuống[đây](https://releases.aspose.com/cad/java/).
- Bộ công cụ phát triển Java (JDK): Đảm bảo rằng bạn đã cài đặt phiên bản JDK mới nhất trên hệ thống của mình.

## Gói nhập khẩu

Trong dự án Java của bạn, hãy nhập các gói Aspose.CAD cần thiết để bắt đầu:

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Bước 1: Thêm MTEXT mới

```java
//thêm MTEXT mới
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

## Bước 2: Thêm thực thể đơn giản như văn bản

Bạn cũng có thể thêm một thực thể đơn giản hơn như văn bản:

```java
// hoặc thêm thực thể đơn giản hơn như Văn bản
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

## Bước 3: Xuất sang PDF

Xuất bản vẽ CAD có hình mờ được thêm vào tệp PDF:

```java
// xuất sang pdf
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);

```

## Phần kết luận

Chúc mừng! Bạn đã thêm thành công hình mờ vào bản vẽ CAD của mình bằng Aspose.CAD cho Java. Quy trình đơn giản nhưng mạnh mẽ này cho phép bạn cá nhân hóa thiết kế của mình hoặc bảo vệ chúng bằng thương hiệu.

## Câu hỏi thường gặp

### Câu hỏi 1: Aspose.CAD có tương thích với tất cả các định dạng tệp CAD không?

Trả lời 1: Aspose.CAD hỗ trợ nhiều định dạng CAD khác nhau, bao gồm DWG, DXF, DWT và DWF.

### Câu hỏi 2: Tôi có thể tùy chỉnh hình thức của văn bản hình mờ không?

Câu trả lời 2: Có, bạn có toàn quyền kiểm soát hình thức của hình mờ, bao gồm kích thước văn bản, màu sắc và vị trí.

### Câu hỏi 3: Có phiên bản dùng thử cho Aspose.CAD cho Java không?

 A3: Có, bạn có thể tải xuống phiên bản dùng thử[đây](https://releases.aspose.com/).

### Câu hỏi 4: Làm cách nào tôi có thể nhận được hỗ trợ cho Aspose.CAD?

 A4: Tham quan[Diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để hỗ trợ cộng đồng.

### Câu hỏi 5: Tôi có thể tìm tài liệu đầy đủ về Aspose.CAD cho Java ở đâu?

 A5: Hãy tham khảo[tài liệu](https://reference.aspose.com/cad/java/) để biết thông tin chi tiết.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
