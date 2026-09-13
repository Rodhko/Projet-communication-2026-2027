# Affiches des vitrines — Projet PIC

Site pédagogique présentant le menu et les 3 affiches de la salle d'exposition
(promo BTS GPN — Projet PIC) au format A3 :

- **Vitrine 1 — Les Oiseaux d'eau** (anatidés)
- **Vitrine 2 — Les Échassiers**
- **Vitrine 3 — Les Rapaces**

Tout se consulte depuis une seule page `index.html` : navigation par onglets,
affichage adapté à l'écran et impression d'une affiche en A3.

## Structure du projet

```
site_web/
├── index.html          # menu + les 3 affiches (page unique)
├── images/             # les 47 photos des espèces (noms simplifiés)
├── deployer_github.sh  # script d'aide au déploiement
└── README.md
```

## Ouvrir en local (simple test)

Double-clique sur `index.html` ou lance :

```bash
python3 -m http.server 8000
# puis http://localhost:8000
```

## Déploiement sur GitHub Pages

### 1. Créer le dépôt (une seule fois)
Sur https://github.com/new : nom **projet-pic**, visibilité **Public**, dépôt **vide**
(ne pas cocher « Add a README »).

### 2. Publier le dossier
```bash
cd site_web
git remote add origin https://github.com/UTILISATEUR/projet-pic.git
git push -u origin main
```

> À la demande de mot de passe, coller un **Personal Access Token** (Settings →
> Developer settings → Personal access tokens → cocher `repo`), pas le mot de passe.

### 3. Activer la mise en ligne
1. GitHub → dépôt `projet-pic` → **Settings → Pages**
2. Source : **Deploy from a branch** → branche **main** → **/ (root)** → **Save**
3. En ligne en ~1 min sur : `https://UTILISATEUR.github.io/projet-pic/`

## Mettre à jour le site

```bash
cd site_web
git add .
git commit -m "nouvelle mise à jour"
git push
```

## Crédits

Photos des espèces (Oiseaux d'eau) : Wikimedia Commons — images sous licence libre
(Wikimedia Foundation). Photographies des Échassiers et des Rapaces : photos
personnelles prises lors du projet.
