---
title: Substituting Fonts in Aspose.CAD for .NET
linktitle: Substituting Fonts
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 17
url: /net/cad-features-and-support/substituting-fonts/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadTables;

namespace Aspose.CAD.Examples.CSharp.ConvertingCAD
{
    public class SubstitutingFonts
    {
        public static void Run()
        {
            //ExStart:SubstitutingFonts
            // The path to the documents directory.
            string MyDir = "Your Document Directory";
            string sourceFilePath = MyDir + "conic_pyramid.dxf";
            // Load a CAD drawing  in an instance of CadImage
            using (Aspose.CAD.FileFormats.Cad.CadImage cadImage = (Aspose.CAD.FileFormats.Cad.CadImage)Aspose.CAD.Image.Load(sourceFilePath))
            {
                // Iterate over the items of CadStyleDictionary
                foreach (CadStyleTableObject style in cadImage.Styles)
                {
                    // Set the font name
                    style.PrimaryFontName = "Arial";
                }
            }            
                    
            Console.WriteLine("\nFont changed successfully.");
        }
        public static void SubstitutingFontByName()
        {
            //ExStart:SubstitutingFontByName
            // The path to the documents directory.
            string MyDir = "Your Document Directory";
            string sourceFilePath = MyDir + "conic_pyramid.dxf";
            // Load a CAD drawing in an instance of CadImage
            using (Aspose.CAD.FileFormats.Cad.CadImage cadImage = (Aspose.CAD.FileFormats.Cad.CadImage)Aspose.CAD.Image.Load(sourceFilePath))
            {
                // Iterate over the items of CadStyleDictionary
                foreach (CadStyleTableObject style in cadImage.Styles)
                {
                    if (style.StyleName == "Roman")
                    {
                        // Specify the font for one particular style
                        style.PrimaryFontName = "Arial";
                    }
                }
            }
       
        }

        //ExEnd:SubstitutingFonts 
    }
}

```
