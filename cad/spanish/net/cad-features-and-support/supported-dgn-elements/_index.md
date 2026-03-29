---
date: 2026-03-29
description: Aprenda cómo convertir DGN a PNG usando Aspose.CAD para .NET. Esta guía
  también cubre el soporte de formatos de archivo CAD y el conjunto completo de elementos
  DGN compatibles.
linktitle: Supported DGN Elements
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Convertir DGN a PNG con Aspose.CAD para .NET
url: /es/net/cad-features-and-support/supported-dgn-elements/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir DGN a PNG con Aspose.CAD para .NET

## Introducción

¿Eres un desarrollador .NET que busca **convertir DGN a PNG** sin problemas? Aspose.CAD para .NET ofrece una solución robusta para manejar archivos DGN de manera eficiente. En este tutorial, profundizaremos en los elementos DGN compatibles, guiándote a través del proceso de trabajo con Aspose.CAD para .NET y mostrándote exactamente cómo exportar esos elementos a imágenes PNG.

## Respuestas rápidas
- **¿Qué hace Aspose.CAD?** Lee, modifica y convierte archivos CAD/BIM (incluido DGN) a formatos raster como PNG.  
- **¿Puedo convertir elementos DGN 2D y 3D?** Sí, se admiten tanto entidades 2‑D como 3‑D.  
- **¿Qué versiones de .NET se requieren?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **¿Necesito una licencia para pruebas?** Hay una prueba gratuita disponible; se requiere una licencia para producción.  
- **¿Dónde obtengo la biblioteca?** Descárgala desde el sitio oficial de Aspose (enlace a continuación).

## ¿Qué es “convertir DGN a PNG”?
Convertir DGN a PNG significa renderizar el dibujo DGN basado en vectores (2‑D o 3‑D) a un formato de imagen raster (PNG). Esto es útil cuando necesitas mostrar dibujos CAD en la web, incrustarlos en informes o generar miniaturas sin requerir un visor CAD.

## ¿Por qué usar Aspose.CAD para .NET para el soporte de formatos de archivo CAD?
- **Soporte completo de formatos de archivo CAD** – DGN, DWG, DXF, DWF y más.  
- **Sin dependencias externas** – biblioteca .NET pura, sin instalaciones nativas de CAD.  
- **Renderizado de alta fidelidad** – preserva grosores de línea, colores y geometría 3‑D.  
- **Procesamiento por lotes** – recorre fácilmente muchos archivos en una aplicación del lado del servidor.

## Requisitos previos

Antes de comenzar, asegúrate de tener lo siguiente:

- Conocimientos básicos de programación .NET.  
- Visual Studio instalado en tu máquina.  
- Biblioteca Aspose.CAD para .NET, que puedes descargar [aquí](https://releases.aspose.com/cad/net/).

## Importar espacios de nombres

Para iniciar tu proyecto, importa los espacios de nombres necesarios en tu aplicación .NET. Este paso garantiza que tengas acceso a las funcionalidades proporcionadas por Aspose.CAD para .NET.

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

## Cómo convertir DGN a PNG

A continuación se muestra una guía paso a paso que te lleva a cargar un archivo DGN, iterar sus elementos, manejar tanto entidades 2‑D como 3‑D y, finalmente, exportar el resultado a una imagen raster PNG.

### Paso 1: Cargar el archivo DGN

Comienza cargando un archivo DGN existente como `DgnImage` en tu aplicación .NET.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

### Paso 2: Iterar a través de los elementos DGN

Itera a través de los elementos DGN usando un bucle `foreach`. Aspose.CAD para .NET proporciona una variedad de tipos de elementos DGN con los que puedes trabajar.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Your code here
}
```

### Paso 3: Manejar entidades 2‑D previamente soportadas

Estas entidades ahora también son compatibles con el renderizado 3‑D. La instrucción switch te permite ramificar la lógica según el tipo de elemento.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Additional cases
        {
            // Your code here
            break;
        }
}
```

### Paso 4: Manejar entidades 3‑D compatibles

Aspose.CAD añade soporte completo para varios elementos DGN 3‑D. Amplía el switch para procesarlos según sea necesario.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Your code here
            break;
        }
}
```

### Paso 5: Exportar y guardar como PNG

Después de cualquier manipulación requerida, exporta el dibujo DGN a una imagen raster PNG y guárdala en el directorio especificado.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

> **Consejo:** Usa `Image.Save` con `new PngOptions()` para controlar la resolución, el color de fondo y otras configuraciones específicas de PNG.

## Visión general del soporte de formatos de archivo CAD

Aspose.CAD para .NET no se limita a DGN. También admite DWG, DXF, DWF y muchos otros formatos CAD, brindándote una única API para manejar un amplio espectro de dibujos de ingeniería. Esto lo hace ideal para proyectos que requieren **soporte de formatos de archivo CAD** en varios estándares.

## Problemas comunes y soluciones

| Problema | Razón | Solución |
|----------|-------|----------|
| **La imagen aparece en blanco** | Exportada con DPI cero | Especifica `ResolutionX` y `ResolutionY` en `PngOptions`. |
| **Falta geometría 3‑D** | Tipo de elemento no manejado en el switch | Agrega el caso `DgnElementType` faltante y renderiza en consecuencia. |
| **Falta de memoria en archivos grandes** | Cargando todo el archivo de una vez | Procesa los elementos por lotes o usa streaming cuando sea posible. |

## Preguntas frecuentes

### P1: ¿Dónde puedo encontrar la documentación de Aspose.CAD para .NET?
R1: Puedes encontrar la documentación [aquí](https://reference.aspose.com/cad/net/).

### P2: ¿Cómo descargo Aspose.CAD para .NET?
R2: Puedes descargar la biblioteca [aquí](https://releases.aspose.com/cad/net/).

### P3: ¿Hay una prueba gratuita disponible para Aspose.CAD para .NET?
R3: Sí, puedes acceder a la prueba gratuita [aquí](https://releases.aspose.com/).

### P4: ¿Dónde puedo obtener licencias temporales para Aspose.CAD para .NET?
R4: Las licencias temporales están disponibles [aquí](https://purchase.aspose.com/temporary-license/).

### P5: ¿Necesitas ayuda o tienes preguntas?
R5: Visita la comunidad de Aspose.CAD para .NET en el [foro de soporte](https://forum.aspose.com/c/cad/19).

---

**Última actualización:** 2026-03-29  
**Probado con:** Aspose.CAD para .NET 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}