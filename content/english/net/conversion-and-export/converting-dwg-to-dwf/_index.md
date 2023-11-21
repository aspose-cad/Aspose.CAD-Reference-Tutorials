---
title: Converting DWG to DWF Format - Aspose.CAD Guide
linktitle: Converting DWG to DWF Format - Aspose.CAD Guide
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 14
url: /net/conversion-and-export/converting-dwg-to-dwf/
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
    class DWGToDWF
    {
        public static void Run()
        {
            //ExStart:DWGToDWF
            string MyDir = RunExamples.GetDataDir_DWGDrawings();

            string inputFile = MyDir + "Line.dwg";
            string outFile = MyDir + "Line_20.1.dwf";
            using (var cadImage = (CadImage)Image.Load(inputFile))
            {
                cadImage.Save(outFile);
            }


            //ExEnd:DWGToDWF
        }

    }
}

```
