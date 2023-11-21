---
title: Working with ACAD Proxy Entities - Aspose.CAD Guide
linktitle: Working with ACAD Proxy Entities - Aspose.CAD Guide
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 13
url: /net/layout-and-object-handling/working-with-acad-proxy-entities/
---

## Complete Source Code
```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.CAD.Examples.CSharp.Export
{
	class ACADProxyEntities
	{
		public static void Run()
		{

			//ExStart:ACADProxyEntities
			string MyDir = RunExamples.GetDataDir_ConvertingCAD();
			string sourceFilePath = MyDir + "conic_pyramid.dxf";

			using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
			{
				CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
				rasterizationOptions.UnitType = UnitType.Inch;
				rasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
				rasterizationOptions.BackgroundColor = Color.Black;
				rasterizationOptions.Layouts = new string[] { "Model" };
				PdfOptions pdfOptions = new PdfOptions
				{
					VectorRasterizationOptions = rasterizationOptions
				};
				cadImage.Save(MyDir+"output.pdf", pdfOptions);
			}
			//ExEnd:ACADProxyEntities
		}
	}
}

```
