---
date: 2026-03-02
description: Откройте потенциал Aspose.CAD для Java. Легко экспортируйте OLE‑объекты
  и **сохраняйте CAD в PNG**. Скачайте сейчас для беспроблемного управления CAD‑данными.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: Сохранить CAD в PNG – экспортировать OLE‑объекты с помощью Aspose.CAD для Java
url: /ru/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Save CAD as PNG – Export OLE Objects Using Aspose.CAD for Java

## Введение

В динамичном мире систем автоматизированного проектирования (CAD) эффективное управление и извлечение OLE (Object Linking and Embedding) объектов, а также возможность **save CAD as PNG**, имеют решающее значение для последующих процессов, таких как отчётность, веб‑просмотр или архивирование. Aspose.CAD for Java предоставляет мощное решение, ориентированное на код, которое позволяет как экспортировать OLE‑объекты, так и конвертировать CAD‑чертежи в высококачественные PNG‑изображения всего в несколько строк кода.

## Быстрые ответы
- **Что делает Aspose.CAD?** Он читает, изменяет и конвертирует CAD‑файлы (DWG, DXF, DGN и т.д.) без необходимости в нативном CAD‑ПО.  
- **Могу ли я сохранить CAD как PNG?** Да — используйте `PngOptions` вместе с `CadRasterizationOptions` для растеризации любого макета.  
- **Как экспортировать OLE‑объекты?** Загрузите CAD‑файл с помощью `Image.load` и сохраните каждый макет, содержащий OLE, как PNG.  
- **Нужна ли лицензия?** Доступна бесплатная пробная версия; коммерческая лицензия снимает ограничения оценки.  
- **Какая версия Java требуется?** Полностью поддерживается Java 8 и выше.

## Что такое **save CAD as PNG**?
Сохранить CAD как PNG означает растеризовать векторные CAD‑чертежи в пиксельное PNG‑изображение. Такая конверсия полезна, когда нужен лёгкий, универсально просматриваемый формат для веб‑страниц, мобильных приложений или документации.

## Почему использовать Aspose.CAD for Java для **convert CAD to PNG**?
- **Не требуется установка CAD** – библиотека полностью работает в Java.  
- **Сохраняет точность макета** – вы можете выбирать конкретные макеты, контролировать DPI и сохранять качество линий.  
- **Пакетная обработка** – перебирайте несколько файлов с помощью простого цикла.  
- **Экспорт OLE‑объектов** – OLE‑контент, встроенный в файлы DWG/DXF, автоматически рендерится в PNG‑вывод.

## Предварительные требования

Перед тем как приступить к руководству, убедитесь, что у вас есть следующие требования:

- **Среда Java** – Убедитесь, что на вашей машине настроена среда разработки Java.  
- **Aspose.CAD for Java** – Скачайте и установите библиотеку Aspose.CAD for Java. Вы можете найти библиотеку по [download link](https://releases.aspose.com/cad/java/).  
- **CAD‑файлы** – Подготовьте CAD‑файлы, содержащие OLE‑объекты, которые вы хотите экспортировать.

## Импорт пространств имён

Для начала импортируйте необходимые пространства имён в ваш Java‑проект. Эти пространства имён предоставляют основные классы и функции, необходимые для работы с CAD‑файлами с помощью Aspose.CAD.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Теперь разберём процесс экспорта OLE‑объектов из CAD на несколько шагов:

## Как **save CAD as PNG** и экспортировать OLE‑объекты

### Шаг 1: Установите каталог документов

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

Убедитесь, что заменили `"Your Document Directory"` на путь к каталогу, содержащему ваши CAD‑файлы.

### Шаг 2: Определите имена CAD‑файлов

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

Укажите имена CAD‑файлов, которые вы хотите обработать, в массиве `files`.

### Шаг 3: Установите параметры экспорта PNG

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

Настройте параметры экспорта PNG, включая растеризацию векторов и параметры макета. Эти параметры позволяют вам **convert CAD to PNG** с желаемым качеством.

### Шаг 4: Переберите CAD‑файлы

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

Переберите каждый указанный CAD‑файл, загрузите его с помощью Aspose.CAD и сохраните OLE‑объекты как PNG‑изображения. Этот цикл демонстрирует простой способ **convert DWG to PNG** пакетно.

## Распространённые проблемы и решения

| Проблема | Причина | Решение |
|----------|---------|----------|
| **Пустой PNG‑файл** | Несоответствие имени макета | Убедитесь, что имя макета (`"Layout1"`) существует в исходном DWG. |
| **Отсутствует графика OLE** | OLE‑объекты находятся в другом макете | Включите все необходимые макеты в `rasterizationOptions.setLayouts(...)`. |
| **Ошибка нехватки памяти при больших файлах** | Высокие настройки DPI | Уменьшите DPI с помощью `rasterizationOptions.setResolution(...)` или обрабатывайте файлы по одному. |

## Часто задаваемые вопросы

**Q: Совместим ли Aspose.CAD со всеми форматами CAD‑файлов?**  
A: Aspose.CAD поддерживает различные форматы CAD, включая DWG, DXF и DGN. См. полный список в [documentation](https://reference.aspose.com/cad/java/).

**Q: Можно ли настроить параметры экспорта для OLE‑объектов?**  
A: Да, Aspose.CAD предоставляет обширные возможности настройки параметров экспорта, позволяя адаптировать вывод под ваши конкретные требования.

**Q: Доступна ли бесплатная пробная версия Aspose.CAD?**  
A: Да, вы можете изучить возможности Aspose.CAD, получив бесплатную пробную версию по ссылке [here](https://releases.aspose.com/).

**Q: Где можно получить поддержку сообщества для Aspose.CAD?**  
A: Присоединяйтесь к сообществу Aspose.CAD на [forum](https://forum.aspose.com/c/cad/19), чтобы задать вопросы и поделиться опытом.

**Q: Как приобрести лицензию на Aspose.CAD?**  
A: Посетите страницу [purchase page](https://purchase.aspose.com/buy), чтобы приобрести лицензию, соответствующую вашим потребностям разработки.

## Заключение

С помощью этих простых, но мощных шагов вы сможете без проблем **save CAD as PNG**, одновременно экспортируя OLE‑объекты из CAD‑файлов с помощью Aspose.CAD for Java. Этот универсальный инструмент позволяет разработчикам эффективно управлять CAD‑данными, открывая новые возможности в разработке CAD‑приложений и последующих рабочих процессах, основанных на изображениях.

---

**Последнее обновление:** 2026-03-02  
**Тестировано с:** Aspose.CAD for Java 24.12  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}