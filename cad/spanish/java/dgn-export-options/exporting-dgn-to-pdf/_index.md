---
date: 2026-05-04
description: Aprende cómo convertir archivos PDF de CAD exportando DGN a PDF de AutoCAD
  usando Aspose.CAD para Java. Guía paso a paso con tamaño de PDF personalizable y
  opciones.
keywords:
- convert cad pdf
- how to export dgn
- customize pdf size
- aspose cad download
- set pdf options
linktitle: Exportar DGN en formato AutoCAD a PDF
second_title: Aspose.CAD Java API
title: Convertir PDF CAD – Exportación sin esfuerzo de DGN a PDF de AutoCAD con Aspose.CAD
  para Java
url: /es/java/dgn-export-options/exporting-dgn-to-pdf/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir CAD PDF: Exportación sin esfuerzo de DGN a PDF AutoCAD con Aspose.CAD para Java

## Introducción

Si necesita **convertir CAD PDF** directamente desde fuentes DGN, ha llegado al lugar correcto. En este tutorial le guiaremos paso a paso sobre cómo usar Aspose.CAD para Java para exportar archivos DGN a un PDF compatible con AutoCAD. Verá cómo establecer dimensiones de página personalizadas, seleccionar diseños específicos y afinar la salida PDF, todo con código claro y paso a paso que puede incorporar en su propio proyecto.

## Respuestas rápidas
- **¿Qué significa “convertir CAD PDF”?** Se refiere a transformar archivos fuente CAD (como DGN) en un PDF que preserva los datos vectoriales y la fidelidad del diseño.  
- **¿Qué biblioteca maneja la conversión?** Aspose.CAD para Java ofrece una prueba fiable y sin licencia para esta tarea.  
- **¿Necesito una licencia para el desarrollo?** Una prueba gratuita funciona para pruebas; se requiere una licencia comercial para uso en producción.  
- **¿Puedo personalizar el tamaño del PDF?** Sí – las `CadRasterizationOptions` le permiten establecer el ancho, alto y escalado de la página.  
- **¿Cuántas líneas de código se requieren?** Menos de 20 líneas de código Java para cargar, configurar y guardar el PDF.

## ¿Qué es “convertir CAD PDF”?
Convertir CAD PDF significa tomar un dibujo CAD nativo (p. ej., DGN) y producir un PDF que retenga los gráficos vectoriales originales, capas e información de diseño. El PDF resultante puede verse en cualquier dispositivo sin necesidad de software CAD, lo que lo hace ideal para compartir, imprimir o archivar.

## ¿Por qué usar Aspose.CAD para Java para convertir CAD PDF?
- **Compatibilidad total de formatos** – DGN, DWG, DXF y muchos más.  
- **Sin dependencias externas** – Java puro, sin DLLs nativas.  
- **Control granular** – puede elegir qué diseños exportar, establecer tamaños de página personalizados y controlar la calidad de rasterización.  
- **Escalable para trabajos por lotes** – cargar y guardar decenas de archivos en un bucle con un mínimo sobrecosto.

## Requisitos previos
Antes de comenzar, asegúrese de contar con lo siguiente:

