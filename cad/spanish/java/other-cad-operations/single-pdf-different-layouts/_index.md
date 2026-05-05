---
date: 2026-01-22
description: Aprende a crear PDF a partir de dibujos CAD, convertir DWG a PDF y personalizar
  el tamaño de página del PDF usando Aspose.CAD para Java.
linktitle: Single PDF with Different Layouts
second_title: Aspose.CAD Java API
title: Cómo crear PDF a partir de dibujos CAD con Aspose.CAD para Java
url: /es/java/other-cad-operations/single-pdf-different-layouts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo crear PDF a partir de dibujos CAD con Aspose.CAD para Java

## Introducción

En este tutorial descubrirá **cómo crear PDF a partir de CAD** usando la biblioteca Aspose.CAD para Java. Ya sea que necesite **convertir DWG a PDF**, exportar un archivo CAD complejo o aplicar un **tamaño de página PDF personalizado**, los pasos a continuación le guiarán a través de una solución limpia y programática. Recorramos el proceso juntos, para que pueda generar un único PDF que contenga múltiples páginas de diseño, todo con solo unas pocas líneas de código Java.

## Respuestas rápidas
- **¿Qué hace Aspose.CAD?** Permite a los desarrolladores Java cargar, manipular y exportar dibujos CAD a formatos como PDF.
- **¿Puedo export para uso comercial.
- **¿ Java rasterizar dibujos CAD basados en vectores en un documento de diseño fijo (PDF) que puede verse en cualquier dispositivo sin necesidad de software CAD. Esto es ideal para compartir diseños, imprimir planos o archivar trabajos de ingeniería.

## ¿Por qué usar Aspose.CAD para Java?
- **Sin dependencias externas** – Java puro, sin DLLs nativas.
- **Control fino** sobre opciones de rasterizado como DPI, tamaño de página y selección de diseño.
- **Procesamiento por lotes** – manejar muchos dibujos en una sola de comenzar, asegúrese de contar con lo siguiente:

- **Entorno Java** – JDK 8 o más reciente instalado.
- **Biblioteca Aspose.CAD** – Descargue e instale la biblioteca Aspose.CAD para Java desde el [enlace de descarga](https://releases.aspose.com/cad/java/).
- **Directorio de documentos** – Una carpeta que contiene los dibujos DWG (u otros CAD) que desea convertir.

## Importar paquetes

En su proyecto Java, importe las clases necesarias:

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## Guía paso a paso

### Paso 1: Cargar dibujo CAD

Primero, cargue el archivo CAD de origen (p.ej., un DWG) en un objeto `CadImage`. Este es el punto de entrada para cualquier operación de **exportar CAD a PDF**.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

### Paso 2: Configurar opciones de rasterizado

Defina cómo se debe rasterizar los datos CAD. Aquí establecemos un ancho y alto de página base que se usará para los diseños que no tengan un tamaño personalizado.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

### Paso 3: Personalizar tamaños de página de los diseños

Si necesita un **tamaño de página PDF personalizado**, añada entradas para cada diseño que desea que aparezca en el PDF final. Esto le permite **convertir DWG a PDF** con diferentes dimensiones por diseño.

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

### Paso 4: Establecer opciones de PDF

Combine las configuraciones de rasterizado con opciones específicas de PDF. La propiedad `VectorRasterizationOptions` indica a Aspose.CAD que use los tamaños de diseño que acabamos de definir.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Paso 5: Guardar como PDF

Finalmente, exporte el dibujo CAD a un único archivo PDF que contenga todos los diseños especificados. Este paso **guarda CAD como PDF** en una sola llamada.

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

> **Consejo:** Reutilice el mismo objeto `PdfOptions` si necesita exportar varios dibujos en un lote – reduce la sobrecarga de creación de objetos.

## Problemas comunes y soluciones

| Problema | Solución |
|----------|----------|
| **Páginas en blanco en el PDF de salida** | Verifique que los nombres de los diseños (`"ANSI C Plot"`, `"8.5 x 11 Plot"`) coincidan exactamente con los definidos en el archivo CAD. |
| **Salida de baja resolución** | Aumente el DPI llamando a `rasterizationOptions.setResolution(300);` antes de guardar. |
| **Licencia no aplicada** | Cargue su licencia temporal o completa antes de cualquier llamada a Aspose.CAD: `License license = new License(); license.setLicense("Aspose.CAD.lic");` |

## Preguntas frecuentes

### Q1: ¿Puedo usar Aspose.CAD para Java con otras bibliotecas Java?

A1: Sí, Aspose.CAD para Java está diseñado para integrarse sin problemas con otras bibliotecas Java, proporcionando una funcionalidad extensa.

### Q2: ¿Hay una versión de prueba disponible?

A2: ¡Absolutamente! Puede acceder a una versión de prueba gratuita [aquí](https://releases.aspose.com/).

### Q3: ¿Dónde puedo encontrar soporte adicional?

A3: Visite el [foro de Aspose.CAD](https://forum.aspose.com/c/cad/19) para soporte comunitario y discusiones.

### Q4: ¿Cómo obtengo una licencia temporal?

A4: Puede obtener una licencia temporal [aquí](https://purchase.aspose.com/temporary-license/).

### Q5: ¿Dónde puedo comprar la versión completa?

A5: Compre la versión completa de Aspose.CAD para Java [aquí](https://purchase.aspose.com/buy).

---

**Última actualización:** 2026-01-22  
**Probado con:** Aspose.CAD para Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}