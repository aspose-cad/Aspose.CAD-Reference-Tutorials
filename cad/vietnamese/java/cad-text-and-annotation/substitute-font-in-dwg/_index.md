---
date: 2026-05-04
description: Học cách chuyển đổi dxf sang dwg và thiết lập phông chữ chính trong Java
  bằng Aspose.CAD. Hướng dẫn từng bước để có hình ảnh CAD hoàn hảo.
keywords:
- convert dxf to dwg
- set primary font
- change dwg text style
- how to substitute font
- aspose cad licensing
linktitle: Thay thế phông chữ trong DWG
second_title: Aspose.CAD Java API
title: Chuyển đổi dxf sang dwg và thay đổi phông chữ trong DWG Aspose.CAD Java
url: /vi/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách tải tệp DWG trong Java và thay thế phông chữ bằng Aspose.CAD

## Giới thiệu

Nếu bạn cần **convert dxf to dwg** trong các ứng dụng Java và muốn bản vẽ của mình trông chuyên nghiệp hơn, việc thay thế phông chữ là một cách nhanh chóng. Với Aspose.CAD for Java, bạn có thể thay thế kiểu chữ mặc định bằng bất kỳ phông chữ nào đã được cài đặt trên hệ thống, đảm bảo mọi chú thích hiển thị chính xác như mong muốn. Trong hướng dẫn này, chúng ta sẽ đi qua toàn bộ quy trình — từ việc tải tệp DWG trong Java đến việc sử dụng phương thức `setPrimaryFontName` để thay đổi phông chữ.

## Câu trả lời nhanh
- **What library do I need?** Aspose.CAD for Java.  
- **Can I load a DWG file in Java?** Có, chỉ cần gọi `Image.load()` với đường dẫn DWG.  
- **Which method changes the font?** `setPrimaryFontName`.  
- **Do I need a license for production?** Có, cần giấy phép thương mại.  
- **Is batch processing possible?** Chắc chắn – có thể lặp qua nhiều tệp với cùng một đoạn mã.

## convert dxf to dwg là gì?

“Convert dxf to dwg” đề cập đến việc chuyển đổi một tệp DXF (Drawing Exchange Format) sang định dạng DWG gốc được sử dụng bởi nhiều ứng dụng CAD. Việc chuyển đổi cho phép bạn lấy một bản vẽ DXF được hỗ trợ rộng rãi, đưa nó vào quy trình DWG, và sau đó áp dụng các kiểu dáng nâng cao — chẳng hạn như thay thế phông chữ — bằng Aspose.CAD.

## Tại sao phải thay thế phông chữ trong tệp DWG?

- **Consistency:** Đảm bảo mọi người cộng tác đều thấy cùng một kiểu chữ, bất kể cấu hình phông chữ cục bộ của họ.  
- **Readability:** Một số phông chữ CAD mặc định khó đọc trên màn hình; chuyển sang phông chữ sạch như Arial sẽ cải thiện độ rõ ràng.  
- **Branding:** Đồng nhất bản vẽ kỹ thuật với hướng dẫn phong cách của công ty.  

## Các trường hợp sử dụng phổ biến

| Kịch bản | Lý do quan trọng |
|----------|-------------------|
| **Batch conversion of legacy DXF drawings** | Bạn có thể chuyển chúng sang DWG và áp dụng phông chữ công ty trong một lần xử lý. |
| **Preparing drawings for client presentations** | Phông chữ nhất quán, dễ đọc giúp tài liệu trông chuyên nghiệp hơn. |
| **Automated CAD pipelines** | Nhúng việc thay thế phông chữ loại bỏ các bước xử lý thủ công sau khi tạo bản vẽ. |

## Yêu cầu trước

