---
date: 2026-01-10
description: Tìm hiểu cách đọc tệp DWG và tạo các thực thể multileader DWG bằng Aspose.CAD
  cho Java trong hướng dẫn từng bước này.
linktitle: Support MLeader Entity for DWG Format with Java
second_title: Aspose.CAD Java API
title: Cách Đọc DWG và Hỗ trợ MLeader với Aspose.CAD cho Java
url: /vi/java/cad-text-and-formatting/support-mleader-entity/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách Đọc DWG và Hỗ Trợ MLeader với Aspose.CAD cho Java

## Giới thiệu

Nếu bạn cần **đọc DWG** và làm việc với các thực thể **multileader DWG** trong một ứng dụng Java, bạn đã đến đúng nơi. Aspose.CAD cho Java cung cấp cho bạn một cách tiếp cận lập trình sạch sẽ để mở bản vẽ DWG, kiểm tra các đối tượng MLeader và xác thực các thuộc tính của chúng — tất cả mà không cần một workstation CAD đầy đủ. Trong hướng dẫn này, chúng tôi sẽ đi qua từng bước, từ việc tải tệp DWG đến việc xác nhận dữ liệu multileader khớp với kiểu mong muốn.

## Câu trả lời nhanh
- **“Cách đọc dwg” bao gồm những gì?** Tải DWG bằng `Image.load()` và ép kiểu thành `CadImage`.
- **Tôi có thể tạo các thực thể multileader dwg không?** Có – bạn có thể thêm, chỉnh sửa và xác thực các đối tượng MLeader bằng API CadMLeader.
- **Phiên bản thư viện nào được yêu cầu?** Bất kỳ bản phát hành Aspose.CAD cho Java gần đây nào (API được trình bày hoạt động với các bản build 2024+).
- **Tôi có cần giấy phép cho việc phát triển không?** Giấy phép tạm thời hoạt động cho việc thử nghiệm; giấy phép đầy đủ cần thiết cho môi trường sản xuất.
- **Mã có đa nền tảng không?** Chắc chắn – Java chạy trên Windows, Linux và macOS.

## “Cách đọc dwg” là gì với Aspose.CAD?

Đọc một tệp DWG có nghĩa là chuyển đổi bản vẽ nhị phân thành một đối tượng `CadImage` trong bộ nhớ. Khi có đối tượng này, bạn có thể liệt kê các thực thể của nó (đường, vòng tròn, văn bản, **MLeader**, v.v.) và kiểm tra các thuộc tính của chúng.

## Tại sao hỗ trợ các thực thể MLeader?

Các đối tượng MLeader (multileader) kết hợp các đường leader với văn bản hoặc block đính kèm, làm cho chúng trở nên thiết yếu cho các chú thích trong bản vẽ kỹ thuật. Hỗ trợ chúng cho phép bạn:

- Xác thực rằng các chú thích tuân thủ tiêu chuẩn công ty.
- Trích xuất văn bản để xử lý tiếp theo (ví dụ: tạo BOM).
- Thay đổi kiểu leader hoặc thay thế nội dung block một cách lập trình.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn rằng bạn đã có:

1. **Môi trường phát triển Java** – JDK 11+ và IDE yêu thích của bạn (IntelliJ, Eclipse, VS Code).  
2. **Aspose.CAD cho Java** – Tải JAR mới nhất từ [liên kết tải xuống](https://releases.aspose.com/cad/java/).  

## Nhập các namespace

Thêm các import sau vào lớp Java của bạn để làm việc với các thực thể DWG và các tùy chọn rasterization:

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

## Cách Đọc Tệp DWG Sử Dụng Aspose.CAD cho Java

### Bước 1: Tải tệp DWG và lấy một `CadImage`

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

### Bước 2: Xác thực rằng bản vẽ chứa các thực thể MLeader

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### Bước 3: Xác minh kiểu MLeader và các thuộc tính cơ bản

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

### Bước 4: Truy cập dữ liệu ngữ cảnh MLeader (trái tim của multileader)

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

### Bước 5: Xác thực các thuộc tính mức ngữ cảnh

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(),
    "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

### Bước 6: Làm việc với nút MLeader và đường leader của nó

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

### Bước 7: Xác thực các thuộc tính bổ sung của nút MLeader

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

### Bước 8: Kiểm tra các thuộc tính liên quan đến văn bản

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

### Bước 9: Xem xét các thuộc tính MLeader khác để hoàn thiện

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Nguyên nhân | Cách khắc phục |
|-------|-------------|----------------|
| `ClassCastException` khi ép kiểu thực thể | Chỉ mục đã chọn không phải là đối tượng MLeader. | Kiểm tra `cadImage.getEntities()[i] instanceof CadMLeader` trước khi ép kiểu. |
| Giá trị `null` cho các điểm đường leader | Bản vẽ sử dụng kiểu leader tùy chỉnh không được hỗ trợ đầy đủ. | Sử dụng phiên bản Aspose.CAD mới nhất hoặc quay lại kiểu mặc định để thử nghiệm. |
| Lỗi khẳng định trên các giá trị số | Sự chênh lệch làm tròn nhẹ giữa các phiên bản CAD. | Điều chỉnh độ dung sai trong `Assert.areEqual(..., delta)` như trong các ví dụ. |

## Câu hỏi thường gặp

**Q: Tôi có thể sử dụng Aspose.CAD cho Java với các định dạng CAD khác không?**  
A: Có, Aspose.CAD hỗ trợ DXF, DWF, DGN và một số định dạng raster khác ngoài DWG.

**Q: Tôi có thể tìm tài liệu chi tiết cho Aspose.CAD cho Java ở đâu?**  
A: Tham khảo [documentation](https://reference.aspose.com/cad/java/) chính thức để biết chi tiết API và các mẫu mã.

**Q: Có bản dùng thử miễn phí không?**  
A: Chắc chắn – bạn có thể tải bản dùng thử từ trang [free trial](https://releases.aspose.com/).

**Q: Làm thế nào để tôi có được giấy phép tạm thời để thử nghiệm?**  
A: Nhận giấy phép tạm thời qua [temporary license link](https://purchase.aspose.com/temporary-license/).

**Q: Tôi có thể hỏi cộng đồng để được giúp đỡ ở đâu?**  
A: Diễn đàn [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) là nơi tốt nhất để chia sẻ câu hỏi và giải pháp.

## Kết luận

Bạn đã có một hướng dẫn toàn diện, từ đầu đến cuối cho **cách đọc DWG** và **tạo các thực thể multileader DWG** bằng Aspose.CAD cho Java. Bằng cách thực hiện các bước trên, bạn có thể xác thực kiểu MLeader, trích xuất dữ liệu chú thích và tích hợp xử lý DWG vào bất kỳ quy trình làm việc nào dựa trên Java.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Cập nhật lần cuối:** 2026-01-10  
**Kiểm tra với:** Aspose.CAD 24.11 cho Java  
**Tác giả:** Aspose