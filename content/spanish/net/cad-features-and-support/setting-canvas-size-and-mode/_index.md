---
title: Configuración del tamaño y modo del lienzo en Aspose.CAD para .NET
linktitle: Configuración del tamaño y modo del lienzo
second_title: Aspose.CAD .NET - Formato de archivo CAD y BIM
description: Explore la guía paso a paso sobre cómo configurar el tamaño y el modo del lienzo en Aspose.CAD para .NET. Optimice su renderizado CAD con facilidad utilizando este completo tutorial.
type: docs
weight: 16
url: /es/net/cad-features-and-support/setting-canvas-size-and-mode/
---
## Introducción

¿Está listo para desbloquear todo el potencial de Aspose.CAD para .NET y revolucionar su experiencia de renderizado CAD? En este tutorial paso a paso, profundizaremos en las complejidades de configurar el tamaño y el modo del lienzo utilizando la potente biblioteca Aspose.CAD. Ya sea que sea un desarrollador experimentado o recién esté comenzando, esta guía lo guiará a través del proceso, asegurándole que aproveche las capacidades de Aspose.CAD de manera efectiva.

## Requisitos previos

Antes de sumergirnos en el tutorial, asegúrese de cumplir con los siguientes requisitos previos:

-  Biblioteca Aspose.CAD: descargue e instale la biblioteca Aspose.CAD desde[Sitio web de Aspose.CAD](https://releases.aspose.com/cad/net/).

- Entorno de desarrollo: asegúrese de tener un entorno de desarrollo .NET configurado en su máquina.

-  Archivo CAD de muestra: para este tutorial, usaremos un archivo DXF de muestra. Puedes encontrar uno en el[Documentación de Aspose.CAD](https://reference.aspose.com/cad/net/).

## Importar espacios de nombres

Para comenzar, importe los espacios de nombres necesarios al comienzo de su aplicación .NET:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Paso 1: cargar el archivo CAD

Comience cargando el archivo CAD usando el siguiente código:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    //Su código para pasos adicionales irá aquí
}
```

## Paso 2: crear CadRasterizationOptions

 Crear una instancia de`CadRasterizationOptions` y establece sus propiedades:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

## Paso 3: crear opciones de PDF

 Crear una instancia de`PdfOptions` y establecer su`VectorRasterizationOptions` propiedad:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Paso 4: exportar a PDF

Exporte el archivo CAD a PDF usando las opciones configuradas:

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## Paso 5: crear opciones Tiff

 Crear una instancia de`TiffOptions` y establecer su`VectorRasterizationOptions` propiedad:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Paso 6: Exportar a TIFF

Exporte el archivo CAD a TIFF usando las opciones configuradas:

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Conclusión

¡Felicidades! Ha configurado correctamente el tamaño y el modo del lienzo en Aspose.CAD para .NET. Esta poderosa característica abre un mundo de posibilidades para la renderización CAD. Experimente con diferentes opciones y descubra todo el potencial de Aspose.CAD en sus aplicaciones .NET.

## Preguntas frecuentes

### P1: ¿Puedo usar Aspose.CAD con otras bibliotecas .NET?

R1: Sí, Aspose.CAD se integra perfectamente con otras bibliotecas .NET, proporcionando capacidades mejoradas para la manipulación de CAD.

### P2: ¿Hay una prueba gratuita disponible para Aspose.CAD?

 R2: Sí, puede explorar las funciones de Aspose.CAD con una prueba gratuita. Visita[aquí](https://releases.aspose.com/) Para empezar.

### P3: ¿Cómo puedo obtener soporte para Aspose.CAD?

 R3: Para soporte y discusiones, visite el[Foro Aspose.CAD](https://forum.aspose.com/c/cad/19).

### P4: ¿Dónde puedo encontrar documentación completa para Aspose.CAD?

 A4: Consulte el[Documentación de Aspose.CAD](https://reference.aspose.com/cad/net/) para obtener información detallada y ejemplos.

### P5: ¿Cómo compro Aspose.CAD para .NET?

 R5: Para comprar Aspose.CAD, visite el[pagina de compra](https://purchase.aspose.com/buy).