---
title: Agregar marcas de agua a dibujos CAD - Guía Aspose.CAD
linktitle: Agregar marcas de agua a dibujos CAD
second_title: Aspose.CAD .NET - Formato de archivo CAD y BIM
description: Mejore sus dibujos CAD con marcas de agua profesionales utilizando Aspose.CAD para .NET. Siga nuestra guía paso a paso para obtener diseños personalizados y atractivos.
type: docs
weight: 11
url: /es/net/plt-and-watermarking/adding-watermarks-to-cad-drawings/
---
## Introducción

¿Está buscando mejorar sus dibujos CAD agregando marcas de agua profesionales? Aspose.CAD para .NET proporciona una solución sólida para integrar perfectamente marcas de agua en sus archivos CAD. En esta guía paso a paso, lo guiaremos a través del proceso de agregar marcas de agua usando Aspose.CAD, asegurando que sus dibujos no solo transmitan información crítica sino que también lleven su marca única.

## Requisitos previos

Antes de sumergirse en el tutorial, asegúrese de tener lo siguiente:
-  Aspose.CAD para .NET: asegúrese de tener instalada la biblioteca Aspose.CAD. Puedes descargarlo[aquí](https://releases.aspose.com/cad/net/).
- Su directorio de documentos: configure un directorio para almacenar sus dibujos CAD.
¡Ahora comencemos a agregar marcas de agua a sus dibujos CAD!

## Importar espacios de nombres

Comience importando los espacios de nombres necesarios a su proyecto .NET:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Paso 1: cargue el dibujo CAD

```csharp
// La ruta al directorio de documentos.
string MyDir = "Your Document Directory";
using (CadImage cadImage = (CadImage)Image.Load(MyDir + "Drawing11.dwg")) {
```

## Paso 2: agregar marca de agua como MTEXT

```csharp
// Agregar nuevo TEXTO M
CadMText watermark = new CadMText();
watermark.Text = "Watermark message";
watermark.InitialTextHeight = 40;
watermark.InsertionPoint = new Cad3DPoint(300, 40);
watermark.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(watermark);
```

## Paso 3: o agregue una marca de agua como texto

```csharp
// Alternativamente, agregue una entidad más simple como Texto
CadText text = new CadText();
text.DefaultValue = "Watermark text";
text.TextHeight = 40;
text.FirstAlignment = new Cad3DPoint(300, 40);
text.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(text);
```

## Paso 4: exportar a PDF

```csharp
// Exporte el dibujo CAD con marca de agua a PDF
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.Layouts = new[] { "Model" };
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "AddWatermark_out.pdf", pdfOptions);
```

Repita estos pasos para diferentes dibujos y tendrá archivos CAD con marcas de agua de aspecto profesional en poco tiempo.

## Conclusión

¡Felicidades! Ha aprendido con éxito cómo agregar marcas de agua a sus dibujos CAD usando Aspose.CAD para .NET. Este proceso simple pero poderoso le permite personalizar sus diseños manteniendo la integridad de sus dibujos técnicos.

## Preguntas frecuentes

### P1: ¿Puedo personalizar la apariencia de la marca de agua?

R1: Sí, puedes personalizar el texto, la fuente, el tamaño y la posición de la marca de agua según tus preferencias.

### P2: ¿Aspose.CAD es compatible con diferentes formatos de archivos CAD?

R2: Aspose.CAD admite varios formatos de archivos CAD, incluidos DWG y DXF, lo que garantiza una amplia compatibilidad.

### P3: ¿Puedo agregar varias marcas de agua a un solo dibujo CAD?

R3: ¡Absolutamente! Puede agregar tantas marcas de agua como sea necesario, lo que brinda flexibilidad para diferentes casos de uso.

### P4: ¿Aspose.CAD ofrece una prueba gratuita?

R4: Sí, puede explorar las funciones de Aspose.CAD con una prueba gratuita. Consíguelo[aquí](https://releases.aspose.com/).

### P5: ¿Dónde puedo encontrar soporte para Aspose.CAD?

 R5: Para cualquier consulta o ayuda, visite el[Foro Aspose.CAD](https://forum.aspose.com/c/cad/19).