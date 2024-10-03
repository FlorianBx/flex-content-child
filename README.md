# Démonstration Flexbox et display: contents

Ce projet a pour objectif de vous familiariser avec l'utilisation combinée de display: flex et display: contents. Vous apprendrez comment créer des mises en page flexibles tout en préservant l'alignement des éléments enfants.

## Concept clé : display: contents

La propriété `display: contents` est un outil puissant lorsqu'il s'agit de travailler avec Flexbox. Voici comment elle fonctionne :

1. Lorsqu'un élément est défini avec `display: contents`, il est essentiellement "invisible" pour le rendu, mais ses enfants sont traités comme s'ils étaient des enfants directs de l'élément parent.
2. Cela permet aux enfants de participer au contexte de mise en page Flexbox du parent, même s'ils sont imbriqués dans un conteneur intermédiaire.

## Exemple de code

Voici un exemple de la structure HTML utilisée dans ce projet :

```html
<nav>
  <a href="#"><img src="assets/bolt.svg" alt="Bolt"></a>
  <a href="#"><img src="assets/git.svg" alt="Book"></a>
  <a href="#"><img src="assets/book.svg" alt="Calendar"></a>
  <div class="search">
    <input type="search" placeholder="Search">
    <a href="#"><img src="assets/search.svg" alt="Chat"></a>
    <a href="#"><img src="assets/plus.svg" alt="Check"></a>
  </div>
</nav>
```

Et le CSS correspondant :

```css
nav {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.search {
  display: contents;
}
```

## Explication

1. La `<nav>` utilise `display: flex` pour aligner ses enfants horizontalement.
2. La `<div class="search">` utilise `display: contents`, ce qui fait que ses enfants (l'input et les liens) sont traités comme des enfants directs de `<nav>`.
3. Résultat : tous les éléments (liens, input, et liens dans .search) sont alignés horizontalement dans la barre de navigation, comme s'ils étaient tous des enfants directs de `<nav>`.

## Avantages

- Permet de maintenir une structure HTML sémantique et logique.
- Évite d'avoir à ajouter des classes Flexbox supplémentaires à chaque élément.
- Facilite la création de mises en page complexes tout en gardant un HTML propre.

## Comment utiliser ce projet

1. Clonez ce dépôt.
2. Ouvrez `index.html` dans votre navigateur.
3. Examinez le code source et les styles CSS pour comprendre comment `display: flex` et `display: contents` interagissent.
4. Expérimentez en modifiant les styles et la structure HTML pour voir comment cela affecte la mise en page.

N'hésitez pas à poser des questions ou à proposer des améliorations !
