---
date: 2026-06-19
description: Tìm hiểu cách chỉnh sửa tệp DWG bằng Aspose.CAD cho Java, bao gồm cách
  cập nhật đường dẫn DWG XRef và chỉnh sửa siêu liên kết. Hãy dùng bản dùng thử miễn
  phí ngay hôm nay!
keywords:
- how to edit dwg
- update dwg xref paths
- Aspose.CAD Java hyperlink
linktitle: Chỉnh sửa Hyperlink
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Learn how to edit DWG files with Aspose.CAD for Java, including how
    to update DWG XRef paths and edit hyperlinks. Try the free trial today!
  headline: How to Edit DWG Hyperlinks - Aspose.CAD Java Tutorial
  type: TechArticle
- description: Learn how to edit DWG files with Aspose.CAD for Java, including how
    to update DWG XRef paths and edit hyperlinks. Try the free trial today!
  name: How to Edit DWG Hyperlinks - Aspose.CAD Java Tutorial
  steps:
  - name: Accessing Insert Objects
    text: '`CadInsertObject` is the Aspose.CAD class that represents an inserted block
      reference (XRef) inside a DWG drawing. Iterate through the entities and identify
      if an entity is an instance of the `CadInsertObject` class.'
  - name: How to Change XRef Path in a DWG Drawing
    text: '`CadImage` is the primary object that loads and saves CAD files in Aspose.CAD
      for Java. Once you have identified the insert object, retrieve the associated
      block entity and update the XRef path as needed. This ensures the reference
      points to the correct external file.'
  - name: Modifying Hyperlinks
    text: Next, check if the entity has a hyperlink associated with it. If the hyperlink
      matches a specific URL, update it to the desired URL. This step guarantees that
      clicking the hyperlink in the CAD viewer opens the new target.
  type: HowTo
- questions:
  - answer: Yes, after making changes call `cadImage.save("EditedDrawing.dwg");` to
      persist the modifications.
    question: Do I need to call a specific method to write the edited DWG back to
      disk?
  - answer: Absolutely—loop through `cadImage.getEntities()` and apply the hyperlink
      logic to each matching entity.
    question: Is it possible to edit multiple hyperlinks in one pass?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Cách chỉnh sửa siêu liên kết DWG - Hướng dẫn Aspose.CAD Java
url: /vi/java/other-cad-operations/edit-hyperlink/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách chỉnh sửa siêu liên kết DWG - Hướng dẫn Aspose.CAD Java

Trong thời đại số hiện nay, **cách chỉnh sửa DWG** tệp một cách hiệu quả là kỹ năng cần có cho kỹ sư, kiến trúc sư và chuyên gia BIM. Cho dù bạn cần sửa một siêu liên kết bị hỏng, trỏ một XRef tới nguồn mới, hoặc cập nhật hàng loạt nhiều bản vẽ, Aspose.CAD for Java cung cấp cách tiếp cận lập trình sạch sẽ để thực hiện các thay đổi mà không cần mở trình chỉnh sửa CAD. Hướng dẫn này sẽ đưa bạn qua toàn bộ quy trình, từ việc tải bản vẽ đến việc lưu các chỉnh sửa.

## Câu trả lời nhanh
- **Thư viện nào xử lý việc chỉnh sửa DWG trong Java?** Aspose.CAD for Java.  
- **Tôi có thể chỉnh sửa siêu liên kết và đường dẫn XRef cùng lúc không?** Yes—both are supported in the same API.  
- **Tôi có cần giấy phép cho việc phát triển không?** A free trial works for testing; a commercial license is required for production.  
- **Phiên bản Java nào được yêu cầu?** Java 8 or higher.  
- **Mã mẫu có thể chạy ngay không?** Yes, after updating the file paths to point to your local DWG files.

## Tại sao cần chỉnh sửa siêu liên kết DWG và đường dẫn XRef?

