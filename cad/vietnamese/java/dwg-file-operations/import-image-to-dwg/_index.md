---
date: 2026-05-20
description: Tìm hiểu cách thêm hình ảnh vào các tệp DWG bằng Aspose.CAD for Java
  và cũng chuyển đổi DWG sang PDF. Hãy làm theo hướng dẫn chi tiết của chúng tôi để
  phát triển hiệu quả.
keywords:
- add image to dwg
- convert dwg to pdf
- import image into dwg
- embed raster image dwg
- dwg file operations
linktitle: Nhập hình ảnh vào tệp DWG bằng Java
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  headline: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  type: TechArticle
- description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  name: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  steps:
  - name: Load the DWG File
    text: First, point to the folder that contains your DWG drawing and load it with
      `Image.load`.
  - name: Define the Raster Image Definition
    text: The `CadRasterImageDef` class defines the external raster image resource
      to be embedded in the drawing.
  - name: Set Insertion Point and Scaling Vectors
    text: The insertion point determines where the lower‑left corner of the image
      will appear. The **U** and **V** vectors control horizontal and vertical scaling.
  - name: Create the CadRasterImage Object
    text: The `CadRasterImage` entity represents a raster picture placed in the DWG
      model space.
  - name: Add the Image to Model Space
    text: Insert the raster image into the `*Model_Space` block, then update the drawing’s
      object collection so the definition is saved.
  - name: Configure PDF Export Options (Optional)
    text: '`PdfOptions` specifies settings for saving a CAD drawing as a PDF file.
      `CadRasterizationOptions` defines how the CAD content is rasterized during PDF
      conversion.'
  - name: Save the Resulting PDF
    text: 'Finally, export the modified drawing as a PDF file. The same `image` instance
      is used, so the PDF reflects the newly added raster image. By following these
      steps, you can **add image to dwg** files quickly and also **save dwg as pdf**
      when needed, covering the most common **dwg file operations** in '
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java works with any IDE that supports JDK 8+, including
      IntelliJ IDEA, Eclipse, and VS Code.
    question: Is Aspose.CAD for Java compatible with all Java development environments?
  - answer: Yes, you can use Aspose.CAD for Java for commercial projects. Visit **[here](https://purchase.aspose.com/buy)**
      for licensing details.
    question: Can I use Aspose.CAD for Java for commercial projects?
  - answer: Yes, you can access the free trial **[here](https://releases.aspose.com/)**.
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: You can seek support on the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**.
    question: How can I get support for Aspose.CAD for Java?
  - answer: Yes, you can get a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.
    question: Can I obtain a temporary license for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Thêm hình ảnh vào các tệp DWG một cách dễ dàng bằng Aspose.CAD Java
url: /vi/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Thêm Hình Ảnh vào Tệp DWG Một Cách Dễ Dàng Sử Dụng Aspose.CAD Java

Trong các ứng dụng Java hiện đại, **việc thêm hình ảnh vào DWG** là một yêu cầu phổ biến—cho dù bạn đang xây dựng một trình xem CAD, tự động cập nhật bản vẽ, hay tạo tài liệu. Aspose.CAD for Java cung cấp cho bạn một cách tiếp cận đơn giản, hiệu năng cao để nhúng hình ảnh raster trực tiếp vào bản vẽ DWG mà không cần một engine CAD đầy đủ. Trong hướng dẫn này, chúng tôi sẽ dẫn bạn qua toàn bộ quy trình, từ tải DWG đến xuất kết quả dưới dạng PDF, và chúng tôi cũng sẽ đề cập cách **nhập hình ảnh vào dwg** và **chuyển đổi dwg sang pdf** trong một luồng công việc duy nhất.

## Câu trả lời nhanh
- **Thư viện tôi cần là gì?** Aspose.CAD for Java  
- **Tôi có thể xuất ra PDF không?** Có – sử dụng `PdfOptions` cùng `CadRasterizationOptions`  
- **Tôi có cần giấy phép cho việc phát triển không?** Bản dùng thử miễn phí đủ cho việc thử nghiệm; cần giấy phép thương mại cho môi trường sản xuất  
- **Phiên bản Java nào được hỗ trợ?** Java 8 trở lên  
- **Thời gian thực hiện khoảng bao lâu?** Khoảng 10‑15 phút cho một việc nhập hình ảnh cơ bản  

## “Thêm hình ảnh vào dwg” là gì?
Thêm hình ảnh vào tệp DWG có nghĩa là nhúng một bức ảnh raster (PNG, JPEG, v.v.) dưới dạng thực thể **CadRasterImage** trong không gian mô hình của bản vẽ, nơi nó có thể được định vị, thu phóng và tùy chọn cắt giống như bất kỳ đối tượng CAD nào khác. Nó được lưu trong bảng đối tượng của bản vẽ và được hiển thị bởi các trình xem CAD tiêu chuẩn.

## Tại sao nên dùng Aspose.CAD for Java để thêm hình ảnh vào dwg?
Bạn có thể nhúng đồ họa raster vào tệp DWG mà không cần cài đặt phần mềm CAD của bên thứ ba, và API cung cấp cho bạn kiểm soát pixel‑perfect đối với điểm chèn, vectơ thu phóng và ranh giới cắt. Aspose.CAD xử lý các tệp lên tới 2 GB, hỗ trợ **hơn 50 định dạng đầu vào và đầu ra**, và chạy trên Windows, Linux và macOS, cho phép bạn tích hợp thao tác CAD vào bất kỳ backend Java nào.

## Yêu cầu trước
- **Aspose.CAD for Java** – tải JAR mới nhất từ trang chính thức **[here](https://releases.aspose.com/cad/java/)**.  
- **Java Development Kit** – JDK 8 hoặc mới hơn, với IDE ưa thích của bạn (IntelliJ IDEA, Eclipse, VS Code, v.v.).  
- Một **giấy phép Aspose.CAD** hợp lệ cho việc sử dụng trong sản xuất (bản dùng thử đủ cho việc thử nghiệm).  

## Nhập Gói
Các lệnh import sau đưa vào các lớp Aspose.CAD cần thiết cho việc xử lý hình ảnh và chuyển đổi PDF.  
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Hướng dẫn từng bước

### Bước 1: Tải Tệp DWG
Đầu tiên, chỉ đến thư mục chứa bản vẽ DWG của bạn và tải nó bằng `Image.load`.  
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### Bước 2: Định Nghĩa Raster Image Definition
Lớp `CadRasterImageDef` định nghĩa tài nguyên hình ảnh raster bên ngoài sẽ được nhúng vào bản vẽ.  
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### Bước 3: Đặt Điểm Chèn và Vectơ Thu Phóng
Điểm chèn xác định vị trí góc dưới‑trái của hình ảnh sẽ xuất hiện. Các vectơ **U** và **V** kiểm soát việc thu phóng theo chiều ngang và chiều dọc.  
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Bước 4: Tạo Đối Tượng CadRasterImage
Thực thể `CadRasterImage` đại diện cho một bức ảnh raster được đặt trong không gian mô hình DWG.  
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### Bước 5: Thêm Hình Ảnh vào Model Space
Chèn hình raster vào block `*Model_Space`, sau đó cập nhật bộ sưu tập đối tượng của bản vẽ để định nghĩa được lưu lại.  
```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadRasterImage);
CadBaseObject[] objs = cadImage.getObjects();
CadBaseObject[] arr = new CadBaseObject[objs.length + 1];
int ind = 0;
for (CadBaseObject obj : objs)
{
    arr[ind] = obj;
    ind++;
}
arr[ind] = cadRasterImageDef;
cadImage.setObjects(arr);
```

### Bước 6: Cấu Hình Tùy Chọn Xuất PDF (Tùy Chọn)
`PdfOptions` chỉ định các cài đặt khi lưu bản vẽ CAD dưới dạng tệp PDF. `CadRasterizationOptions` định nghĩa cách nội dung CAD được raster hoá trong quá trình chuyển đổi sang PDF.  
```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

### Bước 7: Lưu PDF Kết Quả
Cuối cùng, xuất bản vẽ đã chỉnh sửa dưới dạng tệp PDF. Cùng một instance `image` được sử dụng, vì vậy PDF sẽ phản ánh hình raster mới được thêm vào.  
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

Bằng cách làm theo các bước này, bạn có thể **thêm hình ảnh vào dwg** một cách nhanh chóng và cũng **lưu dwg dưới dạng pdf** khi cần, bao quát các **hoạt động với tệp dwg** phổ biến nhất trong một quy trình ngắn gọn.

## Các vấn đề thường gặp và giải pháp
- **Hình ảnh không hiển thị** – Kiểm tra lại đường dẫn tệp hình ảnh (`road-sign-custom.png`) có đúng không và kích thước hình ảnh có khớp với các giá trị truyền vào `CadRasterImageDef`.  
- **Thu phóng không đúng** – Điều chỉnh các vectơ U và V; chúng đại diện cho đơn vị vẽ trên mỗi pixel.  
- **PDF xuất ra trắng** – Đảm bảo `CadRasterizationOptions.setDrawType` được đặt thành `UseObjectColor` hoặc chế độ phù hợp khác.  

## Câu hỏi thường gặp

**Q: Aspose.CAD for Java có tương thích với mọi môi trường phát triển Java không?**  
A: Có, Aspose.CAD for Java hoạt động với bất kỳ IDE nào hỗ trợ JDK 8+, bao gồm IntelliJ IDEA, Eclipse và VS Code.

**Q: Tôi có thể sử dụng Aspose.CAD for Java cho các dự án thương mại không?**  
A: Có, bạn có thể sử dụng Aspose.CAD for Java cho các dự án thương mại. Truy cập **[here](https://purchase.aspose.com/buy)** để biết chi tiết về giấy phép.

**Q: Có bản dùng thử miễn phí cho Aspose.CAD for Java không?**  
A: Có, bạn có thể truy cập bản dùng thử miễn phí **[here](https://releases.aspose.com/)**.

**Q: Làm sao tôi có thể nhận hỗ trợ cho Aspose.CAD for Java?**  
A: Bạn có thể tìm kiếm hỗ trợ trên **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**.

**Q: Tôi có thể lấy giấy phép tạm thời cho Aspose.CAD for Java không?**  
A: Có, bạn có thể nhận giấy phép tạm thời **[here](https://purchase.aspose.com/temporary-license/)**.

---

**Cập nhật lần cuối:** 2026-05-20  
**Kiểm tra với:** Aspose.CAD for Java 24.11  
**Tác giả:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Hướng dẫn liên quan

- [Export DWG to PDF or Raster Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Add Custom Properties DWG Files Using Aspose.CAD for Java](/cad/java/additional-features/add-custom-properties/)
- [Save CAD as PNG – Convert CAD Drawing to Raster Image Format Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}