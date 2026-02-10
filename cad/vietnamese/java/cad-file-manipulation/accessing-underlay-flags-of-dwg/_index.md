---
date: 2025-12-22
description: Tìm hiểu cách tải tệp DWG và trích xuất thông tin underlay bằng Aspose.CAD
  cho Java – hướng dẫn từng bước bao gồm các cờ underlay.
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: Tải tệp DWG & Truy cập cờ Underlay – Aspose.CAD cho Java
url: /vi/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tải cờ cơ sở truy cập và tệp DWG – Aspose.CAD cho Java

Trong quy trình làm việc CAD hiện đại, **việc tải một tệp DWG** nhanh chóng và trích xuất các chi tiết underlay là một yêu cầu phổ biến. Dù bạn đang xây dựng một trình xem, bộ xử lý tự động hóa hàng loạt, hay trích xuất siêu dữ liệu để phân tích GIS hợp lý, Aspose.CAD for Java sẽ cung cấp cho bạn một cách tiếp cận sạch sẽ dựa trên mã hóa. Trong hướng dẫn này, chúng tôi sẽ thực hiện các bước **tải tệp DWG**, duyệt các thực thể của nó và đọc các cờ lót mà nhiều nhà phát triển thường bỏ qua.

## Trả lời nhanh
- **Lớp chính để mở DWG là gì?** `com.aspose.cad.Image.load()` trả về một `CadImage`.
- **Đối tượng nào chứa underlay thông tin?** `CadUnderlay` (hoặc các loại kế hoạch khác như `CadDgnUnderlay`).
- **Có cần giấy phép để phát triển không?** Bản dùng thử miễn phí hoạt động cho thử nghiệm; giấy phép thương mại cần thiết cho môi trường sản xuất.
- **Có thể xử lý nhiều tệp DWG trong một vòng lặp không?** Có – chỉ cần lặp lại tải mẫu và duy nhất.
- **Hướng dẫn tiếp theo này có tương thích với Java11+ không?** Hoàn toàn, Aspose.CAD hỗ trợ Java8 tới phiên bản LTS mới nhất.

## “tải tệp dwg” trong Aspose.CAD là gì?
`Image.load()` đọc DWG nhị phân nội dung và tạo một đối tượng `CadImage` trong bộ nhớ. Từ đó, bạn có thể khám phá các lớp, chặn và thực hiện lớp lót mà không cần xử lý trực tiếp dưới dạng tệp DWG.

## Tại sao phải trích xuất cờ lót từ DWG?
Lớp lót cờ cho bạn biết cách một bên ngoài tham chiếu (như lớp lót DGN hoặc PDF) được đặt ở vị trí, chế độ và xoay trong bản vẽ. Việc biết các giá trị này giúp bạn:

- Tái tạo bố cục hình ảnh chính xác trong một trình chỉnh sửa xem.
- Chuyển đổi lớp lót sang bản gốc CAD của các thiết bị thực thi để tiếp tục chỉnh sửa.
- Tạo báo cáo bao gồm lớp lót siêu dữ liệu cho mục tiêu hoặc tài liệu.

## Điều kiện tiên quyết
- **Thư viện Aspose.CAD** – tải về từ trang [releases](https://releases.aspose.com/cad/java/).
- **Bộ công cụ phát triển Java** – JDK8 hoặc mới hơn.
- **Một thư mục** chứa các tệp DWG mà bạn muốn phân tích. Thay thế `"Thư mục tài liệu của bạn"` bằng mã hóa bằng đường dẫn thực tế của bạn.

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

### Bước 1: Thiết lập thư mục tài nguyên
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```
Xác định vị trí các tệp DWG của bạn. Sử dụng một thư mục riêng giúp mẫu code gọn gàng và dễ di chuyển.

### Bước 2: Tải tệp DWG
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
Ở đây chúng ta **load dwg file** `BlockRefDgn.dwg` vào một thể hiện `CadImage`, sẵn sàng để kiểm tra.

### Bước 3: Duyệt qua các đối tượng DWG
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
Vòng lặp duyệt qua mọi thực thể—đường thẳng, vòng tròn, block và underlay—để chúng ta có thể chọn ra những gì cần thiết.

### Bước 4: Xác định các đối tượng CadDgnUnderlay
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
Chỉ các đối tượng `CadDgnUnderlay` mới chứa các cờ underlay mà chúng ta đang tìm, vì vậy chúng ta sẽ lọc chúng.

### Bước 5: Truy cập thông tin lớp phủ
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
Khi đã có một `CadUnderlay`, chúng ta có thể đọc đường dẫn, tên, điểm chèn, góc xoay, hệ số tỉ lệ, và enum `UnderlayFlags` cho biết trạng thái hiển thị, cắt, và các tùy chọn render khác.

## Các vấn đề thường gặp & Mẹo
- **Đường dẫn lót rỗng** – Đảm bảo DWG thực sự tham chiếu tới một tệp bên ngoài; if not đường dẫn sẽ trống.
- **Loại lớp phủ không được hỗ trợ** – DGN lớp phủ hỗ trợ duy nhất Aspose.CAD hiện hỗ trợ; Underlay PDF chưa được cung cấp qua API.
- **Các ngoại lệ về giấy phép** – Chạy mã mà không có hợp lệ giấy phép sẽ thêm hình mờ vào bất kỳ hình ảnh nào được xuất ra.

## Câu hỏi thường gặp

**Hỏi: Tôi có thể sử dụng Aspose.CAD cho Java với các định dạng tệp CAD khác không?**
A: Aspose.CAD chủ yếu tập trung vào định dạng DWG, nhưng cũng hỗ trợ DXF, DWF và các định dạng CAD khác.

**Hỏi: Có phiên bản dùng thử nào dành cho Aspose.CAD cho Java không?**
Đáp: Có, bạn có thể khám phá các tính năng bằng bản dùng thử miễn phí tại [tại đây](https://releases.aspose.com/).

**Hỏi: Làm thế nào để nhận được hỗ trợ hoặc tìm kiếm trợ giúp về Aspose.CAD cho Java?**
Trả lời: Hãy truy cập [diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để được hỗ trợ và thảo luận từ cộng đồng.

**Hỏi: Có giấy phép tạm thời cho Aspose.CAD cho Java không?**
Trả lời: Có, bạn có thể nhận được giấy phép tạm thời [tại đây](https://purchase.aspose.com/temporary-license/).

**Hỏi: Tôi có thể tìm tài liệu đầy đủ về Aspose.CAD cho Java ở đâu?**
Trả lời: Tham khảo [tài liệu](https://reference.aspose.com/cad/java/) để biết thông tin chi tiết.

---

**Cập nhật lần cuối:** 2025-12-22
**Đã kiểm thử với:** Aspose.CAD 24.12 cho Java
**Tác giả:** Aspose 

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}