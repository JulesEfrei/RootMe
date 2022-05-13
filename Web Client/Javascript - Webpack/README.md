# Javascript - Webpack

## Énoncé

Trouvez le mot de passe

## Méthode de résolution

1. Ouvrir la console

2. Aller sur l'onglet `source`

3. Ouvrir le dossier `Webpack>src/components`

4. Ouvrir le fichier `YouWillNotFindThisRouteBecauseItIsHidden.vue`

5. Récupérer le mot de passe du challenge

```js
export default {
  name: 'Duck',
  data () {
    return {
        // Did you know that comment are readable by the end user ?
        // Well, this because I build the application with the source maps enabled !!!

        // So please, disable source map when you build for production

        // Here is your flag : BecauseSourceMapsAreGreatForDebuggingButNotForProduction

        'msg': 'Quack quack !! :).'
    }
  }
}
```

**=> BecauseSourceMapsAreGreatForDebuggingButNotForProduction**