--- 
title_meta  : Chapitre 2
title       : Introduction
description : Dans ce chapitre vous allez faire vos premiers pas avec R. Vous allez apprendre à utiliser la console comme calculatrice et à fabriquer vos premières variables. Vous allez aussi découvrir les principaux types d'objets que vous allez être amené à utiliser dans R. Tout va bien se passer, c'est parti ! 

--- type:NormalExercise xp:100
## L'interface de DataCamp

Dans la partie **éditeur** sur votre droite vous allez devoir taper du code R pour résoudre les exercices. 

R utilise le symbole `#` pour permettre l'écriture de commentaires dans vos scripts. Les commentaires sont utiles pour tout le monde : pour expliquer aux autres ce que vous faites, mais aussi pour vous, pour vous rafraîchir la mémoire. En tant que débutant, commentez, c'est essentiel ! 
Bien entendu ces commentaires ne sont pas interprétés par R, ils n'influençent pas les résultats.

Lorsque vous allez envoyer des instructions à R, celui-ci va vous répondre dans la **console** en bas à droite de votre écran. Les éventuels graphiques arriveront en haut à droite de votre écran.

Pour envoyer des instructions de l'éditeur vers la console il vous suffit de placer votre curseur dans l'éditeur au niveau de la ligne que vous voulez envoyer (ou de séléctionner ce que vous voulez envoyer) et de presser les touches "ctrl + ENTREE"

*** =instructions
- En appuyant sur "Get Hint" (le bouton orange) l'interface vous proposera un indice pour résoudre le problème. Ensuite si vraiment vous ne voyez pas comment résoudre le souci, vous pouvez demander la solution en cliquant "Get Solution" (le bouton rouge).
- Cliquez sur "Submit Answer" (le bouton vert) et observez la console, plusieurs lignes vont apparaître. Ces instructions sont générées automatiquement par la commande `demo("graphics")`. Plusieurs graphiques ont été générés, vous pouvez naviguer de l'un à l'autre via les boutons "previous plot" et "next plot". Cette fenêtre se fermera à la prochaine étape.
- La toute dernière ligne doit afficher `7` il s'agit du résultat de l'instruction `3+4` que vous venez d'exécuter. De la manière la plus basique, R peut être utilisé en tant que calculatrice, mais permet aussi, vous l'avez vu, de générer des graphiques... et bien plus encore.

*** =hint
Cliquez simplement sur le bouton 'Submit Answer'.

*** =pre_exercise_code
```{r eval=FALSE}
# no pec
```

*** =sample_code
```{r eval=FALSE}
# Ceci est l'éditeur, vous pouvez écrire dedans. La partie en dessous est la console
# Vous trouverez la console en dessous de ce bloc-notes.

# Le symbole dièse `#` est utilisé pour rajouter des commentaires

# Cette instruction permet de lancer une démonstration de graphiques qu'il est possible de générer avec R
demo("graphics")

# Calculez 3 + 4
3 + 4
```

*** =solution
```{r eval=FALSE}
# Ceci est l'éditeur, vous pouvez écrire dedans. La partie en dessous est la console
# Vous trouverez la console en dessous de ce bloc-notes.

# Le symbole dièse `#` est utilisé pour rajouter des commentaires

# Cette instruction permet de lancer une démonstration de graphiques qu'il est possible de générer avec R
demo("graphics")

# Calculez 3 + 4
3 + 4
```

*** =sct
```{r eval=FALSE}
success_msg("Super ! Maintenant que vous êtes familiarisés avec l'interface, rentrons un peu plus dans le vif du sujet ! ")
```

*** =skills
1

--- type:NormalExercise xp:100
## Un peu d'arithmétique

Comme vu précédemment, R peut être utilisé très basiquement comme une simple calculatrice. Examinez les opérateurs arithmétiques suivant :


- Addition: `+`
- Soustraction: `-`
- Multiplication: `*`
- Division: `/`
- Exponentiel: `^`
- Modulo: `%%`

Les deux derniers peuvent nécessiter un peu d'explications :
- L'opérateur `^` élève le nombre de gauche à la puissance qui correspond au nombre de droite: par exemple `3^2` donne 9.
- L'opérateur modulo retourne le reste de la division euclidienne du nombre de gauche par le nombre de droite, ainsi `5 %% 3` vaut 2.

*** =instructions
- Tapez `2^5` dans l'éditeur pour calculer 2 puissance 5.
- Tapez `28 %% 6` pour calculer 28 modulo 6.
- Cliquez sur `Submit Answer` et regardez la sortie de R dans la console.
- Remarquez l'usage du symbole `#` pour le rajout de commentaires dans le code R.

