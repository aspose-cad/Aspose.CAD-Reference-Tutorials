---
date: 2026-06-19
description: Tìm hiểu cách phân tách đối tượng chèn CAD trong Java bằng Aspose.CAD.
  Thực hiện theo hướng dẫn từng bước này để phá vỡ các đối tượng chèn một cách hiệu
  quả.
keywords:
- decompose cad insert
- Aspose.CAD Java
- CAD block extraction
linktitle: Phân tách Đối tượng Chèn CAD với Java
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Learn how to decompose cad insert object in Java using Aspose.CAD.
    Follow this step‑by‑step guide to break down insert objects efficiently.
  headline: Decompose CAD Insert Object with Aspose.CAD In Java
  type: TechArticle
- description: Learn how to decompose cad insert object in Java using Aspose.CAD.
    Follow this step‑by‑step guide to break down insert objects efficiently.
  name: Decompose CAD Insert Object with Aspose.CAD In Java
  steps:
  - name: Set the Resource Directory Path
    text: Define a stable folder that holds all sample drawings. Keeping files in
      a dedicated **DXFDrawings** directory avoids path‑related errors across development
      machines. *Pro tip:* Use `System.getProperty("user.dir")` to build an absolute
      path that works on both Windows and Linux environments.
  - name: Load CAD Image
    text: '`CadImage` is the main class that represents a CAD drawing in memory. When
      you instantiate it with a file path, Aspose.CAD parses the file and builds an
      entity tree ready for traversal. At this point `cadImage` represents the entire
      drawing, including any insert objects it contains.'
  - name: Iterate Through CAD Entities
    text: '`CadEntity` is the base type for every drawable object. By checking the
      entity type you can isolate INSERT objects, fetch their block definitions, and
      then enumerate the inner geometries. `CadBlockEntity` represents a block definition
      that can be referenced by one or more INSERT objects. It contains'
  - name: Dispose of Resources
    text: Aspose.CAD allocates native resources for large drawings. Calling `close()`
      (or using a try‑with‑resources block) releases those handles and prevents memory
      leaks, especially important when processing many files in a batch job.
  type: HowTo
