---
description: valeur nulle
seo-description: valeur nulle
seo-title: Modèles
solution: Target
title: Modèles
topic: Appendices,Site search and merchandising
uuid: 78299032-dc23-4dfe-b68f-cd57b2b6d7d8
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# Modèles{#templates}

## Modèles {#concept_A5CFB6BD805D49459A96219AF1B17842}

## Balises de modèle de présentation {#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64}

Liste des balises et attributs de recherche/marchandisage de site pour les modèles de présentation.


Un modèle de présentation est un fichier HTML qui comprend des balises de modèle de présentation définies par la recherche/le marchandisage sur le site. Ces balises indiquent le format des résultats de recherche affichés par les clients.

Voir [A propos des modèles](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

Vous pouvez sélectionner l’un des groupes de balises de présentation suivants :

* [Déclarations](../c-appendices/c-templates.md#section_82C5CA734D2941EB858FEFE3B695D2EC)
* [Résultats](../c-appendices/c-templates.md#section_06F249C9F6AE4B0F8C32117E19DCC905)
* [Facettes](../c-appendices/c-templates.md#section_EA4C5678D5864B89BAB4D0DFE62A4624)
* [Chemin de navigation](../c-appendices/c-templates.md#section_9B39B71FA6EC49FA8D88AD8A3BA987F7)
* [Menus](../c-appendices/c-templates.md#section_1D489ADF041F4351A66E5D5742125CA8)
* [Pagenav](../c-appendices/c-templates.md#section_2EE397635C514BBC8D668278EA314F35)
* [Recherches récentes](../c-appendices/c-templates.md#section_8CD907521F584257B475595B01A5964B)
* [Voulez-vous dire](../c-appendices/c-templates.md#section_C1EB3B9D8E1242798A6E04609D1E3543)
* [Remplissage automatique](../c-appendices/c-templates.md#section_897316BEE1454E839A56B565CA4AF018)
* [Magasin](../c-appendices/c-templates.md#section_A33E25DB5E67404A823BD9618665B773)
* [Zones](../c-appendices/c-templates.md#section_B9B3179E000C42D492E1541F2FE44CB5)
* [Indicateurs de boucle](../c-appendices/c-templates.md#section_387322CA0AA843A2ACF2795C328673E9)
* [Langue diverse](../c-appendices/c-templates.md#section_BFE8DC98E26F4D7BB60FEC54D9A5DC6C)

## Déclarations {#section_82C5CA734D2941EB858FEFE3B695D2EC}

Les déclarations sont des balises de déclaration guidée spéciales que vous pouvez définir en haut d’un modèle de présentation de niveau supérieur. Toutes les déclarations suivantes sont ignorées, y compris les déclarations dans les modèles inclus.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Baliser </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-content-type-header content="content-type"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Par défaut, le modèle de présentation est renvoyé avec un type MIME de texte/html. Vous pouvez modifier le type de contenu utilisé avec cette balise. </p> <p>Déclarez cette balise aussi haut que possible dans votre modèle de présentation. N’ajoutez pas d’autre texte sur la même ligne avec cette balise. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-xml-statement [charset="charset"]&gt; </span> </p> </td> 
   <td colname="col2"> <p> Si vous renvoyez du code XML, vous pouvez utiliser cette balise pour créer la déclaration XML. Faites de cette balise la première ligne du modèle de présentation. Lorsque vous utilisez cette balise, le type de contenu est automatiquement défini sur text/xml, sauf si vous le remplacez par <span class="codeph"> &lt;guided-content-type-header&gt; </span> dans la première ligne. Si vous ne spécifiez pas de jeu de caractères, la valeur par défaut est UTF-8. Cette balise génère la sortie suivante dans votre document XML : </p> <p> <span class="codeph"> &lt;?xml version="1.0" encoding="nom_jeu" standalone="yes" ?&gt; </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Résultats {#section_06F249C9F6AE4B0F8C32117E19DCC905}

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Baliser </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng 1/31/13--> <span class="codeph"> &lt;guided-results [gsname="searchname"]&gt;&lt;/guided-results&gt; </span> </p> </td> 
   <td colname="col2"> <p>La balise guided-results définit les limites d’une boucle de résultats. Tout jeu de résultats est accessible en spécifiant un attribut <span class="codeph"> gsname </span> . Si aucun <span class="codeph"> nom de domaine </span> n'est donné, les résultats de recherche par défaut s'affichent. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng 1/31/13--> <span class="codeph"> &lt;guided-result-link [gsname="fieldname"] [attr="value"]+&gt;&lt;/guided-result-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Pour créer un lien vers un résultat donné, utilisez la <span class="codeph"> </span> balise de lien de résultat guidé. En définissant un attribut <span class="codeph"> gsname </span> , vous pouvez utiliser un champ de l’index au lieu de la balise "loc" standard qui fait référence à "search-url". Tous les autres attributs, tels que class et target, peuvent également être transmis, qui sont générés dans la balise d’ancrage résultante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng 1/31/13--> <span class="codeph"> &lt;guided-result-img gsname="fieldname" [attr="value"]+&gt; </span> </p> </td> 
   <td colname="col2"> <p>La <span class="codeph"> balise &lt;guided-result-img&gt; </span> permet de créer des balises d’image plutôt que d’incorporer des variables dans une balise img brute <span class="codeph"> </span> . </p> <p>Spécifiez le champ à utiliser pour le chemin d’accès à l’image dans l’attribut <span class="codeph"> gsname </span> . Le résultat est une balise <span class="codeph"> img </span> avec tous les attributs HTML standard que vous avez définis, transmis. Ainsi, l’exemple suivant : </p> <p> <code class="syntax html"> &lt;guided-result-img&nbsp;gsname="thumbnail" 
      &nbsp;class="thumb"&nbsp;border="0"/&gt; </code> </p> <p>becomes: </p> <p> <code class="syntax html"> &lt;img&nbsp;src="prod8172.jpg"&nbsp;class="thumb" 
      &nbsp;border="0"/&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 1/31/13; search-eng version does not have [escape...] Added ijson on 8/28/2015--> <span class="codeph"> &lt;guided-result-field gsname="fieldname" [escape="html|url|js|json|ijson|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p> Toute information à présenter dans les résultats s’affiche sous la forme d’une balise <span class="codeph"> &lt;guided-result-field&gt; </span> (sauf lors de l’utilisation de balises de génération automatique telles que la <span class="codeph"> balise &lt;guided-result-img&gt; </span> ). </p> <p>Indiquez le nom du champ d’index de recherche dans <span class="codeph"> gsname </span>. La chaîne exacte transmise est générée dans le modèle. </p> <p>Vous pouvez spécifier une option d’échappement si vous souhaitez que ce champ soit séparé de ce qui a été spécifié dans le modèle de transport. </p> <p>Ce codage est appliqué au-dessus du codage spécifié dans le modèle de transport. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <span class="codeph"> &lt;guided-if[-not]-result-field gsname="nom_champ&gt;&lt;/guided-if-résultat-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cet ensemble de balises conditionnelles est vrai s’il existe du contenu dans le champ spécifique à afficher. Si aucun contenu n’existe, la condition est false. Vous pouvez utiliser les balises pour décider si le code HTML environnant est affiché ou non si une valeur n’existe pas, ou si une autre image est affichée, etc. </p> <p> <code class="syntax html"> &lt;guided-if-result-field&nbsp;gsname="thumbnail"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-result-img&nbsp;gsname="thumbnail"&nbsp;class="thumb"&nbsp;/&gt; 
      &lt;guided-else-result-field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;img&nbsp;src="nothumb.jpg"&nbsp;class="nothumb"&nbsp;/&gt; 
      &lt;/guided-if-result-field&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <code> &lt;guided-if[-not]-result-wrap&gt; 
      &lt;guided-else-result-wrap&gt; 
      &lt;/guided-if[-not]-result-wrap&gt; </code> </p> </td> 
   <td colname="col2"> <p>Lors de l’affichage des résultats dans des colonnes, cette balise permet d’identifier si le résultat actuel marque la fin d’une colonne. </p> <p>Lorsque la condition booléenne est vraie, du code HTML est ajouté à la fin du résultat pour terminer la ligne et en démarrer une nouvelle. Lorsqu’il s’agit de la dernière ligne, aucune nouvelle ligne n’est démarrée. </p> <p>Voir <span class="codeph"> &lt;guided-if-not-last&gt; </span> pour en savoir plus sur cette balise. </p> <p> <code class="syntax html"> &lt;guided-if-result-wrap&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-not-last&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-not-last&gt; 
      &nbsp;&lt;/guided-if-result-wrap&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-results-found [gsname="searchname"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Renvoie une valeur de 1 si la requête de recherche principale renvoyait des résultats et de 0 dans le cas contraire. Si aucun <span class="codeph"> nom de domaine </span> n’est spécifié, la balise suppose la recherche principale. Cette balise est utile pour transmettre la logique aux routines JavaScript. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-results-total [gsname="searchname"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Renvoie le nombre total de résultats dans l’ensemble de résultats spécifié. Suppose la recherche par défaut lorsqu’aucun <span class="codeph"> nom </span> gsname n’est donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-results-lower [gsname="searchname"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Renvoie le numéro de résultat du résultat inférieur sur la page pour le jeu de résultats spécifié. Suppose la recherche par défaut lorsqu’aucun <span class="codeph"> nom </span> gsname n’est donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-results-upper [gsname="searchname"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Renvoie le numéro de résultat du résultat supérieur sur la page pour le jeu de résultats spécifié. Suppose la recherche par défaut lorsqu’aucun <span class="codeph"> nom </span> gsname n’est donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> 

    &amp;lt;/guided-if[-not]-results-found&amp;gt; &lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>Affiche le contenu lorsque les résultats sont trouvés. Ou, ne montre aucun résultat HTML lorsque les résultats sont introuvables. </p> <p> <code class="syntax html"> &lt;guided-if-results-found&nbsp;gsname="products"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-results&nbsp;gsname="products"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;... 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-results&gt; 
      &lt;guided-else-results-found&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;No&nbsp;results&nbsp;were&nbsp;found. 
      &lt;/guided-if-results-found&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-title/&gt; </span> </p> </td> 
   <td colname="col2"> <p>La balise <span class="codeph"> &lt;guided-result-title&gt; </span> donne la valeur du champ de modèle de transport de titre spécifié avec <span class="codeph"> &lt;title&gt; </span> balise de transport. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-description/&gt; </span> </p> </td> 
   <td colname="col2"> <p>La balise <span class="codeph"> &lt;guided-result-description&gt; </span> donne la valeur du champ de modèle de transport de description spécifié avec <span class="codeph"> &lt;description&gt; </span> balise de transport. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-loc/&gt; </span> </p> </td> 
   <td colname="col2"> <p>La balise &lt; <span class="codeph"> guided-result-loc&gt; </span> donne la valeur du champ de modèle de transport loc spécifié avec <span class="codeph"> &lt;loc&gt; </span> balise de transport. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;/guided-if-result-field&amp;gt; &lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>True s’il existe du contenu dans le champ spécifique à afficher. Si aucun contenu n’existe, la condition est false. Utilisez les balises pour déterminer si le code HTML environnant est affiché ou non si une valeur n’existe pas, ou si une autre image est affichée, etc. </p> <p> <code class="syntax html"> &lt;guided-if-result-field&nbsp;gsname="thumbnail"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-result-img&nbsp;gsname="thumbnail"&nbsp;class="thumb"/&gt; 
      &lt;guided-else-result-field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;img&nbsp;src="nothumb.jpg"&nbsp;class="nothumb"/&gt; 
      &lt;/guided-if-result-field&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-attribute-table gsname="nom_table"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cette balise fournit une boucle à travers la table d’attributs définie dans le modèle de transport avec la balise de transport <span class="codeph"> &lt;attribute_table&gt; </span> . Il existe une <span class="codeph"> balise &lt;guided-result-attribute-table-field&gt; </span> pour afficher les valeurs de champ de table d’attributs. Il est également possible d’utiliser une balise <span class="codeph"> de champ de résultats guidés ordinaire </span> dans une boucle pour afficher d’autres champs de résultats. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-attribute-table-field gsname="nom du champ" [escape="html|url|js|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Affiche le champ de la table d’attributs tel que défini dans le modèle de transport. </p> <p> 

    ...
    
    &amp;lt;ul&amp;gt;
    
    &amp;lt;guided-result-attribute-table&amp;nbsp;gsname=&quot;downloads&quot;&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;lt;li&amp;
    &amp;nbsp;&amp;nbsp;nbsp;nbsp; sp;&amp;nbsp;&amp;lt;a&amp;nbsp;href=&quot;&amp;lt;guided-result-attribute-table-field&amp;nbsp;gsname=&quot;download_link&quot;&amp;nbsp;/&amp;gt;gt;gt;
    &amp;nbsp;&amp;nbsp;&amp;nbsp;;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;guided-result-attribute-table-field&amp;nbsp;gsname=&quot;download_title&quot;&amp;nbsp;gt;
    &amp;nbsp;&amp;nbsp; amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;/a&amp;gt;&amp;nbsp;(&amp;lt;guided-result-field&amp;nbsp;gsname=&quot;title&quot;/&amp;gt;)
    &amp;nbsp;&amp;nbsp;&amp;lt;/li&amp;;
    &amp;lt;/guided-result-attribute-table&amp;gt;&amp;lt;/ul&amp;gt;...
    
    &amp;lt;/guided-results&amp;gt; &lt;/code> &lt;/p> &lt;/td>
    
    
    
    
</tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release in October 2014--> <span class="codeph"> &lt;guided-trace [gsname="nom_recherche"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Génère les informations de trace trouvées dans les données de trace dans la section générale de la sortie des données JSON par le modèle de transport pour la recherche donnée. </p> <p>Si aucun nom de recherche n’est spécifié, <span class="codeph"> la valeur par défaut </span> est utilisée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release on October 30, 2014)--> <span class="codeph"> &lt;guided-result-trace/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Génère le contenu JSON trouvé dans les résultats &gt; informations de trace de la sortie de données JSON par le modèle de transport pour le résultat de recherche actuel. </p> <p>Cette balise n’est valide que dans la boucle <span class="codeph"> &lt;guided-results&gt;&lt;/guided-results&gt; </span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Facettes {#section_EA4C5678D5864B89BAB4D0DFE62A4624}

Les facettes sont des composants de navigation qui vous permettent d’analyser les résultats de la recherche. Vous pouvez utiliser les balises facet pour afficher diverses facettes sur votre modèle de présentation. Vous référencez les facettes par nom.

Voir [A propos des facettes](../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5).

Voir [A propos de la rampe de facettes](../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB).

Voir [A propos des facettes](../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899)dynamiques.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Baliser </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 02/27/2014--> <span class="codeph"> &lt;guided-dynamic-facets&gt;&lt;/guided-dynamic-facets&gt; </span> </p> </td> 
   <td colname="col2"> 
    <!--NEW 2/2/2014--> <p>Contexte de boucle pour toutes les facettes dynamiques d’une recherche donnée. </p> <p>La balise de modèle de présentation <span class="codeph"> &lt;guided-facet&gt; </span> est modifiée de sorte que l’attribut gsname soit automatiquement fourni par le contexte de boucle <span class="codeph"> &lt;guided-dynamic-facets&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-display-name gsname=" <span class="varname"> facetname </span>"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Renvoie le libellé d’affichage de la facette. </p> <p>Si la facette utilise la balise <span class="codeph"> &lt;display-name&gt; </span> sur le modèle de transport, le contenu de cette balise devient le libellé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-rail&gt;&lt;/guided-facet-rail&gt; </span> </p> </td> 
   <td colname="col2"> <p> Définit une section du modèle de présentation utilisée comme modèle répété pour chaque facette du rail de facettes. </p> <p> Chaque facette appartenant au rail de facettes utilise cette section pour évaluer sa sortie. </p> <p>Voici un exemple de rail de facettes : </p> <p> <code class="syntax html"> &lt;guided-facet-rail&gt; 
      &nbsp;&nbsp;&lt;guided-facet&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-display-name/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;... 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet&gt; 
      &nbsp;&nbsp;&lt;/guided-facet-rail&gt; </code> </p> <p>Notez que les balises suivantes n’ont pas besoin de l’attribut <span class="codeph"> gsname </span> lorsqu’elles se trouvent à l’intérieur de la balise <span class="codeph"> &lt;guided-facet-rail&gt; </span> comme une valeur déterminée dynamiquement au moment de la recherche et correctement substituée : </p> 
    <ul id="ul_5B5ACAFD2B8848DDB27471AB9DA7BE6E"> 
     <li id="li_5A07E78D51FE4708879DD742C877FFFF">guidé-facette </li> 
     <li id="li_B875DCACD7AB4FC890A456A6939AB657">guided-facet-display-name </li> 
     <li id="li_B70450749E864DE7BA401E3CD6EF5EB3">guidé-facette-total-count </li> 
     <li id="li_DECDF5EF6FF7454F86C236D322F2BFEA">guided-facet-undo-link </li> 
     <li id="li_176949227AC14E8CA643A419E10F7B5A">guided-facet-undo-path </li> 
     <li id="li_B32D981281744462BC680F6EFEAC0069">guidé-facette-comportement </li> 
    </ul> <p>Les critères de tri sur la <span class="wintitle"> page </span> du rail de facettes déterminent la position des facettes. Vous pouvez choisir l’ordre de tri dans la liste déroulante Méthode de facettes de tri. </p> <p> 
     <!--NEW 02/27/2014-->Cette balise peut éventuellement accepter une valeur d’attribut gsname de <span class="codeph"> _dynamic_facets </span>, qui fournit un contexte de boucle pour toutes les facettes dynamiques de cette recherche. Ce rail de facettes prédéfini est également exposé dans l’interface utilisateur des règles de fonctionnement pour que la <span class="codeph"> facette Push X de l’action dans le rail de facettes '_dynamic_facets' soit positionnée Y </span>". </p> <p>Voir <a href="../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB" format="dita" scope="local">A propos de la rampe de facettes </a>. </p> <p>Voir aussi <a href="../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> A propos des facettes dynamiques </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match current search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet gsname=" <span class="varname"> facetname </span>" height=" 60px <span class="varname"> " width=" </span>120px <span class="varname"> </span>"&gt;&lt;/guided-facet&gt; </span> </p> </td> 
   <td colname="col2"> <p>Utilisez la <span class="codeph"> balise de facette </span> guidée pour définir une zone dans laquelle toutes les balises de facette se rapportent à une facette spécifique. Cette balise est également une balise booléenne qui masque tout le contenu s’il n’existe aucune valeur dans la facette. Dans ce cas, il n’y a aucun intérêt à extraire les valeurs de facette). </p> <p>Les attributs de hauteur et de largeur sont facultatifs et les dimensions sont spécifiées en pixels (px). Le Créateur de règles visuel (VRB) utilise ces deux attributs et affiche une zone en pointillés sous forme d’espace réservé interactif lorsque la facette est masquée. </p> <p> Lorsque le nom d’affichage se trouve dans la facette et que celle-ci est masquée, le nom est également masqué. Cependant, si le nom se trouve en dehors de la facette, vous ne pouvez masquer le nom que si une <span class="codeph"> balise </span> de zone ou une <span class="codeph"> balise visible par </span> -facette est entourée d’une balise . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-if[-not]-facet-long [gsname="facetname"]&gt;&lt;/guided-if[-not]-facet-long&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cette balise conditionnelle est vraie lorsque le nombre de valeurs de facette dépasse le seuil de longueur défini dans la configuration. Utilisez-la pour afficher une facette sous la forme d’un élément d’interface utilisateur différent (comme une liste tronquée ou une zone de défilement) lorsque la liste est trop longue. </p> <p> <code class="syntax xml"> &lt;guided-facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;select&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-option&nbsp;/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/select&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-long&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>Vous pouvez également utiliser cette condition en dehors du contexte d’un <span class="codeph"> bloc de facettes guidées nommé en référençant une facette spécifique directement à l’aide de l’ </span> attribut gsname <span class="codeph"> </span> . </p> <p> <code class="syntax html"> &lt;guided-if-facet-long&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;very&nbsp;long! 
      &lt;/guided-if-facet-long&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-if[-not]-facet-selected [gsname="facetname"]&gt;&lt;/guided-if[-not]-facet-selected&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cette balise conditionnelle est vraie lorsque l’utilisateur clique au moins une fois sur la facette et qu’une valeur de facette est actuellement sélectionnée. Il est utilisé pour afficher ou masquer les balises HTML ou gs selon qu’une facette a été cliquée ou non. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This&nbsp;facet&nbsp;has&nbsp;been&nbsp;selected.&nbsp;&nbsp;You&nbsp;can&nbsp;no&nbsp;longer&nbsp;refine&nbsp;it. 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-selected&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>Vous pouvez également utiliser cette condition en dehors du contexte d’un <span class="codeph"> bloc de facettes guidées nommé en référençant une facette spécifique directement à l’aide de l’ </span> attribut gsname <span class="codeph"> </span> . </p> <p> <code> &lt;guided-if-facet-selected&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;selected! 
      &lt;/guided-if-facet-selected&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-if[-not]-facet-single [gsname="facetname"]&gt;&lt;/guided-if[-not]-facet-single&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cette balise conditionnelle est vraie lorsqu’il n’existe qu’une seule valeur de facette. Utilisez la balise pour modifier l’affichage de la facette lorsqu’elle n’est pas en mesure d’affiner les résultats. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Facet&nbsp;is&nbsp;not&nbsp;refinable. 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-single&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>Vous pouvez également utiliser cette condition en dehors du contexte d’un <span class="codeph"> bloc de facettes guidées nommé en référençant une facette spécifique directement à l’aide de l’ </span> attribut gsname <span class="codeph"> </span> . </p> <p> <code class="syntax html"> &lt;guided-if-facet-single&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;There&nbsp;is&nbsp;only&nbsp;one&nbsp;value&nbsp;in&nbsp;the&nbsp;category&nbsp;facet! 
      &lt;/guided-if-facet-single&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--Added 7/15/2014--> <span class="codeph"> &lt;guided-if[-not]-facet-multiselect [gsname="facetname"]&gt;&lt;/guided-if[-not]-facet-multiselect&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cette balise conditionnelle est vraie lorsque la facette est à sélection multiple. Utilisez la balise pour modifier l’affichage de la facette à l’intérieur des balises <span class="codeph"> &lt;guided-facet-rail&gt; </span> ou <span class="codeph"> &lt;guided-dynamic-facets&gt; </span> . </p> <p> 

    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;guided-if-facet-multiselect&amp;gt;
    &amp;nbsp;..
    &amp;nbsp;&amp;lt;guided-else-facet-multiselect&amp;gt;
    &amp;nbsp;...
    &amp;nbsp;&amp;lt;/guided-if-facet-multiselect&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;...
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;/guided-facet&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;lt;/guided-facet-rail&amp;gt; &lt;/code> &lt;/p> &lt;/td>
</tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-values [gsname=" <span class="varname"> facetname </span>"]&gt;&lt;/guided-facet-values&gt; </span> </p> </td> 
   <td colname="col2"> <p>Il s’agit de la balise d’itérateur de boucle de valeur de facette. Vous pouvez le définir dans le contexte d’un <span class="codeph"> bloc de facettes guidées nommé, auquel cas vous pouvez omettre le </span> nom de <span class="codeph"> gsname <span class="varname"></span> </span>. Vous pouvez également le définir en dehors de tout <span class="codeph"> bloc de facettes </span> guidées, mais l’ <span class="codeph"> attribut gsname <span class="varname"></span> </span> est nécessaire pour identifier le jeu de valeurs de facettes affiché. </p> <p>Vous pouvez également utiliser cette balise pour afficher les valeurs de facette en dehors du contexte d’un <span class="codeph"> </span> bloc de facettes guidées nommé. Vous référencez directement une facette spécifique à l’aide de l’ <span class="codeph"> attribut <span class="varname"> </span> </span> gsname. </p> <p> <code class="syntax html"> &lt;script&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;registerFacetValues('category',&nbsp;'&lt;guided-facet-values&nbsp;gsname="category"&gt;&lt;guided-facet-value/&gt;,&lt;/guided-facet-values&gt;'); 
      &lt;/script&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-value [escape="html|url|js|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Renvoie la chaîne de la valeur de facette actuelle. </p> <p>Par défaut, la valeur est séquence d’échappement HTML. Vous pouvez utiliser l’option d’échappement pour modifier le mode d’échappement de la valeur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-count/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Génère le nombre de résultats correspondant à la valeur de facette actuelle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-facet-value-link [attr="valeur"]+&gt;&lt;/guided-facet-value-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Crée un lien autour de la chaîne de valeur de facette sur laquelle le visiteur du site doit cliquer. Le chemin est généré automatiquement pour restreindre les résultats en fonction de la valeur de facette actuelle. Il prend en charge le transfert direct de tout attribut à la balise d’ancrage. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&nbsp;class="facetlink"&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-value-link&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> <code> &lt;guided-if-facet-value-selected&gt; 
      &lt;guided-else-facet- 
      value-selected&gt; 
      &lt;/guided-if-facet-value-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>Modifie l’affichage de la valeur de facette lorsqu’elle est actuellement sélectionnée. S'il a déjà été choisi, il n'est plus possible de le lier dans la plupart des cas. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-value-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;b&gt;&lt;guided-facet-value/&gt;&lt;/b&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-value-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt;&nbsp;&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-value-selected&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> 

    &amp;lt;/guided-if[-not]-facet-value-ghost&amp;gt; &lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>Modifie l’affichage de la valeur de facette lorsqu’il s’agit d’une valeur fantôme. Lorsqu’une valeur de facette est une valeur fantôme, elle est généralement affichée en italique pour indiquer que la valeur est absente ou "fantôme". </p> <p>L’extrait de code suivant est un exemple de bloc de facettes : </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-value-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;b&gt;&lt;guided-facet-value&nbsp;/&gt;&nbsp;(&lt;guided-facet-count&nbsp;/&gt;)&lt;/b&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-value-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-value-ghost&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;i&gt;&lt;guided-facet-value&nbsp;/&gt;&nbsp;(0)&lt;/i&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-value-ghost&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&nbsp;class="link"&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt;&nbsp;(&lt;guided-facet-count&nbsp;/&gt;) 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-value-ghost&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-value-selected&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-undo-link gsname=" <span class="varname"> facetname </span>"&gt;&lt;/guided-facet-undo-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Affiche un lien d’annulation pour une facette donnée. S’il existe des facettes à sélection multiple, ce lien désélectionne toutes les valeurs de facette donnée. Donnez un nom à la facette. Si la facette n’est pas actuellement sélectionnée, le lien est le chemin d’accès actif. </p> <p>Voici un exemple d’utilisation de cette balise : </p> <p> <code class="syntax html"> &lt;guided-if-facet-selected&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-undo-link&nbsp;gsname="category"&gt;Undo&nbsp;Category&lt;/guided-facet-undo-link&gt; 
      &lt;/guided-if-facet-selected&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <varname></varname> </p> </td> 
   <td colname="col2"> <p>Cette balise conditionnelle est vraie lorsque le nombre de valeurs de facette dépasse le seuil de longueur défini dans la configuration. Utilisez-la pour afficher une facette en tant qu’élément d’interface utilisateur différent (comme une liste tronquée ou une zone de défilement) lorsque la liste est trop longue. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;div&nbsp;class="long_facet"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;div&nbsp;class="facet"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-long&gt; 
      &nbsp;&lt;/guided-facet&gt; </code> </p> <p>Vous pouvez également utiliser cette condition en dehors du contexte d’un bloc de facettes <span class="codeph"> guidées nommé </span> en référençant une facette spécifique directement à l’aide de l’ <span class="codeph"> attribut <span class="varname"> </span> </span> gsname. </p> <p> <code class="syntax html"> &lt;guided-if-facet-long&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;very&nbsp;long! 
      &lt;/guided-if-facet-long&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-selected [gsname="facetname"]&gt; 
      &lt;guided-else-facet-selected&gt;&lt;/guided-if-facet-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>Cette balise conditionnelle est vraie lorsque l’utilisateur clique au moins une fois sur la facette et qu’une valeur de facette est actuellement sélectionnée. Il peut être utilisé pour afficher ou masquer des balises HTML ou gs selon qu’une facette est cliquée ou non. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This&nbsp;facet&nbsp;has&nbsp;been&nbsp;selected.&nbsp;&nbsp;You&nbsp;can&nbsp;no&nbsp;longer&nbsp;refine&nbsp;it. 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-selected&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>Vous pouvez également utiliser cette condition en dehors du contexte d’un <span class="codeph"> bloc de facettes guidées nommé en référençant une facette spécifique directement à l’aide de l’ </span> attribut gsname <span class="codeph"> </span> . </p> <p> <code class="syntax html"> &lt;guided-if-facet-selected&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;selected! 
      &lt;/guided-if-facet-selected&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> <varname></varname> </p> </td> 
   <td colname="col2"> <p>Cette balise conditionnelle est vraie lorsqu’il n’existe qu’une seule valeur de facette. Il peut être utilisé pour modifier l’affichage de la facette lorsqu’il n’est pas en mesure d’affiner les résultats. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Facet&nbsp;is&nbsp;not&nbsp;refinable. 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-single&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>Vous pouvez également utiliser cette condition en dehors du contexte d’un bloc de facettes <span class="codeph"> guidées nommé </span> en référençant une facette spécifique directement à l’aide de l’ <span class="codeph"> attribut <span class="varname"> </span> </span> gsname. </p> <p> <code class="syntax html"> &lt;guided-if-facet-single&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;There&nbsp;is&nbsp;only&nbsp;one&nbsp;value&nbsp;in&nbsp;the&nbsp;category&nbsp;facet! 
      &lt;/guided-if-facet-single&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> <varname></varname> </p> </td> 
   <td colname="col2"> <p>Cette condition vous permet de vérifier si la facette spécifiée comporte des valeurs. Vous pouvez l’utiliser pour afficher une autre facette au lieu d’une facette vide. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>20 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-total-count gsname=" <span class="varname"> facetname </span>"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Génère le nombre total de résultats qui se trouvent dans la facette donnée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>21 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value gsname=" valeur de facette personnalisée <span class="varname"> associée </span>" [escape="html|url|js|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Renvoie la chaîne d’une valeur associée à la facette. Vous pouvez associer 0 ou plusieurs champs à une facette. Le fait d’avoir des champs associés est rare et pour ce faire, vous devez configurer le modèle de transport. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>22 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;Guided-if-facet-value gsname=" <span class="varname"> valeur de facette personnalisée </span>"/&gt;&lt;guidé-else-facet-value&gt;&lt;/guidé-if-facet-value&gt; </span> </p> </td> 
   <td colname="col2"> <p>Teste si la valeur de facette est associée à une valeur de champ. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>23 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-link [attr=" <span class="varname"> value </span>"]+&gt;&lt;/guided-facet-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Crée un lien autour de la chaîne de valeur de facette sur laquelle le client doit cliquer. Le chemin est généré automatiquement pour restreindre les résultats en fonction de la valeur de facette actuelle. Il prend en charge le transfert direct de tout attribut à la balise d’ancrage. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&nbsp;class="facetlink"&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>24 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-path [escape="html|url|js|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Crée votre propre lien vers une valeur de facette. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-lt/&gt;a&nbsp;href="&lt;guided-facet-value-path/&gt;"&lt;guided-gt/&gt;&lt;guided-facet-value/&gt;&lt;/a&gt; 
      &lt;/guided-facet-values&gt; </code> </p> <p>Par défaut, la valeur est Coupée d’une séquence d’échappement d’URL. Vous pouvez toutefois ajouter un autre calque de codage en spécifiant le mode d’échappement à utiliser au moyen du paramètre d’échappement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>25 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-children&gt;&lt;/guided-facet-value-children&gt; </span> </p> </td> 
   <td colname="col2"> <p>Alors que <span class="codeph"> &lt;guided-facet-values&gt; </span> effectue une itération sur chaque valeur de facette, cette balise effectue une itération sur toutes les valeurs enfants d’une facette imbriquée. Dans cette balise, utilisez les balises de facette standard pour créer des liens, créer des liens d’annulation et afficher les valeurs de facette. Cette balise doit se trouver à l’intérieur de <span class="codeph"> &lt;guided-facet-values&gt; </span> , car elle ne bouge pas imbriquée. </p> <p>Voici un exemple d’utilisation de cette balise : </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&lt;guided-facet-link&nbsp;title='&lt;guided-facet-value&nbsp;/&gt;'&gt;&lt;guided-facet-value&nbsp;/&gt;&nbsp;(&lt;guided-facet-count&nbsp;/&gt;)&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&lt;guided-if-facet-value-has-children&gt; 
      &nbsp;&nbsp;&nbsp;&lt;guided-facet-value-children&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&nbsp;title='&lt;guided-facet-value&nbsp;/&gt;'&gt;&lt;guided-facet-value&nbsp;/&gt;&nbsp;(&lt;guided-facet-count&nbsp;/&gt;)&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&lt;/guided-facet-value-children&gt; 
      &nbsp;&nbsp;&lt;/guided-if-facet-value-has-children&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>26 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-value-has-children&gt; 
      &lt;guided-else-facet- 
      value-has-children&gt; 
      &lt;/guided-if-facet-value-has-children&gt; </code> </p> </td> 
   <td colname="col2"> <p>Vérifie si la valeur de facette actuelle comporte des valeurs enfants. Il est recommandé d’utiliser avant d’utiliser les balises <span class="codeph"> &lt;guided-facet-value-children&gt; </span> . La clause "else" est facultative. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>27 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;guided-else[-not]-facet-value-au-dessus de la longueur-seuil&amp;gt;
    
    &amp;lt;/guided-if[-not]-facet-value-au-dessus de la longueur-seuil&amp;gt; &lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>Détermine si la valeur de facette actuelle dans la boucle facet-values est supérieure au seuil de longueur. Il est généralement utilisé pour afficher uniquement les valeurs inférieures au seuil sur une longue facette (à moins que l’utilisateur ait précédemment sélectionné un lien "Voir plus" affiché sous la facette). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>28 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;guidé-else[-not]-facet-value-equals-length-seuil&amp;gt;
    
    &amp;lt;/guidé-if[-not]-facet-value-equals-length-seuil&amp;gt; &lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>Détermine si la valeur de facette actuelle dans la boucle facet-values est égale au seuil de longueur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>29 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-undo-link&gt;&lt;/guided-facet-value-undo-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Affiche un lien d’annulation pour une valeur de facette sélectionnée donnée. Utilisez-la pour afficher un lien Annuler en regard d’une valeur de facette sélectionnée. Comme ce lien d’annulation annule uniquement cette valeur sélectionnée particulière, il diffère de <span class="codeph"> &lt;guided-facet-undo-link&gt; </span> qui désélectionne toutes les valeurs sélectionnées. </p> <p> <p>Remarque :  Si la facette n’a pas de comportement de sélection multiple, les deux liens d’annulation ont le même comportement. Autrement dit, la facette ne peut avoir qu’une seule valeur sélectionnée. </p> </p> <p>Si la facette n’est pas actuellement sélectionnée, le lien est le chemin d’accès actif. Utilisez cette balise uniquement dans une boucle <span class="codeph"> guidé-facette-values </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>30 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-undo-path/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Créez votre propre lien d’annulation de valeur de facette. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>31 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-undo-path gsname=" <span class="varname"> facetname </span>"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Créez votre propre lien d’annulation de facette. </p> <p> Semblable à la balise <span class="codeph"> &lt;guided-facet-undo-link&gt; </span> , sauf qu’elle vous donne le chemin brut pour créer votre propre lien d’annulation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>32 </p> </td> 
   <td colname="col1"> <p> <varname></varname> </p> </td> 
   <td colname="col2"> <p>Affichage conditionnel du code HTML lorsque la facette donnée a la valeur "value" sélectionnée ou unique. Cet ensemble de balises est souvent utilisé pour afficher une facette en fonction de la valeur sélectionnée dans une autre facette. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>33 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-comportement gsname=" <span class="varname"> facetname </span>"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Déterminez le comportement d’une facette (normal, collant ou à sélection multiple, par exemple). Il est utile pour les clients qui reçoivent des résultats XML et souhaitent modifier dynamiquement la manière dont la facette est affichée en fonction de son comportement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>34 </p> </td> 
   <td colname="col1"> <p> <varname></varname>

    &amp;lt;/guided-if-facet[-not]-visible&amp;gt; &lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>Le contenu encapsulé par cette balise est masqué ou affiché en fonction de l’état de visibilité de la facette. Si une règle de fonctionnement masque ou révèle directement la facette, tout contenu de la facette est masqué ou révélé. Il n’est pas nécessaire que ces balises entourent la facette. </p> <p> Cette balise est couramment utilisée pour masquer le nom d’affichage lorsque le nom se trouve en dehors de la facette. Lorsque vous placez cette balise autour du nom d’affichage, le nom disparaît lorsque la facette est masquée. </p> <p>Cette balise remplace la zone et présente plusieurs des mêmes avantages en termes de performances que l’utilisation de zones. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Chemin de navigation {#section_9B39B71FA6EC49FA8D88AD8A3BA987F7}

Voir [A propos des chemins de navigation](../c-about-design-menu/c-about-breadcrumbs.md#concept_FB8A943C594A4A1593B118141DA61F03).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Baliser </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-breadcrumb [gsname=" <span class="varname"> breadcrumbname </span>"]&gt;&lt;/guided-breadcrumb&gt; </span> </p> </td> 
   <td colname="col2"> <p>Balise de boucle du chemin de navigation. Tout contenu entre les balises d’ouverture et de fermeture est itéré pour chaque numéro de requête de l’état actuel. </p> <p>Si <span class="codeph"> gsname <span class="varname"> </span> </span> est omis, le chemin de navigation nommé "default" est utilisé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-breadcrumb-link [gsname="goto|remove|drop"] [attr="value"]+&gt;&lt;/guided-breadcrumb-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Crée un lien dans le chemin de navigation. Le comportement par défaut est le comportement "goto". Si le lien se comporte différemment, utilisez l’attribut <span class="codeph"> gsname <span class="varname"> </span> </span> facultatif pour spécifier "remove" ou "drop". Tout attribut inclus dans la balise est transmis à la balise d’ancrage résultante. </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&nbsp;gsname="remove"&nbsp;class="bc_link"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-value/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-breadcrumb-value /&gt; </span> </p> </td> 
   <td colname="col2"> <p>La balise value imprime la valeur transformée de l’itération du chemin de navigation actuelle. Il est utilisé uniquement dans le contexte d’un <span class="codeph"> </span> bloc de chemin de navigation guidé. </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-value/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-breadcrumb-label /&gt; </span> </p> </td> 
   <td colname="col2"> <p>La balise d’étiquette génère un libellé pour une valeur de chemin de navigation qui détaille la facette sélectionnée pour générer cet élément de chemin de navigation. Elle est uniquement utilisée dans le contexte d’un <span class="codeph"> </span> bloc de chemin de navigation guidé. </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-label/&gt;:&nbsp;&lt;guided-breadcrumb-value/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to search-eng version, 2/1/2013--> <code> &lt;guided-if-breadcrumb-label&gt; 
      &lt;guided-else- 
      breadcrumb-label&gt; 
      &lt;guided-if-breadcrumb-label /&gt; </code> </p> </td> 
   <td colname="col2"> <p>Cette balise conditionnelle est utilisée pour afficher sous condition le contenu si la valeur actuelle du chemin de navigation comporte une étiquette. Il est utilisé pour afficher uniquement les étiquettes et le contenu associé lorsqu’une étiquette existe réellement. Elle est uniquement utilisée dans le contexte d’un <span class="codeph"> </span> bloc de chemin de navigation guidé. </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-breadcrumb-label&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-label/&gt;: 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-breadcrumb-label&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-value/&gt;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-breadcrumb-path [gsname="goto|remove|drop"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Utilisé pour créer votre propre lien de chemin de navigation. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Menus {#section_1D489ADF041F4351A66E5D5742125CA8}

Voir [A propos des menus](../c-about-design-menu/c-about-menus.md#concept_68123CE5CF4447B59217B5D721424E32).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Baliser </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu gsname="menuname"&gt;&lt;/guided-menu&gt; </span> </p> </td> 
   <td colname="col2"> <p>Il s’agit de la balise d’itérateur de boucle de valeur de menu. Utilisez l'attribut <span class="codeph"> gsname </span> pour identifier le jeu d'éléments de menu qui s'affiche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-link [attr="valeur"]+&gt;&lt;/guided-menu-item-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Donne l'URL pour affiner la recherche actuelle de l'option de menu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-option [attr="valeur"]+ /&gt; </span> </p> </td> 
   <td colname="col2"> <p>En règle générale, un menu s’affiche dans un contrôle de sélection sur un modèle. Cette balise facilite la création du contrôle select, car elle génère le code HTML permettant de générer l’option du contrôle select. </p> <p>Par exemple, le bloc de code suivant : </p> <p> <code class="syntax html"> &lt;select&nbsp;name="sort"&nbsp;onchange="gcGo(this);"&gt; 
      &lt;guided-menu&nbsp;gsname="sort"&gt; 
      &lt;guided-menu-item-option/&gt; 
      &lt;/guided-menu&gt; 
      &lt;/select&gt; </code> </p> <p>Peut générer du code HTML comme suit : </p> <p> <code class="syntax html"> &lt;select&nbsp;name="sort"&nbsp;onchange="gcGo(this);"&gt; 
      &nbsp;&nbsp;&lt;option&nbsp;value="?sort=relevance;sp_sfvl_field=product-type|category|size;"&nbsp;selected="selected"&gt;Sort&nbsp;by&nbsp;Relevance&lt;/option&gt; 
      &nbsp;&nbsp;&lt;option&nbsp;value="?sort=avail-code;sp_sfvl_field=product-type|category|size;"&gt;Sort&nbsp;by&nbsp;Availability&lt;/option&gt; 
      &nbsp;&nbsp;&lt;option&nbsp;value="?sort=price;sp_sfvl_field=product-type|category|size;"&gt;Sort&nbsp;by&nbsp;Price&lt;/option&gt; 
      &lt;/select&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-value /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Renvoie la chaîne de la valeur associée au menu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-label /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Renvoie la chaîne de l’étiquette associée au menu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-path /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Renvoie la chaîne de chemin. Utilisez la balise si vous souhaitez ajouter un paramètre au chemin et créer un lien personnalisé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if-menu-item-selected&gt; 
      &lt;guided-else-menu- 
      item-selected&gt; 
      &lt;/guided-if-menu-item-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>Renvoie 1 ou 0 pour indiquer si l’option de menu active est sélectionnée. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Pagenav {#section_2EE397635C514BBC8D668278EA314F35}

Les balises de navigation de la page peuvent être utilisées pour créer un ensemble de liens permettant à un utilisateur de parcourir les résultats de la recherche.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Baliser </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;pages guidées&gt;&lt;/pages guidées&gt; </span> </p> </td> 
   <td colname="col2"> <p>Balise de boucle pour la navigation dans la page. Tout contenu entre les balises d’ouverture et de fermeture est itéré pour chaque page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-page-link [attr="value"]+&gt;&lt;/guided-page-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Crée un lien dans le volet de navigation de la page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-page-link gsname="first|prev|next|last|viewall|viewpages" [attr="value"]+&gt;&lt;/guided-page-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Crée un lien vers la première, la précédente, la suivante ou la dernière page. Il peut également créer un lien pour afficher toutes les pages d’une page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-page-number /&gt; </span> </p> </td> 
   <td colname="col2"> <p> Renvoie une chaîne avec le numéro de page actuel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if-page-selected&gt; 
      &lt;guided-else-page- 
      selected&gt; 
      &lt;/guided-if-page-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>Cet ensemble de balises conditionnelles est true si la page sur laquelle l’itération est effectuée est sélectionnée. Il est généralement utilisé pour afficher différemment le numéro de page dans le contrôle de navigation par page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-prev&gt; 
      &lt;guided-else-page- 
      prev&gt; 
      &lt;/guided-if[-not]-page-prev&gt; </code> </p> </td> 
   <td colname="col2"> <p> Cet ensemble de balises conditionnelles est vrai si la page active comporte une page précédente. Il est généralement utilisé pour afficher un lien précédent dans la navigation de la page, lorsqu’il est logique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-next&gt; 
      &lt;guided-else-page- 
      next&gt; 
      &lt;/guided-if[-not]-page-next&gt; </code> </p> </td> 
   <td colname="col2"> <p> Cet ensemble de balises conditionnelles est vrai si la page active comporte une page suivante. Il est généralement utilisé pour afficher un lien précédent dans la navigation de la page, lorsqu’il est logique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-viewall&gt; 
      &lt;guided-else-page- 
      viewall&gt; 
      &lt;/guided-if[-not]-page-viewall&gt; </code> </p> </td> 
   <td colname="col2"> <p> Lorsqu'une recherche renvoie un jeu de résultats volumineux, vous ne souhaiterez peut-être pas offrir la possibilité d'afficher tous les résultats. Par conséquent, vous pouvez utiliser cet ensemble de balises conditionnelles pour déterminer quand afficher le lien Afficher tout. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-viewpages&gt; 
      &lt;guided-else-page- 
      viewpages&gt; 
      &lt;/guided-if[-not]-page-viewpages&gt; </code> </p> </td> 
   <td colname="col2"> <p>Vous pouvez utiliser cet ensemble de balises conditionnelles pour déterminer quand afficher le lien Afficher les pages. Il est généralement utilisé pour permettre à un client d’afficher certaines pages. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> 

    &amp;lt;guided-else-page-link&amp;gt;
    &amp;lt;/guided-if[-not]-page-link&amp;gt; &lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>Teste si la navigation de la page comporte une première page, une page précédente, une page suivante, etc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-page-total /&gt; </span> </p> </td> 
   <td colname="col2"> <p> Renvoie une chaîne avec le nombre total de pages des résultats de la recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-pagination gsname= 
      "pagination_name"&gt;&lt;/guided-pagination&gt; </code> </p> </td> 
   <td colname="col2"> <p>Utilisez la <span class="codeph"> balise de pagination </span> guidée pour définir une zone dans laquelle toutes les balises de pagination se rapportent à un paramètre de pagination spécifique si vous avez défini quelques paramètres de navigation de page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> 

    next|last|viewall|viewpages]/&amp;gt; &lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>Crée votre propre lien dans le volet de navigation de la page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-page-high-eq-last&gt; 
      &lt;guided-else-page- 
      high-eq-last&gt; 
      &lt;/guided-if-page-high-eq-last&gt; </code> </p> </td> 
   <td colname="col2"> <p>Teste si la page la plus élevée dans la navigation de la page est égale au nombre total de pages. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-page-low-eq-first&gt; 
      &lt;guided-else-page-low-eq-first&gt; &lt;/guided-if-page-low-eq-first&gt; </code> </p> </td> 
   <td colname="col2"> <p>Teste si la page la plus basse du volet de navigation de la page est égale à celle-ci. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-page-is-multipage&gt; &lt;guided-else-page-is-multipage&gt; &lt;/guided-if-page-is-multipage&gt; </span> </p> </td> 
   <td colname="col2"> <p>Teste s’il existe une page de résultats unique ou plusieurs pages de résultats. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Recherches récentes {#section_8CD907521F584257B475595B01A5964B}

Vous pouvez utiliser des balises de recherche récentes pour créer un ensemble de liens permettant à un utilisateur d’exécuter rapidement une recherche précédente, comme dans l’exemple suivant :

```
<guided-if-recent-searches> 
    <span>Recent Searches</span><br/> 
    <guided-recent-searches> 
        <guided-recent-searches-link><guided-recent-searches-value></guided-recent-searches-link><br/> 
    </guided-recent-searches> 
    <guided-recent-searches-clear-link>Clear Recent Searches</guided-recent-searches-clear-link> 
</guided-if-recent-searches>
```

Voir [Configuration des recherches](../c-about-design-menu/t-configuring-recent-searches.md#task_E9E8ACA04C90484F8AFD5262167B2562)récentes.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Baliser </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-récent-searches&gt;&lt;/guided-récent-searches&gt; </span> </p> </td> 
   <td colname="col2"> <p>Balise de boucle pour les recherches récentes. Tout contenu entre les balises d’ouverture et de fermeture est itéré pour chaque page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-recent-searches-link [attr="value"]+&gt; 
      &lt;/guided-recent-searches-link&gt; </code> </p> </td> 
   <td colname="col2"> <p>Permet de créer un lien vers une recherche récente. Il prend en charge le transfert direct des attributs HTML vers la balise d’ancrage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-récent-searches-path/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Vous permet de saisir le chemin d’URL relatif pour une recherche récente, dans une <span class="codeph"> boucle de recherche récente </span> guidée. En règle générale, vous utiliseriez le lien <span class="codeph"> guidé-récent-recherche-lien </span>. Cependant, si vous souhaitez créer votre propre lien, vous pouvez utiliser cette balise. Voici un exemple : </p> <p> <code class="syntax html"> &lt;guided-lt/&gt;a&amp;nbsp;href="&lt;guided_recent_searches_path&gt;"&gt;&lt;guided-recent-searches-value&gt;&lt;/a&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-récent-searches-value&gt; </span> </p> </td> 
   <td colname="col2"> <p>Permet de saisir le terme de requête associé à une recherche récente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-récent-searches-clear-link [attr="valeur"]+&gt;&lt;/guided-new-searches-clear-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Vous permet d’offrir à vos clients la possibilité d’effacer les recherches enregistrées récemment. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-récent-searches-clear-path/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Renvoie le chemin utilisé par <span class="codeph"> &lt;guided-new-searches-clear-link&gt; </span> afin que vous puissiez créer votre propre lien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;/guided-if-récent-searches&amp;gt; &lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>Vous permet d’afficher les recherches récentes lorsqu’un client a effectué une recherche récente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voulez-vous dire {#section_C1EB3B9D8E1242798A6E04609D1E3543}

Vous pouvez utiliser les balises Voulez-vous dire pour créer un ensemble de liens vers des suggestions lorsqu’une recherche ne renvoie aucun résultat et que le terme de recherche ne figure pas dans le dictionnaire du compte. Voici un exemple d’utilisation des balises Did You Mean :

```
<guided-if-suggestions> 
    <span>Did You Mean?</span><br/> 
    <guided-suggestions> 
        <guided-suggestion-link><guided-suggestion/></guided-suggestion-link><br/> 
    </guided-suggestions> 
</guided-if-suggestions>
```

Voir [A propos de Vouliez-vous dire](../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E)

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Baliser </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matches search-eng version, 2/1/2013--> <span class="codeph"> &lt;Guided-Suggestions&gt;&lt;/Guided-Suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>Il s’agit de la balise de boucle permettant de parcourir les suggestions en boucle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matches search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-suggestion-link [attr="value"]+&gt;&lt;/guided-suggestion-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Crée un lien vers la suggestion donnée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Newly added from search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-suggestion-value /&gt; </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-suggestions&gt;&lt;guided-else[-not]- 
      suggestions&gt;&lt;/guided-if[-not]-suggestions&gt; </code> </p> </td> 
   <td colname="col2"> <p>Vous permet de tester s’il existe des suggestions. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-suggestion-path/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Renvoie la chaîne de chemin vers la suggestion. Vous pouvez l’utiliser pour créer votre propre balise d’ancrage. En règle générale, <span class="codeph"> le lien-suggestion-guidé </span> est utilisé à la place. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-suggestion/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Une suggestion. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-suggestion-result-count/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Nombre de résultats pour la suggestion. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-suggestion-autosearch&gt; 
      &lt;guided-else[-not]-suggestion-autosearch&gt; 
      &lt;/guided-if[-not]-suggestion-autosearch&gt; </code> </p> </td> 
   <td colname="col2"> <p>Permet de tester si la recherche automatique par suggestion sur zéro résultat a été effectuée, au cas où cette fonction serait activée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-suggestion-original-query/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Renvoie la requête d’origine si une recherche automatique a été effectuée. </p> <p>Exemple d’utilisation : </p> <p> <code class="syntax html"> &lt;guided-if-suggestion-autosearch&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;Search&nbsp;for&nbsp;&lt;guided-query-param&nbsp;gsname="q"&nbsp;/&gt;&nbsp;instead&nbsp;of&nbsp;&lt;guided-suggestion-original-query&nbsp;/&gt; 
      &lt;/guided-if-suggestion-autosearch&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-suggestion-low-results&gt; 
      &lt;guided-else[-not]-suggestion-low-results&gt; 
      &lt;/guided-if[-not]-suggestion-low-results&gt; </code> </p> </td> 
   <td colname="col2"> <p>Cette condition est vraie si des suggestions sont faites en raison d’un faible nombre de résultats, au cas où cette fonctionnalité serait activée. </p> <p>Voici un exemple d’utilisation de cette balise : </p> <p> <code class="syntax html"> &lt;guided-if-suggestion-low-results&gt; 
      &nbsp;&nbsp;&nbsp;You&nbsp;have&nbsp;a&nbsp;low&nbsp;result&nbsp;count&nbsp;for&nbsp;&lt;guided-query-param&nbsp;gsname="q"&nbsp;/&gt;. 
      &nbsp;&nbsp;&nbsp;Did&nbsp;you&nbsp;mean:&nbsp;&lt;guided-suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestion-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestion&nbsp;/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-suggestion-link&gt;&lt;guided-if-not-last&gt;,&nbsp;&lt;/guided-if-not-last&gt; 
      &nbsp;&nbsp;&nbsp;&lt;/guided-suggestions&gt; 
      &lt;/guided-if-suggestion-low-results&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Remplissage automatique {#section_897316BEE1454E839A56B565CA4AF018}

Les balises suivantes peuvent être utilisées pour ajouter la saisie automatique à votre formulaire de recherche. Les balises head-content et form-content sont requises pour que la saisie automatique fonctionne correctement. Il est recommandé d’utiliser les balises plutôt que de coder en dur le code JavaScript et le code CSS à saisie automatique dans le modèle de présentation. La raison en est que les balises permettent à vos modèles de sélectionner de nouveaux ID de cache d’échec chaque fois que vous modifiez vos paramètres de saisie automatique sans avoir à mettre à jour manuellement votre modèle.

Voir [A propos du remplissage](../c-about-auto-complete.md#concept_093A9CD754864BA79B456FE4BEB64578)automatique.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Baliser </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-autocomplete&gt; &lt;guided-else-autocomplete&gt; &lt;/guided-if-autocomplete&gt; </span> </p> </td> 
   <td colname="col2"> <p>Détecte si la fonction de saisie automatique est activée. Vous pouvez utiliser les balises pour sélectionner éventuellement le contenu de l’en-tête et du formulaire requis pour la saisie automatique. Cela vous permet d’activer ou de désactiver la fonction et de ne pas avoir à modifier les modèles de présentation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-ac-css/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Utilisé dans la section head du modèle de présentation et remplacé par le script CSS approprié pour la saisie automatique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-ac-form-content/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Utilisé dans le formulaire de recherche (entre les balises <span class="codeph"> &lt;form&gt; </span> et <span class="codeph"> &lt;/form&gt; </span> ) du modèle de présentation au lieu de coder en dur les balises de saisie automatique dans le formulaire. Les balises sont remplacées par le code HTML approprié requis pour que la saisie automatique fonctionne. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-ac-javascript/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Génère les liens vers le code JavaScript de saisie semi-automatique. Pour de meilleures performances, il est recommandé de placer cette balise près du bas de la page avant la balise de fermeture "body". </p> </td> 
  </tr> 
 </tbody> 
</table>

## Store {#section_A33E25DB5E67404A823BD9618665B773}

Utilisez les balises suivantes pour tester et afficher la boutique dans laquelle se trouve actuellement un utilisateur.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Baliser </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-store/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Génère le magasin actuel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-store-defined&gt; &lt;guided-else-store-defined&gt; &lt;/guided-if-store-defined&gt; </span> </p> </td> 
   <td colname="col2"> <p>Détecte si l’utilisateur se trouve dans un magasin. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-store gsname="store"&gt; &lt;guided-else-store&gt; &lt;/guided-if-store&gt; </span> </p> </td> 
   <td colname="col2"> <p>Détecte si l’utilisateur se trouve dans le magasin spécifié par le <span class="codeph"> paramètre gsname </span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Zones {#section_B9B3179E000C42D492E1541F2FE44CB5}

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Baliser </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;Guided-zone gsname="zone area" [search="recherche associée"] [facet="facette associée"] [width="xx" height="yy"]&gt; </span> </p> </td> 
   <td colname="col2"> <p>Vous pouvez placer n’importe quel contenu dans des balises de zone pour créer une zone en dehors de cette zone. Vous pouvez ainsi utiliser des règles de fonctionnement pour afficher la zone selon vos besoins. Par défaut, les zones sont toujours affichées. Vous pouvez utiliser les paramètres facultatifs de recherche et de facette pour indiquer la recherche ou la facette associée à la zone. Cette fonctionnalité permet au logiciel de sauter les recherches ou les facettes lorsqu’une zone est masquée, améliorant ainsi les performances en temps de recherche. Les attributs de hauteur et de largeur sont facultatifs et sont utilisés pour configurer l’affichage de l’espace réservé dans le Créateur de règles visuel lorsqu’une zone est supprimée. </p> <p> Dans la mesure du possible, utilisez la <span class="codeph"> </span> balise guidé-if-facet[-not]-visible au lieu de la zone. Il simplifie le modèle de présentation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-zone gsname="zone"&gt; &lt;guided-else-zone&gt; &lt;/guided-if-zone&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cet ensemble de balises permet de tester si une zone est actuellement affichée. Il est utile lorsque vous avez du contenu ailleurs sur la page que vous souhaitez afficher uniquement lorsque la zone est affichée. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Indicateurs de boucle {#section_387322CA0AA843A2ACF2795C328673E9}

Vous pouvez utiliser chacun des indicateurs de boucle suivants dans l’un de ces blocs de boucle :

* guidé-résultats
* valeurs de facette guidée
* chemin de navigation guidé
* guidé-menu-éléments
* pages guidées

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Baliser </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-first&gt;&lt;guided-else[-not]-first&gt; 
      &lt;/guided-if[-not]-first&gt; </code> </p> </td> 
   <td colname="col2"> <p>Cette condition est vraie lorsque l’itération actuelle est la première itération de la boucle. Cela ne signifie pas nécessairement le premier résultat ou la première page, mais la première. Si le visiteur du site se trouve sur la page 2 d’un jeu de résultats de 10 par page, la première itération est le résultat 11. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-last&gt;&lt;guided-else[-not]-last&gt; 
      &lt;/guided-if[-not]-last&gt; </code> </p> </td> 
   <td colname="col2"> <p>Cette condition est vraie lorsque l’itération actuelle est la dernière itération de la boucle. Cela ne signifie pas nécessairement le dernier résultat ou la dernière page, mais le dernier dans le contexte actuel (page). Si le visiteur du site se trouve sur la page 1 d’un jeu de résultats qui contient 200 résultats, mais qui ne contient que 10 résultats par page, la dernière itération est le résultat 10 au lieu du résultat 200. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-odd&gt;&lt;guided-else[-not]-odd&gt; 
      &lt;/guided-if[-not]-odd&gt; </code> </p> </td> 
   <td colname="col2"> <p>Cette condition est vraie lorsque l’itération actuelle est une itération impaire de la boucle (par rapport à une itération paire). Cela s’avère utile pour afficher des couleurs de rangées variables. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-even&gt;&lt;guided-else[-not]-even&gt; 
      &lt;/guided-if[-not]-even&gt; </code> </p> </td> 
   <td colname="col2"> <p>Cette condition est vraie lorsque l’itération actuelle est une itération paire de la boucle (par rapport à une itération impaire). Cela s’avère utile pour afficher des couleurs de rangées variables. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-alt&gt;&lt;guided-else[-not]-alt&gt; 
      &lt;/guided-if[-not]-alt&gt; </code> </p> </td> 
   <td colname="col2"> <p>Cette condition est vraie lorsque l’itération actuelle est une itération paire de la boucle. Cela s’avère utile pour afficher des couleurs de rangées variables. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-inner&gt;&lt;guided-else[-not]-inner&gt; 
      &lt;/guided-if[-not]-inner&gt; </code> </p> </td> 
   <td colname="col2"> <p>Inclut le texte entre eux si l’itération actuelle n’est ni la première ni la dernière. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-outer&gt;&lt;guided-else[-not]-outer&gt; 
      &lt;/guided-if[-not]-outer&gt; </code> </p> </td> 
   <td colname="col2"> <p>Inclut le texte entre eux si l’itération actuelle est la première ou la dernière. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-loop-index&gt; </span> </p> </td> 
   <td colname="col2"> <p>Entier (commençant par 0) dont la valeur est incrémentée pour chaque itération de la boucle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-loop-compteur&gt; </span> </p> </td> 
   <td colname="col2"> <p>Entier (commençant par 1) dont la valeur est incrémentée pour chaque itération de la boucle. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Langue diverse {#section_BFE8DC98E26F4D7BB60FEC54D9A5DC6C}

Les balises suivantes sont disponibles pour vous permettre d’effectuer des tâches plus avancées avec votre modèle, comme la création de votre propre mini-facette.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Baliser </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng, 2/1/2013--> <span class="codeph"> &lt;guided-current-path [escape="html|url|js|json|0"] /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Vous donne le chemin actuel utilisé. Il est généralement utilisé pour créer un lien qui ajoute un nouveau paramètre à la recherche existante. Par défaut, le chemin d’accès est une séquence d’échappement d’URL. Vous pouvez spécifier le mode d’échappement à utiliser au moyen du paramètre d’échappement. </p> <p>Exemple : </p> <p> <code class="syntax html"> &lt;a&nbsp;href="&lt;guided-current-path&nbsp;/&gt;&amp;lang=fr"&gt; 
      French&nbsp;Version </code> </p> <p>Dans cet exemple, une règle de traitement de recherche utilise lang pour sélectionner la version française. </p> <p>Le chemin actuel comporte toujours au moins un paramètre de requête. S’il n’existe aucun autre paramètre de requête, il est défini sur <span class="codeph"> q=* </span> ce qui facilite l’ajout de paramètres supplémentaires. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> Chemin de base </span> </p> </td> 
   <td colname="col2"> <p> Si vous souhaitez créer un lien à l'aide du chemin de base, utilisez <span class="codeph"> / </span> au début de votre <span class="codeph"> href </span> et ajoutez des paramètres. </p> <p> <code class="syntax html"> &lt;a&nbsp;href="/"&gt;All&nbsp;Products&lt;/a&gt; 
      Would&nbsp;create&nbsp;a&nbsp;link&nbsp;"All&nbsp;Products"&nbsp;to&nbsp;your 
      basepath,&nbsp;for&nbsp;example&nbsp;https://search.mycompany.com/ 
       </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng, 2/1/2013--> <span class="codeph"> &lt;guided-query-param gsname="query_parameter" [escape="html|url"] /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Permet de saisir la valeur existante d’un paramètre de requête figurant sur l’URL. Si votre paramètre n’existe pas, cette balise renvoie une chaîne vide. Si vous ne spécifiez pas d’option d’échappement, la chaîne renvoyée est automatiquement une séquence d’échappement HTML, vous pouvez spécifier une séquence d’échappement HTML ou URL. </p> <p>Exemple : </p> <p> 

    &amp;lt;guided-query-param&amp;nbsp;gsname=&quot;q&quot;&amp;nbsp;/&amp;gt;
    donnees&amp;nbsp;you&amp;nbsp;the&amp;nbsp;value&amp;nbsp;pantalon
    
    &amp;lt;guided-query-param&amp;nbsp;gsname&quot; lang&quot;&amp;nbsp;/&amp;gt;
    donne&amp;nbsp;you&amp;nbsp;the&amp;nbsp;value&amp;nbsp;en
    
    &amp;lt;guided-query-param&amp;nbsp;gsname=&quot;test&quot;&amp;nbsp;/&amp;gt;
    don&amp;namp;nbsp bsp;you&amp;nbsp;an&amp;nbsp;empty&amp;nbsp;string
    &amp;nbsp;
    &amp;nbsp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;nbsp;nbsp;&amp;nbsp;nbsp; &lt;/code> &lt;/p> &lt;/td>
</tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-query-param-name gsname="param#" offset="offset_number"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>La recherche guidée a la notion d’un numéro de requête, qui est utilisé dans le contrôle de chemin de navigation. <span class="codeph"> guidé-query-param-name </span> permet de définir des paramètres dans le cadre d’un lien du modèle de présentation dans lequel la recherche guidée détermine le numéro de requête correct pour vous. Le <span class="codeph"> nom de fichier </span> contient un "x", que la recherche guidée remplace par le nombre correct. La valeur de décalage peut être comprise entre 0 et 15, où 0 indique que le prochain numéro de requête disponible est utilisé. Une valeur 1 indique que vous souhaitez ajouter 1 à cette valeur, etc. </p> <p>Combiné à un chemin <span class="codeph"> guidé-courant </span>, vous pouvez créer votre propre lien de mini facette ou autoriser un niveau d’exploration supplémentaire. </p> <p>Exemple : </p> <p> <code class="syntax html"> &lt;a&nbsp;href="&lt;guided-current-path 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;&amp;&lt;guided-query-param-name&nbsp;gsname="q#"&nbsp;offset="0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=mens&amp;&lt;guided-query-param-name&nbsp;gsname="x#"&nbsp;offset="0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=category"&nbsp;&gt;Category:Men&lt;/a&gt;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </code> </p> <p> <code class="syntax html"> &lt;a&nbsp;href="&lt;guided-current-path 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;&amp;&lt;guided-query-param-name&nbsp;gsname="sp_q_exact_#"&nbsp;offset="0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=mens&amp;&lt;guided-query-param-name&nbsp;gsname="sp_x_#"&nbsp;offset="0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=category&amp;&lt;guided-query-param-name&nbsp;gsname="sp_q_exact_#"&nbsp;offset="1" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=Jeans&amp;&lt;guided-query-param-name&nbsp;gsname="sp_x_#"&nbsp;offset="1" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=product-type"&nbsp;&gt;Cat:Men&nbsp;-&nbsp;Product:Jeans&lt;/a&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-include gsfile="nom_fichier" /&gt; </span> </p> </td> 
   <td colname="col2"> <p> Vous permet d’inclure d’autres fichiers de modèle. Cela signifie que vous pouvez créer plusieurs modèles à l’aide de sous-modèles sous forme de modules. </p> <p>Dans l’exemple suivant, les <span class="filepath"> chemins de navigation </span> et <span class="filepath"> les fichiers de facettes </span> sont inclus : </p> <p> <code class="syntax html"> &lt;guided-include&nbsp;gsfile='breadcrumbs.tmpl'&nbsp;/&gt; 
      &lt;guided-include&nbsp;gsfile='facets.tmpl'&nbsp;/&gt; </code> </p> <p>Les inclusions dynamiques ne sont pas prises en charge. En d’autres termes, <span class="codeph"> gsfile </span> ne peut pas être une variable. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 1/17/2013--> <span class="codeph"> &lt;guided-search-time&gt; </span> </p> </td> 
   <td colname="col2"> <p> Identifie la durée de la recherche. La valeur de temps de recherche renvoyée est spécifiée en ms. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 1/17/2013--> <span class="codeph"> &lt;guided-fall-through-searches&gt; </span> </p> </td> 
   <td colname="col2"> <p> Renvoie le nombre de recherches de noyaux utilisées pour créer la page des résultats de la recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 1/17/2013--> <span class="codeph"> &lt;guided-if-fall-through-search&gt;&lt;/guided-if-fall-through-search&gt; </span> </p> </td> 
   <td colname="col2"> <p>Teste si le nombre de recherches principales est supérieur à un. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-even&gt;&lt;guided-else[-not]-even&gt; 
      &lt;/guided-if[-not]-even&gt; </code> </p> </td> 
   <td colname="col2"> <p>Cette condition est vraie lorsque l’itération actuelle est une itération paire de la boucle (par rapport à une itération impaire). Cela s’avère utile pour afficher des couleurs de rangées variables. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-alt&gt;&lt;guided-else[-not]-alt&gt; 
      &lt;/guided-if[-not]-alt&gt; </code> </p> </td> 
   <td colname="col2"> <p>Cette condition est vraie lorsque l’itération actuelle est une itération paire de la boucle. Cela s’avère utile pour afficher des couleurs de rangées variables. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-inner&gt;&lt;guided-else[-not]-inner&gt; 
      &lt;/guided-if[-not]-inner&gt; </code> </p> </td> 
   <td colname="col2"> <p>Inclut le texte entre eux si l’itération actuelle n’est ni la première ni la dernière. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-outer&gt;&lt;guided-else[-not]-outer&gt; 
      &lt;/guided-if[-not]-outer&gt; </code> </p> </td> 
   <td colname="col2"> <p>Inclut le texte entre eux si l’itération actuelle est la première ou la dernière. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-first-search&gt;&lt;guided-else-first-search&gt; 
      &lt;/guided-if-first-search&gt; </code> </p> </td> 
   <td colname="col2"> <p>Vous permet de vérifier si vous êtes sur la recherche initiale ou non (la requête était le résultat d'une recherche dans la zone de recherche). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-search-url/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Vous pouvez utiliser cette balise dans votre modèle pour vous empêcher de figer l’action du formulaire de recherche. Il détecte lorsque vous êtes dans l’environnement d’évaluation ou de production et change en conséquence. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-query-param-defined gsname="query_parameter"&gt; &lt;guided-else-query-param-defined&gt; &lt;/guided-if-query-param-defined&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cet ensemble de balises vous permet de tester les paramètres CGI définis dans le chemin de recherche. Vous pouvez tester les valeurs des paramètres uniquement si elles sont définies. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-next-query-number [gsname="offset"] /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Le moteur de recherche guidée qui conduit le modèle a la notion de nombres de requêtes flottants où chaque nouveau lien généré par le moteur utilise le prochain numéro de requête disponible. Cette balise vous permet de saisir le ou les décalages suivants de la requête afin de créer des liens personnalisés qui explorent le jeu de résultats. Le décalage vous permet de décaler dans le numéro de requête suivant. Par exemple, si vous avez sélectionné une facette, le numéro de requête suivant est 2, avec un décalage de 1, le numéro de requête renvoyé est 3. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-custom-var gsname="custom_variable" [escape="html|url|js|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Permet de saisir la valeur existante d’une variable personnalisée définie par vos règles de traitement. Si vous ne spécifiez pas d’option d’échappement, la chaîne renvoyée est automatiquement une séquence d’échappement HTML, vous pouvez spécifier <span class="codeph"> html </span>, <span class="codeph"> url </span>, <span class="codeph"> js </span>ou <span class="codeph"> 0 . </span> Si vous utilisez une règle de traitement pour copier un paramètre CGI entrant dans une variable personnalisée, puis l’afficher ou l’utiliser dans votre modèle avec l’option d’échappement définie sur none ou js, vous pouvez créer une vulnérabilité XSS dans votre recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-custom-var-defined gsname="custom_variable"&gt; &lt;guided-else-custom-var-defined&gt; &lt;/guided-if-custom-var-defined&gt; </span> </p> </td> 
   <td colname="col2"> <p>Active le test si une variable personnalisée est définie dans les règles de traitement (nettoyage des requêtes, traitement avant recherche et post-recherche). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-general-field gsname="nom_recherche" field="nom_champ" [escape="html|url|js|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Permet d’afficher le contenu d’un champ général défini dans le modèle de transport. Si vous ne spécifiez pas d’option d’échappement, la chaîne renvoyée est codée au format que vous avez spécifié dans le modèle de transport pour ce champ. La spécification d’une option d’échappement s’applique au-dessus du format de codage du champ tel que celui de votre modèle de transport. Vous pouvez spécifier <span class="codeph"> html </span>, <span class="codeph"> url </span>, <span class="codeph"> js </span>, <span class="codeph"> json  ou  0 .</span><span class="codeph"></span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>20 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-general-field gsname="nom_recherche" field="nom_champ"&gt; &lt;guidé-else-general-field&gt; &lt;/guidé-if-general-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Active le test si le contenu d’un champ général, tel que défini dans le modèle de transport, existe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>21 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-cookie-value gsname="nom_cookie" [escape="html|url|js|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Vous permet de saisir la valeur d’un cookie, en supposant qu’il soit disponible. Si vous ne spécifiez pas d’option d’échappement, la chaîne renvoyée est automatiquement une séquence d’échappement HTML, vous pouvez spécifier <span class="codeph"> html </span>, <span class="codeph"> url </span>, <span class="codeph"> js </span>, <span class="codeph"> json  ou  0 .</span><span class="codeph"></span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>22 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-cookie gsname="nom_cookie"&gt; &lt;cookie-else&gt; &lt;/guided-if-cookie&gt; </span> </p> </td> 
   <td colname="col2"> <p>Active le test s’il existe un cookie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>23 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-banner gsname="bannière area" [escape="html|url|js|json|0"] [width="xx" height="yy"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Génère la bannière pour une zone donnée. Les attributs facultatifs de largeur et de hauteur sont utilisés dans le Créateur de règles visuel pour permettre l’affichage d’un espace réservé significatif permettant aux utilisateurs de sélectionner une bannière. Par défaut, les bannières ne sont pas ignorées. Vous souhaitez plutôt injecter du code HTML dans le modèle de présentation. Cependant, si vous créez un modèle JSON, pensez à utiliser l’option d’échappement js. </p> <p>Exemple : </p> <p> <code class="syntax html"> &lt;guided-banner&nbsp;gsname="top"&nbsp;width="400px" 
      &nbsp;height="50px"/&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>24 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-banner-set gsname="bannière-zone"&gt; &lt;guided-else-banner-set&gt; &lt;/guided-if-banner-set&gt; </span> </p> </td> 
   <td colname="col2"> <p>Active le test si une zone de bannière est définie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>25 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-simulator-mode&gt; &lt;guided-else-simulator-mode&gt; &lt;/guided-if-simulator-mode&gt; </span> </p> </td> 
   <td colname="col2"> <p>Permet de détecter le moment où vous affichez votre recherche dans le simulateur ou le créateur de règles visuel. Il est normalement utilisé pour afficher des informations de débogage supplémentaires pour vous. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>26 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-tnt-business-rule&gt; &lt;guided-else-tnt-business-rule&gt; &lt;/guided-if-tnt-business-rule&gt; </span> </p> </td> 
   <td colname="col2"> <p>Permet de détecter si vous avez des règles de fonctionnement référençant une <span class="keyword"> campagne </span> Adobe Target. Il est généralement utilisé dans le cadre de l’intégration à <span class="keyword"> Adobe Target </span> afin d’empêcher l’accès aux <span class="keyword"> serveurs Target </span> lorsque cela n’est pas nécessaire. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>27 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-redirect/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Par défaut, les redirections sont exécutées automatiquement. Cependant, si vous avez configuré la recherche/marchandisage de site pour renvoyer une réponse XML ou JSON à votre application Web, vous pouvez soit analyser la réponse 302/301 dans votre application Web, soit vous faire passer la redirection dans le jeu de résultats. Si vous transmettez la redirection dans le cadre du jeu de résultats, cette balise peut être utilisée dans le modèle pour générer l’emplacement de redirection. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>28 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-redirect&gt; &lt;guided-else-redirect&gt; &lt;/guided-if-redirect&gt; </span> </p> </td> 
   <td colname="col2"> <p>Lorsque vous avez configuré la recherche/marchandisage du site pour renvoyer des redirections dans le jeu de résultats, cet ensemble de balises peut être utilisé pour déterminer s’il existe une redirection vers la sortie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>29 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-lt/&gt; &lt;guided-gt/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cet ensemble de balises vous permet d’incorporer des balises de modèle guidées dans des attributs HTML. </p> <p>Exemple : </p> <p> <code class="syntax html"> &lt;guided-lt/&gt;div&nbsp;&lt;guided-if-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;style="height:&nbsp;125px;&nbsp;overflow: 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;auto;"&lt;/guided-if-facet-long&gt;&lt;guided-gt/&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Balises de modèle de transport {#reference_227D199F5A7248049BE1D405C0584751}

Les modèles de transport sont des modèles XML qui transmettent les données de la recherche principale à la couche de présentation Recherche guidée.

<!-- 

r_transport_template_tags.xml

 -->

Dans la couche de présentation, vous pouvez disposer d’un modèle de présentation unique qui présente les résultats de plusieurs recherches. Chaque recherche peut utiliser le même modèle de transport ou un modèle de transport personnalisé pour transmettre les données à la couche de présentation.

Le modèle de transport étant uniquement utilisé pour transmettre des données à la couche de présentation, il ne comporte aucun code HTML qui se préoccupe de l’affichage des résultats de la recherche. Le modèle de transport utilise des balises XML de modèle de transport pour transmettre les résultats de la recherche afin de renseigner les composants de recherche guidée, tels que les facettes, les chemins de navigation et les menus. Dans ces balises, les balises de modèle de recherche standard sont utilisées pour afficher les valeurs réelles.

Voir [Modification d’une présentation ou d’un modèle](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)de transport.

Voir [Rechercher des balises](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)de modèle.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Balise de modèle de transport </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-xml&gt;&lt;/guided-xml&gt; </span> </p> </td> 
   <td colname="col2"> <p>Balises XML racine utilisées par la couche de présentation pour détecter ce qui est analysé à partir du modèle de transport. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;general&gt;&lt;/general&gt; </span> </p> </td> 
   <td colname="col2"> <p>Les balises entourent les balises de modèle de recherche qui fournissent des données de résumé basées sur le jeu de résultats. En règle générale, ces balises contiennent des balises de recherche pour le nombre total de résultats, le résultat inférieur et le résultat supérieur. Vous pouvez définir un nombre illimité de champs globaux supplémentaires à l’aide de la balise <span class="codeph"> general-field </span> , comme dans l’exemple suivant : </p> <p> <code class="syntax html"> &lt;general&gt; 
      &nbsp;&nbsp;&lt;total&gt;&lt;search-total&nbsp;/&gt;&lt;/total&gt; 
      &nbsp;&nbsp;&lt;lower&gt;&lt;search-lower&nbsp;/&gt;&lt;/lower&gt; 
      &nbsp;&nbsp;&lt;upper&gt;&lt;search-upper&nbsp;/&gt;&lt;/upper&gt; 
      &nbsp;&nbsp;&lt;general-field&nbsp;name="my_custom_field"&gt;Some&nbsp;global&nbsp;content&lt;/general-field&gt; 
      &lt;/general&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;results&gt;&lt;/results&gt; </span> </p> </td> 
   <td colname="col2"> <p>Les balises sont entourées des résultats de la recherche, de sorte que la recherche guidée sache où les rechercher. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;result&gt;&lt;/result&gt; </span> </p> </td> 
   <td colname="col2"> <p>Les balises sont entourées de chaque résultat de recherche, de sorte que la recherche guidée identifie où commence et se termine le contenu d’un seul résultat de recherche, comme dans l’exemple suivant : </p> <code class="syntax html"> &lt;results&gt; 
     &nbsp;&nbsp;&lt;search-results&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-cdata&gt;&lt;search-url&nbsp;length="500"&nbsp;/&gt;&lt;/search-cdata&gt;&lt;/loc&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
     &nbsp;&nbsp;&lt;/search-results&gt; 
     &lt;/results&gt; </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;attribute-table name="nom_table"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Permet de parcourir chaque élément d’une liste à plusieurs valeurs en boucle pour obtenir un seul résultat. N’utilisez cette balise que dans un résultat. Son objectif est de vous permettre d’effectuer une itération sur les attributs appartenant à un champ de résultat, comme dans l’exemple suivant : </p> <code class="syntax html"> &lt;results&gt; 
     &nbsp;&nbsp;&lt;search-results&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-url&nbsp;/&gt;&lt;/loc&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;title&gt;&lt;search-title&nbsp;/&gt;&lt;/title&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;attribute-table&nbsp;name="downloads"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;field&nbsp;name="download_title"&gt;&lt;search-display-field&nbsp;name="download_title"&nbsp;/&gt;&lt;/field&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;field&nbsp;name="download_link"&nbsp;delimiter="|"&gt;&lt;search-display-field&nbsp;name="download_link"&nbsp;/&gt;&lt;/field&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/attribute-table&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
     &nbsp;&nbsp;&lt;/search-results&gt; 
     &lt;/results&gt; </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facettes&gt;&lt;/facettes&gt; </span> </p> </td> 
   <td colname="col2"> <p>Transmet les résultats qui renseignent les facettes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <!--NEW 2/27/2014--> <span class="codeph"> &lt;facette dynamique&gt;&lt;/facette dynamique&gt; </span> </p> </td> 
   <td colname="col2"> <p> Vous pouvez désigner une facette comme une facette dynamique et comme membre d’un rail de facettes. Toutefois, leur traitement est indépendant par rapport aux balises de modèle de présentation associées. </p> <p>En d’autres termes, l’imbrication d’un contexte de boucle de rail de facettes dans un contexte de boucle de facettes dynamique, ou vice versa, n’est pas autorisée. </p> <p>Pour les facettes dynamiques et échouées, seules les facettes dynamiques renvoyées pour une recherche donnée sont visibles dans le contexte de boucle du rail de facettes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facet name="name"&gt;&lt;/facet&gt; </span> </p> </td> 
   <td colname="col2"> <p> Chaque facette possède ses propres balises de facette où le paramètre name correspond au nom de la facette. Les balises de recherche sont utilisées dans les balises de facette pour les valeurs de facette, comme dans l’exemple suivant : </p> <code class="syntax html"> &lt;facets&gt; 
     &nbsp;&nbsp;&lt;facet&nbsp;name="brand"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
     &nbsp;&nbsp;&lt;/facet&gt; 
     &nbsp;&nbsp;&lt;facet&nbsp;name="category"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
     &nbsp;&nbsp;&lt;/facet&gt; 
     &lt;/facets&gt; </code> <p> Les comptes utilisant des facettes en pointillés peuvent utiliser la balise dynamique et la balise display-names. Ces deux balises facilitent le mappage entre les facettes en pointillés et les facettes réelles lors de la création de règles de fonctionnement. </p> <code class="syntax html"> &lt;facets&gt; 
     &nbsp;&nbsp;&lt;facet&nbsp;name="facet_values01"&gt; 
     &nbsp;&lt;dynamic&gt;1&lt;/dynamic&gt; 
     &nbsp;&lt;display-names&gt;&lt;search-field-value-list&nbsp;name="facet_names01"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/display-names&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="facet_values01"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="facet_values01"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
     &nbsp;&nbsp;&lt;/facet&gt; </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field separator=","&gt; </span> </p> </td> 
   <td colname="col2"> <p>L’attribut <span class="codeph"> Separator </span> permet de modifier le délimiteur utilisé lors de la sortie des données de champ de recherche-affichage-de-recherche pour les listes. La valeur par défaut est une virgule. </p> <p>En règle générale, le délimiteur que vous utilisez doit être quelque chose qui n’apparaît pas facilement dans le contenu du champ. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;suggestions&gt;&lt;/suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p> Encapsulez vos suggestions Voulez-vous dire avec des balises afin que la recherche guidée identifie les noeuds XML qui contiennent des suggestions. </p> <p>Voir <a href="../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E" type="concept" format="dita" scope="local">A propos de Vouliez-vous dire</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;suggestion&gt;&lt;/suggestion&gt; </span> </p> </td> 
   <td colname="col2"> <p>Encapsulez chaque suggestion Voulez-vous dire avec des balises, comme dans l’exemple suivant : </p> <code class="syntax html"> &lt;search-if-suggestions&gt; 
     &nbsp;&nbsp;&lt;suggestions&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;search-suggestions&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;suggestion&gt;&lt;search-suggestion-text&nbsp;/&gt;&lt;/suggestion&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-suggestions&gt; 
     &nbsp;&nbsp;&lt;/suggestions&gt; 
     &lt;/search-if-suggestions&gt; </code> <p>Voir <a href="../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E" type="concept" format="dita" scope="local">A propos de Vouliez-vous dire</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Rechercher des balises de modèle {#reference_F7AA3FF602314E42842BBC740D2CA1A4}

Un modèle de recherche est un fichier HTML qui comprend des balises de modèle définies par la recherche sur le site/le marchandisage. Ces balises indiquent le format des résultats de la recherche. La référence suivante contient une brève description de chaque balise de modèle de recherche et de ses attributs.

<!-- 

r_search_template_tags.xml

 -->

>[!NOTE]
>
>Utilisez uniquement des balises de modèle de recherche dans les fichiers de modèle de transport (.tpl).

Vous pouvez sélectionner l’un des groupes de balises de modèle de recherche et le matériel de référence suivants.

Les balises valides uniquement dans la boucle de résultats sont les suivantes :

* [A propos des balises de boucle Résultats](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)
* [Balises de chaîne de boucle de résultats](../c-appendices/c-templates.md#section_80D68334E8D04A33937A6E58ABAAA320)
* [Balises conditionnelles de boucle de résultats](../c-appendices/c-templates.md#section_35C367969E384A06A9865E388F1F9360)
* [Balises de lien d’ancrage de boucle de résultats](../c-appendices/c-templates.md#section_C5FAEF520E9E42ADAD1F90651922AA02)
* [Balises conditionnelles de position de boucle](../c-appendices/c-templates.md#section_E0C29DDA09E043C9A396F36334F05EBB)

Les balises valides dans tout le modèle sont les suivantes :

* [Balises de liste de valeurs de champ](../c-appendices/c-templates.md#section_D3298B5F976447DBA0032B883DCC91B1)
* [Balises de boucle de liste de valeurs de champ](../c-appendices/c-templates.md#section_0717FA09F0FC449CB916883B0500A60E)
* [Suggérer des balises](../c-appendices/c-templates.md#section_C28EB8B4F7DC4E278A0F143BCFEEB1AC)
* [Balises de chaîne de modèle](../c-appendices/c-templates.md#section_67E3D529661F4F03A1FF469D9D658CAF)
* [Balises de lien d’ancrage de modèle](../c-appendices/c-templates.md#section_3A51D27616C541E2B818CC52B2B856BA)
* [Modèles de balises conditionnelles](../c-appendices/c-templates.md#section_18D9BC66DE484881932FD2F7EA9D170D)
* [Modèles de balises de contrôle de formulaire](../c-appendices/c-templates.md#section_45AFC414ACA74825B72FEAA8456F8DD2)

Rechercher dans les rubriques de référence des modèles

* [Chaînes de format de date](../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4)
* [Identifiants de langue](../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911)
* [Spécification de l’en-tête HTTP de type de contenu](../c-appendices/c-templates.md#section_AEED823E9938448A9EDB2F286D9CFD90)
* [Spécification d’un jeu de caractères dans un modèle HTML](../c-appendices/c-templates.md#section_E0D1816ABB5846BEBE9C26D5980CCBE6)
* [Spécification d’un jeu de caractères dans un modèle XML](../c-appendices/c-templates.md#section_17DC31CDCC104F5F8081466B41A96E9D)
* [Inclusion d’un modèle de recherche dans un autre](../c-appendices/c-templates.md#section_7D1FCD3D9E2340C291E354C9720E8BC0)

## A propos des balises de boucle Résultats {#section_D4DC7B4560144663972E8DBC3369C629}

La balise de boucle de résultats est le cheval de travail du système de modèles. Lorsque la balise est rencontrée lors d’une recherche, le code HTML est répété et d’autres balises entre les balises de boucle de résultats de début et de fin, remplaçant ainsi toutes les autres balises par les résultats de la recherche.

`<search-results> ... </search-results>`

Les balises de boucle de résultats entourent le code HTML qui affiche les résultats de la recherche. Le code HTML entre les balises est répété pour chaque résultat et s’affiche sur la page.

Les balises suivantes ne sont valides que dans la boucle de résultats :

* [Balises de chaîne de boucle de résultats](../c-appendices/c-templates.md#section_80D68334E8D04A33937A6E58ABAAA320)
* [Balises conditionnelles de boucle de résultats](../c-appendices/c-templates.md#section_35C367969E384A06A9865E388F1F9360)
* [Balises de lien d’ancrage de boucle de résultats](../c-appendices/c-templates.md#section_C5FAEF520E9E42ADAD1F90651922AA02)
* [Balises conditionnelles de position de boucle](../c-appendices/c-templates.md#section_E0C29DDA09E043C9A396F36334F05EBB)

## Balises de chaîne de boucle de résultats {#section_80D68334E8D04A33937A6E58ABAAA320}

Les balises suivantes renvoient une chaîne.

Voir [A propos des balises](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)de boucle Résultats.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Baliser </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-index&gt; </span> </p> </td> 
   <td colname="col2"> <p>Renvoie l’index numérique du résultat actuel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-title length="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Renvoie le titre de la page du résultat actuel. L’attribut de longueur facultatif est utilisé pour limiter la longueur des chaînes affichées, avec une valeur par défaut de 80 caractères. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;searchbody-text length="XX" encoding="html/javascript/json/perl/url/none" &gt; </span> </p> </td> 
   <td colname="col2"> <p>Renvoie le texte du corps à partir du haut de la page. Les termes pertinents sont indiqués en caractères gras. L’attribut de longueur facultatif est utilisé pour limiter la longueur des chaînes affichées, avec une valeur par défaut de 80 caractères. L’attribut encoding est facultatif et peut coder les caractères de sortie avec le codage HTML (par défaut), le codage JavaScript, le codage Perl ou aucun. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-description length="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Renvoie la description du résultat actuel. Si la balise meta description existe et que l’attribut content n’est pas vide, ce texte s’affiche. Sinon, le début du corps du texte de la page s’affiche. L’attribut de longueur facultatif est utilisé pour limiter la longueur des chaînes affichées, avec une valeur par défaut de 80 caractères. </p> <p>L’attribut facultatif <span class="codeph"> encoding </span> contrôle si la sortie est codée au format HTML, JavaScript, Perl, URL ou non codée, pour la sortie sur la page de résultats. La valeur par défaut du <span class="codeph"> codage </span> est <span class="codeph"> html </span>. Normalement, vous n’avez pas besoin de spécifier l’attribut de codage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;score de recherche grade="dynamic/static/dynamic-raw/static-raw/final-raw" précision="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Renvoie le score du résultat actuel, qui est un nombre compris entre 0 et 100. Si vous avez défini un champ de classement sous <span class="uicontrol"> Options </span> &gt; <span class="uicontrol"> Métadonnées </span> &gt; <span class="uicontrol"> Définitions </span>, vous pouvez afficher le classement dynamique des pages en définissant l’attribut de classement sur dynamique ( <span class="codeph"> &lt;score de recherche ="dynamique"&gt; ). </span> Vous pouvez afficher le classement de page statique en définissant l'attribut de classement sur statique ( <span class="codeph"> &lt;score de recherche grade="statique"&gt; </span>). Vous pouvez utiliser l’attribut de précision facultatif pour spécifier le nombre de décimales à afficher. La valeur par défaut est 0, ce qui affiche le score entier). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-date length="XX" none="text" date-format="date-format-string" gmt="yes/no" language="0/2/language-id"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Renvoie la date du résultat actuel. La valeur de texte facultative "aucun" s’affiche si aucune date n’est associée au résultat actuel. Si la valeur facultative "aucun" n’est pas indiquée, le texte "Aucune date" s’affiche si aucune date n’est associée au résultat actuel. </p> <p>L’attribut "date-format" utilise une chaîne de format de date de style UNIX telle que "%A, %B %d, %Y" (pour "Lundi, 25 juillet 2016"). "gmt" est défini par défaut sur "yes" et contrôle si la partie "time" de la chaîne de date doit être générée en GMT ("yes") ou le fuseau horaire du compte ("no"). </p> <p>L’attribut "language" contrôle les conventions de langue et de paramètres régionaux de la chaîne de date de sortie. "0" (valeur par défaut) signifie "Utiliser la langue du compte". "2" signifie "Utiliser la langue du document". La valeur "langue" "1" est réservée pour une utilisation ultérieure. Toute autre valeur "language" est interprétée comme un identifiant de langue spécifique, par exemple, "en_US" signifie "English (United States)". </p> <p>L’attribut de longueur facultatif est utilisé pour limiter la longueur des chaînes affichées, avec une valeur par défaut de 80 caractères. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-size&gt; </span> </p> </td> 
   <td colname="col2"> <p>Renvoie la taille du résultat actuel en octets. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-url length="XX" encoding="html/javascript/json/perl/url/none" &gt; </span> </p> </td> 
   <td colname="col2"> <p>Renvoie l’URL du résultat actuel. </p> <p>Utilisez l’attribut facultatif <span class="codeph"> length </span> pour limiter la longueur des chaînes affichées, avec un nombre par défaut de caractères illimités. </p> <p>L’ <span class="codeph"> attribut </span> encoding est facultatif et peut coder les caractères de sortie avec le codage HTML, le codage JavaScript, le codage Perl ou aucun. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-url-path-query length="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Renvoie les parties chemin et requête, y compris le point d’interrogation de l’URL du résultat actuel. </p> <p>Utilisez l’attribut facultatif <span class="codeph"> length </span> pour limiter la longueur des chaînes affichées, avec un nombre par défaut de caractères illimités. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-context length="XX" encoding="html/javascript/json/perl/url/none" &gt; </span> </p> </td> 
   <td colname="col2"> <p>Renvoie la ligne de contexte suivante pour le terme recherché. Les termes pertinents sont indiqués en caractères gras. Appelez cette balise plusieurs fois pour afficher plusieurs lignes contextuelles pour le résultat actuel. </p> <p>Utilisez l’attribut facultatif <span class="codeph"> length </span> pour limiter la longueur des chaînes affichées, avec une valeur par défaut de 80 caractères. L’attribut <span class="codeph"> length </span> est ignoré si cette balise est entourée soit <span class="codeph"> &lt;search-if-context&gt; </span> , soit <span class="codeph"> &lt;search-if-any-context&gt; </span> jeux de balises qui contiennent un attribut length. </p> <p>L’ <span class="codeph"> attribut </span> encoding est facultatif et peut coder les caractères de sortie avec le codage HTML (par défaut), le codage JavaScript, le codage Perl ou aucun. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field name="field-name" length="XX" none="text" date-format="date-format-string" gmt="yes/no" language="0/2/language-id" encoding="html/javascript/json/perl/url/none" Guillemets="yes/no" virgules="yes/no" units="miles/kilomètres" séparateurs""|"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cette balise avancée affiche le contenu du champ de métadonnées (url, title, desc, keys, target, body, alt, date, charset et la langue ou des champs définis sous <span class="uicontrol"> Options </span> &gt; <span class="uicontrol"> Métadonnées </span> &gt; Définitions) spécifié dans l’attribut de <span class="codeph"> nom </span> , pour le résultat actuel. Par exemple : </p> <p> <span class="codeph"> &lt;search-display-field name="title" length="70" none="aucun titre"&gt; </span> </p> <p>Génère le titre de la page pour un résultat de recherche. Si l’attribut facultatif <span class="codeph"> none </span> est spécifié, sa valeur s’affiche dans la page de résultats uniquement si aucun contenu n’est associé au champ. </p> <p>Les attributs <span class="codeph"> de format de date </span>, <span class="codeph"> gmt </span> et de langue ne sont pertinents que si le type de contenu du champ spécifié est le  de <span class="codeph"> </span> <span class="codeph"> date.</span> </p> <p>L'attribut <span class="codeph"> format de date </span> prend une chaîne de format de date de style UNIX, telle que <span class="codeph"> %A, %B %d, %Y </span> (pour le lundi 25 juillet 2016). <span class="codeph"> gmt </span> utilise par défaut <span class="codeph"> yes </span> et contrôle si la partie "time" de la chaîne de date est générée en GMT ( <span class="codeph"> oui </span>) ou le fuseau horaire du compte ( <span class="codeph"> non </span>). </p> <p>Voir <a href="../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4" type="section" format="dita" scope="local"> Chaînes</a>de format de date. </p> <p>L’ <span class="codeph"> attribut </span> de langue contrôle les conventions de langue et de paramètres régionaux de la chaîne de date de sortie. <span class="codeph"> 0 </span> (valeur par défaut) signifie "Utiliser la langue du compte". <span class="codeph"> 2 </span> signifie "Utiliser la langue du document". La <span class="codeph"> valeur </span> de langue <span class="codeph"> 1 </span> est réservée pour une utilisation ultérieure). Toute autre <span class="codeph"> valeur </span> de langue est interprétée comme un identifiant de langue spécifique, par exemple <span class="codeph"> en_US </span> signifie "Anglais (Etats-Unis)". </p> <p>Voir <a href="../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911" type="section" format="dita" scope="local"> Identifiants</a>de langue. </p> <p>L’attribut <span class="codeph"> de longueur facultatif </span> permet de limiter la longueur des chaînes affichées, avec une valeur par défaut de 80 caractères. </p> <p>L’attribut facultatif <span class="codeph"> encoding </span> contrôle si la sortie est codée au format HTML, JavaScript, Perl, URL ou non codée, pour la sortie sur la page de résultats. La valeur par défaut du <span class="codeph"> codage </span> est <span class="codeph"> html </span>. Normalement, vous n’avez pas besoin de spécifier l’attribut de codage. </p> <p>L’attribut <span class="codeph"> de guillemets facultatifs </span> contrôle si la sortie des éléments individuels est entourée de guillemets doubles (ou de guillemets simples, si <span class="codeph"> encoding=perl </span>). La valeur par défaut des <span class="codeph"> guillemets </span> est <span class="codeph"> non </span>. </p> <p>L’attribut facultatif <span class="codeph"> virgules </span> contrôle si la sortie des éléments individuels est séparée par des virgules. La valeur par défaut des <span class="codeph"> virgules </span> est <span class="codeph"> yes </span>. L’attribut <span class="codeph"> virgules </span> est ignoré pour les champs non de type liste. </p> <p>L’attribut <span class="codeph"> Unités facultatives </span> contrôle les unités de distance appliquées à un champ de sortie de recherche de proximité. La valeur par défaut des <span class="codeph"> unités </span> est déterminée à partir du paramètre "Unités par défaut" du champ location-type associé au champ de sortie de recherche de proximité donné. </p> <p>Voir <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> A propos de la recherche</a>de proximité. </p> <p>L’attribut facultatif <span class="codeph"> Separator </span> définit le caractère unique, ou délimiteur, inséré entre les valeurs de la sortie pour les champs de type liste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-values name="field-name"&gt; ...&lt;search-display-field-values&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cette balise crée une boucle pour l’énumération des valeurs de champ de métadonnées (url, title, desc, keys, target, body, alt, date, charset et langue ou des champs définis sous <span class="uicontrol"> Options </span> &gt; <span class="uicontrol"> Métadonnées </span> &gt; <span class="uicontrol"> Définitions </span>) pour le résultat actuel. N’imbriquez pas cette balise dans une autre <span class="codeph"> &lt;search-display-field-values&gt; </span> . L’ <span class="codeph"> attribut name </span> spécifie le nom du champ contenant les valeurs à énumérer. Cette balise est particulièrement utile lorsque l’attribut <span class="uicontrol"> Autoriser les listes </span> est coché (sous <span class="uicontrol"> Options </span> &gt; <span class="uicontrol"> Métadonnées </span> &gt; <span class="uicontrol"> Définitions ).</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-value date-format="date-format-string" gmt="yes/no" language="0/language-id" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cette balise génère la valeur du champ de métadonnées (url, title, desc, keys, target, body, alt, date, charset et langue ou des champs définis sous <span class="uicontrol"> Options </span> &gt; <span class="uicontrol"> Métadonnées </span> &gt; <span class="uicontrol"> Définitions </span>) pour l’itération de la <span class="codeph"> boucle active &lt;search-display-field-values&gt; . </span> Cette balise n’est valide que dans une boucle <span class="codeph"> &lt;search-display-field-values&gt; </span> . Les attributs <span class="codeph"> de format de date </span>, <span class="codeph"> gmt </span> et de langue ne sont pertinents que si le type de contenu du nom de champ spécifié dans la balise <span class="codeph"> </span> <span class="codeph"> &lt;search-display-field-values&gt;  est  date . </span><span class="codeph"></span> L’attribut <span class="codeph"> format-date </span> utilise une chaîne de format de date de style UNIX, telle que <span class="codeph"> "%A </span>, <span class="codeph"> %B </span> <span class="codeph"> %d ,  %Y " (pour "Lundi, 25 juillet 2016"). </span><span class="codeph"></span> L’attribut <span class="codeph"> gmt </span> prend par défaut la valeur <span class="codeph"> oui </span> et contrôle si la partie Heure de la chaîne de date est générée en GMT ( <span class="codeph"> oui </span>) ou le fuseau horaire du compte ( <span class="codeph"> pas de ).</span> </p> <p>L’ <span class="codeph"> attribut </span> de langue contrôle les conventions de langue et de paramètres régionaux de la chaîne de date de sortie. <span class="codeph"> 0 </span> (valeur par défaut) signifie "Utiliser la langue du compte". Toute autre <span class="codeph"> valeur </span> de langue est interprétée comme un identifiant de langue spécifique, par exemple <span class="codeph"> en_US </span> signifie "Anglais (Etats-Unis)". </p> <p>L’attribut facultatif <span class="codeph"> encoding </span> contrôle si la sortie est codée au format HTML, JavaScript, Perl, URL ou non codée, pour la sortie sur la page de résultats. La valeur par défaut du <span class="codeph"> codage </span> est <span class="codeph"> html </span>. Normalement, vous n’avez pas besoin de spécifier l’attribut de codage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-value-count name="field-name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Génère le nombre total de valeurs dans le résultat actuel pour le champ de métadonnées (url, title, desc, keys, target, body, alt, date, charset et langue ou les champs définis sous <span class="uicontrol"> Options </span> &gt; <span class="uicontrol"> Métadonnées </span> &gt; <span class="uicontrol"> Définitions </span>) spécifiés avec l’attribut name. Cette balise peut apparaître n’importe où dans la boucle de résultats. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-value-compteur&gt; </span> </p> </td> 
   <td colname="col2"> <p>Génère le compteur ordinal (1, 2, 3, etc.) pour l’itération en <span class="codeph"> boucle actuelle de </span> &lt;search-display-field-values&gt;. Cette balise n’est valide que dans une boucle <span class="codeph"> &lt;search-display-field-values&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-dynamic-facet-fields&gt; </span> </p> </td> 
   <td colname="col2"> <p>Commence un contexte de boucle pour les champs de facettes dynamiques renvoyés pour cette recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-dynamic-facet-field-name&gt; </span> </p> </td> 
   <td colname="col2"> <p>Génère le nom du champ de facette dynamique actuel pour cette itération de boucle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release on October 30 2014--> <span class="codeph"> &lt;search-result-trace encoding="html/javascript/ json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Génère des informations relatives à l’emplacement du résultat actuel, par exemple, toute action basée sur les résultats qui affecte la position du résultat. </p> <p>Le format de sortie de cette balise est JSON, comme dans l’exemple suivant : </p> <p> <code> { 
      &nbsp;&nbsp;"sliceID":&nbsp;5, 
      &nbsp;&nbsp;"indexID":&nbsp;5894, 
      &nbsp;&nbsp;"finalScore":&nbsp;98.5, 
      &nbsp;&nbsp;"dynamicScore":&nbsp;15.3, 
      &nbsp;&nbsp;"staticScore":&nbsp;55.456, 
      &nbsp;&nbsp;"position":&nbsp;1, 
      &nbsp;&nbsp;"rbtaActionListID":&nbsp;117, 
      &nbsp;&nbsp;"rbtaActionID":&nbsp;57 
      } </code> </p> 
    <!--<p> Results added to the results set by way of <codeph>rbta</codeph> have a "naturalPosition" value of -1. </p>--> <p>L’ <span class="codeph"> attribut </span> de codage est facultatif ; la valeur par défaut est <span class="codeph"> html </span>. </p> <p> <p>Remarque :  Cette balise n’a de sortie que si <span class="codeph"> sp_trace=1 </span> est spécifié avec les paramètres de requête de recherche principaux. </p> </p> <p>Reportez-vous à la ligne 48 du tableau figurant dans les paramètres <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" format="dita" scope="local"></a>CGI de recherche en arrière-plan. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Balises conditionnelles de boucle de résultats {#section_35C367969E384A06A9865E388F1F9360}

Les balises suivantes incluent de manière conditionnelle le code HTML entre elles.

Voir [A propos des balises](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)de boucle Résultats.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Baliser </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-title&gt; ... &lt;/search-if-title&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-title&gt;... &lt;/search-if-not-title&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ces balises comprennent le code HTML entre elles si l’appel suivant à <span class="codeph"> &lt;search-title&gt; </span> renvoie (ou ne renvoie pas) du texte du titre du document. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-description length="XX"&gt; ... /search-if-description&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-description&gt;... &lt;/search-if-not-description&gt; </span> </p> </td> 
   <td colname="col2"> <p> Ces balises comprennent le code HTML entre elles si l’appel suivant à <span class="codeph"> &lt;search-description&gt; </span> renvoie (ou ne renvoie pas) du texte de la description du document. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-body-text&gt;... &lt;/search-if-body-text&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-body-text&gt;... &lt;/search-if-not-body-text&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ces balises comprennent le code HTML entre elles si l’appel suivant à <span class="codeph"> &lt;search-body text&gt; </span> renvoie (ou ne renvoie pas) du texte du corps du document. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-context length="XX"&gt; ... &lt;/search-if-context&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-context&gt; ... &lt;/search-if-not-context&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ces balises comprennent le code HTML entre elles si l’appel suivant à <span class="codeph"> &lt;search-context&gt; </span> renvoie (ou ne renvoie pas) une chaîne de contexte non vide. L’attribut length remplace l’attribut length sur toute balise <span class="codeph"> &lt;search-context&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-any-context length="XX"&gt; ... /search-if-any-context&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-any-context&gt; ... &lt;/search-if-not-any-context&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ces balises incluent le code HTML entre elles s’il existe (ou n’est pas) une chaîne contextuelle associée au résultat. L’attribut length remplace l’attribut length sur toute balise <span class="codeph"> &lt;search-context&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-score lower="XX" upper="yy" level="dynamic/static-raw/static-raw/static-raw/final-raw"&gt;... &lt;/search-if-score&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-score lower=XX upper=yy grade="dynamic/static"&gt;&gt;... &lt;/search-if-not-score&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ces balises incluent le code HTML entre elles si le score du résultat actuel est (ou n’est pas) compris entre XX et YY. Utile pour ajouter des puces ou des graphiques afin de montrer à quel point le résultat est pertinent. Si vous avez défini un champ de type de classement sous <span class="uicontrol"> Options </span> &gt; <span class="uicontrol"> Métadonnées </span> &gt; <span class="uicontrol"> Définitions </span>, vous pouvez vérifier le classement dynamique des pages en définissant l’attribut de classement sur dynamique ( <span class="codeph"> &lt;search-if-score grade="dynamic" lower=XX upper=YY&gt; ). </span> Vous pouvez vérifier le classement des pages statiques en définissant l’attribut de classement sur statique ( <span class="codeph"> &lt;search-if-score grade="static" lower=XX upper=YY&gt; </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-field name="field-name" value="value"&gt; ... &lt;/search-if-field&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-field name="field-name" value="value"&gt; ... &lt;/search-if-not-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ces balises avancées incluent le code HTML entre elles selon que le champ spécifié dans l’attribut "name" contient ou non du contenu. Si l’attribut "value" facultatif est spécifié, les balises incluent le code HTML entre elles selon que la valeur donnée correspond (ou non) à la valeur du champ dans le résultat actuel. Ces balises fonctionnent uniquement dans la boucle de résultats (entre les balises <span class="codeph"> &lt;search-results&gt; </span> et <span class="codeph"> &lt;/search-results&gt; </span> ). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Balises de lien d’ancrage de boucle de résultats {#section_C5FAEF520E9E42ADAD1F90651922AA02}

Voir [A propos des balises](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)de boucle Résultats.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Baliser </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-link target="frame-name" hbx-enable="yes/no" hbx-linkid-name="field-name" hbx-linkid-none="text" hbx-linkid-length="XX" &gt; ... &lt;/search-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cette paire de balises crée un lien d’ancrage autour du code HTML entre ces deux balises. Lorsque vous cliquez sur le lien, la page des résultats s’affiche. Un attribut cible facultatif spécifie la fenêtre nommée dans laquelle les navigateurs capables d’afficher les images doivent afficher la page de résultats. </p> <p>Définissez l’attribut hbx-enable sur "yes" pour tirer parti des analyses disponibles via HBX. Définissez hbx-linkid-name sur le nom d’un champ de métadonnées dont vous souhaitez effectuer le suivi. Par exemple, pour suivre les résultats de la recherche par numéro de SKU, définissez hbx-linkid-name sur le nom du champ Meta-data qui contient les informations de SKU. </p> <p>Les champs de type de date ne sont actuellement pas pris en charge. La valeur de hbx-linkid-name est ajoutée à l’ID de lien dans l’ancre générée. La valeur de l’attribut hbx-linkid-none est ajoutée à l’ID de lien chaque fois que le champ Meta-data nommé est vide. La valeur de hbx-linkid-length limite le nombre de caractères récupérés et affichés à partir de la balise Meta. Le nombre de caractères par défaut est 12. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-smart-link target="frame-name" hbx-enable="yes/no" hbx-linkid-name="field-name" hbx-linkid-none="text" hbx-linkid-length="XX"&gt; ... &lt;/search-smart-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cette paire de balises est similaire au <span class="codeph"> &lt;lien de recherche&gt; ... &lt;/search-link&gt; </span> balises. Lorsque vous cliquez sur les liens d’ancrage générés, la page de résultats s’affiche, mais avec le défilement de la page vers la balise d’ancrage la plus proche précédant le résultat. Pour les liens PDF, la visionneuse Acrobat affiche la page qui contient le résultat. Un attribut cible facultatif spécifie la fenêtre nommée dans laquelle les navigateurs capables d’afficher les images doivent afficher la page de résultats. </p> <p>Définissez l’attribut hbx-enable sur "yes" pour tirer parti des analyses disponibles via HBX. Définissez hbx-linkid-name sur le nom d’un champ de métadonnées dont vous souhaitez effectuer le suivi. Par exemple, pour suivre les résultats de la recherche par numéro de SKU, définissez hbx-linkid-name sur le nom du champ Meta-data qui contient les informations de SKU. </p> <p>Les champs de type de date ne sont actuellement pas pris en charge. La valeur de hbx-linkid-name est ajoutée à l’ID de lien dans l’ancre générée. La valeur de l’attribut hbx-linkid-none est ajoutée à l’ID de lien chaque fois que le champ Meta-data nommé est vide. La valeur de hbx-linkid-length limite le nombre de caractères récupérés et affichés à partir de la balise Meta. Le nombre de caractères par défaut est 12. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-link-extension&gt;... &lt;/search-if-link-extension&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-link-extension&gt;... &lt;/search-if-not-link-extension&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ces balises comprennent le code HTML entre elles si un attribut de valeur spécifie une extension qui correspond à la fin de l’URL du résultat. Cette balise est utile pour inclure un graphique dans les résultats de la recherche en fonction de l’extension du lien. L’attribut value est une liste d’une ou de plusieurs extensions (espacement), comme suit : VALUE=".pdf" ou VALUE=".html.htm". </p> </td> 
  </tr> 
 </tbody> 
</table>

## Balises conditionnelles de position de boucle {#section_E0C29DDA09E043C9A396F36334F05EBB}

Les balises suivantes incluent de manière conditionnelle le texte entre elles. Ils ne peuvent apparaître qu’à l’intérieur des balises de boucle : &lt; `search-results>` et `<search-field-values>`. Ils sont utilisés pour tester la position du résultat actuel dans le jeu de résultats.

Voir [A propos des balises](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)de boucle Résultats.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Baliser </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-first&gt; ... &lt;/search-if-first&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-first&gt; ... &lt;/search-if-not-first&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ces balises comprennent le texte entre elles si le résultat actuel est (ou n’est pas) le premier résultat sur la page (lorsqu’il est utilisé dans <span class="codeph"> &lt;search-results&gt; </span>) ou la première valeur de champ (lorsqu’il est utilisé dans <span class="codeph"> &lt;search-field-values&gt; </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-last&gt; ... &lt;/search-if-last&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-last&gt; ... &lt;/search-if-not-last&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ces balises comprennent le texte entre elles si le résultat actuel est (ou n’est pas) le dernier résultat sur la page (lorsqu’il est utilisé dans <span class="codeph"> &lt;search-results&gt; </span>) ou la dernière valeur de champ (lorsqu’il est utilisé dans <span class="codeph"> &lt;search-field-values&gt; </span>). Cette balise peut être utilisée pour insérer un séparateur entre les résultats. Par exemple, une balise <span class="codeph"> &lt;hr&gt; </span> est insérée entre les résultats : </p> <p> <code class="syntax html"> &lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&lt;search-lt&gt;tr&lt;search-if-alt&gt;&nbsp;class="alt"&lt;/search-if-alt&gt;&lt;search-gt&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;td&gt;&lt;search-url&gt;&lt;/td&gt; 
      &nbsp;&nbsp;&nbsp;&lt;/tr&gt; 
      &lt;/search-results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-inner&gt;... &lt;/search-if-inner&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-inner&gt;... &lt;/search-if-not-inner&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ces balises comprennent le texte entre elles si le résultat actuel n’est ni le premier ni le dernier résultat de la page (lorsqu’il est utilisé dans <span class="codeph"> &lt;search-results&gt; </span>), ni la première ni la dernière valeur du champ (lorsqu’il est utilisé dans <span class="codeph"> &lt;search-field-values&gt; </span>). La version "not" de la balise teste si le résultat est le premier ou le dernier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-alt&gt;... &lt;/search-if-alt&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-alt&gt; ... &lt;/search-if-not-alt&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ces balises comprennent le texte entre elles si le résultat actuel est (ou n’est pas) un résultat alternatif sur la page (lorsqu’il est utilisé dans <span class="codeph"> &lt;search-results&gt; </span>) ou une autre valeur de champ (lorsqu’il est utilisé dans <span class="codeph"> &lt;search-field-values&gt; </span>). Les résultats "alternatifs" sont les deuxième, quatrième, sixième, etc., sur la page. Cet exemple applique une classe différente aux rangées de tableau de remplacement. Notez l’utilisation des balises <span class="codeph"> &lt;search-lt&gt; </span> et <span class="codeph"> &lt;search-gt&gt; </span> pour permettre de placer la balise <span class="codeph"> &lt;search-if-alt&gt; </span> dans la balise <span class="codeph"> &lt;tr&gt; .</span> </p> <p> <code class="syntax html"> &nbsp;&nbsp;&nbsp;&nbsp;&lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-lt&gt;tr&lt;search-if-alt&gt;&nbsp;class="alt"&lt;/search-if-alt&gt;&lt;search-gt&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;td&gt;&lt;search-url&gt;&lt;/td&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/tr&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-even&gt; ... &lt;/search-if-even&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-even&gt;... &lt;/search-if-not-even&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ces balises comprennent le texte entre elles si le résultat actuel est (ou n’est pas) un résultat pair (lorsqu’il est utilisé à l’intérieur de <span class="codeph"> &lt;search-results&gt; </span>) ou une valeur de champ pair (lorsqu’il est utilisé à l’intérieur de <span class="codeph"> &lt;search-field-values&gt; </span>). Un résultat de recherche est pair si sa valeur <span class="codeph"> &lt;search-index&gt; </span> est paire. En d’autres termes, si sa position dans l’ensemble du jeu de résultats est égale. Cela peut être différent de <span class="codeph"> &lt;search-if-alt&gt; </span> qui teste la position d’un résultat sur la page et non dans l’ensemble du jeu de résultats. Les deux tableaux suivants illustrent cette différence : </p> </td> 
  </tr> 
 </tbody> 
</table>

### Première page, sp_n=1

<table>  
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Index </p> </th> 
   <th colname="col2" class="entry"> <p>Résultats </p> </th> 
   <th colname="col3" class="entry"> <p>Même ? </p> </th> 
   <th colname="col4" class="entry"> <p>Alt ? </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>Premier résultat </p> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Non </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>Second résultat </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>Troisième résultat </p> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Non </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>Quatrième résultat </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>Cinquième résultat </p> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Non </p> </td> 
  </tr> 
 </tbody> 
</table>

### Page suivante, sp_n=10

<table>  
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Index </p> </th> 
   <th colname="col2" class="entry"> <p>Résultats </p> </th> 
   <th colname="col3" class="entry"> <p>Même ? </p> </th> 
   <th colname="col4" class="entry"> <p>Alt ? </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>10 </p> </td> 
   <td colname="col2"> <p>Dixième résultat </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Non </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>11 </p> </td> 
   <td colname="col2"> <p>Onzième résultat </p> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>12 </p> </td> 
   <td colname="col2"> <p>Douzième résultat </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Non </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>13 </p> </td> 
   <td colname="col2"> <p>Treizième résultat </p> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>14 </p> </td> 
   <td colname="col2"> <p>Quatorzième résultat </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Non </p> </td> 
  </tr> 
 </tbody> 
</table>

Enfin, notez que `<search-if-even>` c’est toujours la même chose que `<search-if-alt>` pour les valeurs de champ de recherche, car les valeurs de champ ne sont pas paginées.

## Balises de liste de valeurs de champ {#section_D3298B5F976447DBA0032B883DCC91B1}

Les balises avancées suivantes génèrent des valeurs de champ et des données associées à partir de l’ensemble des résultats de recherche. Ces balises ne génèrent que des résultats pour les champs spécifiés par les paramètres `sp-sfvl-field` CGI dans la requête de recherche.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Baliser </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;nom-champ-valeur-liste-nom-champ="nom-champ" guillemets="oui/non" virgules="oui/non" data="valeurs/nombres/résultats" separator="X" sortby="aucun/valeurs/nombres/résultats" max-items="XX" format-date="chaîne-format-date" gmt="oui/non" language="0/language-id" html="encodage" ascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cette balise affiche une liste de valeurs de champ uniques, de valeurs ou de résultats dans l’ensemble du jeu de résultats. </p> <p>Cette balise ne génère une sortie que pour les champs spécifiés par les paramètres <span class="codeph"> sp_sfvl_field </span> CGI dans la requête de recherche. L’attribut "guillemets" facultatif contrôle si la sortie des éléments individuels est entourée de guillemets doubles (ou de guillemets simples, si encoding=perl). La valeur par défaut de "quotes" est "yes". L’attribut facultatif "virgules" contrôle si la sortie des éléments individuels est séparée par des virgules. La valeur par défaut de "virgules" est "yes". L’attribut "data" facultatif contrôle si chaque valeur de champ unique est une sortie (data="valeurs"), le nombre total de chaque valeur de champ unique est une sortie (data="counts") ou le nombre de résultats contenant chaque valeur unique (data="results") est une sortie. La valeur par défaut de "data" est "values". Pour les champs non de type liste, data="counts" et data="results" sont équivalents. L’attribut separator définit le caractère unique, ou délimiteur, à insérer entre les valeurs de la sortie. L'attribut facultatif "sortby" contrôle l'ordre de la sortie; sortby="none" signifie aucun ordre particulier, sortby="valeurs" signifie le tri par valeurs de champ (dans l’ordre croissant ou décroissant selon la propriété de tri du champ), sortby="counts" signifie le tri dans l’ordre décroissant des valeurs de champ et sortby="results" signifie le tri dans l’ordre décroissant du nombre de résultats contenant chaque valeur. </p> <p>Notez que sortby="counts" et sortby="results" sont équivalents pour les champs non-list-type. L’attribut facultatif "max-items" limite le nombre d’éléments à générer. La valeur par défaut de "max-items" est -1, ce qui signifie "output all items". </p> <p>Il existe une limite absolue de 100 pour les éléments max.. Les attributs "date-format", "gmt" et "langue" ne sont pertinents que si le type de contenu du champ spécifié est "date". L’attribut "date-format" utilise une chaîne de format de date de style UNIX telle que "%A, %B %d, %Y" (pour "Lundi, 25 juillet 2016"). "gmt" est défini par défaut sur "yes" et contrôle si la partie "time" de la chaîne de date doit être générée en GMT ("yes") ou le fuseau horaire du compte ("no"). </p> <p>Voir <a href="../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4" type="section" format="dita" scope="local"> Chaînes</a>de format de date. </p> <p>L’attribut "language" contrôle les conventions de langue et de paramètres régionaux de la chaîne de date de sortie. "0" (valeur par défaut) signifie "Utiliser la langue du compte". Toute autre valeur "language" est interprétée comme un identifiant de langue spécifique, par exemple, "en_US" signifie "English (United States)". L’attribut "encoding" facultatif contrôle si les caractères de la chaîne de sortie sont codés au format HTML, JavaScript, Perl, URL ou non codés, pour une sortie sur la page de résultats. La valeur par défaut de "encoding" est "html". </p> <p>Voir <a href="../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911" type="section" format="dita" scope="local"> Identifiants</a>de langue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;nom-champ-valeur-liste-nom-champ="nom-champ" valeur="valeur-champ" résultats="oui/non"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cette balise affiche les informations de nombre pour une liste de valeurs de champ de recherche donnée. Il existe trois utilisations distinctes pour cette balise. Si seul l’attribut "name" est fourni, cette balise génère le nombre de valeurs uniques pour le champ nommé dans l’ensemble des résultats. Si les attributs "name" et "value" sont tous deux fournis, cette balise indique soit le nombre total de la valeur donnée dans l’ensemble du jeu de résultats (pour results="no"), soit le nombre total de résultats contenant la valeur donnée dans l’ensemble du jeu de résultats (pour results="yes"). La valeur par défaut de "results" est "no". Remarque : Pour les champs qui ne sont pas de type liste, les résultats="yes" et les résultats="no" sont équivalents. La valeur de "results" est ignorée si l’attribut "value" n’est pas fourni. Cette balise ne génère une sortie que pour les champs spécifiés par les paramètres <span class="codeph"> sp-sfvl-field </span> CGI dans la requête de recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-field-value-list-count name="field-name" value="field-value"&gt; ... &lt;/search-if-field-value-list-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-field-value-list-count name="field-name" value="field-value"&gt; ... &lt;/search-if-not-field-value-list-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ces balises affichent le code HTML entre elles si l’appel équivalent à <span class="codeph"> &lt;search-field-value-list-count name="field-name" value="field-value"&gt; </span> avec les attributs donnés renvoie (ou ne renvoie pas) une valeur supérieure à zéro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-single-field-value-list-count name="field-name"&gt;&gt; ... &lt;/search-if-single-field-value-list-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ces balises affichent le contenu entre elles si l’appel équivalent à <span class="codeph"> &lt;search-field-value-list-count name="field-name" value="field-value"&gt; </span> avec les attributs donnés renvoie (ou ne renvoie pas) une seule valeur. Cette méthode est généralement utilisée lorsqu’un compte utilise des emplacements de facettes. Avec les emplacements de facette, vous ne souhaitez généralement afficher l’emplacement de valeur que lorsque l’emplacement de nom associé comporte un seul élément. Cette vérification dans le modèle de transport est plus efficace que dans la couche de présentation. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Balises de boucle de liste de valeurs de champ {#section_0717FA09F0FC449CB916883B0500A60E}

Les balises avancées suivantes énumèrent et génèrent les valeurs des champs et les données associées de l’ensemble des résultats de recherche à l’aide d’une méthode de boucle. Ces balises ne génèrent que des résultats pour les champs spécifiés par les paramètres `sp-sfvl-field` CGI dans la requête de recherche.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Baliser </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-values name="field-name" sortby="none/values/counts/results" max-items="XX"&gt; ... &lt;/search-field-values&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cette balise crée une boucle pour l’énumération des valeurs de champ et des données associées pour un champ particulier dans l’ensemble des résultats. N’imbriquez pas cette balise dans une autre <span class="codeph"> &lt;search-field-values&gt; </span> balise . L’attribut "name" spécifie le nom du champ contenant les valeurs à énumérer. L’attribut facultatif "sortby" contrôle l’ordre d’énumération : "none" signifie pas d’ordre particulier, "values" signifie le tri par valeurs de champ (dans l’ordre croissant ou décroissant selon la propriété de tri du champ), sortby="counts" signifie le tri dans l’ordre décroissant des valeurs de champ, et sortby="results" signifie le tri dans l’ordre décroissant du nombre de résultats contenant chaque valeur. </p> <p>Notez que sortby="counts" et sortby="results" sont équivalents pour les champs non-list-type. . L’attribut facultatif "max-items" limite le nombre d’itérations à la valeur donnée. La valeur par défaut de "max-items" est -1, ce qui signifie "enumerate all values". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value date-format="date-format-string" encoding="html/javascript/json/perl/url/none" gmt="yes/no" language="0/language-id"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cette balise génère la valeur du champ pour l’itération de boucle &lt;search-field-values&gt; actuelle. Cette balise n’est valide que dans une boucle <span class="codeph"> &lt;search-field-values&gt; </span> . Les attributs "date-format", "gmt" et "language" ne sont pertinents que si le type de contenu du nom de champ spécifié dans la balise &lt;search-field-values&gt; englobante est "date". L’attribut "date-format" utilise une chaîne de format de date de style UNIX telle que "%A, %B %d, %Y" (pour "Lundi, 25 juillet 2020"). </p> <p>Voir <a href="../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4" type="section" format="dita" scope="local"> Chaînes</a>de format de date. </p> <p>L’attribut "encoding" facultatif contrôle si les caractères de la chaîne de sortie sont codés au format HTML, JavaScript, Perl, URL ou non codés, pour une sortie sur la page de résultats. La valeur par défaut de "encoding" est "none". Normalement, vous n’avez pas besoin de spécifier l’attribut de codage. "gmt" est défini par défaut sur "yes" et contrôle si la partie "time" de la chaîne de date doit être générée en GMT ("yes") ou le fuseau horaire du compte ("no"). L’attribut "language" contrôle les conventions de langue et de paramètres régionaux de la chaîne de date de sortie. "0" (valeur par défaut) signifie "Utiliser la langue du compte". Toute autre valeur "language" est interprétée comme un identifiant de langue spécifique, par exemple, "en_US" signifie "English (United States)". </p> <p>Voir <a href="../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911" type="section" format="dita" scope="local"> Identifiants</a>de langue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-count results="yes/no"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cette balise génère le nombre associé à l’itération de <span class="codeph"> boucle </span> &lt;search-field-values&gt; en cours. Le nombre de résultats est soit le nombre de résultats dans l’ensemble des résultats contenant la valeur du champ (results="yes"), soit le nombre total de la valeur du champ dans l’ensemble des résultats. La valeur par défaut de "results" est "no". </p> <p>Pour les champs qui ne sont pas de type liste, les résultats="yes" et les résultats="no" sont équivalents. Cette balise n’est valide que dans une boucle <span class="codeph"> &lt;search-field-values&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-compteur&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cette balise génère le compteur ordinal pour l’itération de <span class="codeph"> boucle actuelle </span> &lt;search-field-values&gt;. Cette balise n’est valide que dans une boucle <span class="codeph"> &lt;search-field-values&gt; </span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Suggérer des balises {#section_C28EB8B4F7DC4E278A0F143BCFEEB1AC}

Suggest fournit un &quot;Voulez-vous dire ?&quot; convivial pour suggérer d’autres termes de recherche. Si un utilisateur a mal orthographié un terme de recherche, par exemple, Suggérer peut l’aider à trouver des résultats en suggérant une orthographe correcte. Le système peut également suggérer des mots-clés apparentés qui peuvent aider un utilisateur à découvrir des résultats. Lors de la génération de suggestions, le service Suggestion utilise deux dictionnaires : l’une basée sur la langue du compte (définie sous **[!UICONTROL Indexing]** > **[!UICONTROL Words and Languages]** > **[!UICONTROL Language]**) et l’autre créée de manière unique à partir des mots-clés de l’index du compte.

>[!NOTE]
>
>Le service Suggest ne fonctionne pas pour le chinois, le japonais ou le coréen.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Baliser </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-suggestions&gt;... &lt;/search-if-suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>Entourez ces balises avec les balises de modèle "Suggérer", telles que <span class="codeph"> &lt;suggestion-recherche&gt; </span>, <span class="codeph"> &lt;lien-suggestion-recherche&gt; </span>, etc. Si la recherche génère des suggestions, le moteur de recherche génère et traite tout entre les balises open et close. Si la recherche ne génère pas de suggestions, aucun contenu imbriqué n’est généré. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestions&gt;... &lt;/search-suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cette balise génère la boucle "Suggérer", qui contient une liste de termes de recherche suggérés (par exemple, "compte", "intention" et "intention", pour une requête saisie à l’origine comme "intentions"). Lors de la génération de la liste de termes, le moteur de recherche répète jusqu’à cinq fois les balises HTML et/ou de modèle imbriquées, ce qui correspond au nombre maximum de suggestions. Utilisez l’attribut count pour spécifier le nombre de suggestions générées (entre 0 et 5). </p> <p>La balise <span class="codeph"> &lt;search-suggestions&gt; </span> peut apparaître plusieurs fois sur la page pour répéter la liste des suggestions. Plusieurs suggestions sont triées en fonction du nombre de résultats que chacun produit. </p> <p>Imbriquez la <span class="codeph"> balise &lt;search-suggestions&gt; </span> entre les balises open et close <span class="codeph"> &lt;search-if-suggestions&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-link&gt; ... &lt;/search-suggestion-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cette balise génère un lien vers la requête de recherche d’origine à l’aide du terme de recherche suggéré sélectionné au lieu du terme d’origine. La balise accepte et imprime simplement tout attribut HTML tel que class, target et style. La balise peut également accepter un attribut d’URL, dont la valeur est utilisée comme URL de base pour le lien généré. Les balises ne peuvent apparaître qu’à l’intérieur de la boucle <span class="codeph"> &lt;search-suggestions&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-text/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cette balise imprime le terme de requête actuellement suggéré (par exemple, "compte" pour une requête saisie à l’origine comme "compte"). La balise n’a aucun attribut et ne peut apparaître qu’à l’intérieur de la boucle <span class="codeph"> &lt;search-suggestions&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-not-suggestions&gt;... &lt;/search-if-not-suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>Si la recherche ne génère aucune suggestion, le moteur de recherche génère et traite tout entre la balise d'ouverture et la balise de fermeture. Si la recherche génère des suggestions, aucun contenu imbriqué n’est généré. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if[-not]-first-suggestion&gt;... &lt;/search-if[-not]-first-suggestion&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ces balises conditionnelles incluent le code HTML entre elles selon que le terme suggéré est le premier terme de la boucle Suggérer. Les balises doivent apparaître entre les balises open et close <span class="codeph"> &lt;search-suggestion&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if[-not]-last-suggestion&gt;... &lt;/search-if[-not]-last-suggestion&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ces balises conditionnelles incluent le code HTML entre elles selon que le terme suggéré est le dernier terme de la boucle Suggérer. Les balises doivent apparaître entre les balises open et close <span class="codeph"> &lt;search-suggestion&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-index&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cette balise renvoie l’index numérique du terme de recherche suggéré actuel. La balise doit apparaître entre les balises open et close <span class="codeph"> &lt;search-suggestion&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-total&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cette balise renvoie le nombre total de termes de recherche suggérés générés. La balise doit apparaître entre les balises open et close <span class="codeph"> &lt;search-suggestion&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-result-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cette balise renvoie le nombre total de résultats pour le terme de recherche suggéré. La balise doit apparaître entre les balises open et close <span class="codeph"> &lt;search-suggestion&gt; </span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Balises de chaîne de modèle {#section_67E3D529661F4F03A1FF469D9D658CAF}

Les balises suivantes génèrent une chaîne dans le code HTML à ce stade du modèle.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Baliser </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-body&gt; </span> </p> </td> 
   <td colname="col2"> <p>Balise de contenu HTML avec les paramètres de couleur du lien de recherche que la section Aspect de base définit sous le lien Modèle. Ajoutez un attribut d’arrière-plan à cette balise pour afficher les images d’arrière-plan sur la page de résultats. Les attributs de couleur ajoutés à cette balise remplacent les paramètres de couleur du lien de recherche définis par la section Aspect de base. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-header&gt; </span> </p> </td> 
   <td colname="col2"> <p>Code HTML de l’en-tête des résultats de recherche tel que défini dans la section Aspect de base sous le lien Modèle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-cdata&gt; ... &lt;/search-cdata&gt; </span> </p> </td> 
   <td colname="col2"> <p>Les balises search-data sont remplacées par leurs équivalents XML : <span class="codeph"> &lt;search-cdata&gt; </span> est remplacé par <span class="codeph"> &lt;![CDATA[" et la balise &lt;/search-cdata&gt; </span> est remplacée par " <span class="codeph"> ]]&gt; </span>". Un analyseur XML n’analyse aucune information entre les balises open et close. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-query-query-number="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Requête saisie par le visiteur. L’attribut avancé facultatif "query-number" contrôle quelle chaîne de requête numérotée est générée par cette balise. Par exemple, <span class="codeph"> &lt;search-query query-query-number=1&gt; </span> génère le contenu du paramètre <span class="codeph"> cgi </span> sp_q_1. Si "query-number" n’est pas spécifié ou si query-number est "0", la requête principale ( <span class="codeph"> sp_q </span>) est générée. L’attribut "encoding" facultatif contrôle si la sortie est codée au format HTML, JavaScript, Perl, URL ou non codée, pour la sortie sur la page de résultats. La valeur par défaut de "encoding" est "html". Normalement, vous n’avez pas besoin de spécifier l’attribut de codage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-total&gt; </span> </p> </td> 
   <td colname="col2"> <p>Nombre total de résultats pour cette recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Nombre de résultats signalés pour cette page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-lower&gt; </span> </p> </td> 
   <td colname="col2"> <p>Numéro du premier résultat rapporté pour cette page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-upper&gt; </span> </p> </td> 
   <td colname="col2"> <p>Numéro du dernier résultat rapporté pour cette page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-prev-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Nombre de résultats signalés pour la page précédente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-next-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Nombre de résultats signalés pour la page suivante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-time&gt; </span> </p> </td> 
   <td colname="col2"> <p>Temps en secondes pour cette recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-logo&gt; </span> </p> </td> 
   <td colname="col2"> <p>Code HTML du logo de recherche configuré pour votre compte, le cas échéant. Ce logo est l'image qui attribue du crédit à la recherche/marchandisage sur le site </p> <p>Pour le moment, la plupart des comptes n’ont pas de logo de recherche associé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-collection all="name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Collection des résultats de cette recherche. L’attribut facultatif "all" est utilisé pour indiquer le nom de la collection qui représente l’ensemble du site Web. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-form&gt;...&lt;/search-form&gt; </span> </p> </td> 
   <td colname="col2"> <p>Insère les balises de formulaire de début et de fin. Insère les attributs de méthode et d’action dans la balise de début de formulaire. Accepte d’autres attributs, notamment l’attribut dir="RTL" pour le langage, ainsi que les attributs "name" et "onSubmit" liés à JavaScript. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-account&gt; </span> </p> </td> 
   <td colname="col2"> <p>Insère une balise d’entrée de formulaire qui spécifie le numéro de compte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-gallerie&gt; </span> </p> </td> 
   <td colname="col2"> <p>Insère une balise d’entrée de formulaire qui spécifie le numéro de la galerie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-query-query-number="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Insère une balise d’entrée de formulaire qui spécifie la chaîne de requête. L’attribut avancé facultatif "query-number" contrôle quelle requête numérotée est utilisée pour la balise d’entrée de formulaire. Par exemple, <span class="codeph"> &lt;search-input-query-query-number=1&gt; </span> génère une balise d’entrée de formulaire pour la <span class="codeph"> requête </span> sp_q_1. Si "query-number" n’est pas spécifié ou si "query-number" est "0", une balise d’entrée pour la requête <span class="codeph"> sp_q principale </span> est insérée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-collections all="name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Insère une balise de sélection de formulaire et le code HTML associé qui affiche le menu de sélection des collections. L’attribut facultatif "all" est utilisé pour indiquer le nom de la collection qui représente l’ensemble du site Web. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-lt&gt; </span> </p> </td> 
   <td colname="col2"> <p>Insère la sortie de l’une des balises de modèle Rechercher dans d’autres balises HTML ou de modèle sur la page de résultats. <span class="codeph"> &lt;search-lt&gt; </span> insère un caractère inférieur à. L’utilisation de <span class="codeph"> &lt;search-lt&gt; </span> et <span class="codeph"> &lt;search-gt&gt; </span> permet d’échapper à la définition d’une balise afin que vous puissiez utiliser les balises de modèle de recherche comme valeurs d’attribut. Lorsque le modèle est généré en réponse à une recherche, un signe inférieur à (&lt;) remplace la <span class="codeph"> balise &lt;search-lt&gt; </span> . Par exemple, <span class="codeph"> &lt;search-link&gt; </span> est équivalent à <span class="codeph"> &lt;search-lt&gt;a href="&lt;search-url&gt;"&lt;search-gt&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>20 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-gt&gt; </span> </p> </td> 
   <td colname="col2"> <p>Insère la sortie de l’une des balises de modèle Rechercher dans d’autres balises HTML ou de modèle sur la page de résultats. <span class="codeph"> &lt;search-gt&gt; </span> insère un caractère supérieur à. L’utilisation de <span class="codeph"> &lt;search-lt&gt; </span> et <span class="codeph"> &lt;search-gt&gt; </span> permet d’échapper à la définition d’une balise afin que vous puissiez utiliser d’autres balises de modèle comme valeurs d’attribut. Lorsque le modèle est généré en réponse à une recherche, un signe supérieur à (&gt;) remplace la <span class="codeph"> balise &lt;search-gt&gt; </span> . Par exemple, <span class="codeph"> &lt;search-link&gt; </span> est équivalent à <span class="codeph"> &lt;search-lt&gt;a href="&lt;search-url&gt;"&lt;search-gt&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>21 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-param name="param-name" length="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Renvoie la valeur du paramètre cgi nommé "param-name" de la requête de recherche active. L’attribut "encoding" facultatif contrôle si la sortie est codée au format HTML, JavaScript, Perl, URL ou non codée, pour la sortie sur la page de résultats. La valeur par défaut de "encoding" est "html". Normalement, vous n’avez pas besoin de spécifier l’attribut de codage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>22 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release on October 30 2014--> <span class="codeph"> &lt;search-trace encoding="html/javascript/ json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> 
    <!--<p>This global core search template tag outputs a representation of the submitted core search query, including any "fuzzy-search" query term expansions that happen by way of synonyms, sound-alikes, and so forth. </p>--> <p>L’ <span class="codeph"> attribut </span> de codage est facultatif ; la valeur par défaut est <span class="codeph"> json </span>. </p> <p> <p>Remarque :  Cette balise n’a de sortie que si <span class="codeph"> sp_trace=1 </span> est spécifié avec les paramètres de requête de recherche principaux. </p> </p> <p>Reportez-vous à la ligne 48 du tableau figurant dans les paramètres <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" format="dita" scope="local"></a>CGI de recherche en arrière-plan. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Balises de lien d’ancrage de modèle {#section_3A51D27616C541E2B818CC52B2B856BA}

Les balises suivantes sont des balises qui provoquent un lien d’ancrage entourant le code HTML entre elles. Lorsque vous cliquez dessus, le lien d’ancrage demande l’affichage d’une autre page de résultats. L’attribut facultatif &quot;count&quot; demande que de nombreux résultats de la page s’affichent. Si elle n’est pas spécifiée, le nombre demandé sur la page active est utilisé. L’attribut &quot;URL&quot; facultatif avancé contrôle le domaine vers lequel le lien associé est dirigé. Par défaut, le domaine est `https://search.atomz.com/search/`, mais vous pouvez le modifier à l’aide de l’attribut URL.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Baliser </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-next URL="https://search.yourdomain.com/search/"&gt;... &lt;/search-next&gt; </span> </p> <p> <span class="codeph"> &lt;search-prev URL="https://search.yourdomain.com/search/"&gt; ... &lt;/search-prev&gt; </span> </p> </td> 
   <td colname="col2"> <p>Affiche la page suivante ou précédente des résultats. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-sort-by-date URL="https://search.yourdomain.com/search/"&gt; ... &lt;/search-sort-by-date&gt; </span> </p> <p> <span class="codeph"> &lt;search-sort-by-score URL="https://search.yourdomain.com/search/"&gt; ... &lt;/search-sort-by-score&gt; </span> </p> </td> 
   <td colname="col2"> <p>Trie les résultats par date ou par pertinence. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-show-summary URL="https://search.yourdomain.com/search/"&gt; ... &lt;/search-show-summary&gt; </span> </p> <p> <span class="codeph"> &lt;search-hide-summary URL="https://search.yourdomain.com/search/"&gt; ... &lt;/search-hide-summary&gt; </span> </p> </td> 
   <td colname="col2"> <p>Affiche ou masque les résumés. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Modèles de balises conditionnelles {#section_18D9BC66DE484881932FD2F7EA9D170D}

Balises qui vous permettent d’inclure du code HTML de manière conditionnelle entre elles.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Baliser </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-results&gt; ... &lt;/search-if-results&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-results&gt;...&lt;/search-if-not-results&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ces balises incluent du code HTML si la page active contient des résultats de recherche (ou pas). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-prev-count&gt; ... &lt;/search-if-prev-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-prev-count&gt;... &lt;/search-if-not-prev-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-next-count&gt; ... &lt;/search-if-next-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-next-count&gt;... &lt;/search-if-not-next-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ces balises incluent du code HTML si la page précédente ou suivante est associée à des résultats (ou aucun). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-sort-by-score&gt;... &lt;/search-if-sort-by-score&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-sort-by-score&gt;... &lt;/search-if-not-sort-by-score&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-sort-by-date&gt;... &lt;/search-if-sort-by-date&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-sort-by-date&gt;... &lt;/search-if-not-sort-by-date&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ces balises comprennent du code HTML si la page active est triée par pertinence ou par date. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-show-summary&gt;... &lt;/search-if-show-summary&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-hide-summary&gt;... &lt;/search-if-hide-summary&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ces balises comprennent du code HTML si la page active affiche ou masque des résumés. Vous pouvez utiliser ces balises pour inclure ou exclure n’importe quelle partie des résultats de la recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-input-collections&gt;... &lt;/search-if-input-collections&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-input-collections&gt;... &lt;/search-if-not-input-collections&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ces balises incluent du code HTML si une collection a été spécifiée dans la génération des résultats de recherche pour la page active. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-advanced&gt;... &lt;/search-if-advanced&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-advanced&gt;... &lt;/search-if-not-advanced&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ces balises incluent du code HTML si le paramètre <span class="codeph"> sp_advanced=1 </span> CGI a été spécifié pour la requête de recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-bad-param name="parameter-name"&gt; ... &lt;/search-if-bad-param&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-bad-param name="parameter-name"&gt; ... &lt;/search-if-not-bad-param&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ces balises incluent ou excluent le code HTML entre elles si le paramètre donné est, ou non, non valide. </p> <p>Actuellement, seul le paramètre <span class="codeph"> sp_q_location[_#] </span> est pris en charge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-param name="param-name" value="param-value"&gt; ... &lt;/search-if-param&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-param name="param-name" value="param-value"&gt; ... &lt;/search-if-not-param&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ces balises avancées incluent le code HTML entre elles selon que le paramètre CGI spécifié dans l’attribut "name" a la valeur spécifiée dans l’attribut "value". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-sort-by-field name="field-name"&gt; ... &lt;/search-if-sort-by-field&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-sort-by-field name="field-name"&gt; ... &lt;/search-if-not-sort-by-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ces balises avancées incluent le code HTML entre elles si la page active est ou n’est pas triée selon le nom de champ donné. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Modèles de balises de contrôle de formulaire {#section_45AFC414ACA74825B72FEAA8456F8DD2}

Balises qui vous permettent de contrôler l’état de sélection par défaut des cases à cocher, des boutons radio et des zones de liste dans un `<form>` modèle de recherche.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Baliser </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input&gt; </span> </p> </td> 
   <td colname="col2"> <p>Utilisé dans un modèle à la place d’une balise <span class="codeph"> &lt;input&gt; </span> . Lorsque la balise est écrite dans le navigateur, le mot <span class="codeph"> input </span> remplace <span class="codeph"> -search-input </span> et toutes les autres informations de la balise sont output as-is. En outre, si le <span class="codeph"> nom </span> spécifié dans la balise est répertorié comme paramètre CGI et si la <span class="codeph"> valeur </span> spécifiée dans la balise est la valeur de ce paramètre CGI, le mot <span class="codeph"> coché </span> est ajouté à la fin de la balise . De cette manière, vous pouvez automatiquement définir l’état par défaut du bouton radio ou de la case à cocher dans le résultat de la recherche, de la même manière que la requête active. </p> <p>Par exemple, le code HTML d’une case à cocher peut ressembler à ce qui suit : </p> <p> <span class="codeph"> &lt;input type=checkbox name="sp_w" value="exact"&gt;Aucune correspondance de type son </span> </p> <p>Le code de modèle correspondant à cette case à cocher est le suivant : </p> <p> <span class="codeph"> &lt;search-input type=checkbox name="sp_w" value="exact"&gt;Aucune correspondance de type son </span> </p> <p>Si la chaîne de paramètre CGI de la requête contient <span class="codeph"> sp_w=exact </span>, la balise écrite dans le navigateur avec les résultats de la recherche ressemble à ce qui suit (le mot <span class="codeph"> coché </span> est inséré à la fin de la balise) : </p> <p> <span class="codeph"> &lt;input type=checkbox name="sp_w" value="exact" check&gt;Aucune correspondance de type son </span> </p> <p>Si la chaîne de paramètre CGI de la requête ne contient pas <span class="codeph"> sp_w=exact </span>, la balise écrite dans le navigateur avec les résultats de la recherche ressemble à ce qui suit (le mot <span class="codeph"> coché </span> n’est pas répertorié dans la balise) : </p> <p> <span class="codeph"> &lt;input type=checkbox name="sp_w" value="exact"&gt;Aucune correspondance de type son </span> </p> <p>La balise <span class="codeph"> &lt;search-input&gt; </span> est utile pour placer des cases à cocher et des boutons radio dans votre modèle de recherche. Si vous souhaitez ajouter des cases à cocher ou des boutons radio au <span class="codeph"> &lt;formulaire&gt; </span> dans votre modèle de recherche, utilisez <span class="codeph"> &lt;search-input...&gt; </span> à la place de <span class="codeph"> &lt;input...&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-select&gt;... &lt;/search-select&gt; </span> </p> <p> <span class="codeph"> &lt;option de recherche&gt;... &lt;/search-option&gt; </span> </p> </td> 
   <td colname="col2"> <p>Les zones de liste déroulante d’une balise <span class="codeph"> &lt;form&gt; </span> sont lancées avec une balise <span class="codeph"> &lt;select&gt; </span> et se terminent par une balise <span class="codeph"> &lt;/select&gt; </span> . Le <span class="codeph"> nom </span> du paramètre CGI associé est répertorié dans la balise <span class="codeph"> &lt;select&gt; </span> . La balise <span class="codeph"> &lt;select&gt; </span> suivante est une liste de balises <span class="codeph"> &lt;option&gt; </span> qui spécifient les valeurs à afficher dans la zone de liste. </p> <p>Les balises <span class="codeph"> &lt;search-select&gt; </span>, <span class="codeph"> &lt;/search-select&gt; </span>, <span class="codeph"> &lt;search-option&gt; </span>et <span class="codeph"> &lt;/search-option&gt;  offrent des fonctionnalités similaires à la balise  &lt;search-input&gt; . </span><span class="codeph"></span> En d’autres termes, le mot <span class="codeph"> sélectionné </span> est automatiquement ajouté à la fin de la balise <span class="codeph"> &lt;option&gt; </span> envoyée au navigateur si le <span class="codeph"> nom </span> dans la balise <span class="codeph"> &lt;search-select&gt;  est répertorié comme paramètre CGI et si la valeur  de ce paramètre CGI est répertoriée comme valeur de dans une balise de &lt;search-option&gt; particulière. </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span> Ainsi, vous pouvez automatiquement faire en sorte que le choix de la zone de liste par défaut dans le résultat de la recherche soit identique à celui de la requête active. </p> <p>Par exemple, une zone de liste type se présente comme suit : </p> <p> <code class="syntax html"> &lt;select&nbsp;name="sp_x"&nbsp;size=1&gt; 
      &lt;option&nbsp;value="any"&nbsp;selected&gt;Anywhere&lt;/option&gt; 
      &lt;option&nbsp;value="title"&gt;Title&lt;/option&gt; 
      &lt;option&nbsp;value="desc"&gt;Description&lt;/option&gt; 
      &lt;option&nbsp;value="keys"&gt;Keywords&lt;/option&gt; 
      &lt;option&nbsp;value="body"&gt;Body&lt;/option&gt; 
      &lt;option&nbsp;value="alt"&gt;Alternate&nbsp;text&lt;/option&gt; 
      &lt;option&nbsp;value="url"&gt;URL&lt;/option&gt; 
      &lt;option&nbsp;value="target"&gt;Target&lt;/option&gt; 
      &lt;/select&gt; </code> </p> <p>Le code de modèle correspondant à cette zone de liste est le suivant : </p> <p> <code class="syntax html"> &lt;search-select&nbsp;name="sp_x"&nbsp;size=1&gt; 
      &lt;search-option&nbsp;value="any"&gt;Anywhere&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="title"&gt;Title&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="desc"&gt;Description&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="keys"&gt;Keywords&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="body"&gt;Body&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="alt"&gt;Alternate&nbsp;text&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="url"&gt;URL&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="target"&gt;Target&lt;/search-option&gt; 
      &lt;/search-select&gt; </code> </p> <p>Si vous souhaitez ajouter des zones de liste au <span class="codeph"> &lt;formulaire&gt; </span> dans votre modèle de recherche, utilisez <span class="codeph"> &lt;search-select...&gt; </span> à la place de <span class="codeph"> &lt;select...&gt; </span>, <span class="codeph"> &lt;/search-select&gt;  à la place de  &lt;/select&gt; , de l'&lt;search-option...&gt; à la place du &lt;option...&gt; et du &lt;/search-option&gt; à la place du &lt;/fr option&gt;.</span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;nom_tri_par_champ="nom_champ" count="XX"&gt; ... &lt;/search-sort-by-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ces balises avancées créent un lien d’ancrage autour du code HTML entre elles. Lorsque vous cliquez sur cette ancre, une page de résultats triée sur le champ donné s’affiche. L’ <span class="codeph"> attribut facultatif </span> count spécifie le nombre de résultats à afficher sur la page de résultats. Si <span class="codeph"> count </span> est omis, le nombre utilisé sur la page active est utilisé. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Chaînes de format de date {#section_4BBDBBEF2B96414497617CD4B52D96E4}

Vous pouvez utiliser les spécifications de conversion suivantes dans les chaînes de format de date :

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Chaîne de format de date </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>%Une </p> </td> 
   <td colname="col2"> <p> Correspond à la représentation nationale du nom complet du jour de la semaine, par exemple "Lundi". Le paramètre dans <span class="uicontrol"> Linguistique </span> &gt; <span class="uicontrol"> Mots et langues </span> &gt; Langue <span class="uicontrol"> </span> détermine la représentation nationale. </p> <p>Voir <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> A propos des mots et de la langue</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%a </p> </td> 
   <td colname="col2"> <p> Correspond à la représentation nationale du nom abrégé du jour de la semaine, où l’abréviation est les trois premiers caractères, par exemple "Mon". Le paramètre dans <span class="uicontrol"> Linguistique </span> &gt; <span class="uicontrol"> Mots et langues </span> &gt; Langue <span class="uicontrol"> </span> détermine la représentation nationale. </p> <p>Voir <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> A propos des mots et de la langue</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%B </p> </td> 
   <td colname="col2"> <p> Correspond à la représentation nationale du nom complet du mois, par exemple "Juin". Le paramètre dans <span class="uicontrol"> Linguistique </span> &gt; <span class="uicontrol"> Mots et langues </span> &gt; Langue <span class="uicontrol"> </span> détermine la représentation nationale. </p> <p>Voir <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> A propos des mots et de la langue</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%b </p> </td> 
   <td colname="col2"> <p> Correspond à la représentation nationale du nom du mois abrégé, où l’abréviation est les trois premiers caractères, par exemple "Jun". Le paramètre dans <span class="uicontrol"> Linguistique </span> &gt; <span class="uicontrol"> Mots et langues </span> &gt; Langue <span class="uicontrol"> </span> détermine la représentation nationale. </p> <p>Voir <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> A propos des mots et de la langue</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%D </p> </td> 
   <td colname="col2"> <p>Équivalent à "%m/%d/%y", par exemple "25/07/13". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%d </p> </td> 
   <td colname="col2"> <p> Correspond au jour du mois en tant que nombre décimal (01-31). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%e </p> </td> 
   <td colname="col2"> <p> Correspond au jour du mois en tant que nombre décimal (1-31). Un blanc précède des chiffres uniques. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%H </p> </td> 
   <td colname="col2"> <p> Correspond à l’horloge de 24 heures sous la forme d’un nombre décimal (00-23). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%h </p> </td> 
   <td colname="col2"> <p> Correspond à la représentation nationale du nom abrégé du mois, où l’abréviation est les trois premiers caractères, par exemple "Jun" (identique à %b). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%I </p> </td> 
   <td colname="col2"> <p> Correspond à l’horloge de 12 heures sous la forme d’un nombre décimal (01-12). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%j </p> </td> 
   <td colname="col2"> <p> Correspond au jour de l’année sous forme de nombre décimal (001-366). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%k </p> </td> 
   <td colname="col2"> <p> Correspond à l’horloge (24 heures) sous la forme d’un nombre décimal (0-23). Un blanc précède des chiffres uniques. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%l </p> </td> 
   <td colname="col2"> <p> Correspond à l’horloge de 12 heures sous la forme d’un nombre décimal (1-12). Un blanc précède des chiffres uniques. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%M </p> </td> 
   <td colname="col2"> <p> Correspond à la minute sous forme de nombre décimal (00-59). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%m </p> </td> 
   <td colname="col2"> <p> Correspond au mois sous forme de nombre décimal (01-12). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%p </p> </td> 
   <td colname="col2"> <p> Correspond à la représentation nationale de "ante meridiem" ou "post meridiem" selon le cas, par exemple "PM". Le paramètre dans <span class="uicontrol"> Linguistique </span> &gt; <span class="uicontrol"> Mots et langues </span> &gt; Langue <span class="uicontrol"> </span> détermine la représentation nationale. </p> <p>Voir <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> A propos des mots et de la langue</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%R </p> </td> 
   <td colname="col2"> <p>Équivalent à "%H:%M", par exemple, "13:23". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%r </p> </td> 
   <td colname="col2"> <p>Équivalent à "%I:%M:%S %p", par exemple, "01:23:45 PM". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%S </p> </td> 
   <td colname="col2"> <p> Correspond au second nombre décimal (00-60). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%T </p> </td> 
   <td colname="col2"> <p>Équivalent à "%H:%M:%S", par exemple, "13:26:47". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%U </p> </td> 
   <td colname="col2"> <p> Correspond au numéro de semaine de l’année (dimanche comme premier jour de la semaine) sous forme de nombre décimal (00-53). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%v </p> </td> 
   <td colname="col2"> <p>Équivalent à "%e-%b-%Y", par exemple, "25-Jul-2013". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%O </p> </td> 
   <td colname="col2"> <p> Correspond à l’année avec le siècle comme nombre décimal, par exemple "2013". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%y </p> </td> 
   <td colname="col2"> <p> Correspond à l’année sans siècle comme nombre décimal (00-99). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%Z </p> </td> 
   <td colname="col2"> <p> Correspond au nom du fuseau horaire. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%% </p> </td> 
   <td colname="col2"> <p> Correspond à "%". </p> </td> 
  </tr> 
 </tbody> 
</table>

## Identifiants de langue {#section_0490DECC00E34691ADE5A9ED90A6D911}

Le tableau suivant contient les identifiants de langue pour chaque langue prise en charge. Vous pouvez utiliser ces identifiants comme valeurs pour l’attribut facultatif &quot;language&quot; dans les balises de modèle suivantes :

* `search-date` et `search-display-field`.

   Voir Balises [de chaîne de boucle](../c-appendices/c-templates.md#section_80D68334E8D04A33937A6E58ABAAA320)Résultats.

* `search-field-value-list` Voir Balises [de liste de valeurs de](../c-appendices/c-templates.md#section_D3298B5F976447DBA0032B883DCC91B1)champ.

* `search-field-value` Voir Balises [de boucle de liste de valeurs de](../c-appendices/c-templates.md#section_0717FA09F0FC449CB916883B0500A60E)champ.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Langue </p> </th> 
   <th colname="col2" class="entry"> <p>Identifiant de langue </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Bulgare (Bulgarie) </p> </td> 
   <td colname="col2"> <p> bg_BG </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinois (Chine) </p> </td> 
   <td colname="col2"> <p> zh_CN </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinois (Hong Kong) </p> </td> 
   <td colname="col2"> <p> zh_HK </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinois (Singapour) </p> </td> 
   <td colname="col2"> <p>zh_SG </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinois (Taïwan) </p> </td> 
   <td colname="col2"> <p> zh_TW </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tchèque (République tchèque) </p> </td> 
   <td colname="col2"> <p> cs_CZ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Danois (Danemark) </p> </td> 
   <td colname="col2"> <p> da_DK </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Néerlandais (Belgique) </p> </td> 
   <td colname="col2"> <p> nl_BE </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Néerlandais (Pays-Bas) </p> </td> 
   <td colname="col2"> <p> nl_NL </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Anglais (Australie) </p> </td> 
   <td colname="col2"> <p> en_AU </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Anglais (Canada) </p> </td> 
   <td colname="col2"> <p> en_CA </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Anglais (Grande-Bretagne) </p> </td> 
   <td colname="col2"> <p> en_GB </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Anglais (États-Unis) </p> </td> 
   <td colname="col2"> <p> en_US </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Français (Belgique) </p> </td> 
   <td colname="col2"> <p> fr_BE </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Français (Canada) </p> </td> 
   <td colname="col2"> <p>fr_CA </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Finnois (Finlande) </p> </td> 
   <td colname="col2"> <p> fi_FI </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Français (France) </p> </td> 
   <td colname="col2"> <p> fr_FR </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Français (Suisse) </p> </td> 
   <td colname="col2"> <p> fr_CH </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Allemand (Autriche) </p> </td> 
   <td colname="col2"> <p> de_AT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Allemand (Allemagne) </p> </td> 
   <td colname="col2"> <p> de_DE </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Allemand (Suisse) </p> </td> 
   <td colname="col2"> <p> de_CH </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Grec (Grèce) </p> </td> 
   <td colname="col2"> <p> el_GR </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Irlandais gaélique (Irlande) </p> </td> 
   <td colname="col2"> <p> ga_IE </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Italien (Italie) </p> </td> 
   <td colname="col2"> <p> it_IT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Japonais (Japon) </p> </td> 
   <td colname="col2"> <p> ja_JP </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Coréen (Corée) </p> </td> 
   <td colname="col2"> <p> ko_KR </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Norvégien (Norvège) </p> </td> 
   <td colname="col2"> <p> no_NO </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Polonais (Pologne) </p> </td> 
   <td colname="col2"> <p> pl_PL </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Portugais (Brésil) </p> </td> 
   <td colname="col2"> <p> pt_BR </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Portugais (Portugal) </p> </td> 
   <td colname="col2"> <p> pt_PT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Russe (ex-Union soviétique) </p> </td> 
   <td colname="col2"> <p> ru_SU </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Slovaque (Slovaquie) </p> </td> 
   <td colname="col2"> <p> sk_SK </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Slovaque (Slovénie) </p> </td> 
   <td colname="col2"> <p>sl_SI </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Espagnol (Mexique) </p> </td> 
   <td colname="col2"> <p> es_MX </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Espagnol (Espagne) </p> </td> 
   <td colname="col2"> <p> es_ES </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Suédois (Suède) </p> </td> 
   <td colname="col2"> <p> sv_SE </p> </td> 
  </tr> 
 </tbody> 
</table>

## Spécification de l’en-tête HTTP de type de contenu {#section_AEED823E9938448A9EDB2F286D9CFD90}

Vous pouvez spécifier l’en-tête de réponse HTTP Content-Type à l’aide de la balise suivante :

`<search-content-type-header [content="MIME-type"] [charset="charset-name"]>`

Les attributs `content` et `charset` sont facultatifs. Cette balise doit apparaître le plus tôt possible dans le modèle. Il est également recommandé de l’afficher avant `<search-html-meta-charset>` ou `<search-xml-decl>`, car cela affecte le comportement de ces balises.

Si vous ne spécifiez pas l’ `content` attribut, la valeur de `MIME-type` est définie par défaut dans **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**. Si vous spécifiez un `content` attribut, il est utilisé comme `content` attribut par défaut pour la `<search-html-meta-charset>` balise .

Si vous ne spécifiez pas l’ `charset` attribut, aucune `charset` valeur n’est écrite dans l’ `content-type` en-tête.

Si vous spécifiez `charset="1"` alors la valeur réelle de `charset-name` est la valeur du paramètre `sp_f` CGI. Si aucun paramètre `sp_f` CGI n’est envoyé avec la recherche, la valeur réelle de `charset-name` est lue à partir des paramètres de votre compte. Vous pouvez afficher ou modifier le jeu de caractères associé à votre compte sous **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]** > **[!UICONTROL Character Encoding]**.

Voir [Configuration de vos informations](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)d’utilisateur personnelles.

Vous pouvez choisir un nom de jeu de caractères spécifique en le répertoriant comme `charset` valeur, par exemple `charset="iso-8859-1"` ou `charset="Shift-JIS"`.

Si vous spécifiez un `charset` attribut, il est utilisé comme `charset` attribut par défaut pour les balises `<search-html-meta-charset>` et `<search-xml-decl>` , ainsi que comme sortie dans l’ `content-type` en-tête.

## Spécification d’un jeu de caractères dans un modèle HTML {#section_E0D1816ABB5846BEBE9C26D5980CCBE6}

Les modèles de résultats de recherche HTML par défaut spécifient le jeu de caractères associé au compte actuel au moyen de la balise suivante :

`<search-html-meta-charset [content="MIME-type"] [charset="charset-name"]>`

Les attributs de contenu et de jeu de caractères sont facultatifs. Cette balise doit apparaître dans la section HTML `<head>` du modèle. Cette balise génère la balise suivante sur la page HTML générée à partir du modèle :

`<meta http-equiv="content-type" content="MIME-type; charset=charset-name">`

Si vous ne spécifiez pas l’attribut de contenu, la valeur réelle de `MIME-type` l’une des deux valeurs par défaut est l’une des deux. Si la `<search-content-type-header>` balise a spécifié un `content` attribut, cette valeur est utilisée. Sinon, la valeur utilisée est celle définie dans l’onglet **[!UICONTROL Templates]** > **[!UICONTROL Settings]** > **[!UICONTROL Content Type]** .

Si vous ne spécifiez pas l’ `charset` attribut, la valeur réelle de `charset-name` l’attribut est définie par défaut sur l’une des deux valeurs. Si la `<search-content-type-header>` balise a spécifié un `charset` attribut, cette valeur est utilisée. Sinon, la valeur réelle de `charset-name` est lue à partir des paramètres de votre compte. Vous pouvez afficher ou modifier le jeu de caractères associé à votre compte sous **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]** > **[!UICONTROL Character Encoding]**.

Voir [Configuration de vos informations](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)d’utilisateur personnelles.

Si vous spécifiez `charset="1"` alors la valeur réelle de `charset-name` est la valeur du paramètre `sp_f` CGI. Si aucun paramètre `sp_f` CGI n’est envoyé avec la recherche, la valeur réelle de `charset-name` est soit la valeur définie dans la `<search-content-type-header>` balise si elle a été spécifiée, soit la valeur définie dans les paramètres de votre compte.

Vous pouvez spécifier un nom de jeu de caractères spécifique, comme dans `charset="charset-name"`. For example, `charset="iso-8859-1"` or `charset="Shift-JIS"`.

La `<search-html-meta-charset>` balise est facultative. Si vous le supprimez, le navigateur utilise les valeurs par défaut pour `content-type`, à savoir : `content="text/html; charset=ISO-8859-1"`. Vous pouvez également choisir de remplacer la `<search-html-meta-charset>` balise par votre propre `http-equiv` balise.

## Spécification d’un jeu de caractères dans un modèle XML {#section_17DC31CDCC104F5F8081466B41A96E9D}

Le modèle de résultat de recherche XML par défaut spécifie le jeu de caractères associé au compte actuel au moyen de la balise suivante :

`<search-xml-decl [charset="charset-name"]>`

L’ `charset` attribut est facultatif. Cette balise doit apparaître en haut du modèle, mais après n’importe quelle `<search-content-type-header>` balise. Cette balise génère la balise suivante sur le document XML généré à partir du modèle :

`<?xml version="1.0" encoding="charset-name" standalone="yes" ?>`

Si vous ne spécifiez pas le `charset`, la valeur réelle de `charset-name` la variable est définie par défaut sur l’une des deux valeurs. Si `<search-content-type-header>` vous avez spécifié un `charset` attribut, cette valeur est utilisée. Sinon, la valeur réelle de `charset-name` est lue à partir des paramètres de votre compte. Vous pouvez afficher ou modifier le jeu de caractères associé à votre compte sous **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]** > **[!UICONTROL Character Encoding]**.

Voir [Configuration de vos informations](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)d’utilisateur personnelles.

Si vous spécifiez `charset="1"` alors la valeur réelle de `charset-name` est la valeur du paramètre `sp_f` CGI. Si aucun paramètre `sp_f` CGI n’est envoyé avec la recherche, la valeur réelle de `charset-name` est soit la valeur définie dans la `<search-content-type-header>` balise si elle a été spécifiée, soit la valeur définie dans les paramètres de votre compte.

Vous pouvez spécifier un nom de jeu de caractères spécifique, comme dans `charset="charset-name"`le cas échéant. Par exemple, `charset="iso-8859-1" or charset="Shift-JIS"`.

Vous pouvez choisir de remplacer la `<search-xml-decl>` balise par votre propre `?xml` balise.

## Inclusion d’un modèle de recherche dans un autre {#section_7D1FCD3D9E2340C291E354C9720E8BC0}

Pour inclure un modèle de recherche dans un autre, utilisez la `<search-include>` balise , en définissant l’attribut de fichier sur le nom du fichier de modèle à inclure, comme dans l’exemple suivant :

`<search-include file="seo/seo_search_title.tpl" />`

Les segments de modèles de recherche SEO se trouvent dans le `seo/` sous-dossier et les modèles de recherche standard dans le `templates/` sous-dossier. Seuls les fichiers .tpl sont significatifs à inclure dans ce contexte.

## Gestion de plusieurs modèles de transport pour votre site Web {#reference_12AAB3B9F4C74C11956F1DBA95714C2F}

Vous pouvez contrôler l&#39;apparence des résultats de recherche sur votre site Web en utilisant différents modèles de transport de recherche pour chaque zone.

<!-- 

r_managing_multiple_templates.xml

 -->

Pour ce type de fonctionnalité de recherche, vous pouvez gérer vos modèles de transport dans la recherche/marchandisage de site. Vous pouvez également gérer vos modèles de transport dans Publier. Tout comme la recherche/le marchandisage sur le site, Publier vous permet de modifier, prévisualiser et publier plusieurs modèles de transport de recherche.

Pour configurer vos formulaires de recherche pour utiliser un modèle de transport spécifique (autre que le modèle par défaut), utilisez le paramètre de `sp_t` requête. Supposons, par exemple, que vous disposiez d’un modèle de recherche appelé &quot;autorisation&quot; pour la zone de vente délimitée de votre site Web. Vous utilisez le formulaire de recherche HTML standard avec le code de formulaire supplémentaire suivant :

`<input type=hidden name="sp_t" value="clearance">`

Lorsqu’un client clique sur un formulaire standard qui contient cette ligne de code, le modèle de transport de recherche &quot;d’autorisation&quot; s’affiche avec ses résultats de recherche.

Voir [Utilisation des collections dans les formulaires](../c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3)de recherche.

Voir [Utilisation de cadres avec des formulaires](../c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5).

Voir [Exemple de formulaire](../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A)de recherche avancée.