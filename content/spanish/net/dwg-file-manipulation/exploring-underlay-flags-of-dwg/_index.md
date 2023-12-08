---
title: Exploración de indicadores subyacentes de archivos DWG - Tutorial de Aspose.CAD
linktitle: Exploración de indicadores subyacentes de archivos DWG
second_title: Aspose.CAD .NET - Formato de archivo CAD y BIM
description: Desbloquee el poder de Aspose.CAD para .NET al explorar indicadores de capas subyacentes de archivos DWG. Sigue nuestra guía paso a paso.
type: docs
weight: 13
url: /es/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
---
## Introducción

Si estás profundizando en el intrincado mundo de los archivos CAD, específicamente los archivos DWG, y quieres desbloquear los misterios de las banderas subyacentes, estás en el lugar correcto. Este tutorial lo guiará a través del proceso de exploración de indicadores subyacentes en archivos DWG utilizando la potente biblioteca Aspose.CAD para .NET.

## Requisitos previos

Antes de sumergirnos en el tutorial, asegúrese de tener lo siguiente:

- Un conocimiento básico de la programación en C# y .NET.
-  Aspose.CAD para la biblioteca .NET instalada. Si no, puedes descargarlo.[aquí](https://releases.aspose.com/cad/net/).
- Un archivo DWG para realizar pruebas. Puede utilizar el archivo de muestra "BlockRefDgn.dwg" que se proporciona en el tutorial.

## Importar espacios de nombres

Para comenzar, necesita importar los espacios de nombres necesarios. Aquí tienes un fragmento que te ayudará:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;

```

## Paso 1: cargue el archivo DWG y conviértalo a CadImage

Comience cargando el archivo DWG existente y convirtiéndolo en CadImage:

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Cargue el archivo DWG y conviértalo a CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // Su código para los pasos siguientes irá aquí
}
```

## Paso 2: iterar a través de entidades

A continuación, recorra cada entidad dentro del archivo DWG:

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // Su código para los pasos siguientes irá aquí
}
```

## Paso 3: Verifique el tipo CadDgnUnderlay

Compruebe si la entidad es del tipo CadDgnUnderlay:

```csharp
if (entity is CadDgnUnderlay)
{
    // Su código para los pasos siguientes irá aquí
}
```

## Paso 4: Acceda a las banderas subyacentes

Acceda a diferentes indicadores subyacentes y extraiga información relevante:

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

## Conclusión

¡Felicidades! Ha explorado con éxito los indicadores subyacentes de los archivos DWG utilizando Aspose.CAD para .NET. Este tutorial le proporcionó el conocimiento para navegar a través de entidades y extraer información crucial sobre capas subyacentes.

## Preguntas frecuentes

### P1: ¿Puedo utilizar Aspose.CAD para .NET con otros formatos de archivos CAD?

R1: Aspose.CAD admite varios formatos CAD, incluidos DWG, DXF, DGN y más. Consulte la documentación para obtener la lista completa.

### P2: ¿Hay una licencia temporal disponible para Aspose.CAD para .NET?

 R2: Sí, puedes obtener una licencia temporal[aquí](https://purchase.aspose.com/temporary-license/).

### P3: ¿Dónde puedo encontrar soporte para Aspose.CAD para .NET?

 A3: Visita el foro de soporte[aquí](https://forum.aspose.com/c/cad/19) para asistencia.

### P4: ¿Cómo compro Aspose.CAD para .NET?

A4: Compra la biblioteca[aquí](https://purchase.aspose.com/buy).

### P5: ¿Hay una prueba gratuita disponible?

 R5: Sí, puedes acceder a la prueba gratuita[aquí](https://releases.aspose.com/).
