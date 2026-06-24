---
date: 2026-03-29
description: Aprende a crear PDF a partir de CAD, establecer el tamaño del lienzo
  y exportar CAD a PDF o TIFF usando Aspose.CAD para .NET en esta guía paso a paso.
linktitle: Setting Canvas Size and Mode
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 'Cómo crear PDF a partir de CAD: establecer el tamaño del lienzo y el modo
  en Aspose.CAD para .NET'
url: /es/net/cad-features-and-support/setting-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Configuración del tamaño del lienzo y modo en Aspose.CAD para .NET

## Introducción

¿Listo para **crear PDF a partir de CAD** mientras controla las dimensiones de salida? En este tutorial recorreremos la configuración del tamaño del lienzo y modo, la carga de un archivo CAD y su exportación a PDF o TIFF con Aspose.CAD para .NET. Ya sea que necesite **convertir DXF a PDF**, generar dibujos de alta resolución o simplemente ajustar el área de rasterización, los pasos a continuación le ofrecerán una solución sólida y lista para producción.

## Respuestas rápidas
- **¿Qué significa “create PDF from CAD”?** Convertir un dibujo CAD (p. ej., DXF, DWG) en un documento PDF que conserva los detalles vectoriales y raster.
- **¿Qué opción controla el tamaño de salida?** `CadRasterizationOptions.PageWidth` y `PageHeight` (tamaño del lienzo).
- **¿Puedo exportar también a TIFF?** Sí – use `TiffOptions` con la misma configuración de rasterización.
- **¿Necesito una licencia para producción?** Se requiere una licencia comercial; hay una prueba gratuita disponible.
- **¿Versiones de .NET compatibles?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## ¿Qué es “create PDF from CAD”?
Crear un PDF a partir de CAD significa renderizar el dibujo CAD en un formato orientado a página (PDF) que puede ser visualizado, impreso o compartido sin necesidad de software CAD. Aspose.CAD se encarga del trabajo pesado, permitiéndole definir el tamaño del lienzo, la escala y el formato de salida.

## ¿Por qué establecer el tamaño del lienzo al crear PDF a partir de CAD?
Establecer el tamaño del lienzo le brinda un control preciso sobre la resolución y dimensiones del PDF o TIFF resultante. Esto es especialmente útil cuando:
- Se preparan dibujos para imprimir en tamaños de papel específicos.  
- Se generan miniaturas o imágenes de alta resolución para vista previa web.  
- Se asegura una disposición consistente en varios documentos.

## Requisitos previos

- Biblioteca Aspose.CAD: Descargue e instale la biblioteca Aspose.CAD desde el [sitio web de Aspose.CAD](https://releases.aspose.com/cad/net/).
- Entorno de desarrollo: Asegúrese de tener un entorno de desarrollo .NET configurado en su máquina.
- Archivo CAD de ejemplo: Para este tutorial, utilizaremos un archivo DXF de ejemplo. Puede encontrar uno en la [documentación de Aspose.CAD](https://reference.aspose.com/cad/net/).

## Importar espacios de nombres

Primero, importe los espacios de nombres requeridos para el procesamiento CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Cómo crear PDF a partir de CAD con tamaño de lienzo personalizado

### Paso 1: Cargar archivo CAD

Comenzamos **cargando el archivo CAD** (p. ej., un DXF) en un objeto `Image`. Este es el punto donde **carga el archivo CAD** en memoria.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps will go here
}
```

### Paso 2: Crear CadRasterizationOptions

Cree una instancia de `CadRasterizationOptions` y defina el tamaño del lienzo. Las propiedades `PageWidth` y `PageHeight` le permiten **establecer el tamaño del lienzo** a las dimensiones exactas que necesita.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

### Paso 3: Crear PdfOptions (Exportar CAD a PDF)

Vincule la configuración de rasterización a un objeto `PdfOptions`. Esta configuración le permite **exportar CAD a PDF** con el lienzo personalizado que definió.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Paso 4: Exportar a PDF (Convertir DXF a PDF)

Ahora guarde la imagen como PDF. Este paso **crea PDF a partir de CAD** usando las opciones que configuramos.

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

### Paso 5: Crear TiffOptions (Exportar CAD a TIFF)

Si también necesita una imagen raster, configure `TiffOptions`. Se reutilizan las mismas opciones de rasterización, por lo que la **exportación de CAD a TIFF** respeta el tamaño del lienzo.

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Paso 6: Exportar a TIFF

Finalmente, guarde el dibujo como un archivo TIFF.

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Problemas comunes y soluciones

- **El lienzo aparece recortado** – Verifique que `AutomaticLayoutsScaling` esté configurado en `true` y `NoScaling` en `false` para que el dibujo se escale y ajuste al lienzo.  
- **PDF de baja resolución** – Aumente `PageWidth`/`PageHeight` o establezca `Resolution` en `CadRasterizationOptions`.  
- **Error de archivo no encontrado** – Asegúrese de que `MyDir` apunte a un directorio válido y que el nombre del archivo DXF coincida exactamente.

## Preguntas frecuentes

### P1: ¿Puedo usar Aspose.CAD con otras bibliotecas .NET?
R1: Sí, Aspose.CAD se integra sin problemas con otras bibliotecas .NET, proporcionando capacidades mejoradas para la manipulación de CAD.

### P2: ¿Hay una prueba gratuita disponible para Aspose.CAD?
R2: Sí, puede explorar las funciones de Aspose.CAD con una prueba gratuita. Visite [aquí](https://releases.aspose.com/) para comenzar.

### P3: ¿Cómo puedo obtener soporte para Aspose.CAD?
R3: Para soporte y discusiones, visite el [foro de Aspose.CAD](https://forum.aspose.com/c/cad/19).

### P4: ¿Dónde puedo encontrar documentación completa para Aspose.CAD?
R4: Consulte la [documentación de Aspose.CAD](https://reference.aspose.com/cad/net/) para información detallada y ejemplos.

### P5: ¿Cómo compro Aspose.CAD para .NET?
R5: Para comprar Aspose.CAD, visite la [página de compra](https://purchase.aspose.com/buy).

**P: ¿Puedo exportar un dibujo CAD de varias páginas a un solo PDF?**  
R: Sí. Establezca `PageCount` en `CadRasterizationOptions` y la biblioteca concatenará las páginas en un solo PDF.

**P: ¿Afecta el tamaño del lienzo a la calidad de los datos vectoriales?**  
R: Los datos vectoriales siguen siendo independientes de la resolución; el tamaño del lienzo solo influye en los elementos rasterizados y la resolución de la imagen.

---

**Última actualización:** 2026-03-29  
**Probado con:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}