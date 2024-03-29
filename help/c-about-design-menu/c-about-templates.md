---
description: Vous pouvez utiliser des modèles pour gérer vos modèles de présentation et les modèles de transport.
solution: Target
title: A propos des modèles
topic-legacy: Design,Site search and merchandising
uuid: f5805d3e-43bf-4e13-95df-b6bd6b762d11
exl-id: 846f34b3-9857-494e-9010-3db0b48412d3
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '2647'
ht-degree: 1%

---

# À propos des modèles{#about-templates}

Vous pouvez utiliser **[!UICONTROL Templates]** pour gérer vos modèles de présentation et de transport.

## À propos des modèles {#concept_06EB481B14864E18A8AE2BCD1D6EF0B5}

<!-- 

c_about_templates.xml

 -->

Vous pouvez ajouter, modifier, copier, renommer ou supprimer des modèles de présentation et des modèles de transport. Lorsque vous cliquez sur un nom de modèle existant dans le tableau Modèles, il s’ouvre dans une fenêtre d’éditeur (ou de visionneuse) où vous pouvez apporter vos modifications.

Vous pouvez annuler les modifications apportées aux modèles à l’aide de la fonction Historique à partir de la liste déroulante du nom du modèle dans le tableau Modèles.

Vous pouvez réduire le poids de page d’un modèle de présentation en cochant la case **[!UICONTROL Minimize]** correspondante du modèle dans le tableau du modèle. En réduisant le poids de page du modèle, vous réduisez dynamiquement le code JavaScript et CSS intégré. Vous supprimez également les espaces blancs redondants dans le code HTML. La réduction du poids de page du modèle de présentation peut aider à obtenir plus rapidement les résultats de recherche.

Vous pouvez prévisualisation l’aspect du modèle réduit en cliquant sur la liste déroulante en regard du nom de fichier, puis en cliquant sur **[!UICONTROL Preview minimized]**. Si vous réduisez le modèle de présentation principal, veillez à activer la réduction pour les modèles inclus (avec une balise `guided-include`) car cette option n’est pas héritable.

Même si vous réduisez au minimum un modèle de présentation, vous pouvez toujours modifier la version &quot;non minimisée&quot; du même modèle.

Vous pouvez utiliser les règles de pré-recherche, les règles de post-recherche et les règles de fonctionnement pour déterminer quand utiliser l’un de vos autres modèles de présentation. Il est courant de disposer d’une règle telle que &quot;Pour chaque recherche, définissez le modèle ciblé sur xxxx&quot;. Une telle règle étant en place, lorsque vous modifiez le modèle &quot;Par défaut&quot; dans le tableau Modèles, il semble n’avoir aucun effet.

Voir [A propos des règles préalables à la recherche](../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F).

Voir [A propos des règles de post-recherche](../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE).

