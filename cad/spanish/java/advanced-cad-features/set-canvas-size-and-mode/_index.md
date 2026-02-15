---
date: 2026-02-15
description: Aprenda cómo establecer el tamaño de página PDF y convertir CAD a PDF
  usando Aspose.CAD para Java, con escalado automático del diseño y exportación a
  TIFF.
linktitle: Set PDF Page Size – Convert CAD to PDF
second_title: Aspose.CAD Java API
title: Establecer tamaño de página PDF – Convertir CAD a PDF (Java)
url: /es/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Establecer tamaño del lienzo y modo

## Introducción

Si necesitas **establecer el tamaño de página PDF** al convertir dibujos CAD a PDF, has llegado al lugar correcto. En este tutorial te mostraremos cómo usar Aspose.CAD para Java para definir dimensiones exactas del lienzo, habilitar el escalado automático del diseño y luego exportar el resultado tanto a PDF como a TIFF. Ya sea que estés preparando esquemas de ingeniería para impresión o generando miniaturas para una galería web, controlar el tamaño de página y la resolución de salida es esencial.

## Respuestas rápidas
- **¿Qué significa “convertir CAD a PDF”?** Transformar un dibujo CAD (p. ej., DXF, DWG) en un documento PDF que puede visualizarse en cualquier plataforma.  
- **¿También puedo exportar a TIFF?** Sí—utiliza `TiffOptions` para crear imágenes raster de alta resolución.  
- **¿Qué opción controla el tamaño del lienzo en Java?** `CadRasterizationOptions.setPageWidth/Height`.  
- **¿Qué es el escalado automático del diseño?** Una bandera (`setAutomaticLayoutsScaling(true)`) que preserva las proporciones originales del diseño cuando cambia el tamaño del lienzo.  
- **¿Necesito una licencia para Aspose.CAD?** Se requiere una licencia temporal o permanente para uso en producción.

## Cómo establecer el tamaño de página PDF al convertir CAD a PDF (Java)

Establecer el tamaño de página PDF (o tamaño del lienzo) te permite dictar las dimensiones finales del documento, lo cual es especialmente útil cuando debes **cambiar las dimensiones del PDF** para que coincidan con estándares de impresión o requisitos de UI. A continuación, repasamos cada paso, explicando el *por qué* detrás de cada línea de código.

## ¿Qué es **convertir CAD a PDF**?

Convertir CAD a PDF significa tomar dibujos de ingeniería basados en vectores y renderizarlos como páginas PDF, preservando líneas, capas y geometría mientras se hace el archivo accesible universalmente.

## ¿Por qué establecer el tamaño del lienzo **java**?

Establecer el tamaño del lienzo en Java te permite definir la resolución de salida y las dimensiones de la página, asegurando que el PDF o TIFF resultante cumpla con tus requisitos de impresión o visualización. También te brinda control sobre el comportamiento de escalado, esencial para dibujos de gran formato.

## Requisitos previos

Antes de sumergirte en el tutorial, asegúrate de contar con los siguientes requisitos:

