---
title: Substitute Font of a Particular Style in DWG
linktitle: Substitute Font of a Particular Style in DWG
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 12
url: /java/cad-text-and-annotation/substitute-font-of-particular-style-in-dwg/
---

## Complete Source Code
```java


import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;

public class SubstituteFontOfAParticularStyle {

	public static void main(String[] args) {
		
		// The path to the resource directory.
		String dataDir = "Your Document Directory" + "CADConversion/";
		//ExStart:SubstituteFontOfAParticularStyle
                String srcFile = dataDir + "conic_pyramid.dxf";
		
		// Load a CAD drawing in an instance of CadImage
		CadImage cadImage = (CadImage)Image.load(srcFile);
		
		// Specify the font for one particular style
                 
                ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)cadImage.getStyles().get_Item(0)).setPrimaryFontName("Arial");
	//ExEnd:SubstituteFontOfAParticularStyle
        
        }
}

```