Voir [A propos des règles de fonctionnement](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

## À propos des modèles de présentation {#section_ACDDEA5C499E481C828A517C230D4596}

Les modèles de présentation sont des modèles HTML qu’un client voit lorsqu’il consulte les résultats de sa recherche sur votre site Web.

Dans la couche de présentation, vous pouvez disposer d’un modèle de présentation unique qui présente les résultats de plusieurs recherches provenant de différentes sources. Vous pouvez définir autant de modèles de présentation que vous le souhaitez et même définir des modèles de présentation que les autres modèles partagent à l&#39;aide des commandes `include`. Le modèle de présentation permet à tous les composants Design, tels que les facettes, les menus et les chemins de navigation, de se regrouper. Pour afficher les différents composants de conception, vous devez utiliser des balises de modèle de présentation.

Voir [Balises de modèle de présentation](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)

Lorsque vous disposez de plusieurs modèles de présentation, vous définissez dans quelles conditions les différents modèles de présentation sont utilisés. Vous pouvez sélectionner le modèle de présentation à utiliser en fonction des paramètres CGI entrants et des cookies. Vous pouvez également changer le modèle de présentation que vous utilisez en fonction du résultat d’une recherche précédente.

Lorsque vous utilisez plusieurs modèles de présentation, veillez à indiquer quel modèle vous souhaitez que les résultats de la recherche s&#39;affichent initialement. Pour ce faire, utilisez la colonne **[!UICONTROL Default]** du tableau Modèles.

## À propos des modèles de transport {#section_35FD3E8AAA4E4695A737DB7E00C3258B}

Les modèles de transport peuvent être des modèles XML ou JSON qui transmettent des données de la recherche principale à la couche de présentation Recherche guidée.

Par défaut, votre compte est configuré pour utiliser des modèles de transport XML. Cependant, si vous préférez utiliser JSON pour transmettre vos données à la recherche guidée, contactez le service de conseil en Adobe qui peut vous aider.

Dans la couche de présentation, vous pouvez disposer d’un modèle de présentation unique qui présente les résultats de plusieurs recherches. Chaque recherche peut utiliser le même modèle de transport ou un modèle de transport personnalisé pour transmettre les données à la couche de présentation. Le modèle de transport n&#39;étant utilisé que pour transmettre des données à la couche de présentation, il ne doit pas comporter de code HTML permettant d&#39;afficher les résultats de la recherche. Le modèle utilise des balises de modèle de transport pour transmettre les résultats de la recherche et les résultats de remplissage des facettes. Dans ces balises, les balises de modèle de recherche standard sont utilisées pour afficher les valeurs réelles.

Voir [Rechercher des balises de modèle](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

**Balises spécifiques au modèle de transport XML**

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Balise de modèle de transport XML </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-xml&gt;&lt;/guided-xml&gt; </span> </p> </td> 
   <td colname="col2"> <p>Il s’agit des balises XML racine que la couche de présentation utilise pour détecter ce qu’elle doit analyser en dehors du modèle de transport. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;general&gt;&lt;/general&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ce jeu de balises entoure les balises de modèle de recherche qui fournissent des données récapitulatives basées sur le jeu de résultats. En règle générale, ces balises contiennent des balises de recherche pour le nombre total de résultats, le résultat le plus faible et le résultat le plus élevé. Vous pouvez définir le nombre de champs globaux supplémentaires que vous souhaitez avec la balise <span class="codeph"> general-field </span>. </p> <p> <b>Exemple</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;general&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;total&gt;&lt;search-total&nbsp;/&gt;&lt;/total&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;lower&gt;&lt;search-lower&nbsp;/&gt;&lt;/lower&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;upper&gt;&lt;search-upper&nbsp;/&gt;&lt;/upper&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;general-field&nbsp;name="my_custom_field"&gt;Some&nbsp;global&nbsp;content&lt;/general-field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/general&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;results&gt;&lt;/results&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cet ensemble de balises est enveloppé dans les résultats de la recherche, de sorte que la recherche guidée sache où les rechercher. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;result&gt;&lt;/result&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ce jeu de balises est enveloppé autour de chaque résultat de recherche, de sorte que la recherche guidée identifie où se trouve le contenu d’un seul résultat de recherche, début et fin. </p> <p> <b>Exemple</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-cdata&gt;&lt;search-url&nbsp;length="500"&nbsp;/&gt;&lt;/search-cdata&gt;&lt;/loc&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;attribute-table name="tablename"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cette balise vous permet de parcourir en boucle chaque élément dans une liste à plusieurs valeurs pour un seul résultat. N’utilisez la balise que dans un résultat. Son Principal objectif est de vous permettre d’effectuer une itération sur les attributs appartenant à un champ de résultat. </p> <p> <b>Exemple</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-url&nbsp;/&gt;&lt;/loc&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;title&gt;&lt;search-title&nbsp;/&gt;&lt;/title&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;attribute-table&nbsp;name="downloads"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;field&nbsp;name="download_title"&gt;&lt;search-display-field&nbsp;name="download_title"&nbsp;/&gt;&lt;/field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;field&nbsp;name="download_link"&nbsp;delimiter="|"&gt;&lt;search-display-field&nbsp;name="download_link"&nbsp;/&gt;&lt;/field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/attribute-table&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facets&gt;&lt;/facets&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cet ensemble de balises transmet les résultats qui remplissent les facettes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facet name="name"&gt;&lt;/facet&gt; </span> </p> </td> 
   <td colname="col2"> <p>Chaque facette doit comporter ses propres balises de facette où le paramètre name correspond au nom de la facette. Les balises de recherche sont utilisées dans les balises de facette pour les valeurs de facette. </p> <p>Voir <a href="../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5" type="concept" format="dita" scope="local"> A propos des facettes </a>. </p> <p> <b>Exemple</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;facets&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;facet&nbsp;name="brand"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/facet&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/facet&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/facets&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;suggestions&gt;&lt;/suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cet ensemble de balises encapsule vos suggestions Voulez-vous dire afin que la recherche guidée identifie les noeuds XML qui contiennent des suggestions. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;suggestion&gt;&lt;/suggestion&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cet ensemble de balises encapsule chaque suggestion Voulez-vous dire. </p> <p> <b>Exemple</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;search-if-suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;suggestion&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;value&gt;&lt;search-suggestion-text&nbsp;/&gt;&lt;/value&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;count&gt;&lt;search-suggestion-result-count&nbsp;/&gt;&lt;/count&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/suggestion&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-if-suggestions&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Balises spécifiques au modèle de transport JSON**

La transmission de JSON par rapport à XML à partir du moteur de recherche est connue pour être plus rapide car sa charge utile est plus faible et l’analyseur plus rapide. Soyez toutefois prudent lorsque vous utilisez JSON pour vous assurer que la sortie est un JSON strict, car l’analyseur n’est pas indulgent.

Si vous découvrez JSON, vous pouvez utiliser les liens et exemples suivants pour vous aider à démarrer :

* Présentation de JSON. Voir [https://www.json.org/](https://www.json.org/).
* Testez votre fichier JSON pour vous assurer qu’il est valide. Voir [https://jsonlint.com/](https://jsonlint.com/).

**Exemple de modèle JSON**

```
{ 
 "general": 
 { 
  "total" : "<search-total />", 
  "lower" : "<search-lower />", 
  "upper" : "<search-upper />", 
  "rbt-trigger-list" : "<search-rbta-trigger-id-list>", 
  "fields" :  
  [ 
   { 
    "name" : "seo_search_title", 
    "value" : "<search-include file="seo/seo_search_title.tpl" />" 
   }, 
   { 
    "name" : "seo_search_keywords", 
    "value" : "<search-include file="seo/seo_search_keywords.tpl" />" 
   } 
  ] 
 }, 
 
 <search-if-suggestions> 
 "suggestions": 
  [ 
  <search-suggestions> 
  { 
   "suggestion":"<search-suggestion-text />", 
   "count": "<search-suggestion-result-count>" 
  }<search-if-not-last-suggestion>,</search-if-not-last-suggestion> 
  </search-suggestions> 
 ], 
 </search-if-suggestions> 
 
 "facets" : 
 [ 
  { 
   "name" : "leveli", 
   "values" : [ <search-field-value-list name="leveli" quotes="yes" sortby="values" data="values" encoding="json"/>], 
   "counts" : [<search-field-value-list name="leveli" quotes="no" sortby="values" data="results" />] 
  }, 
  { 
   "name" :"levelii", 
   "values" : [<search-field-value-list name="levelii" quotes="yes" sortby="values" data="values" encoding="json"/>], 
   "counts" : [<search-field-value-list name="levelii" quotes="no" sortby="values" data="results" />] 
  }, 
  { 
   "name" : "brand", 
   "values" : [<search-field-value-list name="brand" quotes="yes" sortby="values" data="values" encoding="json"/>], 
   "counts" : [<search-field-value-list name="brand" quotes="no" sortby="values" data="results" />] 
  }, 
 ], 
 "results" : 
 [ 
  <search-results> 
  { 
   "fields" : 
   [ 
    { 
     "name" : "index", 
     "value" : "<search-index />" 
    }, 
    { 
     "name" : "loc", 
     "value" : "<search-display-field name="url" length="500" encoding="json"/>" 
    }, 
    { 
     "name" : "title", 
     "value" : "<search-display-field name="title" encoding="json"/>" 
    }, 
    { 
     "name" : "img_url_thumbnail", 
     "value" : "<search-display-field name="img_url_thumbnail" encoding="json"/>" 
    }, 
    { 
     "name" : "description", 
     "value" : "<search-display-field name="description" encoding="json"/>" 
    }, 
    { 
     "name" : "mdi", 
     "value" : "<SEARCH-RBTA-DISPLAY-MDI-FIELD>" 
    } 
   ] 
  }<search-if-not-last>,</search-if-not-last>  
  </search-results> 
 ] 
}
```

**Exemple de section de résultat JSON avec une table d’attributs de résultats**

```
{ 
 "results" : 
 [ 
  <search-results> 
  { 
   "fields" : 
   [ 
    { 
     "name" : "index", 
     "value" : "<search-index />" 
    }, 
    { 
     "name" : "loc", 
     "value" : "<search-display-field name="url" length="500" encoding="json"/>" 
    } 
   ], 
   "tables" : 
   [ 
    { 
     "name" : "downloads", 
     "fields" : 
     [ 
      { 
       "name" : "download_title", 
       "value" : <search-display-field name="download_title" encoding="json"/> 
      }, 
      { 
       "name" : "download_link", 
       "value" : <search-display-field name="download_link" encoding="json"/> 
      } 
     ] 
    } 
   ] 
  }<search-if-not-last>,</search-if-not-last>  
  </search-results> 
 ] 
}
```

**Exemple de section Facette JSON pour une facette avec des champs associés**

```
{ 
 facets" : 
 [ 
  { 
   "name" : "t1", 
   "values" : [<search-field-value-list name="t1" quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />], 
   "counts" : [<search-field-value-list name="t1" quotes="yes" commas="yes" data="results" sortby="values" />], 
   "custom-fields" : 
   [ 
    { 
     "name" : "taxonmyId", 
     "value" : [<search-field-value-list name="tax1" quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />] 
    } 
   ] 
  } 
 ] 
}
```

**Exemple de section de facette JSON pour les facettes avec graphique à secteurs**

```
{ 
  "facets" : 
  [  
   { 
    "name" : "fvalue0", 
                  "dynamic" : 1, 
                  "display-names" : [<search-field-value-list name="fname0" quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />], 
    "values" : [<search-field-value-list name="fvalue0" quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />], 
    "counts" : [<search-field-value-list name="fvalue0" quotes="no" commas="yes" data="results" sortby="values" />] 
   } 
  ] 
} 
```

## Ajouter un nouveau fichier de présentation ou de modèle de transport {#task_73199757B6E748CAA604902FF913F012}

Vous pouvez utiliser **[!UICONTROL Add Template]** pour ajouter des modèles de présentation (.tmpl) ou des modèles de transport (.tpl) à la page [!DNL Templates].

<!-- 

t_adding_a_new_presentation_or_transport_template_file.xml

 -->

**Pour ajouter une nouvelle présentation ou un fichier de modèle de transport**

1. Dans le menu produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Sur la page [!DNL Templates], cliquez sur **[!UICONTROL Add New Template]**.
1. Dans la boîte de dialogue [!DNL Add Template], définissez les options de votre choix.

   <!-- 
   
   r_add_template_options.xml
   
   -->

   | Option | Description |
   |--- |--- |
   | Nouveau nom de fichier | Indique le nom du modèle à ajouter. L’extension de fichier appropriée est automatiquement ajoutée au nom du fichier, en fonction du type de modèle sélectionné.  Les modèles de présentation ont une extension de fichier .tmpl ; Les modèles de transport ont une extension de fichier .tpl. |
   | Nouveau type de modèle | Vous permet de choisir une présentation ou un modèle de transport à ajouter.  Voir [À propos des modèles](../c-about-design-menu/c-about-templates.md). |

   Voir aussi [Modification d&#39;une présentation ou d&#39;un modèle de transport](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3).
1. Cliquez sur **[!UICONTROL Add]**.
1. (Facultatif) Sur la page [!DNL Templates], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Modification d&#39;une présentation ou d&#39;un modèle de transport {#task_800E0E2265C34C028C92FEB5A1243EC3}

Vous pouvez utiliser l’éditeur de modèles pour vue et modifier le contenu de votre présentation et transporter les fichiers de modèles.

<!-- 

t_editing_a_template.xml

 -->

Vous pouvez modifier et tester votre présentation par étapes et vos modèles de transport, pendant que les visiteurs de votre site Web continuent à utiliser les versions en direct de vos modèles. Vous testez votre modèle intermédiaire à l’aide de la version intermédiaire de l’URL de votre domaine de recherche. Par exemple, vous pouvez tester votre modèle de transport par étapes en exécutant une requête par étapes ( `sp_staged=1`) avec `sp_t` définie sur le nom de votre modèle de transport. Lorsque vous êtes satisfait de l’apparence de la mise en page, vous pouvez utiliser **[!UICONTROL Push Live]** depuis l’éditeur de modèles pour diffuser le modèle. Une fois que le modèle est actif, les visiteurs du site commencent à l’utiliser.

Utilisez la référence de balise du modèle de présentation pour savoir comment associer votre modèle de présentation aux composants de recherche guidée tels que les facettes, les chemins de navigation et les menus.

Voir [Balises de modèle de présentation](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)

Utilisez la référence de balise de modèle de transport pour en savoir plus sur les balises à utiliser dans les modèles de transport.

Voir [Balises de modèle de transport](../c-appendices/c-templates.md#reference_227D199F5A7248049BE1D405C0584751)

**[!UICONTROL To edit a presentation or a transport template]**

1. Dans le menu produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Sur la page [!DNL Templates], cliquez sur une présentation ou un nom de fichier de modèle de transport.
1. Sur la page [!DNL Template Editor], effectuez les modifications que vous souhaitez apporter aux balises et au codage.

   Soyez prudent quant aux modifications que vous apportez dans le fichier [!DNL Template Editor]; il n&#39;existe pas de fonction Annuler. Si vous effectuez une modification non souhaitée et souhaitez revenir à la version précédente du fichier, vous pouvez cliquer sur **[!UICONTROL Cancel]** pour revenir à la table des modèles (en supposant que vous n&#39;ayez enregistré aucune de vos modifications jusqu&#39;à ce moment). Si vous avez déjà enregistré vos modifications, vous pouvez utiliser **[!UICONTROL History]** dans l’éditeur pour annuler ces modifications.
1. (Facultatif) Cliquez sur **[!UICONTROL Insert Symbol]** pour entrer des caractères spéciaux et des symboles qui ne comportent pas de clés correspondantes sur les claviers anglais des États-Unis.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

1. Fermez la page Editeur de modèle lorsque vous avez terminé ; vous revenez à la page Modèles.

## Copie d&#39;une présentation ou d&#39;un fichier de modèle de transport {#task_B744AB3384C84DD59C33CD25E18C2C90}

Vous pouvez utiliser **[!UICONTROL Copy Template]** pour gagner du temps en dupliquant un modèle de présentation existant (.tmpl) ou un modèle de transport (.tpl) et l&#39;ajouter à la page Modèles.

<!-- 

t_copying_a_presentation_or_a_transport_template.xml

 -->

Vous devez modifier le nom du modèle, son type ou les deux. Si vous n’apportez aucune modification, le modèle n’est pas copié.

Un modèle doit déjà être ajouté pour pouvoir copier un modèle.

Voir [Ajouter un nouveau fichier de présentation ou de modèle de transport](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012).

**Pour copier une présentation ou un fichier de modèle de transport**

1. Dans le menu produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Sur la page [!DNL Templates], dans la liste déroulante en regard d’un nom de modèle à copier, cliquez sur **[!UICONTROL Copy]**.
1. Dans la boîte de dialogue [!DNL Copy Template], définissez une ou plusieurs options de votre choix.
1. Cliquez sur **[!UICONTROL Copy]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Attribution d’un nouveau nom à une présentation ou à un fichier de modèle de transport {#task_CC30050FC2DE4898BF44379D8378EB31}

Vous pouvez utiliser [!DNL Rename Template] pour modifier le nom d&#39;un modèle de présentation existant (.tmpl) ou d&#39;un modèle de transport (.tpl).

<!-- 

t_renaming_a_presentation_or_a_transport_template_file.xml

 -->

Vous pouvez également modifier le type de modèle, si vous le souhaitez.

Un modèle doit déjà être ajouté pour renommer un modèle.

Voir [Ajouter un nouveau fichier de présentation ou de modèle de transport](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012).

**Pour renommer une présentation ou un fichier de modèle de transport**

1. Dans le menu produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Sur la page [!DNL Templates], dans la liste déroulante en regard d’un nom de modèle que vous souhaitez renommer, cliquez sur **[!UICONTROL Rename]**.
1. Dans la boîte de dialogue [!DNL Rename Template], définissez une ou plusieurs options de votre choix.
1. Cliquez sur **[!UICONTROL Rename]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Suppression d&#39;une présentation ou d&#39;un fichier de modèle de transport {#task_67E532C2B83A449687737E3B06C5AA58}

Vous pouvez utiliser **[!UICONTROL Delete Template]** pour supprimer un modèle de présentation existant (.tmpl) ou un modèle de transport (.tpl).

<!-- 

t_deleting_a_presentation_or_a_transport_template_file.xml

 -->

Vous disposez peut-être déjà d’une version correspondante du modèle mis en scène qui est publiée. Si tel est le cas, veillez à publier le modèle supprimé en utilisant **[!UICONTROL Staging]** afin qu’il soit également supprimé de l’environnement en direct. Vous pouvez également utiliser **[!UICONTROL Push Live]** sur la page Modèles.

Voir [A propos de l’évaluation](../c-about-staging.md#concept_08B8F3CA1F4241108F14BA7FC7806CA7)

Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)

Un modèle doit déjà être ajouté pour pouvoir supprimer un modèle.

Voir [Ajouter une nouvelle présentation ou un nouveau fichier de modèle de transport](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)

**Pour supprimer une présentation ou un fichier de modèle de transport**

1. Dans le menu produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Sur la page [!DNL Templates], dans la liste déroulante en regard d&#39;un nom de modèle à supprimer, cliquez sur **[!UICONTROL Delete]**.
1. Dans la boîte de dialogue [!DNL Delete Template], cliquez sur **[!UICONTROL Delete.]**
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Aperçu du modèle de présentation minimisé {#task_1757B6207CC74221AE4BFFE5674D320B}

Vous pouvez utiliser **[!UICONTROL Preview minimized]** pour voir à quoi ressemblerait le poids de page réduit d&#39;un modèle de présentation si vous choisissez de le réduire.

<!-- 

t_previewing_the_presentation_template_minimized.xml

 -->

Si vous réduisez le modèle de présentation principal, veillez à activer la réduction pour les modèles inclus (avec balise d’inclusion guidée) car cette option n’est pas héritable.

Voir [Réduction du poids de page d&#39;un modèle de présentation sur votre...](../c-about-design-menu/c-about-templates.md#task_B09BB3CE89714DEAAE8D9A899CF3009E)

Un modèle doit déjà être ajouté à la prévisualisation du modèle réduit.

Voir [Ajouter une nouvelle présentation ou un nouveau fichier de modèle de transport](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)

Vous pouvez prévisualisation le code XML d’un fichier de modèle de transport.

Voir [Prévisualisation du XML d&#39;un fichier de modèle de transport](../c-about-design-menu/c-about-templates.md#task_58C6C52078E14AD88D2B2F0B3C439AE8)

**Pour prévisualisation le modèle de présentation réduit**

1. Dans le menu produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Sur la page [!DNL Templates], dans la liste déroulante en regard du nom d’un modèle de présentation, cliquez sur **[!UICONTROL Preview minimized]**.

   Utilisez la colonne **[!UICONTROL Type]** du tableau Modèles pour trier les modèles par présentation et par transport.
1. (Facultatif) Sur la page [!DNL Preview Minimized Template], cochez **[!UICONTROL Wrap lines]** pour lire les balises dans la fenêtre définie.
1. Cliquez sur **[!UICONTROL Close]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Réduction du poids de page d’un modèle de présentation sur votre site Web {#task_B09BB3CE89714DEAAE8D9A899CF3009E}

Vous pouvez réduire le poids de page d’un modèle de présentation en utilisant l’option **[!UICONTROL Minimize]** du tableau de modèle.

<!-- 

t_reducing_the_page_weight_of_a_presentation_template.xml

 -->

En réduisant le poids de page du modèle, vous réduisez dynamiquement le code JavaScript et CSS intégré. Vous supprimez également les espaces blancs redondants dans le code HTML. La réduction du poids de page du modèle de présentation peut aider à obtenir plus rapidement les résultats de recherche.

Vous pouvez également prévisualisation l’aspect du modèle de présentation minimisé à l’aide de **[!UICONTROL Preview minimized]**.

Voir [Prévisualisation du modèle de présentation minimisé](../c-about-design-menu/c-about-templates.md#task_1757B6207CC74221AE4BFFE5674D320B).

**[!UICONTROL To reduce the page weight of a presentation template on your website]**

1. Dans le menu produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Sur la page [!DNL Templates], sous la colonne [!DNL Minimize], cochez la case correspondant à un ou plusieurs fichiers de modèle de présentation que vous souhaitez réduire au minimum sur votre site Web.

   Utilisez la colonne **[!UICONTROL Type]** du tableau [!DNL Templates] pour trier les modèles par présentation et par transport.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Définition du fichier de modèle de présentation par défaut à utiliser sur votre site Web {#task_C1E8CE817E4D43E096167A347C54DD53}

Lorsque vous disposez de plusieurs modèles de présentation, vous pouvez indiquer le modèle qui est initialement utilisé pour afficher les résultats de la recherche.

<!-- 

t_setting_the_default_presentation_template_file_to_use.xml

 -->

Vous pouvez utiliser les règles de pré-recherche, les règles de post-recherche et les règles de fonctionnement pour déterminer à quel moment l’un des autres modèles de présentation doit être utilisé.

Voir [A propos des règles préalables à la recherche](../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F).

Voir [A propos des règles de post-recherche](../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE).

Voir [A propos des règles de fonctionnement](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

Il est courant de disposer d’une règle telle que &quot;Pour chaque recherche, définissez le modèle de présentation ciblé sur xxxx&quot;. Une telle règle étant en place, la modification du modèle &quot;par défaut&quot; sur la page Modèles semble n’avoir aucun effet.

**[!UICONTROL To set the default presentation template file to use on your website]**

1. Dans le menu produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Sur la page [!DNL Templates], sous la colonne [!DNL Default], cliquez sur le bouton radio du fichier de modèle de présentation correspondant que vous souhaitez utiliser par défaut.

   Utilisez la colonne **[!UICONTROL Type]** du tableau [!DNL Templates] pour trier les modèles par présentation et par transport.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Prévisualisation du XML d&#39;un fichier de modèle de transport {#task_58C6C52078E14AD88D2B2F0B3C439AE8}

Vous pouvez utiliser [!DNL Preview] pour examiner le XML d&#39;un modèle de transport que vous avez ajouté.

<!-- 

t_previewing_the_xml_of_a_transport_template_file.xml

 -->

Un modèle de transport doit déjà être ajouté à la prévisualisation du code XML du modèle.

Voir [Ajouter un nouveau fichier de présentation ou de modèle de transport](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012).

Vous pouvez prévisualisation des fichiers de modèle de présentation minimisés pour vue de leur poids de page réduit.

Voir [Prévisualisation du modèle de présentation minimisé](../c-about-design-menu/c-about-templates.md#task_1757B6207CC74221AE4BFFE5674D320B).

**Pour prévisualisation du XML d’un fichier de modèle de transport**

1. Dans le menu produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Sur la page [!DNL Templates], dans la liste déroulante en regard d&#39;un nom de modèle de transport, cliquez sur **[!UICONTROL Preview]**.

   Utilisez la colonne **[!UICONTROL Type]** du tableau [!DNL Templates] pour trier les modèles par présentation et par transport.
1. Fermez la fenêtre d’affichage et revenez à [!DNL site search/merchandising].
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
