---
title: Ajustar el tamaño del dibujo CAD en Aspose.CAD para .NET
linktitle: Ajustar el tamaño del dibujo CAD
second_title: Aspose.CAD .NET - Formato de archivo CAD y BIM
description: Aprenda cómo ajustar sin esfuerzo los tamaños de los dibujos CAD en .NET usando Aspose.CAD. Siga nuestra guía paso a paso para cambiar el tamaño sin problemas.
type: docs
weight: 10
url: /es/net/cad-drawing-manipulation/adjust-cad-drawing-size/
---
## Introducción

¿Está buscando ajustar sin problemas el tamaño de los dibujos CAD en sus aplicaciones .NET? Aspose.CAD para .NET proporciona una solución sólida que le permite manejar sin esfuerzo el cambio de tamaño de los dibujos CAD. En este tutorial, lo guiaremos a través del proceso, desglosando cada paso para asegurarnos de que comprenda las complejidades de cambiar el tamaño de los dibujos CAD usando Aspose.CAD.

## Requisitos previos

Antes de sumergirnos en el tutorial, asegúrese de cumplir con los siguientes requisitos previos:

- Aspose.CAD para la biblioteca .NET: descargue e instale la biblioteca desde[Página de descarga de Aspose.CAD para .NET](https://releases.aspose.com/cad/net/).
- Dibujo CAD de muestra: asegúrese de tener un archivo de dibujo CAD de muestra (por ejemplo, "sample.dwg") en su directorio de documentos.

## Importar espacios de nombres

Comience importando los espacios de nombres necesarios a su aplicación .NET. Este paso es crucial para acceder a las funcionalidades proporcionadas por Aspose.CAD para .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Paso 1: cargar el dibujo CAD

Comience cargando el dibujo CAD en una instancia de la clase Aspose.CAD.Image. Asegúrese de tener la ruta de archivo correcta para su dibujo de muestra.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Cargar un dibujo CAD en una instancia de Imagen
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Tu código aquí...
}
```

## Paso 2: crear BmpOptions

Cree una instancia de la clase BmpOptions, que es responsable de especificar opciones al guardar el dibujo CAD como un archivo BMP.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Paso 3: configurar CadRasterizationOptions

Cree una instancia de la clase CadRasterizationOptions y configure sus propiedades para la rasterización de vectores.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Paso 4: Establecer la propiedad UnitType

Establezca la propiedad UnitType de CadRasterizationOptions para especificar el tipo de unidad para cambiar el tamaño. En este ejemplo, está configurado en Centímetro.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Paso 5: Establecer la propiedad de diseños

Especifique los diseños que desea incluir en el dibujo redimensionado configurando la propiedad Diseños.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Paso 6: Exportar a BMP

Finalmente, guarde el diseño redimensionado como un archivo BMP usando el método Guardar.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

¡Ahora ha ajustado con éxito el tamaño de su dibujo CAD usando Aspose.CAD para .NET!

## Conclusión

En este tutorial, recorrimos el proceso de cambiar el tamaño de dibujos CAD en .NET usando Aspose.CAD. Si sigue estos pasos, podrá integrar perfectamente esta funcionalidad en sus aplicaciones, proporcionando una experiencia de usuario fluida.

## Preguntas frecuentes

### P1: ¿Aspose.CAD para .NET es compatible con todos los formatos CAD?

 R1: Aspose.CAD para .NET admite una amplia gama de formatos CAD, incluidos DWG, DXF, DWF y más. Comprobar el[documentación](https://reference.aspose.com/cad/net/) para la lista completa.

### P2: ¿Puedo cambiar el tamaño de varios diseños simultáneamente?

R2: Sí, puede cambiar el tamaño de varios diseños ajustando la matriz de diseños en CadRasterizationOptions.

### P3: ¿Dónde puedo obtener soporte para Aspose.CAD para .NET?

 A3: Visita el[Foro Aspose.CAD](https://forum.aspose.com/c/cad/19) para el apoyo y asistencia de la comunidad.

### P4: ¿Hay una prueba gratuita disponible?

 R4: Sí, puedes explorar un[prueba gratis](https://releases.aspose.com/) para evaluar las características de Aspose.CAD para .NET.

### P5: ¿Cómo puedo obtener una licencia temporal de Aspose.CAD para .NET?

 R5: Obtener una licencia temporal para realizar pruebas[aquí](https://purchase.aspose.com/temporary-license/).