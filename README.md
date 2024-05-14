# Template

Ce template a été conçu à l'origine pour les rapports de stage de l'IMT Nord Europe.
Le résultat obtenu après compilation de ce template peut être visualisé dans le fichier `preview.pdf`.

**Remarque** : Il ne peut pas être compilé avec `pdflatex` en raison des polices d'écriture utilisées. Dans la suite de ce README, c'est `xelatex` qui sera utilisé.

# On Ubuntu

Updating apt repositories :
```
sudo apt update
```

Installing TexLive :
```
sudo apt install texlive-xetex
```

Installing your language's babel package :

_(Adapt this line to the language you need for your document)_
```
sudo apt install texlive-lang-french
```

Installing Biber package :
```
sudo apt install texlive-bibtex-extra biber
```

Installing **latexmk** :
```
sudo apt install latexmk
```

# First compilation
- To simply generate a pdf, named `main.pdf` in your root folder :
```
latexmk
```
- To generate a pdf that will automatically open in your web browser :
```
latexmk -pv
```
- To generate a pdf, and regenerate it automatically when the code changes :
```
latexmk -pvc
```

# Installation sur Windows

2 solutions sont possibles. Dans le cadre d'un rapport de stage, l'installation en **local** est préférable, en raison des temps de compilation qui peuvent être très longs.

### Environnement en local

- Téléchargez MikTek : https://miktex.org/
- Clonez le projet, puis ouvrez-le avec VS Code.
- Installez l'extension VS Code pour LaTeX la plus populaire, et avec le nouveau menu sur le côté dédié à LaTeX, compilez avec **xelatex** par exemple.
- Le résultat sera le fichier appelé `main.pdf` dans votre projet.

### Environnement en ligne

Vous pouvez vous créer un compte sur *Overleaf* : https://www.overleaf.com/

Puis importez le projet, et compilez-le en choisissant bien un compilateur différent de `pdflatex`. Et attention à bien compiler le fichier `main.tex`.

**PROBLÈME :** Avec l'environnement en ligne, le principal problème est que le temps de compilation peut être très long (de l'ordre de la minute), voire dépasser le temps de compilation autorisé par *Overleaf* si votre projet est trop gros.
