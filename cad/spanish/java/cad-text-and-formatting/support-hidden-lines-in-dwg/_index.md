---
date: 2026-01-02
description: Aprenda cómo exportar DWG a PDF, habilitar líneas ocultas y convertir
  DWG a PDF con Aspose.CAD para Java en este tutorial paso a paso.
linktitle: Export DWG as PDF with Hidden Lines Using Java
second_title: Aspose.CAD Java API
title: Exportar DWG como PDF con líneas ocultas – Aspose.CAD para Java
url: /es/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar DWG como PDF con Líneas Ocultas – Aspose.CAD para Java

## Introducción

En este tutorial aprenderás a **exportar DWG como PDF** mientras preservas las líneas ocultas usando Aspose.CAD para Java. Ya sea que necesites **convertir DWG a PDF**, generar una guía al estilo **tutorial de dwg a pdf**, o simplemente **guardar DWG como PDF** con soporte de líneas ocultas, te guiaremos paso a paso. Al final, tendrás una solución lista para usar que podrás integrar en cualquier proyecto Java.

## Respuestas Rápidas
- **¿Qué cubre este tutorial?** Habilitar el renderizado de líneas ocultas al exportar DWG a PDF con Aspose.CAD para Java.  
- **¿Qué operación principal se realiza?** `export dwg as pdf`.  
- **¿Necesito una licencia?** Una prueba gratuita funciona para pruebas; se requiere una licencia comercial para producción.  
- **¿Cuáles son los requisitos previos?** Entorno de desarrollo Java, la biblioteca Aspose.CAD para Java y archivos DWG.  
- **¿Cuánto tiempo lleva la implementación?** Aproximadamente 10‑15 minutos para una configuración básica.

## ¿Qué es “export dwg as pdf”?
Exportar un archivo DWG a PDF convierte el dibujo CAD basado en vectores a un formato de documento portátil, preservando capas, tipos de línea y el renderizado opcional de líneas ocultas. Esto facilita compartir diseños CAD con partes interesadas que pueden no disponer de software CAD.

## ¿Por qué habilitar líneas ocultas al exportar?
Las líneas ocultas proporcionan una representación visual más clara de modelos 3D complejos en una página 2‑D, asegurando que solo se enfatizan los bordes visibles. Esto mejora la legibilidad y a menudo se requiere para la documentación de ingeniería.

## Requisitos Previos

1. **Aspose.CAD for Java** – descarga la biblioteca desde el sitio oficial [aquí](https://releases.aspose.com/cad/java/).  
2. **Archivos DWG** – ten los dibujos DWG fuente almacenados en un directorio conocido.  
3. **Entorno de desarrollo Java** – JDK 8+ y tu IDE preferido (Eclipse, IntelliJ, etc.).  

Ahora que estás listo, sumerjámonos en el código.

## Importar Espacios de Nombres

Comienza importando las clases necesarias para trabajar con imágenes CAD y opciones de PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## Paso 1: Configura tu Proyecto

Crea un proyecto Java y agrega el JAR de Aspose.CAD a tu ruta de compilación. Luego define el directorio que contiene tus archivos DWG.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **Consejo profesional:** Usa una ruta absoluta o configura una ruta relativa basada en la carpeta de recursos de tu proyecto.

## Paso 2: Cargar el Archivo DWG

Carga el archivo DWG fuente en un objeto `CadImage` para poder manipularlo.

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## Paso 3: Configurar Opciones de Rasterización

Selecciona las capas que deseas incluir y establece el tamaño de página para que coincida con el dibujo original. Aquí es donde habilitamos el renderizado de líneas ocultas especificando el diseño.

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## Paso 4: Configurar Opciones de PDF

Indica a Aspose.CAD que rasterice los datos vectoriales en un PDF, usando el diseño “Model” para mantener las líneas ocultas ocultas.

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Paso 5: Guardar el Resultado

Finalmente, exporta el DWG como un archivo PDF. Las líneas ocultas se respetarán según el diseño que hayas configurado.

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **Error Común:** Olvidar establecer el diseño a `"Model"` hará que todas las líneas (incluidas las ocultas) aparezcan sólidas en el PDF.

## Conclusión

Ahora tienes un método completo y listo para producción para **exportar DWG como PDF** con soporte de líneas ocultas usando Aspose.CAD para Java. Este enfoque puede integrarse en herramientas de procesamiento por lotes, servicios web o aplicaciones de escritorio para automatizar la conversión de CAD a PDF.

## Preguntas Frecuentes

### Q1: ¿Puedo usar Aspose.CAD para Java con otros formatos de archivo CAD?
A1: Sí, Aspose.CAD admite varios formatos CAD como DWG, DXF, DWF y más.

### Q2: ¿Hay una prueba gratuita disponible para Aspose.CAD para Java?
A2: Sí, puedes encontrar la prueba gratuita [aquí](https://releases.aspose.com/).

### Q3: ¿Cómo obtengo soporte para Aspose.CAD para Java?
A3: Visita el foro de Aspose.CAD [aquí](https://forum.aspose.com/c/cad/19) para soporte comunitario.

### Q4: ¿Dónde puedo encontrar documentación detallada para Aspose.CAD para Java?
A4: Consulta la documentación [aquí](https://reference.aspose.com/cad/java/).

### Q5: ¿Puedo comprar una licencia temporal para Aspose.CAD para Java?
A5: Sí, puedes obtener una licencia temporal [aquí](https://purchase.aspose.com/temporary-license/).

### Q6: ¿Este método también funciona para convertir DWG a PDF en un entorno de servidor sin interfaz?
A6: Absolutamente. Dado que el código usa solo la API de Aspose.CAD, se ejecuta sin dependencias de UI, lo que lo hace ideal para la automatización del lado del servidor.

**Última actualización:** 2026-01-02  
**Probado con:** Aspose.CAD para Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}