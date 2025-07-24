# Pokédex Vue.js 🔍

Ce projet est une petite application frontend développée avec **Vue.js 3**, qui interagit avec l'API [PokeBuild](https://pokebuildapi.fr/api/v1) pour afficher et rechercher parmi 100 Pokémon.

## 🧩 Fonctionnalités

- 🔁 Appel de l'API PokeBuild (limitée à 100 Pokémon)
- 🔎 Barre de recherche dynamique
- 🎴 Affichage des cartes de Pokémon
- 💬 Message d'erreur si aucun Pokémon ne correspond à la recherche
- ✨ Transitions douces entre les composants

## 📦 Technologies utilisées

- [Vue.js 3](https://vuejs.org/)
- [Vite](https://vitejs.dev/)
- Tailwind CSS (optionnel si utilisé)
- API publique : [https://pokebuildapi.fr/api/v1/pokemon/limit/100](https://pokebuildapi.fr/api/v1/pokemon/limit/100)

## ▶️ Lancer le projet en local

```bash
# 1. Clone le dépôt
git clone <url-de-ton-repo>

# 2. Va dans le dossier
cd nom-du-dossier

# 3. Installe les dépendances
npm install

# 4. Démarre le serveur de développement
npm run dev
