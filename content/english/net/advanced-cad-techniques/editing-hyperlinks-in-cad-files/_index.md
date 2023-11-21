---
title: Editing Hyperlinks in CAD Files - Aspose.CAD Tutorial
linktitle: Editing Hyperlinks in CAD Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 14
url: /net/advanced-cad-techniques/editing-hyperlinks-in-cad-files/
---

## Complete Source Code
```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.CAD.Examples.CSharp.Hyperlinks
{
    class EditHyperlink
    {

        public static void Run() {

            //ExStart:EditHyperlink


            // The path to the documents directory.
            string MyDir = RunExamples.GetDataDir_DWGDrawings();
            string dwgPathToFile = MyDir + "AutoCad_Sample.dwg";

            using (CadImage cadImage = (CadImage)Image.Load(dwgPathToFile))
            {
                foreach (CadBaseEntity entity in cadImage.Entities)
                {
                    if (entity is CadInsertObject)
                    {
                        CadBlockEntity block = cadImage.BlockEntities[((CadInsertObject)entity).Name];
                        if (!string.IsNullOrEmpty(block.XRefPathName.Value))
                        {
                            block.XRefPathName.Value = "new file reference.dwg";
                        }
                    }

                    if (entity.Hyperlink == "https://products.aspose.com")
                    {
                        entity.Hyperlink = "https://www.aspose.com";
                    }
                }
            }

            //ExEnd:EditHyperlink

        }
    }
}

```
