---
date: 2026-05-25
description: Apprenez comment configurer la licence à compteurs dans Aspose.CAD pour
  Java afin d'optimiser le traitement CAD, de réduire les coûts et de suivre l'utilisation
  efficacement.
keywords:
- how to set metered
- Aspose.CAD licensing
- Java metered licensing
linktitle: Comment configurer la licence à compteurs dans Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-05-25'
  description: Learn how to set metered licensing in Aspose.CAD for Java to optimize
    CAD processing, reduce costs, and track usage efficiently.
  headline: How to Set Metered Licensing in Aspose.CAD
  type: TechArticle
- questions:
  - answer: A usage‑based model that tracks API calls and charges per consumption
      unit.
    question: What is metered licensing?
  - answer: Two keys – a public and a private key – generated from your Aspose account.
    question: How many keys are required?
  - answer: Yes, call `License.getConsumptionQuantity()` before and after processing.
    question: Can I check usage programmatically?
  - answer: A free trial license can be obtained from the Aspose website.
    question: Is a trial available?
  - answer: Java 8 through 17 are fully supported.
    question: Which Java version is supported?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Comment configurer la licence à compteurs dans Aspose.CAD
url: /fr/java/licensing-and-configuration/metered-licensing-in-aspose-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Licence à la consommation dans Aspose.CAD

## Introduction

Débloquez tout le potentiel d'Aspose.CAD pour Java avec la licence **comment définir la licence à la consommation** ! Ce guide étape par étape vous accompagne à chaque étape — de l'installation des prérequis, l'importation des bons packages, à la mesure de la consommation avant et après le traitement. À la fin, vous saurez exactement **comment définir la licence à la consommation**, lire les métriques d'utilisation et garder votre flux de travail CAD rentable.

## Réponses rapides
- **Qu'est-ce que la licence à la consommation ?** Un modèle basé sur l'usage qui suit les appels d'API et facture par unité de consommation.  
- **Combien de clés sont requises ?** Deux clés – une clé publique et une clé privée – générées depuis votre compte Aspose.  
- **Puis-je vérifier l'utilisation par programme ?** Oui, appelez `License.getConsumptionQuantity()` avant et après le traitement.  
- **Une version d'essai est‑elle disponible ?** Une licence d'essai gratuite peut être obtenue depuis le site Aspose.  
- **Quelle version de Java est prise en charge ?** Java 8 à 17 sont entièrement prises en charge.

## Qu'est-ce que la licence à la consommation dans Aspose.CAD ?

La licence à la consommation est le modèle « pay‑as‑you‑go » d'Aspose.CAD qui enregistre chaque appel d'API comme une unité de consommation. Elle vous permet de suivre l'utilisation exacte, d'éviter le sur‑approvisionnement et de ne payer que ce que vous consommez réellement.

## Pourquoi utiliser la licence à la consommation pour le traitement CAD ?

Aspose.CAD prend en charge **plus de 50** formats d'entrée et de sortie — notamment DWG, DXF, DGN et SVG — et peut traiter des fichiers jusqu'à **2 Go** sans charger le document complet en mémoire. Cette efficacité se traduit par des coûts serveur plus faibles, surtout lors du traitement de gros lots de dessins.

## Prérequis

Avant de plonger dans le monde de la licence à la consommation avec Aspose.CAD, assurez‑vous d'avoir les éléments suivants en place :

### Installation du Java Development Kit (JDK)

Assurez‑vous d'avoir la dernière version du Java Development Kit installée sur votre système. Vous pouvez le télécharger [ici](https://www.oracle.com/java/technologies/javase-downloads.html).

### Bibliothèque Aspose.CAD pour Java

