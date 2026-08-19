---
description: 'Aprende a convertir DWG a PNG y extraer objetos OLE de archivos DWG
  usando Aspose.CAD para .NET: una guía rápida y centrada en el código.'
linktitle: Exporting OLE Objects from DWG Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Convertir DWG a PNG y Exportar Objetos OLE - Tutorial de Aspose.CAD
url: /es/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportando objetos OLE de archivos DWG - Tutorial de Aspose.CAD

## Introducción

Si necesitas **convertir DWG a PNG** mientras extraes objetos OLE incrustados, has llegado al lugar correcto. Aspose.CAD para .NET hace que este proceso de dos pasos sea sencillo, permitiéndote automatizar la extracción y rasterización en solo unas pocas líneas de C#. En los próximos minutos recorreremos todo el flujo de trabajo, desde la configuración del entorno hasta guardar cada DWG como un PNG que contiene los datos OLE extraídos.

## Respuestas rápidas
- **¿Qué cubre este tutorial?** Convertir DWG a PNG y extraer objetos OLE usando Aspose.CAD para .NET.  
- **¿Necesito una licencia?** Una prueba gratuita funciona para desarrollo; se requiere una licencia comercial para producción.  
- **¿Qué versiones de .NET son compatibles?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **¿Puedo procesar varios archivos DWG a la vez?** Sí – el ejemplo recorre una matriz de nombres de archivo.  
- **¿Dónde puedo encontrar más ejemplos?** Consulte la documentación oficial de Aspose.CAD y los enlaces del foro a continuación.

## ¿Qué es **convert DWG to PNG**?
Convertir un DWG (dibujo de AutoCAD) a una imagen PNG rasteriza los datos vectoriales, facilitando su visualización o inserción en páginas web, informes u otras aplicaciones que no admiten DWG de forma nativa. Cuando existen objetos OLE, pueden extraerse y guardarse como activos separados durante la conversión.

## ¿Por qué extraer objetos OLE de archivos CAD?
Muchos dibujos DWG incrustan hojas de cálculo, gráficos u otros documentos de Office como objetos OLE. Extraerlos permite reutilizar los datos originales, automatizar informes o migrar contenido a formatos más recientes sin perder la información incrustada.

## Requisitos previos

- Aspose.CAD for .NET Library: Asegúrate de tener la biblioteca instalada. Puedes descargarla desde la [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).
- Document Directory: Configura un directorio donde se almacenen tus archivos DWG. Reemplaza `"Your Document Directory"` en el fragmento de código proporcionado con la ruta real.

## Importar espacios de nombres

En tu proyecto .NET, importa los espacios de nombres requeridos:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Guía paso a paso

### Paso 1: Establecer el directorio de documentos

```csharp
string MyDir = "Your Document Directory";
```

Reemplaza `"Your Document Directory"` con la ruta donde se encuentran tus archivos DWG.

### Paso 2: Enumerar los archivos DWG que deseas procesar

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Paso 3: Configurar opciones de exportación para la conversión a PNG

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

Puedes ajustar `CadRasterizationOptions` (p. ej., `PageWidth`, `PageHeight`, `BackgroundColor`) para que coincida con la resolución de salida deseada.

### Paso 4: Recorrer cada DWG y realizar la conversión

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

Durante este bucle la biblioteca extrae automáticamente **objetos OLE** incrustados en cada dibujo e incluye esos datos en el PNG generado. Si necesitas los flujos OLE sin procesar, puedes acceder a la colección `cadImage.OleObjects`, una forma práctica de **cómo extraer ole** programáticamente.

## Problemas comunes y solución de problemas

- **Missing layout name** – Asegúrate de que el diseño que especificas (`"Layout1"` en el ejemplo) exista en el DWG de origen; de lo contrario, el rasterizador volverá al espacio modelo predeterminado.
- **Large files cause memory pressure** – Procesa los archivos uno a la vez (como se muestra) y libera los objetos `CadImage` rápidamente con `using`.
- **Unexpected colors** – Establece `rasterizationOptions.BackgroundColor` para que coincida con el fondo del dibujo si se requiere transparencia.

## Preguntas frecuentes

### P1: ¿Es Aspose.CAD para .NET adecuado tanto para archivos CAD junior como senior?
**R1:** Sí, Aspose.CAD para .NET es versátil y puede manejar una amplia gama de archivos CAD, incluidos tanto variantes junior como senior.

### P2: ¿Puedo personalizar las opciones de exportación para diferentes diseños?
**R2:** ¡Absolutamente! Como se muestra en el tutorial, puedes adaptar las opciones de exportación, incluidos los diseños, para satisfacer tus necesidades específicas.

### P3: ¿Dónde puedo encontrar documentación detallada para Aspose.CAD para .NET?
**R3:** Explora la [Aspose.CAD for .NET documentation](https://reference.aspose.com/cad/net/) para obtener información profunda y ejemplos.

### P4: ¿Hay una prueba gratuita disponible?
**R4:** Sí, puedes probar las capacidades de Aspose.CAD para .NET con una prueba gratuita. Visita [this link](https://releases.aspose.com/) para comenzar.

### P5: ¿Cómo puedo obtener soporte o conectarme con la comunidad?
**R5:** Para soporte y participación comunitaria, visita el [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

### P6: ¿Cómo **extraer OLE de archivos CAD** sin convertir a PNG?
**R6:** Utiliza la colección `CadImage.OleObjects` después de cargar el DWG; puedes iterar cada `OleObject` y guardar sus datos sin procesar en un archivo.

## Conclusión

Ahora sabes cómo **convertir DWG a PNG** mientras extraes sin problemas **objetos OLE** usando Aspose.CAD para .NET. Este enfoque ahorra tiempo, elimina pasos manuales de copiar‑pegar e integra perfectamente en pipelines automatizados. Siéntete libre de experimentar con otros formatos raster (JPEG, BMP) o explorar el amplio conjunto de funciones de manipulación CAD que Aspose ofrece.

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}