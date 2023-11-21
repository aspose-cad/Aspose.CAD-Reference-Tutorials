---
title: Exporting DXF Specific Layer to PDF - Aspose.CAD Tutorial
linktitle: Exporting DXF Specific Layer to PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 10
url: /net/export-techniques/exporting-dxf-specific-layer-to-pdf/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
namespace Aspose.CAD.Examples.CSharp.DXF_Drawings
{
    public class ExportDXFSpecificLayerToPDF
    {
        public static void Run()
        {
            //ExStart:ExportDXFSpecificLayerToPDF
            // The path to the documents directory.
            string MyDir = "Your Document Directory";
            string sourceFilePath = MyDir + "conic_pyramid.dxf";
            using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
            {
                //  Create an instance of CadRasterizationOptions and set its various properties
                Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
                rasterizationOptions.PageWidth = 1600;
                rasterizationOptions.PageHeight = 1600;
                // Add desired layers
                rasterizationOptions.Layers = new string[] { "LayerA" };
				// Create an instance of PdfOptions
				Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
                // Set the VectorRasterizationOptions property
                pdfOptions.VectorRasterizationOptions = rasterizationOptions;

                MyDir = MyDir + "conic_pyramid_layer_out.pdf";
                //Export the DXF to PDF
                image.Save(MyDir, pdfOptions);                
            }
            //ExEnd:ExportDXFSpecificLayerToPDF            
            Console.WriteLine("\nThe DXF file with specific layer exported successfully to PDF.\nFile saved at " + MyDir);

        }
    }
}

```
