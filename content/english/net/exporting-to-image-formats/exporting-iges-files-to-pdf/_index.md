---
title: Exporting IGES Files to PDF - Aspose.CAD Guide
linktitle: Exporting IGES Files to PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 11
url: /net/exporting-to-image-formats/exporting-iges-files-to-pdf/
---

## Complete Source Code
```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using static Aspose.CAD.Examples.CSharp.DWG_Drawings.SupportMLeaderEntityForDWGFormat;
using Aspose.CAD.ImageOptions;

namespace Aspose.CAD.Examples.CSharp.IGES_Drawings
{
    class ExportIGEStoPDF
    {
        public static void Run()
        {
            //ExStart:ExportIGEStoPDF
            // The path to the documents directory.
            string MyDir = "Your Document Directory";
            string sourceFilePath = MyDir + "figa2.igs";
           
            using (Image cadImage = Image.Load(sourceFilePath))
            {

                CadRasterizationOptions options = new CadRasterizationOptions
                {
                    PageHeight = 1000,
                    PageWidth = 1000,
                    
                };

                PdfOptions pdfOptions = new PdfOptions();
                pdfOptions.VectorRasterizationOptions = options;

                cadImage.Save(MyDir+ "figa2.pdf", pdfOptions);
            }
            //ExEnd:ExportIGEStoPDF
        }


    }
    
}

    



```
