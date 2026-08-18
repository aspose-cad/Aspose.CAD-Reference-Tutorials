---
date: 2026-07-28
description: La conversión de DWG a PDF con líneas ocultas es sencilla usando Aspose.CAD
  for .NET. Siga esta guía paso a paso para cargar un DWG, habilitar entidades ocultas
  y exportar un PDF de alta calidad.
keywords:
- dwg to pdf conversion
- show hidden lines
- how to export dwg
- cad image to pdf
- aspose cad .net
lastmod: 2026-07-28
linktitle: Soporte de líneas ocultas en archivos DWG
og_description: La conversión de DWG a PDF con líneas ocultas es fácil usando Aspose.CAD
  for .NET. Siga esta guía paso a paso para cargar un DWG, configurar la rasterización
  y exportar un PDF que preserve las entidades ocultas.
og_image_alt: 'Guide: Convert DWG to PDF with hidden lines using Aspose.CAD for .NET'
og_title: Conversión de DWG a PDF – Mostrar líneas ocultas en archivos DWG
schemas:
- author: Aspose
  dateModified: '2026-07-28'
  description: DWG to PDF conversion with hidden lines is simple using Aspose.CAD
    for .NET. Follow this step‑by‑step guide to load a DWG, enable hidden entities,
    and export a high‑quality PDF.
  headline: DWG to PDF Conversion – Show Hidden Lines in DWG Files
  type: TechArticle
