---
date: 2026-05-20
description: Aprenda cómo convertir DWG a PDF mientras anula la detección automática
  de code page detection usando Aspose.CAD for Java. Incluye pasos para exportar dwg
  a pdf, consejos de encoding y troubleshooting.
keywords:
- convert dwg pdf
- export dwg to pdf
- Aspose.CAD Java
linktitle: Anular la detección automática de code page detection en archivos DWG
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to convert DWG to PDF while overriding automatic code page
    detection using Aspose.CAD for Java. Includes export dwg to pdf steps, encoding
    tips, and troubleshooting.
  headline: Convert DWG to PDF – Override Code Page Detection in Java
  type: TechArticle
- description: Learn how to convert DWG to PDF while overriding automatic code page
    detection using Aspose.CAD for Java. Includes export dwg to pdf steps, encoding
    tips, and troubleshooting.
  name: Convert DWG to PDF – Override Code Page Detection in Java
  steps:
  - name: Set Up the Java Project
    text: Create a Maven or Gradle project and add the Aspose.CAD JAR to the classpath.
      This ensures the IDE can resolve the imported classes and that the runtime can
      locate the library.
  - name: Load the DWG File with a Specified Code Page
    text: Tell Aspose.CAD which encoding to use and whether to attempt recovery of
      malformed CIF/MIF data.
  - name: Export the CAD Image to PDF
    text: With the correct code page applied, you can safely export the drawing. The
      `PdfOptions` object lets you fine‑tune the PDF output (compression, rasterization,
      etc.).
  - name: Verify Success
    text: A simple console message confirms that the process completed without exceptions.
      You can repeat these steps for multiple DWG files, adjusting the source path
      and output name as needed.
  type: HowTo
- questions:
  - answer: It forces Aspose.CAD to use a specific character encoding instead of guessing.
    question: What does “override code page” mean?
  - answer: Yes – after setting the correct code page, you can save the CAD image
      as PDF.
    question: Can I export DWG directly to PDF?
  - answer: '`CodePages.Japanese` and `MifCodePages.Japanese` are the right choices.'
    question: Which encoding works for Japanese text?
  - answer: A commercial license is required; a temporary license is available for
      testing.
    question: Do I need a license for production use?
  - answer: Any recent version that supports `LoadOptions` and `PdfOptions`.
    question: What version of Aspose.CAD is needed?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Convertir DWG a PDF – Anular la detección automática de code page detection
  en Java
url: /es/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir DWG a PDF – Anular la detección de página de códigos en Java

En este tutorial exhaustivo aprenderás **cómo convertir DWG a PDF** mientras anulas la detección automática de página de códigos que puede corromper el texto. Aspose.CAD para Java te brinda un control preciso sobre la codificación de caracteres, permitiéndote recuperar datos CIF/MIF malformados y generar una salida PDF confiable. Ya sea que estés construyendo un conversor por lotes o añadiendo procesamiento CAD a un servicio Java más grande, los pasos a continuación te guiarán a través de todo el flujo de trabajo, desde la configuración del proyecto hasta la verificación.

## Respuestas rápidas
- **¿Qué significa “override code page”?** Obliga a Aspose.CAD a usar una codificación de caracteres específica en lugar de adivinar.
- **¿Puedo exportar DWG directamente a PDF?** Sí, después de establecer la página de códigos correcta, puedes guardar la imagen CAD como PDF.
- **¿Qué codificación funciona para texto japonés?** `CodePages.Japanese` y `MifCodePages.Japanese` son las opciones correctas.
- **¿Necesito una licencia para uso en producción?** Se requiere una licencia comercial; una licencia temporal está disponible para pruebas.
- **¿Qué versión de Aspose.CAD se necesita?** Cualquier versión reciente que admita `LoadOptions` y `PdfOptions`.

## Qué es “export CAD to PDF”
Exportar CAD a PDF transforma un dibujo DWG basado en vectores en un documento PDF de diseño fijo y universalmente visible. La conversión conserva todas las entidades geométricas, líneas, capas y texto incrustado, a la vez que aplana el dibujo en un formato que puede compartirse, imprimirse, archivarse o incrustarse en otras aplicaciones sin requerir software CAD.

## Por qué anular la detección automática de página de códigos
Especificar manualmente la página de códigos garantiza que los bytes de texto se interpreten correctamente, eliminando los caracteres distorsionados que a menudo aparecen cuando la detección automática de Aspose.CAD adivina una codificación heredada incorrecta. Esto es esencial para scripts no latinos como japonés, cirílico o árabe, y asegura que el PDF exportado coincida con el diseño original.

