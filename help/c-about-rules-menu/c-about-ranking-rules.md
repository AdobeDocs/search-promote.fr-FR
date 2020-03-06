---
description: Vous pouvez utiliser des règles de classement pour contrôler le positionnement ou le classement relatif des résultats de recherche d’un client en fonction du contenu des balises meta contenues et des mesures Adobe Analytics associées.
seo-description: Vous pouvez utiliser des règles de classement pour contrôler le positionnement ou le classement relatif des résultats de recherche d’un client en fonction du contenu des balises meta contenues et des mesures Adobe Analytics associées.
seo-title: A propos des règles de classement
solution: Target
subtopic: Ranking Rules
title: A propos des règles de classement
topic: Rules,Site search and merchandising
uuid: 21962f9a-1d9c-442f-a6c4-5f452436c640
translation-type: tm+mt
source-git-commit: f4f69e6bdb37fb39045f8f25cffa4bf616834e54

---


# A propos des règles de classement{#about-ranking-rules}

Vous pouvez utiliser des règles de classement pour contrôler le positionnement ou le classement relatif des résultats de recherche d’un client en fonction du contenu des balises meta contenues et des mesures Adobe Analytics associées.

## Utilisation des règles de classement {#concept_F555C076759B4E81B925441CFE707397}

Vous définissez des règles de classement pour affecter le positionnement relatif des documents dans les résultats de la recherche, en fonction du contenu de chaque document. Vous pouvez baser les règles de classement sur le contenu des balises de métadonnées, les mesures Adobe Analytics (si votre compte est configuré pour fonctionner avec Adobe Analytics) ou les mesures Adobe Analytics HBX (si votre compte est configuré pour fonctionner avec Adobe Analytics HBX).

Vous pouvez définir des pages Web qui contiennent des balises meta présentant les caractéristiques souhaitées, telles qu’un certain nom ou prix de marque, ou des pages Web présentant des indicateurs de performances clés Adobe Analytics souhaitables, tels que des visionneuses uniques, pour qu’elles reçoivent un classement supérieur à celui des pages Web qui ne le sont pas. Les caractéristiques &quot;souhaitables&quot; sont facilement mises à jour en ajoutant ou en modifiant des règles de classement, puis en réindexant votre site Web.

Si plusieurs balises meta de type &quot;grade&quot; sont définies, vous pouvez créer des collections distinctes de règles à utiliser dans le calcul des différents champs de classement. Vous pouvez ajouter un groupe de règles de classement que vous pouvez ensuite affecter à l’un de vos champs Classement définis. Les groupes de règles contiennent normalement une ou plusieurs définitions de règles, mais ils peuvent également faire référence à d’autres groupes de règles. Vous pouvez donc créer un ou plusieurs groupes de règles couramment utilisées qui sont partagés lors du calcul de vos plusieurs grades.

Voir [Ajout d’un groupe](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)de règles de classement.

Une valeur de classement positive favorise les résultats de recherche vers le haut ; une valeur de classement négative dénote les résultats de recherche vers le bas des résultats de recherche. La plage normale des valeurs de classement est 1,0, ce qui correspond à la promotion maximale dans les résultats de la recherche, tandis que -1,0 est la rétrogradation maximale. Bien que vous puissiez personnaliser cette plage en modifiant le champ Classement dans les définitions de métadonnées, ce type de personnalisation est généralement inutile.

