---
description: Search&amp ; amp ; Notes de mise à jour de Promote 8.14.0.
solution: Target
title: Notes de mise à jour de Search&amp ; amp ; Promote 8.14.0 (22/05/2014)
topic-legacy: Release Notes,Site search and merchandising
uuid: 308d84a9-ec38-4fec-b146-e8a353e65be4
exl-id: fcc00d85-128e-4015-aa82-7d31606cb076
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 67%

---

# Notes de mise à jour de la version 8.14.0 (22/05/2014){#search-promote-release-notes} de la Search &amp; Promote 8.14.0

**Correctifs**

* En cas d’échec de [!DNL sqlite_open], l’ancien fichier de base de données sqlite est supprimé et un nouveau fichier est entièrement créé.
* Les résultats principaux d’une recherche étaient incohérents lorsque la même recherche était effectuée à plusieurs reprises.
* Amélioration des performances du traitement des modèles lorsque de nombreux champs s’affichent par résultat de recherche.
* Notes Ajoutées à **[!UICONTROL Business Rule History]**.
* Lors des opérations d’indexation, les performances des déclencheurs basés sur les résultats et de la phase de regénération de l’index se dégradaient au fil du temps.
* L&#39;option **[!UICONTROL Reset SPIN cache]** booléenne no/next-run a été remplacée par une option à trois états : no/always/next-run.
