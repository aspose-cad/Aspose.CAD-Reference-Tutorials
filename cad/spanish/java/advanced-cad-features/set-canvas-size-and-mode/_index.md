---
date: 2025-12-10
description: Aprenda a convertir CAD a PDF usando Aspose.CAD para Java mientras establece
  el tamaño del lienzo, el escalado automático del diseño y la exportación a TIFF.
linktitle: Convert CAD to PDF – Set Canvas Size & Mode
second_title: Aspose.CAD Java API
title: Convertir CAD a PDF – Establecer tamaño y modo del lienzo (Java)
url: /es/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Establecer tamaño del lienzo y modo

## Introducción

¿Está buscando **convert CAD to PDF** mientras tiene control total sobre el tamaño del lienzo y el modo de renderizado? Esta guía completa lo lleva paso a paso para establecer el tamaño del lienzo en Java, habilitar el escalado automático de diseño y luego exportar el resultado a formatos PDF y TIFF usando Aspose.CAD. Ya sea que esté perfeccionando una canalización de producción o experimentando con un prototipo, encontrará instrucciones claras y accionables aquí.

## Respuestas rápidas
- **¿Qué significa “convert CAD to PDF”?** Transformar un dibujo CAD (p. ej., DXF, DWG) en un documento PDF que puede verse en cualquier plataforma.  
- **¿Puedo también exportar a TIFF?** Sí—use `TiffOptions` para crear imágenes raster de alta resolución.  
- **¿Qué opción controla el tamaño del lienzo en Java?** `CadRasterizationOptions.setPageWidth/Height`.  
- **¿Qué es el escalado automático de diseño?** Una bandera (`setAutomaticLayoutsScaling(true)`) que preserva las proporciones originales del diseño cuando el tamaño del lienzo cambia.  
- **¿Necesito una licencia para Aspose.CAD?** Se requiere una licencia temporal o permanente para uso en producción.

## ¿Qué es **convert CAD to PDF**?

Convertir CAD a PDF significa tomar dibujos de ingeniería basados en vectores y renderizarlos como páginas PDF, preservando líneas, capas y geometría mientras se hace el archivo universalmente accesible.

## ¿Por qué establecer el tamaño del lienzo **java**?

Establecer el tamaño del lienzo en Java le permite definir la resolución de salida y las dimensiones de la página, asegurando que el PDF o TIFF resultante coincida con sus requisitos de impresión o visualización. También le brinda control sobre el comportamiento de escalado, lo cual es esencial para dibujos de gran formato.

## Requisitos previos

Antes de sumergirse en el tutorial, asegúrese de que tenga los siguientes requisitos previos preparados:

- Aspose.CAD para Java: Asegúrese de que tiene la biblioteca Aspose.CAD instalada en su entorno Java. Puede descargarla [aquí](https://releases.aspose.com/cad/java/).

- Directorio de documentos: Configure un directorio de documentos para almacenar sus archivos CAD. Este directorio será referenciado en los pasos del tutorial.

Ahora, comencemos con la guía paso a paso.

## Importar espacios de nombres

En este paso, importaremos los espacios de nombres necesarios para iniciar su proyecto Aspose.CAD.

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

## Paso 2: Establecer propiedades de **CadRasterizationOptions** (set canvas size java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Aquí, creamos una instancia de `CadRasterizationOptions` y configuramos propiedades como el ancho de página, la altura de página y el **automatic layout scaling**. Este es el núcleo de **configure canvas mode** para su conversión.

## Paso 3: Crear PdfOptions y establecer VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Ahora, creamos una instancia de `PdfOptions` y establecemos su propiedad `VectorRasterizationOptions` a la `CadRasterizationOptions` configurada previamente.

## Paso 4: Exportar a PDF (convert cad to pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Finalmente, guardamos la imagen CAD en un archivo PDF usando las opciones especificadas, completando el proceso de **convert CAD to PDF**.

## Paso 5: Crear TiffOptions y establecer VectorRasterizationOptions (export cad to tiff)

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

Finalmente, guardamos la imagen CAD en un archivo TIFF usando las opciones especificadas, demostrando cómo **export CAD to TIFF** después de configurar el tamaño del lienzo.

## Problemas comunes y soluciones

| Problema | Causa | Solución |
|----------|-------|----------|
| El PDF de salida está en blanco | `setNoScaling(true)` deshabilita el renderizado para algunos dibujos | Elimine `setNoScaling(true)` o configúrelo a `false`. |
| La resolución del TIFF parece baja | Ancho/alto de página demasiado pequeño | Aumente los valores de `setPageWidth` / `setPageHeight`. |
| El diseño se ve distorsionado | Escalado automático de diseño deshabilitado | Asegúrese de que `setAutomaticLayoutsScaling(true)` esté habilitado. |

## Conclusión

¡Felicidades! Ha convertido con éxito **convert CAD to PDF** y **export CAD to TIFF** mientras **set canvas size java**, habilitando **automatic layout scaling**, y aprendiendo a **configure canvas mode** para obtener resultados de alta calidad. Este tutorial brinda una base sólida para sus proyectos de conversión CAD. Explore más funciones y posibilidades en la [documentación de Aspose.CAD](https://reference.aspose.com/cad/java/).

## Preguntas frecuentes

### Q1: ¿Puedo usar Aspose.CAD para Java con otros frameworks de Java?

A1: Sí, Aspose.CAD está diseñado para integrarse sin problemas con varios frameworks de Java.

### Q2: ¿Está disponible una licencia temporal para Aspose.CAD?

A2: Sí, puede obtener una licencia temporal [aquí](https://purchase.aspose.com/temporary-license/).

### Q3: ¿Dónde puedo obtener soporte comunitario para Aspose.CAD?

A3: Visite el [foro de Aspose.CAD](https://forum.aspose.com/c/cad/19) para soporte y discusiones de la comunidad.

### Q4: ¿Puedo probar Aspose.CAD gratis?

A4: ¡Absolutamente! Obtenga una prueba gratuita [aquí](https://releases.aspose.com/).

### Q5: ¿Cómo compro Aspose.CAD para Java?

A5: Compre el producto [aquí](https://purchase.aspose.com/buy).

**Preguntas adicionales**

**P: ¿Afecta el tamaño del lienzo la calidad vectorial en el PDF?**  
R: No. El tamaño del lienzo controla las dimensiones de la página; los datos vectoriales siguen siendo independientes de la resolución, garantizando un renderizado nítido a cualquier nivel de zoom.

**P: ¿Puedo establecer un DPI diferente para la salida TIFF?**  
R: Sí. Ajuste `rasterizationOptions.setResolution(dpiValue)` antes de crear `TiffOptions`.

---

**Last Updated:** 2025-12-10  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}