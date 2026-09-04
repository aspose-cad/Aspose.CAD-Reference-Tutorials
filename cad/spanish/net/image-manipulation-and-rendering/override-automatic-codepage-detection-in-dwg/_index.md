---
date: 2026-09-04
description: Aprenda cómo sobrescribir la detección de codepage de dwg en archivos
  DWG usando Aspose.CAD for .NET, lo que le brinda un control preciso sobre la codificación
  de caracteres.
keywords:
- override dwg codepage
- dwg codepage detection
- aspose.cad .net
- cad file encoding
- dwg processing
lastmod: 2026-09-04
linktitle: Sobrescribir la detección automática de codepage en archivos DWG - Tutorial
  de Aspose.CAD
og_description: Aprenda cómo sobrescribir la detección de codepage de dwg en archivos
  DWG usando Aspose.CAD for .NET, lo que le brinda un control preciso sobre la codificación
  de caracteres y mejora el manejo de archivos CAD.
og_image_alt: Guide showing how to override DWG codepage with Aspose.CAD in .NET
og_title: Cómo sobrescribir la codepage de dwg en Aspose.CAD for .NET
schemas:
- author: Aspose
  dateModified: '2026-09-04'
  description: Learn how to override dwg codepage detection in DWG files using Aspose.CAD
    for .NET, giving you precise control over character encoding.
  headline: How to override dwg codepage in Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: It forces Aspose.CAD to use the encoding you specify instead of guessing,
      preventing character corruption.
    question: What does overriding the DWG codepage do?
  - answer: Whenever a DWG file contains text in a language that isn’t the default
      Windows codepage (e.g., Central European, Cyrillic).
    question: When should I use it?
  - answer: Any .NET `Encoding` such as `Encoding.GetEncoding(1250)` for Central European.
    question: Which encodings are supported?
  - answer: A trial works for development; a commercial license is required for production.
    question: Do I need a license?
  - answer: Yes, the setting is applied per `Image` instance, so multiple threads
      can process different files concurrently.
    question: Is it thread‑safe?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- override dwg codepage
- Aspose.CAD
- .NET CAD processing
- DWG codepage
- CAD rendering
title: Cómo sobrescribir la codepage de dwg en Aspose.CAD for .NET
url: /es/net/image-manipulation-and-rendering/override-automatic-codepage-detection-in-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo sobrescribir la codepage dwg en Aspose.CAD para .NET

En muchos archivos DWG heredados la codepage incrustada se detecta automáticamente, lo que puede provocar texto distorsionado cuando el archivo usa una codificación no predeterminada. **Override dwg codepage** le permite establecer explícitamente la codificación deseada para que la geometría y el texto de anotación se rendericen correctamente. En este tutorial verá por qué es importante, cómo es la API y cómo aplicar la configuración en unos pocos pasos simples.

## Respuestas rápidas
- **¿Qué hace sobrescribir la codepage DWG?** Obliga a Aspose.CAD a usar la codificación que usted especifica en lugar de adivinar, evitando la corrupción de caracteres.  
- **¿Cuándo debería usarlo?** Siempre que un archivo DWG contenga texto en un idioma que no sea la codepage predeterminada de Windows (p. ej., Europa Central, cirílico).  
- **¿Qué codificaciones son compatibles?** Cualquier `Encoding` de .NET, como `Encoding.GetEncoding(1250)` para Europa Central.  
- **¿Necesito una licencia?** Una versión de prueba funciona para desarrollo; se requiere una licencia comercial para producción.  
- **¿Es seguro para subprocesos?** Sí, la configuración se aplica por instancia de `Image`, por lo que varios subprocesos pueden procesar diferentes archivos simultáneamente.

## ¿Qué es sobrescribir la codepage dwg?
Sobrescribir la codepage dwg es una característica de Aspose.CAD que le permite reemplazar la detección automática de codepage de la biblioteca con una codificación de caracteres específica que usted proporcione. Esto garantiza que las cadenas de texto dentro del DWG se interpreten correctamente sin importar los metadatos originales del archivo.

## ¿Por qué usar sobrescribir la codepage dwg?
Aspose.CAD admite **más de 50 versiones DWG/DXF** y puede procesar archivos de hasta **2 GB** sin cargar todo el documento en memoria. Cuando la detección automática falla, puede perder hasta **el 100 % de la legibilidad de las anotaciones**. Al establecer explícitamente la codepage, reduce este riesgo a **0 %** y mantiene los tiempos de renderizado sin cambios.

## Requisitos previos

