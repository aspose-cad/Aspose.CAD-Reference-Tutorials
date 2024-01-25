---
title: Hỗ trợ Thực thể MLeader cho Định dạng DWG với Aspose.CAD cho Java
linktitle: Hỗ trợ Thực thể MLeader cho Định dạng DWG bằng Java
second_title: API Java Aspose.CAD
description: Khai phá sức mạnh của Aspose.CAD cho Java bằng hướng dẫn từng bước của chúng tôi về cách hỗ trợ các thực thể MLeader ở định dạng DWG.
type: docs
weight: 12
url: /vi/java/cad-text-and-formatting/support-mleader-entity/
---
## Giới thiệu

Trong lĩnh vực thiết kế có sự hỗ trợ của máy tính (CAD) với Java, việc hiểu và triển khai hỗ trợ cho các thực thể MLeader ở định dạng DWG là một kỹ năng có giá trị. Aspose.CAD cho Java cung cấp một giải pháp mạnh mẽ cho những tác vụ như vậy, cung cấp một bộ công cụ và chức năng mạnh mẽ. Hướng dẫn này sẽ hướng dẫn bạn quy trình hỗ trợ các thực thể MLeader trong tệp DWG bằng Java với Aspose.CAD.

## Điều kiện tiên quyết

Trước khi chúng ta đi sâu vào hướng dẫn, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

1. Môi trường phát triển Java: Đảm bảo bạn đã thiết lập môi trường phát triển Java trên hệ thống của mình.

2.  Thư viện Aspose.CAD: Tải xuống và cài đặt thư viện Aspose.CAD cho Java từ[Liên kết tải xuống](https://releases.aspose.com/cad/java/).

## Nhập không gian tên

Trong dự án Java của bạn, hãy nhập các vùng tên cần thiết để tận dụng hiệu quả các khả năng của Aspose.CAD. Bao gồm các dòng sau trong mã của bạn:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeader;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderContextData;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderLine;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderNode;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;

```

Bây giờ, hãy chia mã thành hướng dẫn từng bước để hỗ trợ các thực thể MLeader cho định dạng DWG bằng Java với Aspose.CAD.

## 1. Load file DWG và truy cập CadImage

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

## 2. Xác thực các thực thể MLeader

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### 3. Xác minh Kiểu và Thuộc tính MLeader

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

## 4. Truy cập dữ liệu ngữ cảnh MLeader

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

## 5. Xác thực thuộc tính ngữ cảnh

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(), "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

## 6. Truy cập Nút MLeader và Dòng lãnh đạo

```java
CadMLeaderNode mleaderNode = context.getLeaderNode();
Assert.areEqual(mleaderNode.getLastLeaderLinePoint().getX(), 473, 1);

CadMLeaderLine leaderLine = mleaderNode.getLeaderLine();
Assert.areEqual(leaderLine.getBreakEndPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getBreakPointIndex().getValue()), Integer.toString(0));
Assert.areEqual(leaderLine.getBreakStartPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getLeaderLineIndex().getValue()), Integer.toString(0));
Assert.areEqual(Integer.toString(leaderLine.getLeaderPoints().size()), Integer.toString(4));
```

## 7. Xác thực các thuộc tính MLeader bổ sung

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

## 8. Xác thực thuộc tính văn bản

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

## 9. Thuộc tính MLeader bổ sung

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## Phần kết luận

Chúc mừng! Bạn đã điều hướng thành công qua hướng dẫn toàn diện về cách hỗ trợ các thực thể MLeader cho định dạng DWG bằng Java và Aspose.CAD. Khả năng này mở ra cánh cửa cho các thao tác CAD nâng cao và nâng cao bộ công cụ phát triển Java của bạn.

## Câu hỏi thường gặp

### Câu hỏi 1: Tôi có thể sử dụng Aspose.CAD cho Java với các định dạng CAD khác không?

Câu trả lời 1: Có, Aspose.CAD hỗ trợ nhiều định dạng CAD khác nhau ngoài DWG, mang lại tính linh hoạt trong các dự án của bạn.

### Câu hỏi 2: Tôi có thể tìm tài liệu chi tiết về Aspose.CAD cho Java ở đâu?

 A2: Tham khảo[tài liệu](https://reference.aspose.com/cad/java/) để có những hiểu biết sâu sắc về khả năng của Aspose.CAD.

### Câu 3: Có bản dùng thử miễn phí không?

 Câu trả lời 3: Có, hãy khám phá trực tiếp các chức năng với[dùng thử miễn phí](https://releases.aspose.com/).

### Câu hỏi 4: Làm cách nào tôi có thể nhận được giấy phép tạm thời cho Aspose.CAD?

A4: Xin giấy phép tạm thời thông qua[liên kết này](https://purchase.aspose.com/temporary-license/).

### Câu hỏi 5: Tôi có thể tìm kiếm sự hỗ trợ và giúp đỡ của cộng đồng ở đâu?

A5: Tham quan[Diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để kết nối với cộng đồng và nhận trợ giúp.