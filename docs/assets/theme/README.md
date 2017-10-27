# Theme Landslide pour Makina Corpus

Le dossier du thème landslide pour Makina Corpus est dans ce dépôt dédié.

À terme chaque formation aura son dépôt, l'idée est de permettre l'utilisation du thème en submodule git dans chaque dépôt de formation. L'avantage est que chaque dépôt peut rester "pinné" sur un commit du thème qui fonctionne bien, tout en ayant un seul dépôt dédié au thème. Le formateur qui doit donner la prochaine session d'une formation peut choisir s'il récupère les dernières mises à jour du thème ou bien rester sur la version précédente selon le temps dont il dispose pour préparer / mettre à jour le support.

Si vous ne connaissez pas les submodules, [la doc est pas mal faite](https://git-scm.com/book/fr/v2/Utilitaires-Git-Sous-modules)

## Ajouter le sous-module du thème dans le dépôt d'une formation

Préparer l'arborescence du dépôt de votre formation

    ```bash
    mkdir -p docs/assets
    ln -s docs/assets assets
    ```

Ajouter le dépôt en sous-module (submodule) git

    ```bash
    cd docs/assets
    git submodule add git@gitlab.makina-corpus.net:ehe/landslide-theme-makina.git docs/assets/makina
    git commit
    git push
    ```

Utiliser le thème dans votre fichier `.cfg`

    ```
    [landslide]
    theme = assets/makina
    source = src/support-en-markdown.md
    destination = docs/export-html.html
    relative = True
    embed = True
    linenos = no
    ```

## Contribuer au thème

Créez une branche pour vos modifications dans le dossier du thème.

    ```bash
    cd docs/assets/makina
    # Vous êtes dans le sous-module, ce que vous commitez ne va pas dans le projet parent
    git co -b <votre-branche>
    # faites vos modifications
    ```

Commitez vos modifications

    ```bash
    cd -
    git add docs/assets/makina .gitmodules
    git commit
    git push
    ```

## Récupérer le dépôt d'une formation et le thème en submodule

    ```bash
    git clone --recursive <url-du-depot-de-la-formation>
    ```

Si votre dépôt existe déjà et que vous avez récupéré les dernières modifications contenant l'ajout du submodule, vous devez l'initialiser

    ```bash
    git submodule init
    git submodule update
    ```

## Conventions pour vos slides

Ajouter à la fin du slide `.fx: macro` où macro est le nom de la classe que vous souhaitez voir appliquée.

### Classes landslide

* **alternate** couleur de fond sombre
* **quoteslide** to display a quote in a single slide
* **smaller** et **larger** pour afficher le texte en plus petit ou plus gros
* **titleslide** pour avoir un h1 (titre) et un h2 (sous-titre) sur le même slide
* **imageslide** pour avoir une image en background avec un titre

### Classes spécifiques à Makina

* **toc** pour afficher un plan
* **wide**
* **title1** (**page-heading1**)
* **title2** (**page-heading2**)
* **bg-image** to add last image added in the slide as a background
