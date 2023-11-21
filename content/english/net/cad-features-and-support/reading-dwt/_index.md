---
title: Reading DWT in Aspose.CAD for .NET
linktitle: Reading DWT
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 13
url: /net/cad-features-and-support/reading-dwt/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;

namespace Aspose.CAD.Examples.CSharp.ConvertingCAD
{
    public class ReadingDWT
    {
        public static void Run()
        {
            //ExStart:ReadingDWT
            // The path to the documents directory.
            string MyDir = "Your Document Directory";
            using (CadImage image = (CadImage)Image.Load(MyDir+"example.dwt"))
          {
           foreach (CadBaseEntity entity in image.Entities)
         {
         //do your work here
          }
          }
            }
            //ExEnd:ReadingDWT
        }
    }


```
