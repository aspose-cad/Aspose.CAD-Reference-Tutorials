---
date: 2026-01-22
description: Aprenda cómo establecer un tiempo de espera al guardar CAD en PDF usando
  Aspose.CAD para Java. Mejore el rendimiento con esta guía paso a paso.
linktitle: Put Timeout on Save
second_title: Aspose.CAD Java API
title: Cómo establecer un tiempo de espera al guardar CAD con Aspose.CAD
url: /es/java/other-cad-operations/put-timeout-on-save/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Timeout on Save for CAD with Aspose.CAD

## Introducción

Bienvenido al tutorial sobre **cómo establecer un tiempo de espera** al guardar dibujos CAD usando Aspose.CAD para Java. En esta guía, le mostraremos paso a paso cómo configurar un tiempo de espera para la operación de guardado, lo que ayuda a que su aplicación permanezca receptiva y mejora el rendimiento general. Aspose.CAD para Java es una biblioteca potente que le permite trabajar con archivos CAD sin problemas.

## Respuestas rápidas
- **¿Qué hace el tiempo de espera?** Aborta la operación de guardado si supera la duración especificada, evitando bloqueos prolongados.  
- **¿Qué formato se usa en el ejemplo?** El dibujo CAD se guarda como un archivo PDF.  
- **¿Necesito una licencia?** Se requiere una licencia temporal o permanente de Aspose.CAD para uso en producción.  
- **¿Qué versión de Java es compatible?** El código funciona con Java 8 y versiones posteriores.  
- **¿Puedo ajustar la duración del tiempo de espera?** Sí, simplemente cambie el valor de `TimeUnit.SECONDS.sleep(...)`.

## Cómo establecer un tiempo de espera al guardar

### ¿Qué es un tiempo de espera en el contexto de Aspose.CAD?
Un tiempo de espera es una medida de seguridad que detiene un proceso de rasterización o conversión prolongado. Al proporcionar un `InterruptionTokenSource`, puede indicar a la biblioteca que aborte la operación después de un período definido, asegurando que su aplicación siga siendo receptiva.

### ¿Por qué establecer un tiempo de espera al guardar CAD a PDF?
Guardar dibujos CAD grandes o complejos puede consumir una cantidad significativa de CPU y memoria. Añadir un tiempo de espera:
- Evita que la aplicación se congele.  
- Le permite manejar tareas de larga duración de forma elegante.  
- Mejora la experiencia del usuario, especialmente en entornos web o con interfaces gráficas.

## Requisitos previos

- **Aspose.CAD for Java Library** – Asegúrese de que la biblioteca esté integrada en su proyecto. Puede descargarla desde el [sitio web](https://releases.aspose.com/cad/java/).  
- **Entorno de desarrollo** – Un IDE de Java (IntelliJ, Eclipse, etc.) con JDK 8+ instalado.

## Importar paquetes

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Ahora, desglosaremos el código de ejemplo en instrucciones paso a paso:

## Paso 1: Establecer directorios de origen y salida

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Asegúrese de que los directorios de origen y salida sean correctos para sus dibujos CAD.

## Paso 2: Crear fuente de token de interrupción

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Inicialice una fuente de token de interrupción para gestionar interrupciones durante la operación de guardado.

## Paso 3: Cargar dibujo CAD

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

Cargue el dibujo CAD en un objeto `CadImage`.

## Paso 4: Configurar opciones de rasterización

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Configure las opciones de rasterización para el dibujo CAD.

## Paso 5: Configurar opciones de PDF

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Configure las opciones de PDF con las opciones de rasterización vectorial y el token de interrupción.

## Paso 6: Guardar dibujo con tiempo de espera

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Guarde el dibujo CAD en un archivo PDF con el tiempo de espera especificado.

## Paso 7: Manejar interrupción

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

Cree un hilo para manejar la operación de guardado e interrumpirla después de un tiempo de espera especificado.

## Errores comunes y solución de problemas

- **Tiempo de espera demasiado corto** – Si el dibujo es grande, un tiempo de espera muy corto puede abortar la operación antes de que termine. Aumente la duración del `sleep` o ajuste la configuración de rasterización.  
- **Licencia ausente** – Ejecutar sin una licencia válida lanzará una excepción. Aplique una licencia temporal o permanente antes de ejecutar el código.  
- **Rutas incorrectas** – Asegúrese de que `SourceDir` y `OutputDir` apunten a carpetas existentes; de lo contrario, `Image.load` o `save` fallarán.

## Preguntas frecuentes

**P: ¿Cómo puedo descargar Aspose.CAD para Java?**  
R: Puede descargarlo desde la [página de lanzamientos](https://releases.aspose.com/cad/java/).

**P: ¿Dónde encuentro la documentación de Aspose.CAD para Java?**  
R: Consulte la [documentación](https://reference.aspose.com/cad/java/) para obtener información completa.

**P: ¿Hay una prueba gratuita disponible?**  
R: Sí, puede obtener una prueba gratuita en [este enlace](https://releases.aspose.com/).

**P: ¿Cómo obtengo una licencia temporal?**  
R: Visite [aquí](https://purchase.aspose.com/temporary-license/) para obtener detalles sobre licencias temporales.

**P: ¿Necesita ayuda o tiene preguntas?**  
R: Diríjase al [foro de Aspose.CAD](https://forum.aspose.com/c/cad/19) para soporte de la comunidad.

## Conclusión

¡Felicidades! Ahora sabe **cómo establecer un tiempo de espera** en las operaciones de guardado al convertir dibujos CAD a PDF usando Aspose.CAD para Java. Implementar este tiempo de espera mejora la fiabilidad y la capacidad de respuesta de sus aplicaciones relacionadas con CAD.

---

**Última actualización:** 2026-01-22  
**Probado con:** Aspose.CAD for Java 24.11 (latest)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}