---
title: Adding Attributes to CAD Drawings - Aspose.CAD Tutorial
linktitle: Adding Attributes to CAD Drawings
second_title: Aspose.CAD .NET - CAD and BIM File Format
description: 
type: docs
weight: 10
url: /net/attribute-and-property-management/adding-attributes-to-cad-drawings/
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
	class AddAttribute
	{
		public static void Run()
		{
			//ExStart:AddAttribute
			// The path to the documents directory.
			string MyDir = "Your Document Directory";
			string sourceFilePath = MyDir + "conic_pyramid.dxf";
			List<CadBaseEntity> mtextList = new List<CadBaseEntity>();
			List<CadBaseEntity> attribList = new List<CadBaseEntity>();

			using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
			{
				foreach (var entity in cadImage.Entities)
				{
					if (entity.TypeName == CadEntityTypeName.MTEXT)
					{
						mtextList.Add(entity);
					}

					if (entity.TypeName == CadEntityTypeName.INSERT)
					{
						foreach (var childObject in entity.ChildObjects)
						{
							if (childObject.TypeName == CadEntityTypeName.ATTRIB)
							{
								attribList.Add(childObject);
							}
						}
					}
				}
                 
                Assert.AreEqual(6, mtextList.Count);
				Assert.AreEqual(34, attribList.Count);
			}
		}

	}

}
//ExEnd:AddAttribute
```
