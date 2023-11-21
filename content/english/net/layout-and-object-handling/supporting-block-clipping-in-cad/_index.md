---
title: Supporting Block Clipping in CAD - Aspose.CAD Tutorial
linktitle: Supporting Block Clipping in CAD
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 12
url: /net/layout-and-object-handling/supporting-block-clipping-in-cad/
---

## Complete Source Code
```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.CAD.Examples.CSharp.DXF_Drawings
{
    class SupportOfBlockClipping
    {
        public static void Run()
        {
            //ExStart:SupportOfBlockClipping
            // The path to the documents directory.
            string MyDir = "Your Document Directory";

            string inputFile = MyDir + "SLS-CW-CD-CE001-R01_blockClip.dxf";
            string outputFile = MyDir + "SLS-CW-CD-CE001-R01_blockClip.pdf";

            using (CadImage cadImage = (CadImage)Image.Load(inputFile))
            {
                var rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions
                {
                    BackgroundColor = Aspose.CAD.Color.White,
                    DrawType = Aspose.CAD.FileFormats.Cad.CadDrawTypeMode.UseObjectColor,
                    PageWidth = 1200,
                    PageHeight = 1600,
                    Margins = new Margins
                    {
                        Top = 5,
                        Right = 30,
                        Bottom = 5,
                        Left = 30
                    },
                    
                    Layouts = new string[] { "Model" }
                };

                PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions
                {
                    VectorRasterizationOptions = rasterizationOptions
                };

                cadImage.Save(outputFile, pdfOptions);
                //ExEnd:SupportOfBlockClipping

            }
        }
    }
}

```
