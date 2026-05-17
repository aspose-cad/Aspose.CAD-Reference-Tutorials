---
date: 2026-03-24
description: Aprende cómo convertir dgn a png y guardar CAD como jpeg usando Aspose.CAD
  para .NET – una guía rápida para la conversión de CAD a imagen.
linktitle: Export DGN to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Cómo convertir DGN a PNG en Aspose.CAD para .NET
url: /es/net/cad-export-formats/export-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir DGN a PNG en Aspose.CAD para .NET

En el desarrollo moderno de .NET, **convert dgn to png** es un requisito común cuando necesitas mostrar dibujos CAD en la web o incrustarlos en informes. Aspose.CAD para .NET hace que esta conversión sea sencilla, permitiéndote convertir un archivo DGN en una imagen raster de alta calidad con solo unas pocas líneas de código. En esta guía recorreremos todo el proceso, desde la configuración del proyecto hasta guardar el archivo PNG (o JPEG) final.

## Respuestas rápidas
- **¿Puedo convertir DGN a PNG con Aspose.CAD?** Sí, solo configura las opciones de rasterización y elige la salida PNG o JPEG.  
- **¿Necesito una licencia para uso en producción?** Se requiere una licencia válida de Aspose.CAD para implementaciones que no sean de prueba.  
- **¿Qué versiones de .NET son compatibles?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.  
- **¿Qué formatos de imagen están disponibles?** PNG, JPEG, BMP, GIF, TIFF y más.  
- **¿Es necesario el manejo de excepciones?** Absolutamente, envuelve la conversión en try/catch para manejar problemas de acceso a archivos.

## ¿Qué es “convert dgn to png”?
Convertir un archivo DGN (MicroStation) a PNG significa rasterizar datos CAD vectoriales en una imagen basada en píxeles. Esto es útil para generar vistas previas, incrustar dibujos en correos electrónicos HTML o crear miniaturas para sistemas de gestión documental.

## ¿Por qué usar Aspose.CAD para la conversión de CAD a imagen?
- **Sin dependencias externas** – funciona completamente en código administrado.  
- **Alta fidelidad** – preserva grosores de línea, capas y colores.  
- **Salida flexible** – cambia entre PNG, JPEG, BMP, etc., modificando una sola opción.  
- **Optimizado para rendimiento** – la rasterización es rápida incluso para dibujos grandes.

## Requisitos previos

Antes de comenzar, asegúrate de tener:

- **Aspose.CAD for .NET** instalado en tu proyecto. Puedes descargarlo desde el [sitio web](https://reference.aspose.com/cad/net/).  
- Un archivo DGN de muestra (p.ej., `Nikon_D90_Camera.dgn`) colocado en un directorio conocido.

## Importar espacios de nombres

Comienza añadiendo las declaraciones `using` requeridas para que puedas acceder a las clases de Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Paso 1: Cargar el archivo DGN

Carga el DGN de origen en un objeto `CadImage`. Este objeto representa el dibujo CAD en memoria y será la fuente para la rasterización.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Paso 2: Definir opciones de rasterización

Configura cómo debe rasterizarse el dibujo CAD. Aquí puedes controlar el tamaño de la imagen, el escalado y el color de fondo.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Paso 3: Elegir el formato de salida (PNG o JPEG)

Aunque el tutorial se centra en PNG, también podrías querer **guardar cad como jpeg**. Crea el objeto de opciones de imagen apropiado y adjunta la configuración de rasterización.

```csharp
ImageOptionsBase options = new JpegOptions();   // Change to PngOptions() for PNG output
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Consejo profesional:** Para generar un archivo PNG, reemplaza `new JpegOptions()` con `new PngOptions()`.

## Paso 4: Guardar la imagen raster

Finalmente, llama a `Save` en la instancia `CadImage`, proporcionando el nombre de archivo deseado y el objeto de opciones que configuraste.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

Si cambiaste a `PngOptions`, el archivo se guardará como `ExportDGNToRasterImage_out.png`.

## Problemas comunes y soluciones

| Problema | Causa | Solución |
|----------|-------|----------|
| **Imagen de salida en blanco** | `NoScaling` configurado incorrectamente o diseño no seleccionado | Establece `AutomaticLayoutsScaling = true` o especifica el diseño deseado. |
| **Falta de memoria para archivos grandes** | Cargando un DGN enorme sin transmisión | Utiliza `Image.Load(sourceFilePath, new LoadOptions { LoadOnDemand = true })`. |
| **Versión DGN no compatible** | Versiones antiguas de MicroStation | Asegúrate de tener la última versión de Aspose.CAD que soporta formatos heredados. |

## Preguntas frecuentes

**P: ¿Puedo exportar archivos DGN a formatos diferentes de JPEG?**  
R: Sí, Aspose.CAD para .NET soporta PNG, BMP, GIF, TIFF y más – solo cambia la clase de opciones (p.ej., `new PngOptions()`).

**P: ¿Cómo debo manejar excepciones durante la conversión?**  
R: Envuelve el código de conversión en un bloque `try/catch` y registra `Aspose.CAD.CadException` para obtener información detallada del error.

**P: ¿Hay una versión de prueba disponible para Aspose.CAD para .NET?**  
R: Sí, puedes explorar el producto con una prueba gratuita. Visita [aquí](https://releases.aspose.com/) para más información.

**P: ¿Dónde puedo buscar asistencia o discutir problemas relacionados con Aspose.CAD para .NET?**  
R: Dirígete al [foro de Aspose.CAD](https://forum.aspose.com/c/cad/19) para soporte comunitario y discusiones.

**P: ¿Cómo obtengo una licencia temporal para Aspose.CAD para .NET?**  
R: Visita [este enlace](https://purchase.aspose.com/temporary-license/) para adquirir una licencia temporal para tus necesidades de desarrollo.

## Conclusión

Ahora has aprendido cómo **convert dgn to png** (o JPEG) usando Aspose.CAD para .NET. Ajustando las opciones de rasterización y cambiando la clase de opciones de imagen, puedes adaptar la salida a cualquier requisito del proyecto. Siéntete libre de experimentar con diferentes tamaños de página, configuraciones de DPI y formatos de archivo para obtener la imagen raster perfecta para tu aplicación.

---

**Última actualización:** 2026-03-24  
**Probado con:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}