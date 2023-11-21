---
title: Exporting CAD Drawings to SVG Format - Aspose.CAD Guide
linktitle: Exporting CAD Drawings to SVG Format
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 15
url: /net/advanced-export-techniques/exporting-cad-drawings-to-svg/
---

## Complete Source Code
```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.CAD.Examples.CSharp.DWG_Drawings
{
    class ExportToSVG
    {

        public static void Run() {

            //ExStart:ExportToSVG
            // The path to the documents directory.
            string MyDir = "Your Document Directory";

            using (Image image = Image.Load(MyDir + "sample.dwg"))
            {
                var options = new SvgOptions();
                options.ColorType = Aspose.CAD.ImageOptions.SvgOptionsParameters.SvgColorMode.Grayscale;
                options.TextAsShapes = true;
                image.Save(MyDir + "sample.svg");
            }
            //ExEnd:ExportToSVG
        }
    }
}

```
