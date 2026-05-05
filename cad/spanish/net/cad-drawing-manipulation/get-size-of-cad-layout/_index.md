---
date: 2026-03-21
description: Aprende cómo obtener el tamaño del diseño CAD en .NET usando Aspose.CAD.
  Sigue nuestra guía paso a paso para una manipulación eficiente de archivos CAD.
linktitle: Get Size of CAD Layout
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Obtener el tamaño del diseño CAD en Aspose.CAD para .NET
url: /es/net/cad-drawing-manipulation/get-size-of-cad-layout/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Obtener el tamaño del diseño CAD en Aspose.CAD para .NET

## Introducción

En este tutorial completo descubrirás **cómo obtener el tamaño del diseño CAD** usando la biblioteca Aspose.CAD para .NET. Ya sea que estés creando un visor CAD, generando miniaturas o necesites dimensiones precisas del diseño para procesamiento posterior, conocer el tamaño exacto de cada diseño es esencial. Recorreremos todo el flujo de trabajo—desde cargar un dibujo hasta extraer las dimensiones del diseño y, opcionalmente, guardarlas como imágenes—para que puedas integrar esta capacidad en tus propias aplicaciones con confianza.

## Respuestas rápidas
- **¿Qué significa “obtener el tamaño del diseño CAD”?** Significa recuperar el ancho y la altura (en unidades del dibujo) de cada diseño no vacío en un archivo CAD.  
- **¿Qué biblioteca lo soporta?** Aspose.CAD para .NET proporciona una API sencilla para acceder a la información de los diseños.  
- **¿Necesito una licencia?** Una prueba gratuita funciona para evaluación; se requiere una licencia comercial para uso en producción.  
- **¿Formatos compatibles?** DWG, DXF y muchos otros formatos CAD/BIM son totalmente compatibles.  
- **¿Tiempo típico de implementación?** Aproximadamente 10‑15 minutos para una rutina básica de obtención de tamaño.

## ¿Qué es “obtener el tamaño del diseño CAD”?
Obtener el tamaño del diseño CAD significa extraer la extensión geométrica de cada diseño (espacio papel) definido en un dibujo CAD. Estas extensiones se expresan en las unidades nativas del dibujo (usualmente milímetros o pulgadas) y son útiles para tareas como escalado, impresión o generación de imágenes de vista previa.

## ¿Por qué obtener el tamaño del diseño CAD con Aspose.CAD?
- **Sin necesidad de software CAD** – Funciona completamente del lado del servidor.  
- **Multiplataforma** – Funciona con .NET Framework, .NET Core y .NET 5/6+.  
- **Mediciones precisas** – Devuelve las extensiones exactas tal como están almacenadas en el archivo, evitando análisis manuales.  
- **Integración sencilla** – Llamadas API simples encajan de forma natural en proyectos C# existentes.

## Requisitos previos

Antes de sumergirnos en el código, asegúrate de contar con lo siguiente:

- Aspose.CAD para .NET instalado. Puedes descargarlo desde la [página de descarga de Aspose.CAD para .NET](https://releases.aspose.com/cad/net/).
- Uno o más archivos CAD (DWG, DXF, etc.) que desees analizar. Esta guía usa `conic_pyramid.dxf` y `Bottom_plate.dwg` como archivos de ejemplo.

## Importar espacios de nombres

En tu proyecto .NET, comienza importando los espacios de nombres requeridos:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

## Paso 1: Configurar el directorio del documento

Define la carpeta que contiene tus archivos CAD. Reemplaza el marcador de posición con la ruta real en tu máquina.

```csharp
string MyDir = "Your Document Directory";
```

## Paso 2: Especificar rutas de archivos CAD

Crea una matriz que apunte a cada archivo CAD que quieras procesar.

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## Paso 3: Recorrer los archivos CAD

Carga cada archivo, detecta su formato y prepárate para extraer la información del diseño.

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ... (continue to the next step)
    }
}
```

## Paso 4: Obtener diseños no vacíos

Necesitamos un método auxiliar que devuelva solo los diseños que realmente contienen entidades de dibujo. Los diseños vacíos se ignoran porque no tienen tamaño que reportar.

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ... (continue to the next step)
}
```

## Paso 5: Obtener diseños para archivos DWG

Los archivos DWG almacenan la información de los diseños en la tabla `HeaderVariables`. El siguiente método extrae los nombres de todos los diseños no vacíos para un dibujo DWG.

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## Paso 6: Obtener diseños para archivos DXF

Los archivos DXF usan una estructura diferente. Este método analiza la colección `Tables` para encontrar diseños de espacio papel que contengan entidades.

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## Paso 7: Recuperar el tamaño del diseño y guardarlo como imagen

Finalmente, recorre cada diseño descubierto, lee sus extensiones y, opcionalmente, renderiza el diseño a un archivo de imagen para verificación visual.

```csharp
foreach (string layout in layouts)
{
    // ... (continue to the next step)
}
```

## Problemas comunes y consejos

- **Nombres de diseño faltantes:** Asegúrate de que el archivo CAD realmente contenga diseños de espacio papel; algunos archivos solo tienen espacio modelo.  
- **Unidades incorrectas:** El tamaño se devuelve en las unidades nativas del dibujo. Convierte a milímetros o pulgadas si es necesario.  
- **Rendimiento:** Cargar archivos DWG/DXF muy grandes puede consumir mucha memoria; considera procesar los archivos de forma asíncrona o por lotes.

## Preguntas frecuentes

**P: ¿Aspose.CAD es compatible con todos los formatos de archivo CAD?**  
R: Sí, Aspose.CAD soporta una amplia gama de formatos, incluidos DWG, DXF, DGN y muchos tipos de archivos BIM.

**P: ¿Puedo personalizar las opciones de guardado de la imagen?**  
R: ¡Por supuesto! Puedes ajustar `CadRasterizationOptions` (formato, resolución, color de fondo, etc.) para satisfacer tus necesidades específicas.

**P: ¿Dónde puedo encontrar documentación adicional?**  
R: Consulta la [documentación de Aspose.CAD](https://reference.aspose.com/cad/net/) para referencias API detalladas y más ejemplos.

**P: ¿Hay una prueba gratuita disponible?**  
R: Sí, puedes explorar Aspose.CAD con una [prueba gratuita](https://releases.aspose.com/).

**P: ¿Cómo puedo obtener soporte técnico?**  
R: Para soporte técnico, visita el [foro de Aspose.CAD](https://forum.aspose.com/c/cad/19).

---

**Última actualización:** 2026-03-21  
**Probado con:** Aspose.CAD 24.11 para .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}