---
date: 2026-04-03
description: Aprende a configurar el viewport y convertir DWG a PDF en C# usando Aspose.CAD.
  Este tutorial de DWG a PDF muestra una exportación precisa con coordenadas.
keywords:
- how to set viewport
- dwg to pdf tutorial
- convert dwg to pdf c#
linktitle: Convertir DWG a PDF con coordenadas en C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Cómo establecer el viewport al convertir DWG a PDF con coordenadas en C# -
  Tutorial de Aspose.CAD
url: /es/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir DWG a PDF con coordenadas en C# - Tutorial de Aspose.CAD

## Introducción

Bienvenido a este tutorial completo sobre **how to set viewport** mientras se convierten archivos DWG a PDF con coordenadas especificadas usando Aspose.CAD para .NET. Al controlar el viewport obtienes PDFs de píxel perfecto que coinciden exactamente con el área que necesitas, perfecto para planos de construcción, vistas previas de planos de planta o cualquier flujo de trabajo BIM.

## Respuestas rápidas
- **¿Qué significa “set viewport”?** Define la región visible y la escala del dibujo CAD durante la rasterización.  
- **¿Qué biblioteca maneja la conversión?** Aspose.CAD for .NET.  
- **¿Necesito una licencia?** Una prueba gratuita funciona para evaluación; se requiere una licencia comercial para producción.  
- **¿Plataformas compatibles?** Windows, Linux y macOS con .NET 5/6/7 o .NET Framework 4.6+.  
- **¿Tiempo típico de implementación?** Alrededor de 10‑15 minutos para una conversión básica.

## Requisitos previos

Antes de comenzar, asegúrate de contar con los siguientes requisitos:

- **Aspose.CAD Library** – Descarga e instala la biblioteca Aspose.CAD para .NET. Puedes encontrar la biblioteca [aquí](https://releases.aspose.com/cad/net/).
- **Entorno de desarrollo** – Visual Studio, Rider, o cualquier IDE que soporte desarrollo .NET.
- **Archivo DWG** – Ten un archivo DWG listo para la conversión. Puedes usar el archivo de ejemplo proporcionado o tu propio archivo DWG.

## Cómo establecer el viewport para una exportación PDF precisa

Establecer el viewport es el paso central que te permite definir el área exacta del dibujo que deseas renderizar. En el código a continuación creamos un nuevo `CadVportTableObject`, lo posicionamos con la coordenada superior izquierda y calculamos el ancho, la altura y la relación de aspecto. Esta es la implementación de **how to set viewport** que impulsa el resto de la conversión.

## Importar espacios de nombres

En tu proyecto C#, importa los espacios de nombres necesarios:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

## Paso 1: Definir el directorio del documento

```csharp
string MyDir = "Your Document Directory";
```

## Paso 2: Establecer la ruta del archivo DWG de origen

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## Paso 3: Cargar el archivo DWG y configurar las opciones de rasterización

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## Paso 4: Definir coordenadas y viewport  

Aquí realmente **set the viewport** (how to set viewport) especificando la esquina superior izquierda, el ancho y la altura del área que deseas exportar.

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## Paso 5: Aplicar la configuración del viewport

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## Paso 6: Configurar opciones PDF y exportar  

Ahora unimos todo y **convert DWG to PDF** usando las opciones de rasterización que acabamos de preparar.

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## Paso 7: Mostrar mensaje de éxito

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Casos de uso comunes

- **Construction documentation** – Generar PDFs imprimibles de secciones específicas del plano de planta.  
- **BIM coordination** – Exportar solo el área de interés para detección de interferencias.  
- **Client presentations** – Proporcionar un PDF limpio de una habitación o elevación seleccionada sin exponer todo el dibujo.

## Conclusión

¡Felicidades! Has **converted DWG to PDF** con coordenadas precisas y aprendido **how to set viewport** usando Aspose.CAD para .NET. Este **dwg to pdf tutorial** demuestra cómo **create pdf from dwg** y **export dwg as pdf c#** mientras mantienes el control total sobre el área de salida.

## Preguntas frecuentes

### Q1: ¿Puedo usar Aspose.CAD con otros formatos de archivo CAD?

A1: Sí, Aspose.CAD soporta varios formatos CAD, incluidos DWG, DXF, DWF y más.

### Q2: ¿Cómo puedo manejar errores durante el proceso de conversión?

A2: Implementa mecanismos de manejo de errores usando bloques try‑catch para capturar y gestionar excepciones.

### Q3: ¿Es Aspose.CAD adecuado para entornos Windows y Linux?

A3: Sí, Aspose.CAD es compatible con plataformas Windows y Linux.

### Q4: ¿Puedo personalizar aún más la salida PDF?

A4: ¡Por supuesto! Explora las amplias opciones que ofrece Aspose.CAD para adaptar la salida PDF a tus requisitos específicos.

### Q5: ¿Dónde puedo encontrar soporte adicional o discusiones de la comunidad?

A5: Visita el [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) para soporte comunitario y discusiones.

## Preguntas frecuentes adicionales

**Q: ¿Este enfoque funciona con archivos DWG grandes (cientos de MB)?**  
A: Sí. La rasterización se realiza página por página, y puedes ajustar `rasterizationOptions` (p.ej., `Resolution`) para equilibrar calidad y uso de memoria.

**Q: ¿Puedo exportar varios viewports en páginas PDF separadas?**  
A: Puedes iterar sobre `cadImage.ViewPorts`, establecer cada uno como activo y llamar a `Save` para cada página, luego combinar los PDFs usando Aspose.PDF.

**Q: ¿Es posible añadir una marca de agua al PDF generado?**  
A: Después de guardar el PDF, puedes volver a abrirlo con Aspose.PDF y aplicar una marca de agua de texto o imagen antes de entregarlo al usuario.

---

**Última actualización:** 2026-04-03  
**Probado con:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}