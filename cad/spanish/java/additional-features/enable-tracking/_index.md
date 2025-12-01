---
date: 2025-12-01
description: Aprenda a establecer el tamaño de página PDF, convertir DWG a PDF y habilitar
  el seguimiento de cambios en DWG usando Aspose.CAD para Java.
language: es
linktitle: Set PDF Page Size and Track DWG with Java
second_title: Aspose.CAD Java API
title: Establecer el tamaño de página PDF y rastrear DWG con Aspose.CAD Java
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Establecer el tamaño de página PDF y rastrear DWG con Aspose.CAD Java

## Introducción

Cuando se colabora en proyectos CAD, a menudo es necesario **establecer el tamaño de página PDF** para un diseño coherente, **convertir DWG a PDF** y hacer un seguimiento de cada cambio realizado en el dibujo. Aspose.CAD para Java hace todo esto posible en un flujo de trabajo único y simplificado. En este tutorial recorreremos los pasos exactos para **establecer el tamaño de página PDF**, habilitar el **seguimiento de cambios en DWG** y exportar el dibujo como PDF, todo usando Java.

## Respuestas rápidas
- **¿Cómo establezco el tamaño de página PDF?** Use `CadRasterizationOptions.setPageWidth()` and `setPageHeight()` before exporting.  
- **¿Puedo rastrear cambios al exportar?** Sí – implemente un `CadRenderHandler` personalizado para capturar los resultados del seguimiento.  
- **¿Qué método convierte DWG a PDF?** Llame a `image.save(stream, pdfOptions)` después de configurar las opciones.  
- **¿Cuáles son los requisitos principales?** JDK, Aspose.CAD para Java y una carpeta con archivos DWG/DXF.  
- **¿Se requiere una licencia para producción?** Sí, se necesita una licencia válida de Aspose.CAD para implementaciones que no sean de prueba.

## ¿Qué significa “establecer el tamaño de página PDF” en el contexto de la exportación DWG?

Establecer el tamaño de página PDF determina las dimensiones del lienzo PDF resultante (ancho × alto en píxeles). Esto es esencial cuando desea que el dibujo exportado se ajuste a un tamaño de papel o disposición de pantalla específico, garantizando que todos los elementos aparezcan exactamente donde los espera.

## ¿Por qué habilitar el seguimiento al exportar archivos DWG?

El seguimiento (o seguimiento de cambios) registra cualquier problema de renderizado, fuentes faltantes o entidades no compatibles que ocurren durante la conversión. Al capturar esta información puede:
- Identificar rápidamente los problemas que necesitan ser corregidos antes de la entrega final.  
- Proporcionar retroalimentación clara a los miembros del equipo sobre lo que se modificó o omitió.  
- Mantener un registro de auditoría para industrias con altas exigencias de cumplimiento.

## Requisitos previos

