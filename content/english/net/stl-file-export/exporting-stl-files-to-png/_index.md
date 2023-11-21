---
title: Exporting STL Files to PNG - Aspose.CAD Tutorial
linktitle: Exporting STL Files to PNG
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 10
url: /net/stl-file-export/exporting-stl-files-to-png/
---

## Complete Source Code
```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.CAD.Examples.CSharp.STL_Drawings
{
    class ExportingSTLtoPNG
    {
        public static void Run() 
        {
           //ExStart:ExportingSTLtoPNG
            string MyDir = "Your Document Directory";
            string sourceFilePath = MyDir + "galeon.stl";
            using (var cadImage = (CadImage)Image.Load(sourceFilePath))
            {
                var rasterizationOptions = new CadRasterizationOptions();
                
                rasterizationOptions.PageWidth = 100;
                rasterizationOptions.PageHeight = 100;

                PngOptions pngOptions = new PngOptions();
                pngOptions.VectorRasterizationOptions = rasterizationOptions;
               
                string outPath = sourceFilePath + ".png";
                cadImage.Save(outPath, pngOptions);
            }
        }
              //ExEnd:ExportingSTLtoPNG
    }
}

```
