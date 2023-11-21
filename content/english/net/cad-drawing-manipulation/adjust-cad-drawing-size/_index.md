---
title: Adjusting CAD Drawing Size in Aspose.CAD for .NET
linktitle: Adjusting CAD Drawing Size
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 10
url: /net/cad-drawing-manipulation/adjust-cad-drawing-size/
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
    public class AdjustingCADDrawingSize
    {
        public static void Run()
        {
            //ExStart:AdjustingCADDrawingSize

            // The path to the documents directory.
            string MyDir = "Your Document Directory";

            string sourceFilePath = MyDir + "sample.dwg";
            
            // Load a CAD drawing in an instance of Image
            using (var image = Aspose.CAD.Image.Load(sourceFilePath))
            {
                // Create an instance of BmpOptions class
                Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();

                // Create an instance of CadRasterizationOptions and set its various properties
                Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
                bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
                
                // Set the UnitType property
                cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimenter;

                // Set the layouts property
                cadRasterizationOptions.Layouts = new string[] { "Model" };

                //Export layout to BMP format
                string outPath = sourceFilePath + ".bmp";
                image.Save(outPath, bmpOptions);
            }

          
        }

        public static void AutoAdjustingCADDrawingSize()
        {
         

            // The path to the documents directory.
            string MyDir = "Your Document Directory";

            string sourceFilePath = MyDir + "sample.dwg";

            // Load a CAD drawing in an instance of Image
            using (var image = Aspose.CAD.Image.Load(sourceFilePath))
            {
                // Create an instance of BmpOptions class
                Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();

                // Create an instance of CadRasterizationOptions and set its various properties
                Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
                bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
                                            
                // Set the layouts property
                cadRasterizationOptions.Layouts = new string[] { "Model" };

                //Export layout to BMP format
                string outPath = sourceFilePath + ".bmp";
                image.Save(outPath, bmpOptions);
            }

            //ExEnd:AutoAdjustingCADDrawingSize
            
        }

    }
}

```
