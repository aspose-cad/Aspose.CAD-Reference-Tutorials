---
date: 2026-03-05
description: Tìm hiểu cách đặt thời gian chờ cho các thao tác lưu khi chuyển đổi DWG
  sang PDF bằng Aspose.CAD cho .NET. Tăng cường hiệu suất và kiểm soát trong các ứng
  dụng .NET của bạn.
linktitle: Setting Timeout on Save Operation
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Cách Đặt Thời Gian Hết Hạn cho Hoạt Động Lưu - Hướng Dẫn Aspose.CAD
url: /vi/net/advanced-cad-techniques/setting-timeout-on-save-operation/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cách Đặt Thời Gian Chờ cho Hoạt Động Lưu - Hướng Dẫn Aspose.CAD

## Introduction

Trong hướng dẫn này, bạn sẽ học **cách đặt thời gian chờ** cho các hoạt động lưu CAD, một kỹ thuật giúp bạn ngăn các quá trình chuyển đổi kéo dài trở thành không phản hồi. Quản lý thời gian chờ đặc biệt hữu ích khi bạn **chuyển đổi DWG sang PDF** hoặc **xuất file CAD PDF** trong các công việc batch hoặc dịch vụ web. Aspose.CAD cho .NET cung cấp một API sạch sẽ cho phép bạn kiểm soát hoạt động lưu đồng thời vẫn tận dụng động cơ rasterization mạnh mẽ của nó.

## Quick Answers
- **Thời gian chờ kiểm soát gì?** Nó sẽ hủy bỏ hoạt động lưu/ xuất nếu chạy lâu hơn khoảng thời gian đã chỉ định.  
- **Định dạng nào hưởng lợi nhất?** Chuyển đổi các file DWG lớn sang PDF hoặc hình raster, nơi thời gian xử lý có thể thay đổi.  
- **Tôi có cần giấy phép không?** Cần có giấy phép Aspose.CAD hợp lệ cho môi trường sản xuất; bản dùng thử miễn phí đủ cho việc đánh giá.  
- **Tôi có thể tùy chỉnh thời lượng không?** Có — chỉ cần thay đổi giá trị `Thread.Sleep` (theo mili giây) cho phù hợp với kịch bản của bạn.  
- **Cách tiếp cận này có thân thiện với async không?** Ví dụ sử dụng `Task.Factory.StartNew`, giúp dễ dàng tích hợp vào quy trình async.

## What is “how to set timeout” in the context of CAD saving?

Việc “đặt thời gian chờ” trong ngữ cảnh lưu CAD có nghĩa là gì?  
Đặt thời gian chờ có nghĩa là gắn một `InterruptionToken` vào các tùy chọn lưu và kích hoạt ngắt sau một khoảng thời gian định trước. Điều này ngăn hoạt động bị treo vô hạn, mang lại hiệu năng dự đoán được và quản lý tài nguyên tốt hơn.

## Why use Aspose.CAD to convert DWG to PDF with a timeout?

- **Độ tin cậy:** Đảm bảo một quá trình chuyển đổi chạy quá thời gian sẽ không làm nghẽn dịch vụ của bạn.  
- **Khả năng mở rộng:** Cho phép xử lý nhiều file đồng thời mà không lo một file duy nhất làm chậm pipeline.  
- **Chất lượng:** Giữ nguyên rasterization độ chính xác cao của Aspose.CAD đồng thời bổ sung các biện pháp an toàn.

## Prerequisites

Trước khi bắt đầu, hãy chắc chắn bạn có:

- **Aspose.CAD cho .NET** – được tích hợp vào dự án của bạn. Bạn có thể tải xuống [tại đây](https://releases.aspose.com/cad/net/).
- **Thư mục tài liệu** – một thư mục nơi lưu trữ các file DWG nguồn và các file PDF đầu ra.

## Import Namespaces

Đầu tiên, nhập các namespace cung cấp các lớp cần thiết cho rasterization, tùy chọn PDF và cơ chế ngắt.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Threading;
using System.Threading.Tasks;
```

## How to Set Timeout on Save Operation

Dưới đây là hướng dẫn từng bước. Mỗi bước bao gồm một giải thích ngắn gọn và sau đó là khối mã gốc (không thay đổi).

### Step 1: Load CAD Drawing

**Bước 1: Tải Bản Vẽ CAD**

Chúng ta tải file DWG nguồn từ thư mục đã chỉ định. Phương thức `Image.Load` trả về một đối tượng `Image` đại diện cho bản vẽ CAD.

```csharp
// Example: Loading CAD Drawing
string SourceDir = "Your Document Directory";
string OutputDir = "Your Document Directory";

using (Image cadDrawing = Image.Load(SourceDir + "Drawing11.dwg"))
{
    // Code for subsequent steps will be placed here
}
```

### Step 2: Configure Rasterization Options

**Bước 2: Cấu Hình Tùy Chọn Rasterization**

Đặt các tùy chọn rasterization sao cho PDF xuất ra khớp với kích thước bản vẽ gốc. Đây là nơi bạn kiểm soát chiều rộng, chiều cao trang và các thiết lập render khác.

```csharp
// Example: Configuring Rasterization Options
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = cadDrawing.Size.Width;
rasterizationOptions.PageHeight = cadDrawing.Size.Height;
```

### Step 3: Create PDF Options (Export CAD PDF)

**Bước 3: Tạo Tùy Chọn PDF (Xuất CAD PDF)**

Tạo một thể hiện `PdfOptions` và gắn các cài đặt rasterization. Đối tượng này sẽ được truyền vào phương thức `Save` để tạo phiên bản PDF của file DWG.

```csharp
// Example: Creating PDF Options
PdfOptions CADf = new PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
```

### Step 4: Implement Timeout Mechanism

**Bước 4: Triển Khai Cơ Chế Thời Gian Chờ**

Chúng ta sử dụng `InterruptionTokenSource` để lấy một token có thể ngắt hoạt động lưu. Một task nền thực hiện việc xuất, trong khi luồng chính ngủ trong khoảng thời gian chờ mong muốn (ví dụ, 10 giây). Sau thời gian ngủ, chúng ta gọi `Interrupt()` để hủy thao tác nếu nó vẫn đang chạy.

```csharp
// Example: Implementing Timeout Mechanism
using (var its = new InterruptionTokenSource())
{
    CADf.InterruptionToken = its.Token;

    var exportTask = Task.Factory.StartNew(() =>
    {
        cadDrawing.Save(OutputDir + "PutTimeoutOnSave_out.pdf", CADf);
    });

    Thread.Sleep(10000); // Set your desired timeout duration in milliseconds
    its.Interrupt();

    exportTask.Wait();
}
```

### Step 5: Finalize and Confirm

**Bước 5: Hoàn Tất và Xác Nhận**

Sau khi xuất (hoặc ngắt), ghi một thông báo xác nhận lên console. Trong một ứng dụng thực tế, bạn có thể ghi log kết quả hoặc phát sinh một sự kiện.

```csharp
// Example: Finalizing and Confirming
Console.WriteLine("PutTimeoutOnSave executed successfully");
```

## Common Issues and Solutions

| Vấn đề | Nguyên nhân | Giải pháp |
|-------|------------|-----------|
| Xuất bị treo vô thời hạn | Không có token ngắt được gắn | Đảm bảo `CADf.InterruptionToken = its.Token;` được thiết lập trước khi bắt đầu task. |
| PDF rỗng hoặc bị hỏng | Đường dẫn thư mục đầu ra không đúng | Kiểm tra `OutputDir` kết thúc bằng dấu phân tách đường dẫn và tên file hợp lệ. |
| Thời gian chờ quá ngắn, gây hủy sớm | Giá trị `Thread.Sleep` quá thấp đối với file lớn | Tăng thời gian ngủ hoặc tính toán thời gian chờ thích ứng dựa trên kích thước file. |

## Frequently Asked Questions

**Q1: Tôi có thể tùy chỉnh thời lượng thời gian chờ không?**  
A: Chắc chắn. Thay đổi giá trị truyền vào `Thread.Sleep` (theo mili giây) để phù hợp với mong đợi hiệu năng của bạn.

**Q2: Có các tùy chọn khác cho rasterization không?**  
A: Có. `CadRasterizationOptions` cung cấp các thuộc tính như `Resolution`, `BackgroundColor` và `DrawType` để tinh chỉnh đầu ra PDF.

**Q3: Làm sao tôi có thể xử lý các lần ngắt trong ứng dụng?**  
A: Sử dụng các lớp `InterruptionToken` và `InterruptionTokenSource` như đã minh họa. Chúng cung cấp cách an toàn đa luồng để hủy các thao tác chạy lâu.

**Q4: Aspose.CAD có phù hợp cho cả file CAD 2D và 3D không?**  
A: Nó hỗ trợ một loạt các định dạng 2D và 3D, bao gồm DWG, DXF, DGN và nhiều hơn nữa.

**Q5: Tôi có thể tìm trợ giúp hoặc hỗ trợ cộng đồng ở đâu?**  
A: Truy cập [diễn đàn Aspose.CAD](https://forum.aspose.com/c/cad/19) để thảo luận cộng đồng, mẫu code và các mẹo khắc phục sự cố.

## Conclusion

Bằng cách thực hiện các bước trên, bạn đã biết **cách đặt thời gian chờ** cho các hoạt động lưu CAD, cho phép bạn một cách đáng tin cậy **chuyển đổi DWG sang PDF** hoặc **xuất CAD PDF** mà không lo các quá trình không phản hồi. Áp dụng mẫu này vào các bộ chuyển đổi batch, dịch vụ web hoặc bất kỳ pipeline tự động nào mà tính dự đoán là quan trọng.

---

**Cập nhật lần cuối:** 2026-03-05  
**Kiểm tra với:** Aspose.CAD 24.12 cho .NET  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}