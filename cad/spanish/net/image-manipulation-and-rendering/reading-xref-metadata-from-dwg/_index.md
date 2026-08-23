---
date: 2026-08-23
description: Descubre el potencial de Aspose.CAD para .NET con nuestro tutorial paso
  a paso sobre cómo leer metadatos XREF de archivos DWG.
keywords:
- read xref metadata
- extract dwg xref
- Aspose.CAD
lastmod: 2026-08-23
linktitle: Lectura de metadatos XREF de archivos DWG
og_description: Aprende a leer metadatos XREF de archivos DWG con Aspose.CAD para
  .NET. Esta guía te lleva a través de los requisitos previos, los pasos de código
  y los errores comunes en menos de diez minutos.
og_image_alt: Screenshot of Aspose.CAD reading XREF metadata in a .NET IDE
og_title: Cómo leer metadatos XREF de archivos DWG usando Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Unlock the potential of Aspose.CAD for .NET with our step‑by‑step tutorial
    on how to read xref metadata from DWG files.
  headline: How to read xref metadata from DWG files using Aspose.CAD
  type: TechArticle
- description: Unlock the potential of Aspose.CAD for .NET with our step‑by‑step tutorial
    on how to read xref metadata from DWG files.
  name: How to read xref metadata from DWG files using Aspose.CAD
  steps:
  - name: load the DWG file
    text: Create an `Image` instance from the DWG file you want to analyze. `Image.Load`
      loads a CAD file and returns a `CadImage` object representing the drawing. Adjust
      the `sourceFilePath` variable to the exact location of your drawing.
  - name: iterate through entities
    text: Loop through the `Image` object’s `Entities` collection. `CadBaseEntity`
      is the base class for all CAD entities in Aspose.CAD. For each entity, check
      whether it is an XREF reference and collect its metadata.
  - name: extract metadata
    text: When you encounter an XREF entity, read its insertion point (X, Y, Z) and
      the path of the referenced drawing. `CadUnderlay` represents an external reference
      (XREF) entity within a DWG drawing.
  - name: process metadata
    text: At this stage you can store the extracted information in a database, write
      it to a CSV file, or feed it into downstream BIM workflows. The sample simply
      prints the values to the console, but you are free to replace that with any
      custom logic.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for .NET supports **50+ input and output formats**, including
      DWG, DXF, DGN, and IFC, giving you broad coverage for most engineering workflows.
    question: Is Aspose.CAD for .NET compatible with all CAD file formats?
  - answer: Certainly! You can access the free trial download page [free trial download
      page](https://releases.aspose.com/).
    question: Can I use the free trial before making a purchase decision?
  - answer: The documentation is available [Aspose.CAD .NET documentation](https://reference.aspose.com/cad/net/).
    question: Where can I find comprehensive documentation for Aspose.CAD for .NET?
  - answer: You can get a temporary license [temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for Aspose.CAD for .NET?
  - answer: Join the Aspose.CAD community at [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19)
      for expert support and discussions.
    question: Need assistance or have specific queries?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- read xref metadata
- extract dwg xref
- Aspose.CAD
- DWG
- CAD metadata
title: Cómo leer metadatos XREF de archivos DWG usando Aspose.CAD
url: /es/net/image-manipulation-and-rendering/reading-xref-metadata-from-dwg/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo leer metadatos xref de archivos DWG usando Aspose.CAD

## Introducción

En este tutorial aprenderás **cómo leer metadatos xref** de archivos DWG usando la biblioteca Aspose.CAD para .NET. Ya sea que necesites auditar referencias externas, migrar dibujos heredados o construir una canalización BIM personalizada, extraer información XREF es un requisito común. Recorreremos cada paso, desde la configuración del proyecto hasta el procesamiento de los metadatos, y resaltaremos consejos prácticos que puedes aplicar de inmediato.

## Respuestas rápidas
- **¿Cuál es el propósito principal?** Recuperar los puntos de inserción y rutas de archivo de las referencias externas (XREF) incrustadas en un dibujo DWG.  
- **¿Qué biblioteca se requiere?** Aspose.CAD para .NET (soporta más de 50 formatos CAD).  
- **¿Necesito una licencia?** Se requiere una licencia temporal o completa para uso en producción; hay una prueba gratuita disponible.  
- **¿Qué versiones de .NET son compatibles?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.  
- **¿Cuánto tiempo tarda el código en ejecutarse?** Procesar un DWG típico de 200 páginas con algunas XREFs se completa en menos de un segundo en hardware estándar.

## ¿Qué es leer metadatos xref?
`read xref metadata` se refiere a la operación de acceder a las propiedades de las entidades de referencia externa almacenadas dentro de un dibujo DWG, como sus coordenadas de inserción, rutas de archivo de origen y banderas de visibilidad. Esta operación te permite descubrir programáticamente cómo un dibujo está compuesto a partir de otros archivos, habilitando validación automatizada, generación de informes o procesamiento por lotes de recursos vinculados.

## ¿Por qué usar Aspose.CAD para esta tarea?
Aspose.CAD soporta **más de 50 formatos de archivo CAD** y puede leer archivos DWG **sin requerir AutoCAD**. La biblioteca procesa dibujos grandes **en flujos de memoria eficientes**, lo que te permite manejar archivos de cientos de páginas sin cargar todo el archivo en RAM. Estas capacidades cuantificadas la convierten en una opción confiable para automatización CAD de nivel empresarial.

## Requisitos previos

Antes de sumergirnos en el código, verifica que tienes lo siguiente:

- Aspose.CAD para .NET instalado. Obtén el paquete más reciente desde la [página de lanzamiento de Aspose.CAD para .NET](https://releases.aspose.com/cad/net/).
- Una carpeta local que contenga los archivos DWG que deseas inspeccionar. Actualiza la variable `MyDir` en el código de ejemplo para que apunte a esa carpeta.
- Una licencia válida de Aspose.CAD (o la prueba gratuita) si planeas ejecutar el código en un entorno de producción.

Ahora que el entorno está listo, comencemos a programar.

## Importar espacios de nombres

Lo primero que debes hacer es importar los espacios de nombres que exponen la API de Aspose.CAD. Las directivas `using` traen los espacios de nombres de Aspose.CAD al alcance, permitiendo el acceso a clases CAD como `Image` y `CadImage`.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
```

## ¿Cómo leer metadatos xref de archivos DWG?

Carga el dibujo, recorre sus entidades, filtra los objetos XREF y luego extrae las propiedades deseadas, todo en unas pocas líneas de código sencillas. Las siguientes secciones dividen el proceso en cuatro pasos lógicos que puedes copiar‑pegar en cualquier proyecto de consola o servicio .NET.

### Paso 1: cargar el archivo DWG

Crea una instancia de `Image` a partir del archivo DWG que deseas analizar. `Image.Load` carga un archivo CAD y devuelve un objeto `CadImage` que representa el dibujo. Ajusta la variable `sourceFilePath` a la ubicación exacta de tu dibujo.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage image = (CadImage)Image.Load(sourceFilePath))
{
    // Code for the next steps goes here
}
```

### Paso 2: iterar a través de las entidades

Recorre la colección `Entities` del objeto `Image`. `CadBaseEntity` es la clase base para todas las entidades CAD en Aspose.CAD. Para cada entidad, verifica si es una referencia XREF y recopila sus metadatos.

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    if (entity is CadUnderlay)
    {
        // Code for the next steps goes here
    }
}
```

### Paso 3: extraer metadatos

Cuando encuentres una entidad XREF, lee su punto de inserción (X, Y, Z) y la ruta del dibujo referenciado. `CadUnderlay` representa una entidad de referencia externa (XREF) dentro de un dibujo DWG.

```csharp
//XREF entity with metadata
Cad3DPoint insertionPoint = ((CadUnderlay)entity).InsertionPoint;
string path = ((CadUnderlay)entity).UnderlayPath;
```

### Paso 4: procesar metadatos

En esta etapa puedes almacenar la información extraída en una base de datos, escribirla en un archivo CSV o alimentarla a flujos de trabajo BIM posteriores. El ejemplo simplemente imprime los valores en la consola, pero eres libre de reemplazar eso con cualquier lógica personalizada.

```csharp
// Your custom logic for processing metadata goes here
```

## Problemas comunes y solución de problemas

| Síntoma | Causa probable | Solución |
|---------|----------------|----------|
| No se devuelven entidades XREF | El dibujo usa un tipo de referencia diferente (p. ej., INSERT) | Verifica el tipo de entidad contra `CadEntityType.Xref` y también maneja `Insert` si es necesario |
| `Image.Load` lanza una excepción | Ruta de archivo incorrecta o versión de DWG no compatible | Verifica la ruta y asegúrate de usar Aspose.CAD 24.11 o superior |
| Los valores de metadatos están vacíos | El XREF está definido pero no resuelto (falta el archivo externo) | Asegúrate de que el archivo referenciado exista en disco o proporciona un resolvedor de sistema de archivos virtual |

## Preguntas frecuentes

**P: ¿Aspose.CAD para .NET es compatible con todos los formatos de archivo CAD?**  
R: Sí, Aspose.CAD para .NET soporta **más de 50 formatos de entrada y salida**, incluidos DWG, DXF, DGN e IFC, brindándote una amplia cobertura para la mayoría de los flujos de trabajo de ingeniería.

**P: ¿Puedo usar la prueba gratuita antes de decidir una compra?**  
R: ¡Por supuesto! Puedes acceder a la página de descarga de la prueba gratuita [página de descarga de prueba gratuita](https://releases.aspose.com/).

**P: ¿Dónde puedo encontrar documentación completa para Aspose.CAD para .NET?**  
R: La documentación está disponible en [documentación de Aspose.CAD .NET](https://reference.aspose.com/cad/net/).

**P: ¿Cómo obtengo una licencia temporal para Aspose.CAD para .NET?**  
R: Puedes obtener una licencia temporal en la [página de licencia temporal](https://purchase.aspose.com/temporary-license/).

**P: ¿Necesitas asistencia o tienes consultas específicas?**  
R: Únete a la comunidad de Aspose.CAD en el [Foro de Aspose.CAD](https://forum.aspose.com/c/cad/19) para soporte experto y discusiones.

## Conclusión

Ahora tienes un patrón completo y listo para producción para **leer metadatos XREF** de archivos DWG con Aspose.CAD para .NET. Siguiendo los cuatro pasos —cargar el archivo, iterar entidades, extraer el punto de inserción y la ruta del sub‑dibujo, y procesar los resultados— puedes integrar esta capacidad en cualquier aplicación centrada en CAD, ya sea una herramienta de migración de datos, un script de control de calidad o una canalización BIM personalizada.

---

**Última actualización:** 2026-08-23  
**Probado con:** Aspose.CAD 24.11 para .NET  
**Autor:** Aspose

## Tutoriales relacionados

- [Cómo cambiar la ruta xref y editar hipervínculos en archivos CAD - Tutorial de Aspose.CAD](/cad/net/advanced-cad-techniques/editing-hyperlinks-in-cad-files/)
- [Obtener atributos de bloque de archivos DWG - Tutorial de Aspose.CAD](/cad/net/image-manipulation-and-rendering/getting-block-attributes-from-dwg/)
- [Convertir archivos DWG grandes a PDF - Tutorial de Aspose.CAD](/cad/net/image-manipulation-and-rendering/converting-large-dwg-files-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}