- Aspose.CAD para Java: Asegúrate de tener la biblioteca Aspose.CAD instalada en tu entorno Java. Puedes descargarla [aquí](https://releases.aspose.com/cad/java/).
- Directorio de documentos: Configura un directorio de documentos para almacenar tus archivos CAD. Este directorio será referenciado en los pasos del tutorial.

Ahora, comencemos con la guía paso a paso.

## Importar espacios de nombres

En este paso, importaremos los espacios de nombres necesarios para iniciar tu proyecto Aspose.CAD.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Paso 1: Importar clases de Aspose.CAD

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

En este fragmento, configuramos la ruta al directorio de recursos y cargamos un archivo DXF usando la clase `Image` de Aspose.CAD.

## Paso 2: Establecer propiedades de **CadRasterizationOptions** (establecer tamaño del lienzo java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Aquí, creamos una instancia de `CadRasterizationOptions` y configuramos propiedades como ancho de página, alto de página y **escalado automático del diseño**. Este es el núcleo de **configurar modo de lienzo** para tu conversión.

## Paso 3: Crear PdfOptions y establecer VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Ahora, creamos una instancia de `PdfOptions` y asignamos su propiedad `VectorRasterizationOptions` a la `CadRasterizationOptions` configurada previamente.

## Paso 4: Exportar a PDF (convertir cad a pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Finalmente, guardamos la imagen CAD en un archivo PDF usando las opciones especificadas, completando el proceso de **convertir CAD a PDF**.

## Paso 5: Crear TiffOptions y establecer VectorRasterizationOptions (exportar cad a tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

En este paso, configuramos una instancia de `TiffOptions` y establecemos su propiedad `VectorRasterizationOptions`.

## Paso 6: Exportar a TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Finalmente, guardamos la imagen CAD en un archivo TIFF usando las opciones especificadas, demostrando cómo **exportar CAD a TIFF** después de configurar el tamaño del lienzo.

## Problemas comunes y soluciones

| Problema | Causa | Solución |
|----------|-------|----------|
| El PDF de salida está en blanco | `setNoScaling(true)` deshabilita el renderizado para algunos dibujos | Elimina `setNoScaling(true)` o configúralo en `false`. |
| La resolución del TIFF se ve baja | Ancho/alto de página demasiado pequeño | Incrementa los valores de `setPageWidth` / `setPageHeight`. |
| El diseño se ve distorsionado | Escalado automático del diseño deshabilitado | Asegúrate de que `setAutomaticLayoutsScaling(true)` esté habilitado. |

## ¿Por qué ajustar el tamaño del lienzo y DPI?

Cambiar el tamaño del lienzo influye directamente en la resolución de rasterización de la salida. Si necesitas **incrementar la resolución del TIFF**, simplemente aumenta los valores de `setPageWidth` / `setPageHeight` o llama a `rasterizationOptions.setResolution(300)` antes de crear el `TiffOptions`. Esto te brinda imágenes raster de alta calidad adecuadas para impresión o inspección detallada.

## Preguntas frecuentes

### Q1: ¿Puedo usar Aspose.CAD para Java con otros frameworks de Java?

A1: Sí, Aspose.CAD está diseñado para integrarse sin problemas con varios frameworks de Java.

### Q2: ¿Existe una licencia temporal disponible para Aspose.CAD?

A2: Sí, puedes obtener una licencia temporal [aquí](https://purchase.aspose.com/temporary-license/).

### Q3: ¿Dónde puedo obtener soporte comunitario para Aspose.CAD?

A3: Visita el [foro de Aspose.CAD](https://forum.aspose.com/c/cad/19) para soporte y discusiones de la comunidad.

### Q4: ¿Puedo probar Aspose.CAD gratis?

A4: ¡Claro! Obtén una prueba gratuita [aquí](https://releases.aspose.com/).

### Q5: ¿Cómo compro Aspose.CAD para Java?

A5: Compra el producto [aquí](https://purchase.aspose.com/buy).

**Preguntas y respuestas adicionales**

**P: ¿El tamaño del lienzo afecta la calidad vectorial en el PDF?**  
R: No. El tamaño del lienzo controla las dimensiones de la página; los datos vectoriales siguen siendo independientes de la resolución, garantizando un renderizado nítido a cualquier nivel de zoom.

**P: ¿Puedo establecer un DPI diferente para la salida TIFF?**  
R: Sí. Ajusta `rasterizationOptions.setResolution(dpiValue)` antes de crear `TiffOptions`.

**P: ¿Cómo puedo **cambiar las dimensiones del PDF** para un PDF existente sin volver a renderizar el CAD?**  
R: Usa Aspose.PDF para cargar el PDF generado y llama a `pdf.getPages().setPageSize(PageSize.A4)` o a un tamaño personalizado.

**P: ¿Cuál es la mejor manera de **convertir dxf a pdf** manteniendo capas?**  
R: Mantén `setAutomaticLayoutsScaling(true)` y evita `setNoScaling(true)`; esto conserva la visibilidad de capas y la fidelidad del diseño.

## Conclusión

¡Felicidades! Has convertido con éxito **CAD a PDF** y **CAD a TIFF** mientras **establecías el tamaño del lienzo java**, habilitando **escalado automático del diseño**, y aprendiendo a **configurar modo de lienzo** para salidas de alta calidad. Este tutorial proporciona una base sólida para tus proyectos de conversión CAD. Explora más funciones y posibilidades en la [documentación de Aspose.CAD](https://reference.aspose.com/cad/java/).

---

**Última actualización:** 2026-02-15  
**Probado con:** Aspose.CAD para Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}