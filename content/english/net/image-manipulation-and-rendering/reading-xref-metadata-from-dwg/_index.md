---
title: Reading XREF Metadata from DWG Files - Aspose.CAD Tutorial
linktitle: Reading XREF Metadata from DWG Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 16
url: /net/image-manipulation-and-rendering/reading-xref-metadata-from-dwg/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;

namespace Aspose.CAD.Examples.CSharp.DWG_Drawings
{
    public class ReadXREEFMetaData
    {
        public static void Run()
        {
            //ExStart:ReadXREEFMetaData
            // The path to the documents directory.
            string MyDir = "Your Document Directory";
            string sourceFilePath = MyDir + "Bottom_plate.dwg";
            using (CadImage image = (CadImage)Image.Load(sourceFilePath))
            {
                foreach (CadBaseEntity entity in image.Entities)
                {
                    if (entity is CadUnderlay)
                    {
                        //XREF entity with metadata
                        Cad3DPoint insertionPoint = ((CadUnderlay)entity).InsertionPoint;
                        string path = ((CadUnderlay)entity).UnderlayPath;
                    }
                }
            }
            //ExEnd:ReadXREEFMetaData            
            Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);

        }
    }
}

```
