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

# Load DWG File & Access Underlay Flags – Aspose.CAD for Java

Trong các quy trình làm việc CAD hiện đại, **việc tải một tệp DWG** nhanh chóng và trích xuất các chi tiết underlay là một yêu cầu phổ biến. Dù bạn đang xây dựng một trình xem, tự động hoá xử lý hàng loạt, hay trích xuất siêu dữ liệu cho tích hợp GIS, Aspose.CAD for Java cung cấp cho bạn một cách tiếp cận sạch sẽ, dựa trên mã. Trong hướng dẫn này, chúng ta sẽ đi qua các bước **tải tệp DWG**, duyệt các thực thể của nó, và đọc các cờ underlay mà nhiều nhà phát triển thường bỏ qua.

## Quick Answers
- **Lớp chính để mở DWG là gì?** `com.aspose.cad.Image.load()` trả về một `CadImage`.
- **Đối tượng nào chứa thông tin underlay?** `CadUnderlay` (hoặc các loại kế thừa như `CadDgnUnderlay`).
- **Có cần giấy phép cho việc phát triển không?** Bản dùng thử miễn phí hoạt động cho việc thử nghiệm; giấy phép thương mại cần thiết cho môi trường sản xuất.
- **Có thể xử lý nhiều tệp DWG trong một vòng lặp không?** Có – chỉ cần lặp lại mẫu tải‑và‑duyệt.
- **Cách tiếp cận này có tương thích với Java 11+ không?** Hoàn toàn, Aspose.CAD hỗ trợ Java 8 tới các phiên bản LTS mới nhất.

## What is “load dwg file” in Aspose.CAD?
`Image.load()` đọc nội dung nhị phân DWG và tạo một đối tượng `CadImage` trong bộ nhớ. Từ đó bạn có thể khám phá các lớp, block và thực thể underlay mà không cần xử lý định dạng tệp DWG trực tiếp.

## Why extract underlay flags from a DWG?
Các cờ underlay cho bạn biết cách một tham chiếu bên ngoài (như underlay DGN hoặc PDF) được đặt vị trí, tỉ lệ và xoay trong bản vẽ. Biết các giá trị này giúp bạn:

- Tái tạo bố cục hình ảnh chính xác trong một trình xem tùy chỉnh.
- Chuyển đổi underlay sang các thực thể CAD gốc để tiếp tục chỉnh sửa.
- Tạo báo cáo bao gồm siêu dữ liệu underlay cho mục đích tuân thủ hoặc tài liệu.

## Prerequisites
- **Thư viện Aspose.CAD** – tải về từ trang [releases](https://releases.aspose.com/cad/java/).
- **Bộ công cụ phát triển Java** – JDK 8 hoặc mới hơn.
- **Một thư mục** chứa các tệp DWG bạn muốn phân tích. Thay thế `"Your Document Directory"` trong mã bằng đường dẫn thực tế của bạn.

## Import Namespaces

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.CadUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.UnderlayFlags;
```

## Step‑by‑Step Guide

### Step 1: Set the Resource Directory
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```
Xác định vị trí các tệp DWG của bạn. Sử dụng một thư mục riêng giúp mẫu code gọn gàng và dễ di chuyển.

### Step 2: Load the DWG File
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
Ở đây chúng ta **load dwg file** `BlockRefDgn.dwg` vào một thể hiện `CadImage`, sẵn sàng để kiểm tra.

### Step 3: Iterate Through DWG Entities
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
Vòng lặp duyệt qua mọi thực thể—đường thẳng, vòng tròn, block và underlay—để chúng ta có thể chọn ra những gì cần thiết.

### Step 4: Identify CadDgnUnderlay Entities
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
Chỉ các đối tượng `CadDgnUnderlay` mới chứa các cờ underlay mà chúng ta đang tìm, vì vậy chúng ta sẽ lọc chúng.

### Step 5: Access Underlay Information
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
Khi đã có một `CadUnderlay`, chúng ta có thể đọc đường dẫn, tên, điểm chèn, góc xoay, hệ số tỉ lệ, và enum `UnderlayFlags` cho biết trạng thái hiển thị, cắt, và các tùy chọn render khác.

## Common Issues & Tips
- **Null underlay path** – Đảm bảo DWG thực sự tham chiếu tới một tệp bên ngoài; nếu không đường dẫn sẽ rỗng.
- **Unsupported underlay type** – Aspose.CAD hiện chỉ hỗ trợ underlay DGN; underlay PDF chưa được cung cấp qua API.
- **License exceptions** – Chạy mã mà không có giấy phép hợp lệ sẽ thêm watermark vào bất kỳ hình ảnh xuất ra nào.

## Frequently Asked Questions

**Q: Can I use Aspose.CAD for Java with other CAD file formats?**  
A: Aspose.CAD chủ yếu tập trung vào định dạng DWG, nhưng cũng hỗ trợ DXF, DWF và các định dạng CAD khác.

**Q: Is there a trial version available for Aspose.CAD for Java?**  
A: Yes, you can explore the features with a free trial from [here](https://releases.aspose.com/).

**Q: How can I get support or seek assistance with Aspose.CAD for Java?**  
A: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community support and discussions.

**Q: Are temporary licenses available for Aspose.CAD for Java?**  
A: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).

**Q: Where can I find the comprehensive documentation for Aspose.CAD for Java?**  
A: Refer to the [documentation](https://reference.aspose.com/cad/java/) for detailed information.

---

**Last Updated:** 2025-12-22  
**Tested With:** Aspose.CAD 24.12 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}