- **Biblioteca Aspose.CAD** – descárguela [aquí](https://releases.aspose.com/cad/java/).  
- **Directorio de documentos** – una carpeta en su máquina donde estarán los archivos DGN de entrada y los PDFs de salida.

## Importar paquetes

En su proyecto Java, importe los paquetes necesarios para acceder a las funcionalidades de Aspose.CAD:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Ahora, desglosaremos el código de ejemplo en varios pasos:

## Paso 1: Definir rutas de archivo (cómo exportar dgn)

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

Asegúrese de reemplazar `"Your Document Directory"` con la ruta real donde se encuentran sus archivos.

## Paso 2: Cargar imagen DGN

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Cargue el archivo DGN usando Aspose.CAD.

## Paso 3: Configurar opciones de exportación PDF (personalizar tamaño pdf, establecer opciones pdf)

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Export specific views
options.setVectorRasterizationOptions(vectorOptions);
```

Aquí definimos las opciones de exportación PDF, incluidas las dimensiones de página, el escalado automático y los diseños DGN (vistas) específicos que desea incluir en el PDF final.

## Paso 4: Guardar archivo PDF

```java
objImage.save(outFile, options);
```

Guarde el archivo PDF exportado. El método `save` aplica todas las opciones que configuró en el paso anterior.

Repita estos pasos para cualquier archivo DGN adicional que desee convertir. ¡Felicidades! Ha **convertido CAD PDF** con éxito exportando archivos DGN al formato AutoCAD en PDF usando Aspose.CAD para Java.

## Problemas comunes y soluciones
| Problema | Por qué ocurre | Solución |
|----------|----------------|----------|
| **Archivo no encontrado** | Ruta `dataDir` incorrecta | Verifique la ruta de la carpeta y asegúrese de que el archivo DGN exista. |
| **Páginas en blanco en el PDF** | `AutomaticLayoutsScaling` configurado en `false` o IDs de diseño faltantes | Mantenga `setAutomaticLayoutsScaling(true)` y verifique los nombres de los diseños (`"1","2",…`). |
| **Salida de baja resolución** | El DPI de rasterización predeterminado es bajo | Use `vectorOptions.setResolution(300);` para aumentar la calidad (añádalo antes de `setVectorRasterizationOptions`). |
| **Excepción de licencia** | Ejecutando sin una licencia válida en producción | Aplique una licencia temporal o comprada como se describe en la documentación de Aspose. |

## Preguntas frecuentes (Adicionales)

**P: ¿Puedo exportar solo un diseño único de un archivo DGN con múltiples diseños?**  
R: Sí – especifique los IDs de diseño deseados en `vectorOptions.setLayouts(new String[] { "2" });`.

**P: ¿Es posible incrustar fuentes en el PDF resultante?**  
R: Aspose.CAD incrusta automáticamente las fuentes necesarias cuando los datos vectoriales se rasterizan; también puede controlar la incrustación de fuentes mediante `PdfOptions` si lo necesita.

**P: ¿Cómo proceso muchos archivos DGN en lote?**  
R: Envuelva los pasos dentro de un bucle `for` que itere sobre una lista de nombres de archivo, reutilizando la misma instancia de `PdfOptions` en cada iteración.

**P: ¿La biblioteca admite PDFs protegidos con contraseña?**  
R: Sí – puede establecer una contraseña en el objeto `PdfOptions` mediante `options.setPassword("yourPassword");`.

**P: ¿Dónde puedo encontrar más ejemplos?**  
R: La documentación oficial de Aspose.CAD y el repositorio de ejemplos contienen muchos escenarios adicionales.

## Preguntas frecuentes (Original)

### P1: ¿Es Aspose.CAD compatible con todos los formatos de archivo CAD?

R1: Sí, Aspose.CAD admite una amplia gama de formatos CAD, lo que garantiza versatilidad al manejar varios tipos de archivo.

### P2: ¿Puedo personalizar la configuración de exportación PDF?

R2: Absolutamente. Como se muestra en el tutorial, puede ajustar opciones como dimensiones de página y diseños para adaptarse a sus requisitos.

### P3: ¿Dónde puedo encontrar soporte o asistencia adicional?

R3: Visite el [foro de Aspose.CAD](https://forum.aspose.com/c/cad/19) para obtener soporte comunitario y discusiones.

### P4: ¿Hay una prueba gratuita disponible?

R4: Sí, puede acceder a la prueba gratuita [aquí](https://releases.aspose.com/).

### P5: ¿Cómo puedo obtener una licencia temporal?

R5: Obtenga una licencia temporal [aquí](https://purchase.aspose.com/temporary-license/).

## Conclusión

En este tutorial exploramos cómo **convertir CAD PDF** utilizando Aspose.CAD para Java. Con solo unas pocas líneas de código puede cargar un dibujo DGN, afinar las opciones de exportación PDF y generar PDFs de alta calidad listos para compartir o archivar. Siéntase libre de experimentar con diferentes tamaños de página, diseños o procesamiento por lotes para adaptarse a las necesidades de su proyecto.

---

**Última actualización:** 2026-05-04  
**Probado con:** Aspose.CAD for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}