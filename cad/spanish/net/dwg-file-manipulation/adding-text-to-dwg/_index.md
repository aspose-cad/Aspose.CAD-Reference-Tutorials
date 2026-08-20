---
date: 2026-04-06
description: Aprende a convertir DWG a PDF y agregar texto personalizado usando C#
  y Aspose.CAD. Esta guía paso a paso cubre la generación de PDF a partir de DWG,
  la inserción de una entidad de texto y el cambio de la fuente del texto en DWG.
keywords:
- convert dwg to pdf
- generate pdf from dwg
- insert text entity
- change dwg text font
- aspose cad dwg pdf
linktitle: Agregar texto a archivos DWG en C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Convertir DWG a PDF y agregar texto en C# – Tutorial de Aspose.CAD
url: /es/net/dwg-file-manipulation/adding-text-to-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir DWG a PDF y Añadir Texto en C# – Tutorial de Aspose.CAD

## Introducción

En el mundo de rápido movimiento del CAD y el desarrollo .NET, **convertir DWG a PDF** mientras se insertan anotaciones personalizadas es un requisito frecuente. Ya sea que necesites generar dibujos imprimibles para clientes o incrustar notas dinámicas directamente en un DWG, Aspose.CAD hace el trabajo sencillo. En este tutorial aprenderás a **convertir DWG a PDF**, **añadir una entidad de texto**, e incluso **cambiar la fuente del texto DWG** usando C#.

## Respuestas rápidas
- **¿Qué biblioteca es la mejor para la conversión de DWG a PDF?** Aspose.CAD para .NET  
- **¿Puedo añadir texto personalizado durante la conversión?** Sí – crea una entidad `CadText` y añádela antes de guardar.  
- **¿Necesito una licencia para uso en producción?** Se requiere una licencia comercial; hay una prueba gratuita disponible.  
- **¿Qué versiones de .NET son compatibles?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **¿Es posible cambiar la fuente del texto?** Sí, ajusta las propiedades de `CadText` como `StyleType` y `TextHeight`.

## ¿Qué es “convertir dwg a pdf”?

Convertir un archivo DWG a PDF transforma un dibujo CAD basado en vectores en un documento ampliamente compartible e independiente del dispositivo. El PDF conserva la geometría y capas originales, mientras permite incrustar anotaciones, texto u otros metadatos. Aspose.CAD maneja la rasterización y el renderizado vectorial automáticamente, por lo que no necesitas ningún software CAD de terceros en el servidor.

## ¿Por qué añadir texto a un DWG antes de la conversión?

Incrustar texto directamente en el DWG te brinda control total sobre la ubicación, estilo y asignación de capas. Cuando el archivo se convierte posteriormente a PDF, el texto aparece exactamente donde lo posicionaste, preservando la intención del diseño y eliminando la necesidad de post‑procesamiento en un editor de PDF.

## Requisitos previos

Antes de comenzar, asegúrate de tener:

