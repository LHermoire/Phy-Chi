---
author: Mireille
title: Exemples de QCM
tags:
  - qcm
  - Difficulté **
---


## Un QCM non intéractif mais avec des explications

???+ question "QCM à volets avec explications"

    Voici diverses propositions

    === "Cocher la ou les affirmations correctes"

        - [ ] Proposition 1
        - [ ] Proposition 2
        - [ ] Proposition 3
        - [ ] Proposition 4

    === "Solution"

        - :x: ~~Proposition 1~~ Optionnel : Faux car ... 
        - :white_check_mark: Proposition 2 . Optionnel : Juste car ...
        - :white_check_mark: Proposition 3 . Optionnel : Juste car ...
        - :x: ~~Proposition 4~~ Optionnel : Faux car ... 



## Un QCM intéractif, avec mélange des questions et réponses, et score de réussite

Pour pouvoir tester, voici les réponses attendues : 

* Question 1 : proposition 1
* Question 2 : proposition 2
* Question 3 : propositions 4 et 6



{{multi_qcm(
["Question 1 : ...", 
["Proposition 1", "Proposition 2", "Proposition 3", "Proposition 4", "Proposition 5"], [1]],

["Question 2 : ...",
["Proposition 1", "Proposition 2", "Proposition 3", "Proposition 4", "Proposition 5", "Proposition 6" ], [2]],

["Question 3 : cocher les deux bonnes réponses",
["Proposition 1", "Proposition 2", "Proposition 3", "Proposition 4", "Proposition 5", "Proposition 6" ], [4, 6], {'multi':True}],

multi = False,
qcm_title = "Un QCM avec mélange automatique des questions (bouton en bas pour recommencer)",
shuffle = True,
)}}




## Un QCM avec des questions plus développées

Pour pouvoir tester, voici les réponses attendues : 

* Première question : proposition 3
* Deuxième question : proposition 1
* Troisième question : propositions 1 et 3

{{ multi_qcm(
    [
"""
Première question qui prend plusieurs ligne :

Enoncé : ...............

Vous devez choisir une seule bonne réponse
""",
        [
            "Proposition 1",
            "Proposition 2",
            "Proposition 3",
            "Proposition 4",
        ],
        [3]
    ],
    [
        "Deuxième question qui ttient en une seule ligne : ...   - choisir l'unique bonne réponse",
        [
            "Proposition 1",
            "Proposition 2",
            "Proposition 3",
            "Proposition 4",
        ],
        [1],
    ],
    [
"""
Troisième question avec plusieurs lignes

Enoncé ....

Vous devez choisir deux bonnes répones
""",
        [
            "$\\int_0^{42} 1 dx = 42$",
            "Proposition 2",
            "Proposition 3",
            "Proposition 4",
        ],
        [1, 3],
        {'multi':True}
    ],
    multi = False,
    qcm_title = "Un QCM avec mélange automatique des questions (bouton en bas pour recommencer)",
    shuffle = True,
) }}
