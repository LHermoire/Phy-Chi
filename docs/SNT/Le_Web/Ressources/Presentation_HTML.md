---
author: Hermoire Loïc
title: Le langage HTML
---

# Le langage HTML

## Présentation
HTML (pour HyperText Markup Language, qu'on peut traduire en « langage de balisage hypertexte ») est le langage utilisé pour structurer une page web et son contenu. On peut par exemple organiser le contenu en un ensemble de paragraphes, une liste d'éléments, utiliser des images ou des tableaux de données. Dans cet article, nous verrons les notions de base pour comprendre HTML et ses fonctionnalités.

Le HTML est un langage fonctionnant avec des balises, ce qui signifie que chaque élément du code doit contenir 3 parties :  

1. **La balise ouvrante** : celle-ci se compose du nom de l'élément (ici p), entre deux chevrons (le premier ouvrant < et le second fermant >). Cela indique le début de l'élément, ici cela indique où le paragraphe commence.  

2. **La balise fermante** : à la différence de la balise ouvrante, une barre oblique (slash) est ajoutée avant le nom de l'élément. Cela indique la fin de l'élément. Dans notre exemple, c'est l'endroit où le paragraphe s'arrête. Oublier cette balise fermante est une erreur qu'on fait souvent au début et qui peut déclencher des effets étranges et indésirables.  

3. **Le contenu** : le contenu de l'élément. Pour cet exemple, il s'agit uniquement de texte.  

!!! note "Exemple  :"
    `<p> Ceci est le contenu d'un paragraphe. </p>`  
    1. `<p>` est la balise ouvrante de l'élément paragraphe (p).  
    2. `</p>` est la balise fermante de l'élément paragraphe.  
    3. `Ceci est le contenu d'un paragraphe.` est le contenu de l'élément paragraphe.  

## Anatomie d'un document HTML
Un élément HTML seul n'a pas vraiment d'intérêt. Pour créer une page HTML avec plusieurs éléments, il faut introduire des balises qui permettent de structurer le document, comme le montre l'exemple ci-dessous :

<div style="background-color:#f5f5f5 ; border-radius:10px;">
```html
<!doctype html>
<html lang="fr">
    <head>
        <meta charset="utf-8" />
        <meta name="viewport" content="width=device-width" />
        <title>Ma page de test</title>
    </head>
    <body>
        <img src="../assets/images/computer.png" alt="Mon image de test" />
    </body>
</html>
```
</div>


Voici ce qu'on y trouve :

* `<!DOCTYPE html>`
 Le « doctype ». Il s'agit d'un préambule obligatoire. Aux débuts de HTML (en 1991/1992), les doctypes servaient de liens vers des ensembles de règles qu'une page HTML devait suivre pour être considérée valides (avec des fonctionnalités de vérifications d'erreur et autres). Aujourd'hui, ils ne sont plus utilisés ainsi et ce marqueur sert uniquement au bon comportement du document.  

* `<html>...</html>`
L'élément `<html>` est celui qui contient tout le reste de la page. On l'appelle aussi l'élément racine. Il contient ici l'attribut lang qui indique la langue principale du contenu du document.  

* `<head>...</head>`
L'élément `<head>` sert de conteneur pour tout ce qu'on veut inclure dans une page HTML qui n'est pas du contenu à afficher à l'écran. Cela inclut les mots-clés et une description de la page destinée aux moteurs de recherches, les liens vers le CSS qui mettra en forme notre contenu, les déclarations pour les jeux de caractères utilisés, etc.  

* `<body>...</body>`
L'élément `<body>` contient tout le contenu qu'on veut afficher aux utilisatrices et utilisateurs web lorsqu'ils visitent la page, que ce soit du texte, des vidéos, des jeux, des pistes audio, etc.  

## Les différentes balises HTML

Une balise **titre** s'écit de la forme `<h1>...</h1>` pour un gros titre ou `<h2>...</h2>`, `<h3>...</h3>`, `<h4>...</h4>` pour les titres secondaires.

??? note "Exemple  :"
	<div style="background-color:#f5f5f5 ; border-radius:5px;">
	```html
		<h1>
			Titre de niveau 1 (gros titre)
		</h1>
		<h2>
			Titre de niveau 2 (plus petit)
		</h2>
		<h3>
			Titre de niveau 3 (encore plus petit)
		</h3>
	```
	</div>
	<div style="border:2px solid black ; padding:10px">
		<h1>
			Titre de niveau 1 (gros titre)
		</h1>
		<h2>
			Titre de niveau 2 (plus petit)
		</h2>
		<h3>
			Titre de niveau 3 (encore plus petit)
		</h3>
	</div>

La balise qui trace une **ligne de séparation** est `<hr/>`.
??? note "Exemple  :"
	<div style="background-color:#f5f5f5 ; border-radius:5px;">
	```html
		<hr/>
	```
	</div>
	<div style="border:2px solid black ; padding:10px">
		<hr/>
	</div>

Les balises de **paragraphe** ne contiennent que du texte. Il s'écrivent sous la forme `<p>...</p>`.
??? note "Exemple  :"
	<div style="background-color:#f5f5f5 ; border-radius:5px;">
	```html
		<p> Ceci est un paragraphe. </p>
	```
	</div>
	<div style="border:2px solid black ; padding:10px">
		<p> Ceci est un paragraphe. </p>
	</div>


La balise `<br/>` permet d'**aller à la ligne**.
??? note "Exemple  :"
	<div style="background-color:#f5f5f5 ; border-radius:5px;">
	```html
		<p> Ceci est un paragraphe <br/> avec un retour à la ligne. </p>
	```
	</div>
	<div style="border:2px solid black ; padding:10px">
		<p> Ceci est un paragraphe <br/> avec un retour à la ligne. </p>
	</div>

