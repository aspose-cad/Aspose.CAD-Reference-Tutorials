---
date: 2026-02-23
description: 'Aprende a cargar archivos DWG usando Aspose.CAD.DWG para Java y a extraer
  las banderas de subyacente: una guía paso a paso para desarrolladores.'
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: aspose cad dwg – Cargar DWG y acceder a las banderas de subyacente (Java)
url: /es/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cargar archivo DWG y acceder a los indicadores de subyacente – Aspose.CAD para Java

En los flujos de trabajo CAD modernos, **con aspose cad dwg puedes cargar rápidamente un archivo DWG** y extraer los detalles de subyacente que a menudo están ocultos para los usuarios casuales. Ya sea que estés construyendo un visor DWG en Java, automatizando una canalización de procesamiento por lotes dwg, o extrayendo metadatos para integración GIS, Aspose.CAD para Java te brinda una forma limpia, basada en código, de hacerlo. En este tutorial recorreremos los pasos exactos para **cargar un archivo DWG**, iterar sus entidades y leer los indicadores de subyacente que muchos desarrolladores pasan por alto.

## Respuestas rápidas
- **¿Cuál es la clase principal para abrir un DWG?** `com.aspose.cad.Image.load()` devuelve un `CadImage`.
- **¿Qué objeto contiene la información del subyacente?** `CadUnderlay` (o sus tipos derivados como `CadDgnUnderlay`).
- **¿Necesito una licencia para desarrollo?** Una prueba gratuita funciona para pruebas; se requiere una licencia comercial para producción.
- **¿Puedo procesar varios archivos DWG en un bucle?** Sí, solo repite el patrón de cargar‑e‑iterar.
- **¿Este enfoque es compatible con Java 11+?** Absolutamente, Aspose.CAD soporta Java 8 hasta las últimas versiones LTS.

## aspose cad dwg – Cargando un archivo DWG (Java)

`Image.load()` lee el contenido binario DWG y crea un objeto `CadImage` en memoria. Desde allí puedes explorar capas, bloques y entidades de subyacente sin tener que manejar el formato de archivo DWG tú mismo.

## ¿Por qué extraer los indicadores de subyacente de un DWG?

Los indicadores de subyacente te indican cómo se posiciona, escala y rota una referencia externa (como un subyacente DGN o PDF) dentro del dibujo. Conocer estos valores te permite:

- Recrear el diseño visual exacto en un **visor java dwg** personalizado.
- Convertir subyacentes a entidades CAD nativas para una edición posterior.
- Generar informes que incluyan metadatos de subyacente para cumplimiento o documentación.
- **Procesar dwg por lotes** y almacenar sus metadatos de subyacente en una base de datos para análisis posterior.

## Requisitos previos
- **Aspose.CAD Library** – descarga desde la página de [releases](https://releases.aspose.com/cad/java/) .  
- **Java Development Kit** – JDK 8 o superior.  
- **Una carpeta** que contenga los archivos DWG que deseas analizar. Reemplaza `"Your Document Directory"` en el código con la ruta real.

## Importar espacios de nombres

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.CadUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.UnderlayFlags;
```

## Guía paso a paso

### Paso 1: Establecer el directorio de recursos
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```
Define dónde se encuentran tus archivos DWG. Usar una carpeta dedicada mantiene el ejemplo limpio y portátil.

### Paso 2: Cargar el archivo DWG
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
Aquí **cargamos el archivo dwg** `BlockRefDgn.dwg` en una instancia `CadImage`, lista para inspección.

### Paso 3: Iterar a través de las entidades DWG
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
El bucle recorre cada entidad—líneas, círculos, bloques y subyacentes—para que podamos seleccionar las que necesitamos.

### Paso 4: Identificar entidades CadDgnUnderlay
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
Solo los objetos `CadDgnUnderlay` contienen los indicadores de subyacente que buscamos, por lo que los filtramos.

### Paso 5: Acceder a la información del subyacente
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
Una vez que tenemos un `CadUnderlay`, podemos leer su ruta, nombre, punto de inserción, rotación, factores de escala y el enumerado `UnderlayFlags` que indica visibilidad, recorte y otras opciones de renderizado.

## Cómo cargar archivos dwg en un proceso por lotes

Si necesitas **procesar dwg por lotes**, envuelve los pasos anteriores en un simple bucle `for` que itere sobre todos los archivos en `dataDir`. La misma llamada `Image.load()` funciona para cada archivo, y puedes almacenar los indicadores extraídos en un CSV o en una base de datos para informes posteriores.

## Problemas comunes y consejos
- **Ruta de subyacente nula** – Asegúrate de que el DWG realmente haga referencia a un archivo externo; de lo contrario la ruta estará vacía.
- **Tipo de subyacente no soportado** – Aspose.CAD actualmente soporta subyacentes DGN; los subyacentes PDF aún no están expuestos vía la API.
- **Excepciones de licencia** – Ejecutar el código sin una licencia válida añadirá una marca de agua a cualquier imagen exportada.
- **Consejo de rendimiento:** Reutiliza una única instancia `Image` al procesar muchos archivos en un lote para reducir la presión del GC.

## Preguntas frecuentes

**P: ¿Puedo usar Aspose.CAD para Java con otros formatos de archivo CAD?**  
R: Aspose.CAD se centra principalmente en el formato DWG, pero también soporta DXF, DWF y otros formatos CAD.

**P: ¿Existe una versión de prueba disponible para Aspose.CAD para Java?**  
R: Sí, puedes explorar las funciones con una prueba gratuita desde [here](https://releases.aspose.com/).

**P: ¿Cómo puedo obtener soporte o asistencia con Aspose.CAD para Java?**  
R: Visita el [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) para soporte comunitario y discusiones.

**P: ¿Hay licencias temporales disponibles para Aspose.CAD para Java?**  
R: Sí, puedes obtener una licencia temporal [here](https://purchase.aspose.com/temporary-license/).

**P: ¿Dónde puedo encontrar la documentación completa para Aspose.CAD para Java?**  
R: Consulta la [documentation](https://reference.aspose.com/cad/java/) para información detallada.

---

**Última actualización:** 2026-02-23  
**Probado con:** Aspose.CAD 24.12 para Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}