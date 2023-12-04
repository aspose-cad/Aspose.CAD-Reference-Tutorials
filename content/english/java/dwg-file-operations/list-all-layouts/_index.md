---
title: List All Layouts in AutoCAD Drawing with Java
linktitle: List All Layouts in AutoCAD Drawing with Java
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 11
url: /java/dwg-file-operations/list-all-layouts/
---

## Complete Source Code
```java

import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadLayoutDictionary;
import com.aspose.cad.fileformats.cad.cadobjects.CadLayout;

public class ListAllLayoutsInAnAutoCADDrawing {

	public static void main(String[] args) {
		
		// The path to the resource directory.
            String dataDir = "Your Document Directory" + "DWGDrawings/";
            
            String srcFile = dataDir + "conic_pyramid.dxf";

            Image image = Image.load(srcFile);
		
	    CadImage cadImage = (CadImage)image;

	    CadLayoutDictionary layouts = cadImage.getLayouts();
	    for (CadLayout layout : layouts.getValues())
            {
	        System.out.println("Layout " + layout.getLayoutName());
	    }
            
            
	}

}

```
