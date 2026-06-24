---
date: 2026-02-17
description: Aprende cómo guardar DWG como JPEG en Java usando Aspose.CAD, agregar
  múltiples capas y ajustar las dimensiones del CAD para una conversión de imagen
  precisa.
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: Guardar DWG como JPEG con soporte de capas en Java
url: /es/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Guardar DWG como JPEG con soporte de capas en Java

## Introducción

En este tutorial descubrirás cómo **guardar DWG como JPEG** aprovechando al máximo el soporte de capas en Aspose.CAD para Java. Las capas te permiten aislar partes específicas de un dibujo, facilitando la exportación solo de lo que necesitas. Recorreremos cada paso, desde la configuración del entorno hasta la exportación de un JPEG que incluya únicamente las capas que elijas.

## Respuestas rápidas
- **¿Qué significa “guardar DWG como JPEG”?** Convierte un dibujo DWG (u otro CAD) en una imagen raster JPEG.  
- **¿Puedo incluir solo capas seleccionadas?** Sí – usa el método `setLayers` para especificar qué capas renderizar.  
- **¿Cómo cambio el tamaño de la imagen?** Ajusta `setPageWidth` y `setPageHeight` en `CadRasterizationOptions`.  
- **¿Es una solución solo para Java?** El ejemplo utiliza Aspose.CAD para Java, pero los mismos conceptos se aplican a otros lenguajes.  
- **¿Necesito una licencia?** Una prueba gratuita funciona para pruebas; se requiere una licencia comercial para producción.

## ¿Qué es “guardar DWG como JPEG”?
Guardar DWG como JPEG significa rasterizar un archivo CAD vectorial (DWG, DWF, DXF, etc.) en un bitmap JPEG estándar. Esto es útil cuando necesitas incrustar dibujos CAD en páginas web, correos electrónicos o informes que solo admiten imágenes raster.

## ¿Por qué usar conversión JPEG con conocimiento de capas?
- **Enfócate en los datos relevantes:** Exporta solo las capas que necesitas, reduciendo el tamaño del archivo y el desorden visual.  
- **Mantén la intención del diseño:** Las capas preservan la agrupación lógica de objetos, de modo que puedes reutilizar el mismo archivo fuente para diferentes salidas.  
- **Control total sobre dimensiones:** Al ajustar las opciones de rasterización puedes producir imágenes de alta resolución que coincidan con los requisitos de publicación.

## Requisitos previos

Antes de comenzar, asegúrate de contar con lo siguiente:

1. **Biblioteca Aspose.CAD para Java** – descárgala desde el [sitio web](https://releases.aspose.com/cad/java/). Sigue la guía de instalación para agregar los archivos JAR al classpath de tu proyecto.  
2. **Entorno de desarrollo Java** – un JDK reciente (8 o superior) instalado en tu máquina.

Ahora que estamos listos, exploremos el código necesario para **guardar DWG como JPEG** con renderizado selectivo de capas.

## Importar espacios de nombres

Comienza importando las clases de Aspose.CAD requeridas y las utilidades estándar de Java:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## Guía paso a paso

### Paso 1: Configurar rutas de archivo

Define dónde se encuentra el archivo DWF de origen y dónde se escribirá el JPEG de salida.

```java
String dataDir = "Your Document Directory" + "DWFDrawings/";
String srcFile = dataDir + "for_layers_test.dwf";
String outFile = dataDir + "for_layers_test.jpg";
```

### Paso 2: Cargar la imagen DWF

Utiliza el método `Image.load` de Aspose.CAD para leer el dibujo CAD.

```java
Image image = Image.load(srcFile);
```

### Paso 3: Configurar opciones de rasterización (Ajustar dimensiones CAD)

Crea una instancia de `CadRasterizationOptions` y establece el tamaño de salida deseado. Cambiar estos valores te permite **ajustar las dimensiones CAD** para el JPEG final.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Paso 4: Especificar capas (Agregar múltiples capas)

Si deseas renderizar más de una capa, simplemente agrega sus nombres a la lista. Aquí comenzamos con una sola capa llamada “LayerA”.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*Consejo profesional:* Para **agregar múltiples capas**, amplía la llamada `Arrays.asList`, por ejemplo, `Arrays.asList("LayerA", "LayerB", "LayerC")`. Esto te permite **seleccionar capas CAD específicas** para la conversión.

### Paso 5: Configurar opciones JPEG (Convertir imagen CAD en Java)

Vincula la configuración de rasterización al formato de salida JPEG.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Paso 6: Exportar a JPG (Guardar DWG como JPEG)

Finalmente, escribe la imagen en disco. Este paso **guarda el dibujo CAD como un archivo JPEG** que contiene solo las capas seleccionadas.

```java
image.save(outFile, jpegOptions);
```

Al seguir estos pasos has guardado con éxito **DWG como JPEG** mientras controlas qué capas aparecen y personalizas las dimensiones de la imagen.

## Cómo convertir DWF a JPEG con selección de capas

Aunque el ejemplo usa un origen DWF, la misma canalización de rasterización funciona para cualquier formato CAD compatible (DWG, DXF, DGN, etc.). Simplemente cambia la extensión del archivo en `srcFile` y la biblioteca manejará automáticamente la operación de **convertir DWF a JPEG** (u otro formato).

## Problemas comunes y soluciones

| Problema | Solución |
|----------|----------|
| **Las capas no aparecen** | Verifica que los nombres de capa coincidan exactamente con los almacenados en el archivo DWF (sensible a mayúsculas y minúsculas). |
| **La imagen de salida está en blanco** | Asegúrate de que `setPageWidth` y `setPageHeight` sean lo suficientemente grandes para las extensiones del dibujo. |
| **Excepción de licencia** | Usa una licencia de prueba para pruebas; obtén una licencia completa para entornos de producción. |

## Preguntas frecuentes

**P: ¿Puedo agregar múltiples capas a las opciones de rasterización?**  
R: Por supuesto. Amplía la `stringList` con nombres de capa adicionales, por ejemplo, `Arrays.asList("LayerA", "LayerB")`.

**P: ¿Aspose.CAD es compatible con otros formatos CAD?**  
R: Sí, admite DWG, DXF, DWF y muchos más formatos.

**P: ¿Cómo puedo cambiar las dimensiones de la imagen de salida?**  
R: Modifica `setPageWidth` y `setPageHeight` en la instancia de `CadRasterizationOptions`.

**P: ¿Dónde puedo comprar una licencia para Aspose.CAD?**  
R: Puedes explorar las opciones de licencia [aquí](https://purchase.aspose.com/buy).

**P: ¿Dónde puedo obtener soporte de la comunidad?**  
R: Únete a la comunidad de Aspose.CAD en el [foro](https://forum.aspose.com/c/cad/19) para asistencia y discusiones.

---

**Última actualización:** 2026-02-17  
**Probado con:** Aspose.CAD para Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}