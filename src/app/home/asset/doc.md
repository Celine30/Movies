# MyAdista3 : Bonne pratique

### Définition de bonne pratique
Les conventions de nommage sont un ensemble de règles qui permettent de rendre le code plus lisible pour un humain. La raison est simple, tout notre code est rempli de noms d'éléments : variables, fichiers, répertoires, fonctions... Et chacun de ces éléments représente quelque chose en particulier. Appelons-le de la manière la plus claire possible pour savoir ce qu'il fait. 

Qu'est-ce qui caractérise un code "bien écrit" ?
1. Le code doit être facile à lire
2. une organisation logique et évidente
3. Le code doit être explicite 
4. Le code doit être soigné et robuste au temps qui passe

### Nos bonnes pratiques

**L’indentation du code**
utiliser des tabulations

**Convention de nommage** :
* *Constantes* :
    1. Accessibilité : public/private/protected
    2. Type : const
    3. Nom de la variable en UPPERCASE
* *Variables “classiques”* :
    1. Accessibilité : public/private/protected
    2. Type : let
    3. Nom de la variable en camelCase
    4. Identifier noms trop courts, trop longs.
    5. Identifier valeurs littérales (remplacer en constante)
* **Fonctions** :
    1. Accessibilité : public/private/protected
    2. Type : function
    3. Nom de la fonction en camelCase
    4. Paramètres avec leur typage : (type $param1, type $param2, etc.)
    5. Type de retour de la fonction
    6. Au mieux, une fonction ne doit pas dépasser, en hauteur, la taille de l’écran.

**preference d'écriture** :
* *Chaînes de caractères* :
    préférez :
    >let myName = "Chris";
    console.log(`Hi! I'm ${myName}!`);  

    à :
    >console.log('Hi! I\'m' + myName + '!');
* *fin d'excecution* :
    à chaque excécution ";"
    > console.log(maVariable);
* *boucles* : 
    >let cats = ["Athena", "Luna"];
    for (let i of cats) {
    console.log(i);
    }
    * Il ne doit y avoir aucun espace entre un mot-clé de boucle et sa parenthèse ouvrante.
    * Il doit y avoir un espace entre les parenthèses et l'accolade ouvrante.
    * if / switch (pas de “Pyramid of Doom”).
    * foreach / array_map
* *fonctions* : 
    >const array1 = [1, 2, 3, 4];
    let sum = array.reduce(function (a, b) {
    return a + b;
    });
    * Il ne doit y avoir aucun espace entre un nom de fonction et sa parenthèse ouvrante.
    * Il doit y avoir un espace entre les parenthèses et l'accolade ouvrante.
* *Ecriture tertiaire* : 
    >let condition=true;
    let x = condition ? 1 : 0 ;

>ECMAScript 2022





1. Valider le code avec typescript-eslint.
2. SonarQube OK