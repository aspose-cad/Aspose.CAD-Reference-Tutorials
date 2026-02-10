---
date: 2025-12-28
description: Tìm hiểu cách tải tệp DWG vào các dự án Java và đặt tên phông chữ chính
  bằng Aspose.CAD cho Java. Hướng dẫn từng bước để có hình ảnh CAD hoàn hảo.
linktitle: Substitute Font in DWG
second_title: Aspose.CAD Java API
title: Cách tải tệp DWG trong Java và thay thế phông chữ bằng Aspose.CAD
url: /vi/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách tải tệp DWG trong Java và thay thế phông chữ bằng Aspose.CAD

## Giới thiệu

Nếu bạn cần **tải tệp DWG trong Java** cho các ứng dụng và muốn bản vẽ của mình trông chuyên nghiệp hơn, việc thay thế phông chữ là một cách nhanh chóng. Với Aspose.CAD for Java, bạn có thể thay đổi kiểu chữ mặc định bằng bất kỳ phông chữ nào đã được cài đặt trên hệ thống, đảm bảo mọi chú thích hiển thị chính xác như mong muốn. Trong hướng dẫn này, chúng ta sẽ đi qua toàn bộ quy trình — từ việc tải tệp DWG trong Java đến việc sử dụng phương thức `setPrimaryFontName` để thay đổi phông chữ.

## Câu trả lời nhanh
- **Thư viện tôi cần là gì?** Aspose.CAD for Java.  
- **Tôi có thể tải tệp DWG trong Java không?** Có, chỉ cần gọi `Image.load()` với đường dẫn DWG.  
- **Phương thức nào thay đổi phông chữ?** `setPrimaryFontName`.  
- **Tôi có cần giấy phép cho môi trường production không?** Có, cần giấy phép thương mại.  
- **Có thể xử lý hàng loạt không?** Chắc chắn — lặp qua nhiều tệp với cùng một đoạn mã.

## “load dwg file java” là gì?

Tải tệp DWG trong môi trường Java có nghĩa là đọc dữ liệu CAD nhị phân vào một đối tượng `Image` mà Aspose.CAD có thể thao tác. Khi tệp đã được tải, bạn sẽ có quyền truy cập lập trình đầy đủ vào các lớp, kiểu dáng và thực thể văn bản.

## Tại sao phải thay thế phông chữ trong tệp DWG?

- **Tính nhất quán:** Đảm bảo mọi người cộng tác nhìn thấy cùng một kiểu chữ, bất kể cài đặt phông chữ cục bộ của họ.  
- **Độ đọc được:** Một số phông chữ CAD mặc định khó đọc trên màn hình; chuyển sang phông chữ sạch như Arial sẽ cải thiện độ rõ ràng.  
- **Thương hiệu:** Đưa các bản vẽ kỹ thuật phù hợp với hướng dẫn phong cách của công ty.

## Yêu cầu trước

- **Java Development Kit (JDK)** – bất kỳ phiên bản mới nào (khuyến nghị 8+).  
- **Aspose.CAD for Java** – tải về từ [website](https://releases.aspose.com/cad/java/).  
- **Tệp DWG mẫu** – bản vẽ bạn muốn chỉnh sửa (bạn có thể dùng bất kỳ tệp DWG hoặc DXF nào để thử).

## Nhập không gian tên

Trong dự án Java của bạn, nhập các lớp cần thiết để làm việc với Aspose.CAD. Những import này cho phép bạn tải ảnh, truy cập các đối tượng CAD và thao tác kiểu dáng.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## Hướng dẫn từng bước để thay thế phông chữ

### Bước 1: Tải tệp DWG của bạn (load dwg file java)

Đầu tiên, chỉ định vị trí tệp DWG (hoặc DXF) và tải nó vào đối tượng `CadImage`.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **Mẹo:** Nếu bạn làm việc trực tiếp với tệp DWG, thay đổi phần mở rộng `.dxf` thành `.dwg` trong biến `srcFile`.

### Bước 2: Duyệt bảng kiểu và đặt tên phông chữ chính

Mỗi bản vẽ CAD chứa một tập hợp các đối tượng kiểu. Lặp qua chúng và sử dụng phương thức `setPrimaryFontName` (lệnh API **đặt tên phông chữ chính**) để thay thế phông chữ.

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

## Các vấn đề thường gặp và giải pháp

| Vấn đề | Giải pháp |
|-------|----------|
| **Phông chữ không được áp dụng** | Kiểm tra phông chữ đã được cài đặt trên hệ điều hành và tên viết đúng hoàn toàn. |
| **`Image.load` gây ra ngoại lệ** | Đảm bảo đường dẫn tệp đúng và tệp là định dạng DWG/DXF được hỗ trợ. |
| **Giảm hiệu năng khi xử lý tệp lớn** | Xử lý tệp trong luồng riêng hoặc batch để tránh chặn UI. |

## Các câu hỏi thường gặp khác

**Hỏi: Phương thức `setPrimaryFontName` chỉ ảnh hưởng đến các thực thể văn bản?**  
Đáp: Nó cập nhật phông chữ chính cho bảng kiểu, do đó ảnh hưởng tới tất cả các đối tượng văn bản tham chiếu tới kiểu đó.

**Hỏi: Tôi có thể sử dụng phông chữ tùy chỉnh chưa được cài đặt trên hệ thống không?**  
Đáp: Aspose.CAD dựa vào registry phông chữ của hệ điều hành. Để dùng phông chữ tùy chỉnh, hãy cài đặt nó trên máy chạy mã.

**Hỏi: Có thể thay đổi phông chữ chỉ cho một lớp duy nhất không?**  
Đáp: Có, bạn có thể lọc các kiểu theo tên lớp trước khi gọi `setPrimaryFontName`.

**Hỏi: Phiên bản Aspose.CAD nào cần thiết cho tệp DWG 2022?**  
Đáp: Bản phát hành mới nhất (tính đến năm 2025) hoàn toàn hỗ trợ DWG 2022. Luôn kiểm tra ghi chú phát hành để biết chi tiết hỗ trợ định dạng.

**Hỏi: Làm sao xử lý giấy phép trong môi trường phát triển?**  
Đáp: Sử dụng giấy phép đánh giá tạm thời để thử nghiệm. Đối với production, nhúng file giấy phép đã mua bằng `License.setLicense("Aspose.Total.Java.lic");`.

---

**Cập nhật lần cuối:** 2025-12-28  
**Kiểm thử với:** Aspose.CAD for Java 24.11  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}