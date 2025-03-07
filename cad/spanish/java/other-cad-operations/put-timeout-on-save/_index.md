---
title: Tiempo de espera al guardar para CAD con Aspose.CAD
linktitle: Poner tiempo de espera al guardar
second_title: API de Java Aspose.CAD
description: Aprenda cómo aumentar el rendimiento de su aplicación Java con Aspose.CAD. Establezca un tiempo de espera para guardar dibujos CAD. Sigue nuestra guía paso a paso.
weight: 15
url: /es/java/other-cad-operations/put-timeout-on-save/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tiempo de espera al guardar para CAD con Aspose.CAD

## Introducción

Bienvenido al tutorial sobre cómo poner un tiempo de espera al guardar usando Aspose.CAD para Java. En esta guía, lo guiaremos a través del proceso de establecer un tiempo de espera para guardar dibujos CAD para mejorar el rendimiento de su aplicación. Aspose.CAD para Java es una potente biblioteca que le permite trabajar con archivos CAD en sus aplicaciones Java sin problemas.

## Requisitos previos

Antes de sumergirse en el tutorial, asegúrese de cumplir con los siguientes requisitos previos:
-  Biblioteca Aspose.CAD para Java: asegúrese de tener la biblioteca Aspose.CAD para Java integrada en su proyecto. Puedes descargar la biblioteca desde[sitio web](https://releases.aspose.com/cad/java/).
- Entorno de desarrollo: configure su entorno de desarrollo Java con todas las herramientas y dependencias necesarias.

## Importar paquetes

Para comenzar, importe los paquetes necesarios a su proyecto Java. Agregue las siguientes líneas al comienzo de su archivo Java:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Ahora, analicemos el código de ejemplo en instrucciones paso a paso:

## Paso 1: configurar los directorios de origen y de salida

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Asegúrese de tener los directorios de origen y salida correctos para sus dibujos CAD.

## Paso 2: crear una fuente de token de interrupción

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Inicialice una fuente de token de interrupción para gestionar las interrupciones durante la operación de guardar.

## Paso 3: cargar el dibujo CAD

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

 Cargue el dibujo CAD en un`CadImage` objeto.

## Paso 4: configurar las opciones de rasterización

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Configure las opciones de rasterización para el dibujo CAD.

## Paso 5: configurar las opciones de PDF

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Configure opciones de PDF con opciones de rasterización vectorial y el token de interrupción.

## Paso 6: guardar el dibujo con tiempo de espera

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Guarde el dibujo CAD en un archivo PDF con el tiempo de espera especificado.

## Paso 7: Manejar la interrupción

```java
java.lang.Thread thread = new java.lang.Thread(new Runnable() {
    @Override
    public void run() {
        try {
            cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
        } catch (Throwable th) {
            System.out.println("interrupted !!!");
        }
    }
});
thread.start();
TimeUnit.SECONDS.sleep(3);
source.interrupt();
thread.join();
```

Cree un hilo para manejar la operación de guardar e interrumpirla después de un tiempo de espera específico.

## Conclusión

¡Felicidades! Ha aprendido con éxito cómo poner un tiempo de espera al guardar usando Aspose.CAD para Java. Esta característica puede mejorar enormemente la eficiencia de sus aplicaciones relacionadas con CAD.

## Preguntas frecuentes

### P1: ¿Cómo puedo descargar Aspose.CAD para Java?

 R1: Puedes descargarlo desde el[página de lanzamientos](https://releases.aspose.com/cad/java/).

### P2: ¿Dónde puedo encontrar la documentación de Aspose.CAD para Java?

 A2: Consulte el[documentación](https://reference.aspose.com/cad/java/) para obtener información completa.

### P3: ¿Hay una prueba gratuita disponible?

R3: Sí, puedes obtener una prueba gratuita desde[este enlace](https://releases.aspose.com/).

### P4: ¿Cómo obtengo una licencia temporal?

 A4: Visita[aquí](https://purchase.aspose.com/temporary-license/) para obtener detalles de la licencia temporal.

### P5: ¿Necesita ayuda o tiene preguntas?

 A5: Dirígete al[Foro Aspose.CAD](https://forum.aspose.com/c/cad/19) para el apoyo de la comunidad.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
