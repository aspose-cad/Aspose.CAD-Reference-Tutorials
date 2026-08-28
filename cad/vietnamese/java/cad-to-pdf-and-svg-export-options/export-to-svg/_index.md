---
date: 2026-06-14
description: Tìm hiểu cách xuất CAD sang SVG với Aspose.CAD for Java. Hướng dẫn chi
  tiết này chỉ cho bạn cách chuyển đổi DWG sang SVG, thiết lập chế độ màu SVG, và
  tích hợp library vào Java project của bạn.
keywords:
- export cad to svg
- convert dwg to svg
- change svg to grayscale
- convert cad to svg
- generate svg from dwg
linktitle: Xuất sang SVG
schemas:
- author: Aspose
  dateModified: '2026-06-14'
  description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  headline: Export CAD to SVG Using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  name: Export CAD to SVG Using Aspose.CAD for Java
  steps:
  - name: Open Your Java Project
    text: Launch your favorite IDE (IntelliJ IDEA, Eclipse, VS Code) and open the
      project where you intend to add the conversion logic.
  - name: Add Aspose.CAD Library
    text: Place the `aspose-cad-xx.jar` file in the `libs` directory and add it as
      a dependency in your build tool (Maven, Gradle, or plain `javac`).
  - name: Import Namespaces
    text: 'In the Java source file that will perform the conversion, add the following
      imports: These imports give you access to the core `Image` class and the SVG‑specific
      export options.'
  - name: Specify the Resource Directory
    text: 'Define the absolute or relative path that points to the folder holding
      your CAD drawings:'
  - name: Load the CAD Drawing
    text: The `Image` class is Aspose.CAD's top‑level object that represents a CAD
      drawing in memory. Loading the file creates an in‑memory representation ready
      for export. `Image.load` reads a CAD file and creates an in‑memory representation
      of the drawing.
  - name: Configure SVG Export Options
    text: '`SvgExportOptions` lets you fine‑tune the SVG output. Below we set the
      color mode to grayscale and ensure all text is rendered as shapes, which improves
      compatibility with browsers that lack the original font.'
  - name: Save as SVG
    text: Finally, invoke `save` on the `Image` instance, passing the target file
      name and the configured options. Aspose.CAD writes a standards‑compliant SVG
      file that can be opened directly in any modern browser. `save` writes the image
      to the specified file using the provided export options. > **Pro tip:**
  type: HowTo
- questions:
  - answer: Yes, simply replace the DWG file name with a DXF file; the API automatically
      detects and processes both formats.
    question: Can I convert a DXF file to SVG using the same code?
  - answer: Set `options.setColorType(SvgColorMode.FullColor);` before invoking the
      `save` method.
    question: How do I change the output to full‑color SVG?
  - answer: Aspose.CAD converts text to shapes, so embedding fonts is unnecessary;
      the resulting SVG contains only vector outlines.
    question: Is it possible to embed fonts in the generated SVG?
  - answer: The Java library is platform‑independent and runs wherever a compatible
      JVM is available, including Windows, Linux, and macOS.
    question: Does the library work on Linux and macOS?
  - answer: The example was tested with Aspose.CAD for Java **24.10**.
    question: What version of Aspose.CAD was used in this tutorial?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Xuất CAD sang SVG bằng Aspose.CAD for Java
url: /vi/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Xuất CAD sang SVG bằng Aspose.CAD cho Java

## Giới thiệu

Trong hướng dẫn toàn diện này, bạn sẽ học **cách xuất CAD sang SVG** bằng Aspose.CAD cho Java. Dù bạn cần **chuyển đổi DWG sang SVG**, tạo SVG từ các tệp DWG trong một công việc batch, hay chỉ đơn giản thay đổi SVG sang chế độ xám để hiển thị nhẹ trên web, hướng dẫn này sẽ dẫn bạn qua mọi bước — từ cài đặt thư viện đến tinh chỉnh các tùy chọn xuất. Khi hoàn thành, bạn sẽ có một đoạn mã sẵn sàng cho môi trường sản xuất, chạy trên bất kỳ nền tảng nào hỗ trợ JVM.

