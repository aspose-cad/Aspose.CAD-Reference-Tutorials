---
title: Rendering Colors in CAD Files - Aspose.CAD Guide
linktitle: Rendering Colors in CAD Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 10
url: /net/conversion-and-export/rendering-colors-in-cad-files/
---

## Complete Source Code
```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;

namespace Aspose.CAD.Examples.CSharp.DWG_Drawings
{
    class ColorRendering
    {
        public static void Run() {

            //ExStart:ColorRendering

            // The path to the documents directory.
            string MyDir = "Your Document Directory";
            string inputFile = MyDir + "test1.dwg";
            string outputFile = MyDir + "test1.png";
            using (FileStream fs = new FileStream(inputFile, FileMode.Open))
            {
                using (FileStream output = new FileStream(outputFile, FileMode.Create))
                {
                    Image document = Image.Load(fs);

                    PngOptions saveOptions = new PngOptions();

                    CadRasterizationOptions options = new CadRasterizationOptions();
                    options.NoScaling = false;
                    
                    options.PageHeight = document.Height * 10;
                    options.PageWidth = document.Width * 10;
                    options.DrawType = Aspose.CAD.FileFormats.Cad.CadDrawTypeMode.UseObjectColor;
                    saveOptions.VectorRasterizationOptions = options;

                    document.Save(output, saveOptions);
                }
            }

            //ExEnd:ColorRendering

        }
    }
}

```
