# 🛠 Discover - Application

Bienvenue dans le projet **Discover**, une application dédiée à l'exploration des NFTs et des cryptomonnaies ! Ce README vous fournira une vue d'ensemble des différentes parties de l'application que j'ai développées, à savoir la partie **NFTs** et la partie **Coins**. Voici un aperçu de ce que chaque section couvre et comment elle fonctionne.

---

## 📋 Table des matières

- [Présentation du projet](#présentation-du-projet)
- [Technologies utilisées](#technologies-utilisées)
- [Partie NFTs](#partie-nfts)
  - [Fonctionnalités principales](#fonctionnalités-principales)
  - [Description technique](#description-technique)
  - [Gestion des données](#gestion-des-données)
- [Partie Coins](#partie-coins)
  - [Fonctionnalités principales](#fonctionnalités-principales)
  - [Description technique](#description-technique)
- [Notes et limitations](#notes-et-limitations)

---

## 🎯 Présentation du projet

**Discover** est une application qui permet aux utilisateurs d'explorer les NFTs et les cryptomonnaies en temps réel. En utilisant des API externes, l'application fournit des informations à jour sur les prix, les variations, les tendances, ainsi que des détails approfondis sur chaque actif.

L'application est divisée en deux parties principales :
1. La section **NFTs** - pour la découverte des Non-Fungible Tokens (NFTs).
2. La section **Coins** - pour le suivi des cryptomonnaies.

---

## 🛠️ Technologies utilisées

- **HTML5 / CSS3** : Pour la structure et le style de l'application.
- **JavaScript / jQuery** : Pour la logique côté client, les interactions dynamiques et les appels API.
- **API CoinGecko** : Pour récupérer des données en temps réel sur les NFTs et les cryptomonnaies.
- **Font Nunito** : Pour un style d'écriture cohérent et élégant.

---

## 🎨 Partie NFTs

### 📌 Fonctionnalités principales
- Affichage des **images** et **noms** des NFTs à partir de l'API.
- Affichage des **variations de prix sur 24h** pour chaque NFT.
- Gestion de l'affichage du nom sur plusieurs lignes si le nom est trop long.
- Mise en évidence des variations de prix en utilisant des couleurs (vert pour les augmentations, rouge pour les diminutions).
- Fonctionnalité pour masquer les variations si elles sont égales à **0%**.

### 🛠️ Description technique
- **API utilisée** : Les données des NFTs sont récupérées via l'API de CoinGecko.
- **Affichage conditionnel** : Si le nom d'un NFT dépasse 15 caractères, il est automatiquement divisé en deux lignes tout en respectant les mots complets.
- **Gestion des pourcentages** : Si la variation de prix sur 24h est de **0%**, l'affichage devient transparent pour éviter de surcharger l'interface.

### 🗃️ Gestion des données
Les données des NFTs sont récupérées avec des appels AJAX et affichées dynamiquement. Voici un exemple d'URL utilisé pour obtenir les informations :

```
https://pro-api.coingecko.com/api/v3/nfts/{nom_du_nft}?x_cg_pro_api_key={API_KEY}
```

Les informations récupérées incluent :
- L'image du NFT.
- Le nom du NFT.
- La variation du prix au cours des dernières 24h.

---

## 💰 Partie Coins

### 📌 Fonctionnalités principales
- Affichage des **variations de prix** pour les cryptomonnaies (24h, 7 jours, 30 jours, etc.).
- Mise à jour des pourcentages selon la **durée sélectionnée** à partir des boutons dynamiques.
- Utilisation d'indicateurs visuels pour les augmentations ou les baisses de prix (flèches montantes ou descendantes).
- Affichage en **transparent** lorsque la variation de prix est de **0%**.

### 🛠️ Description technique
- **API utilisée** : Les informations sur les cryptomonnaies sont également récupérées via l'API de CoinGecko.
- **Comportement dynamique** : Lorsque l'utilisateur sélectionne une durée spécifique (ex : 24h, 7d, 30d), les pourcentages changent dynamiquement pour refléter les variations de prix correspondantes.
- **Affichage conditionnel** : Si la variation est **0%**, les informations sont affichées en transparent.

---

## ⚠️ Notes et limitations
- L'application utilise les données fournies par CoinGecko, donc la disponibilité des données dépend de l'API.
- Certaines informations peuvent être manquantes si l'API ne fournit pas de données à jour.
- Les variations de prix sont mises à jour lorsque l'utilisateur sélectionne différentes durées, mais un délai peut exister en raison des limites de l'API.

---
