---
title: Conversión de DWG a PDF con coordenadas en C# - Tutorial de Aspose.CAD
linktitle: Conversión de DWG a PDF con coordenadas en C#
second_title: Aspose.CAD .NET - Formato de archivo CAD y BIM
description: Aprenda a convertir DWG a PDF con coordenadas específicas en C# usando Aspose.CAD. Siga nuestra guía paso a paso para realizar conversiones de archivos CAD precisas y eficientes.
type: docs
weight: 11
url: /es/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
---
## Introducción

Bienvenido a este tutorial completo sobre cómo convertir archivos DWG a PDF con coordenadas específicas usando Aspose.CAD para .NET. Aspose.CAD es una potente biblioteca que permite a los desarrolladores trabajar sin problemas con formatos de archivos CAD en sus aplicaciones .NET. En este tutorial, lo guiaremos a través del proceso de convertir un archivo DWG a PDF y le proporcionaremos coordenadas específicas para mejorar la precisión.

## Requisitos previos

Antes de comenzar, asegúrese de tener los siguientes requisitos previos:

-  Biblioteca Aspose.CAD: descargue e instale la biblioteca Aspose.CAD para .NET. Puedes encontrar la biblioteca.[aquí](https://releases.aspose.com/cad/net/).

- Entorno de desarrollo: asegúrese de tener configurado un entorno de desarrollo compatible, incluido Visual Studio o cualquier otro IDE preferido.

- Archivo DWG: tenga un archivo DWG listo para la conversión. Puede utilizar el archivo de ejemplo proporcionado o su archivo DWG personalizado.

## Importar espacios de nombres

En su proyecto C#, importe los espacios de nombres necesarios:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

Dividamos el código en una guía paso a paso para una mejor comprensión:

## Paso 1: definir el directorio de documentos

```csharp
string MyDir = "Your Document Directory";
```

## Paso 2: Establecer la ruta del archivo DWG de origen

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## Paso 3: cargar el archivo DWG y configurar las opciones de rasterización

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## Paso 4: definir coordenadas y ventana gráfica

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## Paso 5: aplicar la configuración de la ventana gráfica

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## Paso 6: configurar las opciones de PDF y exportar

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## Paso 7: Mostrar mensaje de éxito

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Conclusión

¡Felicidades! Ha convertido con éxito un archivo DWG a PDF con coordenadas especificadas utilizando Aspose.CAD para .NET. Este tutorial cubrió pasos esenciales y proporcionó una guía clara para los desarrolladores.

## Preguntas frecuentes

### P1: ¿Puedo utilizar Aspose.CAD con otros formatos de archivos CAD?

R1: Sí, Aspose.CAD admite varios formatos CAD, incluidos DWG, DXF, DWF y más.

### P2: ¿Cómo puedo manejar los errores durante el proceso de conversión?

A2: Implemente mecanismos de manejo de errores utilizando bloques try-catch para capturar y administrar excepciones.

### P3: ¿Aspose.CAD es adecuado para entornos Windows y Linux?

R3: Sí, Aspose.CAD es compatible con las plataformas Windows y Linux.

### P4: ¿Puedo personalizar aún más la salida del PDF?

R4: ¡Por supuesto! Explore las amplias opciones proporcionadas por Aspose.CAD para adaptar la salida PDF a sus requisitos específicos.

### P5: ¿Dónde puedo encontrar apoyo adicional o debates comunitarios?

 A5: Visita el[Foro Aspose.CAD](https://forum.aspose.com/c/cad/19) para apoyo y debates de la comunidad.