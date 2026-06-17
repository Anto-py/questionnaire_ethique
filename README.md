# Quel utilisateur·rice d'IA es-tu ?

Questionnaire d'**autopositionnement** sur les enjeux de l'intelligence artificielle en
éducation, conçu pour une formation d'enseignant·es du secondaire (Fédération
Wallonie-Bruxelles).

L'outil n'est pas un test : il révèle un **profil d'usage de l'IA** à travers sept enjeux,
restitué sous forme d'un radar et de feedbacks personnalisés.

## Les sept enjeux

🔵 Éthique · 🟢 Juridique · 🟡 Écologique · 🔴 Esprit critique ·
🟠 Cybersécurité · 🟣 Démocratique · ⚫ Géopolitique

## Comment ça marche

1. Une question à la fois, dans un ordre tiré au hasard (la première réaction compte).
2. Les réponses sont scorées par enjeu (0–100 %).
3. Un **rapport** s'affiche : radar des sept enjeux, scores détaillés, points d'appui,
   angles morts, et un feedback par enjeu.

Chaque feedback est pensé dans une logique de **besoin de formation**, jamais de jugement :
un score bas signale un enjeu à explorer, pas une lacune.

## Confidentialité

100 % côté navigateur. **Aucune donnée n'est envoyée ni stockée** : tout est calculé
localement, sans connexion à un quelconque service. Rien n'est conservé après la fermeture
de l'onglet.

## Technique

Un seul fichier [`index.html`](index.html) : HTML + CSS + JavaScript, sans dépendance ni
backend. Le radar est tracé en SVG pur ; les feedbacks sont déterministes (calculés à partir
des scores). Charte graphique rétrofuturiste.

## Déploiement

Hébergement statique — aucune configuration serveur requise.

**GitHub Pages** : `Settings → Pages → Source: Deploy from a branch → main / root`.
Le site est alors servi à l'adresse `https://<utilisateur>.github.io/<dépôt>/`.

Pour un test local : ouvrir `index.html` directement, ou
`python3 -m http.server 8000` puis `http://localhost:8000`.

## Personnalisation

En tête du `<script>` de [`index.html`](index.html), l'objet `CONFIG` permet de renseigner
le nom du formateur et un contact. Les textes des feedbacks sont regroupés dans l'objet
`FEEDBACK`.