*** =hint
Un autre exemple pour l'opérateur modulo: `9 %% 5` vaut `4`.

*** =pre_exercise_code
```{r eval=FALSE}
# no pec
```

*** =sample_code
```{r eval=FALSE}
# une addition
5 + 5 

# une soustraction
5 - 5 

# une multiplication
3 * 5

 # une division
(5 + 5)/2 

# une exponentiation 


# Modulo

```

*** =solution
```{r eval=FALSE}
# une addition
5 + 5 

# une soustraction
5 - 5 

# une multiplication
3 * 5

 # une division
(5 + 5)/2 

# une exponentiation 
2^5

# Modulo
28 %% 6
```

*** =sct
```{r eval=FALSE}
msg = "N'enlevez pas les autres exemples de calculs ! "
test_output_contains("5 + 5", incorrect_msg = msg)
test_output_contains("5 - 5", incorrect_msg = msg)
test_output_contains("(5 + 5)/2", incorrect_msg = msg)
test_output_contains("2^5", incorrect_msg = "L'exponentiation ne semble pas correcte. Vous Etes certain de bien avoir suivi les instructions ? ")
test_output_contains("28 %% 6", incorrect_msg = "Il y a un souci avec le modulo. Relisez bien les instructions.")
success_msg("Bien jouE. On continue...")
```

*** =skills
1

--- type:NormalExercise xp:100
## Assignation de variable


Un des éléments de base en programmation statistique est appelé une **variable**. 

Une variable permet de stocker une valeur (par exemple 4) ou un objet (par exemple une description de fonction) dans R. Vous pouvez ensuite utiliser plus tard le nom de cette variable pour accéder facilement à la valeur ou l'objet qui est stocké dans cette variable. 

Vous pouvez assigner une valeur de 4 à une variable `ma_variable` avec la commande



```
ma_variable <- 4
```

*** =instructions
Complétez le code dans l'éditeur de telle sorte qu'il assigne la valeur 42 à la variable `x`. Cliquez sur 'Submit Answer'. Notez que lorsque vous demandez à R d'afficher `x`, la valeur 42 apparaît.

*** =hint
Regardez comment la valeur 4 a été attribuée à `ma_variable` dans le début du script. Faites exactement la même chose dans l'éditeur, cette fois en assignant 42 à la variable `x`.
*** =pre_exercise_code
```{r eval=FALSE}
# no pec
```

*** =sample_code
```{r eval=FALSE}
# Assignez la valeur 42 à  'x'
x <- 

# Affichez le contenu de la variable 'x'
x
```

*** =solution
```{r eval=FALSE}
# Assignez la valeur 42 à  'x'
x <- 42

# Affichez le contenu de la variable 'x'
x
```

*** =sct
```{r eval=FALSE}
test_object("x", undefined_msg = "Faites attention à bien créer une variable ayant pour nom <code>x</code>.",
            incorrect_msg = "la valeur que vous avez donné à  <code>x</code> ne semble pas correcte.") 
success_msg("Bon boulot ! Avez-vous remarqué que R n'imprime pas la valeur d'une variable dans la console lorsque vous la créez ? <code>x <- 42</code> n'a pas généré de sortie, car R suppose que vous aurez besoin cette variable à l'avenir. Sinon vous n'auriez pas stocké cette valeur dans une variable, n'est-ce pas ? Vous pouvez passer à l'exercice suivant ! ")
```

*** =skills
1

--- type:NormalExercise xp:100
## Assignation de variable (2)

Supposons que vous ayez un panier de fruits avec cinq pommes. En tant que statisticien en formation, vous souhaitez stocker le nombre de pommes dans une variable avec le nom `mes_pommes`. 

*** =instructions
- Tapez le code suivant dans l'éditeur: `mes_pommes <- 5`. Cela affectera la valeur 5 à `mes_pommes`.
- Tapez: `mes_pommes` sous le deuxième commentaire. Cet exemple affiche la valeur de `mes_pommes`.
- Cliquez sur `Submit Answer` et regardez la console : vous voyez que le numéro 5 est imprimé. R associe maintenant la variable `mes_pommes` à la valeur 5.