Assurez‑vous de télécharger et d'installer la bibliothèque Aspose.CAD pour Java. Vous pouvez trouver la bibliothèque [ici](https://releases.aspose.com/cad/java/). Vous pouvez également parcourir les autres versions d'Aspose [ici](https://releases.aspose.com/).

## Comment configurer la licence à la consommation dans Aspose.CAD pour Java ?

Chargez vos clés publiques et privées, appelez `License.setMeteredKey(publicKey, privateKey)`, et la bibliothèque passe instantanément en mode licence à la consommation. Cet appel unique active le suivi de l'utilisation pour chaque opération d'API subséquente, vous permettant d'interroger la consommation avant et après toute étape de traitement.

## Importer les packages

Pour utiliser la bibliothèque, importez son package principal :

`import com.aspose.cad.*;`

```java
import com.aspose.cad;
```

## Étape 1 : Définir la clé à la consommation

`setMeteredKey` enregistre vos clés publiques et privées auprès de la bibliothèque Aspose.CAD.

Tout d'abord, définissez la clé à la consommation en utilisant la méthode `setMeteredKey`. Remplacez `<valid public key>` et `<valid private key>` par vos vraies clés publiques et privées.

```java
Metered.setMeteredKey("<valid public key>", "<valid private key>");
```

## Étape 2 : Obtenir la quantité de consommation avant le traitement

`getConsumptionQuantity` renvoie le nombre total d'unités de consommation enregistrées jusqu'à présent.

Récupérez la valeur de la quantité consommée avant d'accéder à l'API Aspose.CAD pour obtenir une première estimation.

```java
BigDecimal quantityOld = Metered.getConsumptionQuantity();
System.out.println("Consumption quantity before processing: " + quantityOld);
```

## Étape 3 : Traitement

Effectuez le traitement CAD souhaité en utilisant les fonctionnalités d'Aspose.CAD. Décommentez le fragment de code lié à votre tâche spécifique, comme le chargement d'une image CAD.

```java
// Example:
// com.aspose.cad.fileformats.cad.CadImage image =
// (com.aspose.cad.fileformats.cad.CadImage)com.aspose.cad.Image.load("BlockRefDgn.dwg");
```

## Étape 4 : Obtenir la quantité de consommation après le traitement

Après le traitement, obtenez à nouveau la valeur de la quantité consommée afin d'évaluer l'impact.

```java
BigDecimal quantity = Metered.getConsumptionQuantity();
System.out.println("Consumption quantity after processing: " + quantity);
```

Répétez ces étapes pour tout traitement ou tâche supplémentaire selon les besoins.

## Problèmes courants et solutions

- **Erreur de clé invalide :** Vérifiez que les deux clés sont copiées exactement comme indiqué dans votre compte Aspose ; les espaces supplémentaires provoquent des échecs d'authentification.  
- **Consommation nulle signalée :** Assurez‑vous d'appeler `License.getConsumptionQuantity()` *après* la première utilisation de l'API ; le premier appel initialise le compteur.  
- **Ralentissement des performances sur les gros fichiers :** Utilisez `CadImage.load(..., LoadOptions)` avec `LoadOptions.setLoadMode(LoadMode.Stream)` pour éviter de charger le fichier complet en mémoire.

## Questions fréquemment posées

**Q1 : Puis‑je utiliser la licence à la consommation à des fins d'évaluation ?**  
A1 : Oui, vous pouvez obtenir une licence d'essai gratuite [ici](https://releases.aspose.com/).

**Q2 : Où puis‑je trouver la documentation détaillée d'Aspose.CAD pour Java ?**  
A2 : Consultez la documentation [ici](https://reference.aspose.com/cad/java/).

**Q3 : Comment acheter une licence pour Aspose.CAD pour Java ?**  
A3 : Visitez la page d'achat [ici](https://purchase.aspose.com/buy).

**Q4 : Existe‑t‑il une option de licence temporaire ?**  
A5 : Oui, vous pouvez explorer les licences temporaires [ici](https://purchase.aspose.com/temporary-license/).

**Q5 : Besoin de soutien communautaire ou avez‑vous des questions spécifiques ?**  
A5 : Rendez‑vous sur le forum Aspose.CAD [ici](https://forum.aspose.com/c/cad/19).

**Q6 : La licence à la consommation fonctionne‑t‑elle avec les déploiements cloud ?**  
A6 : Absolument. Le même appel `setMeteredKey` fonctionne dans Docker, Kubernetes ou les environnements serverless.

**Q7 : Puis‑je réinitialiser le compteur de consommation ?**  
A7 : Le compteur se réinitialise automatiquement au début de chaque nouvelle période de facturation ; vous ne pouvez pas le réinitialiser manuellement.

## Conclusion

Félicitations ! Vous avez maîtrisé avec succès **comment définir la licence à la consommation** avec Aspose.CAD pour Java. En suivant ce guide, vous avez configuré et intégré la licence à la consommation de manière fluide dans votre projet Java, garantissant une utilisation efficace des capacités d'Aspose.CAD tout en maintenant la transparence des coûts.

---

**Dernière mise à jour :** 2026-05-25  
**Testé avec :** Aspose.CAD for Java 24.10  
**Auteur :** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriels associés

- [Convertir CAD en PDF avec Aspose.CAD pour Java – Tutoriels complets](/cad/java/)
- [Créer un PDF à partir de CAD – Exporter DXF en PDF avec Aspose.CAD pour Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Définir la taille du canevas – Fonctionnalités CAD avancées avec Aspose.CAD pour Java](/cad/java/advanced-cad-features/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}