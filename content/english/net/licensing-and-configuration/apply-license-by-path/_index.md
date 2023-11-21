---
title: Apply License by Path in Aspose.CAD for .NET
linktitle: Apply License by Path
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 10
url: /net/licensing-and-configuration/apply-license-by-path/
---

## Complete Source Code
```csharp
using Aspose.CAD;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.CAD.Examples.CSharp.ApplyLicense
{
    public class ApplyLicenseByPath
    {
        public static void Run() 
        {
            //ExStart:ApplyLicenseByPath
            // Set path of the license file, i.e. c:\temp\
            string dataDir = @"c:\temp\";

            License license = new License();
            license.SetLicense(dataDir + "Aspose.CAD.lic");
            //ExEnd:ApplyLicenseByPath
        }
    }
}

```
