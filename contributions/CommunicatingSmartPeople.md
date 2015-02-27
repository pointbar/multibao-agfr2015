## Communicating Smart People
Programmer, en utilisant TDD, un processeur multi-coeur, composé d'humains, pour résoudre des sudoku.
![](https://www.dropbox.com/s/gmoelq6c7w9qs4s/20150227_164825.jpg?dl=1)

### Objectif
- Comprendre les defis de la programmation concurrentiel
- Apprendre comment appliquer TDD sur du code concurrentiel
- Voir comment un processeur parallèle fonctionne et est programmé
- Voir que des règles simples et la collaboration peut résoudre des problèmes complèxes.

### Description
Il devient de plus en plus important de savoir travailler sur des systèmes parallèles. C'est aujourd'hui peu maitrisé, et c'est supposé ne pas pouvoir être fait en TDD. Ici on voit que c'est possible, même simple. Peut-être que vous verrez les choses différemment après.

**Pas besoin de savoir programmer**

![](https://www.dropbox.com/s/zhx5nwivfl4uo5f/20150227_164820.jpg?dl=1)
### Retour d'expérience 
Participants
- Pas très fun, mais prenant et très intéressant
- Très agréable de voir la solution apparaître
- Il était difficile de déchiffrer les messages, notamment on mélange fréquemment la colonne avec la ligne. Une autre notation peut-être?
Une personne a proposé "au lieu d'envoyer des messages aux voisins, n'envoyer que au display qui lui relayerait les messages". Certes mais on tombe dans une solution plus difficilement scalable - contention au niveau du display.

Animateur
- J'ai voulu afficher la solution en cours d'élaboration. C'était très apprécié mais certaines personnes se sont servis de ces informations, ce qui les a détourné de l'algorithme qu'on voulait vivre.
- Les participants n'ont pas respecté le passage des messages en synchrone en attendant qu'on accepte leur message, mais l'ont fait de façon asynchrone. Je ne sais pas si cela a une réelle importance finalement.
- En l'absence de binômage dans la phase résolution, rend probable l'introduction d'erreurs que je ne vois pas comment corriger.

Conclusions de l'animateur pour la prochaine fois
- Je tenterai une notation qui évite la confusion entre ligne et colonne. Ex pour "Grid E, ligne 1 et colonne 2 a la veleur 6" : E(L1, C2)=6 au lieu de E(1,2)=6. 
- Les personnes ne verront pas l'affichage avant la fin.


### Source
Pascal Van Cauwenberghe
http://www.agilecoach.net/coach-tools/concurrent-algorithms/