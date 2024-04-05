---
title: Ponto de vista gratuito em desenhos CAD - Guia Aspose.CAD
linktitle: Ponto de vista gratuito em desenhos CAD
second_title: Aspose.CAD .NET - Formato de arquivo CAD e BIM
description: Explore a liberdade da visualização CAD com Aspose.CAD for .NET. Siga nosso guia passo a passo para obter um ponto de vista único.
type: docs
weight: 11
url: /pt/net/advanced-cad-techniques/free-point-of-view-in-cad-drawings/
---
No domínio do Design Assistido por Computador (CAD), obter um ponto de vista livre nos desenhos é um aspecto crucial da visualização e apresentação de projetos complexos. Aspose.CAD for .NET fornece uma solução robusta para alcançar essa liberdade, permitindo aos usuários manipular e otimizar desenhos CAD com facilidade. Neste guia passo a passo, exploraremos o processo de obtenção de um ponto de vista livre em desenhos CAD usando Aspose.CAD for .NET.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:

1. Instalação do Aspose.CAD
 Certifique-se de ter o Aspose.CAD for .NET instalado em seu ambiente de desenvolvimento. Caso contrário, você pode baixá-lo no[Site Aspose.CAD](https://releases.aspose.com/cad/net/).

2. Arquivo de desenho CAD
Prepare um arquivo de desenho CAD que deseja manipular. Para este guia, usaremos um arquivo de amostra chamado “conic_pyramid.dxf”.

3. Ambiente de desenvolvimento
Tenha um ambiente de desenvolvimento .NET funcional configurado com o Visual Studio ou qualquer IDE de sua preferência.

## Importar namespaces

Em seu projeto .NET, importe os namespaces necessários para a funcionalidade Aspose.CAD. Adicione o seguinte trecho de código ao topo do seu arquivo:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```


## Etapa 1: definir o diretório de documentos

```csharp
// O caminho para o diretório de documentos.
string MyDir = "Your Document Directory";
```

Certifique-se de substituir "Seu diretório de documentos" pelo caminho real para o diretório de documentos.

## Etapa 2: especificar o arquivo de origem

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
```

Forneça o caminho para o seu arquivo de desenho CAD.

## Etapa 3: definir caminho de saída

```csharp
var outPath = Path.Combine(MyDir, "FreePointOfView_out.jpg");
```

Defina o caminho onde o desenho CAD manipulado será salvo.

## Etapa 4: carregar imagem CAD

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
```

Carregue o desenho CAD usando Aspose.CAD.

## Etapa 5: configurar opções JPEG

```csharp
JpegOptions options = new JpegOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500, PageHeight = 1500
    }
};
```

Configure as opções de exportação do desenho CAD para o formato JPEG.

## Etapa 6: definir ângulos de rotação

```csharp
float xAngle = 10; //Ângulo de rotação ao longo do eixo X
float yAngle = 30; //Ângulo de rotação ao longo do eixo Y
float zAngle = 40; //Ângulo de rotação ao longo do eixo Z
((CadRasterizationOptions)(options.VectorRasterizationOptions)).ObserverPoint = new ObserverPoint(xAngle, yAngle, zAngle);
```

Especifique os ângulos de rotação ao longo dos eixos X, Y e Z para obter o ponto de vista desejado.

## Etapa 7: Salve o desenho CAD manipulado

```csharp
cadImage.Save(outPath, options);
}
```

Salve o desenho CAD manipulado no caminho de saída especificado.

## Etapa 8: exibir mensagem de sucesso

```csharp
Console.WriteLine("\n3D images exported successfully to JPEG.\nFile saved at " + outPath);
```

Informe o usuário sobre a exportação bem-sucedida da imagem 3D.

## Conclusão

Neste tutorial, exploramos o processo de obtenção de um ponto de vista livre em desenhos CAD usando Aspose.CAD for .NET. Seguindo estas instruções passo a passo, você pode aprimorar seus recursos de visualização CAD e apresentar seus projetos com uma nova perspectiva.


## Perguntas frequentes

### Q1: Posso usar o Aspose.CAD for .NET com outros formatos de arquivo CAD?

A1: Sim, Aspose.CAD for .NET suporta vários formatos de arquivo CAD, incluindo DWG e DXF.

### Q2: Existe uma versão de teste do Aspose.CAD disponível?

 A2: Sim, você pode baixar uma versão de avaliação gratuita em[aqui](https://releases.aspose.com/).

### Q3: Como posso obter uma licença temporária para Aspose.CAD?

 A3: Você pode adquirir uma licença temporária de[aqui](https://purchase.aspose.com/temporary-license/).

### Q4: Onde posso encontrar suporte adicional para Aspose.CAD?

 A4: Visite o[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) para apoio e discussões da comunidade.

### P5: Posso personalizar as opções de exportação para diferentes formatos de imagem?

A5: Certamente! Aspose.CAD oferece uma gama de opções de personalização, permitindo adaptar o processo de exportação às suas necessidades específicas.