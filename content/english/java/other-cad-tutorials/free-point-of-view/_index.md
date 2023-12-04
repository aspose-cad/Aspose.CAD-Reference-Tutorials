---
title: Free Point of View - Aspose.CAD for Java Tutorial
linktitle: Free Point of View - Aspose.CAD for Java Tutorial
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 14
url: /java/other-cad-tutorials/free-point-of-view/
---

## Complete Source Code
```java




import com.aspose.cad.fileformats.ObserverPoint;
import com.aspose.cad.imageoptions.CadRasterizationOptions;


public class FreePointOfView {
    
    public static void main(String[] args) 
    {
        
        
        String dataDir = "Your Document Directory" + "CADConversion/";
        // Path to source file
        String sourceFilePath = dataDir+"conic_pyramid.dxf";
        
        // Load a CAD drawing in an instance of Image
        com.aspose.cad.Image objImage = com.aspose.cad.Image.load(sourceFilePath);
        
        CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
        cadRasterizationOptions.setPageHeight(1500);
        cadRasterizationOptions.setPageWidth(1500);
        // Create an instance of JpegOptions class
        com.aspose.cad.imageoptions.JpegOptions options = new com.aspose.cad.imageoptions.JpegOptions();
        
        options.setVectorRasterizationOptions(cadRasterizationOptions);
        
        
        float xAngle = 10; //Angle of rotation along the X axis
        float yAngle = 30; //Angle of rotation along the Y axis
        float zAngle = 40; //Angle of rotation along the Z axis
        
        ObserverPoint obvPoint = new ObserverPoint(xAngle,yAngle,zAngle);
        cadRasterizationOptions.setObserverPoint(obvPoint);
        
        options.setVectorRasterizationOptions(cadRasterizationOptions);
        
        //Saving to Image
         objImage.save(dataDir+"FreePointOfView_out.jpeg", options);
        
    }
}

```
