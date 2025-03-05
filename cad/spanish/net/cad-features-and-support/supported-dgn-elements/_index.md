---
title: Elementos DGN compatibles en Aspose.CAD para .NET
linktitle: Elementos DGN compatibles
second_title: Aspose.CAD .NET - Formato de archivo CAD y BIM
description: Explore Aspose.CAD para conocer las potentes funciones de .NET para manejar archivos DGN. Siga nuestra guía paso a paso para trabajar sin problemas con elementos 2D y 3D.
type: docs
weight: 18
url: /es/net/cad-features-and-support/supported-dgn-elements/
---
## Introducción

¿Es usted un desarrollador .NET y busca trabajar con archivos DGN sin problemas? Aspose.CAD para .NET proporciona una solución sólida para manejar archivos DGN de manera eficiente. En este tutorial, profundizaremos en los elementos DGN compatibles y lo guiaremos a través del proceso de trabajo con Aspose.CAD para .NET.

## Requisitos previos

Antes de comenzar, asegúrese de tener lo siguiente:

- Conocimientos básicos de programación .NET.
- Visual Studio instalado en su máquina.
-  Biblioteca Aspose.CAD para .NET, que puedes descargar[aquí](https://releases.aspose.com/cad/net/).

## Importar espacios de nombres

Para poner en marcha su proyecto, importe los espacios de nombres necesarios a su aplicación .NET. Este paso garantiza que tenga acceso a las funcionalidades proporcionadas por Aspose.CAD para .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## Paso 1: cargue el archivo DGN

Comience cargando un archivo DGN existente como CadImage en su aplicación .NET.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Tu código aquí
}
```

## Paso 2: iterar a través de elementos DGN

Itere a través de los elementos DGN utilizando un bucle foreach. Aspose.CAD para .NET proporciona una variedad de tipos de elementos DGN con los que puede trabajar.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Tu código aquí
}
```

## Paso 3: Manejar entidades previamente admitidas

Maneje las entidades 2D admitidas anteriormente, que ahora también son compatibles con 3D.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Casos adicionales
        {
            // Tu código aquí
            break;
        }
}
```

## Paso 4: Manejar entidades 3D compatibles

Maneje las entidades 3D admitidas proporcionadas por Aspose.CAD para .NET.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Tu código aquí
            break;
        }
}
```

## Paso 5: exportar y guardar

Finalmente, exporte el archivo DGN modificado a una imagen rasterizada y guárdelo en el directorio especificado.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

## Conclusión

En este tutorial, exploramos las capacidades de Aspose.CAD para .NET en el manejo y manipulación de archivos DGN. Si sigue la guía paso a paso, podrá trabajar de manera eficiente con elementos DGN compatibles, ya sean entidades 2D o 3D. Aspose.CAD para .NET le permite integrar perfectamente el procesamiento de archivos DGN en sus aplicaciones .NET.

## Preguntas frecuentes

### P1: ¿Dónde puedo encontrar la documentación de Aspose.CAD para .NET?

 A1: Puedes encontrar la documentación.[aquí](https://reference.aspose.com/cad/net/).

### P2: ¿Cómo descargo Aspose.CAD para .NET?

 A2: Puedes descargar la biblioteca.[aquí](https://releases.aspose.com/cad/net/).

### P3: ¿Hay una prueba gratuita disponible de Aspose.CAD para .NET?

 R3: Sí, puedes acceder a la prueba gratuita[aquí](https://releases.aspose.com/).

### P4: ¿Dónde puedo obtener licencias temporales de Aspose.CAD para .NET?

 A4: Hay licencias temporales disponibles[aquí](https://purchase.aspose.com/temporary-license/).

### P5: ¿Necesita ayuda o tiene preguntas?

 A5: Visite la comunidad Aspose.CAD para .NET[Foro de soporte](https://forum.aspose.com/c/cad/19).