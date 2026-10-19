---
date: 2026-10-19
description: Aprenda a crear miniaturas PNG de archivos IFC con Aspose.CAD for Java
  en solo unas pocas líneas de código.
keywords:
- create png thumbnail ifc
- ifc to png conversion
- aspose cad java
- java image processing
- bIM visualization
lastmod: 2026-10-19
linktitle: Exportar IFC a PNG
og_description: Cree miniaturas PNG de archivos IFC sin esfuerzo usando Aspose.CAD
  for Java. Esta guía paso a paso le muestra cómo cargar, rasterizar y guardar modelos
  IFC como imágenes PNG de alta calidad.
og_image_alt: Developer guide showing Java code that converts IFC files to PNG thumbnails
  using Aspose.CAD
og_title: Crear miniatura PNG de IFC con Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  headline: How to create PNG thumbnail IFC with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  name: How to create PNG thumbnail IFC with Aspose.CAD for Java
  steps:
  - name: load the IFC file
    text: First, point to the folder where your IFC file lives and load it with `CadImage.load`.
      `CadImage.load` reads a CAD file and returns an image object that can be rasterized.
      > **Why this matters:** Loading the file as a `CadImage` gives you access to
      vector‑raster conversion options that control resol
  - name: set rasterization options
    text: Define the output dimensions and any other vector‑related settings through
      `VectorRasterizationOptions`. `VectorRasterizationOptions` lets you specify
      output size, background color, and other rasterization parameters. > Adjust
      `PageWidth` and `PageHeight` to control the final PNG resolution, which i
  - name: configure PNG options
    text: Link the rasterization options to the PNG exporter by creating a `PngOptions`
      instance.
  - name: save the image as PNG
    text: Finally, write the rasterized image to disk using the `save` method. `save`
      writes the rasterized image to the specified file path in the chosen format.
      > After this step you have successfully **created a PNG thumbnail IFC** and
      can use the resulting `example.png` anywhere you need a raster image.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports many formats (DWG, DXF, DGN, etc.). Simply change
      the file extension and load the appropriate image class.
    question: Can I use this approach to convert other CAD formats to PNG?
  - answer: DPI is controlled indirectly via `PageWidth`/`PageHeight`. Adjust these
      values relative to the desired physical size to achieve the required DPI.
    question: Does the library let me set a custom DPI?
  - answer: PNG is a lossless format, so the rasterized image retains the full visual
      fidelity of the original vector data.
    question: Is the PNG output loss‑less?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- ifc conversion
- png thumbnail
- aspose.cad
- java image processing
- bim visualization
title: Cómo crear miniatura PNG de IFC con Aspose.CAD for Java
url: /es/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar IFC a PNG con Aspose.CAD para Java

## Introducción

En este tutorial aprenderá a **crear archivos PNG miniatura IFC** con Aspose.CAD para Java. Ya sea que necesite vistas previas rápidas para un portal BIM, generar miniaturas para un sistema de gestión de documentos, o automatizar conversiones por lotes, los pasos a continuación le permitirán rasterizar un modelo IFC 3‑D en una nítida imagen PNG 2‑D con solo unas pocas líneas de código Java.

## Respuestas rápidas
- **¿Qué biblioteca se requiere?** Aspose.CAD para Java.  
- **¿Puedo crear una miniatura PNG IFC en unas pocas líneas de código?** Sí – todo el flujo de trabajo cabe en menos de 20 líneas.  
- **¿Necesito una licencia para producción?** Una licencia temporal funciona para pruebas; se requiere una licencia completa para despliegue comercial.  
- **¿La salida es escalable?** Puede establecer cualquier dimensión de píxel, por lo que el PNG se escala a cualquier tamaño que necesite.  
- **¿Qué versión de Java se admite?** Java 8 o superior.

## ¿Qué es “convertir IFC a PNG”?
Convertir IFC (Industry Foundation Classes) a PNG significa rasterizar el modelo de edificio 3‑D en una imagen bitmap 2‑D. Este proceso crea una miniatura visual que puede mostrarse en navegadores, informes o aplicaciones móviles sin requerir un visor CAD completo.

## ¿Por qué usar Aspose.CAD para Java?
Aspose.CAD admite **más de 30 formatos CAD y BIM**, incluidos IFC, DWG, DXF y DGN, y puede procesar archivos de hasta **2 GB** sin cargar todo el documento en memoria.  
La biblioteca es pura Java, tiene **cero dependencias externas**, y se ejecuta en Windows, Linux y macOS, lo que la hace ideal para la generación de imágenes del lado del servidor.  
Proporciona rasterización de alto rendimiento, amplio soporte de formatos y fácil integración en aplicaciones Java.

## Requisitos previos