*** =hint
N'oubliez pas que si vous voulez attribuer un numéro ou un objet à une variable R, vous devez utiliser l'opérateur d'assignation `<-`. Cela dit, vous pouvez utiliser `=`, mais `<-` est largement préférable et simplifiera votre apprentissage.


*** =pre_exercise_code
```{r eval=FALSE}
```

*** =sample_code
```{r eval=FALSE}
# Affectez la valeur 5 à la variable appelée `mes_pommes`


# Afficher la valeur de la variable `mes_pommes`

```

*** =solution
```{r eval=FALSE}
# Affectez la valeur 5 à la variable appelée `mes_pommes`
mes_pommes <- 5

# Afficher la valeur de la variable `mes_pommes`
mes_pommes
```

*** =sct
```{r eval=FALSE}
test_object("mes_pommes", 
            undefined_msg = "Faites attention à bien définir la variable <code>mes_pommes</code>.",
            incorrect_msg = "Faites attention à bien définir la bonne valeur à <code>mes_pommes</code>.")
test_output_contains("mes_pommes", 
                     incorrect_msg = "Avez-vous dit explicitement à R d'afficher la variable <code>mes_pommes</code> dans la console ? ")
success_msg("Bien ! Passons à l'exercice suivant ! ")
```

*** =skills
1

--- type:NormalExercise xp:100
## Assignation de variable (3)

Chaque panier de fruit digne de ce nom a besoin d'oranges, donc vous décidez d'ajouter six oranges. En tant que statisticien, votre réflexe est de créer immédiatement la variable `mes_oranges` en lui affectant la valeur 6. Ensuite, vous voulez calculer combien de fruits vous avez au total. Puisque vous avez donné des noms à ces valeurs, vous pouvez maintenant coder ceci d'une manière claire : 

```
mes_pommes + mes_oranges
```

*** =instructions
- Assignez à `mes_oranges` la valeur 6.
- R vous permet de combiner les variables `mes_pommes` et `mes_oranges` dans une nouvelle variable `mes_fruits`. Créez cette nouvelle variable `mes_fruits`, qui est le nombre total de fruits dans votre corbeille de fruits.

*** =hint
`mes_fruits` est simplement la somme de `mes_pommes` et `mes_oranges`. Vous pouvez utiliser l'opérateur `+` pour sommer les deux et `<-` pour stocker le résultat dans la variable `mes_fruits`.

*** =pre_exercise_code
```{r eval=FALSE}
# no pec
```

*** =sample_code
```{r eval=FALSE}
# Assignez les bonnes valeurs aux variables 'mes_pommes' et 'mes_oranges'
mes_pommes <- 5


# Sommez ces 2 variables ensemble et demandez à R d'afficher le résultat dans la console


# Créez la variable 'mes_fruits'

```

*** =solution
```{r eval=FALSE}
# Assignez les bonnes valeurs aux variables 'mes_pommes' et 'mes_oranges'
mes_pommes  <- 5
mes_oranges <- 6

# Sommez ces 2 variables ensemble et demandez à R d'afficher le résultat dans la console
mes_pommes + mes_oranges

# Créez la variable 'mes_fruits'
mes_fruits <- mes_pommes + mes_oranges
```

*** =sct
```{r eval=FALSE}
test_object("mes_pommes", 
            undefined_msg = "Faites attention à bien définir la variable <code>mes_pommes</code>.",
            incorrect_msg = "Ne modifiez pas l'assignation de la variable <code>mes_pommes</code> ! ")
test_object("mes_oranges", 
            undefined_msg = "Avez-vous défini la variable <code>mes_oranges</code> ? ",
            incorrect_msg = "Avez-vous assigné la bonne valeur à la variable <code>mes_oranges</code> ? ")
test_output_contains("mes_pommes + mes_oranges",
                     incorrect_msg = "La sortie ne contient pas la somme des variables <code>mes_pommes</code> et <code>mes_oranges</code>. Essayez à nouveau")
test_object("mes_fruits",
            undefined_msg = "Faites attention à bien définir la variable <code>mes_fruits</code>.",
            incorrect_msg = "Faites attention à bien avoir défini la bonne valeur à <code>mes_fruits</code>.")
success_msg("Très bien ! Le grand avantage de faire des calculs avec les variables est que vous pouvez les réutiliser. Si vous modifiez simplement <code>mes_pommes</code> en changeant la valeur à 12 au lieu de 5 et que vous exécutez de nouveau le script (et seulement si vous l'éxecutez à nouveau), la valeur de <code>mes_fruits</code> sera automatiquement mis à jour. On passe à l'exercice suivant.")
```