## Requisitos previos
- **Entorno de desarrollo Java** – JDK 8+ y tu IDE preferido.  
- **Aspose.CAD para Java** – Descarga la biblioteca desde el sitio oficial [here](https://releases.aspose.com/cad/java/).  
- **Archivo de muestra DWG** – Usa el `SimpleEntities.dwg` proporcionado o cualquier DWG que necesites convertir.

## Importar paquetes
Las clases `Document`, `LoadOptions` y `PdfOptions` son el núcleo del proceso de conversión.

La clase `Document` representa un dibujo CAD en memoria, proporcionando métodos para cargar, manipular y guardar el archivo en varios formatos.  
La clase `LoadOptions` te permite especificar la página de códigos y opciones de recuperación al cargar un archivo DWG.  
La clase `PdfOptions` controla configuraciones específicas de PDF como compresión, rasterización y metadatos.

En tu proyecto Java, importa las clases necesarias de Aspose.CAD:

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## Cómo convertir DWG a PDF con anulación de página de códigos
Carga el archivo DWG usando `LoadOptions` para especificar la página de códigos exacta, luego invoca el método `save` en el `CadImage` resultante con una instancia configurada de `PdfOptions`. Este enfoque de dos pasos asegura que el texto se interprete correctamente y que el PDF generado preserve la fidelidad, capas y calidad vectorial del dibujo original.

### Paso 1: Configurar el proyecto Java
Crea un proyecto Maven o Gradle y agrega el JAR de Aspose.CAD al classpath. Esto permite que el IDE resuelva las clases importadas y que el tiempo de ejecución localice la biblioteca.

### Paso 2: Cargar el archivo DWG con una página de códigos especificada
Indica a Aspose.CAD qué codificación usar y si debe intentar recuperar datos CIF/MIF malformados.

```java
String SourceDir = "Your Document Directory";
String dwgPathToFile = SourceDir + "SimpleEntites.dwg";
LoadOptions opts = new LoadOptions();
opts.setSpecifiedEncoding(CodePages.Japanese);
opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
opts.setRecoverMalformedCifMif(false);
CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);
```

### Paso 3: Exportar la imagen CAD a PDF
Con la página de códigos correcta aplicada, puedes exportar el dibujo de forma segura. El objeto `PdfOptions` te permite afinar la salida PDF (compresión, rasterización, etc.).

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### Paso 4: Verificar el éxito
Un simple mensaje en la consola confirma que el proceso se completó sin excepciones.

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

Puedes repetir estos pasos para varios archivos DWG, ajustando la ruta de origen y el nombre de salida según sea necesario.

## Problemas comunes y soluciones
- **Los caracteres basura siguen apareciendo:** Verifica que `specifiedEncoding` coincida con la página de códigos original del DWG. Usa un enum `CodePages` diferente si es necesario.  
- **`NullPointerException` en `cadImage.save`:** Asegúrate de que el archivo DWG se cargue correctamente; verifica la ruta y los permisos del archivo.  
- **El tamaño del PDF es grande:** Habilita la compresión en `PdfOptions` (p. ej., `pdfOptions.setCompress(true)`) para reducir el tamaño del archivo sin perder calidad.

## Preguntas frecuentes

**Q1: ¿Es Aspose.CAD compatible con todas las versiones de archivos DWG?**  
A1: Aspose.CAD admite más de 30 versiones de DWG, incluidas AutoCAD 2018 y versiones anteriores.

**Q2: ¿Puedo usar Aspose.CAD para proyectos comerciales?**  
A2: Sí, se requiere una licencia comercial para uso en producción. Puedes obtener una licencia [here](https://purchase.aspose.com/buy).

**Q3: ¿Hay limitaciones en la versión de prueba gratuita?**  
A1: La prueba impone restricciones de tamaño y funcionalidades; consulta la documentación oficial para más detalles.

**Q4: ¿Cómo puedo obtener soporte para Aspose.CAD?**  
A4: Visita la comunidad [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) para asistencia y discusiones.

**Q5: ¿Existe una licencia temporal disponible para propósitos de prueba?**  
A5: Sí, se puede solicitar una licencia temporal [here](https://purchase.aspose.com/temporary-license/).

---

**Última actualización:** 2026-05-20  
**Probado con:** Aspose.CAD para Java 24.11 (última disponible al momento de escribir)  
**Autor:** Aspose

## Tutoriales relacionados

- [Exportar DWG a PDF y convertir dibujos CAD – Tutorial Aspose.CAD Java](/cad/java/cad-drawing-conversion/)
- [Exportar diseño DWG específico a PDF usando Aspose.CAD para Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Exportar DWG a PDF o raster usando Aspose.CAD para Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}