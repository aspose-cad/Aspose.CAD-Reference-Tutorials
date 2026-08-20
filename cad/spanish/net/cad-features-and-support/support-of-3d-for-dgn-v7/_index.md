---
date: 2026-03-29
description: Aprenda cómo configurar las opciones de rasterización CAD y exportar
  DGN a PDF con soporte 3D usando Aspose.CAD para .NET.
linktitle: Support of 3D for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Configurar opciones de rasterización CAD para DGN V7 3D
url: /es/net/cad-features-and-support/support-of-3d-for-dgn-v7/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Configurar opciones de rasterización CAD para DGN V7 3D

## Introducción

En este tutorial exhaustivo aprenderá **cómo configurar las opciones de rasterización CAD** para exportar un archivo DGN V7 3‑D a PDF usando Aspose.CAD para .NET. Ya sea que esté creando un visor CAD, una herramienta de informes o una canalización de conversión automatizada, dominar estas configuraciones le brinda un control preciso sobre el tamaño de página, el escalado del diseño, los colores de fondo y las vistas específicas que desea renderizar. Vamos a recorrer el proceso paso a paso.

## Respuestas rápidas
- **¿Qué significa “configurar opciones de rasterización CAD”?**  
  Se refiere a establecer propiedades como dimensiones de página, escalado, color de fondo y selección de diseño antes de convertir un archivo CAD a un formato raster (p. ej., PDF).
- **¿Cómo exportar DGN a PDF con soporte 3‑D?**  
  Cargue el DGN con `DgnImage`, defina `PdfOptions` + `CadRasterizationOptions`, luego llame a `Save`.
- **¿Necesito una licencia para uso en producción?**  
  Sí, se requiere una licencia comercial para el despliegue; hay una prueba gratuita disponible.
- **¿Qué versiones de .NET son compatibles?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **¿Puedo elegir vistas específicas para exportar?**  
  Absolutamente, establezca la matriz `Layouts` en las opciones de rasterización.

## ¿Qué significa “configurar opciones de rasterización CAD”?

Configurar opciones de rasterización CAD implica personalizar cómo se rasteriza (convierte de vector a bitmap o PDF) un dibujo CAD. Al ajustar estas configuraciones controla la salida visual, el rendimiento y el tamaño del archivo del documento resultante.

## ¿Por qué usar Aspose.CAD para la exportación DGN V7 3‑D?

- **Integración completa con .NET** – no se requieren COM ni DLL nativas.  
- **Soporta geometría 3‑D** – conserva la información de profundidad al renderizar a PDF.  
- **Control granular** – elija diseños exactos, escalado y colores de fondo.  
- **Multiplataforma** – funciona en Windows, Linux y macOS con .NET Core.

## Requisitos previos

Antes de comenzar, asegúrese de tener:

- **Aspose.CAD para .NET** – descárguelo desde [aquí](https://releases.aspose.com/cad/net/).  
- **Visual Studio** o cualquier IDE compatible con .NET.  
- **Un archivo DGN de ejemplo** – para esta guía usaremos `Nikon_D90_Camera.dgn` (incluido en el paquete de ejemplos de Aspose).  

Ahora que todo está listo, profundicemos en el código.

## Importar espacios de nombres

En su proyecto .NET, importe los espacios de nombres requeridos:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## Paso 1: Configurar el directorio de documentos

Cree una variable que apunte a la carpeta donde se encuentran su DGN de origen y los archivos de salida.

```csharp
string MyDir = "Your Document Directory";
```

## Paso 2: Cargar el archivo DGN

Cargue el archivo DGN como un `DgnImage`. Este objeto le brinda acceso a los datos CAD y al pipeline de rasterización.

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Paso 3: Configurar opciones de exportación PDF (Configurar opciones de rasterización CAD)

Aquí **configuramos las opciones de rasterización CAD** que determinan cómo se renderiza el modelo 3‑D a PDF. Puede ajustar el tamaño de página, habilitar el escalado automático de diseños, establecer un color de fondo y seleccionar los diseños (vistas) exactos que desea exportar.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Only export specified views
    }
};
```

## Paso 4: Guardar la imagen rasterizada

Finalmente, exporte el DGN a un archivo PDF usando las opciones que acaba de configurar.

```csharp
dgnImage.Save(outFile, options);
```

## Problemas comunes y soluciones

| Problema | Solución |
|----------|----------|
| **Salida PDF en blanco** | Verifique que la matriz `Layouts` contenga los identificadores de vista correctos presentes en el archivo DGN. |
| **Colores incorrectos** | Asegúrese de que `BackgroundColor` esté configurado al valor deseado; use `Color.White` para un fondo claro. |
| **Cuello de botella de rendimiento en archivos grandes** | Habilite `AutomaticLayoutsScaling` y considere reducir `PageWidth/PageHeight` para una resolución raster más pequeña. |
| **Excepción de licencia** | Instale una licencia válida de Aspose.CAD antes de cargar la imagen para evitar marcas de agua de prueba. |

## Preguntas frecuentes

**P: ¿Puedo usar Aspose.CAD para .NET con otros formatos de archivo CAD?**  
R: Sí, Aspose.CAD admite DWG, DXF, DWF, DGN y muchos más formatos.

**P: ¿Cómo puedo manejar excepciones al trabajar con Aspose.CAD?**  
R: Envuelva su código en un bloque `try‑catch` y examine `Aspose.CAD.CADException` para obtener información detallada del error.

**P: ¿Aspose.CAD es adecuado para proyectos comerciales?**  
R: Absolutamente. Puede adquirir una licencia [aquí](https://purchase.aspose.com/buy).

**P: ¿Puedo probar Aspose.CAD para .NET antes de comprar?**  
R: Sí, hay una prueba gratuita disponible [aquí](https://releases.aspose.com/).

**P: ¿Dónde puedo encontrar soporte comunitario para Aspose.CAD?**  
R: Únase al foro de discusión [aquí](https://forum.aspose.com/c/cad/19).

---

**Última actualización:** 2026-03-29  
**Probado con:** Aspose.CAD 24.11 para .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}