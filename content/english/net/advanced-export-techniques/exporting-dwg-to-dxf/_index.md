---
title: Exporting DWG to DXF Format in C# - Aspose.CAD Tutorial
linktitle: Exporting DWG to DXF Format in C# - Aspose.CAD Tutorial
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 10
url: /net/advanced-export-techniques/exporting-dwg-to-dxf/
---

## Complete Source Code
```csharp
using Aspose.CAD.FileFormats.Cad;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.CAD.Examples.CSharp.DWG_Drawings
{
    class DWGToDXF
    {
        public static void Run() {

            //ExStart:DWGToDXF
            string MyDir = RunExamples.GetDataDir_DWGDrawings();
            string inputFile = MyDir + "Line.dwg";
            string outFile = MyDir + "Line_19.2.dxf"; 
            using (var cadImage = (CadImage)Image.Load(inputFile))
            {
                cadImage.Save(outFile);
            }

            //ExEnd:DWGToDXF
        }
    }
}

```