- **Biblioteca Aspose.CAD** – descargue el último JAR desde el [download link](https://releases.aspose.com/cad/java/).  
- **Kit de desarrollo Java** – JDK 8 o superior instalado en su máquina.  
- **Archivo fuente IFC** – coloque el archivo en una carpeta que pueda referenciar desde su código.

## Importar espacios de nombres

El paquete `com.aspose.cad` proporciona todas las clases que necesita. `CadImage` es el punto de entrada para cargar archivos CAD, mientras que `PngOptions` configura los ajustes de rasterización.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Cómo crear una miniatura PNG de IFC en Java?

Cargue el archivo IFC, defina las opciones de rasterización y guarde el resultado como una imagen PNG – ese es el flujo de trabajo completo de conversión. Las siguientes secciones desglosan cada paso, para que pueda copiar y pegar los fragmentos en su proyecto y ejecutarlos de inmediato.

### Paso 1: cargar el archivo IFC
Primero, indique la carpeta donde se encuentra su archivo IFC y cárguelo con `CadImage.load`.  
`CadImage.load` lee un archivo CAD y devuelve un objeto de imagen que puede rasterizarse.

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

> **Por qué es importante:** Cargar el archivo como `CadImage` le brinda acceso a opciones de conversión vector‑raster que controlan la resolución, el color de fondo y el grosor de línea.

### Paso 2: establecer opciones de rasterización
Defina las dimensiones de salida y cualquier otra configuración relacionada con vectores mediante `VectorRasterizationOptions`.  
`VectorRasterizationOptions` le permite especificar el tamaño de salida, el color de fondo y otros parámetros de rasterización.

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

> Ajuste `PageWidth` y `PageHeight` para controlar la resolución final del PNG, lo cual es esencial cuando **guarda archivos PNG java** para impresiones de alta calidad o miniaturas web.

### Paso 3: configurar opciones PNG
Enlace las opciones de rasterización al exportador PNG creando una instancia de `PngOptions`.

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

### Paso 4: guardar la imagen como PNG
Finalmente, escriba la imagen rasterizada en disco usando el método `save`.  
`save` escribe la imagen rasterizada en la ruta de archivo especificada en el formato elegido.

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

> Después de este paso ha **creado con éxito una miniatura PNG IFC** y puede usar el `example.png` resultante donde necesite una imagen raster.

## Casos de uso comunes
- **Generar miniaturas** para modelos BIM en portales web.  
- **Incorporar instantáneas de planos** en informes PDF o Word.  
- **Conversión por lotes automatizada** de grandes bibliotecas IFC para proyectos de archivo o migración.

## Solución de problemas y consejos
- **Problemas de memoria:** Para archivos IFC muy grandes, aumente el heap de la JVM (`-Xmx2g` o superior).  
- **Texturas faltantes:** Asegúrese de que los recursos externos del archivo IFC sean accesibles desde `dataDir`.  
- **Consejo profesional:** Use `vectorOptions.setBackgroundColor(Color.getWhite())` si prefiere un fondo blanco en lugar del PNG transparente predeterminado.

## Preguntas frecuentes

### P1: ¿Es Aspose.CAD compatible con todas las versiones de archivos IFC?
R1: Aspose.CAD admite varias versiones de IFC. Consulte la [documentation](https://reference.aspose.com/cad/java/) para obtener información detallada de compatibilidad.

### P2: ¿Puedo personalizar aún más las opciones de rasterización?
R2: ¡Absolutamente! Explore la [documentation](https://reference.aspose.com/cad/java/) para configuraciones avanzadas como control de DPI, anti‑aliasing y grosor de línea.

### P3: ¿Hay una versión de prueba disponible?
R3: Sí, puede descargar la prueba gratuita desde el [Aspose.CAD free trial](https://releases.aspose.com/).

### P4: ¿Cómo puedo obtener una licencia temporal para pruebas?
R4: Obtenga una licencia temporal en la [Aspose.CAD temporary license page](https://purchase.aspose.com/temporary-license/).

### P5: ¿Dónde puedo hacer preguntas o reportar problemas?
R5: Únase a la comunidad en el [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) para obtener soporte tanto de ingenieros de Aspose como de otros desarrolladores.

**P: ¿Puedo usar este enfoque para convertir otros formatos CAD a PNG?**  
R: Sí, Aspose.CAD admite muchos formatos (DWG, DXF, DGN, etc.). Simplemente cambie la extensión del archivo y cargue la clase de imagen correspondiente.

**P: ¿La biblioteca me permite establecer un DPI personalizado?**  
R: El DPI se controla indirectamente mediante `PageWidth`/`PageHeight`. Ajuste estos valores en relación con el tamaño físico deseado para lograr el DPI requerido.

**P: ¿La salida PNG es sin pérdida?**  
R: PNG es un formato sin pérdida, por lo que la imagen rasterizada conserva la plena fidelidad visual de los datos vectoriales originales.

## Conclusión

Ahora tiene un método completo y listo para producción para **crear archivos PNG miniatura IFC** usando Aspose.CAD para Java. Integre estos pasos en herramientas de escritorio, servicios del lado del servidor o funciones en la nube para automatizar canalizaciones de visualización BIM y ofrecer miniaturas rápidas y de alta calidad a los usuarios finales.

**Última actualización:** 2026-10-19  
**Probado con:** Aspose.CAD para Java 24.11  
**Autor:** Aspose

## Tutoriales relacionados

- [Cómo convertir STL a PNG con Aspose.CAD para Java](/cad/java/cad-export-options/export-stl-to-png/)
- [Convertir DWG a PNG – Guardar CAD como PNG usando Aspose.CAD para Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)
- [Exportar DWG a PDF en Java – Establecer tamaño de página PDF con Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}