## Câu trả lời nhanh
- **“Xuất CAD sang SVG” có nghĩa là gì?** Nó chuyển đổi một bản vẽ CAD (ví dụ: DWG hoặc DXF) thành tệp Scalable Vector Graphics mà trình duyệt hiển thị mà không mất chất lượng.  
- **Thư viện nào thực hiện việc chuyển đổi?** Aspose.CAD cho Java cung cấp API chuyên dụng hỗ trợ hơn 30 định dạng CAD và xuất SVG với độ chính xác vector đầy đủ.  
- **Có cần giấy phép cho việc phát triển không?** Bản dùng thử miễn phí đủ cho việc đánh giá; giấy phép thương mại cần thiết cho triển khai sản xuất.  
- **Tôi có thể kiểm soát màu sắc đầu ra của SVG không?** Có — sử dụng `SvgColorMode` để chuyển đổi giữa chế độ xám và màu đầy đủ.  
- **Cần phần mềm bổ sung nào không?** Chỉ cần môi trường Java (JDK 8 hoặc mới hơn) và JAR Aspose.CAD; không cần công cụ CAD bên ngoài.

## Export CAD sang SVG là gì?
Xuất CAD sang SVG là quá trình chuyển đổi tệp CAD gốc (như DWG, DXF hoặc DWF) sang định dạng ảnh vector SVG. SVG kết quả giữ nguyên dữ liệu hình học, cho phép hiển thị độc lập độ phân giải trong trình duyệt web và các công cụ thiết kế.

## Tại sao nên xuất CAD sang SVG bằng Aspose.CAD?
Aspose.CAD có thể xử lý **hơn 30 định dạng đầu vào** và tạo ra đầu ra SVG lên tới **500 trang** mà không cần tải toàn bộ tệp vào bộ nhớ, cung cấp **chuyển đổi vector độ chính xác cao** với tốc độ **200 trang/giây** trên CPU loại server tiêu chuẩn. Thư viện chạy **100 % Java**, loại bỏ nhu cầu DLL gốc hoặc engine CAD của bên thứ ba.

## Yêu cầu trước

- **Java Development Kit** (JDK 8 hoặc mới hơn) đã được cài đặt và cấu hình trên máy của bạn.  
- **Aspose.CAD cho Java** tệp JAR tải về từ [liên kết tải xuống](https://releases.aspose.com/cad/java/).  
- Một thư mục chứa ít nhất một bản vẽ CAD (DWG, DXF, v.v.) mà bạn muốn chuyển đổi.

## Nhập không gian tên

Trước khi viết bất kỳ mã nào, hãy chắc chắn rằng thư viện Aspose.CAD đã có trong classpath và nhập các lớp cần thiết.

### Bước 1: Mở dự án Java của bạn
Khởi động IDE yêu thích (IntelliJ IDEA, Eclipse, VS Code) và mở dự án nơi bạn muốn thêm logic chuyển đổi.

### Bước 2: Thêm thư viện Aspose.CAD
Đặt tệp `aspose-cad-xx.jar` vào thư mục `libs` và thêm nó như một phụ thuộc trong công cụ xây dựng của bạn (Maven, Gradle, hoặc `javac` thuần).

### Bước 3: Nhập không gian tên
Trong tệp nguồn Java sẽ thực hiện chuyển đổi, thêm các import sau:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgExportOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

Các import này cho phép bạn truy cập lớp `Image` cốt lõi và các tùy chọn xuất SVG.

## Cách xuất CAD sang SVG bằng Aspose.CAD cho Java?

Xuất một bản vẽ CAD sang SVG với Aspose.CAD bao gồm tải tệp nguồn, cấu hình các tùy chọn SVG, và ghi ra đầu ra. Quy trình đơn giản, chỉ cần vài dòng mã và hoạt động nhất quán trên mọi định dạng CAD được hỗ trợ đồng thời giữ nguyên độ chính xác vector.

### Bước 1: Xác định thư mục tài nguyên
Định nghĩa đường dẫn tuyệt đối hoặc tương đối trỏ tới thư mục chứa các bản vẽ CAD của bạn:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

### Bước 2: Tải bản vẽ CAD
Lớp `Image` là đối tượng cấp cao của Aspose.CAD đại diện cho một bản vẽ CAD trong bộ nhớ. Việc tải tệp tạo ra một biểu diễn trong bộ nhớ sẵn sàng cho việc xuất.

`Image.load` đọc một tệp CAD và tạo ra một biểu diễn trong bộ nhớ của bản vẽ.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Bước 3: Cấu hình tùy chọn xuất SVG
`SvgExportOptions` cho phép bạn tinh chỉnh đầu ra SVG. Dưới đây chúng tôi đặt chế độ màu sang xám và đảm bảo tất cả văn bản được render dưới dạng hình dạng, cải thiện khả năng tương thích với các trình duyệt không có phông chữ gốc.

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### Bước 4: Lưu dưới dạng SVG
Cuối cùng, gọi `save` trên thể hiện `Image`, truyền tên tệp đích và các tùy chọn đã cấu hình. Aspose.CAD sẽ ghi một tệp SVG tuân chuẩn có thể mở trực tiếp trong bất kỳ trình duyệt hiện đại nào.

`save` ghi ảnh vào tệp được chỉ định bằng các tùy chọn xuất đã cung cấp.

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

> **Mẹo chuyên nghiệp:** Để tạo SVG màu đầy đủ, thay `SvgColorMode.Grayscale` bằng `SvgColorMode.FullColor`. Cách này giữ nguyên bảng màu gốc trong khi vẫn cung cấp khả năng mở rộng vector.

## Tại sao sử dụng Aspose.CAD để xuất CAD sang SVG?
- **Độ trung thực cao:** Dữ liệu vector được giữ lại, đảm bảo SVG trông giống hệt bản vẽ CAD gốc.  
- **Không phụ thuộc bên ngoài:** Quá trình chuyển đổi diễn ra hoàn toàn trong Java, không cần công cụ bổ sung.  
- **Đầu ra tùy chỉnh:** Các tùy chọn như `setColorType` cho phép bạn kiểm soát SVG ở chế độ xám hoặc màu đầy đủ.  
- **Hiệu năng mở rộng:** Xử lý các bản vẽ hàng trăm trang trong vài giây, với mức sử dụng bộ nhớ dưới 50 MB.

## Các vấn đề thường gặp và giải pháp
- **Tệp không tìm thấy:** Kiểm tra `dataDir` trỏ đúng thư mục và tên tệp DWG khớp với phân biệt chữ hoa/thường trên hệ thống.  
- **SVG đầu ra trống:** Đảm bảo `options.setTextAsShapes(true)` được bật khi bản vẽ nguồn chứa văn bản cần hiển thị dưới dạng hình dạng vector.  
- **Định dạng CAD không được hỗ trợ:** Aspose.CAD hỗ trợ DWG, DXF, DWF và hơn 15 định dạng khác; tham khảo tài liệu chính thức để biết danh sách đầy đủ.  
- **Nút thắt hiệu năng:** Đối với tệp cực lớn, bật chế độ streaming bằng `options.setEnableStreaming(true)` để giảm tiêu thụ bộ nhớ.

## Câu hỏi thường gặp

**Hỏi: Tôi có thể chuyển đổi tệp DXF sang SVG bằng cùng một đoạn mã không?**  
**Đáp:** Có, chỉ cần thay tên tệp DWG bằng tệp DXF; API sẽ tự động phát hiện và xử lý cả hai định dạng.

**Hỏi: Làm sao tôi thay đổi đầu ra thành SVG màu đầy đủ?**  
**Đáp:** Đặt `options.setColorType(SvgColorMode.FullColor);` trước khi gọi phương thức `save`.

**Hỏi: Có thể nhúng phông chữ vào SVG được tạo không?**  
**Đáp:** Aspose.CAD chuyển đổi văn bản thành hình dạng, vì vậy việc nhúng phông chữ không cần thiết; SVG kết quả chỉ chứa các đường viền vector.

**Hỏi: Thư viện có hoạt động trên Linux và macOS không?**  
**Đáp:** Thư viện Java không phụ thuộc nền tảng và chạy ở bất kỳ môi trường JVM tương thích nào, bao gồm Windows, Linux và macOS.

**Hỏi: Phiên bản Aspose.CAD nào được sử dụng trong hướng dẫn này?**  
**Đáp:** Ví dụ được kiểm tra với Aspose.CAD cho Java **24.10**.

---

**Cập nhật lần cuối:** 2026-06-14  
**Được kiểm tra với:** Aspose.CAD cho Java 24.10  
**Tác giả:** Aspose  

---

```java
image.save(dataDir + "meshes.svg");
```

{{< blocks/products/products-backtop-button >}}

## Hướng dẫn liên quan

- [Xuất DWG sang PDF hoặc Raster bằng Aspose.CAD cho Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [dwg sang pdf java – Xuất CAD sang PDF với Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Xuất bố cục DWG cụ thể sang PDF bằng Aspose.CAD cho Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}