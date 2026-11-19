# Bazik SDK — Guide en français

SDK JavaScript/Node.js **non officiel** pour l'API Bazik, avec des fonctionnalités documentées pour les paiements MonCash, les transferts MonCash/NatCash et la consultation de portefeuilles.

> Ce dépôt n'est pas une documentation officielle de Bazik. Vérifiez les fonctionnalités, frais, limites et autorisations dans la documentation du fournisseur avant une utilisation en production.

## Prérequis

- Node.js 18 ou version ultérieure
- Accès autorisé à l'API Bazik
- Identifiants API conservés côté serveur

## Installation

```bash
npm install bazik-sdk
```

## Initialisation

```js
const { Bazik } = require("bazik-sdk");

const bazik = new Bazik({
  userID: process.env.BAZIK_USER_ID,
  secretKey: process.env.BAZIK_SECRET_KEY,
});
```

Configurez les variables d'environnement sur votre serveur ou votre plateforme d'hébergement. Ne placez jamais les clés dans une application mobile, du JavaScript exécuté dans le navigateur ou un dépôt public.

## Paiements

Le README principal présente les méthodes `bazik.payments.create()` et `bazik.payments.verify()`. Vérifiez le statut de paiement sur votre serveur avant de livrer un produit ou de créditer un compte. Ne considérez pas une simple redirection comme une confirmation de paiement.

## Transferts

Les méthodes documentées comprennent `bazik.transfers.checkCustomer()`, `getQuote()`, `moncash()` et `natcash()`. Contrôlez les montants, les destinataires, les autorisations et les risques de doublons avant tout transfert réel.

## Tests

```bash
npm test
```

La suite de tests existante utilise le module natif `node:test` et des réponses API simulées.

## Contribuer

Consultez [CONTRIBUTING.md](../CONTRIBUTING.md) et le [README principal](../README.md).

## Sécurité

Si des identifiants réels ont été publiés dans Git, leur suppression du fichier courant **ne les supprime pas de l'historique**. Révoquez et renouvelez les clés concernées auprès du fournisseur.
