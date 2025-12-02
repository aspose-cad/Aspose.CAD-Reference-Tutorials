---
date: 2025-11-30
description: Aprenda como adicionar propriedades personalizadas a arquivos DWG em
  Java usando Aspose.CAD. Melhore a organização e a recuperação de informações em
  desenhos CAD sem esforço.
language: pt
linktitle: Add Custom Properties to DWG Files Using Java
second_title: Aspose.CAD Java API
title: Adicionar Propriedades Personalizadas a Arquivos DWG Usando Aspose.CAD para
  Java
url: /java/additional-features/add-custom-properties/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Adicionar Propriedades Personalizadas a Arquivos DWG Usando Aspose.CAD para Java

Manipular desenhos CAD programaticamente é uma necessidade diária para muitos desenvolvedores Java. Neste tutorial você descobrirá **como adicionar propriedades personalizadas a arquivos dwg** usando a poderosa biblioteca Aspose.CAD para Java. Ao final do guia você terá um trecho de código reutilizável que injeta metadados diretamente no cabeçalho de um arquivo DWG, facilitando a catalogação, busca e manutenção dos seus desenhos.

## Introdução

Aspose.CAD para Java é uma biblioteca totalmente gerenciada, livre de .NET, que permite ler, editar e gravar uma ampla variedade de formatos CAD sem a necessidade do AutoCAD. Adicionar propriedades personalizadas a um arquivo DWG oferece uma forma leve de armazenar informações adicionais — como códigos de projeto, notas de revisão ou detalhes do proprietário — diretamente dentro do próprio arquivo de desenho.

## Respostas Rápidas
- **O que significa “add custom properties dwg”?** Significa inserir pares nome/valor definidos pelo usuário nos metadados do cabeçalho de um arquivo DWG.  
- **Qual biblioteca lida com isso?** Aspose.CAD para Java fornece uma API simples para ler e gravar essas propriedades.  
- **Quanto tempo leva a implementação?** Tipicamente 5‑10 minutos para um exemplo básico.  
- **Preciso de licença?** Um teste gratuito funciona para desenvolvimento; uma licença comercial é necessária para produção.  
- **É compatível com outros formatos CAD?** Sim — DXF, DWF e outros são suportados.

## O que é Adicionar Propriedades Personalizadas a Arquivos DWG?

Propriedades personalizadas são pares chave‑valor armazenados no cabeçalho do DWG. Elas não são exibidas na geometria do desenho, mas podem ser acessadas por qualquer aplicação compatível com CAD, permitindo melhor gerenciamento de dados, relatórios automatizados e integração com sistemas PLM.

## Por Que Usar Aspose.CAD para Esta Tarefa?

- **Sem dependência do AutoCAD** – funciona em qualquer SO ou pipeline de CI.  
- **API completa** – ler, modificar e salvar sem perda de fidelidade.  
- **Alto desempenho** – processa desenhos grandes em segundos.  
- **Suporte a múltiplos formatos** – o mesmo código funciona para DXF, DWF e outros.

## Pré‑requisitos

Antes de começar, certifique-se de que você tem:

- **Java Development Kit (JDK) 8+** instalado e configurado em sua IDE.  
- Biblioteca **Aspose.CAD para Java** – baixe o JAR mais recente na [página de download do Aspose.CAD](https://releases.aspose.com/cad/java/).  
- Um **arquivo DWG/DXF de exemplo** para experimentar (o tutorial usa `conic_pyramid.dxf`).

## Importar Namespaces

Adicione as importações necessárias à sua classe Java para que você possa trabalhar com objetos Aspose.CAD.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;

import java.util.Map;
```

## Guia Passo a Passo

### Etapa 1: Configurar Seu Projeto

Crie um novo projeto Maven/Gradle (ou um projeto simples na IDE) e coloque o JAR do Aspose.CAD no classpath. Isso garante que os pacotes `com.aspose.cad.*` estejam disponíveis em tempo de compilação.

### Etapa 2: Definir Caminhos de Arquivo

Especifique onde o desenho fonte está localizado e onde o arquivo modificado deve ser gravado.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
String outFile = dataDir + "AddCustomProperties_out.dxf";
```

### Etapa 3: Carregar o Arquivo DWG

Use o método estático `Image.load` para ler o desenho em um objeto `CadImage`.

```java
CadImage cadImage = (CadImage)Image.load(srcFile);
```

### Etapa 4: Adicionar Propriedades Personalizadas

Insira seus metadados diretamente no cabeçalho do desenho. Cada chamada adiciona um novo par nome/valor.

```java
cadImage.getHeader().getCustomProperties().put("CUSTOM_PROPERTY_1", "Custom property test 1");
cadImage.getHeader().getCustomProperties().put("CUSTOM_PROPERTY_2", "Custom property test 2");
cadImage.getHeader().getCustomProperties().put("CUSTOM_PROPERTY_3", "Custom property test 3");
```

> **Dica:** Mantenha os nomes das propriedades concisos (máx 31 caracteres) e evite espaços para manter a compatibilidade com visualizadores CAD mais antigos.

### Etapa 5: Salvar o Arquivo DWG Modificado

Persista as alterações chamando `save`. O arquivo de saída agora contém as propriedades personalizadas que você adicionou.

```java
cadImage.save(outFile);
```

### Etapa 6: Executar o Código

Execute o programa a partir da sua IDE ou linha de comando. Se tudo estiver configurado corretamente, você verá uma mensagem de confirmação.

```java
System.out.println("\nAddCustomProperties executed successfully.");
```

## Problemas Comuns & Soluções

| Problema | Causa Provável | Solução |
|----------|----------------|---------|
| **`java.lang.NoClassDefFoundError: com/aspose/cad/Image`** | JAR do Aspose.CAD não está no classpath | Adicione o JAR à pasta `libs` do seu projeto ou declare‑o no Maven/Gradle. |
| **Propriedades não aparecem no arquivo salvo** | Usando uma versão de DWG que não suporta propriedades personalizadas | Certifique-se de que está trabalhando com versões DWG/DXF 2000 ou mais recentes; formatos mais antigos podem ignorar cabeçalhos personalizados. |
| **`OutOfMemoryError` on large files** | Carregando um desenho muito grande sem streaming | Use `Image.load` com um objeto `LoadOptions` que habilita carregamento eficiente em memória. |

## Perguntas Frequentes

**Q: Posso adicionar propriedades personalizadas a outros formatos de arquivo CAD?**  
A: Sim. Aspose.CAD para Java suporta DXF, DWF, DGN e mais, e a mesma API `getHeader().getCustomProperties()` funciona nesses formatos.

**Q: O Aspose.CAD para Java é compatível com todas as principais IDEs?**  
A: Absolutamente. Ele funciona com Eclipse, IntelliJ IDEA, NetBeans e até mesmo builds simples de linha de comando.

**Q: Onde posso encontrar mais exemplos e documentação detalhada?**  
A: Visite a [Referência da API Aspose.CAD Java](https://reference.aspose.com/cad/java/) oficial para obter uma lista completa de classes, métodos e projetos de exemplo.

**Q: Posso testar o Aspose.CAD para Java antes de comprar?**  
A: Sim — baixe uma avaliação gratuita de 30 dias na [página de download do Aspose.CAD](https://releases.aspose.com/).

**Q: Como obtenho suporte se encontrar dificuldades?**  
A: O fórum da comunidade Aspose e o portal de suporte dedicado [Aspose.CAD](https://forum.aspose.com/c/cad/19) são ótimos locais para fazer perguntas e compartilhar soluções.

---

**Última atualização:** 2025-11-30  
**Testado com:** Aspose.CAD para Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}