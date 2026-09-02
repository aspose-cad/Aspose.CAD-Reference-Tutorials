---
date: 2026-07-04
description: Aprenda cómo establecer el tamaño de página PDF y exportar PDF a partir
  de imágenes CAD 3D usando Aspose.CAD para .NET – una guía paso a paso para convertir
  DWG a PDF y guardar CAD como PDF.
keywords:
- set pdf page size
- export pdf from cad
- convert dwg to pdf
- save cad as pdf
- cad to pdf tutorial
linktitle: Exportando imágenes 3D a PDF
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  headline: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  type: TechArticle
- description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  name: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  steps:
  - name: Load the CAD Image
    text: '`Image` class represents a CAD drawing loaded into memory, ready for rasterization.'
  - name: Configure Rasterization Options (Save CAD as PDF)
    text: '`RasterizationOptions` class defines how the CAD data is rasterized, including
      page size, DPI, and whether 3‑D entities are rendered.'
  - name: Set PDF Options (Create PDF from CAD)
    text: '`PdfOptions` class holds the output format settings and links the rasterization
      options to PDF generation.'
  - name: Save as PDF (Generate PDF from 3D Model)
    text: '`Save` method on the `Image` object writes the rasterized content to the
      specified PDF file, producing a ready‑to‑share document.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports more than 50 input and output formats, including
      DWG, DXF, DGN, STL, and IFC, ensuring flexibility for any project.
    question: Is Aspose.CAD compatible with all CAD file formats?
  - answer: Absolutely. Set `PageWidth` and `PageHeight` in `RasterizationOptions`
      to any size in points, inches, or millimetres before calling `Save`.
    question: Can I customize the page dimensions when exporting to PDF?
  - answer: Yes, you can obtain temporary licenses for Aspose.CAD by visiting [Temporary
      License](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for Aspose.CAD?
  - answer: Head to the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for
      expert help and peer‑to‑peer advice.
    question: Where can I find additional support or community discussions?
  - answer: Yes, you can explore the features of Aspose.CAD by accessing the [free
      trial](https://releases.aspose.com/).
    question: Is there a free trial version of Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Establecer el tamaño de página PDF – Exportar imágenes 3D a PDF con Aspose.CAD
url: /es/net/3d-image-export/exporting-3d-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar imágenes 3D a PDF - Tutorial de Aspose.CAD

## Introducción

Si necesita **establecer el tamaño de página PDF** al convertir un dibujo CAD 3‑D a PDF, ha llegado al lugar correcto. Este tutorial le muestra, paso a paso, cómo cargar un archivo CAD, configurar las opciones de rasterización —incluyendo dimensiones de página personalizadas— y generar un PDF de alta fidelidad usando Aspose.CAD para .NET. Al final podrá **exportar PDF desde CAD**, **guardar CAD como PDF**, y controlar cada detalle del diseño sin instalar AutoCAD.

## Respuestas rápidas
- **¿Qué significa “exportar PDF desde CAD”?** Convierte un dibujo CAD (DWG, DXF, DGN, etc.) en un PDF que puede abrirse en cualquier dispositivo.  
- **¿Qué biblioteca realiza la conversión?** Aspose.CAD for .NET proporciona rasterización y exportación a PDF sin dependencias externas.  
- **¿Necesito una licencia?** Se requiere una licencia temporal o completa para producción; hay una prueba gratuita disponible.  
- **¿Puedo establecer dimensiones de página personalizadas?** Sí—utilice `PageWidth` y `PageHeight` en `RasterizationOptions`.  
- **¿Se conservará la geometría 3‑D?** Las entidades 3‑D se rasterizan; habilite `TypeOfEntities.Entities3D` para soporte completo 3‑D.

## Qué es “exportar PDF” en el contexto de CAD?

Exportar PDF desde CAD significa tomar un dibujo CAD (DWG, DXF, DGN, etc.) y convertirlo en un archivo PDF que puede contener gráficos vectoriales, vistas 3‑D rasterizadas e información precisa de diseño de página, facilitando su compartición con cualquier persona que no disponga de software CAD.

## ¿Por qué usar Aspose.CAD para exportar PDF?

Aspose.CAD le permite **establecer el tamaño de página PDF** y exportar PDFs completamente en código .NET gestionado. Soporta más de 50 formatos CAD, procesa archivos de hasta 2 GB sin cargar todo el documento en memoria, y preserva grosores de línea, colores y renderizado opcional de entidades 3‑D con una DPI de rasterización de hasta 1200. La biblioteca funciona en Windows, Linux y macOS, por lo que los PDFs generados funcionan en cualquier plataforma.

## Requisitos previos

- **Aspose.CAD for .NET** instalado. Descárguelo desde la [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).  
- Una carpeta que contenga los archivos CAD que desea convertir (p. ej., `C:\CAD\`).  
- .NET 6.0 o posterior (o .NET Framework 4.7.2).  

## Importar espacios de nombres

`using` statements import the Aspose.CAD namespaces needed to work with rasterization and PDF options.  

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Guía paso a paso

### Cómo establecer el tamaño de página PDF al exportar CAD a PDF?

Cargue su archivo CAD, configure las dimensiones de página en `RasterizationOptions`, adjunte esas opciones a una instancia de `PdfOptions` y llame a `Save`. Este flujo de cuatro pasos le brinda control total sobre el tamaño y la calidad de salida manteniendo el código conciso.

### Paso 1: Cargar la imagen CAD

`Image` class represents a CAD drawing loaded into memory, ready for rasterization.  

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD image goes here
}
```

### Paso 2: Configurar opciones de rasterización (Guardar CAD como PDF)

`RasterizationOptions` class defines how the CAD data is rasterized, including page size, DPI, and whether 3‑D entities are rendered.  

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

### Paso 3: Establecer opciones PDF (Crear PDF desde CAD)

`PdfOptions` class holds the output format settings and links the rasterization options to PDF generation.  

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Paso 4: Guardar como PDF (Generar PDF desde modelo 3D)

`Save` method on the `Image` object writes the rasterized content to the specified PDF file, producing a ready‑to‑share document.  

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Problemas comunes y soluciones

| Problema | Razón | Solución |
|----------|-------|----------|
| **El PDF de salida está en blanco** | Nombre de diseño incorrecto o falta el diseño `Model`. | Verifique que `rasterizationOptions.Layouts` coincida con un diseño presente en el archivo CAD. |
| **Baja resolución** | El DPI de rasterización predeterminado es bajo. | Establezca `rasterizationOptions.Resolution = 300;` antes de guardar. |
| **Entidades 3D no mostradas** | `TypeOfEntities` está comentado. | Descomente `rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;`. |
| **Excepción de licencia** | Usando una versión de prueba sin licencia. | Aplique una licencia temporal o permanente mediante `License license = new License(); license.SetLicense("Aspose.CAD.lic");`. |

## Preguntas frecuentes

**Q: ¿Aspose.CAD es compatible con todos los formatos de archivo CAD?**  
A: Sí, Aspose.CAD soporta más de 50 formatos de entrada y salida, incluidos DWG, DXF, DGN, STL e IFC, garantizando flexibilidad para cualquier proyecto.

**Q: ¿Puedo personalizar las dimensiones de página al exportar a PDF?**  
A: Absolutamente. Establezca `PageWidth` y `PageHeight` en `RasterizationOptions` a cualquier tamaño en puntos, pulgadas o milímetros antes de llamar a `Save`.

**Q: ¿Hay licencias temporales disponibles para Aspose.CAD?**  
A: Sí, puede obtener licencias temporales para Aspose.CAD visitando [Temporary License](https://purchase.aspose.com/temporary-license/).

**Q: ¿Dónde puedo encontrar soporte adicional o discusiones de la comunidad?**  
A: Diríjase al [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) para obtener ayuda experta y consejos entre pares.

**Q: ¿Existe una versión de prueba gratuita de Aspose.CAD?**  
A: Sí, puede explorar las funciones de Aspose.CAD accediendo a la [free trial](https://releases.aspose.com/).

## Conclusión

Ahora dispone de un método completo y listo para producción para **establecer el tamaño de página PDF** y **exportar PDF desde imágenes CAD 3D** usando Aspose.CAD para .NET. Ajustando las opciones de rasterización puede afinar la resolución, el diseño de página y el renderizado de entidades 3‑D para cumplir cualquier requisito de documentación. Experimente con diferentes configuraciones de DPI y dimensiones de página para lograr el equilibrio perfecto entre el tamaño del archivo y la fidelidad visual.

{{< blocks/products/products-backtop-button >}}

## Tutoriales relacionados

- [Exportando diseños específicos a PDF - Guía de Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Exportando DWG a PDF o imágenes rasterizadas - Guía de Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Exportar DGN a PDF en Aspose.CAD para .NET](/cad/net/cad-export-formats/export-dgn-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

--- 

**Última actualización:** 2026-07-04  
**Probado con:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose