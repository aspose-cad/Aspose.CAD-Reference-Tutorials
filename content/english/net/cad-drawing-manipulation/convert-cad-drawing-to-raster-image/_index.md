---
title: Convert CAD Drawing to Raster Image in Aspose.CAD for .NET
linktitle: Convert CAD Drawing to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 11
url: /net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
namespace Aspose.CAD.Examples.CSharp.ConvertingCAD
{
    public class ConvertDrawingToRasterImage
    {
        public static void Run()
        {
            //ExStart:ConvertDrawingToRasterImage
            // The path to the documents directory.
            string MyDir = "Your Document Directory";
            string sourceFilePath = MyDir + "conic_pyramid.dxf";
            using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
            {
                // Create an instance of CadRasterizationOptions
                Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
                // Set page width & height
                rasterizationOptions.PageWidth = 1200;
                rasterizationOptions.PageHeight = 1200;

                // Create an instance of PngOptions for the resultant image
                ImageOptionsBase options = new Aspose.CAD.ImageOptions.PngOptions();
                // Set rasterization options
                options.VectorRasterizationOptions = rasterizationOptions;

                MyDir = MyDir + "conic_pyramid_raster_image_out.png";
                // Save resultant image
                image.Save(MyDir, options);                
            }
            //ExEnd:ConvertDrawingToRasterImage            
            Console.WriteLine("\nCAD drawing converted successfully to raster image format.\nFile saved at " + MyDir);

        }
    }
}

```
