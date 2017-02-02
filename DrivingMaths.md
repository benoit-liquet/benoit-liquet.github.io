---
layout: page
title: DRIVING CURIOSITY IN MATHS 
---

## Divisible par 3

*This post is a translation and adaptation of the great [**blog**](http://www.oneonepsilon.com/single-post/2017/01/15/Divide-by-Three) of my friend* **Yoni Nazarathy**

Je suis le père (cela arrivera peut être un jour..) de 3 enfants, donc pour moi, la division par trois fait partie intégrante de ma vie. Un sac de 12 ballons d'eau est divisible par trois. Un sac de 30 fonctionne aussi bien. Mais avec un paquet de 16 il vous restera 1 ballon et vous serez face à un dilemme pour l'attribuer à celui qui le mérite.

Pour les parents avec 2 enfants, les choses sont généralement plus simples. Les nombres pairs sont divisibles par 2 et les nombres impairs ne le sont pas. Mais avec 3 enfants les choses sont plus complexes, comment savoir si un nombre entier est divisible par 3? Existe-t-il une règle ou un modèle simple?

Eh bien, il y a de bonnes chances que votre enfant ai appris cela à l'école. Peut-être même vous souvenez-vous de cette ``astuce'' de l'époque. Il va comme suit : **Additionner les chiffres individuels du nombre et vérifier si la somme des chiffres est divisible par trois. Si la somme des chiffres est divisible par 3, alors le nombre d'origine est aussi divisible par 3**. Sinon, ce n'est pas le cas. L'astuce fonctionne également pour 9, mais nous allons nous concentrer sur 3 ici. Neuf enfants avec des balons d'eau - trop compliqué à gérer!

Voici un exemple: prenez 264. La somme des chiffres est 2 + 6 + 4 = 12. Maintenant, 12 est divisible par 3 et cela implique que 264 est divisible par 3. En fait, \\(264 = 88 \times 3\\). De même, essayer avec 301. La somme des chiffres est \\(3 + 0 + 1 = 4\\). Ce n'est pas divisible par 3 et donc ni 301. Essayez de le diviser par 3 et vous obtiendrez un nombre non entier ou un reste.

Eh bien, c'est l'astuce. Vous pouvez même utiliser cette règle récursivement si vous le souhaitez. Par exemple, le 15 janvier 2017 (heure de Pékin), la population chinoise était estimée à 1 382 765 241 (près de 1,4 milliard de personnes). Est-ce que ce nombre exact est divisible par 3? Eh bien la somme des chiffres est,

$$1 + 3 + 8 + 2 + 7 + 6 + 5 + 2 + 4 + 1 = 39.$$

Et ceci traduit la nouvelle question: "39 est-il divisible par 3"? Eh bien, vous voyez probablement immédiatement que oui, mais pour répondre à cela, vous pouvez également regarder 3 + 9 = 12. Et ensuite pour voir si 12 est divisible par 3, vous pouvez même regarder 1 + 2 = 3 et donc oui il est divisible par 3. Donc puisque 3 est divisible par 3, 12 est divisible par 3 et donc 39 est divisible par 3 et donc la population chinoise (estimation de cet instant exact) est divisible par 3. Cette récursion est plus un exercice académique, parce que vous avez déjà vu que \\(39 = 3 \times 13\\) est divisible par 3.

Ok, donc c'était l'"astuce", une "astuce mathématique". Mais franchement, nous les mathématiciens sont souvent lassés d'utiliser le mot "astuce" parce que nous aimons comprendre la signification profonde derrière les choses. En fait, nous aimerions souvent voir une preuve que cette astuce fonctionne réellement pour n'importe quel nombre. Bien sûr, nous pouvons vérifier cela sur avec le nombre 264, le nombre 301 et la population chinoise, mais comment savoir que cette règle fonctionne toujours?

Voici donc une explication simple: reprenons le nombre 264 comme exemple.

$$264 = 2 \times 100 + 6 \times 10 + 4.$$

Vrai? Ceci est connu pour être l'écriture du nombre 264 en base 10. Cela peut aussi être fait pour la population chinoise, où le terme principal serait, \\(1 \times 10^9\\) (qui se lit comme "10 à la puissance 9", soit un milliard), le deuxième terme est \\(3\times 10^8\\), le troisième terme est \\(8 \times 10^7\\) et ainsi de suite.

Pour en revenir à l'exemple 264, nous pouvons maintenant représenter 100 comme 99 + 1 et 10 comme 9 + 1 donc,

$$264 = 2 \times (99 + 1) + 6 \times (9 + 1) + 4.$$

Maintenant vient le fait que $2 \times (99 + 1) = 2 \times 99 + 2 \times 1$. Cette propriété est appellée la ``distributivité'':

$$A \times (B + C) = A \times B + A \times C,$$

où nous remarquons que l'ordre des opérations est d'effectuer d'abord \\(A \times B\\) et \\(A \times C\\) et seulement plus tard nous additionnons  ces  deux termes. Par conséquent,

$$264 = 2 \times 99 + 2 + 6 \times 9 + 6 + 4.$$

Nous pouvons maintenant réorganiser ceci,

$$264 = 2 \times 99 + 6 \times 9 + (2 + 6 + 4).$$

Maintenant, observer que la dernière partie ci-dessus, (2 + 6 + 4), est en fait la somme des chiffres. Ainsi nous avons obtenu,

$$264 = 2 \times 99 + 6 \times 9 + \textrm{somme des chiffres}.$$

Les termes \\(2 \times 99\\) et \\(6 \times 9\\) sont toujours divisibles par 3, car 99 et 9 sont toujours divisibles par 3. Supposons maintenant que la somme des chiffres soit divisible par 3 (comme c'est le cas pour 2 + 6 + 4). Alors tous les termes du côté droit sont divisibles par 3 et alors 264 est divisible par 3. C'est pourquoi la règle a fonctionné pour 264.

Essayons cela au nombre de 2324.
\begin{eqnarray*}
2324 &=& 2 \times (999 + 1) + 3 \times (99 + 1) + 2 \times (9 + 1) + 4\\
       &=& 2 \times 999 + 3 \times 99 + 2 \times 9 + \textrm{somme des chiffres}
\end{eqnarray*}

La somme des chiffres est alors 2 + 3 + 2 + 4 = 11 et n'est pas divisible par 3. Mais la première partie, \\(2 \times 999 + 3 \times 99 + 2 \times 9\\) est divisible par 3. Donc cela signifie que,

$$2324 = \textrm{quelque chose divisible par 3 + quelque chose non divisible par 3}.$$

Par conséquent, 2324 n'est pas divisible par 3.

Ce qui précède est la base de la preuve de la divisibilité par 3. Il y a de très bonnes chances que vos enfants, âgés de 8 à 13 ans, apprennent cela à l'école. Mais quand il est enseigné, l'enseignant ne risque souvent pas d'expliquer d'où provient cette règle. Il est laissé comme une ``astuce''.

Si vous avez eu la patience de lire tout cheminement, alors peut-être que vous pouvez encore prendre un peu de temps pour  comprendre tout ces détails avec vos enfants. Nourrissez votre connexion avec eux et leur curiosité au sujet de la source de tels astuce mathématiques et bien d'autres encore.
