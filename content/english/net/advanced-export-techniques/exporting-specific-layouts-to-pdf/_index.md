---
title: Exporting Specific Layouts to PDF - Aspose.CAD Guide
linktitle: Exporting Specific Layouts to PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 13
url: /net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
namespace Aspose.CAD.Examples.CSharp.DWG_Drawings
{
    public class ExportSpecificLayoutToPDF
    {
        public static void Run()
        {
            //ExStart:ExportSpecificLayoutToPDF
            // The path to the documents directory.
            string MyDir = RunExamples.GetDataDir_DWGDrawings();
            string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
            using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
            {
                // Create an instance of CadRasterizationOptions and set its various properties
                Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
                rasterizationOptions.PageWidth = 1600;
                rasterizationOptions.PageHeight = 1600;
                // Specify desired layout name
                rasterizationOptions.Layouts = new string[] { "Layout1" };

                // Create an instance of PdfOptions
                Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
                // Set the VectorRasterizationOptions property
                pdfOptions.VectorRasterizationOptions = rasterizationOptions;

                MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
                //Export the DWG to PDF
                image.Save(MyDir, pdfOptions);                
            }
            //ExEnd:ExportSpecificLayoutToPDF            
            Console.WriteLine("\nThe DWG file with specific layout exported successfully to PDF.\nFile saved at " + MyDir);
        }
    }
}

```
