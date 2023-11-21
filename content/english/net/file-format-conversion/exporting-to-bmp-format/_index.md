---
title: Exporting to BMP Format - Aspose.CAD Tutorial
linktitle: Exporting to BMP Format
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 11
url: /net/file-format-conversion/exporting-to-bmp-format/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
namespace Aspose.CAD.Examples.CSharp.Export
{
    public class ExportToBMP
    {
        public static void Run()
        {
            //ExStart:ExportToBMP
            // The path to the documents directory.
            string MyDir = RunExamples.GetDataDir_ConvertingCAD();


            string inputFile = MyDir + "18-12-11 9644 - site.dwf";
            using (Image image = Image.Load(inputFile))
            {
                BmpOptions bmpOptions = new BmpOptions();
                var dwfRasterizationOptions = new CadRasterizationOptions();
                bmpOptions.VectorRasterizationOptions = dwfRasterizationOptions;
                
                dwfRasterizationOptions.PageHeight = 500;
                dwfRasterizationOptions.PageWidth = 500;
                
                // export
                string outPath = MyDir + "18-12-11 9644 - site.bmp";
                image.Save(outPath, bmpOptions);
            }
            
            
            //ExEnd:ExportToBMP           
            Console.WriteLine("\n3D images exported successfully to BMP.\nFile saved at " + MyDir);
        }
    }
}

```
