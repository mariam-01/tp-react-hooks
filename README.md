# TP React Hooks - Application de Gestion de Produits

Ce TP a pour objectif de mettre en pratique l'utilisation des Hooks React (useState, useEffect, useContext) ainsi que la création de Hooks personnalisés.

## Installation et configuration initiale

1. Cloner le dépôt :
```bash
git clone https://github.com/pr-daaif/tp-react-hooks.git
cd tp-react-hooks
```

2. Créer votre propre dépôt sur Github et changer le remote :
```bash
# Supprimer le remote origine
git remote remove origin

# Ajouter votre nouveau remote
git remote add origin https://github.com/[votre-username]/tp-react-hooks.git

# Premier push
git push -u origin main
```

3. Installer les dépendances :
```bash
npm install
```

4. Lancer l'application :
```bash
npm start
```

## Instructions pour le TP

Pour chaque exercice :
1. Lisez attentivement l'énoncé
2. Implémentez la solution
3. Testez votre implémentation (pensez à faire des copies d'écran)
4. Mettez à jour la section correspondante dans ce README avec :
   - Une brève explication de votre solution
   - Des captures d'écran montrant le fonctionnement
   - Les difficultés rencontrées et comment vous les avez résolues
5. Commitez vos changements avec un message descriptif

### Exercice 1 : État et Effets 
#### Objectif : Implémenter une recherche en temps réel

- [ ] 1.1 Modifier le composant ProductSearch pour utiliser la recherche
- [ ] 1.2 Implémenter le debounce sur la recherche
- [ ] 1.3 Documenter votre solution ici

_Votre réponse pour l'exercice 1 :_
Expliquez votre solution ici

**Explication de la solution**

*Expliquez ici comment vous avez :*

- Liaison de l'état du champ de recherche (`searchTerm`) à l'appel de l'API
- Utilisation du hook `useDebounce` pour différer la requête
- Mise à jour du composant `ProductList` avec les résultats filtrés

**Captures d'écran**
![1](images/image1.png)
![2](images/image2.png)

**Difficultés rencontrées et solutions apportées**

- Problème de rafraîchissement excessif des appels API → Résolu avec debounce
- Ajustement du délai de debounce pour un bon compromis réactivité/performance


### Exercice 2 : Context et Internationalisation
#### Objectif : Gérer les préférences de langue

- [ ] 2.1 Créer le LanguageContext
- [ ] 2.2 Ajouter le sélecteur de langue
- [ ] 2.3 Documenter votre solution ici

_Votre réponse pour l'exercice 2 :_
Créé et exporté `LanguageContext` dans `App.js`
- Stocke la langue actuelle (language) et une fonction changeLanguage pour la mise à jour
- Ajouté un sélecteur de langue pour accéder à language et changeLanguage
- Mise à jour de la langue avec setLanguage()


**Captures d'écran**

![1](images/image3.png)
![2](images/image4.png)

**Difficultés rencontrées et solutions apportées**

- Gestion du re-render sur changement de contexte → Vérifié que les providers englobent tous les composants
- Mise en place d’un fallback de langue par défaut


### Exercice 3 : Hooks Personnalisés
#### Objectif : Créer des hooks réutilisables

- [ ] 3.1 Créer le hook useDebounce
- [ ] 3.2 Créer le hook useLocalStorage
- [ ] 3.3 Documenter votre solution ici

_Votre réponse pour l'exercice 3 :_

- useDebounce : Retarde l'exécution d'une fonction pour éviter les appels réseau excessifs lors de la saisie.
- useLocalStorage : Permet de sauvegarder et récupérer des valeurs dans le localStorage

**Captures d'écran**

![1](images/image5.png)



### Exercice 4 : Gestion Asynchrone et Pagination
#### Objectif : Gérer le chargement et la pagination

- [ ] 4.1 Ajouter le bouton de rechargement
- [ ] 4.2 Implémenter la pagination
- [ ] 4.3 Documenter votre solution ici

_Votre réponse pour l'exercice 4 :_

- 4.1 l'Ajout du bouton de rechargement permet de relancer l’appel API.

**Captures d'écran**

![1](images/image6.png)

- 4.2 Implémentation de la pagination
- Géré la pagination avec `currentPage`, `pageSize` et `totalPages`
- Adapté l’URL de l’API et mis à jour les dépendances de `useEffect`
- Intégré les contrôles `Précédent` et `Suivant` dans la barre de pagination

**Captures d'écran**
![1](images/image7.png)
![1](images/image8.png)

**Difficultés rencontrées et solutions apportées**
- Calcul du nombre total de pages → Lecture de data.total retourné par l’API
- Désactivation des boutons aux bornes (page 1 et page finale)

## Rendu

- Ajoutez l'URL de votre dépôt Github dans  **Classroom** et envoyer la réponse dès le démarage de votre projet.
- Les push doivent se faire au fûr et à mesure que vous avancez dans votre projet.
- Le README.md doit être à jour avec vos réponses et captures d'écran. 
- Chaques exercice doit faire l'objet d'au moins un commit avec un message mentionnant le numéro de l'exercice.