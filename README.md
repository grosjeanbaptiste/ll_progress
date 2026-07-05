# ll_progress — LL user snapshots

Public export des progressions d'apprentissage L2 depuis l'app
[LL](https://github.com/grosjeanbaptiste/ll_app). Chaque utilisateur de
l'app pousse un snapshot vers ce repo depuis Réglages → **Publier mes
stats**.

## Structure

Un dossier par utilisateur (slug lowercased) :

```
users/
  <slug>/
    stats.json    # snapshot structuré (paires × paliers × CEFR)
    README.md     # table lisible par paire
```

## Contribuer sa propre progression

1. Installer LL sur iOS.
2. Créer un [Personal Access Token GitHub](https://github.com/settings/tokens)
   avec le scope `public_repo`.
3. Réglages → Publier mes stats sur GitHub → coller le PAT → tap.

Le repo `users/<toi>/` est créé automatiquement à la première publication ;
les suivantes overwrite les fichiers en place (idempotent).

## Access

Le token doit avoir un accès en écriture sur ce repo. Options :

- Owner : ajout comme collaborateur via Settings → Access.
- Fork perso : chacun publie sur son fork, `LL` détecte le repo cible
  configuré (à implémenter côté app si besoin).
