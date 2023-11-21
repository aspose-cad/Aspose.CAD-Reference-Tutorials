---
title: Exporting DWF to PDF - Aspose.CAD Guide
linktitle: Exporting DWF to PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 10
url: /net/file-format-conversion/exporting-dwf-to-pdf/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
namespace Aspose.CAD.Examples.CSharp.Export
{
    public class ExportDWFToPDF
    {
        public static void Run()
        {
            //ExStart:ExportDWFToPDF
            // The path to the documents directory.
            string MyDir = RunExamples.GetDataDir_ConvertingCAD();
            string fileName = MyDir + "18-12-11 9644 - site.dwf";
            using (Image image = Image.Load(fileName))
            {
                
                CadRasterizationOptions dwfRasterizationOptions = new CadRasterizationOptions();                
                
                dwfRasterizationOptions.PageHeight = 500;
                dwfRasterizationOptions.PageWidth = 500;
               

                PdfOptions pdfOptions = new PdfOptions();
                pdfOptions.VectorRasterizationOptions = dwfRasterizationOptions;

                // export
                string outPath = MyDir + "18-12-11 9644 - site.pdf";
                image.Save(outPath, pdfOptions);

                //ExEnd:ExportDWFToPDF          
                Console.WriteLine("\n3D images exported successfully to PDF.\nFile saved at " + MyDir);
            }
        }
    }
}

```