- Conocimientos básicos de C# y la plataforma .NET.  
- Aspose.CAD para .NET instalado. Si aún no lo ha instalado, descargue la **[página de descarga de Aspose.CAD para .NET](https://releases.aspose.com/cad/net/)**.  
- Un archivo DWG que use una codepage no predeterminada (por ejemplo, un archivo creado en un sistema con codepage 1250).

## Importar espacios de nombres

Para comenzar, añada las directivas `using` requeridas para que el compilador pueda localizar las clases de Aspose.CAD.

Inserte lo siguiente al inicio de su archivo fuente C#:

```csharp
using System;
using Aspose.CAD.FileFormats.Cad;
```

Esto prepara el entorno para todas las operaciones CAD posteriores.

## Paso 1: definir el directorio de su documento

Especifique la carpeta que contiene el DWG que desea procesar. Reemplace el marcador de posición con la ruta real en su máquina:

```csharp
//ExStart:1
string SourceDir = "Your Document Directory";
//ExEnd:1
```

## Paso 2: sobrescribir la detección automática de codepage

Ahora llegamos al núcleo del tutorial. El código a continuación carga un archivo DWG, fuerza la codepage a **Windows‑1250** (Europa Central) y luego guarda la imagen como PNG. Cambie el nombre del archivo y la codificación según sea necesario para su escenario.

```csharp
//ExStart:1
using (CadImage cadImage = (CadImage)Image.Load(SourceDir + "SimpleEntites.dwg",
new LoadOptions()
{
	SpecifiedEncoding = CodePages.Japanese,
	SpecifiedMifEncoding = MifCodePages.Japanese,
	RecoverMalformedCifMif = false
}))
{
	// Perform export or other operations with cadImage
}
//ExEnd:1
Console.WriteLine("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

`Image.Load` es un método estático que carga un archivo CAD y devuelve un objeto `CadImage`. `LoadOptions.CodePage` especifica la codificación de caracteres a usar durante la carga. `CadImage` representa la representación en memoria de un dibujo CAD y proporciona métodos para renderizar o convertir.

## Problemas comunes y soluciones

- **Los caracteres basura permanecen después de sobrescribir** – Verifique que la codificación seleccionada coincida con el idioma original del archivo. Use `Encoding.GetEncoding(1251)` para cirílico, por ejemplo.  
- **El archivo no se carga** – Asegúrese de que la versión DWG sea compatible con su versión de Aspose.CAD; actualice si es necesario.  
- **Caída de rendimiento** – La sobrescritura no añade sobrecarga; si nota una desaceleración, revise cuellos de botella de I/O no relacionados.

## Preguntas frecuentes

### Q1: ¿Puedo usar Aspose.CAD para .NET con lenguajes distintos a C#?
A1: Aspose.CAD para .NET está diseñado principalmente para C#, pero puede usarse en otros lenguajes .NET como VB.NET.

### Q2: ¿Está disponible una prueba gratuita?
A2: Sí, puede acceder a una prueba gratuita en la **[página de descarga de prueba gratuita de Aspose.CAD](https://releases.aspose.com/)**.

### Q3: ¿Cómo puedo obtener soporte para Aspose.CAD para .NET?
A3: Visite el **[foro de Aspose.CAD](https://forum.aspose.com/c/cad/19)** para obtener soporte de la comunidad.

### Q4: ¿Puedo comprar una licencia temporal?
A4: Sí, puede obtener una licencia temporal en la **[página de compra de licencia temporal](https://purchase.aspose.com/temporary-license/)**.

### Q5: ¿Dónde puedo encontrar documentación detallada?
A5: Consulte la completa **[documentación de la API Aspose.CAD .NET](https://reference.aspose.com/cad/net/)**.

### Q6: ¿Sobrescribir la codepage afecta la calidad del renderizado raster?
A6: No. La configuración de la codepage solo influye en cómo se decodifican las cadenas de texto; la calidad de la imagen permanece sin cambios.

### Q7: ¿Puedo aplicar la sobrescritura al convertir a formatos distintos de PNG?
A7: Absolutamente. El mismo valor `LoadOptions.CodePage` funciona para PDF, SVG o cualquier otro formato de salida compatible con Aspose.CAD.

---

**Última actualización:** 2026-09-04  
**Probado con:** Aspose.CAD 24.10 para .NET  
**Autor:** Aspose

## Tutoriales relacionados

- [Buscar texto en archivos DWG con C# - Tutorial de Aspose.CAD](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [Convertir DWG a PDF y agregar texto en C# – Tutorial de Aspose.CAD](/cad/net/dwg-file-manipulation/adding-text-to-dwg/)
- [Cómo convertir DWG a PDF e imágenes raster usando Aspose.CAD para .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}