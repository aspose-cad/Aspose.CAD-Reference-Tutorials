---
title: Override Automatic Code Page Detection in DWG Files with Java
linktitle: Override Automatic Code Page Detection in DWG Files with Java
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 13
url: /java/dwg-file-operations/override-code-page-detection/
---

## Complete Source Code
```java
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */


import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;

import com.aspose.cad.fileformats.cad.CadImage;


public class OverrideAutomaticCodePageDetectionDwg {
    public static void main(String[] args) {
        
        String SourceDir = Utils.getDataDir_DWGDrawings();
        String dwgPathToFile = SourceDir + "SimpleEntites.dwg";


        LoadOptions opts = new LoadOptions();
        opts.setSpecifiedEncoding(CodePages.Japanese);
        opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
        opts.setRecoverMalformedCifMif(false);

        CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);

        //do export or something else with cadImage

        
        System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
    }
}
```
