# Atelier IIIF DHNord2020

Support de l'atelier *"Adopter et utiliser les standards IIIF pour vos corpus d'images numériques"*. Conférence [#DHNord2020](https://www.meshs.fr/page/dhnord2020fr) (MESHS, Lille), Mercredi 18 novembre 2020.

Proposé et animé par **Régis Robineau** (coordinateur technique de Biblissima) et **Johann Holland** (TGIR Huma-Num).

------

**Documents :**

- Support de présentation (matin : *Introduction à IIIF*) : <url_pdf>

**Pré-requis techniques :**

- Installer une extension à votre navigateur permettant d'afficher de façon lisible des documents JSON : JSONView pour [Chrome](https://chrome.google.com/webstore/detail/jsonview/chklaanhfefbnpoihckbnefhakgolnmc) ou pour [Firefox](https://addons.mozilla.org/fr/firefox/addon/jsonview/), JSON Peep pour [Safari](https://apps.apple.com/us/app/json-peep-for-safari/id1458969831?mt=12).
- Disposer de préférence d'un éditeur de code, même basique, mais un simple éditeur de texte suffit.

------

**Sommaire :**

- [Ressources utiles en histoire de l'art proposant IIIF](#ressources-utiles-en-histoire-de-l-art-proposant-iiif)
  - [Musées](#musées)
  - [Portails et bibliothèques numériques](#portails-et-bibliothèques-numériques)
- [Exercices](#exercices)
  - Exercice 1 : prendre en main Mirador 3
  - Exercice 2 : Annoter un objet avec SimpleAnnotationServer (SAS)
  - Exercice 3 : créer/éditer un Manifeste avec le Manifest Editor
  - [Bonus](#bonus)

------

## Ressources utiles en histoire de l'art proposant IIIF

### Musées

- [Art Gallery of Ontario](https://ago.ca/collection/browse) (exemple : https://ago.ca/mirador/compare?objects=5997,6275)
- [Belvedere](https://sammlung.belvedere.at/) (exemple : https://sammlung.belvedere.at/objects/6289/der-koch-le-pere-paul)
- [Germanisches Nationalmuseum - GMN](https://www.gnm.de/en/collections/collections/) (exemple : https://tafelmalerei.gnm.de/wisski/navigate/161/view)
- [Harvard Art Museums](https://www.harvardartmuseums.org/collections) (exemple : https://hvrd.art/o/296313)
- [J. Paul Getty Museum](http://www.getty.edu/art/collection/) (exemple : https://www.getty.edu/art/collection/objects/144/vincent-van-gogh-portrait-of-joseph-roulin-dutch-1888/)
- [National Gallery of Art - USA](https://www.nga.gov/collection.html) (exemple : https://www.nga.gov/collection/art-object-page.95419.html)
- [Princeton Art Museum](https://artmuseum.princeton.edu/collections/explore) (exemple : https://artmuseum.princeton.edu/collections/objects/22783)
- [Smithsonian Institution](https://collections.si.edu/search/results.htm?q=&iiif.enabled=true) (exemple : http://n2t.net/ark:/65665/sm489c1c193-694a-4012-8517-03ae07c89191)
- [SMK](https://open.smk.dk/en/) (exemple : https://open.smk.dk/en/artwork/image/KMSsp292)
- [The Royal Collection Trust](https://albert.rct.uk) (exemple : https://albert.rct.uk/collections/raphael-collection/vatican-frescoes/raphael-collection-portfolio-26)
- [The Frick Collection](https://www.frick.org/art) (exemple : https://collections.frick.org/objects/265/antwerp-van-goyen-looking-out-for-a-subject)
- [The Huntington](https://emuseum.huntington.org/collections) (exemple : https://emuseum.huntington.org/objects/12176/santuarioleon)
- [The Leiden Collection](https://www.theleidencollection.com/) (exemple : https://www.theleidencollection.com/viewer/satyrs-nymphs-putti-and-leopards-in-a-landscape/)
- [Yale Center for British Art](https://collections.britishart.yale.edu/) (exemple : https://collections.britishart.yale.edu/catalog/tms:1153)
	

### Portails et bibliothèques numériques

- [Bibliotheca Hertziana, Max-Planck-Institut für Kunstgeschichte, Rom · Fotothek](https://foto.biblhertz.it/exist/foto/search.html) (exemple : https://foto.biblhertz.it/exist/foto/object.xql?id=08051840,T,001)

- [HeidICON](https://heidicon.ub.uni-heidelberg.de/search) (exemple : https://heidicon.ub.uni-heidelberg.de/detail/762656)

- [INHA](https://bibliotheque-numerique.inha.fr) (exemple : https://bibliotheque-numerique.inha.fr/collection/item/5786-le-dome-a-milan)

- [Qatar Digital Library](https://www.qdl.qa/en/search/site/?f%255B0%255D=document_source%3Aarchive_source) (exemple : https://www.qdl.qa/en/archive/81055/vdc_100027090276.0x000004)
	

### **Exemples d'URL de Manifestes IIIF**

```
https://data.artmuseum.princeton.edu/iiif/objects/22783
https://www.theleidencollection.com/iiif/presentation/v2/2372/manifest/
https://www.nga.gov/api/v1/iiif/presentation/manifest.json?cultObj:id=95419
https://api.smk.dk/api/v1/iiif/manifest/?id=KMSsp292
https://foto.biblhertz.it/exist/foto/bhpd43644/manifest.json
https://manifests.britishart.yale.edu/manifest/7237
https://iiif.harvardartmuseums.org/manifests/object/296313
https://iiif.harvardartmuseums.org/manifests/object/170874
https://data.getty.edu/museum/api/iiif/144/manifest.json
https://data.getty.edu/museum/api/iiif/9421/manifest.json
https://www.nga.gov/api/v1/iiif/presentation/manifest.json?cultObj:id=52450
https://heidicon.ub.uni-heidelberg.de/manifest/iiif/1139791/manifest.json
https://iiif.bodleian.ox.ac.uk/iiif/manifest/faeff7fb-f8a7-44b5-95ed-cff9a9ffd198.json
https://www.e-codices.unifr.ch/metadata/iiif/bbb-0318/manifest.json
```

## Exercices

### Exercice 1 : prendre en main Mirador 3

Mirador est un visualiseur d'images configurable, extensible et facile à intégrer, qui permet d'annoter et de comparer des images provenant de différents entrepôts IIIF. Plus d'informations sur [projectmirador.org](https://projectmirador.org/).

**Instance Mirador 3 utilisée pour l'exercice** (vide par défaut) : https://iiif.biblissima.fr/mirador3/?theme=light

Pour charger directement une ressource IIIF via l'URL :

- un Manifeste :
	- `https://iiif.biblissima.fr/mirador3/?iiif-content={URL_MANIFESTE_IIIF}`
	- [Exemple](https://iiif.biblissima.fr/mirador3/?iiif-content=https://media.nga.gov/public/manifests/nga_highlights.json&theme=light) (National Gallery of Art Collection Highlights)
- une Collection : 
	- `https://iiif.biblissima.fr/mirador3/?iiif-content={URL_COLLECTION_IIIF}`
	- [Exemple](https://iiif.biblissima.fr/mirador3/?theme=light&iiif-content=https://portail.biblissima.fr/iiif/collection/ark:/43093/coldata5151005ea5833e5a05e2639cbb210946cb7e0609) (collection de livres numérisés de la Bibliothèque de l'abbaye Saint-Benoît de Fleury à Saint-Benoît-sur-Loire)

#### Étapes de l'exercice

1. **Ouvrir Mirador** : https://iiif.biblissima.fr/mirador3/?theme=light (instance vide)
2. **Importer au moins 2 ou 3 Manifests** de votre choix, par exemple en piochant dans la liste "Exemples d'URL de Manifestes IIIF" ci-dessus
3. **Configurer un environnement multi-fenêtres :**
	- expérimenter les deux types d'espaces d'espace de travail ("Elastique" et "Mosaïque")
	- explorer les différents panneaux (métadonnées, index) et options de fenêtre (modes d'affichage)
4. **Modifier les réglages d'une image** (luminosité, contraste, saturation, rotation etc.)
5. **Télécharger une image entière et un détail au sein d'une image** (région zoomée), en cliquant sur l'icône en forme de trois petits points verticaux au niveau d'une fenêtre
6. **Importer d'autres ressources IIIF** dans votre espace de travail à partir des sites donnés en exemple (cf. supra *"Ressources utiles en histoire de l'art proposant IIIF"*) :
  - importer via l'URL d'un Manifest (copier l'URL et la coller dans le champ `Ajouter une ressource` dans Mirador)
  - par glisser-déposer ("drag and drop") :
  	- d'une image de votre ordinateur (glisser l'image dans l'interface de Mirador)
  	- d'un logo IIIF depuis l'un des sites suivants : Getty, NGA, Princeton Art Museum, Harvard Art Museums, Yale Center for British Art
7. **Importer/exporter une session Mirador** :
	- dans la barre de menu principal (à gauche), cliquer sur l'icône avec les trois petits points horizontaux
	- cliquer sur `Exporter l'espace de travail` puis `Copier`
	- recharger la page, ou bien ouvrir un Mirador vide dans un nouvel onglet ou un autre navigateur
	- cliquer sur `Importer un espace de travail` puis `Coller` et `Importer`
	
	

------

### Exercice 2 : Annoter un objet avec SimpleAnnotationServer (SAS)

#### Exemple

L'oeuvre utilisée dans cet exercice est la suivante : *Picture Gallery with Views of Modern Rome* (1757), Giovanni Paolo Pannini (1691–1765). Museum of Fine Arts, Boston. https://collections.mfa.org/objects/34215 (Consulté le 11/11/2020).

Ressources Wikimedia sur ce tableau :

- Commons : https://commons.wikimedia.org/wiki/File:Giovanni_Paolo_Pannini_-_Picture_Gallery_with_Views_of_Modern_Rome_-_Google_Art_Project.jpg
- Wikidata : https://www.wikidata.org/wiki/Q28796135
- IIIF Manifest : https://wd-image-positions.toolforge.org/iiif/Q28796135/P18/manifest.json

Cet exemple est inspiré de la démo réalisée à partir de l'oeuvre *Galerie de vues de la Rome antique* (Giovanni Paolo Panini, Musée du Louvre) sur Wikimedia Commons :

- Wikidata : http://www.wikidata.org/entity/Q14619165 => voir l'utilisation de la propriété `depicts` (P180) conjointement avec le qualifieur `relative position within image` (P2677) : ces données sont utilisées pour les annotations IIIF.
- Mirador sur Toolforge, avec les annotations IIIF visibles sur l'image : https://mirador.toolforge.org/?manifest=https://wd-image-positions.toolforge.org/iiif/Q14619165/P18/manifest.json (Manifeste IIIF : https://wd-image-positions.toolforge.org/iiif/Q14619165/P18/manifest.json)

#### Démo d'introduction

Un autre exemple d'exploitation dans une interface dédiée des annotations IIIF créées via Mirador et stockées dans SAS :

- *Ovide moralisé ou La Bible des poètes en images. Comparaison de deux cycles iconographiques avec IIIF et Mirador*. Démos Biblissima. https://demos.biblissima.fr/ovide-moralise/

#### **Étapes** de l'exercice

1. **Ouvrir l'interface d'administration de SAS :** https://data-dev.biblissima.fr/simpleAnnotationStore/index.html

	```
	- URL Manifeste source : https://wd-image-positions.toolforge.org/iiif/Q28796135/P18/manifest.json
	- IIIF Search API endpoint : https://data-dev.biblissima.fr/simpleAnnotationStore/search-api/P18/search
	- Manifeste dérivé : https://api.npoint.io/4b814fdc63a68e61da04
	```

2. **Ouvrir un objet à annoter :**
  - cliquer sur `View annotations` dans le menu supérieur
  - La page liste les Manifestes qui ont été importés et indexés dans SAS : cliquer sur l'entrée `Picture Gallery with Views of Modern Rome` 
  - ouvrir le lien `Annotate` dans un nouvel onglet : l'objet devrait s'ouvrir dans Mirador

3. **Annoter l'image dans Mirador :**

  - cliquer sur l'icône en forme de bulles en haut à gauche
  - sélectionner une forme de tracé (rectangle, ovale, tracé libre, polygone, marqueur)
  - délimiter la zone (ou le point) de l'image à annoter ; une fenêtre devrait apparaître au-dessus de l'image
  - saisir votre annotation dans l'éditeur (un formatage html de base est possible) ; un champ "Tags" est aussi disponible
  - cliquer sur `Enregistrer` pour sauvegarder l'annotation : celle-ci est désormais stockée de manière persistente dans SAS (backend utilisé : Jena)

4. **Voir dans le back-office le détail des annotations créées  :**

  - cliquer sur `View annotations` dans le menu supérieur, puis sur le lien `Picture Gallery with Views of Modern Rome`
  - cliquer sur `Download annotations`, puis sur le lien `Picture Gallery with Views of Modern Rome - n annotations` : un document JSON s'ouvre, il contient la liste des annotations qui ont été saisies (ce document JSON est une `AnnotationList` conforme à l'[API Presentation 2.1](https://iiif.io/api/presentation/2.1/))

5. **Visualiser dans Mirador les annotations** créées par les autres participants :

	- Retourner à la page `View annotations` > `Picture Gallery with Views of Modern Rome` : https://data-dev.biblissima.fr/simpleAnnotationStore/manifest.xhtml?manifest=P18
	- Ouvrir Mirador en cliquant sur `Annotate` : https://data-dev.biblissima.fr/simpleAnnotationStore/index.html?iiif-content=https://wd-image-positions.toolforge.org/iiif/Q28796135/P18/manifest.json.
	- Afficher toutes les annotations créées (icône en forme de bulles).

6. **Activer et tester la recherche sur ces annotations** (API *Content Search* de IIIF) :

	- Retourner à la page `View annotations` > `Picture Gallery with Views of Modern Rome` : https://data-dev.biblissima.fr/simpleAnnotationStore/manifest.xhtml?manifest=P18
	- Enregistrer le Manifeste IIIF source sur votre ordinateur (clic-droit "Copier l'adresse du lien") : https://wd-image-positions.toolforge.org/iiif/Q28796135/P18/manifest.json
	- Ouvrir le fichier dans votre éditeur favori
	- Sur la page `Picture Gallery with Views of Modern Rome` de SAS, copier le bloc dans la section `IIIF Search Service` (dupliqué ci-dessous) :

	```
	"service": {
	    "profile": "http://iiif.io/api/search/0/search",
	    "@id": "https://data-dev.biblissima.fr/simpleAnnotationStore/search-api/P18/search",
	    "@context": "http://iiif.io/api/search/0/context.json"
	},
	```

	- Coller ce morceau de JSON dans le Manifeste que vous avez téléchargé à l'étape précédente : l'insérer juste avant ou après le champ `label` par exemple.

	- Copier la totalité du contenu JSON du fichier (Ctrl+A, Ctrl+C)

	- Ouvrir le site https://www.npoint.io, puis coller le JSON dans le champ situé au centre de la page (après avoir supprimé son contenu). Cliquer ensuite sur `Create JSON Bin`.

	- Une fois le JSON importé, cliquer sur le bouton `Share` en haut à droite : dans la fenêtre qui s'ouvre ensuite, copier le premier lien (en dessous du paragraphe `Access this bin via the API at:`).

	- Cette URL pointe désormais vers notre Manifest modifié, que l'on va pouvoir tester sur divers outils de visualisation :

		- Mirador 2 : https://data-dev.biblissima.fr/simpleAnnotationStore/
		- Mirador 3 : [https://iiif.biblissima.fr/mirador3/?iiif-content=](https://iiif.biblissima.fr/mirador3/?iiif-content=){URL_Manifeste}
		- Universal Viewer : https://uv-v3.netlify.app/#?c=&m=&s=&cv=&manifest={URL_Manifeste}

		

------

### Exercice 3 : créer/éditer un Manifeste avec le Manifest Editor

Le IIIF Manifest Editor est un éditeur de Manifestes développées par Bodleian Libraries (Oxford) et *text & bytes LLC*.

#### Exemple

L'exemple donné est une sélection d'images représentant le *Groupe du Laocoon* (Musée Pio-Clementino, Vatican), issues de différentes collections (NGA, INHA, Bibliothèque Vaticane, Smithsonian, Bibliotheca Hertziana), et de différents types (manuscrit enluminé, estampe, sculpture, peinture, dessin, gemme) :

- Ouvrir dans Mirador : https://iiif.biblissima.fr/mirador3/?iiif-content=https://jsonstorage.net/api/items/7ba0b03e-f171-44ef-a58e-2992145441db
- Manifeste IIIF : https://jsonstorage.net/api/items/7ba0b03e-f171-44ef-a58e-2992145441db

#### Étapes de l'exercice

1. **Choisir 2 ou 3 Manifestes**, en piochant dans la liste "Exemples d'URL de Manifestes IIIF" ci-dessus, ou en parcourant les sites compatibles IIIF donnés en exemple

2. **Ouvrir le *Manifest Editor*** : https://digital.bodleian.ox.ac.uk/manifest-editor

3. **Créer un nouveau Manifeste et importer des images :**

	- Cliquer sur `New Manifest`, puis dans le panneau à droite aller sur `Manifest Actions` > `Import Canvases` 
	- Cliquer sur le bouton `Open Sequence`, copier-coller une URL de Manifest dans le champ "Enter a remote Manifest URL", puis cliquer sur `Open`. Une vue zoomable de l'objet devrait s'ouvrir dans une fenêtre.
	- Répéter les points suivants pour chacun des Manifestes que vous avez préalablement choisis.

4. **Composer/éditer la séquence de votre Manifeste :**

	- Une fois vos Manifestes chargés dans l'éditeur, vous pouvez glisser-déposer une à une les images de votre choix dans la partie inférieure (dans l'espace horizontal blanc avec l'indication `+ Add Canvas`) :
		- en survolant la partie inférieure d'une image, un bandeau avec une ou plusieurs vignettes devrait apparaître.
		- glisser-déposer la vignette de votre choix sur la zone `+ Add Canvas`
		- répéter l'opération pour chaque image que vous souhaitez incorporer à votre Manifeste.
	- vous pouvez réordonner la séquence d'images en faisant glisser chaque *Canvas*, vous pouvez aussi dupliquer ou supprimer un *Canvas*

5. **Éditer les métadonnées de votre Manifeste :**

	- Une fois votre sélection faite, cliquer sur `Return to Edit Manifest` dans le panneau de droite
	- Dans ce même panneau latéral, vous pouvez :
		- éditer les métadonnées associées à votre Manifeste dans la section `Manifest Metadata` : éditer les champs pré-existants du Manifeste d'origine, ou ajouter un nouveau champ en cliquant sur `Add metadata field`
		- éditer les métadonnées associées à chaque Canvas dans la section `Canvas Metadata`

6. **Sauvegarder votre Manifeste :**

	- Dans le panneau latéral, cliquer sur l'icône en forme de roue dentée en haut à droite de l'écran (paramètres). Une fenêtre `Server Endpoint Settings` s'affiche.

	- Cliquer sur le lien `click here to use JsonStorage.net ` dans le paragraphe de texte. Les 2 champs de formulaire situés en dessous se remplissent automatiquement. Cliquer ensuite sur `Save Settings`, puis `Close`.

	- Cliquer sur le bouton `Save Manifest`, à partir de là vous pouvez :

		- télécharger votre Manifeste (JSON) sur votre ordinateur, pour pouvoir ensuite le publier sur votre propre serveur (`Download manifest`)
		- publier directement votre Manifeste sur le service en ligne *JsonStorage.net* : cela présente l'avantage de le rendre immédiatement accessible en ligne à travers une URL, mais sans garantie de pérennité. Après avoir cliqué sur `Store Manifets on Server`, un message de confirmation apparaît et l'URL de votre Manifeste est indiquée en dessous (sous la forme `https://jsonstorage.net/api/items/abc123...`).

		

------

### Bonus

#### Bonus 1 : Créer une mini-exposition virtuelle avec Exhibit.co

**Exemple préparé pour l'atelier** : "exhibit" créé à partir de la série de tableaux *The Voyage of Life*, par Thomas Cole (National Gallery of Art, Washington D.C.). Source : [nga.gov](https://www.nga.gov/collection-search-result.html?artist=Cole%2C%20Thomas&title=voyage%20of%20life&artobj_imagesonly=Images_online). 

Voir l'exposition : https://exhibit.so/exhibits/t153UkCxJXovu1jeuLV3

Autres exemples : https://exhibit.so/#showcase



#### Bonus 2 : Créer une "curation" de contenus avec le IIIF Curation Viewer

**Exemple préparé pour l'atelier** : "curation" de ressources IIIF de monnaies grecques de Panticapée (Royaume du Bosphore Cimmérien). Sources : Harvard Art Museums, Gallica.

Voir la démo : http://codh.rois.ac.jp/software/iiif-curation-viewer/demo/?curation=https://mp.ex.nii.ac.jp/api/curation/json/962dc427-6241-4200-82ad-69a0821b573c&lang=en

Curation (JSON) : https://mp.ex.nii.ac.jp/api/curation/json/962dc427-6241-4200-82ad-69a0821b573c 
