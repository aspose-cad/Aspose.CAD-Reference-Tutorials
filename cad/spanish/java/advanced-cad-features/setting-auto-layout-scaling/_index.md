---
date: 2026-02-15
description: Aprenda cómo establecer un tamaño de página personalizado y crear PDF
  a partir de CAD usando Aspose.CAD para Java. Esta guía paso a paso cubre la exportación
  de CAD a PDF con escalado automático de diseño.
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: Establecer tamaño de página personalizado – PDF desde CAD con escalado automático
  del diseño
url: /es/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

 final output.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Establecer tamaño de página personalizado – Crear PDF desde CAD con escalado automático de diseño

## Introducción

Si necesitas **establecer un tamaño de página personalizado** mientras **creas PDF desde CAD** de forma rápida y con un escalado perfecto, Aspose.CAD for Java te cubre. Auto Layout Scaling ajusta automáticamente las dimensiones del diseño para que el PDF resultante se vea exactamente como se pretende, sin importar el tamaño de página original del CAD. En este tutorial recorreremos todo el proceso —desde cargar un archivo DXF hasta exportar un PDF— resaltando las capacidades de **export CAD to PDF** de la biblioteca y mostrando cómo también puedes **convert DWG to PDF** o **increase PDF resolution** cuando sea necesario.

## Respuestas rápidas
- **¿Qué hace Auto Layout Scaling?** Redimensiona automáticamente los diseños CAD para que se ajusten a las dimensiones de la página de destino al rasterizar.
- **¿Qué formatos puedo convertir?** Cualquier formato compatible con Aspose.CAD (p. ej., DXF, DWG, DWF) puede convertirse a PDF.
- **¿Necesito una licencia para producción?** Sí, se requiere una licencia comercial para uso que no sea de evaluación.
- **¿Cuánto tiempo tarda la conversión?** Normalmente menos de un segundo para archivos estándar en hardware moderno.
- **¿Puedo cambiar el tamaño de la página?** Sí, puedes establecer dimensiones de página personalizadas mediante `CadRasterizationOptions`.

## ¿Qué es “create PDF from CAD”?

Crear un PDF desde CAD significa tomar un dibujo de ingeniería basado en vectores (DXF, DWG, etc.) y rasterizarlo en un documento PDF. El PDF conserva la fidelidad visual del dibujo original y puede visualizarse en cualquier plataforma.

## ¿Por qué usar Auto Layout Scaling?

- **Salida consistente:** Garantiza que todos los diseños llenen la página PDF sin cálculos manuales de tamaño.
- **Ahorro de tiempo:** Elimina la necesidad de ajustar manualmente los factores de escalado para cada dibujo.
- **Alta calidad:** Mantiene el grosor de línea y la precisión geométrica durante la conversión.
- **Flexibilidad:** Funciona para **convert dxf to pdf**, **convert dwg to pdf**, e incluso cuando necesitas **increase PDF resolution** para archivos listos para imprimir.

## Requisitos previos

