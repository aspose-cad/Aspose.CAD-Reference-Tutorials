---
title: Exportación de archivos DGN integrados - Tutorial de Aspose.CAD
linktitle: Exportación de archivos DGN integrados
second_title: Aspose.CAD .NET - Formato de archivo CAD y BIM
description: Explore el poder de Aspose.CAD para .NET. Aprenda a exportar archivos DGN incrustados a PDF sin esfuerzo con este tutorial paso a paso.
type: docs
weight: 14
url: /es/net/export-techniques/exporting-embedded-dgn-files/
---
## Introducción

En el dinámico mundo del desarrollo de software, Aspose.CAD para .NET se destaca como una poderosa herramienta para manejar archivos de diseño asistido por computadora (CAD). Este tutorial lo guiará a través del proceso de exportación de archivos DGN incrustados usando Aspose.CAD para .NET. Ya sea que sea un desarrollador experimentado o un principiante curioso, esta guía paso a paso lo ayudará a aprovechar las capacidades de Aspose.CAD de manera efectiva.

## Requisitos previos

Antes de sumergirse en el tutorial, asegúrese de cumplir con los siguientes requisitos previos:

1.  Aspose.CAD para .NET: descargue e instale la biblioteca desde[Aspose.CAD para .NET](https://releases.aspose.com/cad/net/).

2. Entorno de desarrollo: configure un entorno de desarrollo .NET con Visual Studio o cualquier otro IDE preferido.

3. Archivo DXF de muestra: para este tutorial, usaremos el archivo "conic_pyramid.dxf". Asegúrese de tenerlo disponible en su directorio de documentos designado.

## Importar espacios de nombres

En su código C#, asegúrese de importar los espacios de nombres necesarios:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Paso 1: cargue el archivo DXF

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Su código para pasos adicionales irá aquí
}
```

## Paso 2: configurar las opciones de rasterización

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new[] { "Model" };
```

## Paso 3: configurar las opciones de PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Paso 4: guardar como PDF

```csharp
cadImage.Save(MyDir + "conic_pyramid.pdf", pdfOptions);
```

## Paso 5: Mostrar mensaje de éxito

```csharp
Console.WriteLine("\nThe DXF drawing exported successfully to PDF.\nFile saved at " + MyDir);
```

## Conclusión

¡Felicidades! Ha exportado exitosamente un archivo DGN incrustado a PDF usando Aspose.CAD para .NET. Este tutorial cubrió los pasos esenciales, brindándole una base para explorar funcionalidades más avanzadas que ofrece Aspose.CAD.

## Preguntas frecuentes

### P1: ¿Puedo usar Aspose.CAD para .NET con otros lenguajes de programación?

R1: Aspose.CAD admite principalmente .NET, pero Aspose proporciona bibliotecas para varios lenguajes, incluidos Java y Python.

### P2: ¿Hay una prueba gratuita disponible de Aspose.CAD para .NET?

 R2: Sí, puedes obtener una prueba gratuita desde[aquí](https://releases.aspose.com/).

### P3: ¿Dónde puedo encontrar documentación completa sobre Aspose.CAD para .NET?

 A3: consulte la documentación[aquí](https://reference.aspose.com/cad/net/).

### P4: ¿Cómo obtengo una licencia temporal de Aspose.CAD para .NET?

 A4: Obtener una licencia temporal[aquí](https://purchase.aspose.com/temporary-license/).

### P5: ¿Necesita ayuda o desea interactuar con la comunidad?

 A5: Visita el[Foro Aspose.CAD](https://forum.aspose.com/c/cad/19) para apoyo y discusiones.