La balise **image** permet d'insérer une image dans le document HTML. Elle s'écrit sous la forme `<img src="url de l'image" title="commentaire"/>`.

* Le commentaire apparaît quand on passe sur la photo avec le curseur ou lrosque l'image ne charge pas.  

* L'url peut être locale (sur votre disque à côté du fichier fakebook.html) ou distant (sur un serveur avec un adresse web dite URL).

??? note "Exemple  :"
	<div style="background-color:#f5f5f5 ; border-radius:5px;">
	```html
		<img src="../assets/images/computer.png" alt="Mon image de test" />
	```
	</div>
	<div style="border:2px solid black ; padding:10px">
		<img src="https://forge.apps.education.fr/lhermoire/phy-chi-hermoire/-/raw/main/docs/assets/images/computer.png" alt="Mon image de test" />
	</div>

Pour créer un **tableau**, il faut utiliser différentes balises:

* La balise `<table>` marque le début du tableau, et `</table>` la fin du tableau. 

* La balise `<tr>` ouvre une nouvelle ligne, et `</tr>` ferme cette ligne.  

* La balise `<td>` ouvre une nouvelle cellule, et `</td>` ferme cette cellule.  

Par défaut, les tableaux n'ont pas de bordure. On ajoute une bordure aux cellules dans la feuille `style.css`. Si vous regardez bien votre fichier HTML, vous noterez la présence d'une balise de style tout en haut : c'est à cela qu'elle sert !
??? note "Exemple  :"
	<div style="background-color:#f5f5f5 ; border-radius:5px;">
	```html
		<table> <!-- début du tableau -->
			<tr> <!-- ouverture de la première ligne du tableau -->
				<td> <!-- ouverture de la première cellule du tableau -->
					cellule 1 ligne 1
				</td> <!-- fin de la première cellule du tableau -->
				<td>
					cellule 2 ligne 1
				</td>
			</tr> <!-- fin de la première ligne du tableau -->
			<tr> <!-- ouverture de la deuxième ligne du tableau -->
				<td> <!-- ouverture de la première cellule du tableau -->
					cellule 1 ligne 2
				</td> <!-- fin de la première cellule du tableau -->
				<td>
					cellule 2 ligne 1
				</td>
			</tr> <!-- fin de la deuxième ligne du tableau -->
		</table> <!-- fin du tableau -->
	```
	</div>
	<div style="border:2px solid black ; padding:10px">
		<table style="border-collapse: collapse"> <!-- début du tableau -->
			<tr> <!-- ouverture de la première ligne du tableau -->
				<td style="border:2px solid black ;"> <!-- ouverture de la première cellule du tableau -->
					cellule 1 ligne 1
				</td> <!-- fin de la première cellule du tableau -->
				<td style="border:2px solid black ;">
					cellule 2 ligne 1
				</td>
			</tr> <!-- fin de la première ligne du tableau -->
			<tr> <!-- ouverture de la deuxième ligne du tableau -->
				<td style="border:2px solid black ;"> <!-- ouverture de la première cellule du tableau -->
					cellule 1 ligne 2
				</td> <!-- fin de la première cellule du tableau -->
				<td style="border:2px solid black ;">
					cellule 2 ligne 1
				</td>
			</tr> <!-- fin de la deuxième ligne du tableau -->
		</table> <!-- fin du tableau -->
	</div>

Les balises de **liste** permettent de créer des listes à puces :

* Des listes à puces non numérotées `<ul>...</ul>`.

* Des listes à puces numérotées `<ol>...</ol>`.

??? note "Exemple  :"
	<div style="background-color:#f5f5f5 ; border-radius:5px;">
	```html
		<ul> <!-- série de puces non numérotées-->
			<li> <!-- première puce -->
				première puce non numérotée
			</li> <!-- fin première puce -->
			<li> <!-- deuxième puce -->
				deuxième puce non numérotée
			</li> <!-- fin deuxième puce -->
		</ul>
		<ol> <!-- série de puces numérotées-->
			<li> <!-- première puce -->
				première puce numérotée
			</li> <!-- fin première puce -->
			<li> <!-- deuxième puce -->
				deuxième puce numérotée
			</li> <!-- fin deuxième puce -->
		</ol>
	```
	</div>
	<div style="border:2px solid black ; padding:10px">
		<ul> <!-- série de puces non numérotées-->
			<li> <!-- première puce -->
				première puce non numérotée
			</li> <!-- fin première puce -->
			<li> <!-- deuxième puce -->
				deuxième puce  non numérotée
			</li> <!-- fin deuxième puce -->
		</ul>
		<ol> <!-- série de puces numérotées-->
			<li> <!-- première puce -->
				première puce numérotée
			</li> <!-- fin première puce -->
			<li> <!-- deuxième puce -->
				deuxième puce numérotée
			</li> <!-- fin deuxième puce -->
		</ol>
	</div>

La balise de **lien hypertexte** permet de créer des liens internes ou externes vers d'autres pages ou documents. Elle est de la forme `<a href='url du lien'> description du lien </a>`.

??? note "Exemple  :"
	<div style="background-color:#f5f5f5 ; border-radius:5px;">
	```html
		<a href='https://lhermoire.forge.apps.education.fr/phy-chi-hermoire/SNT/Le_Web/Activites/Le_langage_HTML/'> Lien vers la page de l'activité 2 </a>`
	```
	</div>
	<div style="border:2px solid black ; padding:10px">
		<a href='https://lhermoire.forge.apps.education.fr/phy-chi-hermoire/SNT/Le_Web/Activites/Le_langage_HTML/' width=600; > Lien vers la page de l'activité 2 </a>`
	</div>

<hr/>
Réalisé par Christophe Bonvin (CC-BY-NC-SA)