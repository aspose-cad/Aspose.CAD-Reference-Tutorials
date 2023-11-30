---
title: Exportación de DWG a PDF o imágenes rasterizadas - Guía Aspose.CAD
linktitle: Exportación de DWG a PDF o imágenes rasterizadas
second_title: Aspose.CAD .NET - Formato de archivo CAD y BIM
description: Explore una guía completa sobre cómo exportar DWG a PDF o imágenes rasterizadas usando Aspose.CAD para .NET. Conozca los pasos, los requisitos previos y practique esta potente biblioteca.
type: docs
weight: 11
url: /es/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
---
## Introducción

¿Está buscando convertir sin problemas archivos DWG a PDF o imágenes rasterizadas en su aplicación .NET? ¡No busque más! Esta guía paso a paso lo guiará a través del proceso utilizando la poderosa biblioteca Aspose.CAD para .NET. Ya sea que sea un desarrollador experimentado o recién esté comenzando, este tutorial está dirigido a todos los niveles.

## Requisitos previos

Antes de sumergirnos en el tutorial, asegúrese de tener lo siguiente en su lugar:

- Un conocimiento básico de la programación .NET.
-  Aspose.CAD para la biblioteca .NET instalada. Si no, descárgalo[aquí](https://releases.aspose.com/cad/net/).
- Su entorno de desarrollo integrado (IDE) favorito configurado para el desarrollo .NET.

## Importar espacios de nombres

Comencemos importando los espacios de nombres necesarios en su proyecto .NET. Esto garantiza que tenga acceso a la funcionalidad Aspose.CAD en su código.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Paso 1: cargar el archivo DWG

Comience cargando el archivo DWG que desea convertir. Reemplace "Su directorio de documentos" con la ruta a su archivo DWG.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Su código para cargar DWG va aquí
}
```

## Paso 2: configurar la exportación de PDF

Ahora, configuremos los ajustes de exportación de PDF. Este ejemplo demuestra cómo configurar el diseño y manejar las conversiones de unidades.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Comprobar y definir el sistema de unidades.
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Su código para configurar la exportación de PDF va aquí
```

## Paso 3: exportar a PDF

Ejecute la exportación a PDF utilizando los ajustes configurados.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Paso 4: Exportar a imágenes rasterizadas

Amplíe la funcionalidad para exportar a imágenes rasterizadas, como PNG.

```csharp
// Tamaño A4 a 300 ppp - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Conclusión

¡Felicidades! Ha aprendido con éxito cómo utilizar Aspose.CAD para .NET para exportar archivos DWG a PDF e imágenes rasterizadas. Esta poderosa biblioteca agiliza el proceso, haciéndolo eficiente y fácil de usar para los desarrolladores.

## Preguntas frecuentes

### P1: ¿Puedo utilizar Aspose.CAD para .NET en mis proyectos comerciales?

 R1: Sí, puedes. Visita[compra.aspose.com/buy](https://purchase.aspose.com/buy) para obtener detalles sobre la licencia.

### P2: ¿Hay una prueba gratuita disponible?

 R2: ¡Por supuesto! Consigue tu prueba gratuita[aquí](https://releases.aspose.com/).

### P3: ¿Cómo puedo obtener soporte para Aspose.CAD para .NET?

 A3: Dirígete al[Foro Aspose.CAD](https://forum.aspose.com/c/cad/19) para el apoyo de la comunidad.

### P4: ¿Puedo obtener una licencia temporal para realizar pruebas?

R4: Sí, puedes obtener una licencia temporal[aquí](https://purchase.aspose.com/temporary-license/).

### P5: ¿Dónde puedo encontrar la documentación detallada?

 R5: La documentación está disponible en[Aspose.CAD](https://reference.aspose.com/cad/net/).