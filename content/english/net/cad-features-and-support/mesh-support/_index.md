---
title: Mesh Support in Aspose.CAD for .NET
linktitle: Mesh Support
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 11
url: /net/cad-features-and-support/mesh-support/
---

## Complete Source Code
```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.CAD.Examples.CSharp.ConvertingCAD
{
	class MeshSupport
	{
		public static void Run()
		{

			//ExStart:MeshSupport
			string MyDir = RunExamples.GetDataDir_DWGDrawings();
		
			string sourceFilePath = MyDir+("meshes.dwg");
			string outPath = MyDir+("meshes.pdf");

			using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
			{
				CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
				rasterizationOptions.PageWidth = 1600;
				rasterizationOptions.PageHeight = 1600;
				//rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;
				rasterizationOptions.Layouts = new string[] { "Model" };
				PdfOptions pdfOptions = new PdfOptions
				{
					VectorRasterizationOptions = rasterizationOptions
				};

				{
					cadImage.Save(outPath, pdfOptions);
				}

			}
			//ExEnd:MeshSupport
		}
	}
}
```
