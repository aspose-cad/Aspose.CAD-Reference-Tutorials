---
date: 2025-12-22
description: 'Aprende a cargar archivos DWG y extraer información de subyacente con
  Aspose.CAD para Java: una guía paso a paso que cubre los indicadores de subyacente.'
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: Cargar archivo DWG y acceder a las banderas de subcapa – Aspose.CAD para Java
url: /es/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cargar archivo DWG y acceder a las banderas de subyacente – Aspose.CAD para Java

En los flujos de trabajo CAD modernos, **cargar un archivo DWG** rápidamente y extraer los detalles del subyacente es un requisito común. Ya sea que estés creando un visor, automatizando el procesamiento por lotes o extrayendo metadatos para la integración GIS, Aspose.CAD para Java te ofrece una forma limpia, basada en código, de hacerlo. En este tutorial recorreremos los pasos exactos para **cargar el archivo DWG**, iterar sus entidades y leer las banderas de subyacente que muchos desarrolladores pasan por alto.

## Respuestas rápidas
- **¿Cuál es la clase principal para abrir un DWG?** `com.aspose.cad.Image.load()` devuelve un `CadImage`.
- **¿Qué objeto contiene la información del subyacente?** `CadUnderlay` (o sus tipos derivados como `CadDgnUnderlay`).
- **¿Necesito una licencia para desarrollo?** Una prueba gratuita funciona para pruebas; se requiere una licencia comercial para producción.
- **¿Puedo procesar varios archivos DWG en un bucle?** Sí, solo repite el patrón de cargar‑y‑iterar.
- **¿Es este enfoque compatible con Java 11+?** Absolutamente, Aspose.CAD soporta Java 8 hasta las últimas versiones LTS.

## ¿Qué es “cargar archivo dwg” en Aspose.CAD?
`Image.load()` lee el contenido binario DWG y crea un objeto `CadImage` en memoria. Desde allí puedes explorar capas, bloques y entidades de subyacente sin tener que manejar tú mismo el formato del archivo DWG.

## ¿Por qué extraer las banderas de subyacente de un DWG?
Las banderas de subyacente indican cómo una referencia externa (como un subyacente DGN o PDF) está posicionada, escalada y rotada dentro del dibujo. Conocer estos valores te permite:
- Recrear el diseño visual exacto en un visor personalizado.
- Convertir los subyacentes a entidades CAD nativas para una edición posterior.
- Generar informes que incluyan metadatos de subyacente para cumplimiento o documentación.

## Requisitos previos
- **Biblioteca Aspose.CAD** – descargar desde la página de [releases](https://releases.aspose.com/cad/java/).
- **Java Development Kit** – JDK 8 o superior.
- **Una carpeta** que contenga los archivos DWG que deseas analizar. Reemplaza `"Your Document Directory"` en el código con tu ruta real.

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
Define dónde viven tus archivos DWG. Usar una carpeta dedicada mantiene el ejemplo limpio y portátil.

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
Solo los objetos `CadDgnUnderlay` contienen las banderas de subyacente que buscamos, por lo que los filtramos.

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

## Problemas comunes y consejos
- **Ruta de subyacente nula** – Asegúrate de que el DWG realmente haga referencia a un archivo externo; de lo contrario la ruta estará vacía.
- **Tipo de subyacente no soportado** – Actualmente Aspose.CAD soporta subyacentes DGN; los subyacentes PDF aún no están expuestos a través de la API.
- **Excepciones de licencia** – Ejecutar el código sin una licencia válida añadirá una marca de agua a cualquier imagen exportada.

## Preguntas frecuentes

**P: ¿Puedo usar Aspose.CAD para Java con otros formatos de archivo CAD?**  
R: Aspose.CAD se centra principalmente en el formato DWG, pero también soporta DXF, DWF y otros formatos CAD.

**P: ¿Hay una versión de prueba disponible para Aspose.CAD para Java?**  
R: Sí, puedes explorar las funciones con una prueba gratuita desde [aquí](https://releases.aspose.com/).

**P: ¿Cómo puedo obtener soporte o asistencia con Aspose.CAD para Java?**  
R: Visita el [foro de Aspose.CAD](https://forum.aspose.com/c/cad/19) para soporte comunitario y discusiones.

**P: ¿Hay licencias temporales disponibles para Aspose.CAD para Java?**  
R: Sí, puedes obtener una licencia temporal [aquí](https://purchase.aspose.com/temporary-license/).

**P: ¿Dónde puedo encontrar la documentación completa de Aspose.CAD para Java?**  
R: Consulta la [documentación](https://reference.aspose.com/cad/java/) para información detallada.

---

**Última actualización:** 2025-12-22  
**Probado con:** Aspose.CAD 24.12 para Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}