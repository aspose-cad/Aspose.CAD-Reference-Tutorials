---
date: 2025-12-28
description: 'Aprenda a crear PDF a partir de DWG, guardar DWG como PDF y agregar
  texto a los dibujos DWG con Aspose.CAD para Java: guía paso a paso.'
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: Crear PDF a partir de DWG y agregar texto usando Aspose.CAD para Java
url: /es/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crear PDF a partir de DWG y agregar texto usando Aspose.CAD para Java

## Introducción

Si necesitas **crear PDF a partir de archivos DWG** mientras insertas texto personalizado, estás en el lugar correcto. En este tutorial recorreremos todo el proceso: cargar un dibujo DWG, agregar una anotación de texto y, finalmente, guardar el resultado como PDF usando Aspose.CAD para Java. Al final comprenderás cómo **guardar DWG como PDF**, personalizar la altura del texto y añadir anotaciones básicas.

## Respuestas rápidas
- **¿Puedo convertir DWG a PDF en Java?** Sí, Aspose.CAD para Java ofrece una API sencilla.  
- **¿Necesito una licencia para uso en producción?** Se requiere una licencia comercial; hay una versión de prueba gratuita.  
- **¿Qué método agrega texto a un DWG?** Usa el objeto `CadText` y añádelo al espacio del modelo.  
- **¿Puedo establecer la altura del texto?** Por supuesto—utiliza `setTextHeight()` en la instancia de `CadText`.  
- **¿La salida es vectorial?** Cuando las opciones de rasterización se configuran en `UseObjectColor`, el PDF conserva datos vectoriales de alta calidad.

## Requisitos previos

Antes de sumergirte en el tutorial, asegúrate de contar con los siguientes requisitos:

- Biblioteca Aspose.CAD para Java: Descarga e instala la biblioteca desde la [página de Aspose.CAD para Java](https://releases.aspose.com/cad/java/).

- Java Development Kit (JDK): Asegúrate de tener la última versión del JDK instalada en tu sistema.

- Dibujo DWG: Prepara un archivo de dibujo DWG al que desees agregar texto.

## Importar espacios de nombres

En tu código Java, importa los espacios de nombres necesarios para Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Ahora, desglosaremos el fragmento de código proporcionado en varios pasos:

## Paso 1: Configurar el directorio del documento y la ruta del archivo DWG

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## Paso 2: Cargar la imagen DWG

```java
Image image = Image.load(dwgPathToFile);
```

## Paso 3: Crear el objeto CadText (Agregar texto al DWG)

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);          // set text height in DWG units
cadText.setScaleX(0);
```

## Paso 4: Añadir texto a CadImage (Insertar anotación)

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## Paso 5: Configurar las opciones de PDF (Preparar la creación de PDF a partir de DWG)

```java
PdfOptions pdfOptions = new PdfOptions();
```

## Paso 6: Configurar CadRasterizationOptions (Controlar la renderización del PDF)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## Paso 7: Guardar el DWG modificado como PDF (dwg to pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

Siguiendo estos pasos, podrás **crear PDF a partir de DWG**, agregar texto personalizado y controlar la altura del texto, todo con unas pocas líneas de código Java.

## ¿Por qué agregar texto a DWG y convertir a PDF?

Agregar texto directamente a un archivo DWG es útil para:

- **Marcar diseños** con notas o números de pieza.  
- **Crear documentación imprimible** donde el PDF sirve como un formato de solo lectura y ampliamente compatible.  
- **Automatizar el procesamiento por lotes** de grandes bibliotecas CAD sin edición manual.

## Problemas comunes y consejos

- **¿El texto no aparece?** Verifica que las coordenadas X/Y estén dentro de los límites del dibujo y que la capa sea visible.  
- **¿Altura de texto incorrecta?** Ajusta `setTextHeight()`; el valor está en el sistema de unidades del dibujo.  
- **¿El PDF parece rasterizado?** Asegúrate de que `CadDrawTypeMode.UseObjectColor` esté configurado para mantener la información vectorial.  
- **¿Rendimiento en archivos grandes?** Incrementa `pageHeight`/`pageWidth` solo cuando sea necesario; valores mayores consumen más memoria.

## Preguntas frecuentes

**P: ¿Aspose.CAD es compatible con todas las versiones de archivos DWG?**  
R: Aspose.CAD admite diversas versiones de archivos DWG, garantizando compatibilidad con una amplia gama de software CAD.

**P: ¿Puedo personalizar la fuente y el formato del texto agregado?**  
R: Sí, puedes personalizar la fuente, estilo y otras opciones de formato del texto añadido a los archivos DWG usando Aspose.CAD.

**P: ¿Existe una versión de prueba gratuita para Aspose.CAD para Java?**  
R: Sí, puedes explorar las funciones de Aspose.CAD obteniendo una prueba gratuita [aquí](https://releases.aspose.com/).

**P: ¿Dónde puedo encontrar documentación detallada para Aspose.CAD para Java?**  
R: Consulta la documentación [aquí](https://reference.aspose.com/cad/java/) para obtener información profunda y ejemplos.

**P: ¿Cómo puedo obtener soporte o ayuda con Aspose.CAD?**  
R: Visita el [foro de Aspose.CAD](https://forum.aspose.com/c/cad/19) para recibir asistencia y conectar con la comunidad.

---

**Última actualización:** 2025-12-28  
**Probado con:** Aspose.CAD para Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}