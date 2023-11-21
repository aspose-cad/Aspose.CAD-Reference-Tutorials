---
title: Apply License using FileStream in Aspose.CAD for .NET
linktitle: Apply License using FileStream
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 11
url: /net/licensing-and-configuration/apply-license-using-filestream/
---

## Complete Source Code
```csharp
using Aspose.CAD;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;

namespace Aspose.CAD.Examples.CSharp.ApplyLicense
{
    public class ApplyLicenseUsingFileStream
    {
        public static void Run()
        {
            //ExStart:ApplyLicenseUsingFileStream
            // Set path of the license file, i.e. c:\temp\
            string dataDir = @"c:\temp\";
            // Load an existing file in the stream
            FileStream LicStream = new FileStream(dataDir + "Aspose.CAD.lic", FileMode.Open);

            License license = new License();
            license.SetLicense(LicStream);
            //ExEnd:ApplyLicenseUsingFileStream
        }

    }
}

```
