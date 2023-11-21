---
title: Getting Block Attributes from DWG Files - Aspose.CAD Tutorial
linktitle: Getting Block Attributes from DWG Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 10
url: /net/image-manipulation-and-rendering/getting-block-attributes-from-dwg/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
namespace Aspose.CAD.Examples.CSharp.DWG_Drawings
{
    public class GetBlockAttributeValue
    {
        public static void Run()
        {
            //ExStart:GetBlockAttributeValue
            // The path to the documents directory.
            string MyDir = "Your Document Directory";
            string sourceFilePath = MyDir + "sample.dwg";
            // Load an existing DWG file as CadImage.
            using (Aspose.CAD.FileFormats.Cad.CadImage cadImage = (Aspose.CAD.FileFormats.Cad.CadImage)Aspose.CAD.Image.Load(sourceFilePath))
            {
                System.Console.WriteLine(cadImage.BlockEntities["*MODEL_SPACE"].XRefPathName);
            }
            //ExEnd:GetBlockAttributeValue  
        }
    }
}

```
