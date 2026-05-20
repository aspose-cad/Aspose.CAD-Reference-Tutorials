---
date: 2026-03-05
description: Tanulja meg, hogyan állíthat be időkorlátot a mentési műveletekre a DWG
  PDF-re konvertálása során az Aspose.CAD for .NET használatával. Növelje a hatékonyságot
  és a vezérlést .NET alkalmazásaiban.
linktitle: Setting Timeout on Save Operation
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Hogyan állítsunk be időkorlátot a mentési műveletnél – Aspose.CAD útmutató
url: /hu/net/advanced-cad-techniques/setting-timeout-on-save-operation/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan állítsunk be időkorlátot a mentési műveletnél – Aspose.CAD útmutató

## Introduction

Ebben az útmutatóban megtanulja, **hogyan állítsunk be időkorlátot** a CAD mentési műveleteknél, egy olyan technikát, amely segít megakadályozni, hogy a hosszú ideig futó konverziók váljanak választhatatlan folyamatokká. Az időkorlát kezelése különösen hasznos, amikor **DWG‑t PDF‑re konvertál** vagy **CAD PDF‑et exportál** kötegelt feladatokban vagy webszolgáltatásokban. Az Aspose.CAD for .NET tiszta API‑t biztosít, amely lehetővé teszi a mentési művelet szabályozását, miközben továbbra is kihasználja a hatékony raszterizálási motorját.

## Quick Answers
- **What does the timeout control?** It aborts the save/export operation if it runs longer than the specified period.  
- **Which formats benefit most?** Converting large DWG files to PDF or raster images where processing time can vary.  
- **Do I need a license?** A valid Aspose.CAD license is required for production use; a free trial works for evaluation.  
- **Can I customize the duration?** Yes—simply change the `Thread.Sleep` value (in milliseconds) to suit your scenario.  
- **Is this approach async‑friendly?** The example uses `Task.Factory.StartNew`, making it easy to integrate into async workflows.

## What is “how to set timeout” in the context of CAD saving?
Az időkorlát beállítása azt jelenti, hogy egy `InterruptionToken`‑t csatolunk a mentési beállításokhoz, és egy előre meghatározott időintervallum után megszakítjuk a műveletet. Ez megakadályozza, hogy a folyamat örökké lefagyjon, így kiszámítható teljesítményt és jobb erőforrás-kezelést biztosít.

## Why use Aspose.CAD to convert DWG to PDF with a timeout?
- **Reliability:** Guarantees that a runaway conversion won’t block your service.  
- **Scalability:** Lets you process many files in parallel without fear of a single file stalling the pipeline.  
- **Quality:** Retains Aspose.CAD’s high‑fidelity rasterization while adding safety controls.

## Prerequisites

Mielőtt elkezdenénk, győződjön meg róla, hogy a következők rendelkezésre állnak:

- **Aspose.CAD for .NET** – integrálva a projektjébe. Letöltheti [itt](https://releases.aspose.com/cad/net/).
- **Document Directory** – egy mappa, ahol a forrás DWG fájlok és a kimeneti PDF‑ek tárolódnak.

## Import Namespaces

Először importálja azokat a névtereket, amelyek a raszterizáláshoz, PDF beállításokhoz és az megszakítási mechanizmushoz szükséges osztályokat tartalmazzák.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Threading;
using System.Threading.Tasks;
```

## How to Set Timeout on Save Operation

Az alábbiakban lépésről‑lépésre bemutatjuk a folyamatot. Minden lépés rövid magyarázatot tartalmaz, majd az eredeti kódrészletet (változtatás nélkül).

### Step 1: Load CAD Drawing

Betöltjük a forrás DWG fájlt a megadott könyvtárból. Az `Image.Load` metódus egy `Image` objektumot ad vissza, amely a CAD rajzot képviseli.

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

Állítsa be a raszterizálási opciókat, hogy az exportált PDF megegyezzen az eredeti rajz méreteivel. Itt szabályozhatja az oldal szélességét, magasságát és egyéb megjelenítési beállításokat.

```csharp
// Example: Configuring Rasterization Options
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = cadDrawing.Size.Width;
rasterizationOptions.PageHeight = cadDrawing.Size.Height;
```

### Step 3: Create PDF Options (Export CAD PDF)

Hozzon létre egy `PdfOptions` példányt, és csatolja a raszterizálási beállításokat. Ez az objektum kerül átadásra a `Save` metódusnak, amely a DWG fájlból PDF‑et generál.

```csharp
// Example: Creating PDF Options
PdfOptions CADf = new PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
```

### Step 4: Implement Timeout Mechanism

Az `InterruptionTokenSource`‑t használjuk egy token megszerzéséhez, amely képes megszakítani a mentési műveletet. Egy háttérfeladat végzi az exportálást, míg a fő szál a kívánt időkorlátig (például 10 másodperc) alvó állapotban van. Az alvás után meghívjuk az `Interrupt()`‑et, hogy leállítsuk a műveletet, ha még fut.

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

Az export (vagy megszakítás) után írjon egy megerősítő üzenetet a konzolra. Egy valós alkalmazásban esetleg naplózhatja az eredményt vagy eseményt generálhat.

```csharp
// Example: Finalizing and Confirming
Console.WriteLine("PutTimeoutOnSave executed successfully");
```

## Common Issues and Solutions

| Issue | Cause | Remedy |
|-------|-------|--------|
| Export hangs indefinitely | No interruption token attached | Ensure `CADf.InterruptionToken = its.Token;` is set before starting the task. |
| PDF is empty or corrupted | Output directory path incorrect | Verify `OutputDir` ends with a path separator and the file name is valid. |
| Timeout too short, causing premature abort | `Thread.Sleep` value too low for large files | Increase the sleep duration or calculate an adaptive timeout based on file size. |

## Frequently Asked Questions

**Q1: Can I customize the timeout duration?**  
A: Absolutely. Change the value passed to `Thread.Sleep` (in milliseconds) to match your performance expectations.

**Q2: Are there other options for rasterization?**  
A: Yes. `CadRasterizationOptions` offers properties such as `Resolution`, `BackgroundColor`, and `DrawType` to fine‑tune the PDF output.

**Q3: How can I handle interruptions in my application?**  
A: Use the `InterruptionToken` and `InterruptionTokenSource` classes as shown. They provide a thread‑safe way to abort long‑running operations.

**Q4: Is Aspose.CAD suitable for both 2D and 3D CAD files?**  
A: It supports a wide range of 2D and 3D formats, including DWG, DXF, DGN, and more.

**Q5: Where can I find further assistance or community support?**  
A: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community discussions, sample code, and troubleshooting tips.

## Conclusion

A fenti lépések követésével most már tudja, **hogyan állítsunk be időkorlátot** a CAD mentési műveleteknél, ami lehetővé teszi, hogy megbízhatóan **DWG‑t PDF‑re konvertáljon** vagy **CAD PDF‑et exportáljon** anélkül, hogy a folyamatok választhatatlanná válnának. Alkalmazza ezt a mintát kötegelt konverterekben, webszolgáltatásokban vagy bármely automatizált csővezetékben, ahol a kiszámíthatóság kulcsfontosságú.

---

**Last Updated:** 2026-03-05  
**Tested With:** Aspose.CAD 24.12 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}