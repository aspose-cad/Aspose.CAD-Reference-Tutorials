---
title: Enable Mesh Support for DWG Files in Java
linktitle: Enable Mesh Support for DWG Files in Java
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 12
url: /java/dwg-file-operations/mesh-support-for-dwg/
---

## Complete Source Code
```java


import com.aspose.cad.*;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import java.awt.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.cadconsts.CadEntityTypeName;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.polylines.CadPolyFaceMesh;
import com.aspose.cad.fileformats.cad.cadobjects.polylines.CadPolygonMesh;
import java.util.ArrayList;
import java.util.List;

public class MeshSupportForDWG {
    

    public static void main(String[] args) 
    {
        // The path to the resource directory.
        String dataDir = "Your Document Directory" + "DWGDrawings/";
        
        String srcFile = dataDir + "meshes.dwg";

        // com.aspose.cad. objImage = com.aspose.cad.CImage.load(srcFile);
        CadImage cadImage =(CadImage) com.aspose.cad.Image.load(srcFile);
         
        try
        {
            for (CadBaseEntity entity : cadImage.getEntities())
            {
                if (entity instanceof CadPolyFaceMesh)
                {
                  CadPolyFaceMesh asFaceMesh= (CadPolyFaceMesh)entity;

                  if (asFaceMesh != null)
                  {
                      System.out.println("Vetexes count: " + asFaceMesh.getMeshMVertexCount());
                  }
                }
                else if (entity instanceof CadPolygonMesh)
                {
                    CadPolygonMesh asPolygonMesh= (CadPolygonMesh)entity;

                    if (asPolygonMesh != null)
                    {
                      System.out.println("Vetexes count: " + asPolygonMesh.getMeshMVertexCount());
                   }
                }
            }
        }
        finally
        {
            cadImage.dispose();
        }
        
    }
}

```
