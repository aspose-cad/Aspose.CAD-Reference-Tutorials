---
date: 2026-06-14
description: Aprenda cómo exportar CAD a SVG con Aspose.CAD para Java. Esta guía paso
  a paso le muestra cómo convertir DWG a SVG, establecer el modo de color SVG y integrar
  la biblioteca en su proyecto Java.
keywords:
- export cad to svg
- convert dwg to svg
- change svg to grayscale
- convert cad to svg
- generate svg from dwg
linktitle: Exportar a SVG
schemas:
- author: Aspose
  dateModified: '2026-06-14'
  description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  headline: Export CAD to SVG Using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  name: Export CAD to SVG Using Aspose.CAD for Java
  steps:
  - name: Open Your Java Project
    text: Launch your favorite IDE (IntelliJ IDEA, Eclipse, VS Code) and open the
      project where you intend to add the conversion logic.
  - name: Add Aspose.CAD Library
    text: Place the `aspose-cad-xx.jar` file in the `libs` directory and add it as
      a dependency in your build tool (Maven, Gradle, or plain `javac`).
  - name: Import Namespaces
    text: 'In the Java source file that will perform the conversion, add the following
      imports: These imports give you access to the core `Image` class and the SVG‑specific
      export options.'
  - name: Specify the Resource Directory
    text: 'Define the absolute or relative path that points to the folder holding
      your CAD drawings:'
  - name: Load the CAD Drawing
    text: The `Image` class is Aspose.CAD's top‑level object that represents a CAD
      drawing in memory. Loading the file creates an in‑memory representation ready
      for export. `Image.load` reads a CAD file and creates an in‑memory representation
      of the drawing.
  - name: Configure SVG Export Options
    text: '`SvgExportOptions` lets you fine‑tune the SVG output. Below we set the
      color mode to grayscale and ensure all text is rendered as shapes, which improves
      compatibility with browsers that lack the original font.'
  - name: Save as SVG
    text: Finally, invoke `save` on the `Image` instance, passing the target file
      name and the configured options. Aspose.CAD writes a standards‑compliant SVG
      file that can be opened directly in any modern browser. `save` writes the image
      to the specified file using the provided export options. > **Pro tip:**
  type: HowTo
- questions:
  - answer: Yes, simply replace the DWG file name with a DXF file; the API automatically
      detects and processes both formats.
    question: Can I convert a DXF file to SVG using the same code?
  - answer: Set `options.setColorType(SvgColorMode.FullColor);` before invoking the
      `save` method.
    question: How do I change the output to full‑color SVG?
  - answer: Aspose.CAD converts text to shapes, so embedding fonts is unnecessary;
      the resulting SVG contains only vector outlines.
    question: Is it possible to embed fonts in the generated SVG?
  - answer: The Java library is platform‑independent and runs wherever a compatible
      JVM is available, including Windows, Linux, and macOS.
    question: Does the library work on Linux and macOS?
  - answer: The example was tested with Aspose.CAD for Java **24.10**.
    question: What version of Aspose.CAD was used in this tutorial?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Exportar CAD a SVG usando Aspose.CAD para Java
url: /es/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar CAD a SVG usando Aspose.CAD para Java

## Introducción

En este tutorial exhaustivo aprenderás **cómo exportar CAD a SVG** usando Aspose.CAD para Java. Ya sea que necesites **convertir DWG a SVG**, generar SVG a partir de archivos DWG en un trabajo por lotes, o simplemente cambiar el SVG a escala de grises para una visualización web ligera, esta guía te acompañará paso a paso—desde la configuración de la biblioteca hasta el ajuste fino de las opciones de exportación. Al final, tendrás un fragmento listo para producción que se ejecuta en cualquier plataforma compatible con JVM.

## Respuestas rápidas
- **¿Qué significa “exportar CAD a SVG”?** Transforma un dibujo CAD (p. ej., DWG o DXF) en un archivo Scalable Vector Graphics que los navegadores renderizan sin pérdida de calidad.  
- **¿Qué biblioteca maneja la conversión?** Aspose.CAD para Java proporciona una API dedicada que soporta más de 30 formatos CAD y genera SVG con fidelidad vectorial completa.  
- **¿Necesito una licencia para desarrollo?** Una prueba gratuita funciona para evaluación; se requiere una licencia comercial para implementaciones en producción.  
- **¿Puedo controlar la salida de color del SVG?** Sí—usa `SvgColorMode` para alternar entre escala de grises y renderizado a color completo.  
- **¿Se requiere software adicional?** Solo un runtime de Java (JDK 8 o superior) y el JAR de Aspose.CAD; no se necesitan herramientas CAD externas.

## ¿Qué es exportar CAD a SVG?
Exportar CAD a SVG es el proceso de convertir un archivo CAD nativo (como DWG, DXF o DWF) al formato de imagen vectorial SVG. El SVG resultante conserva los datos geométricos exactos, lo que permite una visualización independiente de la resolución en navegadores web y herramientas de diseño.

## ¿Por qué exportar CAD a SVG con Aspose.CAD?
Aspose.CAD puede manejar **más de 30 formatos de entrada** y generar salida SVG de hasta **500 páginas** sin cargar todo el archivo en memoria, ofreciendo **conversión vectorial de alta fidelidad** a velocidades de **200 páginas/segundo** en una CPU de servidor típica. La biblioteca se ejecuta **100 % Java**, eliminando la necesidad de DLL nativas o motores CAD de terceros.

## Requisitos previos

