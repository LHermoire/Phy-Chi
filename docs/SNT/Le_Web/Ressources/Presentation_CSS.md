---
author: Hermoire Loïc
title: Le langage CSS
---

# Le langage CSS

## Présentation
Les CSS (Cascading Style Sheets en anglais, ou « feuilles de style en cascade ») sont le code utilisé pour mettre en forme une page web. Les bases des CSS présentent ce qu'il faut savoir pour commencer. Nous répondrons à des questions comme : 

* Comment rendre mon texte rouge ou noir ? 

* Comment faire apparaître mon contenu à tel endroit de l'écran ? 

* Comment décorer ma page web avec une image ou une couleur d'arrière-plan ?

Séparer le fond (en HTML) de la forme (en CSS) permet de modifier facilement l'aspect d'une page HTML sans être obligé de la réécrire. Seule la page CSS sera modifiée.

## Modifier la forme d'un page HTML


On peut repérer les objets HTML dans la page CSS de plusieurs façons :

* par leur balise. Toute les balises identiques seront impactées.

??? note "Exemple  : modification du style des titres `h1`"
	<div style="background-color:#f5f5f5 ; border-radius:10px;">
	```css
		h1 {
			/*ici on écrira le code du style de toutes les balises <h1>*/
		}
	```
	</div>

* par un identifiant ajouté dans la balise en HTML. Dans ce cas, seule cette balise sera concernée, deux balises ne pouvant partager un même identifiant. 

??? note "Exemple  : modification du style d'une balise avec un identidifiant"
	Dans la page **HTML** : ajout de l'identifiant `id`.
	<div style="background-color:#f5f5f5 ; border-radius:10px;">
	```html
		<h2 id = "titre_particulier">
			Ceci est un titre très particulier
		</h2>
	```
	</div>

	Dans le fichier **CSS** : on récupère l'identifiant en le nommant après un `#`.
	<div style="background-color:#f5f5f5 ; border-radius:10px;">
	```css
		#titre_particulier {
			/*ici on écrira le code du style de la balise nommée ""titre_particulier"*/
		}
	```
	</div>

* par une classe ajoutée dans des balises en HTML. Plusieurs balises peuvent partager la même classe. Les balises de même classe seront toutes impactées par le style.

??? note "Exemple  : modification du style d'une balise avec une classe"
	Dans la page **HTML** : ajout des classes `class`.
	<div style="background-color:#f5f5f5 ; border-radius:10px;">
	```html
		<ol>
			<li class = "mes_puces">
    			puce 1
 			</li>
 			<li class = "mes_puces">
     			puce 2
 			</li>  
		</ol>
	```
	</div>

	Dans le fichier **CSS** : on récupère les classes en les nommant après un `.`.
	<div style="background-color:#f5f5f5 ; border-radius:10px;">
	```css
		.mes_puces {
			/*ici on écrira le code du style de toutes les balises qui partagent cette classe*/
		}
	```
	</div>

## Quelques fonctions du CSS

Il faut maintenant connaître quelques fonctionnalités du CSS.

* En ce qui concerne les couleurs :
<div style="background-color:#f5f5f5 ; border-radius:10px;">
```CSS
color : red ; /* met la couleur en rouge */
background-color : rgb(230, 230, 230); /*met l'arrière plan dans la couleur définie en rgb, on peut utiliser également le nom de la couleur*/
```
</div>

* En ce qui concerne le texte :
<div style="background-color:#f5f5f5 ; border-radius:10px;">
```css
font-family : tahoma; /* choisit la police tahoma */
font-size : 18px; /* fixe la taille de la police à 18 pixels*/
font-weight : bold; /* met le texte en gras */
font-style : italic; /* met le texte en italic*/
text-align : center; /* centre le texte dans son conteneur*/
```
</div>

* En ce qui concerne les dimensions, quand l'objet en a (pour les images, les tableaux, les blocs...) :
<div style="background-color:#f5f5f5 ; border-radius:10px;">
```css
width : 300px; /* fixe la largeur à 300 pixels*/
height : 350px; /* fixe la hauteur à 350 pixels*/
```
</div>

* En ce qui concerne les bordures (pour les cellules `<TR>` des tableaux par exemple) :
<div style="background-color:#f5f5f5 ; border-radius:10px;">
```css
border : 2px solid black; /* une bordure de 2px en trait continu noir*/
border-radius : 20px; /* arrondi les angles sur 20px*/
box-shadow : 10px 10px 10px black; /* ajoute une ombre -> effet 3D */
border-collapse : collapse; /* fusionne les bordures des différentes cellules */
```
</div>

* En ce qui concerne les marges extérieures :
<div style="background-color:#f5f5f5 ; border-radius:10px;">
```css
margin : 10px; /*une marge de 10px tout autour */
margin-left  : 0px; /* une marge de 0px à gauche, pas de marge donc*/
margin-right  : 10px; /* une marge de 10px à droite*/
margin-top  : 0px; /* une marge de 0px en haut, pas de marge donc*/
margin-bottom : 10px; /* une marge de 10px en bas*/
```
</div>

* En ce qui concerne les marges intérieures :
<div style="background-color:#f5f5f5 ; border-radius:10px;">
```css
padding : 10px; /*une marge intérieure de 10px tout autour du contenu*/
padding-left  : 10px; /* une marge de 10px à gauche*/
padding-right  : 10px; /* une marge de 10px à droite*/
padding-top  : 10px; /* une marge de 10px en haut*/
padding-bottom : 10px; /* une marge de 10px en bas*/
```
</div>