- **Biblioteca Aspose.CAD** – descárgala desde el [enlace de descarga](https://releases.aspose.com/cad/net/).  
- **Un entorno .NET funcional** (Visual Studio 2022, .NET 6, o cualquier versión compatible).  
- **Una carpeta para tus archivos de prueba** – la llamaremos `MyDir` a lo largo de la guía.

Ahora, vamos a recorrer el proceso paso a paso.

## Importar espacios de nombres

Añade las declaraciones `using` requeridas para que puedas acceder a las clases de Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
using Aspose.CAD.ImageOptions;
```

## Paso 1: Cargar el archivo DWG

Carga tu archivo DWG fuente en un objeto `Image`. Este objeto te brinda acceso a las entidades CAD subyacentes.

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Subsequent steps will be performed inside this block
}
```

## Paso 2: Crear un objeto CadText (Insertar entidad de texto)

La clase `CadText` representa una sola línea de texto en un DWG. Aquí establecemos su estilo, valor, color, capa y posición. Ajusta `StyleType` o `TextHeight` para **cambiar la fuente del texto DWG**.

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";          // Font/style – change to alter DWG text font
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;                    // 256 = ByLayer (you can use a specific ACI color)
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;                 // Height influences visual size
cadText.ScaleX = 0.0;
```

## Paso 3: Añadir la entidad de texto al Model Space

El Model Space del DWG contiene la mayoría de las entidades del dibujo. Al añadir nuestro `CadText` al bloque `*Model_Space`, el texto pasa a ser parte del dibujo.

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## Paso 4: Configurar opciones PDF (Generar PDF a partir de DWG)

Configura las opciones de rasterización que controlan cómo se renderiza el DWG en un PDF. Puedes ajustar el tamaño de página, tipo de dibujo y diseño.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Paso 5: Guardar el DWG modificado como PDF

Finalmente, exporta el dibujo modificado. El PDF resultante incluye el texto recién insertado.

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

> **Consejo profesional:** Si necesitas un PDF de mayor resolución, incrementa `PageHeight` y `PageWidth` proporcionalmente.

## Problemas comunes y soluciones

| Problema | Razón | Solución |
|----------|-------|----------|
| El texto no aparece en el PDF | Capa o ID de color incorrectos | Asegúrate de que `LayerName` exista y `ColorId` esté configurado a un color visible (p.ej., 7 para blanco). |
| El texto está mal ubicado | Coordenadas de alineación incorrectas | Verifica los valores `FirstAlignment.X/Y` en relación con las unidades del dibujo. |
| El PDF está en blanco | Opciones de rasterización no configuradas | Configura `DrawType` a `UseObjectColor` o `UseObjectLineWeight`. |

## Preguntas frecuentes (existentes)

### P1: ¿Es Aspose.CAD compatible con todas las versiones de archivos DWG?

**R1:** Aspose.CAD admite una amplia gama de versiones de archivos DWG, garantizando compatibilidad con varios software CAD.

### P2: ¿Puedo añadir múltiples entidades de texto a un solo archivo DWG usando Aspose.CAD?

**R2:** Sí, puedes añadir múltiples entidades de texto a un archivo DWG repitiendo el proceso descrito en el tutorial.

### P3: ¿Cómo puedo cambiar la fuente y el estilo del texto en Aspose.CAD?

**R3:** Para modificar la fuente y el estilo del texto, ajusta las propiedades del objeto `CadText` antes de añadirlo al archivo DWG.

### P4: ¿Existen consideraciones de licencia al usar Aspose.CAD en un proyecto comercial?

**R5:** Sí, asegúrate de cumplir con los términos de licencia de Aspose.CAD. Consulta [Aspose.CAD Purchase](https://purchase.aspose.com/buy) para más detalles.

### P5: ¿Dónde puedo buscar ayuda o discutir consultas relacionadas con Aspose.CAD?

**R5:** Visita el [foro de Aspose.CAD](https://forum.aspose.com/c/cad/19) para conectar con la comunidad y obtener soporte.

## Preguntas frecuentes adicionales

**P:** ¿Cómo genero PDF a partir de DWG sin añadir texto?  
**R:** Omite el paso de creación de `CadText` y configura directamente `PdfOptions` antes de llamar a `image.Save(...)`.

**P:** ¿Puedo cambiar el color del texto programáticamente?  
**R:** Sí, establece `cadText.ColorId` a un número de color ACI específico (p.ej., 1 para rojo).

**P:** ¿Es posible insertar texto multilínea?  
**R:** Usa `CadMText` para bloques de texto multilínea; el enfoque es similar al de `CadText`.

**P:** ¿Aspose.CAD admite la conversión por lotes de varios archivos DWG?  
**R:** Absolutamente – recorre un directorio de archivos DWG, aplica los mismos pasos y guarda cada uno como PDF.

## Conclusión

Ahora tienes un flujo de trabajo completo y listo para producción para **convertir DWG a PDF**, **añadir texto personalizado** y **personalizar la apariencia del texto** usando C# y Aspose.CAD. Esta técnica es ideal para la generación automática de dibujos, pipelines de informes o cualquier escenario donde necesites enriquecer archivos CAD al vuelo.

---

**Last Updated:** 2026-04-06  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}