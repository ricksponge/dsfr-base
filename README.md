# 🇫🇷 DSFR Base – Template Vite + Design de l’État

> 🎨 Un point de départ minimaliste pour créer des sites conformes au Design Système de l’État (DSFR) avec Vite.

---

## 📁 Structure du projet

```
dsfr-base/
├── assets/                 # Images et logos
│   └── logo-gendarmerie.png
├── index.html              # Page principale avec header/footer DSFR
├── main.js                 # Initialisation JS du DSFR
├── style.css               # Import des styles DSFR
├── vite.config.js          # Configuration Vite
├── package.json            # Dépendances et scripts
└── README.md               # Ce fichier
```

---

## 🚀 Installation

1. **Cloner le projet** :

   ```bash
   git clone https://github.com/ton-utilisateur/dsfr-base.git
   cd dsfr-base
   ```

2. **Installer les dépendances** :

   ```bash
   npm install
   ```

3. **Lancer le serveur de développement** :

   ```bash
   npm run dev
   ```

   Le projet sera accessible sur [http://localhost:5173](http://localhost:5173).

---

## 🛠️ Configuration

### `package.json`

```json
{
  "name": "dsfr-base",
  "version": "1.0.0",
  "type": "module",
  "scripts": {
    "dev": "vite",
    "build": "vite build"
  },
  "dependencies": {
    "@gouvfr/dsfr": "^1.13.1"
  },
  "devDependencies": {
    "vite": "^6.2.6"
  }
}
```

### `vite.config.js`

```js
import { defineConfig } from 'vite';

export default defineConfig({
  root: './',
  publicDir: 'assets',
  server: {
    open: true
  }
});
```

---

## 🎨 Utilisation du DSFR

### `style.css`

```css
@import "@gouvfr/dsfr/dist/dsfr.min.css";
@import "@gouvfr/dsfr/dist/utility/icons/icons.css"; /* Pour les icônes */
```

### `main.js`

```js
import '/node_modules/@gouvfr/dsfr/dist/dsfr.module.min.js';

window.dsfr?.start?.(); // Initialise les composants dynamiques
```

---

## 🧪 Tester les composants

Ajoute dans `index.html` :

```html
<button class="fr-btn fr-icon-add-circle-line">Ajouter</button>
```

Assure-toi que l'icône s'affiche correctement. Si ce n'est pas le cas, vérifie l'import des icônes dans `style.css`.

---

## 📦 Créer un nouveau projet basé sur DSFR Base

1. **Copier le dossier `dsfr-base`** :

   ```bash
   cp -r dsfr-base mon-nouveau-projet
   cd mon-nouveau-projet
   ```

2. **Mettre à jour les informations du projet** :

   - Modifier le nom dans `package.json`.
   - Changer le titre dans `index.html`.
   - Personnaliser les logos et les contenus.

3. **Installer les dépendances et lancer le projet** :

   ```bash
   npm install
   npm run dev
   ```

---

## 📚 Ressources utiles

- [Documentation officielle du DSFR](https://www.systeme-de-design.gouv.fr/)
- [Liste des icônes disponibles](https://www.systeme-de-design.gouv.fr/fondamentaux/icone/)
- [Documentation de Vite](https://vitejs.dev/guide/)
