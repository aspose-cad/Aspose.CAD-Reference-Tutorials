---
title: Substitute Font in DWG
linktitle: Substitute Font in DWG
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 11
url: /java/cad-text-and-annotation/substitute-font-in-dwg/
---

## Complete Source Code
```java


import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;

public class SubstituteFont {

	public static void main(String[] args) {
		
		// The path to the resource directory.
		String dataDir = "Your Document Directory" + "CADConversion/";
		
                String srcFile = dataDir + "conic_pyramid.dxf";
		
		// Load a CAD drawing  in an instance of CadImage
		CadImage cadImage = (CadImage) Image.load(srcFile);

		// Iterate over the items of CadStylesDictionary
		for(Object style : cadImage.getStyles())
                {
                    // Set the font name
                    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
                }

                
	}
}

```