1. **Aspose.CAD for Java Library** – descarga la última versión desde la [download page](https://releases.aspose.com/cad/java/).  
2. **Directorio de recursos** – crea una carpeta en tu máquina para almacenar los archivos CAD; reemplaza `"Your Document Directory"` en el código con esa ruta.  
3. **Archivo CAD de ejemplo** – para esta guía usaremos `conic_pyramid.dxf`, que está incluido en el conjunto de datos de ejemplo de Aspose.

## Importar espacios de nombres

Primero, importa las clases requeridas. Esto nos da acceso a la carga de imágenes, rasterización y funciones de exportación a PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Cómo establecer un tamaño de página personalizado para PDF desde CAD

Antes de sumergirnos en el código paso a paso, comprendamos por qué importa establecer un tamaño de página personalizado. Cuando **estableces un tamaño de página personalizado**, controlas las dimensiones físicas del PDF resultante (p. ej., A4, Letter o un tamaño a medida). Esto es esencial en flujos de trabajo de ingeniería donde los dibujos deben coincidir con los estándares de hoja o cuando necesitas incrustar el PDF en documentos más grandes.

### Paso 1: Cargar el archivo CAD

Cargar el archivo de origen es el primer paso en **how to export CAD** a un documento PDF.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Paso 2: Crear opciones de rasterización

Define las dimensiones de página objetivo. También puedes usar este bloque para **set CAD page size** manualmente si prefieres un diseño personalizado.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Paso 3: Establecer Auto Layout Scaling

Habilita la función de escalado automático. Este es el núcleo de **how to set scaling** para una conversión CAD‑to‑PDF.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

### Paso 4: Crear opciones de PDF

Vincula la configuración de rasterización a las opciones de exportación PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Paso 5: Exportar a PDF

Finalmente, guarda la imagen renderizada como un archivo PDF. Este paso completa el flujo de trabajo **convert dxf to pdf**.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Repite los pasos anteriores para cualquier archivo CAD adicional que necesites procesar, ya sea **DWG**, **DWF** u otros formatos compatibles.

## Casos de uso comunes

| Escenario | ¿Por qué establecer un tamaño de página personalizado? |
|----------|--------------------------------------------------------|
| **Presentación de planos de construcción** | Alinea el PDF con los tamaños de hoja estándar A1/A2 requeridos por los organismos reguladores. |
| **Incrustación en manuales técnicos** | Garantiza que el dibujo encaje en el diseño predefinido del manual sin escalado adicional. |
| **Impresión de alta resolución** | Permite aumentar DPI (p. ej., `rasterizationOptions.setResolution(300)`) manteniendo consistentes las dimensiones de la página. |

## Problemas comunes y solución de problemas

| Síntoma | Causa probable | Solución |
|---------|----------------|----------|
| PDF en blanco | Opciones de rasterización no configuradas o ruta de archivo incorrecta | Verifica la ruta `srcFile` y asegura que `setPageWidth/Height` no sean cero |
| Escalado distorsionado | `setAutomaticLayoutsScaling` dejado en `false` | Habilita el escalado automático o calcula manualmente el factor de escalado |
| Capas faltantes | El DXF de origen contiene entidades no compatibles | Revisa las notas de la versión de Aspose.CAD para los tipos de entidad soportados |

## Preguntas frecuentes

**P: ¿Aspose.CAD for Java es compatible con todos los formatos de archivo CAD?**  
R: Aspose.CAD for Java soporta varios formatos CAD, incluidos DWG, DXF y DWF.

**P: ¿Puedo personalizar aún más las opciones de escalado?**  
R: Sí, la clase `CadRasterizationOptions` ofrece propiedades para ajustar finamente el escalado, DPI y otras configuraciones de rasterización.

**P: ¿Dónde puedo encontrar documentación adicional para Aspose.CAD for Java?**  
R: Consulta la [documentation](https://reference.aspose.com/cad/java/) para información detallada y ejemplos.

**P: ¿Hay una prueba gratuita disponible para Aspose.CAD for Java?**  
R: Sí, puedes explorar una [free trial](https://releases.aspose.com/) para experimentar con las capacidades de Aspose.CAD for Java.

**P: ¿Cómo puedo solicitar asistencia o participar en discusiones sobre Aspose.CAD for Java?**  
R: Visita el [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) para conectar con la comunidad y buscar soporte.

**Preguntas comunes adicionales**

**P: ¿Cómo convierto un archivo DWG a PDF en lugar de DXF?**  
R: El mismo código funciona; solo cambia la extensión del archivo en `srcFile` a `.dwg`.

**P: ¿Puedo establecer un DPI personalizado para PDFs de mayor resolución?**  
R: Sí, usa `rasterizationOptions.setResolution(300);` (o cualquier DPI que necesites).

**P: ¿Es posible incrustar fuentes en el PDF generado?**  
R: Aspose.CAD rasteriza el dibujo, por lo que las fuentes se renderizan como vectores; no se requiere incrustación de fuentes separada.

## Conclusión

Al seguir esta guía ahora sabes cómo **set custom page size** y **create PDF from CAD** usando Aspose.CAD for Java con Auto Layout Scaling. El proceso optimiza el flujo de trabajo **export CAD to PDF**, garantiza un escalado consistente y te ahorra tiempo valioso de desarrollo. Siéntete libre de experimentar con diferentes tamaños de página, resoluciones y formatos CAD para adaptarlos a las necesidades de tu proyecto, ya sea **converting DWG to PDF**, **increasing PDF resolution**, o construyendo un procesador por lotes **java CAD to PDF**.

---

**Last Updated:** 2026-02-15  
**Tested With:** Aspose.CAD for Java 24.12 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}