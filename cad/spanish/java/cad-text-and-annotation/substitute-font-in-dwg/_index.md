---
date: 2026-05-04
description: Aprende cómo convertir dxf a dwg y establecer la fuente principal en
  Java usando Aspose.CAD. Guía paso a paso para obtener visuales CAD perfectas.
keywords:
- convert dxf to dwg
- set primary font
- change dwg text style
- how to substitute font
- aspose cad licensing
linktitle: Sustituir fuente en DWG
second_title: Aspose.CAD Java API
title: Convertir dxf a dwg y cambiar la fuente en DWG Aspose.CAD Java
url: /es/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo cargar un archivo DWG en Java y sustituir la fuente con Aspose.CAD

## Introducción

Si necesita **convert dxf to dwg** en aplicaciones Java y dar a sus dibujos un aspecto pulido, sustituir la fuente es una solución rápida. Con Aspose.CAD para Java puede reemplazar el estilo de texto predeterminado con cualquier fuente instalada en el sistema, asegurando que cada anotación aparezca exactamente como espera. En este tutorial recorreremos todo el proceso, desde cargar un archivo DWG en Java hasta usar el método `setPrimaryFontName` para cambiar la fuente.

## Respuestas rápidas
- **¿Qué biblioteca necesito?** Aspose.CAD for Java.  
- **¿Puedo cargar un archivo DWG en Java?** Sí, simplemente llame a `Image.load()` con la ruta del DWG.  
- **¿Qué método cambia la fuente?** `setPrimaryFontName`.  
- **¿Necesito una licencia para producción?** Sí, se requiere una licencia comercial.  
- **¿Es posible el procesamiento por lotes?** Absolutamente – recorra varios archivos con el mismo código.

## Qué es **convert dxf to dwg**?

“Convert dxf to dwg” se refiere a transformar un archivo DXF (Drawing Exchange Format) al formato nativo DWG utilizado por muchas aplicaciones CAD. Convertir le permite tomar un dibujo DXF ampliamente compatible, incorporarlo a un flujo de trabajo DWG y luego aplicar estilos avanzados —como la sustitución de fuentes— usando Aspose.CAD.

## Por qué sustituir fuentes en un archivo DWG?

- **Consistencia:** Garantiza que todos los colaboradores vean la misma tipografía, sin importar su configuración de fuentes local.  
- **Legibilidad:** Algunas fuentes CAD predeterminadas son difíciles de leer en pantallas; cambiar a una fuente limpia como Arial mejora la claridad.  
- **Marca:** Alinea los dibujos técnicos con las guías de estilo corporativas.  

## Casos de uso comunes

| Escenario | Por qué es importante |
|----------|------------------------|
| **Conversión por lotes de dibujos DXF heredados** | Puede convertirlos a DWG y aplicar una fuente corporativa en una sola pasada. |
| **Preparar dibujos para presentaciones a clientes** | Fuentes consistentes y legibles hacen que los documentos se vean profesionales. |
| **Pipelines CAD automatizados** | Incorporar la sustitución de fuentes elimina los pasos manuales de post‑procesamiento. |

## Requisitos previos

- **Java Development Kit (JDK)** – cualquier versión reciente (se recomienda 8+).  
- **Aspose.CAD for Java** – descargue desde el [website](https://releases.aspose.com/cad/java/).  
- **Archivo DWG/DXF de muestra** – un dibujo que desea modificar (puede usar cualquier archivo DWG o DXF para pruebas).

## Importar espacios de nombres

En su proyecto Java, importe las clases necesarias para trabajar con Aspose.CAD. Estas importaciones le dan acceso a la carga de imágenes, objetos específicos de CAD y la manipulación de estilos.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## Guía paso a paso para sustituir la fuente

### Paso 1: Cargar su archivo DWG (load dwg file java)

Primero, indique a la API la ubicación de su archivo DWG (o DXF) y cárguelo en un objeto `CadImage`.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **Consejo profesional:** Si trabaja con archivos DWG directamente, reemplace la extensión `.dxf` por `.dwg` en la variable `srcFile`.

### Paso 2: Recorrer la tabla de estilos y establecer el nombre de la fuente primaria

Cada dibujo CAD contiene una colección de objetos de estilo. Recorra la colección y use el método `setPrimaryFontName` (la llamada de API que **establece el nombre de la fuente primaria**) para reemplazar la fuente.

```java
for(Object style : cadImage.getStyles())
{
    // Set the font name
    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
}
```

Puede cambiar `"Arial"` por cualquier fuente que esté instalada en la máquina que ejecuta el código.

### Paso 3: Guardar el dibujo modificado

Después de actualizar la fuente, escriba los cambios en un nuevo archivo DWG (o sobrescriba el original).

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

El archivo guardado ahora usa la fuente que especificó, y cualquier anotación de texto se renderizará con esa tipografía.

## Problemas comunes y soluciones

| Problema | Solución |
|----------|----------|
| **Fuente no aplicada** | Verifique que la fuente esté instalada en el sistema operativo host y que la ortografía coincida exactamente. |
| **`Image.load` lanza una excepción** | Asegúrese de que la ruta del archivo sea correcta y de que el archivo sea un formato DWG/DXF compatible. |
| **Ralentización del rendimiento en archivos grandes** | Procese los archivos en un hilo separado o en lotes para evitar bloquear la interfaz de usuario. |

## Preguntas frecuentes

**P: ¿El método `setPrimaryFontName` afecta solo a entidades de texto?**  
R: Actualiza la fuente primaria para la tabla de estilos, lo que a su vez influye en todos los objetos de texto que hacen referencia a ese estilo.

**P: ¿Puedo usar una fuente personalizada que no esté instalada en el sistema?**  
R: Aspose.CAD depende del registro de fuentes del sistema operativo. Para usar una fuente personalizada, instálela en la máquina que ejecuta el código.

**P: ¿Es posible cambiar la fuente solo para una capa?**  
R: Sí, puede filtrar los estilos por nombre de capa antes de llamar a `setPrimaryFontName`.

**P: ¿Qué versión de Aspose.CAD se requiere para archivos DWG 2022?**  
R: La última versión (a partir de 2025) soporta completamente DWG 2022. Siempre revise las notas de la versión para el soporte específico de formatos.

**P: ¿Cómo manejo la licencia en un entorno de desarrollo?**  
R: Use una licencia de evaluación temporal para pruebas. Para producción, incruste su archivo de licencia comprado usando `License.setLicense("Aspose.Total.Java.lic");`.

**Última actualización:** 2026-05-04  
**Probado con:** Aspose.CAD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}