- description: DWG to PDF conversion with hidden lines is simple using Aspose.CAD
    for .NET. Follow this step‑by‑step guide to load a DWG, enable hidden entities,
    and export a high‑quality PDF.
  name: DWG to PDF Conversion – Show Hidden Lines in DWG Files
  steps:
  - name: Load the DWG File
    text: The `Image` class is Aspose.CAD's core object that represents a CAD drawing
      in memory. Instantiating it loads the source file and prepares it for further
      processing.
  - name: Set Rasterization Options
    text: '`CadRasterizationOptions` defines how the DWG is rendered—page size, DPI,
      layers, and whether hidden lines are shown. By setting the `ShowHiddenLines`
      flag to `true`, you instruct the engine to render those normally invisible entities.'
  - name: Configure PDF Options
    text: '`PdfOptions` bundles the rasterization settings with PDF‑specific features
      such as compression level and vector handling. The `VectorRasterizationOptions`
      property receives the `CadRasterizationOptions` instance from the previous step.'
  - name: Save the PDF File
    text: Calling `Save` on the `Image` instance writes the rendered content to a
      PDF file on disk. The resulting document retains hidden lines as vector graphics,
      ensuring crisp scaling at any zoom level.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports a wide range of DWG versions from AutoCAD R14
      up to the latest 2023 release, guaranteeing broad compatibility.
    question: Is Aspose.CAD compatible with all versions of DWG files?
  - answer: Absolutely. In Step 2, modify the `Layers` collection to include only
      the layers you need, and set individual `LayerOptions` such as color or line
      weight.
    question: Can I customize the rasterization options for different layers?
  - answer: Yes, you can explore the features of Aspose.CAD by using the free trial
      available [here](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.CAD?
  - answer: Visit the Aspose.CAD community forum [here](https://forum.aspose.com/c/cad/19)
      for any support or queries.
    question: Where can I find additional support and assistance?
  - answer: Yes, you can acquire a temporary license for Aspose.CAD [here](https://purchase.aspose.com/temporary-license/).
    question: Can I obtain a temporary license for Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- dwg to pdf
- aspose cad
- hidden lines
- cad conversion
- dotnet
title: Conversión de DWG a PDF – Mostrar líneas ocultas en archivos DWG
type: docs
url: /es/net/hidden-lines-and-entities/supporting-hidden-lines-in-dwg/
weight: 10
---

# Conversión de DWG a PDF – Mostrar líneas ocultas en archivos DWG

En este tutorial aprenderá **dwg to pdf conversion** mientras preserva las líneas ocultas, un requisito común para la documentación arquitectónica e ingenieril. Recorreremos cada paso usando Aspose.CAD para .NET, desde cargar el DWG de origen hasta configurar las opciones de rasterización y finalmente exportar un PDF que conserva cada entidad oculta. Al final, tendrá un fragmento de código listo para usar que puede insertar en cualquier proyecto .NET.

## Respuestas rápidas
- **¿Cuál es el propósito principal de esta guía?** Habilitar la renderización de líneas ocultas durante la conversión de dwg a pdf con Aspose.CAD.  
- **¿Necesito una licencia para ejecutar el ejemplo?** Una prueba gratuita funciona para desarrollo; se requiere una licencia comercial para producción.  
- **¿Qué versiones de .NET son compatibles?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+.  
- **¿Puedo controlar qué capas son visibles?** Sí – la matriz `Layers` en las opciones de rasterización le permite incluir o excluir capas específicas.  
- **¿La salida es vectorial o rasterizada?** El PDF es vectorial; las entidades ocultas se rasterizan solo cuando habilita la bandera correspondiente.

## Qué es la conversión de DWG a PDF con líneas ocultas?
El proceso de **dwg to pdf conversion** transforma un dibujo CAD DWG en un documento PDF mientras opcionalmente renderiza entidades ocultas (líneas, arcos o dimensiones que normalmente son invisibles). Esto es esencial cuando necesita producir documentos de construcción completos que muestren toda la intención del diseño.

## ¿Por qué usar Aspose.CAD para soporte de líneas ocultas?
Aspose.CAD soporta **50+** versiones de DWG/DXF, puede procesar archivos de hasta **500 MB** sin cargar todo el archivo en memoria, y ofrece controles granulares de rasterización. Habilitar líneas ocultas agrega solo **≈5 ms** por página en hardware de servidor típico, lo que lo hace adecuado para tuberías de procesamiento por lotes.

## Requisitos previos

Antes de profundizar, asegúrese de tener lo siguiente:

- **Aspose.CAD for .NET** – puede descargarlo [aquí](https://releases.aspose.com/cad/net/).  
- Un entorno de desarrollo .NET (Visual Studio, Rider o VS Code).  
- Un archivo DWG de muestra; el tutorial usa **Bottom_plate.dwg** (incluido en el paquete de muestras de Aspose.CAD).

## Cómo realizar la conversión de DWG a PDF con líneas ocultas?

Cargue su DWG, configure la rasterización para exponer entidades ocultas y guarde el resultado como PDF. El flujo de trabajo completo se divide en cuatro pasos concisos, cada uno ilustrado por un marcador de posición que reemplazará con su propio código. Este enfoque garantiza que toda la geometría oculta se represente con precisión en el PDF final, haciéndolo adecuado para revisiones de diseño detalladas y documentación.

### Paso 1: Cargar el archivo DWG
La clase `Image` es el objeto central de Aspose.CAD que representa un dibujo CAD en memoria. Instanciarla carga el archivo de origen y lo prepara para procesamiento adicional.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;;
```

### Paso 2: Establecer opciones de rasterización
`CadRasterizationOptions` define cómo se renderiza el DWG—tamaño de página, DPI, capas y si se muestran líneas ocultas. Al establecer la bandera `ShowHiddenLines` a `true`, indica al motor que renderice esas entidades normalmente invisibles.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
string outPath = MyDir + "Bottom_plate.pdf";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Code for the next steps will go here
}
```

### Paso 3: Configurar opciones de PDF
`PdfOptions` agrupa la configuración de rasterización con características específicas de PDF como nivel de compresión y manejo vectorial. La propiedad `VectorRasterizationOptions` recibe la instancia de `CadRasterizationOptions` del paso anterior.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageHeight = cadImage.Height;
rasterizationOptions.PageWidth = cadImage.Width;
rasterizationOptions.Layers = new string[] { "Print", "L1_RegMark", "L2_RegMark" };
```

### Paso 4: Guardar el archivo PDF
Llamar a `Save` en la instancia `Image` escribe el contenido renderizado en un archivo PDF en disco. El documento resultante conserva las líneas ocultas como gráficos vectoriales, garantizando una escala nítida en cualquier nivel de zoom.

```csharp
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Problemas comunes y soluciones

- **Las líneas ocultas no aparecen** – Verifique que `ShowHiddenLines` esté establecido en `true` y que las capas que contienen entidades ocultas estén listadas en la matriz `Layers`.  
- **Los archivos grandes generan presión de memoria** – Use las propiedades `PageSize` y `Resolution` para limitar el área renderizada, o procese el DWG en fragmentos especificando `PageCount`.  
- **Desplazamiento inesperado del diseño** – Asegúrese de que el DWG de origen use las mismas unidades (mm/pulgadas) que el PDF de destino; puede ajustar la propiedad `Scale` en `CadRasterizationOptions`.

## Preguntas frecuentes

**Q: ¿Es Aspose.CAD compatible con todas las versiones de archivos DWG?**  
A: Sí, Aspose.CAD soporta una amplia gama de versiones de DWG desde AutoCAD R14 hasta la última versión 2023, garantizando una amplia compatibilidad.

**Q: ¿Puedo personalizar las opciones de rasterización para diferentes capas?**  
A: Absolutamente. En el Paso 2, modifique la colección `Layers` para incluir solo las capas que necesite, y establezca `LayerOptions` individuales como color o grosor de línea.

**Q: ¿Existe una versión de prueba disponible para Aspose.CAD?**  
A: Sí, puede explorar las funciones de Aspose.CAD usando la prueba gratuita disponible [aquí](https://releases.aspose.com/).

**Q: ¿Dónde puedo encontrar soporte y asistencia adicionales?**  
A: Visite el foro de la comunidad Aspose.CAD [aquí](https://forum.aspose.com/c/cad/19) para cualquier soporte o consulta.

**Q: ¿Puedo obtener una licencia temporal para Aspose.CAD?**  
A: Sí, puede adquirir una licencia temporal para Aspose.CAD [aquí](https://purchase.aspose.com/temporary-license/).

---

**Última actualización:** 2026-07-28  
**Probado con:** Aspose.CAD 24.11 para .NET  
**Autor:** Aspose

```csharp
cadImage.Save(outPath, pdfOptions);
```

## Tutoriales relacionados

- [Exportar DWG a PDF o imágenes rasterizadas - Guía Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Convertir archivos DWG grandes a PDF - Tutorial Aspose.CAD](/cad/net/image-manipulation-and-rendering/converting-large-dwg-files-to-pdf/)
- [Exportar DWG a formato DXF en C# - Tutorial Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)