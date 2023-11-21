---
title: Exporting PLT Files to Image - Aspose.CAD Tutorial
linktitle: Exporting PLT Files to Image - Aspose.CAD Tutorial
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 10
url: /net/exporting-plt-files/exporting-plt-files-to-image/
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

namespace Aspose.CAD.Examples.CSharp.PLT_Drawings
{
    class ExportPLTtoImage
    {
        public static void Run()
        {
            //ExStart:ExportPLTtoImage
            // The path to the documents directory.
            string MyDir = RunExamples.GetDataDir_PLTDrawings();
            string sourceFilePath = MyDir + "50states.plt";
           
            using (Image cadImage = Image.Load(sourceFilePath))
            {
                ImageOptionsBase imageOptions = new JpegOptions();
                CadRasterizationOptions options = new CadRasterizationOptions
                {
                    PageHeight = 500,
                    PageWidth = 1000,
                    
                };
                imageOptions.VectorRasterizationOptions = options;
                cadImage.Save(MyDir+ "50states.jpg", imageOptions);
            }
            //ExEnd:ExportPLTtoImage
        }

            
            }
    
}

  

```
