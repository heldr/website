# 🖥 CLI

## Commandes

### Serve

Serve démarre un serveur de développement, qui reconstruira automatiquement votre application lorsque vous modifiez des fichiers et prend en charge [le remplacement de module à chaud](hmr.html) pour un développement plus rapide.

```bash
parcel index.html
```

### Build

Build construit les ressources une fois, il active aussi la minification et définit la variable NODE_ENV à production. [Production](production.html)

```bash
parcel build index.html
```

### Watch

La commande watch est similaire à serve, sauf que la commande watch ne démarre pas un serveur.

```bash
parcel watch index.html
```

### Help

Affiche toutes les options possibles de la cli.

```bash
parcel help
```

## Options

### Répertoire de sortie

Par défaut : "dist"

Disponible dans : `serve`, `watch`, `build`

```bash
parcel build entry.js --out-dir build/output
ou
parcel build entry.js -d build/output
```

```base
root
- build
- - output
- - - entry.js
```

### Définit l'URL publique à appliquer

Par défaut : "/"

Disponible dans : `serve`, `watch`, `build`

```bash
parcel build entry.js --public-url ./dist/
```

Cela produira :

```html
<link rel="stylesheet" type="text/css" href="/dist/entry.1a2b3c.css">
ou
<script src="/dist/entry.e5f6g7.js"></script>
```

### La cible (target)

Par défaut : browser

Disponible dans : `serve`, `watch`, `build`

```bash
parcel build entry.js --target node
```

Les cibles possibles sont : node, browser et electron

### Change le niveau de journalisation

Par défaut : 3

Disponible dans : `serve`, `watch`, `build`

```bash
parcel build entry.js --log-level 1
```

| Loglevel | Effet                                       |
|---       |---                                          |
| 0        | Journal désactivé                           |
| 1        | Consigner uniquement les erreurs            |
| 2        | Consigner les erreurs et les avertissements |
| 3        | Tout consigner                              |

### Nom d'hôte du HMR

Par défaut : `location.hostname` du windows courant

Disponible dans : `serve`, `watch`

```bash
parcel build entry.js --hmr-hostname parceljs.org
```

### Port du HMR

Par défaut : Un port disponible au hasard

Disponible dans : `serve`, `watch`

```bash
parcel build entry.js --hmr-port 8080
```

### Nom de fichier en sortie

Par défaut : Nom du fichier original

Disponible dans : `serve`, `watch`, `build`

```bash
parcel build entry.js --out-file output.html
```

Cela modifie le nom du fichier de sortie du paquet

### Imprime un rapport détaillé

Par défaut : rapport minimal

Disponible dans : `build`

```bash
parcel build entry.js --detailed-report
```

### Définit un certificat personnalisé

Par défaut : génère un certificat

Disponible dans : `serve`

```bash
parcel build entry.js --cert certificate.cert --key private.key
```

### Ouvre dans le navigateur

Par défaut : ouverture désactivée

Disponible dans : `serve`

```bash
parcel build entry.js --open
```

### Désactive source-maps

Par défaut : source-maps activé

Disponible dans : `serve`, `watch`, `build`

```bash
parcel build entry.js --no-source-maps
```

### Désactive autoinstall

Par défaut : autoinstall activé

Disponible dans : `serve`, `watch`

```bash
parcel build entry.js --no-autoinstall
```

### Désactive le HMR

Par défaut : HMR activé

Disponible dans : `serve`, `watch`

```bash
parcel build entry.js --no-hmr
```

### Désactive la minification

Par défaut : minification activée

Disponible dans : `build`

```bash
parcel build entry.js --no-minify
```

### Désactive le cache du système de fichiers

Par défaut : cache activé

Disponible dans : `serve`, `watch`, `build`

```bash
parcel build entry.js --no-cache
```