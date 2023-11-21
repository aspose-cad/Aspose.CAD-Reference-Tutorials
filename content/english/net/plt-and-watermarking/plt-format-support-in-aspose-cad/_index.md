---
title: PLT Format Support in Aspose.CAD - Tutorial
linktitle: PLT Format Support in Aspose.CAD - Tutorial
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 10
url: /net/plt-and-watermarking/plt-format-support-in-aspose-cad/
---

## Complete Source Code
```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.CAD.Examples.CSharp.Export
{
	class PLTSupport
	{
		//ExStart:PLTSupport
		public static void Run()
		{

			string MyDir = RunExamples.GetDataDir_ConvertingCAD();
			string sourceFilePath = MyDir + "themepark.plt";
			Image image = Image.Load((sourceFilePath));
			ImageOptionsBase imageOptions = new JpegOptions();
			CadRasterizationOptions options = new CadRasterizationOptions
			{
				PageHeight = 500,
				PageWidth = 1000,
				
			};
			imageOptions.VectorRasterizationOptions = options;
			image.Save((MyDir+"themepark.jpg"), imageOptions);
            }
	       }
         //ExEnd:PLTSupport
}
		

```
