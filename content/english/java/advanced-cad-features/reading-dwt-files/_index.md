---
title: Reading DWT Files
linktitle: Reading DWT Files
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 14
url: /java/advanced-cad-features/reading-dwt-files/
---

## Complete Source Code
```java


import java.awt.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.acadtable.CadTableEntity;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;

public class ReadingDWT {

	public static void main(String[] args) {
		
		// The path to the resource directory.
                 
		String dataDir = "Your Document Directory" + "CADConversion/";
		String srcFile = dataDir + "conic_pyramid.dxf";
		
		// Load a CAD drawing  in an instance of CadImage
		//CadImage cadImage = (CadImage) Image.load(srcFile);
               com.aspose.cad.fileformats.cad.CadImage objImage =(CadImage) com.aspose.cad.Image.load(srcFile);
                       
                for(Object style : objImage.getStyles())
                {
                    // Set the font name
                    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
                }

                
	}
}

```
