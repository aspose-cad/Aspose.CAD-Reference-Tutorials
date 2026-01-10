---
date: 2026-01-10
description: Aprenda cómo exportar DGN a DWG y convertir MicroStation DGN a AutoCAD
  DWG usando Aspose.CAD para Java. Guía paso a paso.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD Java API
title: Exportar DGN a DWG con Aspose.CAD para Java
url: /es/java/dgn-export-options/export-dgn-as-part-of-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar DGN a DWG con Aspose.CAD para Java

## Introducción

En este tutorial, aprenderás a **exportar dgn a dwg** e incrustar un diseño MicroStation DGN dentro de un archivo AutoCAD DWG usando la biblioteca Aspose.CAD para Java. Ya sea que estés migrando dibujos legados de MicroStation o necesites combinar superposiciones DGN con diseños DWG, esta guía te acompañará paso a paso—desde la configuración del entorno hasta la generación de una vista previa en PDF del DWG final.

## Respuestas rápidas
- **¿Qué logra “exportar dgn a dwg”?** Inserta una superposición DGN en un DWG, permitiendo su visualización sin problemas en AutoCAD.
- **¿A qué formato puedo exportar el resultado para una vista previa rápida?** Puedes **exportar el archivo CAD a pdf** usando `PdfOptions`.
- **¿Necesito una licencia para ejecutar el código?** Se requiere una licencia temporal o de pago de Aspose.CAD para uso en producción.
- **¿Qué versión de Java es compatible?** Java 8 o posterior funciona con la última versión de Aspose.CAD para Java.
- **¿Hay una prueba gratuita disponible?** Sí – descarga una prueba desde el sitio web de Aspose.

## ¿Qué es “exportar dgn a dwg”?
Exportar DGN a DWG significa convertir o incrustar un diseño MicroStation DGN como una superposición dentro de un dibujo AutoCAD DWG. Esto permite a los profesionales de CAD aprovechar los activos DGN existentes sin recrear la geometría desde cero.

## ¿Por qué convertir MicroStation DGN a AutoCAD DWG?
- **Colaboración:** Los equipos que usan AutoCAD pueden ver y editar contenido DGN directamente.
- **Estandarización:** DWG es el formato de facto para muchos flujos de trabajo posteriores (p. ej., generación de PDF, renderizado 3D).
- **Preservación:** Mantiene intactas las referencias DGN originales, reduciendo la pérdida de datos.

## Requisitos previos

Antes de sumergirnos en el tutorial, asegúrate de contar con los siguientes requisitos:
1. **Biblioteca Aspose.CAD:** Descarga e instala la biblioteca Aspose.CAD para Java. Puedes encontrar la biblioteca [aquí](https://releases.aspose.com/cad/java/).
2. **Java Development Kit (JDK):** Asegúrate de tener Java instalado en tu sistema.
3. **Entorno de Desarrollo Integrado (IDE):** Elige un IDE Java como Eclipse o IntelliJ para una experiencia de desarrollo más fluida.

## Importar paquetes

En tu proyecto Java, importa los paquetes necesarios de Aspose.CAD para habilitar la manipulación de archivos CAD. Aquí tienes un ejemplo:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Paso 1: Definir rutas de archivo

Define las rutas de archivo de entrada y salida para el archivo DWG. Actualiza las variables `dataDir`, `fileName` y `outPath` según corresponda.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Paso 2: Crear instancia de PdfOptions

Crea una instancia de la clase `PdfOptions`, ya que estamos **exportando el archivo CAD a PDF** para una verificación rápida.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Paso 3: Cargar archivo DWG

Carga el archivo DWG existente como una imagen y conviértelo al tipo `CadImage`.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Paso 4: Recorrer entidades

Recorre cada entidad dentro del archivo DWG y verifica si es una definición de imagen. Si lo es, recupera la referencia externa al objeto.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Paso 5: Definir opciones de rasterización

Define la configuración para el objeto `CadRasterizationOptions`, incluyendo ancho y alto de página, diseños y color de fondo.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## Paso 6: Establecer opciones de rasterización vectorial

Configura las opciones de rasterización vectorial para la exportación.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Paso 7: Exportar DWG a PDF

Finalmente, exporta el DWG a PDF llamando al método `save`.

```java
cadImage.save(outPath, exportOptions);
```

## Problemas comunes y soluciones

| Problema | Causa | Solución |
|----------|-------|----------|
| **No aparece la superposición DGN** | El DWG no contiene una entidad `DGNUNDERLAY`. | Verifica que el DWG de origen incluya una referencia DGN. |
| **El PDF está en blanco** | Las opciones de rasterización están configuradas con tamaño cero o con el diseño incorrecto. | Asegúrate de que `setPageWidth`/`setPageHeight` sean valores positivos y que `setLayouts` coincida con el nombre del diseño DWG. |
| **Excepción de licencia** | Ejecución sin una licencia válida de Aspose.CAD. | Aplica una licencia temporal o comprada antes de llamar a cualquier método de la API. |

## Preguntas frecuentes

### P1: ¿Dónde puedo encontrar la documentación de Aspose.CAD para Java?

R1: La documentación está disponible [aquí](https://reference.aspose.com/cad/java/).

### P2: ¿Cómo puedo descargar la biblioteca Aspose.CAD para Java?

R2: Puedes descargar la biblioteca desde [este enlace](https://releases.aspose.com/cad/java/).

### P3: ¿Hay una prueba gratuita disponible para Aspose.CAD para Java?

R3: Sí, puedes encontrar la prueba gratuita [aquí](https://releases.aspose.com/).

### P4: ¿Dónde puedo obtener una licencia temporal para Aspose.CAD para Java?

R4: Obtén una licencia temporal [aquí](https://purchase.aspose.com/temporary-license/).

### P5: ¿Necesito ayuda o tengo preguntas?

R5: Visita el foro de soporte de la comunidad Aspose.CAD [aquí](https://forum.aspose.com/c/cad/19).

### P6: ¿Puedo convertir el PDF resultante de nuevo a DWG?

R6: El PDF es una vista previa rasterizada; la conversión de vuelta a DWG requiere una herramienta de ingeniería inversa separada.

### P7: ¿Este enfoque funciona con otros formatos CAD como DWF o DXF?

R7: Sí, Aspose.CAD admite muchos formatos; solo necesitas ajustar las extensiones de archivo y la configuración de rasterización según corresponda.

---

**Última actualización:** 2026-01-10  
**Probado con:** Aspose.CAD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}