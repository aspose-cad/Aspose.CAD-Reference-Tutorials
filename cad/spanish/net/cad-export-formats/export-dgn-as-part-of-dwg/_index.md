---
date: 2026-03-21
description: Aprenda cómo crear PDF a partir de DWG y exportar DGN como parte de DWG
  usando Aspose.CAD para .NET. Esta guía también muestra cómo convertir DWG a PDF
  y configurar las opciones de PDF.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Crear PDF a partir de DWG y exportar DGN como parte de DWG – Aspose.CAD para
  .NET
url: /es/net/cad-export-formats/export-dgn-as-part-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crear PDF a partir de DWG y Exportar DGN como Parte de DWG – Aspose.CAD para .NET

## Introducción

Si necesitas **crear PDF a partir de DWG** mientras también incrustas un diseño DGN como parte del DWG, Aspose.CAD para .NET lo hace sencillo. En este tutorial recorreremos todo el flujo de trabajo: cargar un DWG, localizar la superposición DGN incrustada, configurar las opciones de rasterización y, finalmente, exportar el resultado a un documento PDF. Ya sea que estés construyendo una herramienta de conversión por lotes, un motor de informes o un servicio de integración CAD‑BIM, los pasos a continuación te proporcionarán una base sólida y lista para producción.

## Respuestas rápidas
- **¿Qué biblioteca maneja la conversión DWG → PDF?** Aspose.CAD para .NET  
- **¿Puedo exportar una superposición DGN mientras creo el PDF?** Sí – la superposición se accede mediante `CadDgnUnderlay`.  
- **¿Qué método establece las opciones de PDF?** `PdfOptions` junto con `CadRasterizationOptions`.  
- **¿Necesito una licencia para uso comercial?** Sí, se requiere una licencia válida de Aspose.CAD.  
- **¿Versiones .NET compatibles?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## ¿Qué es “crear PDF a partir de DWG”?

Crear un PDF a partir de un archivo DWG significa renderizar el dibujo vectorial en un documento PDF rasterizado o basado en vectores. Este proceso es útil para compartir dibujos con partes interesadas que no disponen de software CAD, para archivado o para generar informes imprimibles. Aspose.CAD simplifica la tarea al encargarse del pesado análisis de entidades DWG y ofrecer un control granular sobre la salida mediante `PdfOptions`.

## ¿Por qué exportar DGN como parte de un DWG?

Una superposición DGN suele representar geometría de referencia de proyectos MicroStation. Al exportar el DGN junto con el DWG preservas el contexto de diseño original, asegurando que los consumidores posteriores vean el conjunto completo de dibujos. Esto es especialmente valioso en proyectos multidisciplinarios donde coexisten archivos DWG y DGN.

## Requisitos previos

- **Aspose.CAD para .NET** – descárgalo [aquí](https://releases.aspose.com/cad/net/).  
- **Entorno de desarrollo** – Visual Studio (cualquier versión reciente) o tu IDE .NET preferido.  
- **Conocimientos básicos de C#** – deberías estar cómodo con la sintaxis de C# y la estructura de proyectos .NET.

## Importar espacios de nombres

Agrega las directivas `using` requeridas al inicio de tu archivo fuente C#:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Guía paso a paso

### Paso 1: Definir rutas de archivo

Establece el archivo DWG de entrada y el nombre del PDF de salida.

```csharp
// Input and Output file paths
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

### Paso 2: Crear instancia de `PdfOptions` (establecer opciones de pdf)

`PdfOptions` te permite controlar cómo se genera el PDF, como el tamaño de página, compresión y metadatos.

```csharp
// Create an instance of PdfOptions class for exporting DWG to PDF
PdfOptions exportOptions = new PdfOptions();
```

### Paso 3: Cargar el archivo DWG

Carga el DWG como un `CadImage` para que puedas inspeccionar sus entidades.

```csharp
// Load the existing DWG file as an image and convert it to CadImage type
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

### Paso 4: Iterar a través de las entidades

Recorre cada entidad del dibujo para localizar la superposición DGN.

```csharp
// Iterate through each entity inside the DWG file
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

### Paso 5: Verificar tipo de entidad (cómo exportar dgn)

Identifica si la entidad actual es una superposición DGN.

```csharp
// Check if the entity is an image definition
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

### Paso 6: Obtener ruta de la superposición

Recupera la ruta de referencia externa del archivo DGN.

```csharp
// If it's an image definition, get the external reference to the object
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

### Paso 7: Definir opciones de rasterización (convertir dwg a pdf)

Configura cómo se rasteriza el DWG antes de insertarlo en el PDF.

```csharp
// Define settings for CadRasterizationOptions object
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

### Paso 8: Exportar DWG a PDF

Finalmente, guarda la imagen renderizada como un archivo PDF.

```csharp
// Export the DWG to PDF by calling Save method
cadImage.Save(outPath, exportOptions);
```

## Problemas comunes y soluciones

| Problema | Razón | Solución |
|----------|-------|----------|
| **`Image.Load` throws “File not found”** | Ruta incorrecta o archivo faltante. | Usa una ruta absoluta o asegura que el DWG se copie a la carpeta de salida. |
| **Underlay path is empty** | La superposición DGN no está incrustada o la referencia está rota. | Verifica que el DWG realmente contenga una superposición DGN y que el archivo DGN externo sea accesible. |
| **PDF output is blank** | Las opciones de rasterización están configuradas con tamaño cero. | Ajusta `PageWidth`/`PageHeight` o establece `NoScaling = false`. |
| **License exception** | Ejecutándose sin una licencia válida de Aspose.CAD. | Aplica la licencia antes de cargar la imagen: `License lic = new License(); lic.SetLicense("Aspose.CAD.lic");` |

## Preguntas frecuentes

### P1: ¿Puedo usar Aspose.CAD para .NET en mis proyectos comerciales?
A1: Sí, puedes. Visita [aquí](https://purchase.aspose.com/buy) para explorar opciones de licencia.

### P2: ¿Existen limitaciones en el tamaño de los archivos DWG que puedo procesar?
A2: Aspose.CAD soporta el manejo de archivos DWG grandes, pero pueden aplicarse limitaciones de hardware.

### P3: ¿Hay una versión de prueba disponible?
A3: Sí, puedes obtener una prueba gratuita [aquí](https://releases.aspose.com/).

### P4: ¿Cómo puedo obtener licencias temporales?
A4: Las licencias temporales se pueden obtener [aquí](https://purchase.aspose.com/temporary-license/).

### P5: ¿Dónde puedo buscar asistencia si encuentro problemas?
A5: Puedes visitar el foro de Aspose.CAD [aquí](https://forum.aspose.com/c/cad/19) para obtener soporte.

**P: ¿Cómo configuro metadatos PDF adicionales (autor, título, etc.)?**  
R: Usa las propiedades `exportOptions.Metadata` antes de llamar a `Save`.

**P: ¿Puedo exportar varios diseños en páginas PDF separadas?**  
R: Sí – establece `Layouts = new string[] { "Layout1", "Layout2" }` en `CadRasterizationOptions`.

**P: ¿Aspose.CAD admite la conversión de DWG a otros formatos de imagen?**  
R: Absolutamente. Puedes exportar a PNG, JPEG, SVG y más usando las sobrecargas correspondientes de `Image.Save`.

**Última actualización:** 2026-03-21  
**Probado con:** Aspose.CAD 24.11 para .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}