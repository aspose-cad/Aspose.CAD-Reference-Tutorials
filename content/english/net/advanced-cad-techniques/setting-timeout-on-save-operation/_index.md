---
title: Setting Timeout on Save Operation - Aspose.CAD Tutorial
linktitle: Setting Timeout on Save Operation
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 12
url: /net/advanced-cad-techniques/setting-timeout-on-save-operation/
---

## Complete Source Code
```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Threading;
using System.Threading.Tasks;

namespace Aspose.CAD.Examples.CSharp.Features
{
    class PutTimeoutOnSave
    {
        public static void Run() 
        {
            //ExStart:1
            string SourceDir = "Your Document Directory";
            string OutputDir = "Your Document Directory";

            using (Image cadDrawing = Image.Load(SourceDir + "Drawing11.dwg"))
            {
                var rasterizationOptions = new CadRasterizationOptions();

                rasterizationOptions.PageWidth = cadDrawing.Size.Width;
                rasterizationOptions.PageHeight = cadDrawing.Size.Height;

                using (var its = new InterruptionTokenSource())
                {
                    PdfOptions CADf = new PdfOptions();
                    CADf.VectorRasterizationOptions = rasterizationOptions;
                    CADf.InterruptionToken = its.Token;

                    var exportTask = Task.Factory.StartNew(() =>
                    {
                        cadDrawing.Save(OutputDir + "PutTimeoutOnSave_out.pdf", CADf);
                    });

                    Thread.Sleep(10000);
                    its.Interrupt();

                    exportTask.Wait();
                }
            }
            //ExEnd:1
            Console.WriteLine("PutTimeoutOnSave executed successfully");
        }
    }
}

```
