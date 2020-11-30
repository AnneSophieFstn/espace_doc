# Design Partern

Les design patterns sont des méthodes souvent utilisées lors du développement logiciel. Ils permettent d'optimiser, de clarifier du code informatique et de le rendre plus robuste.



Les design patterns sont regroupés en 3 grandes familles:
1. Les patterns de création

2. Les patterns de structuration

3. Les patterns comportementaux

Ici, le design pattern State fait partie de la famille des **patterns comportementaux**.

L'une des raisons principales est que le pattern State est utilisé pour **changer le comportement** d'un objet sans toucher à son instanciation.

Nous avons donc un **contexte** (sous-entendu notre objet principal). Ce **contexte** va donc manipuler une **interface de changement d'états**. Cette dernière héritera des différents états que pourra avoir le contexte.

Le **contexte** ne changera donc pas d'instanciation, mais son **comportement**, traduit par les **différents états** qui le composent, changera complètement.

## Exemple

Imaginons que nous souhaitons coder un lecteur vidéo très simple. Ce lecteur pourra uniquement lire une vidéo ou la mettre en pause. Nous voyons donc facilement qu'il n'y que deux états différents possible pour une vidéo dans ce logiciel:

**Lecture**

**Pause**

## Pourquoi utiliser le Design Partern

Après avoir testé la méthode classique et celle utilisant le pattern State, on est en droit de se demander **quel peut être l'intérêt d'utiliser le pattern State**. En effet, il va **nécessiter de créer plus de classe et donc d'écrire plus de code pour au final le même résultat**.

Et bien le pattern State va permettre au code d'évoluer très facilement!

Si nous décidons d'ajouter une fonctionnalité **retour au début de la vidéo**, avec la méthode classique, **nous devrions rajouter une condition dans la méthode action de la classe Video**. Or, avec le design pattern State, nous ne touchons pas au code existant! ** Nous rajoutons simplement la classe RetourAuDebut qui implémente EtatVideo**
