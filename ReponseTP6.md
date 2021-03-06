## Question 3.1.1 :

1. Exemple de parcours en profondeur préfixée, postfixée, et infixée : 
    -		affichage préfixé : on visite A en premier, puis B puis C,
    -		affichage postfixé : on visite B, ensuite C et enfin A,
    -		affichage infixé : on visite B, puis A et enfin C.

2. Pseudo code affichage préfixé pour l'arbre ABC :

```java
System.out.println(arbre1.nomSommet); 
System.out.println(arbre1.filsGauche.nomSommet);
System.out.println(arbre1.filsDroit.nomSommet);
```
PS : (extra) le code correspondant est la fonction AffichagePrefixe sur le ArbreBinaire.java.

----------------------
----------------------

## Question 3.2 :
1. Exemple de parcours en largeur de la figure 1 : 

* (A) (BC) (DEF) (GH)
* (A) (CB) (FED) (HG)

PS : (extra) le code correspondant est la fonction AffichagEnLargeur sur le ArbreBinaire.java.

###Photo de la console après l'exécution du programme ArbreBinaire.java : 

![ArbreBinaire](https://github.com/ArnaudRib/TD6/blob/master/Photos/ArbreBinaire.png)

----------------------
----------------------

##Question 3.3 :

### Photo de l'arbre cobbaye : 

![ArbreFig1](https://github.com/ArnaudRib/TD6/blob/master/Photos/ArbreFig1.png)

_________________________________________

##### Photo du code du Parcours Aléatoire n°1 :

![ParcoursAleatoire21](https://github.com/ArnaudRib/TD6/blob/master/Photos/ParcoursAléatoire.png)

##### Réponse à la question :

```java
		if (a!=null){
			System.out.print(a.nomSommet);
			...
			}
```


-		Cette partie du code indique que la première lettre de la réponse de l'algorithme est obligatoirement A, le sommet de l'arbre.
-		Remonter les racines est impossible. Une fois que l'on a dépassé un niveau dans une même branche, on peut remonter. C'est pourquoi ``acfbehgd`` et ``acfbdegh`` sont faux.

-> Finalement, les deux seuls résultats valables proposés sont : ``abdeghcf`` et ``abegdhcf``.

_________________________________________

##### Photo du code du Parcours Aléatoire n°2 :

![ParcoursAleatoire21](https://github.com/ArnaudRib/TD6/blob/master/Photos/ParcoursAleatoire21.png)

![ParcoursAleatoire22](https://github.com/ArnaudRib/TD6/blob/master/Photos/ParcoursAleatoire22.png)

##### Réponse à la question :

-	Les parcours ``abdeghcf`` et ``abegdhcf`` sont impossibles car passer de la lettre "a" à la lettre "b" implique de voyager vers gauche avant de passer vers la droite ce qui n'est pas permis par le programme. 
-	Même résonnement pour le parcours ``bdehgafc``, ``cfbdegha``, ``acfbdegh`` et ``cfbdegha`` autour de la lettre "b" cette fois.
-	``cfhgeabd`` et ``fchgdbea`` ne sortiront pas de l'algorithme car "e" n'est pas un fils direct de "a" mais un petit fils.
-	Même resonnement pour ``fcaehgbd`` mais à une profondeur de moins.

-> Finalement, il ne reste plus que : ``acfbehgd``, ``cfbehgda``, ``cfabehgd``, ``fcabehgd``, ``cfhgebda``, ``fcehgdba``, ``fchegdba`` et ``fcahgebd``.
