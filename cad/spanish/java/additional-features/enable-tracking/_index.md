---
date: 2025-12-03
description: 'Aprenda a establecer el tamaño de página PDF al convertir DWG a PDF
  y habilitar el seguimiento en archivos DWG usando Aspose.CAD para Java: una guía
  completa para exportar dibujos CAD a PDF con precisión.'
language: es
linktitle: Set PDF Page Size and Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: Establecer el tamaño de página PDF y habilitar el seguimiento en archivos DWG
  usando Aspose.CAD en Java
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Establecer el tamaño de página PDF y habilitar el seguimiento en archivos DWG usando Aspose.CAD en Java

## Introducción

Si necesita **establecer el tamaño de página PDF** al *convertir DWG a PDF* y también mantener un registro de cualquier problema de renderizado, Aspose.CAD para Java le brinda una forma limpia y programática de hacer ambas cosas. En este tutorial recorreremos los pasos exactos para configurar las dimensiones de la página, habilitar el seguimiento y exportar un PDF de dibujo CAD, todo desde Java. Al final comprenderá por qué establecer el tamaño de página correcto es importante para los dibujos CAD y cómo capturar información detallada de seguimiento durante el proceso de exportación.

## Respuestas rápidas
- **¿Qué afecta “establecer el tamaño de página PDF”?** Define el ancho y la altura del lienzo PDF resultante, asegurando que su dibujo encaje perfectamente.  
- **¿Necesito una licencia para usar esta función?** Una versión de prueba funciona para pruebas; se requiere una licencia comercial para producción.  
- **¿Qué versión de Aspose.CAD se requiere?** Cualquier versión reciente que admita `CadRasterizationOptions`.  
- **¿Puedo usar esto con otros formatos CAD?** El ejemplo muestra DWG/DXF, pero el mismo enfoque funciona para la mayoría de los formatos compatibles.  
- **¿Cuánto tiempo lleva la conversión?** Normalmente menos de un segundo para archivos modestos; dibujos más grandes pueden tardar más.

## ¿Qué es “establecer el tamaño de página PDF” en el contexto de la exportación CAD?
Establecer el tamaño de página PDF indica al renderizador las dimensiones exactas (en píxeles o puntos) del lienzo de salida. Esto es especialmente importante para dibujos técnicos donde la escala y el diseño deben preservarse. Sin una configuración explícita del tamaño de página, el PDF puede usar un tamaño predeterminado que recorte o distorsione el dibujo.

## ¿Por qué establecer el tamaño de página PDF al exportar dibujos CAD?
- **Preservar la escala** – Los ingenieros dependen de impresiones a escala real.  
- **Ajustar al papel** – Elija A4, Letter o un tamaño personalizado que coincida con las especificaciones del proyecto.  
- **Mejorar la legibilidad** – Páginas más grandes pueden mostrar detalles finos sin necesidad de hacer zoom.  
- **Salida consistente** – Las canalizaciones automatizadas generan PDFs con dimensiones idénticas en cada ejecución.

## ¿Cómo establecer el tamaño de página PDF al convertir DWG a PDF?
A continuación configuraremos `CadRasterizationOptions` con valores personalizados de ancho y altura antes de la exportación. Este paso aborda directamente la palabra clave principal **establecer el tamaño de página PDF**.

## Requisitos previos

- **Java Development Kit (JDK)** – Java 8 o superior instalado en su máquina.  
- **Aspose.CAD for Java** – Descárguelo desde la página oficial de [Aspose CAD download page](https://releases.aspose.com/cad/java/).  
- **Directorio de documentos** – Una carpeta que contiene los archivos DWG/DXF que desea procesar.

## Importar espacios de nombres

Primero, importe las clases que necesitará. El bloque de código permanece sin cambios respecto al tutorial original.

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

## Paso 1: Cargar el archivo DWG/DXF

Cargue su dibujo fuente. Ajuste la ruta para que apunte a su propio archivo.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Paso 2: Configurar las opciones de exportación PDF (incluyendo el tamaño de página)

Aquí establecemos el ancho y la altura de la página; aquí es donde **establecemos el tamaño de página PDF**. Los valores están en píxeles; puede convertir desde pulgadas o milímetros según sea necesario.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // <-- custom width
cadRasterizationOptions.setPageHeight(600);  // <-- custom height
```

> **Consejo:** Si prefiere tamaños de papel estándar, use la conversión `1 inch = 72 points`. Para una página A4 (8.27 × 11.69 in), establezca `pageWidth = 595` y `pageHeight = 842`.

## Paso 3: Implementar el seguimiento

El seguimiento captura cualquier problema de renderizado. Adjuntamos un controlador personalizado que se invocará después de la exportación.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Paso 4: Exportar a PDF

Ahora realice la conversión. El PDF se creará con las dimensiones que especificó y cualquier información de seguimiento se imprimirá en la consola.

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Paso 5: Clase CadRenderHandler

El controlador imprime cualquier falla que haya ocurrido durante el renderizado. Esto le ayuda a depurar problemas al **exportar PDF de dibujo CAD**.

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

## Problemas comunes y soluciones

| Problema | Causa | Solución |
|----------|-------|----------|
| **PDF en blanco** | Tamaño de página establecido en 0 o demasiado pequeño | Verifique que `setPageWidth` y `setPageHeight` sean valores positivos. |
| **Geometría faltante** | Errores de renderizado capturados por el manejador | Revise la salida de consola de `ErrorHandler` y solucione el `RenderCode` específico. |
| **Archivo no encontrado** | Ruta `dataDir` incorrecta | Utilice una ruta absoluta o asegúrese de que el directorio exista. |
| **Excepción de licencia** | Uso de la versión de prueba sin una licencia válida para archivos grandes | Aplique su licencia de Aspose.CAD antes de cargar la imagen. |

## Preguntas frecuentes

**P: ¿Puedo habilitar el seguimiento para otros formatos de archivo CAD usando Aspose.CAD para Java?**  
R: Aspose.CAD admite principalmente DWG/DXF para el seguimiento. Para otros formatos, consulte la documentación oficial.

**P: ¿Cómo puedo manejar opciones de exportación adicionales en Aspose.CAD para Java?**  
R: La biblioteca ofrece muchas opciones como DPI, color de fondo y rasterización vectorial. Consulte la [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) para más detalles.

**P: ¿Hay una versión de prueba disponible para Aspose.CAD para Java?**  
R: Sí, puede descargar una prueba gratuita desde el [Aspose.CAD Free Trial](https://releases.aspose.com/).

**P: ¿Dónde puedo buscar asistencia o discutir problemas relacionados con Aspose.CAD para Java?**  
R: Visite el [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) para soporte comunitario y respuestas oficiales.

**P: ¿Cómo obtengo una licencia temporal para Aspose.CAD para Java?**  
R: Siga los pasos descritos en la página de [Temporary License](https://purchase.aspose.com/temporary-license/).

---

**Última actualización:** 2025-12-03  
**Probado con:** Aspose.CAD for Java 24.11 (última disponible al momento de escribir)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}