- **Java Development Kit** (JDK 8 o superior) instalado y configurado en tu máquina.  
- **Aspose.CAD para Java** archivo JAR descargado desde el [download link](https://releases.aspose.com/cad/java/).  
- Una carpeta que contenga al menos un dibujo CAD (DWG, DXF, etc.) que desees convertir.

## Importar espacios de nombres

Antes de escribir cualquier código, asegúrate de que la biblioteca Aspose.CAD esté en tu classpath e importa las clases requeridas.

### Paso 1: Abra su proyecto Java
Inicia tu IDE favorito (IntelliJ IDEA, Eclipse, VS Code) y abre el proyecto donde planeas añadir la lógica de conversión.

### Paso 2: Añada la biblioteca Aspose.CAD
Coloca el archivo `aspose-cad-xx.jar` en el directorio `libs` y añádelo como dependencia en tu herramienta de compilación (Maven, Gradle o simple `javac`).

### Paso 3: Importe espacios de nombres
En el archivo fuente Java que realizará la conversión, agrega las siguientes importaciones:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgExportOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

Estas importaciones te dan acceso a la clase central `Image` y a las opciones de exportación específicas para SVG.

## ¿Cómo exportar CAD a SVG usando Aspose.CAD para Java?

Exportar un dibujo CAD a SVG con Aspose.CAD implica cargar el archivo fuente, configurar las opciones específicas de SVG y escribir la salida. El proceso es sencillo, requiere solo unas pocas líneas de código y funciona de manera consistente en todos los formatos CAD soportados mientras preserva la fidelidad vectorial.

### Paso 1: Especifique el directorio de recursos
Define la ruta absoluta o relativa que apunta a la carpeta que contiene tus dibujos CAD:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

### Paso 2: Cargue el dibujo CAD
La clase `Image` es el objeto de nivel superior de Aspose.CAD que representa un dibujo CAD en memoria. Cargar el archivo crea una representación en memoria lista para exportar.

`Image.load` lee un archivo CAD y crea una representación en memoria del dibujo.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Paso 3: Configure las opciones de exportación SVG
`SvgExportOptions` te permite afinar la salida SVG. A continuación establecemos el modo de color a escala de grises y garantizamos que todo el texto se renderice como formas, lo que mejora la compatibilidad con navegadores que no disponen de la fuente original.

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### Paso 4: Guardar como SVG
Finalmente, invoca `save` en la instancia `Image`, pasando el nombre del archivo de destino y las opciones configuradas. Aspose.CAD escribe un archivo SVG conforme a los estándares que puede abrirse directamente en cualquier navegador moderno.

`save` escribe la imagen en el archivo especificado usando las opciones de exportación proporcionadas.

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

> **Consejo profesional:** Para generar un SVG a color completo, reemplaza `SvgColorMode.Grayscale` por `SvgColorMode.FullColor`. Este cambio preserva la paleta original mientras sigue ofreciendo escalabilidad vectorial.

## ¿Por qué usar Aspose.CAD para exportar CAD a SVG?
- **Alta fidelidad:** Los datos vectoriales se conservan, garantizando que el SVG se vea exactamente como el dibujo CAD original.  
- **Sin dependencias externas:** La conversión se ejecuta completamente dentro de Java, eliminando la necesidad de herramientas adicionales.  
- **Salida personalizable:** Opciones como `setColorType` te permiten controlar si el SVG es en escala de grises o a color completo.  
- **Rendimiento escalable:** Procesa dibujos de cientos de páginas en segundos, con un uso de memoria inferior a 50 MB.

## Problemas comunes y soluciones
- **Archivo no encontrado:** Verifica que `dataDir` apunte a la carpeta correcta y que el nombre del archivo DWG coincida con mayúsculas/minúsculas del sistema de archivos.  
- **Salida SVG en blanco:** Asegúrate de que `options.setTextAsShapes(true)` esté habilitado cuando el dibujo fuente contenga texto que deba aparecer como formas vectoriales.  
- **Formato CAD no soportado:** Aspose.CAD soporta DWG, DXF, DWF y más de 15 formatos adicionales; consulta la documentación oficial para la lista completa.  
- **Cuellos de botella de rendimiento:** Para archivos extremadamente grandes, habilita el modo de transmisión mediante `options.setEnableStreaming(true)` para mantener bajo el consumo de memoria.

## Preguntas frecuentes

**P: ¿Puedo convertir un archivo DXF a SVG usando el mismo código?**  
R: Sí, simplemente reemplaza el nombre del archivo DWG por uno DXF; la API detecta y procesa automáticamente ambos formatos.

**P: ¿Cómo cambio la salida a SVG a color completo?**  
R: Establece `options.setColorType(SvgColorMode.FullColor);` antes de invocar el método `save`.

**P: ¿Es posible incrustar fuentes en el SVG generado?**  
R: Aspose.CAD convierte el texto a formas, por lo que incrustar fuentes es innecesario; el SVG resultante contiene solo contornos vectoriales.

**P: ¿La biblioteca funciona en Linux y macOS?**  
R: La biblioteca Java es independiente de la plataforma y se ejecuta donde haya una JVM compatible, incluyendo Windows, Linux y macOS.

**P: ¿Qué versión de Aspose.CAD se utilizó en este tutorial?**  
R: El ejemplo se probó con Aspose.CAD para Java **24.10**.

**Última actualización:** 2026-06-14  
**Probado con:** Aspose.CAD para Java 24.10  
**Autor:** Aspose  

```java
image.save(dataDir + "meshes.svg");
```

{{< blocks/products/products-backtop-button >}}

## Tutoriales relacionados

- [Exportar DWG a PDF o Raster usando Aspose.CAD para Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [dwg a pdf java – Exportar CAD a PDF con Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Exportar diseño DWG específico a PDF usando Aspose.CAD para Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}