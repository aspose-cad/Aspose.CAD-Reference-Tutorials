---
date: 2026-04-09
description: Aprenda cómo convertir DWG a imagen y cómo leer las banderas de subyacente
  usando Aspose.CAD para .NET en esta guía paso a paso.
keywords:
- convert dwg to image
- how to read underlay
- Aspose.CAD DWG underlay flags
linktitle: Explorando las banderas de subyacente de los archivos DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Convertir DWG a Imagen – Explorando las banderas de subyacente de archivos
  DWG - Tutorial de Aspose.CAD
url: /es/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Explorando las banderas de subyacente de archivos DWG - Tutorial de Aspose.CAD

## Introducción

## Respuestas rápidas
- **¿Qué significa “convert DWG to image”?**  
  Significa renderizar un dibujo DWG en un formato raster (PNG, JPEG, etc.) usando Aspose.CAD.
- **¿Qué método revela las banderas de subyacente?**  
  Acceda a la propiedad `Flags` del objeto `CadUnderlay` después de cargar el DWG.
- **¿Necesito una licencia para Aspose.CAD?**  
  Hay una licencia temporal disponible para evaluación; se requiere una licencia completa para producción.
- **¿Qué versiones de .NET son compatibles?**  
  .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6 y posteriores.
- **¿Puedo extraer la geometría del subyacente?**  
  Sí – la ruta del subyacente, el punto de inserción, la escala, la rotación y los estados de las banderas son accesibles.

## ¿Qué es “convert DWG to image” y por qué es importante?

Convertir un archivo DWG a una imagen le permite mostrar dibujos CAD en navegadores, incrustarlos en informes o compartirlos con partes interesadas que no disponen de un visor CAD. Durante el renderizado, a menudo es necesario inspeccionar los objetos **underlay** (por ejemplo, referencias DGN) para garantizar que se muestren correctamente. Comprender las banderas de underlay le ayuda a solucionar problemas de recorte, renderizado en monocromo y visibilidad antes de generar la imagen final.

## Requisitos previos

- Un conocimiento básico de programación en C# y .NET.  
- Biblioteca **Aspose.CAD for .NET** instalada. Si aún no la tiene, descárguela **[aquí](https://releases.aspose.com/cad/net/)**.  
- Un archivo DWG para pruebas – el archivo de ejemplo **“BlockRefDgn.dwg”** se usa a lo largo de esta guía.

## Importar espacios de nombres

Para comenzar, importe los espacios de nombres necesarios:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Paso 1: Cargar el archivo DWG y convertir a `CadImage`

Primero, cargue el archivo DWG y conviértalo a un `CadImage`. Este objeto le brinda acceso a todas las entidades del dibujo, incluidas los underlays.

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Load DWG file and convert to CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // Your code for subsequent steps will go here
}
```

## Paso 2: Iterar a través de las entidades

A continuación, recorra cada entidad del dibujo. Aquí es donde localizará los objetos underlay.

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // Your code for subsequent steps will go here
}
```

## Paso 3: Verificar el tipo `CadDgnUnderlay`

Identifique las entidades underlay comprobando su tipo en tiempo de ejecución. La clase `CadDgnUnderlay` representa los underlays DGN incrustados en un DWG.

```csharp
if (entity is CadDgnUnderlay)
{
    // Your code for subsequent steps will go here
}
```

## Paso 4: Acceder a las banderas de subyacente

Una vez que tenga un `CadDgnUnderlay`, conviértalo a `CadUnderlay` para leer sus propiedades y estados de banderas. Las banderas le indican si el underlay es visible, está recortado o se renderiza en monocromo.

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

### Qué indica la salida

- **UnderlayPath / UnderlayName** – donde reside el archivo DGN externo.  
- **InsertionPoint (X, Y)** – coordenadas donde se coloca el underlay en el espacio DWG.  
- **RotationAngle** – rotación aplicada al underlay.  
- **ScaleX / ScaleY / ScaleZ** – factores de escala para cada eje.  
- **Flags** – valores booleanos que indican visibilidad (`UnderlayIsOn`), recorte (`ClippingIsOn`) y renderizado en monocromo (`Monochrome`).

## Problemas comunes y soluciones

| Problema | Razón | Solución |
|----------|-------|----------|
| No hay salida para las verificaciones de banderas | Las banderas de underlay se establecen en 0 cuando el underlay está desactivado. | Asegúrese de que el DWG contenga realmente un underlay activo o cambie la visibilidad en el archivo CAD de origen. |
| Excepción `Invalid cast` | La entidad no es un `CadDgnUnderlay`. | Verifique la condición `if (entity is CadDgnUnderlay)` antes de realizar el casting. |
| El renderizado de la imagen falla después de extraer las banderas | El underlay puede estar recortado o desactivado, lo que produce un área en blanco. | Ajuste las banderas (`UnderlayIsOn = true`, `ClippingIsOn = false`) antes de renderizar la imagen final. |

## Preguntas frecuentes

### Q1: ¿Puedo usar Aspose.CAD para .NET con otros formatos de archivo CAD?

R1: Aspose.CAD admite varios formatos CAD, incluidos DWG, DXF, DGN y más. Consulte la documentación para obtener la lista completa.

### Q2: ¿Hay una licencia temporal disponible para Aspose.CAD para .NET?

R2: Sí, puede obtener una licencia temporal **[aquí](https://purchase.aspose.com/temporary-license/)**.

### Q3: ¿Dónde puedo encontrar soporte para Aspose.CAD para .NET?

R3: Visite el foro de soporte **[aquí](https://forum.aspose.com/c/cad/19)**.

### Q4: ¿Cómo puedo comprar Aspose.CAD para .NET?

R4: Compre la biblioteca **[aquí](https://purchase.aspose.com/buy)**.

### Q5: ¿Hay una prueba gratuita disponible?

R5: Sí, puede acceder a la prueba gratuita **[aquí](https://releases.aspose.com/)**.

## Conclusión

¡Felicidades! Ha aprendido con éxito **cómo convertir DWG a imagen** y también a dominar **cómo leer las banderas de underlay** usando Aspose.CAD para .NET. Con este conocimiento puede:

- Renderizar dibujos DWG como imágenes raster para escenarios web o de informes.  
- Inspeccionar y manipular las propiedades del underlay para garantizar una visualización correcta.  
- Depurar problemas de visibilidad, recorte y monocromo antes de la generación de la imagen final.

Explore otras funciones de Aspose.CAD, como la gestión de capas, extracción de texto y conversión por lotes, para ampliar aún más sus flujos de trabajo de automatización CAD.

---

**Última actualización:** 2026-04-09  
**Probado con:** Aspose.CAD for .NET 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}