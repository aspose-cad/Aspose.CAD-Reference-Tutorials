---
date: 2026-01-04
description: Aprende a **guardar CAD como PNG** y exporta sin esfuerzo objetos OLE
  de archivos CAD usando Aspose.CAD para Java. Configuración rápida, ejemplo de código
  completo y consejos de buenas prácticas.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: Guardar CAD como PNG y exportar objetos OLE con Aspose.CAD para Java
url: /es/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Guardar CAD como PNG y Exportar Objetos OLE con Aspose.CAD para Java

## Introducción

En el mundo de rápido movimiento del Diseño Asistido por Computadora (CAD), poder **guardar CAD como PNG** mientras se extraen los objetos OLE (Object Linking and Embedding) incrustados puede simplificar drásticamente tu flujo de trabajo. Ya sea que estés creando una herramienta de conversión por lotes, generando miniaturas para un portal web, o simplemente necesites archivar contenido OLE, Aspose.CAD para Java te ofrece una forma limpia y programática de hacerlo. En este tutorial recorreremos todo el proceso, desde la configuración del proyecto hasta la exportación de cada objeto OLE como una imagen PNG.

## Respuestas rápidas
- **¿Puedo exportar objetos OLE directamente a PNG?** Sí – Aspose.CAD carga el archivo CAD y te permite rasterizar cada diseño a PNG.  
- **¿Qué versión de Java se requiere?** Java 8 o posterior.  
- **¿Necesito una licencia para esta función?** Una prueba gratuita sirve para evaluación; se requiere una licencia para producción.  
- **¿Se conservarán los datos vectoriales?** La rasterización a PNG mantiene la fidelidad visual, pero la salida es raster, no vectorial.  
- **¿Se admite el procesamiento por lotes?** Absolutamente – itera sobre un arreglo de archivos como se muestra en el ejemplo de código.

## Requisitos previos

Antes de comenzar, asegúrate de contar con lo siguiente:

- **Java Development Kit (JDK)** – Java 8+ instalado y configurado.  
- **Aspose.CAD para Java** – Descarga la última biblioteca desde el [download link](https://releases.aspose.com/cad/java/).  
- **Archivos fuente CAD** – Cualquier archivo DWG/DXF/DGN que contenga objetos OLE que desees exportar.

## Importar espacios de nombres

Para trabajar con archivos CAD necesitas importar las clases principales de Aspose.CAD. Mantén el bloque de importación exactamente como se muestra – proporciona las clases que se usarán más adelante en el tutorial.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Cómo guardar CAD como PNG

A continuación tienes una guía concisa, paso a paso, que muestra **cómo exportar objetos OLE y guardar CAD como PNG**. Cada paso incluye una breve explicación seguida del código exacto que debes copiar a tu proyecto.

### Paso 1: Establecer el directorio de documentos

Define la carpeta que contiene tus dibujos CAD. Reemplaza el marcador de posición con la ruta real en tu máquina.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Paso 2: Definir los nombres de archivo CAD

Enumera cada archivo CAD que deseas procesar. Puedes añadir tantas entradas como necesites.

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Paso 3: Configurar las opciones de exportación PNG

Configura los ajustes de rasterización. Aquí apuntamos a un diseño específico (`Layout1`) y usamos las opciones PNG predeterminadas.

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

### Paso 4: Iterar a través de los archivos CAD y guardar como PNG

Carga cada archivo CAD, rasteriza los objetos OLE y escribe el archivo PNG de salida. El sufijo `_out.png` te ayuda a identificar las imágenes generadas.

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

## Problemas comunes y soluciones

| Problema | Por qué ocurre | Solución |
|----------|----------------|----------|
| **`Image.load` lanza `FileNotFoundException`** | La ruta `dataDir` es incorrecta o el nombre del archivo tiene un error tipográfico. | Verifica la cadena del directorio y asegura que los nombres de archivo coincidan exactamente, incluidos los espacios. |
| **El PNG de salida está en blanco** | El nombre del diseño no existe en el archivo CAD de origen. | Usa `cadImage.getLayouts()` para listar los diseños disponibles y luego actualiza `rasterizationOptions.setLayouts(...)`. |
| **Archivos CAD grandes provocan OutOfMemoryError** | Rasterizar imágenes de alta resolución consume mucha memoria del heap. | Incrementa el heap de la JVM (`-Xmx2g`) o reduce la resolución de rasterización mediante `rasterizationOptions.setResolution(...)`. |

## Preguntas frecuentes

### Q1: ¿Aspose.CAD es compatible con todos los formatos de archivo CAD?

A1: Aspose.CAD soporta varios formatos CAD, incluidos DWG, DXF y DGN. Consulta la [documentation](https://reference.aspose.com/cad/java/) para la lista completa.

### Q2: ¿Puedo personalizar la configuración de exportación para objetos OLE?

A2: Sí, Aspose.CAD ofrece amplias opciones para personalizar la configuración de exportación, permitiéndote adaptar la salida a tus requisitos específicos.

### Q3: ¿Existe una prueba gratuita disponible para Aspose.CAD?

A3: Sí, puedes explorar las capacidades de Aspose.CAD obteniendo una prueba gratuita [here](https://releases.aspose.com/).

### Q4: ¿Dónde puedo obtener soporte comunitario para Aspose.CAD?

A4: Únete a la comunidad de Aspose.CAD en el [forum](https://forum.aspose.com/c/cad/19) para solicitar ayuda y compartir tus experiencias.

### Q5: ¿Cómo puedo comprar una licencia para Aspose.CAD?

A5: Visita la [purchase page](https://purchase.aspose.com/buy) para adquirir una licencia que se ajuste a tus necesidades de desarrollo.

## Conclusión

Siguiendo estos cinco simples pasos puedes **guardar CAD como PNG** y extraer cada objeto OLE incrustado con solo unas pocas líneas de código Java. Este enfoque es ideal para conversiones por lotes, generación de informes automatizados o cualquier escenario donde necesites imágenes raster de contenido CAD sin exportaciones manuales. Siéntete libre de experimentar con diferentes opciones de rasterización para ajustar la calidad y el rendimiento a tus requerimientos.

---

**Última actualización:** 2026-01-04  
**Probado con:** Aspose.CAD para Java 24.12 (última versión al momento de escribir)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}