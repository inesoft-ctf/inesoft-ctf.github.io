# IneSoft RH

Portail RH de démonstration, volontairement vulnérable, conçu comme un challenge de type CTF (Capture The Flag) sur le thème de la sécurité web.

L'application imite un intranet RH classique : connexion, congés, bulletins de paie, espace d'administration. Votre objectif : partir d'un simple visiteur et progresser jusqu'à la console d'administration, puis récupérer l'export de paie chiffré.

## Le principe

5 drapeaux (flags) à récupérer, du plus accessible au plus retors. Chaque flag a le format `IneCTF{...}`. Ils sont indépendants : vous validez ceux que vous trouvez, même sans terminer.

Difficulté : expert. Compétences mobilisées : reconnaissance, analyse de fichiers exposés, rétro-ingénierie JavaScript, manipulation de JSON Web Tokens et cryptographie.

## Jouer en local

Aucune installation, aucun serveur applicatif : tout se passe côté navigateur. Servez le dossier avec n'importe quel serveur statique, par exemple :

```
python -m http.server 8000
```

Puis ouvrez http://localhost:8000

Important : accédez au site via `http://` et non en ouvrant les fichiers en `file://`, sinon les fonctions cryptographiques du navigateur ne s'activent pas.

## Règles du jeu

- Tout se résout côté client. Inutile d'attaquer l'hébergement, de scanner ou de brute-forcer : ce n'est pas le sujet.
- Restez sur le périmètre de l'application.

## Avertissement

Cette application est volontairement vulnérable et destinée à l'apprentissage de la sécurité web. Ne réutilisez aucun des schémas présents ici dans une application réelle.