- **Java Development Kit (JDK)** – cualquier versión reciente (8+).  
- **Aspose.CAD for Java** – download from the official [página de descarga de Aspose CAD](https://releases.aspose.com/cad/java/).  
- **Directorio de documentos** – una carpeta que contiene los archivos DWG/DXF que desea procesar.

## Importar espacios de nombres

Comience importando las clases necesarias de Aspose.CAD y las clases estándar de Java I/O.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
```

## Paso 1: Cargar el archivo DWG (o DXF)

Cargue su dibujo fuente en un objeto `Image`. Ajuste la ruta para que apunte a su propio directorio.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Paso 2: Configurar las opciones de exportación PDF (incluido el tamaño de página)

Aquí configuramos las opciones PDF y establecemos explícitamente **el tamaño de página PDF** a 800 × 600 píxeles. Aquí es donde se aplica la palabra clave principal.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // set PDF page width
cadRasterizationOptions.setPageHeight(600);  // set PDF page height
```

## Paso 3: Implementar el seguimiento

Cree un controlador de errores personalizado que recibirá la información de seguimiento durante el proceso de conversión.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Paso 4: Exportar a PDF

Con las opciones y el controlador de seguimiento configurados, exporte el dibujo. Este paso **convierte DWG a PDF** (o DXF a PDF en nuestro ejemplo).

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Paso 5: Clase CadRenderHandler – Capturando resultados del seguimiento

La clase `ErrorHandler` extiende `CadRenderHandler` e imprime cualquier problema de renderizado que ocurrió mientras **se rastreaban cambios en archivos DWG**.

```java
public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler {
    @Override
    public void invoke(CadRenderResult result) {
        System.out.println("Tracking results of exporting");

        if (result.isRenderComplete())
            return;

        System.out.println("Have some problems:");

        int idxError = 1;
        for (RenderResult rr : result.getFailures()) {
            System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
            idxError++;
        }
    }
}
```

## Problemas comunes y cómo resolverlos

| Problema | Por qué ocurre | Solución |
|----------|----------------|----------|
| **Fuentes faltantes** | El archivo CAD hace referencia a fuentes que no están instaladas en el servidor. | Instale las fuentes requeridas o incrústelas en el dibujo fuente. |
| **Entidades no compatibles** | Algunas entidades DWG aún no son compatibles con Aspose.CAD. | Utilice la salida del seguimiento para identificarlas y simplificar el dibujo. |
| **Tamaño de página incorrecto** | No se llamó a `setPageWidth/Height` antes de la exportación. | Asegúrese de que el tamaño de página esté configurado en `CadRasterizationOptions` como se muestra arriba. |

## Preguntas frecuentes

### Q1: ¿Puedo habilitar el seguimiento para otros formatos de archivo CAD usando Aspose.CAD para Java?

R1: Aspose.CAD admite principalmente el seguimiento para archivos DWG/DXF. Para otros formatos, consulte la documentación oficial para ver qué funciones están disponibles.

### Q2: ¿Cómo puedo manejar opciones de exportación adicionales en Aspose.CAD para Java?

R2: The library offers many options such as DPI, background color, and vector rasterization. Explore them in the [Documentación de Aspose.CAD Java](https://reference.aspose.com/cad/java/).

### Q3: ¿Hay una versión de prueba disponible para Aspose.CAD para Java?

R3: Yes, you can download a free trial from the [Prueba gratuita de Aspose.CAD](https://releases.aspose.com/).

### Q4: ¿Dónde puedo buscar asistencia o discutir problemas relacionados con Aspose.CAD para Java?

R4: The community forum at the [foro de Aspose.CAD](https://forum.aspose.com/c/cad/19) is a great place to ask questions and share experiences.

### Q5: ¿Cómo obtengo una licencia temporal para Aspose.CAD para Java?

R5: Follow the steps outlined on the [Licencia temporal](https://purchase.aspose.com/temporary-license/) page to request a time‑limited license for evaluation.

### Q6: ¿Puedo **convertir DWG a PDF** mientras preservo capas?

R6: Sí. Configurando `CadRasterizationOptions` puede preservar la información de capas en el PDF resultante.

### Q7: ¿Cuál es la mejor manera de **exportar DWG como PDF** con dimensiones de página personalizadas?

R7: Establezca el ancho y alto deseados usando `setPageWidth` y `setPageHeight` antes de llamar a `image.save()`, exactamente como se muestra en el Paso 2.

## Conclusión

Al seguir los pasos anteriores, puede **establecer el tamaño de página PDF**, **convertir DWG a PDF** y **rastrear cambios en archivos DWG** usando Aspose.CAD para Java. Este flujo de trabajo le brinda control total sobre el diseño de salida mientras proporciona diagnósticos valiosos que mantienen su colaboración CAD fluida y sin errores. No dude en explorar opciones de renderizado adicionales e integrar este código en pipelines de automatización más grandes.

---

**Última actualización:** 2025-12-01  
**Probado con:** Aspose.CAD para Java 24.12 (última versión al momento de escribir)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}