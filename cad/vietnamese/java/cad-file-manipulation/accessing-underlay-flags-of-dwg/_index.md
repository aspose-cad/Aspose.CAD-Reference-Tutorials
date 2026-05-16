---
date: 2026-02-23
description: Tìm hiểu cách tải tệp DWG bằng Aspose.CAD DWG cho Java và trích xuất
  các cờ underlay – hướng dẫn chi tiết từng bước cho các nhà phát triển.
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: aspose cad dwg – Tải DWG & Truy cập Cờ Underlay (Java)
url: /vi/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

 shortcodes.

Finally backtop button shortcode.

Make sure to preserve all markdown formatting.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tải tệp DWG & Truy cập Cờ Underlay – Aspose.CAD cho Java

Trong các quy trình CAD hiện đại, **với aspose cad dwg bạn có thể nhanh chóng tải một tệp DWG** và trích xuất chi tiết underlay thường bị ẩn đối với người xem thông thường. Dù bạn đang xây dựng một **java dwg viewer**, tự động hoá quy trình batch dwg, hay trích xuất siêu dữ liệu cho tích hợp GIS, Aspose.CAD cho Java cung cấp cho bạn một cách tiếp cận sạch sẽ, code‑first. Trong tutorial này chúng ta sẽ đi qua các bước chính xác để **tải một tệp DWG**, duyệt các thực thể của nó, và đọc các cờ underlay mà nhiều nhà phát triển thường bỏ qua.

## Câu trả lời nhanh
- **Lớp chính để mở một DWG là gì?** `com.aspose.cad.Image.load()` trả về một `CadImage`.
- **Đối tượng nào chứa thông tin underlay?** `CadUnderlay` (hoặc các kiểu kế thừa như `CadDgnUnderlay`).
- **Tôi có cần giấy phép cho việc phát triển không?** Bản dùng thử miễn phí hoạt động cho việc thử nghiệm; giấy phép thương mại cần thiết cho môi trường sản xuất.
- **Tôi có thể xử lý nhiều tệp DWG trong một vòng lặp không?** Có – chỉ cần lặp lại mẫu tải‑và‑duyệt.
- **Cách tiếp cận này có tương thích với Java 11+ không?** Hoàn toàn, Aspose.CAD hỗ trợ Java 8 tới các phiên bản LTS mới nhất.

## aspose cad dwg – Tải tệp DWG (Java)

`Image.load()` đọc nội dung nhị phân DWG và tạo một đối tượng `CadImage` trong bộ nhớ. Từ đó bạn có thể khám phá các lớp, block và thực thể underlay mà không cần tự mình xử lý định dạng tệp DWG.

## Tại sao cần trích xuất cờ underlay từ DWG?

Cờ underlay cho bạn biết cách một tham chiếu bên ngoài (như underlay DGN hoặc PDF) được định vị, tỉ lệ và xoay trong bản vẽ. Biết các giá trị này giúp bạn:

- Tái tạo bố cục hình ảnh chính xác trong một **java dwg viewer** tùy chỉnh.
- Chuyển đổi underlay sang các thực thể CAD gốc để chỉnh sửa tiếp.
- Tạo báo cáo bao gồm siêu dữ liệu underlay cho mục đích tuân thủ hoặc tài liệu.
- **Batch process dwg** tệp và lưu siêu dữ liệu underlay của chúng vào cơ sở dữ liệu để phân tích sau.

## Yêu cầu trước
- **Aspose.CAD Library** – tải về từ trang [releases](https://releases.aspose.com/cad/java/).  
- **Java Development Kit** – JDK 8 hoặc mới hơn.  
- **Một thư mục** chứa các tệp DWG bạn muốn phân tích. Thay thế `"Your Document Directory"` trong mã bằng đường dẫn thực tế của bạn.

## Nhập không gian tên

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.CadUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.UnderlayFlags;
```

## Hướng dẫn từng bước

### Bước 1: Đặt Thư mục Tài nguyên
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```
Xác định nơi lưu trữ các tệp DWG của bạn. Sử dụng một thư mục riêng giúp mẫu code sạch sẽ và dễ di chuyển.

### Bước 2: Tải tệp DWG
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
Ở đây chúng ta **load dwg file** `BlockRefDgn.dwg` vào một thể hiện `CadImage`, sẵn sàng để kiểm tra.

### Bước 3: Duyệt qua các Thực thể DWG
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
Vòng lặp duyệt mọi thực thể—đường thẳng, vòng tròn, block và underlay—để chúng ta có thể chọn ra những cái cần thiết.

### Bước 4: Xác định các Thực thể CadDgnUnderlay
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
Chỉ các đối tượng `CadDgnUnderlay` chứa các cờ underlay mà chúng ta cần, vì vậy chúng ta sẽ lọc chúng.

### Bước 5: Truy cập Thông tin Underlay
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
Khi đã có một `CadUnderlay`, chúng ta có thể đọc đường dẫn, tên, điểm chèn, góc xoay, hệ số tỉ lệ, và enum `UnderlayFlags` cho biết trạng thái hiển thị, cắt, và các tùy chọn render khác.

## Cách tải tệp dwg trong quy trình xử lý hàng loạt

Nếu bạn cần **batch process dwg** các tệp, hãy bọc các bước trên trong một vòng lặp `for` đơn giản duyệt qua tất cả các tệp trong `dataDir`. Lệnh `Image.load()` hoạt động cho mỗi tệp, và bạn có thể lưu các cờ đã trích xuất vào CSV hoặc cơ sở dữ liệu để báo cáo downstream.

## Các vấn đề thường gặp & Mẹo
- **Null underlay path** – Đảm bảo DWG thực sự tham chiếu tới một tệp bên ngoài; nếu không đường dẫn sẽ rỗng.
- **Unsupported underlay type** – Aspose.CAD hiện hỗ trợ underlay DGN; underlay PDF chưa được cung cấp qua API.
- **License exceptions** – Chạy mã mà không có giấy phép hợp lệ sẽ thêm watermark vào bất kỳ hình ảnh xuất ra nào.
- **Performance tip:** Tái sử dụng một thể hiện `Image` duy nhất khi xử lý nhiều tệp trong batch để giảm áp lực GC.

## Câu hỏi thường gặp

**Q: Tôi có thể sử dụng Aspose.CAD cho Java với các định dạng tệp CAD khác không?**  
A: Aspose.CAD chủ yếu tập trung vào định dạng DWG, nhưng cũng hỗ trợ DXF, DWF và các định dạng CAD khác.

**Q: Có phiên bản dùng thử cho Aspose.CAD cho Java không?**  
A: Có, bạn có thể khám phá các tính năng với bản dùng thử miễn phí từ [here](https://releases.aspose.com/).

**Q: Làm thế nào để tôi nhận được hỗ trợ hoặc trợ giúp với Aspose.CAD cho Java?**  
A: Truy cập [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) để nhận hỗ trợ cộng đồng và thảo luận.

**Q: Có giấy phép tạm thời cho Aspose.CAD cho Java không?**  
A: Có, bạn có thể lấy giấy phép tạm thời [here](https://purchase.aspose.com/temporary-license/).

**Q: Tôi có thể tìm tài liệu đầy đủ cho Aspose.CAD cho Java ở đâu?**  
A: Tham khảo [documentation](https://reference.aspose.com/cad/java/) để có thông tin chi tiết.

---

**Cập nhật lần cuối:** 2026-02-23  
**Đã kiểm tra với:** Aspose.CAD 24.12 cho Java  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}