!!! note "Exemple  :"
	Un code `HTML` sans feuille de style `CSS`.
	<div style="background-color:#f5f5f5 ; border-radius:10px; float: left; width: 49%;">
	```html
	<!doctype html>
	<html lang="fr">
    <head>
       	<meta charset="utf-8" />
       	<meta name="viewport" content="width=device-width" />
       	<title>Ma page de test</title>
    </head>
    <body>
        <h1> titre de mon exemple </h1>
		<h2> sous-titre 1 de mon exemple </h2>
		<p> Ceci est un exemple de paragraphe </p>
		<h2 class="soustitre"> sous-titre 2 de mon exemple (avec classe) </h2>
		<p id ="p2"> Ceci est un exemple de paragraphe avec identifiant. <p>
		<h2 class="soustitre"> sous-titre 3 de mon exemple (avec classe) </h2>
		<table>
			<tr>
				<td> Cellule 1 ligne 1 </td>
				<td> Cellule 2 ligne 1 </td>
			</tr>
			<tr>
				<td> Cellule 1 ligne 2 </td>
				<td> Cellule 2 ligne 2 </td>
			</tr>
		</table>
    </body>
	</html>
	```
	</div>

	<div style="background-color:#f5f5f5 ; border-radius:10px; float: right; width: 49%;">
	```css
		
	 
	 
	  
	 
	 
	 
	 
	 
	 
	 
	 
	 
	 
	 
	 
	 
	
	 
	 
	 
	 
	 
	 
	 
	```
	</div>
	<div style="display: table;clear: both;"> </div>

	<div style="border:2px solid black ; padding:10px">
		<h1> titre de mon exemple </h1>
		<h2> sous-titre 1 de mon exemple </h2>
		<p> Ceci est un exemple de paragraphe </p>
		<h2 class="soustitre"> sous-titre 2 de mon exemple (avec classe) </h2>
		<p id ="p2"> Ceci est un exemple de paragraphe avec identifiant. <p>
		<h2 class="soustitre"> sous-titre 3 de mon exemple (avec classe) </h2>
		<table>
			<tr>
				<td> Cellule 1 ligne 1 </td>
				<td> Cellule 2 ligne 1 </td>
			</tr>
			<tr>
				<td> Cellule 1 ligne 2 </td>
				<td> Cellule 2 ligne 2 </td>
			</tr>
		</table>
	</div>

	
	Un code `HTML` avec feuille de style `CSS`.
	<div style="background-color:#f5f5f5 ; border-radius:10px; float: left; width: 49%;">
	```html
	<!doctype html>
	<html lang="fr">
    <head>
       	<meta charset="utf-8" />
       	<meta name="viewport" content="width=device-width" />
       	<title>Ma page de test</title>
    </head>
    <body>
        <h1> titre de mon exemple </h1>
		<h2> sous-titre 1 de mon exemple </h2>
		<p> Ceci est un exemple de paragraphe </p>
		<h2 class="soustitre"> sous-titre 2 de mon exemple (avec classe) </h2>
		<p id ="p2"> Ceci est un exemple de paragraphe avec identifiant. <p>
		<h2 class="soustitre"> sous-titre 3 de mon exemple (avec classe) </h2>
		<table>
			<tr>
				<td> Cellule 1 ligne 1 </td>
				<td> Cellule 2 ligne 1 </td>
			</tr>
			<tr>
				<td> Cellule 1 ligne 2 </td>
				<td> Cellule 2 ligne 2 </td>
			</tr>
		</table>
    </body>
	</html>
	```
	</div>

	<div style="background-color:#f5f5f5 ; border-radius:10px; float: right; width: 49%;">
	```css
	body{
		background-color : cyan ;
	}

	h1 {
		color : red ;
		text-align : center ;
	}

	.soustitre{
		color : blue ;
		font-style : italic ;
	}

	p{
		text-align : center ;
	}

	#p2 {
		font-weight : bold ;
	}

	table,td{
		border : 2px solid black ;
		border-radius : 10px; 
		border-collapse : collapse;
	}
	```
	</div>
	<div style="display: table;clear: both;"> </div>

	<div style="border:2px solid black ; padding:10px ; background-color : cyan ;">
		<h1 style="color:red ; text-align : center ;"> titre de mon exemple </h1>
		<h2> sous-titre 1 de mon exemple </h2>
		<p style="text-align : center ;"> Ceci est un exemple de paragraphe </p>
		<h2 style="color : blue ; font-style : italic ;"> sous-titre 2 de mon exemple (avec classe) </h2>
		<p style="text-align:center ; font-weight : bold"> Ceci est un exemple de paragraphe avec identifiant. <p>
		<h2 style="color : blue ; font-style : italic ;"> sous-titre 3 de mon exemple (avec classe) </h2>
		<table style="border : 2px solid black ; text-align : center ; border-radius : 10px; border-collapse : collapse;" >
			<tr>
				<td style="border : 2px solid black ; border-radius : 10px; border-collapse : collapse;"> Cellule 1 ligne 1 </td>
				<td style="border : 2px solid black ; border-radius : 10px; border-collapse : collapse;"> Cellule 2 ligne 1 </td>
			</tr>
			<tr>
				<td style="border : 2px solid black ; border-radius : 10px; border-collapse : collapse;"> Cellule 1 ligne 2 </td>
				<td style="border : 2px solid black ; border-radius : 10px; border-collapse : collapse;"> Cellule 2 ligne 2 </td>
			</tr>
		</table>
	</div>

<hr/>
Réalisé par Christophe Bonvin (CC-BY-NC-SA)
