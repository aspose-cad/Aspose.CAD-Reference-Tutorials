---
date: 2026-01-12
description: Aprenda cómo exportar CAD a PDF mientras anula la detección automática
  de la página de códigos en archivos DWG usando Aspose.CAD para Java. Maneja la codificación
  y los CIF/MIF malformados.
linktitle: Override Automatic Code Page Detection in DWG Files
second_title: Aspose.CAD Java API
title: Exportar CAD a PDF – Anular la detección automática de página de códigos en
  archivos DWG con Java
url: /es/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar CAD a PDF – Anular la detección automática de página de códigos en archivos DWG con Java

## Introducción

En esta guía completa descubrirás **cómo exportar CAD a PDF** mientras anulas la detección automática de la página de códigos que puede corromper el texto en archivos DWG. Aspose.CAD para Java te brinda un control detallado sobre la codificación, permitiéndote recuperar datos CIF/MIF mal formados y producir una salida PDF fiable. Ya sea que estés creando un conversor por lotes o integrando el procesamiento de CAD en una aplicación Java más grande, los pasos a continuación te guiarán a través de todo el flujo de trabajo.

## Respuestas rápidas
- **¿Qué significa “anular la página de códigos”?** Obliga a Aspose.CAD a usar una codificación de caracteres específica en lugar de adivinar.
- **¿Puedo exportar DWG directamente a PDF?** Sí – después de establecer la página de códigos correcta, puedes guardar la imagen CAD como PDF.
- **¿Qué codificación funciona para texto japonés?** `CodePages.Japanese` y `MifCodePages.Japanese` son las opciones correctas.
- **¿Necesito una licencia para uso en producción?** Se requiere una licencia comercial; una licencia temporal está disponible para pruebas.
- **¿Qué versión de Aspose.CAD se necesita?** Cualquier versión reciente que admita `LoadOptions` y `PdfOptions`.

## ¿Qué es “exportar CAD a PDF”?
Exportar CAD a PDF convierte dibujos CAD basados en vectores a un formato de documento de diseño fijo y ampliamente compatible. El PDF resultante preserva líneas, capas y texto, facilitando compartir, imprimir o incrustar el dibujo en otras aplicaciones.

## ¿Por qué anular la detección automática de la página de códigos?
Los archivos DWG a menudo almacenan texto usando páginas de códigos heredadas. La autodetección de Aspose.CAD puede interpretar mal esos bytes, provocando caracteres distorsionados. Al especificar manualmente la página de códigos aseguras que el texto aparezca exactamente como se pretende en el PDF exportado, especialmente para escrituras no latinas como japonés, cirílico o árabe.

## Requisitos previos
- **Entorno de desarrollo Java** – JDK 8+ y tu IDE favorito.
- **Aspose.CAD para Java** – Descarga la biblioteca desde el sitio oficial [here](https://releases.aspose.com/cad/java/).
- **Archivo de muestra DWG** – Usa el `SimpleEntities.dwg` proporcionado o cualquier DWG que necesites convertir.

## Importar paquetes
En tu proyecto Java, importa las clases necesarias de Aspose.CAD:

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## Guía paso a paso

### Paso 1: Configurar el proyecto Java
Crea un nuevo proyecto Maven o Gradle y agrega el JAR de Aspose.CAD al classpath. Este paso garantiza que el IDE pueda resolver las clases importadas.

### Paso 2: Cargar el archivo DWG con una página de códigos especificada
Indica a Aspose.CAD qué codificación usar y si debe intentar recuperar datos CIF/MIF mal formados.

```java
String SourceDir = "Your Document Directory";
String dwgPathToFile = SourceDir + "SimpleEntites.dwg";
LoadOptions opts = new LoadOptions();
opts.setSpecifiedEncoding(CodePages.Japanese);
opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
opts.setRecoverMalformedCifMif(false);
CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);
```

### Paso 3: Exportar la imagen CAD a PDF
Con la página de códigos correcta aplicada, puedes exportar el dibujo de forma segura. El objeto `PdfOptions` te permite afinar la salida PDF (compresión, rasterizado, etc.).

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### Paso 4: Verificar el éxito
Un mensaje simple en la consola confirma que el proceso se completó sin excepciones.

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

Puedes repetir estos pasos para varios archivos DWG, ajustando la ruta de origen y el nombre de salida según sea necesario.

## Problemas comunes y soluciones
- **Aún aparecen caracteres basura:** Verifica que `specifiedEncoding` coincida con la página de códigos original del DWG. Usa un enum `CodePages` diferente si es necesario.
- **`NullPointerException` en `cadImage.save`:** Asegúrate de que el archivo DWG se cargue correctamente; verifica la ruta y los permisos del archivo.
- **El tamaño del PDF es grande:** Habilita la compresión en `PdfOptions` (p. ej., `pdfOptions.setCompress(true)`).

## Preguntas frecuentes

**P1: ¿Aspose.CAD es compatible con todas las versiones de archivos DWG?**  
R1: Aspose.CAD admite una amplia gama de versiones DWG, incluidas AutoCAD 2018 y versiones anteriores.

**P2: ¿Puedo usar Aspose.CAD en proyectos comerciales?**  
R2: Sí, se requiere una licencia comercial para uso en producción. Puedes obtener una licencia [here](https://purchase.aspose.com/buy).

**P3: ¿Hay limitaciones en la versión de prueba gratuita?**  
R3: La prueba impone restricciones de tamaño y funcionalidades; consulta la documentación oficial para más detalles.

**P4: ¿Cómo puedo obtener soporte para Aspose.CAD?**  
R4: Visita la comunidad [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) para asistencia y discusiones.

**P5: ¿Existe una licencia temporal disponible para pruebas?**  
R5: Sí, puedes solicitar una licencia temporal [here](https://purchase.aspose.com/temporary-license/).

---

**Última actualización:** 2026-01-12  
**Probado con:** Aspose.CAD para Java 24.11 (última disponible al momento de escribir)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}