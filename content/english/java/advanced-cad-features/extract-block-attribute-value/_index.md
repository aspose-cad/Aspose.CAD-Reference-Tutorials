---
title: Extract Block Attribute Value from External Reference in Java
linktitle: Extract Block Attribute Value from External Reference in Java
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 19
url: /java/advanced-cad-features/extract-block-attribute-value/
---

## Complete Source Code
```java


import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadparameters.CadStringParameter;

public class GetBlockAttributeValueOfExternalReference {

	public static void main(String[] args) {
		// The path to the resource directory.
		String dataDir = "Your Document Directory" + "DWGDrawings/";
                //ExStart:GetBlockAttributeValueOfExternalReference
		// Load an existing DWG file as CadImage.
		CadImage cadImage = (CadImage) Image.load(dataDir + "sample.dwg");
		
		// Access the external path name property
		CadStringParameter sXternalRef = cadImage.getBlockEntities().get_Item("*MODEL_SPACE").getXRefPathName();
		System.out.println(sXternalRef);
                //ExEnd:GetBlockAttributeValueOfExternalReference
	}

}
```
