---
title: Metered Licensing in Aspose.CAD for .NET
linktitle: Metered Licensing in Aspose.CAD for .NET
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 12
url: /net/licensing-and-configuration/metered-licensing/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.CAD.Examples.CSharp.ApplyLicense
{
    class MeteredLicensing
    {

        public static void Run()
        {
            //ExStart:MeteredLicensing


            // Access the setMeteredKey property and pass public and private keys as parameters
            Aspose.CAD.Metered.SetMeteredKey("PublicKey", "PrivateKey");


            // Get metered data amount before calling API
            decimal amountbefore = Aspose.CAD.Metered.GetConsumptionQuantity();

            // Display information
            Console.WriteLine("Amount Consumed Before: " + amountbefore.ToString());
            
            
            // Do processing
            //Aspose.CAD.FileFormats.Cad.CadImage image = (Aspose.CAD.FileFormats.Cad.CadImage)Aspose.CAD.Image.load("BlockRefDgn.dwg");

            
            // Get metered data amount After calling API
            decimal amountafter = Aspose.CAD.Metered.GetConsumptionQuantity();

            // Display information
            Console.WriteLine("Amount Consumed After: " + amountafter.ToString());

            //ExEnd:MeteredLicensing
        }

    }
}

```
