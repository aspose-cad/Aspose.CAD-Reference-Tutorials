---
title: Decomposing CAD Insert Objects - Aspose.CAD Guide
linktitle: Decomposing CAD Insert Objects
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 11
url: /net/cad-layouts-and-decomposition/decomposing-cad-insert-objects/
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

namespace Aspose.CAD.Examples.CSharp.Export
{
	class DecomposeCADInsertObject
	{
		public static void Run()
		{

			//ExStart:DecomposeCADInsertObject

			string MyDir = RunExamples.GetDataDir_ConvertingCAD();
			string sourceFilePath = MyDir + "conic_pyramid.dxf";
			using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
			{

				for (int i = 0; i < cadImage.Entities.Length; i++)
				{
					if (cadImage.Entities[i].TypeName == CadEntityTypeName.INSERT)
					{
						CadBlockEntity block = cadImage.BlockEntities[(cadImage.Entities[i] as CadInsertObject).Name];

						foreach (CadBaseEntity baseEntity in block.Entities)
						{
							//  processing of entities
						}
					}
				}

				//ExEnd:DecomposeCADInsertObject
			}
		}
	}
}
```