- questions:
  - answer: Yes, you can. Purchase a commercial license to remove evaluation restrictions
      and receive priority support. You can buy a license on the [purchase page](https://purchase.aspose.com/buy).
    question: Can I use Aspose.CAD for Java in a commercial project?
  - answer: Absolutely. Download the trial from the official release page and start
      experimenting without cost.
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: Temporary licenses are provided for 30‑day evaluation periods via the
      [this link](https://purchase.aspose.com/temporary-license/).
    question: How can I obtain a temporary license for Aspose.CAD for Java?
  - answer: The full API reference is available [here](https://reference.aspose.com/cad/java/).
    question: Where can I find detailed documentation for Aspose.CAD for Java?
  - answer: Yes, the Aspose.CAD distribution includes a “DXFDrawings” folder with
      a variety of sample files for testing.
    question: Are there sample drawings I can use to practice?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Phân tách Đối tượng Chèn CAD với Aspose.CAD trong Java
url: /vi/java/additional-features/decompose-cad-insert-object/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Phân tách Đối tượng Chèn CAD với Aspose.CAD trong Java

## Giới thiệu

Trong hướng dẫn toàn diện này, bạn sẽ học **cách phân tách đối tượng chèn CAD** bằng Aspose.CAD cho Java. Cho dù bạn đang tích hợp xử lý CAD vào công cụ desktop hay dịch vụ phía máy chủ, việc tách một đối tượng chèn thành các thực thể riêng lẻ cho phép bạn thao tác, phân tích hoặc chuyển đổi từng phần một cách độc lập. Chúng tôi sẽ hướng dẫn toàn bộ quy trình — từ thiết lập môi trường đến duyệt các thực thể block — để bạn có thể bắt đầu xử lý các đối tượng chèn CAD ngay lập tức. Aspose.CAD là một phần của họ thư viện Aspose, có sẵn tại [here](https://releases.aspose.com/).

## Câu trả lời nhanh
- **Câu hỏi “phân tách đối tượng chèn cad” có nghĩa là gì?** Nó có nghĩa là trích xuất định nghĩa block (chèn) và các thực thể con của nó từ bản vẽ CAD.  
- **Thư viện nào tôi cần?** Aspose.CAD cho Java (phiên bản mới nhất).  
- **Tôi có cần giấy phép cho việc phát triển không?** Bản dùng thử miễn phí đủ cho việc thử nghiệm; giấy phép thương mại cần thiết cho môi trường sản xuất.  
- **Các định dạng CAD nào được hỗ trợ?** DXF, DWG, DWF, DGN và hơn 30 định dạng khác.  
- **Thời gian thực hiện khoảng bao lâu?** Khoảng 10‑15 phút cho việc trích xuất cơ bản.

## Phân tách cad insert là gì?

**Phân tách cad insert** là quá trình tách một thực thể INSERT thành định nghĩa block nền và truy xuất mọi phần tử hình học mà nó chứa. Điều này cho phép phân tích chi tiết, chuyển đổi có chọn lọc hoặc render tùy chỉnh từng thành phần, và thường bao gồm việc trích xuất hàng chục thực thể đường, cung và văn bản tạo nên block gốc.

## Tại sao nên sử dụng Aspose.CAD cho Java?

Aspose.CAD hỗ trợ **hơn 30** định dạng CAD đầu vào và đầu ra — bao gồm DWG, DXF, DWF, DGN và PDF — trong khi xử lý các bản vẽ hàng trăm trang mà không cần tải toàn bộ tệp vào bộ nhớ. API chạy trên bất kỳ nền tảng tương thích Java nào, không yêu cầu cài đặt CAD gốc, và cung cấp hiệu năng xác định tăng tuyến tính với số lượng thực thể.

## Yêu cầu trước

Trước khi bắt đầu hướng dẫn, hãy đảm bảo bạn đã chuẩn bị các yêu cầu sau:

- **Thư viện Aspose.CAD cho Java** – Tải xuống và cài đặt phiên bản mới nhất từ [here](https://releases.aspose.com/cad/java/).  
- **Bộ công cụ phát triển Java (JDK)** – Khuyến nghị JDK 11 hoặc mới hơn.  
- **Môi trường phát triển tích hợp (IDE)** – Sử dụng Eclipse, IntelliJ IDEA hoặc bất kỳ IDE nào bạn thích cho phát triển Java.

## Nhập không gian tên

Các câu lệnh `import` cung cấp quyền truy cập vào các lớp cốt lõi cần thiết cho việc thao tác CAD.

```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadBlockEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadInsertObject;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadconsts.CadEntityTypeName;
import java.util.ArrayList;
import java.util.List;
```

## Cách phân tách đối tượng chèn CAD bằng Aspose.CAD cho Java?

Tải tệp CAD, xác định mọi thực thể INSERT, lấy block liên quan, và sau đó duyệt qua từng thực thể con. Các bước sau đây cho thấy trình tự chính xác bạn cần thực hiện, bao gồm việc quản lý tài nguyên và các mẹo thực hành tốt.

### Bước 1: Đặt Đường dẫn Thư mục Tài nguyên

Xác định một thư mục ổn định chứa tất cả các bản vẽ mẫu. Giữ các tệp trong thư mục **DXFDrawings** riêng biệt giúp tránh lỗi liên quan đến đường dẫn trên các máy phát triển.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
```

*Mẹo:* Sử dụng `System.getProperty("user.dir")` để tạo đường dẫn tuyệt đối hoạt động trên cả môi trường Windows và Linux.

### Bước 2: Tải Hình ảnh CAD

`CadImage` là lớp chính đại diện cho bản vẽ CAD trong bộ nhớ. Khi bạn khởi tạo nó bằng đường dẫn tệp, Aspose.CAD sẽ phân tích tệp và xây dựng cây thực thể sẵn sàng để duyệt.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage =(CadImage) Image.load(srcFile);
```

Tại thời điểm này, `cadImage` đại diện cho toàn bộ bản vẽ, bao gồm bất kỳ đối tượng chèn nào nó chứa.

### Bước 3: Duyệt qua Các Thực thể CAD

`CadEntity` là kiểu cơ sở cho mọi đối tượng có thể vẽ. Bằng cách kiểm tra loại thực thể, bạn có thể tách riêng các đối tượng INSERT, lấy định nghĩa block của chúng, và sau đó liệt kê các hình học bên trong.

`CadBlockEntity` đại diện cho một định nghĩa block có thể được một hoặc nhiều đối tượng INSERT tham chiếu. Nó chứa tập hợp các thực thể con tạo nên block.

```java
for (int i=0; i<cadImage.getEntities().length;i++)
{
    if (cadImage.getEntities()[i].getTypeName() == CadEntityTypeName.INSERT)
    {
        // Retrieve the block entity
        CadBlockEntity block =
            (CadBlockEntity)cadImage.getBlockEntities().get_Item(((CadInsertObject)cadImage.getEntities()[i]).getName());
            
        // Process entities within the block
        for (CadBaseEntity blockChild : block.getEntities())
        {
            // Process each entity within the block
        }
    }
}
```

**Điều gì đang xảy ra ở đây?**  
- Chúng tôi quét mọi thực thể trong bản vẽ.  
- Khi gặp một thực thể loại **INSERT**, chúng tôi lấy `CadBlockEntity` tương ứng.  
- Vòng lặp bên trong cho phép bạn truy cập mỗi thực thể con (đường, cung, vòng tròn, v.v.) trong block đó, thực tế **phân tách đối tượng chèn**.

### Bước 4: Giải phóng Tài nguyên

Aspose.CAD cấp phát tài nguyên gốc cho các bản vẽ lớn. Gọi `close()` (hoặc sử dụng khối try‑with‑resources) sẽ giải phóng các handle và ngăn ngừa rò rỉ bộ nhớ, đặc biệt quan trọng khi xử lý nhiều tệp trong một công việc batch.

```java
finally
{
    cadImage.dispose();
}
```

## Những Cạm Bẫy Thường Gặp & Mẹo

- **Tham chiếu block null:** Nếu một INSERT tham chiếu tới một block bị thiếu, `get_Item` sẽ trả về `null`. Thêm kiểm tra null trước khi xử lý.  
- **Hiệu năng:** Đối với các bản vẽ rất lớn, cân nhắc lọc thực thể theo lớp hoặc loại trước khi duyệt.  
- **Hệ tọa độ:** Các đối tượng chèn có thể có ma trận biến đổi; sử dụng `CadInsertObject.getTransform()` nếu bạn cần tọa độ tuyệt đối.  
- **Sử dụng bộ nhớ:** Aspose.CAD xử lý tệp theo kiểu streaming, nhưng việc cấp phát một `CadImage` cho DWG 500 trang vẫn tiêu tốn khoảng ~150 MB RAM. Hãy giải phóng kịp thời.

## Kết luận

Trong hướng dẫn này, chúng tôi đã khám phá quy trình **phân tách đối tượng chèn cad** bằng Aspose.CAD cho Java. Với API mạnh mẽ, Aspose.CAD giúp việc trích xuất và thao tác các thực thể bên trong của đối tượng chèn trở nên đơn giản, mở ra cơ hội cho phân tích tùy chỉnh, quy trình chuyển đổi hoặc trực quan hoá. Hãy thử nghiệm với mã mẫu, điều chỉnh các vòng lặp theo logic kinh doanh của bạn, và bạn sẽ có nền tảng vững chắc cho bất kỳ ứng dụng Java dựa trên CAD nào.

Nếu bạn gặp bất kỳ khó khăn nào hoặc có câu hỏi, hãy truy cập [diễn đàn hỗ trợ](https://forum.aspose.com/c/cad/19) của chúng tôi.

## Câu hỏi thường gặp

**H: Tôi có thể sử dụng Aspose.CAD cho Java trong dự án thương mại không?**  
A: Có, bạn có thể. Mua giấy phép thương mại để loại bỏ các hạn chế đánh giá và nhận hỗ trợ ưu tiên. Bạn có thể mua giấy phép tại [purchase page](https://purchase.aspose.com/buy).

**H: Có bản dùng thử miễn phí cho Aspose.CAD cho Java không?**  
A: Chắc chắn. Tải bản dùng thử từ trang phát hành chính thức và bắt đầu thử nghiệm mà không tốn phí.

**H: Làm sao tôi có thể nhận giấy phép tạm thời cho Aspose.CAD cho Java?**  
A: Giấy phép tạm thời được cung cấp trong thời gian đánh giá 30 ngày qua [this link](https://purchase.aspose.com/temporary-license/).

**H: Tôi có thể tìm tài liệu chi tiết cho Aspose.CAD cho Java ở đâu?**  
A: Tham khảo đầy đủ API tại [here](https://reference.aspose.com/cad/java/).

**H: Có các bản vẽ mẫu để tôi thực hành không?**  
A: Có, bộ phân phối Aspose.CAD bao gồm thư mục “DXFDrawings” với nhiều tệp mẫu để kiểm tra.

---

**Cập nhật lần cuối:** 2026-06-19  
**Kiểm tra với:** Aspose.CAD cho Java 24.11  
**Tác giả:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Hướng dẫn liên quan

- [Cách Trích xuất Thuộc tính - Giá trị Thuộc tính Block từ Tham chiếu Ngoài bằng Aspose.CAD trong Java](/cad/java/advanced-cad-features/extract-block-attribute-value/)
- [Cách Đọc Tệp DWT với Aspose.CAD cho Java](/cad/java/advanced-cad-features/reading-dwt-files/)
- [Đặt Kích thước Canvas – Tính năng CAD nâng cao với Aspose.CAD cho Java](/cad/java/advanced-cad-features/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}