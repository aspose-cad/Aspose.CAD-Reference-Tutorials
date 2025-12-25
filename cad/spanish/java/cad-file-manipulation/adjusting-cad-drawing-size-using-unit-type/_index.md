---
date: 2025-12-25
description: Aprenda a exportar DWG a BMP usando Aspose.CAD para Java. Esta guía paso
  a paso muestra cómo ajustar el tamaño del dibujo CAD y convertir CAD a BMP de manera
  eficiente.
linktitle: Adjusting CAD Drawing Size Using Unit Type
second_title: Aspose.CAD Java API
title: Exportar DWG a BMP – Ajustar el tamaño del CAD usando el tipo de unidad (Java)
url: /es/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar DWG a BMP – Ajustar el Tamaño del Dibujo CAD Usando el Tipo de Unidad con Aspose.CAD para Java

## Introducción

Cuando necesitas **exportar DWG a BMP**, controlar el tamaño de salida y la unidad de medida es esencial para el procesamiento posterior o la impresión. En este tutorial aprenderás cómo ajustar el tamaño del dibujo CAD y convertir CAD a BMP con Aspose.CAD para Java, usando la propiedad `UnitType` para definir la unidad de medida. Los pasos se explican en lenguaje sencillo, para que puedas seguirlos incluso si eres nuevo en la biblioteca.

## Respuestas rápidas
- **¿Qué significa “exportar DWG a BMP”?** Convertir un dibujo DWG en una imagen raster BMP.  
- **¿Qué propiedad controla el tamaño de salida?** `CadRasterOptions.setUnitType()` establece la unidad (p. ej., centímetro).  
- **¿Necesito una licencia para ejecutar el código?** Una prueba gratuita funciona para evaluación; se requiere una licencia para producción.  
- **¿Puedo elegir otros diseños?** Sí, usa `setLayouts()` para especificar diseños de espacio modelo o papel.  
- **¿Qué formatos de salida son compatibles?** Además de BMP, puedes exportar a PNG, JPEG, TIFF, etc., cambiando la clase de opciones.

## ¿Qué es **exportar DWG a BMP**?

Exportar DWG a BMP significa rasterizar un archivo DWG basado en vectores en una imagen de mapa de bits (BMP). Esto es útil cuando necesitas una representación pixel‑perfecta para sistemas heredados, pipelines de procesamiento de imágenes o escenarios de visualización simples.

## ¿Por qué ajustar el tamaño del dibujo CAD con **Tipo de Unidad**?

Establecer el tipo de unidad te permite controlar las dimensiones físicas de la imagen exportada sin calcular manualmente factores de escala. Esto garantiza que el bitmap coincida con medidas del mundo real (p. ej., centímetros), lo cual es crucial para dibujos de ingeniería y documentación impresa.

## Requisitos previos

Antes de sumergirte en el tutorial, asegúrate de contar con los siguientes requisitos:

- **Entorno de desarrollo Java** – Un JDK funcional (8 o superior) y un IDE o herramienta de compilación (Maven/Gradle).  
- **Biblioteca Aspose.CAD para Java** – Descarga e integra la biblioteca Aspose.CAD en tu proyecto Java. Puedes obtener la biblioteca [aquí](https://releases.aspose.com/cad/java/).

## Importar espacios de nombres

En tu código Java, incluye los espacios de nombres necesarios para acceder a las funcionalidades de Aspose.CAD. Añade las siguientes importaciones:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Ahora, desglosaremos el proceso de ajustar el tamaño del dibujo CAD usando el tipo de unidad en pasos manejables:

## Paso 1: Definir el directorio de datos

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Establece la ruta del directorio donde se encuentran tus archivos CAD.

## Paso 2: Cargar el dibujo CAD

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

Carga el dibujo CAD usando la clase `Image` de Aspose.CAD.

## 3: Crear opciones BMP

```java
BmpOptions bmpOptions = new BmpOptions();
```

Instancia la clase `BmpOptions` para exportar el diseño CAD al formato BMP.

## Paso 4: Configurar opciones de rasterización

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

Crea una instancia de `CadRasterizationOptions` y asóciala con `BmpOptions` para la rasterización vectorial.

## Paso 5: Establecer el Tipo de Unidad

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Especifica el tipo de unidad deseado para el dibujo CAD. En este ejemplo, lo hemos configurado a **Centímetro**, lo que influye directamente en el tamaño de la imagen exportada cuando **ajustas el tamaño del dibujo CAD**.

## Paso 6: Establecer diseños

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Define los diseños que se considerarán durante la exportación. En este caso, hemos seleccionado el diseño **"Model"**, pero puedes cambiar a diseños de espacio papel si lo necesitas.

## Paso 7: Exportar a BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Finalmente, guarda el dibujo CAD modificado en formato BMP. Este paso completa el flujo de trabajo de **exportar DWG a BMP** mientras preserva los ajustes de tamaño que configuraste.

## Problemas comunes y soluciones

| Problema | Razón | Solución |
|----------|-------|----------|
| **La imagen de salida es demasiado pequeña** | No se estableció el tipo de unidad o se usó el predeterminado (píxel) | Llama a `setUnitType()` con la medida deseada (p. ej., `UnitType.Centimeter`). |
| **Se exportó el diseño incorrecto** | Error tipográfico en el nombre del diseño | Verifica los nombres de los diseños con un visor CAD; usa la cadena exacta en `setLayouts()`. |
| **Excepción de licencia** | Ejecutando sin una licencia válida en producción | Aplica una licencia temporal o permanente como se describe en las FAQ. |

## Preguntas frecuentes (extendidas)

**P: ¿Puedo usar Aspose.CAD para Java con otros lenguajes de programación?**  
R: Aspose.CAD se centra principalmente en Java, pero existen versiones disponibles para otros lenguajes como .NET.

**P: ¿Hay opciones de licencia para Aspose.CAD?**  
R: Sí, puedes explorar las opciones de licencia y adquirir Aspose.CAD [aquí](https://purchase.aspose.com/buy).

**P: ¿Existe una prueba gratuita disponible para Aspose.CAD?**  
R: Por supuesto, puedes acceder a una prueba gratuita [aquí](https://releases.aspose.com/).

**P: ¿Cómo puedo obtener soporte para Aspose.CAD para Java?**  
R: Visita el foro de Aspose.CAD [aquí](https://forum.aspose.com/c/cad/19) para obtener soporte integral.

**P: ¿Puedo obtener una licencia temporal para Aspose.CAD?**  
R: Sí, puedes adquirir una licencia temporal [aquí](https://purchase.aspose.com/temporary-license/).

---

**Última actualización:** 2025-12-25  
**Probado con:** Aspose.CAD para Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}