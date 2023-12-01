# MyAdista3 : Bonne pratique

### Définition de bonne pratique
Les conventions de nommage sont un ensemble de règles qui permettent de rendre le code plus lisible pour un humain. La raison est simple, tout notre code est rempli de noms d'éléments : variables, fichiers, répertoires, fonctions... Et chacun de ces éléments représente quelque chose en particulier. Appelons-le de la manière la plus claire possible pour savoir ce qu'il fait. 

Qu'est-ce qui caractérise un code "bien écrit" ?
1. Le code doit être facile à lire
2. une organisation logique et évidente
3. Le code doit être explicite 
4. Le code doit être soigné et robuste au temps qui passe

### Nos bonnes pratiques

La langue anglaise demeure préconisée pour tous les nommages

**L’indentation du code** :
utiliser des tabulations

**Convention de nommage** :

* *Variables “classiques”* :
    * Accessibilité : public/private/protected
    * Type : let
    * Nom de la variable en camelCase
    * Identifier noms trop courts, trop longs.
    * Utiliser ses règles de nommage :
        >  *** {list} pour un tableau //let casesList = [];
        {is} *** pour un boolean //let isOpen = true;
        {has}*** pour un boolean //let hasDroit = false; 
    * Identifier valeurs littérales (remplacer en constante)
* *Constantes* :
    * Accessibilité : public/private/protected
    * Type : const
    * Nom de la variable en UPPERCASE
    * Même regles de nommage que les variables "classiques"
* *Interfaces / CLasses* :
    * Type : interface / class
    * Nom de la variable en PascalCase
    * Même regles de nommage que les variables "classiques" 
* **Fonctions** :
    * Accessibilité : public/private/protected
    * Type : function
    * Nom de la fonction en camelCase
    * Paramètres avec leur typage : (type $param1, type $param2, etc.)
    * Type de retour de la fonction
    * Au mieux, une fonction ne doit pas dépasser, en hauteur, la taille de l’écran.
    * Elles doivent ête commentée (explications, params et return)
        >/**
            * Send custom request using fetch api
            * @param { String } url
            * @param { String } method
            * @param { Object } body
            * @return { Promise }
            */
            function ajax(url, method, body) {
                …
            }

        côté Nest
        >/**
            * Check if the user can do something about on Entity
            * @example checkIfUsercanDoOnEntity('1072166')
            * @param {entity} String, the entity the user wants do something about
            * @throws {UnauthorizedException} if the user can not 
            * @throws {InternalServerErrorException} if an error occurs
            */

* **les fichiers** :
    * Nom du fichier en KebabCase (just-a-steack.componant.ts)
    * ils doivent etre créer via la console :
        pour un component => ng g c *nomducomponent*
        pour un service => ng g s *nomduservice*
        pour une interface => ng generate interface *nomdelinterface* --type=model
    * Ils doivent avoir des noms court et parlant.
    * *Suggestions de nommage* :
        * pour les dialogs => confirm-dialog
        * pour les sideba => sb-contact

**preference d'écriture** :
* *Chaînes de caractères* :
    préférez :
    >let myName = "Chris";
    console.log(`Hi! I'm ${myName}!`);  

    à :
    >console.log('Hi! I\'m' + myName + '!');
* *fin d'excécution* :
    Terminer les instructions par ;
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
* *interface/classe* :
    * Préférere les interfaces : elles ne sont pas compilées en JS (car les interfaces n’existent pas) donc pour notre code final, nous n’avons de surplus.
* *chaine de caractères* :
    * Utilisez des guillemets doubles pour les chaînes.
* *Suggestions de nommage* :
    * Ajouter à une liste : *add ou append*
    * Suppression complète de données : *delete*
    * Retirer un élément d'une liste : *remove*
    * Annulation d'action : *cancel*
    * Ouverture/fermeture : *open/close* (ou si alternatif : *toggle*)
    * Récupération de données : *get* 
    * Remplacement de données : *set*
    * Mise à jour de données : *update* 
    * Réinitialisation à l'état initial : *reset*
    * Callback/gestionnaire : *handle* (ex : handleClick)
    * Dénombrement : *count* (ex: pageCount)
    * Précédent/suivant : *prev*/*next*



**Pour finir** :
Valider le code avec typescript-eslint.
SonarQube OK /(prettier)