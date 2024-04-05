---
title: Thêm văn bản trong DWG bằng Aspose.CAD cho Java
linktitle: Thêm văn bản trong DWG
second_title: API Java Aspose.CAD
description: Nâng cao bản vẽ DWG của bạn một cách dễ dàng với Aspose.CAD cho Java. Thêm văn bản liền mạch với hướng dẫn từng bước của chúng tôi.
type: docs
weight: 10
url: /vi/java/cad-text-and-annotation/add-text-in-dwg/
---
## Giới thiệu

Trong lĩnh vực thiết kế có sự hỗ trợ của máy tính (CAD), Aspose.CAD cho Java nổi bật như một công cụ mạnh mẽ để thao tác và chuyển đổi các bản vẽ DWG. Một trong những tính năng tiện dụng của nó là khả năng thêm văn bản vào tệp DWG một cách liền mạch. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn quy trình thêm văn bản vào bản vẽ DWG của bạn bằng Aspose.CAD cho Java.

## Điều kiện tiên quyết

Trước khi đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

-  Thư viện Aspose.CAD cho Java: Tải xuống và cài đặt thư viện từ[Trang Aspose.CAD cho Java](https://releases.aspose.com/cad/java/).

- Bộ công cụ phát triển Java (JDK): Đảm bảo bạn đã cài đặt JDK mới nhất trên hệ thống của mình.

- Bản vẽ DWG: Chuẩn bị tệp bản vẽ DWG nơi bạn muốn thêm văn bản.

## Nhập không gian tên

Trong mã Java của bạn, hãy nhập các vùng tên cần thiết cho Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Bây giờ, hãy chia đoạn mã được cung cấp thành nhiều bước:

## Bước 1: Thiết lập thư mục tài liệu và đường dẫn tệp DWG

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## Bước 2: Tải hình ảnh DWG

```java
Image image = Image.load(dwgPathToFile);
```

## Bước 3: Tạo đối tượng CadText

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);
cadText.setScaleX(0);
```

## Bước 4: Thêm văn bản vào CadImage

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## Bước 5: Thiết lập tùy chọn PDF

```java
PdfOptions pdfOptions = new PdfOptions();
```

## Bước 6: Cấu hình CadRasterizationOptions

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## Bước 7: Lưu DWG đã sửa đổi dưới dạng PDF

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

Bằng cách làm theo các bước này, bạn sẽ có thể thêm văn bản vào bản vẽ DWG của mình một cách liền mạch bằng Aspose.CAD cho Java.

## Phần kết luận

Aspose.CAD cho Java trao quyền cho các nhà phát triển nâng cao và sửa đổi các bản vẽ DWG theo chương trình. Hướng dẫn này cung cấp hướng dẫn từng bước rõ ràng để thêm văn bản vào tệp DWG của bạn, thể hiện tính đơn giản và sức mạnh của Aspose.CAD.

## Câu hỏi thường gặp

### Câu hỏi 1: Aspose.CAD có tương thích với tất cả các phiên bản của tệp DWG không?

Trả lời 1: Aspose.CAD hỗ trợ nhiều phiên bản khác nhau của tệp DWG, đảm bảo khả năng tương thích với nhiều loại phần mềm CAD.

### Q2: Tôi có thể tùy chỉnh phông chữ và định dạng của văn bản được thêm vào không?

Câu trả lời 2: Có, bạn có thể tùy chỉnh phông chữ, kiểu và các tùy chọn định dạng khác cho văn bản được thêm vào tệp DWG bằng Aspose.CAD.

### Câu hỏi 3: Có bản dùng thử miễn phí dành cho Aspose.CAD cho Java không?

 Câu trả lời 3: Có, bạn có thể khám phá các tính năng của Aspose.CAD bằng cách tải bản dùng thử miễn phí từ[đây](https://releases.aspose.com/).

### Câu hỏi 4: Tôi có thể tìm tài liệu chi tiết về Aspose.CAD cho Java ở đâu?

 A4: Tham khảo tài liệu[đây](https://reference.aspose.com/cad/java/) để biết thông tin chi tiết và ví dụ.

### Câu hỏi 5: Làm cách nào tôi có thể nhận được hỗ trợ hoặc tìm kiếm trợ giúp với Aspose.CAD?

A5: Tham quan[Diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để được hỗ trợ và kết nối với cộng đồng.