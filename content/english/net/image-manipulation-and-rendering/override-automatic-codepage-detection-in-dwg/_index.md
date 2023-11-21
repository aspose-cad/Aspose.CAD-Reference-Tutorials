---
title: Override Automatic Codepage Detection in DWG Files - Aspose.CAD Tutorial
linktitle: Override Automatic Codepage Detection in DWG Files - Aspose.CAD Tutorial
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 14
url: /net/image-manipulation-and-rendering/override-automatic-codepage-detection-in-dwg/
---

## Complete Source Code
```csharp
using System;
using Aspose.CAD.FileFormats.Cad;
namespace Aspose.CAD.Examples.CSharp.DWG_Drawings
{
    class OverrideAutomaticCodePageDetectionDwg
    {
        public static void Run()
        {
            //ExStart:1
            string SourceDir = RunExamples.GetDataDir_DWGDrawings();
            using (CadImage cadImage = (CadImage)Image.Load(SourceDir + "SimpleEntites.dwg",
            new LoadOptions()
            {
                SpecifiedEncoding = CodePages.Japanese,
                SpecifiedMifEncoding = MifCodePages.Japanese,
                RecoverMalformedCifMif = false
            }))
            {
                //do export or something else with cadImage
            }
            //ExEnd:1
            Console.WriteLine("OverrideAutomaticCodePageDetectionDwg executed successfully");
        }
    }
}

```
