# Shorts Auto Editor

Outil web gratuit et illimité, 100% dans le navigateur (aucun serveur, aucun envoi de fichier) :
- Détecte automatiquement les meilleurs passages d'une vidéo (via analyse des silences/temps de parole)
- Découpe en clips verticaux 9:16 prêts pour YouTube Shorts / Reels
- Génère les sous-titres (.srt) de chaque clip via transcription automatique (Whisper, dans le navigateur)

## Utiliser le site

1. Active GitHub Pages : **Settings → Pages → Source: `main` branch, dossier `/ (root)`** → Save
2. Le site sera accessible à `https://hugo01sandovalhs-lab.github.io/shorts-auto-editor4HS/` après ~1 minute
3. Ouvre le lien, dépose ta vidéo, choisis le nombre de Shorts, lance le traitement

## Limites connues (MVP)

- Testé sur Chrome/Edge récents. Si un navigateur bloque le chargement du wasm, réessaie sur Chrome.
- La détection de "meilleur moment" est un premier heuristique (segments de parole les plus longs entre les silences) — pas encore une vraie IA de scoring. On peut l'affiner ensuite.
- Le recadrage 9:16 suppose une vidéo source au format paysage (16:9) standard.
- Vidéos très longues (>30-40 min) : peut être lent selon la puissance de l'ordinateur, tout tourne en local.

## Prochaines étapes possibles

- Sous-titres incrustés directement dans la vidéo (actuellement fichier .srt séparé, à importer sur YouTube ou dans CapCut)
- Scoring plus intelligent des meilleurs moments (énergie audio, visages, mots-clés)
- Automatisation quotidienne (détection des nouveaux uploads via l'API YouTube + traitement automatique)

Si un bug apparaît, note le message d'erreur affiché dans le journal en bas de page et transmets-le pour correction.
