# Authentification Twitter

## Énoncé

Une session d’authentification twitter a été capturée. Retrouvez le mot de passe de l’utilisateur dans cette capture réseau.

## Méthode de résolution

1. On commence par récupérer le fichier du challenge (`./ch3.pcap`)

2. On ouvre ce dernier dans Wireshark

    On peut trouver dans ce fichier une requête HTTP. En l'ouvrant retrouve dans l'entête une information sur le mode de connexion.

    Il s'agit d'une authentification **Basic** dans un format `user:password`

    Wireshark déchiffre pour nous ce chiffrement. Ont trouve donc le nom d'utilisateur et le mot de passe correspondant :

    **usertest:password** => Le mot de passe du challenge est donc **password**