- **Java Development Kit (JDK)** – bất kỳ phiên bản mới nào (khuyến nghị 8+).  
- **Aspose.CAD for Java** – tải về từ [website](https://releases.aspose.com/cad/java/).  
- **Sample DWG/DXF file** – bản vẽ bạn muốn chỉnh sửa (bạn có thể dùng bất kỳ tệp DWG hoặc DXF nào để thử nghiệm).

## Nhập không gian tên

Trong dự án Java của bạn, nhập các lớp cần thiết để làm việc với Aspose.CAD. Các import này cho phép bạn tải hình ảnh, truy cập các đối tượng CAD và thao tác kiểu dáng.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## Hướng dẫn từng bước để thay thế phông chữ

### Bước 1: Tải tệp DWG của bạn (load dwg file java)

Đầu tiên, chỉ định vị trí tệp DWG (hoặc DXF) và tải nó vào một đối tượng `CadImage`.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **Pro tip:** Nếu bạn làm việc trực tiếp với tệp DWG, hãy thay thế phần mở rộng `.dxf` bằng `.dwg` trong biến `srcFile`.

### Bước 2: Duyệt bảng kiểu và đặt tên phông chữ chính

Mỗi bản vẽ CAD chứa một tập hợp các đối tượng style. Duyệt qua chúng và sử dụng phương thức `setPrimaryFontName` (gọi API **đặt tên phông chữ chính**) để thay thế phông chữ.

```java
for(Object style : cadImage.getStyles())
{
    // Set the font name
    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
}
```

Bạn có thể thay `"Arial"` bằng bất kỳ phông chữ nào đã được cài đặt trên máy chạy mã.

### Bước 3: Lưu bản vẽ đã chỉnh sửa

Sau khi cập nhật phông chữ, ghi các thay đổi vào một tệp DWG mới (hoặc ghi đè lên tệp gốc).

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

Tệp đã lưu bây giờ sẽ sử dụng phông chữ bạn chỉ định, và mọi chú thích văn bản sẽ được hiển thị với kiểu chữ đó.

## Vấn đề thường gặp và giải pháp

| Vấn đề | Giải pháp |
|--------|-----------|
| **Font not applied** | Kiểm tra xem phông chữ đã được cài đặt trên hệ điều hành và tên phông chữ có khớp chính xác không. |
| **`Image.load` throws an exception** | Đảm bảo đường dẫn tệp đúng và tệp là định dạng DWG/DXF được hỗ trợ. |
| **Performance slowdown on large files** | Xử lý tệp trong một luồng riêng hoặc batch chúng để tránh làm treo giao diện người dùng. |

## Câu hỏi thường gặp

**Q: Phương thức `setPrimaryFontName` có ảnh hưởng chỉ đến các thực thể văn bản không?**  
A: Nó cập nhật phông chữ chính cho bảng style, từ đó ảnh hưởng tới tất cả các đối tượng văn bản tham chiếu style đó.

**Q: Tôi có thể sử dụng phông chữ tùy chỉnh chưa được cài đặt trên hệ thống không?**  
A: Aspose.CAD dựa vào registry phông chữ của hệ điều hành. Để sử dụng phông chữ tùy chỉnh, bạn cần cài đặt nó trên máy chạy mã.

**Q: Có thể thay đổi phông chữ chỉ cho một lớp duy nhất không?**  
A: Có, bạn có thể lọc các style theo tên lớp trước khi gọi `setPrimaryFontName`.

**Q: Phiên bản Aspose.CAD nào cần thiết cho các tệp DWG 2022?**  
A: Bản phát hành mới nhất (tính đến 2025) hoàn toàn hỗ trợ DWG 2022. Luôn kiểm tra ghi chú phát hành để biết chi tiết hỗ trợ định dạng.

**Q: Làm sao xử lý giấy phép trong môi trường phát triển?**  
A: Sử dụng giấy phép đánh giá tạm thời để thử nghiệm. Đối với môi trường sản xuất, nhúng tệp giấy phép đã mua bằng `License.setLicense("Aspose.Total.Java.lic");`.

---

**Cập nhật lần cuối:** 2026-05-04  
**Kiểm tra với:** Aspose.CAD for Java 24.11  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}