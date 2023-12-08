---
title: Exportar DGN como parte de DWG en Aspose.CAD para .NET
linktitle: Exportar DGN como parte de DWG
second_title: Aspose.CAD .NET - Formato de archivo CAD y BIM
description: Aprenda a exportar DGN como parte de DWG en Aspose.CAD para .NET. Siga nuestra guía paso a paso para una integración perfecta.
type: docs
weight: 11
url: /es/net/cad-export-formats/export-dgn-as-part-of-dwg/
---
## Introducción

En el mundo del desarrollo .NET, Aspose.CAD se destaca como una poderosa biblioteca para trabajar con archivos de diseño asistido por computadora (CAD). Este tutorial lo guiará a través del proceso de exportar un archivo DGN (diseño) como parte de un archivo DWG (dibujo) usando Aspose.CAD para .NET. Ya sea que sea un desarrollador experimentado o recién esté comenzando, esta guía paso a paso lo ayudará a aprovechar las capacidades de Aspose.CAD para realizar esta tarea específica de manera eficiente.

## Requisitos previos

Antes de sumergirse en el tutorial, asegúrese de cumplir con los siguientes requisitos previos:

-  Aspose.CAD para .NET: asegúrese de tener instalada la biblioteca Aspose.CAD para .NET. Puedes descargarlo[aquí](https://releases.aspose.com/cad/net/).

- Entorno de desarrollo: configure su entorno de desarrollo .NET preferido, como Visual Studio.

- Conocimientos básicos de C#: familiarícese con el lenguaje de programación C#.

## Importar espacios de nombres

En su proyecto C#, incluya los espacios de nombres necesarios para acceder a la funcionalidad Aspose.CAD. Agregue las siguientes directivas de uso al comienzo de su archivo de código:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

Ahora, dividamos el código proporcionado en varios pasos:

## Paso 1: definir rutas de archivos

```csharp
//Rutas de archivos de entrada y salida
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

## Paso 2: crear una instancia de PdfOptions

```csharp
// Cree una instancia de la clase PdfOptions para exportar DWG a PDF
PdfOptions exportOptions = new PdfOptions();
```

## Paso 3: cargar el archivo DWG

```csharp
// Cargue el archivo DWG existente como una imagen y conviértalo al tipo CadImage
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

## Paso 4: iterar a través de entidades

```csharp
// Iterar a través de cada entidad dentro del archivo DWG
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

## Paso 5: Verifique el tipo de entidad

```csharp
// Compruebe si la entidad es una definición de imagen.
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

## Paso 6: obtener la ruta subyacente

```csharp
// Si es una definición de imagen, obtenga la referencia externa al objeto.
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

## Paso 7: definir las opciones de rasterización

```csharp
// Definir la configuración para el objeto CadRasterizationOptions
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

## Paso 8: exportar DWG a PDF

```csharp
// Exporte el DWG a PDF llamando al método Guardar
cadImage.Save(outPath, exportOptions);
```

## Conclusión

¡Felicidades! Ha recorrido con éxito el proceso de exportación de un archivo DGN como parte de un archivo DWG utilizando Aspose.CAD para .NET. Este tutorial le ha proporcionado los pasos fundamentales y fragmentos de código para realizar esta tarea específica sin problemas.

## Preguntas frecuentes

### P1: ¿Puedo utilizar Aspose.CAD para .NET en mis proyectos comerciales?
 R1: Sí, puedes. Visita[aquí](https://purchase.aspose.com/buy) para explorar opciones de licencia.

### P2: ¿Existe alguna limitación en el tamaño de los archivos DWG que puedo procesar?
R2: Aspose.CAD admite el manejo de archivos DWG de gran tamaño, pero pueden aplicarse limitaciones de hardware.

### P3: ¿Hay una versión de prueba disponible?
R3: Sí, puedes obtener una prueba gratuita[aquí](https://releases.aspose.com/).

### P4: ¿Cómo puedo obtener licencias temporales?
 R4: Se pueden obtener licencias temporales[aquí](https://purchase.aspose.com/temporary-license/).

### P5: ¿Dónde puedo buscar ayuda si tengo problemas?
 R5: Puedes visitar el foro Aspose.CAD[aquí](https://forum.aspose.com/c/cad/19) para soporte.