# IneSoft RH

> Jouer en ligne : **https://inesoft-ctf.github.io/**

## Le contexte

IneSoft est un constructeur automobile en pleine croissance, spécialisé dans les véhicules électriques nouvelle génération. Comme toute entreprise moderne, IneSoft pilote ses milliers de collaborateurs à travers un portail RH interne : connexion, congés, bulletins de paie et console d'administration du personnel.

Problème : sous la pression des délais, l'équipe de développement a mis le portail en production un peu trop vite. Entre deux sprints, des restes de l'environnement de recette sont restés en ligne, et quelques mauvaises pratiques de sécurité se sont glissées dans le code. Personne ne s'en est rendu compte... jusqu'à aujourd'hui.

## Votre mission

Vous êtes mandaté pour auditer le portail RH d'IneSoft. En partant d'un simple visiteur anonyme, votre objectif est de remonter la chaîne de failles jusqu'à la console d'administration, puis de mettre la main sur l'export de paie chiffré que l'entreprise croyait bien protégé.

Ce challenge compte **5 flags** à capturer, du plus accessible au plus retors. Chaque flag a le format `IneCTF{...}`. Ils sont indépendants : vous validez ceux que vous trouvez, même sans aller au bout.

Difficulté : **expert**. Compétences mobilisées : reconnaissance, analyse de fichiers exposés, rétro-ingénierie JavaScript, manipulation de JSON Web Tokens et cryptographie.

## Jouer en local

Aucune installation, aucun serveur applicatif : tout se joue côté navigateur. Servez le dossier avec n'importe quel serveur statique, par exemple :

```
python -m http.server 8000
```

Puis ouvrez http://localhost:8000

Important : accédez au site via `http://` et non en ouvrant les fichiers en `file://`, sinon les fonctions cryptographiques du navigateur ne s'activent pas et les derniers paliers deviennent injouables.

## Règles du jeu

- Tout se résout côté client. Inutile d'attaquer l'hébergement, de scanner les ports ou de brute-forcer quoi que ce soit : ce n'est pas le sujet et cela ne rapporte aucun flag.
- Restez sur le périmètre de l'application.
- Amusez-vous, et que le meilleur gagne.

## Avertissement

IneSoft et ses collaborateurs sont fictifs. Cette application est volontairement vulnérable et destinée à l'apprentissage de la sécurité web. Ne reproduisez aucun des schémas présents ici dans une application réelle.
