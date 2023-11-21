---
title: Adding Custom Properties to DWG Files - Aspose.CAD Guide
linktitle: Adding Custom Properties to DWG Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 11
url: /net/attribute-and-property-management/adding-custom-properties-to-dwg/
---

## Complete Source Code
```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using static Aspose.CAD.Examples.CSharp.DWG_Drawings.SupportMLeaderEntityForDWGFormat;

namespace Aspose.CAD.Examples.CSharp.DXF_Drawings
{
	class AddCustomProperties
	{
		public static void Run()
		{
			//ExStart:1
			// The path to the documents directory.
			string WorkingDir = RunExamples.GetDataDir_DXFDrawings();

			string fileName = "conic_pyramid.dxf";
			string inputFile = WorkingDir + fileName;
			string outFile = WorkingDir + "AddMetadata_out.dxf";
			using (var cadImage = (CadImage)Image.Load(inputFile))
			{
				cadImage.Header.CustomProperties.Add("CUSTOM_PROPERTY_1", "Custom property test 1");
				cadImage.Header.CustomProperties.Add("CUSTOM_PROPERTY_2", "Custom property test 2");
				cadImage.Header.CustomProperties.Add("CUSTOM_PROPERTY_3", "Custom property test 3");

				cadImage.Save(outFile);
			}
			//ExEnd:1
			Console.WriteLine("\nAddCustomProperties executed successfully.\nFile saved at " + WorkingDir);
		}

	}

}
```