*** =skills
1

--- type:NormalExercise xp:100
## Des pommes et des oranges

On nous dit souvent de ne pas additionner des pommes et des oranges (sur le même principe qu'il ne faut pas mélanger des choux et des carottes). Cependant, c'est exactement ce que nous venons de faire, non ? 
Les variables `mes_pommes` et `mes_oranges` de l'exercice précédent contiennent toutes deux des nombres. L'opérateur `+` fonctionne avec des variables de type `numeric`. Si vous essayez vraiment d'additionner des pommes et des oranges en assignant une valeur de type `character` à `mes_oranges` (cf l'éditeur), vous allez essayer d'additionner une variable numérique et une variable chaîne de caractères. Ce n'est pas possible ! 

*** =instructions
- Cliquez sur  'Submit Answer' et lisez le message d'erreur. Prenez le temps de bien comprendre pourquoi cela ne fonctionne pas.
- Ajustez le code afin que R soit au courant que vous avez 6 oranges et donc un panier de fruits avec 11 fruits.

*** =hint
Vous devez affecter la valeur numérique `6` à la variable `mes_oranges` au lieu de la chaîne de caractère `"six"`. Notez comment les guillemets servent à indiquer que `"six"` est un caractère.

*** =pre_exercise_code
```{r eval=FALSE}
# no pec
```

*** =sample_code
```{r eval=FALSE}
# Assignez une valeur à la variable  'mes_pommes'
mes_pommes <- 5 

# Affichez dans la console la valeur de 'mes_pommes'
mes_pommes       

# Assignez une valeur à la variable 'mes_oranges' et affichez le résultat
mes_oranges <- "six" 
mes_oranges 

# Fabriquez une nouvelle variable qui contient le nombre total de fruits
mes_fruits <- mes_pommes + mes_oranges 
mes_fruits
```

*** =solution
```{r eval=FALSE}
# Assignez une valeur à la variable  'mes_pommes'
mes_pommes <- 5  

# Affichez dans la console la valeur de 'mes_pommes'
mes_pommes  

# Assignez une valeur à la variable 'mes_oranges' et affichez le résultat
mes_oranges <- 6
mes_oranges 

# Fabriquez une nouvelle variable qui contient le nombre total de fruits
mes_fruits <- mes_pommes + mes_oranges 
mes_fruits
```

*** =sct
```{r eval=FALSE}
test_error()
test_object("mes_oranges",
            undefined_msg = "Faites attention à bien définir la variable <code>mes_oranges</code>.",
            incorrect_msg = "Faites attention à bien définir la bonne valeur à <code>mes_oranges</code>. Nombre et chaînes de caractères ne sont pas équivalent ! ")
test_output_contains("mes_pommes + mes_oranges", 
                     incorrect_msg = "La sortie dans la console ne contient pas le résultat de l'addition de <code>mes_pommes</code> et <code>mes_oranges</code>.")
test_object("mes_fruits", 
            undefined_msg = "Faites attention à bien définir la variable <code>mes_fruits</code>.",
            incorrect_msg = "Faites attention à bien définir la bonne valeur à <code>mes_fruits</code>.")
success_msg("Génial ! on peut passer à l'exercice suivant.")
```

*** =skills
1

--- type:NormalExercise xp:100
## Les types d'objets de base en R

R travaille avec de nombreux types de données. Voici les types les plus élémentaires pour débuter :

