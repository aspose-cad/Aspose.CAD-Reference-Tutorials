---
date: 2026-03-02
description: Desbloquea el potencial de Aspose.CAD para Java. Exporta objetos OLE
  sin esfuerzo y **guarda CAD como PNG**. Descarga ahora para una gestión fluida de
  datos CAD.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: Guardar CAD como PNG – Exportar objetos OLE usando Aspose.CAD para Java
url: /es/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Guardar CAD como PNG – Exportar objetos OLE usando Aspose.CAD para Java

## Introducción

En el dinámico mundo del Diseño Asistido por Computadora (CAD), gestionar y extraer objetos OLE (Object Linking and Embedding) de forma eficiente —y poder **guardar CAD como PNG**— es crucial para flujos de trabajo posteriores como informes, vistas previas web o archivado. Aspose.CAD para Java ofrece una solución potente, orientada al código, que permite tanto exportar objetos OLE como convertir dibujos CAD a imágenes PNG de alta calidad en solo unas pocas líneas de código.

## Respuestas rápidas
- **¿Qué hace Aspose.CAD?** Lee, manipula y convierte archivos CAD (DWG, DXF, DGN, etc.) sin necesidad de software CAD nativo.  
- **¿Puedo guardar CAD como PNG?** Sí—utiliza `PngOptions` junto con `CadRasterizationOptions` para rasterizar cualquier layout.  
- **¿Cómo exportar objetos OLE?** Carga el archivo CAD con `Image.load` y guarda cada layout que contenga OLE como PNG.  
- **¿Necesito una licencia?** Hay una prueba gratuita disponible; una licencia comercial elimina las limitaciones de evaluación.  
- **¿Qué versión de Java se requiere?** Java 8 o superior es totalmente compatible.

## ¿Qué es **guardar CAD como PNG**?
Guardar CAD como PNG significa rasterizar dibujos CAD basados en vectores a una imagen PNG basada en píxeles. Esta conversión es útil cuando necesitas un formato ligero y universalmente visible para páginas web, aplicaciones móviles o documentación.

## ¿Por qué usar Aspose.CAD para Java para **convertir CAD a PNG**?
- **No se necesita instalación de CAD** – la biblioteca funciona completamente en Java.  
- **Preserva la fidelidad del layout** – puedes elegir layouts específicos, controlar DPI y mantener la calidad de las líneas.  
- **Procesamiento por lotes** – itera sobre múltiples archivos con un bucle sencillo.  
- **Exportar objetos OLE** – el contenido OLE incrustado en archivos DWG/DXF se renderiza automáticamente en la salida PNG.

## Requisitos previos

Antes de sumergirte en el tutorial, asegúrate de contar con los siguientes requisitos:

- **Entorno Java** – Verifica que tienes un entorno de desarrollo Java configurado en tu máquina.  
- **Aspose.CAD para Java** – Descarga e instala la biblioteca Aspose.CAD para Java. Puedes encontrar la biblioteca en el [enlace de descarga](https://releases.aspose.com/cad/java/).  
- **Archivos CAD** – Prepara los archivos CAD que contengan objetos OLE que deseas exportar.

## Importar espacios de nombres

Para comenzar, importa los espacios de nombres necesarios en tu proyecto Java. Estos espacios de nombres proporcionan las clases y funcionalidades esenciales para trabajar con archivos CAD usando Aspose.CAD.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Ahora, desglosaremos el proceso de exportación de objetos OLE desde CAD en varios pasos:

## Cómo **guardar CAD como PNG** y exportar objetos OLE

### Paso 1: Establecer el directorio de documentos

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

Asegúrate de reemplazar `"Your Document Directory"` con la ruta al directorio que contiene tus archivos CAD.

### Paso 2: Definir los nombres de los archivos CAD

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

Especifica los nombres de los archivos CAD que deseas procesar en el arreglo `files`.

### Paso 3: Configurar las opciones de exportación PNG

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

Configura las opciones de exportación PNG, incluida la rasterización vectorial y la configuración de layouts. Estas opciones son las que te permiten **convertir CAD a PNG** con la calidad deseada.

### Paso 4: Iterar a través de los archivos CAD

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

Itera sobre cada archivo CAD especificado, cárgalo usando Aspose.CAD y guarda los objetos OLE como imágenes PNG. Este bucle muestra una manera sencilla de **convertir DWG a PNG** en bloque.

## Problemas comunes y soluciones

| Problema | Causa | Solución |
|----------|-------|----------|
| **Salida PNG en blanco** | Incompatibilidad del nombre del layout | Verifica que el nombre del layout (`"Layout1"`) exista en el DWG origen. |
| **Gráficos OLE ausentes** | Los objetos OLE están almacenados en un layout diferente | Incluye todos los layouts relevantes en `rasterizationOptions.setLayouts(...)`. |
| **Error de falta de memoria en archivos grandes** | Configuraciones de DPI altas | Reduce el DPI mediante `rasterizationOptions.setResolution(...)` o procesa los archivos uno a la vez. |

## Preguntas frecuentes

**P: ¿Aspose.CAD es compatible con todos los formatos de archivo CAD?**  
R: Aspose.CAD soporta varios formatos CAD, incluidos DWG, DXF y DGN. Consulta la [documentación](https://reference.aspose.com/cad/java/) para obtener la lista completa.

**P: ¿Puedo personalizar la configuración de exportación para objetos OLE?**  
R: Sí, Aspose.CAD ofrece amplias opciones para personalizar la configuración de exportación, permitiéndote adaptar la salida a tus requisitos específicos.

**P: ¿Hay una prueba gratuita disponible para Aspose.CAD?**  
R: Sí, puedes explorar las capacidades de Aspose.CAD obteniendo una prueba gratuita desde [aquí](https://releases.aspose.com/).

**P: ¿Dónde puedo obtener soporte comunitario para Aspose.CAD?**  
R: Únete a la comunidad de Aspose.CAD en el [foro](https://forum.aspose.com/c/cad/19) para solicitar asistencia y compartir tus experiencias.

**P: ¿Cómo puedo comprar una licencia para Aspose.CAD?**  
R: Visita la [página de compra](https://purchase.aspose.com/buy) para adquirir una licencia que se ajuste a tus necesidades de desarrollo.

## Conclusión

Con estos pasos simples pero potentes, puedes **guardar CAD como PNG** mientras exportas objetos OLE de archivos CAD usando Aspose.CAD para Java. Esta herramienta versátil permite a los desarrolladores gestionar datos CAD de manera eficiente, abriendo nuevas posibilidades en el desarrollo de aplicaciones CAD y flujos de trabajo posteriores basados en imágenes.

---

**Última actualización:** 2026-03-02  
**Probado con:** Aspose.CAD para Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}