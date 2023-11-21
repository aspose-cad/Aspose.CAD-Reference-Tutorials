---
title: Exporting OLE Objects from DWG Files - Aspose.CAD Tutorial
linktitle: Exporting OLE Objects from DWG Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 12
url: /net/advanced-export-techniques/exporting-ole-objects-from-dwg/
---

## Complete Source Code
```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.CAD.Examples.CSharp.DWG_Drawings
{
    class ExportOLEObjects
    {
        public static void Run() {

            //ExStart:ExportOLEObjects

            // The path to the documents directory.
            string MyDir = "Your Document Directory";

            string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };

            PngOptions pngOptions = new PngOptions { };
            CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
            pngOptions.VectorRasterizationOptions = rasterizationOptions;
            rasterizationOptions.Layouts = new string[] { "Layout1" };

            foreach (string file in files)
            {
                using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
                {
                    cadImage.Save(MyDir + file + "_out.png", pngOptions);
                }
            }
            //ExEnd:ExportOLEObjects

        }
    }
}

```
