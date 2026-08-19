---
date: 2026-03-19
description: Aprenda cómo redimensionar dibujos CAD en .NET con Aspose.CAD, incluyendo
  cómo escalar unidades de dibujo CAD y ajustar el tamaño del diseño. Siga nuestra
  guía paso a paso.
linktitle: Adjusting CAD Drawing Size
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Cómo redimensionar dibujos CAD con Aspose.CAD para .NET
url: /es/net/cad-drawing-manipulation/adjust-cad-drawing-size/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo redimensionar dibujos CAD con Aspose.CAD para .NET

## Introducción

If you need to **how to resize CAD** files directly from your .NET application, you’ve come to the right place. In this tutorial we’ll show you how to change CAD unit settings, scale CAD drawing dimensions, and adjust CAD size programmatically using Aspose.CAD for .NET. By the end of the guide you’ll have a solid, production‑ready solution for resizing any supported CAD format.

## Respuestas rápidas
- **¿Qué biblioteca se requiere?** Aspose.CAD for .NET  
- **¿Puedo cambiar el tipo de unidad?** Sí – set `UnitType` in `CadRasterizationOptions`  
- **¿Se necesita una licencia para producción?** A valid Aspose.CAD license is required for non‑trial use  
- **¿A qué formato de imagen exporta el ejemplo?** BMP (but any supported raster format works)  
- **¿Cuántas líneas de código?** Less than 30 lines for a complete resize operation  

## ¿Qué es “how to resize CAD” en la práctica?
Redimensionar un dibujo CAD significa convertir los datos vectoriales en una imagen raster a una escala o unidad específica (p. ej., centímetros, pulgadas). Esto es útil cuando necesitas incrustar dibujos en informes, generar miniaturas o integrar visuales CAD en páginas web.

## ¿Por qué ajustar el tamaño de CAD con Aspose.CAD?
- **No se necesita software CAD externo** – todo se ejecuta dentro de tu código .NET.  
- **Control fino** sobre unidades, diseños y opciones de rasterización.  
- **Compatibilidad multiplataforma** – el mismo código funciona para DWG, DXF, DWF y más.  

## Requisitos previos

Antes de comenzar, asegúrate de tener:

- Aspose.CAD for .NET Library: Download and install the library from the [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).  
- Sample CAD Drawing: A file such as `sample.dwg` placed in your project’s document directory.  

## Importar espacios de nombres

Primero, importa los espacios de nombres que te dan acceso a las clases de Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Paso 1: Cargar el dibujo CAD

Carga el archivo fuente en un objeto `Image`. Este objeto representa el dibujo CAD en memoria y será la base para todas las operaciones posteriores.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Load a CAD drawing in an instance of Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code here...
}
```

## Paso 2: Crear BmpOptions (o cualquier otro formato raster)

`BmpOptions` le indica a Aspose.CAD cómo renderizar los datos vectoriales cuando lo guardas como un mapa de bits. Puedes cambiarlo por `PngOptions`, `JpegOptions`, etc., según el formato de destino.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Paso 3: Configurar CadRasterizationOptions

`CadRasterizationOptions` contiene la configuración principal para escalar, convertir unidades y seleccionar el diseño. Vincularlo a la propiedad `VectorRasterizationOptions` de `BmpOptions` garantiza que el rasterizador use tus ajustes personalizados.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Paso 4: Establecer UnitType (cambiar unidad CAD)

Aquí cambiamos la unidad CAD de su valor predeterminado a centímetros. Aquí es donde vive la palabra clave **change cad unit**, y afecta directamente al tamaño final de la imagen.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Paso 5: Elegir diseños (establecer diseños CAD)

Si tu dibujo contiene varios diseños (p. ej., Model, Sheet1), especifica cuáles deseas rasterizar. Seleccionar el diseño correcto es esencial cuando **set cad layouts** para una salida redimensionada.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Paso 6: Exportar a BMP (redimensionar dibujo CAD)

Finalmente, guarda la imagen rasterizada. El archivo de salida refleja el nuevo tamaño, unidad y diseño que configuraste—completando efectivamente la operación **resize CAD drawing**.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

Ahora tienes un archivo BMP que representa el dibujo CAD redimensionado, listo para procesamiento adicional o visualización.

## Problemas comunes y soluciones

| Problema | Por qué ocurre | Solución |
|----------|----------------|----------|
| La salida está borrosa | DPI (puntos por pulgada) bajo por defecto | Set `cadRasterizationOptions.Resolution = 300;` before saving |
| Aparece el diseño incorrecto | Error tipográfico en el nombre del diseño | Verify the exact layout name using a CAD viewer or the `Layouts` collection |
| La conversión de unidades parece incorrecta | Mezcla de unidades métricas e imperiales | Ensure `UnitType` matches the desired measurement system |

## Preguntas frecuentes

### P1: ¿Es Aspose.CAD para .NET compatible con todos los formatos CAD?

A1: Aspose.CAD for .NET supports a wide range of CAD formats, including DWG, DXF, DWF, and more. Check the [documentation](https://reference.aspose.com/cad/net/) for the complete list.

### P2: ¿Puedo redimensionar varios diseños simultáneamente?

A2: Yes, you can resize multiple layouts by adjusting the `Layouts` array in the `CadRasterizationOptions`.

### P3: ¿Dónde puedo obtener soporte para Aspose.CAD para .NET?

A3: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community support and assistance.

### P4: ¿Hay una prueba gratuita disponible?

A4: Yes, you can explore a [free trial](https://releases.aspose.com/) to evaluate the features of Aspose.CAD for .NET.

### P5: ¿Cómo puedo obtener una licencia temporal para Aspose.CAD para .NET?

A5: Obtain a temporary license for testing purposes [here](https://purchase.aspose.com/temporary-license/).

## Preguntas frecuentes

**P: ¿Cómo escalo un dibujo CAD sin cambiar el tipo de unidad?**  
R: Adjust the `Zoom` property of `CadRasterizationOptions` (e.g., `cadRasterizationOptions.Zoom = 2.0;`) to double the size while keeping the original unit.

**P: ¿Puedo exportar a formatos diferentes a BMP?**  
R: Absolutely. Replace `BmpOptions` with `PngOptions`, `JpegOptions`, or any other supported raster format class.

**P: ¿Es posible procesar por lotes una carpeta de dibujos?**  
R: Yes. Loop through the files in a directory, apply the same rasterization logic, and save each output with a unique name.

---

**Last Updated:** 2026-03-19  
**Tested With:** Aspose.CAD for .NET 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}