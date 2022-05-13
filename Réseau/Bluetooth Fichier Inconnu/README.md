# Bluetooth - Fichier inconnu

## Énoncé

Votre ami travaillant à l’ANSSI a récupéré un fichier illisible dans l’ordi d’un hacker. Tout ce qu’il sait est que cela provient d’un échange entre un ordinateur et un téléphone. A vous d’en apprendre le plus possible sur ce téléphone.

La réponse est le hash SHA1 de la concaténation de l’adresse MAC (en majuscules) et du nom du téléphone.

Exemple : 
`AB:CD:EF:12:34:56monTelephone -> 836eca0d42f34291c5fefe91010873008b53c129`

## Méthode de résolution

1. Télécharger le fichier du challenge (`./ch18.bin`)

2. Il s'agit d'un fichier `.bin` il nous ai donc impossible de l'ouvrir avec logiciel de traitement de texte. On peut donc essayer de le lire en utilisant le package File System de NodeJS

```js
const fs = require('fs')

const data = fs.readFileSync("./ch18.bin")
console.log(data.toString());
```

3. En exécutant le script précédent, on peut récupérer un morceaux de texte => **GT-S7390G**
En faisant des recherches, on s'apperçoit qu'il s'agit d'un modèle de téléphone.

4. Ensuite, on essaye d'ouvrir le fichier dans Wireshark.
On repère une requête dans laquelle on retrouve le modèle du téléphone précédement trouvé. Dans cette même requête on trouve l'adresse mac du téléphone.

5. Comme énnoncer dans les consignes, le mot de passe du challenge et la concaténation de l’adresse MAC (en majuscules) et du nom du téléphone.
Il nous reste juste à convertir notre chaine de caractère (**0C:B3:19:B9:4F:C6GT-S7390G**) en SHA1 avec un convertisseur en ligne

6. On obtient le résultat suivant => **c1d0349c153ed96fe2fadf44e880aef9e69c122b**