---
title: Ajustar el tamaño del dibujo CAD usando el tipo de unidad con Aspose.CAD para Java
linktitle: Ajustar el tamaño del dibujo CAD usando el tipo de unidad
second_title: API de Java Aspose.CAD
description: Explore el poder de Aspose.CAD para Java para ajustar los tamaños de los dibujos CAD sin esfuerzo. Siga nuestra guía paso a paso para obtener precisión y adaptabilidad.
type: docs
weight: 14
url: /es/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
---
## Introducción

En el ámbito en constante evolución del diseño asistido por computadora (CAD), la precisión y la adaptabilidad son primordiales. Un requisito común es ajustar el tamaño de los dibujos CAD según tipos de unidades específicas. Aspose.CAD para Java surge como un poderoso aliado, que proporciona capacidades perfectas para manipular archivos CAD mediante programación.

## Requisitos previos

Antes de sumergirse en el tutorial, asegúrese de cumplir con los siguientes requisitos previos:

- Entorno de desarrollo Java: asegúrese de tener un entorno de desarrollo Java funcional configurado en su máquina.

-  Biblioteca Aspose.CAD para Java: descargue e integre la biblioteca Aspose.CAD en su proyecto Java. Puedes obtener la biblioteca.[aquí](https://releases.aspose.com/cad/java/).

## Importar espacios de nombres

En su código Java, incluya los espacios de nombres necesarios para acceder a las funcionalidades de Aspose.CAD. Agregue las siguientes importaciones:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Ahora, analicemos el proceso de ajustar el tamaño del dibujo CAD utilizando el tipo de unidad en pasos manejables:

## Paso 1: definir el directorio de datos

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Establezca la ruta del directorio donde se encuentran sus archivos CAD.

## Paso 2: cargar el dibujo CAD

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

 Cargue el dibujo CAD usando Aspose.CAD.`Image` clase.

## Paso 3: crear opciones BMP

```java
BmpOptions bmpOptions = new BmpOptions();
```

 Instanciar el`BmpOptions` clase para exportar el diseño CAD al formato BMP.

## Paso 4: configurar las opciones de rasterización

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

 Crear una instancia de`CadRasterizationOptions` y asociarlo con el`BmpOptions` para rasterización vectorial.

## Paso 5: establecer el tipo de unidad

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Especifique el tipo de unidad deseada para el dibujo CAD. En este ejemplo, lo hemos configurado en Centímetro.

## Paso 6: establecer diseños

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Defina los diseños que se considerarán durante la exportación. En este caso, hemos seleccionado el diseño "Modelo".

## Paso 7: Exportar a BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Finalmente, guarde el dibujo CAD modificado en formato BMP.

## Conclusión

Con Aspose.CAD para Java, ajustar el tamaño de los dibujos CAD se vuelve muy sencillo. Este tutorial lo ha guiado a través del proceso, enfatizando la importancia de cada paso para lograr resultados precisos.

## Preguntas frecuentes

### P1: ¿Puedo utilizar Aspose.CAD para Java con otros lenguajes de programación?

R1: Aspose.CAD admite principalmente Java, pero hay versiones disponibles para otros lenguajes como .NET.

### P2: ¿Existen opciones de licencia para Aspose.CAD?

 R2: Sí, puede explorar opciones de licencia y comprar Aspose.CAD[aquí](https://purchase.aspose.com/buy).

### P3: ¿Hay una prueba gratuita disponible para Aspose.CAD?

 R3: Ciertamente, puedes acceder a una prueba gratuita.[aquí](https://releases.aspose.com/).

### P4: ¿Cómo puedo obtener soporte para Aspose.CAD para Java?

 A4: Visite el foro Aspose.CAD[aquí](https://forum.aspose.com/c/cad/19) para un soporte integral.

### P5: ¿Puedo obtener una licencia temporal para Aspose.CAD?

 R5: Sí, puedes adquirir una licencia temporal[aquí](https://purchase.aspose.com/temporary-license/).