Voir [A propos des définitions](../c-about-settings-menu/c-about-metadata-menu.md#concept_AE48035C210145169BE067D396975620).

Si vous avez défini plusieurs champs de classement sous Paramètres > Métadonnées > Définitions, vous avez la possibilité de créer d’autres ensembles de règles de classement, un pour chaque champ de classement. Vous pouvez définir d’autres jeux de règles de classement sans être directement associé à un champ de classement. Cette flexibilité vous permet de créer des jeux de règles communes qui peuvent être partagées dans le calcul d’une ou de plusieurs valeurs de classement.

**Important**: Avant de pouvoir utiliser les règles de classement, vous devez exécuter plusieurs étapes de configuration du compte.

Voir [Configuration du classement](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5)

## Configuration du classement {#task_4CEBC13925B047FC95BDC217B48089C5}

Avant de pouvoir utiliser les règles de classement, vous devez effectuer plusieurs étapes de configuration du compte.

**Pour configurer le classement**

1. Choisissez l’une des options suivantes :

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Tâche </p> </th> 
      <th colname="col2" class="entry"> <p>Configuration </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Pour créer des règles de classement basées sur des balises meta </p> </td> 
      <td colname="col2"> <p> 
      <ol id="ol_28ABB980143948DFA79AC4360AAB7556"> 
      <li id="li_544075CFA0964C6F8FAF7941AAA9ECCC"> Dans le menu du produit, cliquez sur <span class="uicontrol"> Paramètres </span> &gt; <span class="uicontrol"> Métadonnées </span> &gt; <span class="uicontrol"> Définitions </span>. </li> 
      <li id="li_F237F13B89E8425080C15D3BD697652C"> Dans la page Définitions, cliquez sur <span class="uicontrol"> Ajouter un nouveau champ </span>. </li> 
      <li id="li_2A839874D71D45FEA661B3D3B8BE2A86"> Sur la page Ajouter un champ, dans le champ Nom <span class="uicontrol"> </span> du champ, saisissez 
      <userinput>
        grade 
      </userinput>; dans le champ de <span class="uicontrol"> texte Nom de la </span> balise méta, saisissez 
      <userinput>
        grade 
      </userinput>; dans la liste <span class="uicontrol"> déroulante Type de </span> données, sélectionnez <span class="uicontrol"> Classement </span>. Conservez toutes les autres options de champ telles quelles. <p>Voir le paramètre de requête <span class="codeph"> sp_sr </span> dans les paramètres CGI de recherche <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> principal </a>. </p> </li> 
      <li id="li_8E91AF4BE51A4A41ABBF9680DDE0B7CE">Cliquez sur <span class="uicontrol">Ajouter </span>. </li> 
      </ol> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Pour créer des règles de classement basées sur les mesures Adobe Analytics </p> </td> 
      <td colname="col2"> <p> 
      <ol id="ol_BE57CBC303D941778B10D855ADC93C68"> 
      <li id="li_8DF5D8F924B24ECBBD2D93C76C69D00C"> Vérifiez que vous avez configuré l’authentification Adobe Analytics à partir de la recherche/marchandisage sur le site. <p>Voir <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_8AA93F6273B747F9B4DE9E8DFBCBDC42" type="task" format="dita" scope="local"> Configuration de l’authentification des mesures Adobe Analytics </a>. </p> </li> 
      <li id="li_CF7DD073FC5A432DADBD282AA8BB9920"> Sélectionnez et ajoutez une suite de rapports disponible. <p>Voir <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_6DE17305EA7146DA8C30FF8FDF68A3C0" type="task" format="dita" scope="local"> Ajout d’une suite de rapports Adobe Analytics </a>. </p> </li> 
      <li id="li_9A63448577D04E028DF211D8715F943A"> Configurez la liste des mesures d’Adobe Analytics que vous souhaitez rendre disponible pour la création de nouvelles règles de classement. <p>Voir <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664" type="task" format="dita" scope="local"> Modification des mesures Adobe Analytics d’une suite de rapports </a>. </p> </li> 
      <li id="li_1ACA3611D9B44AC394604CD89209C966"> Chargez les mesures Adobe Analytics initiales pour les pages de votre site Web. <p>Voir <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_2F3C55189B0A4049AB2113F2291CC181" type="task" format="dita" scope="local"> Chargement des données Adobe Analytics </a>. </p> </li> 
      </ol> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Ajoutez une ou plusieurs règles de classement.

   Voir [Ajout d’une règle](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A)de classement.

1. Cliquez sur **[!UICONTROL regenerate your staged site index]** pour effectuer un réindex complet de votre site Web (à partir de **[!UICONTROL Index]** > **[!UICONTROL Full Index]**).

   Voir [Exécution d’un index complet d’un site Web en direct ou par étape...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Voir [Configuration d’un index incrémentiel d’un site Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)intermédiaire.
1. Vérifiez les valeurs de la colonne Classement dans **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]** pour vous assurer que les règles de classement ont été correctement appliquées.

## A propos du classement des documents par âge {#topic_770815CF1B2A491F83FF765871B6F1B8}

Vous pouvez classer un document HTML par âge avec une fonction de décomposition exponentielle. Le taux de décomposition est spécifié avec une constante de demi-vie choisie, la durée qui doit s’écouler avant que la valeur ne chute à la moitié de sa valeur initiale.

Le classement par âge est basé sur les deux équations suivantes :

`K = -ln(2) / H`

`RANK = e^(K * T)`

Variables `H` et `T` sont des entrées pour cette fonction : `H` est la demi-vie souhaitée et `T` l’âge du document, exprimé en secondes. `K` est la demi-vie calculée et `RANK` est la décomposition exponentielle de la valeur d’âge spécifiée. La valeur obtenue est comprise entre 0 et 1. Un document plus récent a une valeur de classement proche de 1 par rapport à un document plus ancien. En théorie, les documents ne doivent jamais atteindre la valeur 0, mais les erreurs d’arrondi peuvent entraîner la valeur 0.

## Conditions requises pour l’utilisation du classement par âge {#section_D716507D589442C6B7848892BD28F966}

* Votre compte doit déjà être configuré correctement pour le classement. S’il n’est pas configuré, voir [Configuration du classement](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5).
* Le document HTML doit comporter un champ de balise meta HTML qui représente sa date de naissance, sa date de naissance, son heure de naissance ou une autre valeur de date significative.
* La fonction intégrée spéciale, `search_get_age_rank()`spécifiée dans les pages Ajouter ou Modifier une règle de classement, est utilisée pour calculer le classement d’un document par âge. Les sections suivantes décrivent en détail l&#39;utilisation générale de la fonction de classement par âge. Vous trouverez également un exemple illustrant la fonction de classement par âge.

## Utilisation de search_get_age_grade () sur la page Ajouter une règle de classement ou Modifier une règle de classement {#section_34BC5276F2AB4419AD92872A397CA0AF}

Spécifiez `search_get_age_rank()` comme suit :

`search_get_age_rank(Birthdate#Half_Life#Default_Rank)`

* Date de naissance - La date de naissance ou la date de début du fichier doit être une chaîne de date formatée selon les formats de date du champ. Cette chaîne formatée de date doit être une référence de champ, comme dans `{field_name}`.
* Half_Life - La demi-vie est la durée qui doit s&#39;écouler avant que la valeur ne chute à la moitié de sa valeur initiale. Cette valeur est exprimée en nombre de jours et il s’agit d’un nombre entier ou à virgule flottante.
* Default_Rank : le classement par défaut est utilisé comme filet de sécurité au cas où la date de naissance n’est pas valide ou que la date est dans le futur. Vous ne pouvez pas utiliser cette valeur par défaut si le champ de métadonnées associé comporte également une valeur par défaut valide. La valeur ici est un nombre à virgule flottante ou un entier. Consultez ci-dessous les suggestions si vous rencontrez des problèmes pour savoir quelle valeur par défaut est utilisée.

Voir [Ajout d’une règle](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A)de classement.

See [Editing a ranking rule](../c-about-rules-menu/c-about-ranking-rules.md#task_5EBF55A43D6545FEA46BAE5E586FA275).

**Exemple**

Dans l’exemple suivant,

`search_get_age_rank({birthdate}#28#0.20)`

la date contenue dans le `birthdate` champ du document est transmise en tant qu’horodatage. La demi-vie est de 28 jours. La valeur de classement par défaut est 0,20 si la date n’est pas valide.

Voir le tableau des options dans [Ajout d’une règle](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A)de classement.

Dans la section Valeurs/Classement de la page Ajouter une règle de classement ou Modifier la règle de classement, vous ne pouvez utiliser que `search_get_age_rank` des règles personnalisées. Par conséquent, veillez à choisir **Personnalisé** dans la liste déroulante Valeurs/Classements. Lorsque la règle utilise la fonction de classement par âge, aucun espace n’est autorisé dans la partie valeurs de la règle. Assurez-vous qu’il n’y a aucun espace entre les arguments de fonction ou entre eux. Et il n&#39;y a pas d&#39;espaces entre des opérateurs mathématiques ou conditionnels.

Vous trouverez ci-dessous un exemple de règle de valeurs/classements : une règle associée à un champ de texte :

`regexp .* search_get_age_rank({other_field}#365#0.20)`

Cet exemple suppose que `other_field` contient une valeur de date. Si ce champ n’est pas lui-même un champ de type de date, cette valeur est interprétée à l’aide des formats de date associés au champ Date prédéfini. Sinon, les formats de date de ce champ sont utilisés. Cette entrée de valeurs/classements est utilisée chaque fois que le champ du document, que la source de données de la règle identifie, est non vide et que la valeur renvoyée par la fonction (de 0 à 1) est le rang affecté.

Pour une règle associée à un champ numérique, en particulier un champ Date :

`9999999999 search_get_age_rank({other_field}#365#0.20)`

Au fur et à mesure que chaque document est traité, la valeur dans `other_field` est convertie en formulaire &quot;époque&quot; Unix, en utilisant les définitions de format de date du champ. Cette valeur est utilisée dans l’ `search_get_age_rank()` appel. Chaque valeur &quot;époque&quot; étant inférieure à 999999999999 (pour l’instant au moins), la règle fournit simplement la valeur renvoyée par la fonction (de 0 à 1) comme rang.

Dans les deux exemples précédents, il est typique que la source de données de la règle soit le même champ que celui utilisé dans la `search_get_age_rank()` fonction - `other_field` dans ce cas.

## Exemple d’intégration du classement par âge dans les règles de classement {#section_A86D909687CC45E19D4EA7A4A9283F28}

Voici un exemple d’intégration du classement par âge dans les règles de classement. L’exemple montre également les résultats bruts de la fonction de classement par âge et les résultats des règles de classement. L’exemple suppose ce qui suit :

* Les pages Web analysées comportent une balise meta HTML nommée &quot;date de naissance&quot;. Le contenu de cette balise est un horodatage lié au document.
* Les définitions de métadonnées comportent un champ de balise de métadonnées défini pour la balise de date de naissance. Ce champ est défini sur &quot;date&quot;.

**Règles de classement**

Voir [Ajout d’un nouveau champ](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)de balise meta.

Vous ajoutez maintenant une nouvelle règle de classement. La règle est définie pour utiliser le champ &quot;date de naissance&quot; sur le document. Une nouvelle règle de classement est ajoutée avec le jeu de propriétés suivant :

* Type de source de données : Méta-balise
* Nom de la source de données : date de naissance
* Poids/Conditions : 10 - Importance maximale
* Valeurs/grades : 9999999999 search_get_age_grade({date de naissance}#14#0.10)
* Classement par défaut : -1

La règle fait plusieurs choses. Le poids de la règle est défini sur 10. La valeur de rang est simplement le résultat de la fonction de rang d’âge, une valeur comprise entre 0 et 1. Vous ne pouvez pas utiliser d’espaces avec `search_get_age_rank()`. Notez également que le champ &quot;date de naissance&quot; est entouré d’accolades. Enfin, lorsque vous enregistrez cette règle, les virgules de la définition Valeurs/Classement sont remplacées par `#` des caractères ; ce comportement est normal.

**Affichage des résultats**

Utilisez la fonction Vue des données pour afficher rapidement les résultats de la fonction de classement par âge. Ajoutez les champs de métadonnées appropriés. Dans cet exemple, `age_val` et `myrank` sont les deux champs de métadonnées à ajouter à la vue des données. Le `myrank` champ montre comment le classement par âge affecte les valeurs de classement. Le `age_val` champ affiche la sortie brute de la fonction de désintégration exponentielle pour ce document.

## Valeurs par défaut {#section_CB109EF78F914E92955D512ACFC3310E}

Voici les trois valeurs par défaut impliquées dans la fonction `search_get_age_rank()`:

* Valeur par défaut que vous pouvez entrer dans la `search_get_age_rank()` fonction elle-même.
* Valeur de classement par défaut de la règle Classement.
* Valeur par défaut de la définition des métadonnées.

Selon l’endroit où l’échec se produit, vous pouvez obtenir différentes valeurs par défaut.

Par exemple, la valeur par défaut de la définition des métadonnées ne doit jamais se produire si le classement et le filtrage sont correctement implémentés. Cette valeur par défaut est la valeur de dernier recours lorsqu’il n’existe aucun contenu valide ou connu pour ce champ de métadonnées. La valeur par défaut des règles de classement peut s’afficher lorsque `search_get_age_rank()` vous référencez sa propre balise associée et que la balise est absente du document. Dans ce cas, cette règle renvoie directement à la valeur par défaut de la règle. Si la fonction de classement par âge fait référence à la balise d’une autre règle de classement, il est possible que la valeur par défaut transmise à cette fonction de classement par âge soit utilisée si la balise référencée est absente ou non valide.

## Ajout d’une règle de classement {#task_A132789FD4E5423DAD090DCDA7311E8A}

Vous pouvez ajouter [!DNL Ranking Rules] pour affecter le positionnement relatif des pages Web dans les résultats de la recherche, en fonction du contenu de chaque page Web.

Voir [Configuration du classement](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5).

**Pour ajouter une règle de classement**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. (Facultatif) Si vous avez créé un groupe de règles et ajouté des règles au groupe, sur la [!DNL Define Ranking Rules] page, dans la liste **[!UICONTROL Select Rule Group]** déroulante, sélectionnez un groupe de règles contenant les règles à modifier.

   Voir [Ajout d’un groupe](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)de règles de classement.
1. Sur la [!DNL Define Ranking Rules] page, cliquez **[!UICONTROL Add Rule]** pour ajouter une nouvelle règle de classement ou pour ajouter une référence à un jeu de règles.
1. Sur la [!DNL Add Ranking Rule] page, définissez les options de votre choix. Les champs signalés par un astérisque (*) sont obligatoires.

   Le type de source de données que vous sélectionnez affecte les choix disponibles dans la liste [!DNL Data Source Name] déroulante. Si, par exemple, vous avez sélectionné **[!UICONTROL Meta Tag]** le type de source de données, le nom de la source de données fait référence au nom d’une balise meta sur les pages de votre site Web. Si vous avez sélectionné **[!UICONTROL Adobe Analytics Metric (Number)]**, le nom de la source de données fait référence à l’un des noms de mesure Adobe Analytics que vous avez sélectionnés dans une suite de rapports, comme indiqué sur la **[!UICONTROL Edit Adobe Analytics Metrics]** page de la recherche/marchandisage de site.

   Voir [Modification des mesures Adobe Analytics d’une suite](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664)de rapports.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Type de source de données </p> </td> 
      <td colname="col2"> <p>Détermine les caractéristiques de la source de données utilisée comme entrée pour cette règle de classement. </p> <p>Les types de source de données que vous pouvez sélectionner incluent les éléments suivants : 
      <ul id="ul_B0A97BF0E314495985F44A642C86918D"> 
      <li id="li_4D8BDE32853540809AE78FF5FF5677A1"> <span class="uicontrol"> Méta-balise </span> <p> Base cette règle sur les données numériques ou textuelles stockées dans une balise meta nommée sur les pages de votre site Web. </p> </li> 
      <li id="li_4976C31D67254C7F81D554EC49DDBB40"> <span class="uicontrol"> Mesure Adobe Analytics (nombre) </span> <p>Base cette règle sur une mesure numérique Adobe Analytics associée aux pages de votre site. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nom de la source de données </p> </td> 
      <td colname="col2"> <p>Si vous sélectionnez <span class="uicontrol"> Méta-balise </span> comme type de source de données, il s’agit du nom d’une balise meta qui se trouve dans les pages de votre site Web. Les noms du menu déroulant proviennent de la liste des valeurs de métadonnées définies qui ont été configurées dans Paramètres &gt; Métadonnées &gt; Définitions. </p> <p>Voir <a scope="local" href="../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5" type="task" format="dita"> Ajout d’un nouveau champ de balise meta </a>. </p> <p>Si vous sélectionnez Mesure Adobe Analytics (nombre) comme type de source de données, il s’agit du nom d’une mesure Adobe Analytics. Les noms figurant dans le menu déroulant proviennent de la liste des mesures Adobe Analytics disponibles définies et configurées dans Paramètres &gt; Adobe Analytics &gt; Mesures &gt; Modifier. </p> <p>Voir <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664" type="task" format="dita" scope="local"> Modification des mesures Adobe Analytics d’une suite de rapports </a>. </p> <p>Si le nom de la mesure Adobe Analytics que vous avez sélectionnée n’est pas déjà défini dans <span class="uicontrol"> Paramètres </span> &gt; <span class="uicontrol"> Métadonnées </span> &gt; <span class="uicontrol"> Définitions </span>, un champ de texte et un bouton Ajouter s’affichent. Entrez le nom du champ de métadonnées (le nom du champ de métadonnées ne doit pas dépasser 20 caractères), puis cliquez sur <span class="uicontrol"> Ajouter </span>. </p> <p>Lorsque des pages sont rencontrées avec plusieurs clés Adobe Analytics, comme avec une page de produit affichant plusieurs produits, le schéma composite indique comment gérer les multiples valeurs de mesure Adobe Analytics associées à cette page. Sélectionnez l’une des options suivantes : </p> <p> 
      <ul id="ul_D6E51748BB3949048A37C1895F2C0A58"> 
      <li id="li_04F00F382A264C96A519B0D975E25E94"> <span class="uicontrol"> Somme </span> <p>Renvoie la somme des valeurs de mesure. </p> </li> 
      <li id="li_FA44219B663F4CC197BD3A094EB84396"> <span class="uicontrol"> Moyenne </span> <p>Renvoie la moyenne des valeurs (somme divisée par le nombre de valeurs). </p> </li> 
      <li id="li_F0EAAE1EA1754FFEB30F611E5550097B"> <span class="uicontrol"> Maximum </span> <p>Renvoie la plus grande des valeurs. </p> </li> 
      <li id="li_38E3E3F3D9AF4C57803B84B60223FB9D"> <span class="uicontrol"> Tout d’abord </span> <p>Renvoie la valeur correspondant à la première clé. </p> </li> 
      <li id="li_4AEE470CE6BB4D899E975915EC226624"> <span class="uicontrol"> Dernière </span> <p>Renvoie la valeur correspondant à la dernière clé. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Poids/Conditions </p> </td> 
      <td colname="col2"> <p>Contient soit un nombre simple de poids de règle unique, soit une liste combinée de nombres de poids de règle et de conditions de test. </p> <p>Un nombre de poids de règle est une valeur comprise entre 1 et 10 qui indique l’importance de cette règle de classement par rapport aux autres règles de classement pour déterminer le rang global d’un document. Un poids de règle plus élevé indique une importance plus élevée. Un poids de zéro (0) ignore la règle. </p> <p>Choisissez <span class="uicontrol"> Personnalisé </span> dans la liste déroulante pour personnaliser l’épaisseur des règles pour diverses pages en définissant une liste de paires poids/conditions de test. Les conditions de test sont des fragments de Perl utilisés pour tester les valeurs de source de données ou des variables globales définies dans votre script de filtre personnalisé (par exemple, prix, marque, saison ou pages vues, comme dans l’exemple suivant). Si une condition de test est évaluée sur "true", la valeur d’épaisseur de règle associée est appliquée. Si une condition de test est évaluée sur "false", la condition suivante dans la liste est évaluée. <code> 0&nbsp;({price}&nbsp;&gt;&nbsp;50.00)&nbsp;&amp;&amp;&nbsp;({brand}=~/Kuhl/)5&nbsp;{season}&nbsp;=~&nbsp;/Fall/10&nbsp;{pageviews}&nbsp;&gt;&nbsp;1000005 </code>Dans l’exemple de condition/poids créé personnalisé ci-dessus, le poids de règle 0 est appliqué si la première condition de test est évaluée sur "true". Autrement dit, le prix contient une valeur supérieure à 50 et la marque contient "Kuhl"). Si la première condition de test est évaluée sur "false", la condition suivante est évaluée. Si aucune des conditions précédentes n’est remplie, le poids de la règle 5 est affecté. </p> <p>Vous devez toujours indiquer un poids de règle sans condition à la fin de la liste. Si vous ne le faites pas, la règle obtient un poids de 0 dans le cas où aucun des tests de condition n’évalue "true". </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Valeurs/Classements </p> </td> 
      <td colname="col2"> <p>Se compose de l’une des fonctions de classement intégrées ou du contenu de source de données possible avec les grades souhaités. </p> <p>Si vous sélectionnez <span class="uicontrol"> Mesure Adobe Analytics (nombre) </span> comme type de source de données, une liste déroulante s’affiche avec les options suivantes : 
      <ul id="ul_104906B6AA8547BAB6979AA37C4FAB90"> 
      <li id="li_7656A2855A054DB8B64E90FE501517AA"> <span class="uicontrol"> Classement automatique par ordre (par défaut) </span> <p>Calcule un rang basé sur la position relative du document, selon sa mesure Adobe Analytics. Par exemple, plus la position du document est proche du document de premier rang, plus son rang est élevé. </p> </li> 
      <li id="li_1A7D60EA6965434AA6D39B215C158306"> <span class="uicontrol"> Classement automatique par valeur </span> <p>Calcule un classement en fonction de la valeur relative du document, conformément à sa mesure Adobe Analytics. Par exemple, plus la valeur du document est proche de la valeur du document de premier rang, plus son rang est élevé. </p> </li> 
      <li id="li_457DE44D6ADA40619DC77220BF12318E"> <span class="uicontrol"> Personnalisé </span> <p>Spécifie des paramètres personnalisés. Par exemple, une source de données portant le nom de "marque" peut contenir le nom de marque d’un produit particulier. Vous pouvez indiquer l’importance relative de chaque marque en l’répertoriant avec son rang. </p> </li> 
      </ul> </p> <p>Les valeurs de classement renvoyées par les calculs de classement automatique se situent dans la plage 0,0 (plus basse) à 1,0 (plus élevée). Ils ne sont pas ajustés selon les plages définies pour le champ Classement sous Paramètres &gt; Métadonnées &gt; Définitions. </p> <p>Dans l’exemple suivant, si la source de données de la marque d’un résultat de recherche donné correspond exactement à "DKNY", le rang appliqué pour ce résultat est 0,5. Dans le cas contraire, si la marque est "Levis", le classement appliqué est de 0,1. Le contenu de la source de données doit correspondre à la valeur définie. En d’autres termes, si le contenu de la source de données est "Levis Corp.", il ne correspondra pas à la valeur "Levis". La casse est ignorée, de sorte que "DKNY" correspond à "dkny" et "Dkny". <code> DKNY&nbsp;0.5 Levis&nbsp;0.1 Lee&nbsp;0.2 </code> </p> <p>En tant qu’option plus avancée, vous pouvez spécifier des valeurs sous forme d’expressions régulières. Supposons, par exemple, que certaines pages de votre site contiennent la valeur de la marque "Levis" et que d’autres pages contiennent la valeur de la marque "Levis jeans". Vous pouvez utiliser une expression régulière spécifiée avec le mot-clé 
      <userinput>
        regexp 
      </userinput>. </p> <p>Voir <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Expressions régulières </a>. </p> <p>Dans l’exemple suivant, un document de résultat de recherche contenant le contenu de la marque "jeans Levis" a un rang de 0,1. Comme pour la comparaison standard, la casse est ignorée pour les expressions régulières. <code> DKNY&nbsp;0.5 regexp&nbsp;Levis.*&nbsp;0.1 Lee&nbsp;0.2 </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Classement par défaut </p> </td> 
      <td colname="col2"> <p> Indique le rang à appliquer aux documents de résultats de recherche qui ne correspondent à aucune des valeurs spécifiées. Dans l’exemple ci-dessus, la valeur de classement par défaut est affectée à un document de résultats de recherche avec une source de données de "marque" contenant "l’écart", car "l’écart" ne correspond à aucune des valeurs définies. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Remarques </p> </td> 
      <td colname="col2"> <p>Ajoutez des informations relatives à la définition de règle de classement ou à la définition de groupe de règles que vous avez créée. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   La plage des valeurs de classement valides est normalement comprise entre -1,0 et 1,0, comme dans l’exemple suivant :

   * `-1.0` est &quot;Classement minimum (afficher moins dans les résultats de la recherche)&quot;.
   * `0.0` est &quot;Classement neutre (ne changez pas l’ordre des résultats de recherche)&quot;.
   * `1.0` est &quot;Nombre maximal (plus élevé dans les résultats de la recherche)&quot;.
   Les grades définis doivent se trouver dans la même plage pour chaque règle. Les plages de classement doivent également correspondre aux plages définies pour le champ Classement sous **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.

   Voir [Ajout d’un nouveau champ](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)de balise meta.

   Voir aussi [Modification d’une règle](../c-about-rules-menu/c-about-ranking-rules.md#task_5EBF55A43D6545FEA46BAE5E586FA275)de classement.
1. Cliquez sur **[!UICONTROL Add]**.
1. Pour prévisualiser les résultats de l’ajout de règles, cliquez sur **[!UICONTROL regenerate your staged site index]** pour recréer l’index de votre site Web intermédiaire.

   Voir [Exécution d’un index complet d’un site Web en direct ou par étape...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Voir [Exécution d’un index incrémentiel d’un site Web en direct ou d’un site Web intermédiaire...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Modification d’une règle de classement {#task_5EBF55A43D6545FEA46BAE5E586FA275}

Vous pouvez modifier une règle de classement existante que vous avez déjà ajoutée.

Voir [Configuration du classement](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5).

**Pour modifier une règle de classement**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. (Facultatif) Si vous avez créé un groupe de règles et ajouté des règles au groupe, sur la **[!UICONTROL Define Ranking Rules]** page, dans la liste **[!UICONTROL Select Rule Group]** déroulante, sélectionnez un groupe de règles contenant les règles à modifier.

   Voir [Ajout d’un groupe](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)de règles de classement.
1. Dans le tableau, sous l’en-tête de **[!UICONTROL Actions]** colonne, cliquez **[!UICONTROL Edit]** sur le nom de la source de données à modifier.
1. Sur la [!DNL Edit Ranking Rule] page, définissez les options de votre choix. Les champs signalés par un astérisque (*) sont obligatoires.

   Voir le tableau des options sous [Ajout d’une règle](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A)de classement.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. Reconstruisez l’index de votre site Web intermédiaire pour prévisualiser les résultats de la modification de la règle.

   Voir [Exécution d’un index complet d’un site Web en direct ou par étape...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Voir [Exécution d’un index incrémentiel d’un site Web en direct ou d’un site Web intermédiaire...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Suppression d’une règle de classement {#task_742A3BCC2A6E4164BE84CC7408807EBB}

Vous pouvez supprimer les règles de classement que vous n’avez plus besoin d’utiliser.

Voir [Configuration du classement](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5).

Voir [Ajout d’un groupe](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)de règles de classement.

**Pour supprimer une règle de classement**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. (Facultatif) Si vous avez créé un groupe de règles et ajouté des règles au groupe, sur la [!DNL Define Ranking Rules] page, dans la liste **[!UICONTROL Select Rule Group]** déroulante, sélectionnez un groupe de règles qui contient les règles à supprimer.
1. Dans le tableau, sous l’en-tête de **[!UICONTROL Actions]** colonne, cliquez **[!UICONTROL Delete]** sur le nom de la source de données à modifier.
1. Sur la [!DNL Delete Ranking Rule] page, cliquez sur **[!UICONTROL Delete]**.

   Vous êtes renvoyé à la [!DNL Define Ranking Rules] page.
1. Reconstruisez l’index de votre site Web intermédiaire pour prévisualiser les résultats de la suppression de règle.

   Voir [Exécution d’un index complet d’un site Web en direct ou par étape...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Voir [Exécution d’un index incrémentiel d’un site Web en direct ou d’un site Web intermédiaire...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Ajout d’un groupe de règles de classement {#task_B65081B3CC9E4330A7FEE77B7BCD36C8}

Si vous avez défini plusieurs balises meta de type &quot;grade&quot;, vous pouvez créer des collections distinctes de règles à utiliser dans le calcul des différents champs de classement. Vous pouvez ajouter un groupe de règles de classement que vous pouvez ensuite affecter à l’un de vos champs Classement définis.

Les groupes de règles contiennent généralement une ou plusieurs règles que vous avez ajoutées. Toutefois, les groupes de règles peuvent également faire référence à d’autres groupes de règles. Par exemple, vous pouvez créer un ou plusieurs groupes de règles, puis ajouter des règles couramment utilisées à chacun d’eux. Ces règles sont ensuite partagées lors du calcul de vos grades multiples.

Voir [Modification d’un groupe](../c-about-rules-menu/c-about-ranking-rules.md#task_D3EC0437E47144BC9E754FEF99C725E5)de règles de classement.

Voir [Suppression d’un groupe](../c-about-rules-menu/c-about-ranking-rules.md#task_BE5BE01F377843BEA9846E094A07F2EA)de règles de classement.

Voir [Vérification du classement des groupes](../c-about-rules-menu/c-about-ranking-rules.md#task_5694459D050C4254A25186038CD66B6E)de règles.

**Pour ajouter un groupe de règles de classement**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. Sur la [!DNL Define Ranking Rules] page, à droite de la liste **[!UICONTROL Select Rule Group]** déroulante, cliquez sur **[!UICONTROL Add]**.
1. Sur la [!DNL Add Ranking Rule Group] page, dans le **[!UICONTROL Rule Group Name]** champ, saisissez un nom unique pour le nouveau groupe de règles.
1. Dans la liste **[!UICONTROL Rank Field Name]** déroulante, sélectionnez le nom du champ de métadonnées de classement à associer au nouveau groupe de règles. Sélectionnez **[!UICONTROL None]** si vous ne souhaitez pas affecter de rang.

   La liste des noms de champ de classement provient des définitions de métadonnées ajoutées dans **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.

   Voir le tableau des options dans [Ajout d’un nouveau champ](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)de balise meta.
1. Cliquez sur **[!UICONTROL Add]**.
1. Reconstruisez l’index de votre site Web intermédiaire pour prévisualiser les résultats de l’ajout de règles.

   Voir [Exécution d’un index complet d’un site Web en direct ou par étape...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Voir [Exécution d’un index incrémentiel d’un site Web en direct ou d’un site Web intermédiaire...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Modification d’un groupe de règles de classement {#task_D3EC0437E47144BC9E754FEF99C725E5}

Vous pouvez modifier les paramètres d’un groupe de règles de classement existant.

Voir [Ajout d’un groupe](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)de règles de classement.

**Pour modifier un groupe de règles de classement**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. Sur la [!DNL Define Ranking Rules] page, à droite de la liste **[!UICONTROL Select Rule Group]** déroulante, cliquez sur **[!UICONTROL Edit]**.
1. Sur la [!DNL Edit Ranking Rule Group] page, dans le **[!UICONTROL Rule Group Name]** champ, saisissez un nom unique pour le groupe de règles.
1. Dans la liste **[!UICONTROL Rank Field Name]** déroulante, sélectionnez le nom du champ de métadonnées de classement à associer au groupe de règles. Sélectionnez **[!UICONTROL None]** si vous ne souhaitez pas affecter de rang.

   La liste des noms de champ de classement provient des définitions de métadonnées ajoutées dans **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.

   Voir le tableau des options dans [Ajout d’un nouveau champ](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)de balise meta.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. Reconstruisez l’index de votre site Web intermédiaire pour prévisualiser les résultats de l’ajout de règles.

   Voir [Exécution d’un index complet d’un site Web en direct ou par étape...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Voir [Exécution d’un index incrémentiel d’un site Web en direct ou d’un site Web intermédiaire...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Suppression d’un groupe de règles de classement {#task_BE5BE01F377843BEA9846E094A07F2EA}

Vous pouvez supprimer un groupe de règles de classement dont vous n’avez plus besoin ou que vous n’utilisez plus. Lorsque vous supprimez un groupe, toutes les règles qui ont été ajoutées au groupe sont également supprimées. Vous ne pouvez pas supprimer le groupe &quot;Règles de classement&quot; par défaut.

Le contenu des groupes de règles contenus dans le groupe de suppression n&#39;est pas supprimé. seules les références à ces groupes sont supprimées.

Veillez à réindexer votre site Web afin que le changement soit correctement reflété dans les résultats de la recherche.

Voir [Ajout d’un groupe](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)de règles de classement.

**Pour supprimer un groupe de règles de classement**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. Sur la [!DNL Define Ranking Rules] page, dans la liste **[!UICONTROL Select Rule Group]** déroulante, sélectionnez un groupe à supprimer.
1. À droite de la liste **[!UICONTROL Select Rule Group]** déroulante, cliquez sur **[!UICONTROL Delete]**.
1. Sur la [!DNL Delete Ranking Rule Group] page, cliquez sur **[!UICONTROL Delete]**.
1. Reconstruisez l’index de votre site Web intermédiaire pour prévisualiser les résultats de l’ajout de règles.

   Voir [Exécution d’un index complet d’un site Web en direct ou par étape...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Voir [Exécution d’un index incrémentiel d’un site Web en direct ou d’un site Web intermédiaire...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Vérification des groupes de règles de classement {#task_5694459D050C4254A25186038CD66B6E}

Vous pouvez utiliser l’Aperçu des groupes de règles de classement pour afficher chaque groupe Nom du champ de classement, source de données associée et pondération.

Voir [Ajout d’un groupe](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)de règles de classement.

**Pour consulter les groupes de règles de classement**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. Sur la [!DNL Define Ranking Rules] page, à droite de la liste **[!UICONTROL Select Rule Group]** déroulante, cliquez sur **[!UICONTROL Overview]**.
1. Sur la [!DNL Ranking Rule Groups Overview] page, cliquez **[!UICONTROL Close]** pour revenir à la [!DNL Define Ranking Rules] page.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Test des règles de classement {#task_56F64EE7ED5B42E481F0990A9DD98ADB}

Vous pouvez fournir une URL appropriée pour tester les définitions de règle de classement que vous avez configurées. Les mesures utilisées dans les calculs sont affichées, ainsi que la valeur de classement calculée.

Voir [A propos des règles de classement](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397).

**Pour tester les règles de classement**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. Sur la [!DNL Define Ranking Rules] page, dans la **[!UICONTROL Test URL]** zone, saisissez l’URL d’une page Web se trouvant sur votre site Web.
1. Cliquez sur **[!UICONTROL Test]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Ajustement du poids associé aux règles de classement {#task_3CB6FC92A66F4D99874A42D55825DB64}

Vous pouvez modifier les contributions relatives de vos règles de classement individuelles, ainsi que la contribution du classement aux résultats de recherche finale.

Lorsque le classement n’est pas défini, les résultats de la recherche sont définis à 100 % sur le **[!UICONTROL Natural Relevance]** côté de la barre de curseur Règles et pertinence de la **[!UICONTROL Adjust Ranking Weights]** page. Cet équilibre signifie simplement que les résultats de la recherche sont classés uniquement en fonction des termes de recherche.

Lorsque le classement est défini, une valeur Pertinence est affectée au champ de métadonnées Classement associé, allant de 1 à 10. Une valeur de 1 signifie que le classement calculé représente 10 % de l’ordre des résultats de recherche et que la Pertinence naturelle représente les 90 % restants.

Si plusieurs règles sont définies dans un groupe de règles, la valeur Poids de chaque règle détermine la contribution du résultat de cette règle au classement calculé total. Supposons, par exemple, que vous ayez une pertinence naturelle de 80 %, ce qui signifie que la pertinence du champ Classement associé est 2. Vous avez également défini deux règles : l&#39;une avec un poids de 3, l&#39;autre avec un poids de 7. Dans ce cas, la contribution de la première règle au résultat final est de 6 % ((3 / (3+7)) * 20 %). La contribution de la deuxième règle au résultat final est de 14 % ((7 / (3+7)) * 20 %).

**Pour ajuster le poids associé aux règles de classement**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Adjust Weights]**.
1. Sur la [!DNL Adjust Ranking Weights] page, dans la liste **[!UICONTROL Select Rule Group]** déroulante, sélectionnez un groupe dont vous souhaitez ajuster les pondérations de classement.
1. Faites glisser les curseurs pour modifier les valeurs de contribution correspondantes.

   Le graphique circulaire reflète vos modifications sous forme graphique.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. Reconstruisez l’index de votre site Web intermédiaire pour prévisualiser les résultats de l’ajout de règles.

   Voir [Exécution d’un index complet d’un site Web en direct ou par étape...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Voir [Exécution d’un index incrémentiel d’un site Web en direct ou d’un site Web intermédiaire...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).