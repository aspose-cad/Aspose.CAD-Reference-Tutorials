---
title: Conversión de DWG a PDF de cumplimiento - Tutorial de Aspose.CAD
linktitle: Conversión de DWG a PDF de cumplimiento
second_title: Aspose.CAD .NET - Formato de archivo CAD y BIM
description: Convierta DWG a PDF de cumplimiento con Aspose.CAD para .NET. Siga nuestro tutorial para obtener orientación paso a paso.
weight: 13
url: /es/net/conversion-and-export/converting-dwg-to-compliance-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Conversión de DWG a PDF de cumplimiento - Tutorial de Aspose.CAD

## Introducción

Bienvenido a nuestro tutorial paso a paso sobre cómo convertir archivos DWG a PDF de cumplimiento usando Aspose.CAD para .NET. Aspose.CAD es una potente API .NET que permite a los desarrolladores trabajar con formatos de archivos CAD sin esfuerzo. En este tutorial, lo guiaremos a través del proceso de conversión de un archivo DWG a PDF de cumplimiento con ejemplos y explicaciones detalladas.

## Requisitos previos

Antes de comenzar, asegúrese de tener implementados los siguientes requisitos previos:

-  Aspose.CAD para .NET: asegúrese de tener la biblioteca Aspose.CAD integrada en su proyecto .NET. Puedes descargarlo[aquí](https://releases.aspose.com/cad/net/).

- Entorno de desarrollo: tenga instalado un entorno de desarrollo .NET que funcione y asegúrese de que esté configurado correctamente.

- Archivo DWG de muestra: descargue un archivo DWG de muestra que desee convertir a PDF de cumplimiento.

## Importar espacios de nombres

En su proyecto .NET, importe los espacios de nombres necesarios para utilizar las funcionalidades de Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

Ahora, analicemos el proceso de conversión de un archivo DWG a PDF de cumplimiento en varios pasos.

## Paso 1: cargue el archivo DWG

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

Aspose.CAD.Image cadImage = Aspose.CAD.Image.Load(sourceFilePath);
```

## Paso 2: configurar las opciones de rasterización

 Crear una instancia de`CadRasterizationOptions` y configurar sus propiedades, como el color de fondo, el ancho y el alto de la página.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    BackgroundColor = Aspose.CAD.Color.White,
    PageWidth = 1600,
    PageHeight = 1600
};
```

## Paso 3: crear opciones de PDF

 Crear una instancia de`PdfOptions` y configure las opciones de rasterización vectorial.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions,
    CorePdfOptions = new PdfDocumentOptions { Compliance = PdfCompliance.PdfA1a }
};
```

## Paso 4: guardar como PDF (cumplimiento con A1a)

Guarde la imagen CAD como PDF de cumplimiento con cumplimiento A1a.

```csharp
cadImage.Save(MyDir + "PDFA1_A.pdf", pdfOptions);
```

## Paso 5: guardar como PDF (cumplimiento con A1b)

Cambie el tipo de cumplimiento a A1b y guarde la imagen CAD como PDF de cumplimiento.

```csharp
pdfOptions.CorePdfOptions.Compliance = PdfCompliance.PdfA1b;
cadImage.Save(MyDir + "PDFA1_B.pdf", pdfOptions);
```

## Conclusión

¡Felicidades! Ha convertido con éxito un archivo DWG a PDF de cumplimiento utilizando Aspose.CAD para .NET. Este tutorial proporciona una guía completa para desarrolladores que buscan integrar capacidades de conversión CAD en sus aplicaciones.

## Preguntas frecuentes

### P1: ¿Puedo convertir otros formatos CAD a PDF de cumplimiento usando Aspose.CAD?

R1: Sí, Aspose.CAD admite varios formatos CAD, lo que permite la conversión a PDF de cumplimiento.

### P2: ¿Aspose.CAD es compatible con .NET Core?

R2: Sí, Aspose.CAD es compatible tanto con .NET Framework como con .NET Core.

### P3: ¿Existen opciones de licencia para Aspose.CAD?

 R3: Sí, puede explorar opciones de licencia[aquí](https://purchase.aspose.com/buy).

### P4: ¿Hay una prueba gratuita disponible?

 R4: Sí, puedes obtener una prueba gratuita[aquí](https://releases.aspose.com/).

### P5: ¿Dónde puedo obtener soporte para Aspose.CAD?

A5: Visita el[Foro Aspose.CAD](https://forum.aspose.com/c/cad/19) para cualquier consulta relacionada con el soporte.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