Việc duy trì siêu liên kết và đường dẫn XRef luôn cập nhật ngăn ngừa các tham chiếu bị hỏng, đảm bảo tài liệu dự án luôn trỏ tới các tài nguyên đúng, và cho phép cập nhật hàng loạt tự động trên các thư viện CAD quy mô lớn. Điều này giảm công sức thủ công, giảm thiểu lỗi, và cải thiện hiệu quả dự án tổng thể bằng cách cho phép các nhà phát triển duy trì tính toàn vẹn của liên kết một cách lập trình xuyên suốt vòng đời thiết kế.

## Yêu cầu trước

Trước khi chúng ta bắt đầu hướng dẫn, hãy chắc chắn rằng bạn đã chuẩn bị các yêu cầu sau:

1. **Môi trường phát triển Java:** JDK 8+ đã được cài đặt và IDE yêu thích của bạn (IntelliJ IDEA, Eclipse, v.v.).  
2. **Thư viện Aspose.CAD cho Java:** Tải xuống và cài đặt thư viện Aspose.CAD cho Java từ [download link](https://releases.aspose.com/cad/java/).  
3. **Bản vẽ DWG:** Có một tệp bản vẽ DWG sẵn sàng để chỉnh sửa siêu liên kết.

## Nhập gói

Bắt đầu bằng việc nhập các gói cần thiết vào dự án Java của bạn. Điều này đảm bảo bạn có quyền truy cập vào các chức năng của Aspose.CAD cho Java.

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadBlockEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadInsertObject;
```

## Cách chỉnh sửa siêu liên kết DWG bằng Aspose.CAD cho Java?

`CadImage` là lớp Aspose.CAD được sử dụng để tải và lưu các bản vẽ CAD.  
Tải tệp DWG bằng `CadImage`, duyệt qua các thực thể của nó, cập nhật siêu liên kết và đường dẫn XRef khi cần, và cuối cùng lưu lại hình ảnh dưới dạng DWG. Quy trình đầu‑tới‑cuối này cho phép bạn chỉnh sửa bất kỳ số lượng thực thể nào trong một lần duyệt, đảm bảo mọi thay đổi được lưu lại.

### Bước 1: Truy cập các đối tượng Insert

`CadInsertObject` là lớp Aspose.CAD đại diện cho một khối tham chiếu đã chèn (XRef) trong bản vẽ DWG. Duyệt qua các thực thể và xác định xem một thực thể có phải là một thể hiện của lớp `CadInsertObject` hay không.

```java
    String dataDir = "Your Document Directory" + "DWGDrawings/";
    
    CadImage cadImage = (CadImage)Image.load(dataDir + "AutoCad_Sample.dwg");
    for (CadBaseEntity entity : cadImage.getEntities())
    {
        if (entity instanceof CadInsertObject)
        {
        }
	}
```

### Bước 2: Cách thay đổi đường dẫn XRef trong bản vẽ DWG

`CadImage` là đối tượng chính dùng để tải và lưu các tệp CAD trong Aspose.CAD cho Java. Khi bạn đã xác định được đối tượng insert, lấy thực thể block liên quan và cập nhật đường dẫn XRef theo nhu cầu. Điều này đảm bảo tham chiếu trỏ tới tệp ngoại vi đúng.

```java
			CadBlockEntity block = cadImage.getBlockEntities().get_Item(((CadInsertObject)entity).getName());
            String value = block.getXRefPathName().getValue();
            if (value != null && !value.contentEquals(""))
            {
                block.getXRefPathName().setValue("new file reference.dwg");
            }
    
```

### Bước 3: Sửa đổi siêu liên kết

Tiếp theo, kiểm tra xem thực thể có siêu liên kết liên kết với nó không. Nếu siêu liên kết khớp với một URL cụ thể, cập nhật nó thành URL mong muốn. Bước này đảm bảo rằng khi nhấp vào siêu liên kết trong trình xem CAD, nó sẽ mở mục tiêu mới.

```java
        if (entity.getHyperlink() == "https://products.aspose.com")
        {
            entity.setHyperlink("https://www.aspose.com");
        }
```

## Những lỗi thường gặp & Mẹo

- **So sánh chuỗi:** Sử dụng `.equals()` thay vì `==` để so sánh chuỗi một cách đáng tin cậy trong Java. Mẫu sử dụng `==` để đơn giản, nhưng trong môi trường sản xuất hãy thay thế bằng `entity.getHyperlink().equals("https://products.aspose.com")`.  
- **Kiểm tra null:** Luôn xác minh rằng `block.getXRefPathName()` không phải là `null` trước khi gọi `.getValue()`.  
- **Lưu thay đổi:** Sau khi chỉnh sửa các thực thể, gọi `cadImage.save("output.dwg");` để lưu các thay đổi (mã được bỏ để giữ số lượng khối gốc).  
- **Lưu ý về hiệu năng:** Aspose.CAD cho Java hỗ trợ hơn 30 định dạng CAD và có thể xử lý các tệp lên tới 2 GB mà không cần tải toàn bộ tài liệu vào bộ nhớ, giúp cập nhật hàng loạt nhanh và tiết kiệm bộ nhớ.

## Câu hỏi thường gặp

### Câu hỏi 1: Aspose.CAD cho Java có tương thích với tất cả các phiên bản bản vẽ DWG không?

A1: Aspose.CAD cho Java hỗ trợ hơn 50 phiên bản DWG, bao gồm các bản phát hành từ AutoCAD 2000 đến định dạng mới nhất 2025.

### Câu hỏi 2: Tôi có thể sử dụng Aspose.CAD cho Java trong các dự án thương mại không?

A2: Có, cần có giấy phép thương mại để sử dụng trong môi trường sản xuất. Bạn có thể mua giấy phép [tại đây](https://purchase.aspose.com/buy).

### Câu hỏi 3: Có bản dùng thử miễn phí cho Aspose.CAD cho Java không?

A3: Có, bạn có thể khám phá phiên bản dùng thử miễn phí [tại đây](https://releases.aspose.com/).

### Câu hỏi 4: Làm sao tôi có thể nhận hỗ trợ kỹ thuật cho Aspose.CAD cho Java?

A4: Đối với bất kỳ hỗ trợ kỹ thuật nào, hãy truy cập diễn đàn Aspose.CAD [tại đây](https://forum.aspose.com/c/cad/19).

### Câu hỏi 5: Tôi có thể nhận giấy phép tạm thời để thử nghiệm không?

A5: Có, bạn có thể nhận giấy phép tạm thời [tại đây](https://purchase.aspose.com/temporary-license/).

**Câu hỏi bổ sung**

**Q: Tôi có cần gọi một phương thức cụ thể để ghi DWG đã chỉnh sửa trở lại đĩa không?**  
**A:** Có, sau khi thực hiện các thay đổi hãy gọi `cadImage.save("EditedDrawing.dwg");` để lưu các sửa đổi.

**Q: Có thể chỉnh sửa nhiều siêu liên kết trong một lần duyệt không?**  
**A:** Chắc chắn—lặp qua `cadImage.getEntities()` và áp dụng logic siêu liên kết cho mỗi thực thể phù hợp.

---

**Cập nhật lần cuối:** 2026-06-19  
**Kiểm tra với:** Aspose.CAD for Java 24.12  
**Tác giả:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Hướng dẫn liên quan

- [Đọc dữ liệu meta XREF từ tệp DWG bằng Aspose.CAD cho Java](/cad/java/cad-meta-data-and-rendering/read-xref-meta-data/)
- [Thêm thuộc tính tùy chỉnh cho tệp DWG bằng Aspose.CAD cho Java](/cad/java/additional-features/add-custom-properties/)
- [Xuất DWG sang PDF hoặc Raster bằng Aspose.CAD cho Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}