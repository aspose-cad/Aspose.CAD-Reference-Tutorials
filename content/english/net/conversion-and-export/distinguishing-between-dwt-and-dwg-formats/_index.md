---
title: Distinguishing Between DWT and DWG Formats - Aspose.CAD Guide
linktitle: Distinguishing Between DWT and DWG Formats - Aspose.CAD Guide
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 12
url: /net/conversion-and-export/distinguishing-between-dwt-and-dwg-formats/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.CAD.Examples.CSharp.DWG_Drawings
{
    class DistinguishDWTAndDWGFormats
    {
        public static void Run() {
            //ExStart:DistinguishDWTAndDWGFormats
            var formatTypeDwt = Image.GetFileFormat(GetFileFromDesktop("sample.dwt"));
            Assert.IsTrue(formatTypeDwt.ToString().ToLower().Contains("dwt"));
            var formatTypeDwg = Image.GetFileFormat(GetFileFromDesktop("sample.dwg"));
            Assert.IsTrue(formatTypeDwg.ToString().ToLower().Contains("dwg"));

            //ExEnd:DistinguishDWTAndDWGFormats
        }
    }
}

```
