# 🚀 Scriptly — Guide de mise en ligne

## Ce que tu as

Un SaaS complet avec :
- Landing page haute conversion
- App de génération de contenu IA (vraiment fonctionnelle)
- Connexion à Hugging Face (gratuit)
- Historique des générations
- Paramètres & gestion de clé API
- Toggle prix mensuel/annuel

---

## Mise en ligne GRATUITE en 5 minutes (Vercel)

### Étape 1 — Prépare ton dossier
```
scriptly/
├── public/
│   └── index.html   ← le fichier principal
└── vercel.json
```

### Étape 2 — Crée un compte Vercel
→ https://vercel.com (gratuit, connecte-toi avec GitHub)

### Étape 3 — Déploie
**Option A (sans code) :**
1. Va sur https://vercel.com/new
2. Clique "Deploy" → "Browse" → sélectionne ton dossier `scriptly`
3. Clique "Deploy" — c'est tout !

**Option B (avec CLI) :**
```bash
npm install -g vercel
cd scriptly
vercel --prod
```

### Étape 4 — Ton site est en ligne !
Tu récupères une URL du type : `scriptly-xxx.vercel.app`
Tu peux ensuite ajouter un vrai domaine dans le dashboard Vercel.

---

## Clé API Hugging Face (gratuite)

1. Crée un compte sur https://huggingface.co
2. Va dans Settings → Access Tokens
3. Crée un token "Read"
4. Colle-le dans l'app (bouton "Paramètres & Clé IA")

**Limites du plan gratuit HF :** ~1000 requêtes/jour par compte utilisateur
Le modèle utilisé : **Mistral-7B-Instruct** (excellent qualité)

---

## Personnalisation rapide

Dans `index.html`, cherche et remplace :
- `Scriptly` → ton nom de marque
- Les prix (29€, 79€) → tes vrais prix
- Les témoignages → tes vrais avis clients
- `#7C3AED` (violet) → ta couleur principale

---

## Pour aller plus loin (optionnel)

| Fonctionnalité | Outil | Coût |
|---|---|---|
| Paiements abonnement | Stripe | 1.5% + 0.25€/transaction |
| Auth utilisateurs | Supabase Auth | Gratuit jusqu'à 50K users |
| BDD abonnements | Supabase | Gratuit 500MB |
| Emails transac. | Resend | Gratuit 3K emails/mois |

---

## Stack technique
- HTML/CSS/JS vanilla (aucune dépendance)
- Hugging Face Inference API
- LocalStorage pour l'historique et la clé API
- Vercel pour l'hébergement
