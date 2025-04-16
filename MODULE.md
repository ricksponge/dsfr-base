# 🔗 Intégrer DSFR Base comme sous-module Git

Ce guide explique comment intégrer le projet **DSFR Base** dans un autre projet en utilisant les sous-modules Git. Cela permet de maintenir une base commune à jour et réutilisable.

---

## 📥 Ajouter DSFR Base en tant que sous-module

1. **Se positionner dans le répertoire de votre projet principal** :

   ```bash
   cd mon-projet
   ```

2. **Ajouter DSFR Base comme sous-module** :

   ```bash
   git submodule add https://github.com/ton-utilisateur/dsfr-base.git dsfr-base
   ```

   Cela va cloner le dépôt DSFR Base dans le dossier `dsfr-base` de votre projet.

3. **Initialiser et mettre à jour les sous-modules** :

   ```bash
   git submodule update --init --recursive
   ```

4. **Valider les changements** :

   ```bash
   git add .gitmodules dsfr-base
   git commit -m "Ajout du sous-module DSFR Base"
   ```

---

## 🔄 Mettre à jour le sous-module DSFR Base

Pour récupérer les dernières modifications du sous-module dans votre projet principal :

```bash
cd dsfr-base
git checkout main
git pull origin main
cd ..
git add dsfr-base
git commit -m "Mise à jour du sous-module DSFR Base"
```

---

## 📦 Utiliser DSFR Base dans votre projet

Une fois le sous-module ajouté, vous pouvez :

- Inclure les fichiers nécessaires (comme `style.css` et `main.js`) depuis le sous-module.
- Personnaliser les composants DSFR selon les besoins de votre projet.

---

## 📚 Ressources utiles

- [Documentation officielle sur les sous-modules Git](https://git-scm.com/book/en/v2/Git-Tools-Submodules)
