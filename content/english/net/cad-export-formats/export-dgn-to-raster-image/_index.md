---
title: Export DGN to Raster Image in Aspose.CAD for .NET
linktitle: Export DGN to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 13
url: /net/cad-export-formats/export-dgn-to-raster-image/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;

namespace Aspose.CAD.Examples.CSharp.Exporting_DGN
{
    public class ExportDGNToRasterImage
    {
        public static void Run()
        {
            try
            {
                //ExStart:ExportDGNToRasterImage
                // The path to the documents directory.
                string MyDir = "Your Document Directory";
                string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
                // Load an existing DGN file as CadImage.
                using (Aspose.CAD.FileFormats.Cad.CadImage cadImage = (Aspose.CAD.FileFormats.Cad.CadImage)Aspose.CAD.Image.Load(sourceFilePath))
                {
                    // Create an object of DgnRasterizationOptions class and define/set different properties
                    Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
                    rasterizationOptions.PageWidth = 600;
                    rasterizationOptions.PageHeight = 300;
                    
                    rasterizationOptions.NoScaling = true;
                    rasterizationOptions.AutomaticLayoutsScaling = false;

                    // Create an object of JpegOptions class as we are converting the DGN to jpeg and assign DgnRasterizationOptions object to it.
                    Aspose.CAD.ImageOptionsBase options = new Aspose.CAD.ImageOptions.JpegOptions();
                    options.VectorRasterizationOptions = rasterizationOptions;

                    // Call the save method of the CadImage class object.
                    cadImage.Save(MyDir + "ExportDGNToRasterImage_out.pdf", options);
                }
                //ExEnd:ExportDGNToRasterImage            
                Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
            }
            catch (Exception ex)
            {
                Console.WriteLine("Please use valid input file." + ex.Message);
            }

        }
    }
}

```