- Les valeurs décimales comme `4.5` que l'on appelle **numeric**.
- Les nombres entiers comme `4` que l'on appelle **integer**. Les integer sont aussi des numeric.
- Les valeurs booléennes (`TRUE` ou `FALSE`) sont appelées **logical** (`TRUE` signifie `VRAI` et `FALSE` signifie `FAUX`) mais R ne comprend pas le français, il faudra donc utiliser (`TRUE` et `FALSE`).`TRUE` peut être abrégé en `T` et `FALSE` en `F`.
- Les chaînes de caractères (c'est-à-dire du texte) que l'on nomme **character**.

Notez que les guillemets permettent de définir `"du texte"` en tant que `character`.

*** =instructions
Changez la valeur des variables suivantes:
- `mon_numeric` devient `42`.
- `mon_character` variable devient `"quarante-deux"`. Notez que les guillemets indiquent que `"quarante-deux"` est une chaîne de caractères.
- `mon_logical` variable en `FALSE`.

Faites attention, R est sensible à la casse : les minuscules et les majuscules sont considérées comme des caractères différents ! 

*** =hint 
Remplacez les valeurs dans l'éditeur avec les valeurs qui sont fournies dans l'exercice. Par exemple : 
`mon_numeric <- 42` assigne la valeur 42 à la variable `mon_numeric`. 

*** =pre_exercise_code
```{r eval=FALSE}
# no pec
```

*** =sample_code
```{r eval=FALSE}
# Quelle est la réponse à La grande question sur la vie, l'univers et le reste ? 
mon_numeric <- 42.5

# Les guillemets indiquent que la variable est de type chaîne de caractères

mon_character <- "du texte"

mon_logical <- TRUE
```

*** =solution
```{r eval=FALSE}
# Quelle est la réponse à La grande question sur la vie, l'univers et le reste ? 
mon_numeric <- 42

# Les guillemets indiquent que la variable est de type character
mon_character <- "quarante-deux"

mon_logical <- FALSE
```

*** =sct
```{r eval=FALSE}
test_object("mon_numeric", 
            undefined_msg = "Faites attention à bien définir la variable <code>mon_numeric</code>.",
            incorrect_msg = "Faites attention à bien définir la bonne valeur à <code>mon_numeric</code>")
test_object("mon_character",
            undefined_msg = "Faites attention à bien définir la variable <code>mon_character</code>.",
            incorrect_msg = "Faites attention à bien définir la bonne valeur à <code>mon_character</code>. N'oubliez pas les guillemets.")
test_object("mon_logical",
            undefined_msg = "Faites attention à bien définir la variable <code>mon_logical</code>.",
            incorrect_msg = "Faites attention à bien définir la bonne valeur à <code>mon_logical</code>.") 
success_msg("Bon boulot ! On passe à l'exercice suivant.")
```

*** =skills
1

--- type:NormalExercise xp:100
## Quel est le type de cet objet ? 

Vous souvenez-vous que lorsque vous avez ajouté des `5 + "six"` ? Vous avez eu une erreur due à une incompatibilité de types de données. Vous pouvez éviter ces situations embarrassantes en vérifiant le type de données d'une variable au préalable. Vous pouvez le faire comme suit :

```
class(le_nom_de_la_variable)
```

*** =instructions
Complétez le code dans l'éditeur et affichez la classe de `mon_numeric`, `mon_character` et `mon_logical` dans la console. 

*** =hint
Vous pouvez trouver le type de données de la variable `mon_numeric` par exemple en tapant `class(mon_numeric)`. Ce que vous devez faire est similaire pour `mon_character` et `mon_logical`. 

*** =pre_exercise_code
```{r eval=FALSE}
# no pec
```

*** =sample_code
```{r eval=FALSE}
# Déclarez des variables de différents types
mon_numeric <- 42
mon_character <- "quarante-deux"
mon_logical <- FALSE 

# Vérifiez le type de ces variables

```

*** =solution
```{r eval=FALSE}
# Déclarez des variables de différents types:
mon_numeric <- 42
mon_character <- "quarante-deux"
mon_logical <- FALSE

# Vérifiez le type de ces variables
class(mon_numeric)
class(mon_character)
class(mon_logical)
```

*** =sct
```{r eval=FALSE}
test_object("mon_numeric")
test_object("mon_character")
test_object("mon_logical")
test_output_contains("class(mon_numeric)",
                     incorrect_msg = "La sortie ne contient pas la classe de  <code>mon_numeric</code>. Essayez à nouveau.")
test_output_contains("class(mon_character)",
                     incorrect_msg = "La sortie ne contient pas la classe de  <code>mon_character</code>. Essayez encore.")
test_output_contains("class(mon_logical)",
                     incorrect_msg = "La sortie ne contient pas la classe de  <code>mon_logical</code>.")
success_msg("Félicitations ! C'était le dernier exercice pour ce chapitre. Dirigez-vous vers le prochain chapitre et plongez dans le monde merveilleux des vecteurs ! ")
```

*** =skills
1
