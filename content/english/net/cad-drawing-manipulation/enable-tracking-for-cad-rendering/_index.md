---
title: Enable Tracking for CAD Rendering in Aspose.CAD for .NET
linktitle: Enable Tracking for CAD Rendering
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 13
url: /net/cad-drawing-manipulation/enable-tracking-for-cad-rendering/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using System.IO;
namespace Aspose.CAD.Examples.CSharp.ConvertingCAD
{
    public class EnableTrackingForCADRendering
    {
        public static void Run()
        {
            //ExStart:EnableTrackingForCADRendering
            // The path to the documents directory.
            string MyDir = RunExamples.GetDataDir_ConvertingCAD();
            string sourceFilePath = MyDir + "conic_pyramid.dxf";
            using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
            {
                MemoryStream stream = new MemoryStream();
                Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
                // Create an instance of CadRasterizationOptions and set its various properties
                Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
                pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
                cadRasterizationOptions.PageWidth = 800;
                cadRasterizationOptions.PageHeight = 600;               

                image.Save(stream, pdfOptions);
            }
            //ExEnd:EnableTrackingForCADRendering            
            Console.WriteLine("\nTracking enabled successfully for CAD rendering process.");

        }
    }
}



```
