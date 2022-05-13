# CISCO - Mot de passe

## Énoncé

Trouvez le mot de passe "enable"

## Méthode de résolution

1. Ouvrir le fichier

2. On remarque qu'a plusieurs reprise il y a des mots de passe sous la forme => **username <Name> password 7 <Password>**

3. En faisant des recherches, nous sommes tombé sur un convertisseur de mot de passe CISCO. Nous avons tester avec les différents utilisateur présent dans le fichier.

=> Pour l'utilisateur Hub ; **6sK0_hub**
=> Pour l'utilisateur Admin ; **6sK0_admin**

On remarque ici un schéma de mot de passe avec `6sK0_` puis le nom d'utilisateur. Le mot de passe du challenge est donc **6sK0_enable**