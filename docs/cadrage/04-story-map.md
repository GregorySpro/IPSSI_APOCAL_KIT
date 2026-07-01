# Story Map — EduTutor IA

**Date :** 29/06/2026 · **Équipe :** EduTutor Groupe 14

---

## Colonne vertébrale (activités utilisateur)

```
SE CONNECTER → FOURNIR UN COURS → GÉNÉRER UN QUIZ → PASSER LE QUIZ → CONSULTER SES RÉSULTATS → SUIVRE SA PROGRESSION
```

---

## Décomposition par release

### RELEASE 1 — MVP (mercredi 01/07 17h45)

| Activité | User Stories incluses |
|----------|-----------------------|
| **Se connecter** | S'inscrire avec email · Valider son email · Se connecter · Réinitialiser son mot de passe · Gérer son profil |
| **Fournir un cours** | Uploader un PDF ≤ 5 Mo · Saisir un texte ≥ 200 caractères |
| **Générer un quiz** | Lancer la génération de 10 QCM via LLM local · Voir un feedback pendant la génération |
| **Passer le quiz** | Répondre aux 10 questions une par une · Soumettre ses réponses |
| **Consulter ses résultats** | Voir son score /10 · Voir le détail bonnes/mauvaises réponses |
| **Suivre sa progression** | Consulter l'historique des quizz (date, cours, score) |

### RELEASE 2 — Pistes à affiner (jeudi 02/07 17h45)

| Activité | User Stories envisagées |
|----------|-------------------------|
| **Mode enseignant** | Créer un compte enseignant · Générer un quiz pour ses élèves · Relire et modifier les questions · Exporter en PDF |
| **Révision ciblée** | Revoir uniquement les questions ratées · Repasser un quiz sur ses erreurs |
| **Dashboard progression** | Graphique d'évolution du score dans le temps · Identification des notions faibles |
| **Mode sombre** | Basculer entre thème clair et sombre |
| **Génération haute qualité** | Choisir entre génération rapide (llama3.2) et haute qualité (llama3.1, mode différé) |

---

## Priorisation MoSCoW Release 1

| Priorité | Features |
|----------|---------|
| **Must** | F1 Auth · F2 Upload · F3 Génération · F4 Correction · F5 Score · F6 Historique |
| **Should** | Pages légales RGPD · Feedback pendant génération |
| **Could** | Mode sombre (déjà fourni dans la base) |
| **Won't** | Mode enseignant · Export PDF · Dashboard avancé |
