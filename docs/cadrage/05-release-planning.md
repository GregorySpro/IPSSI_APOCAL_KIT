# Release Planning — EduTutor IA

**Date :** 29/06/2026 · **Équipe :** EduTutor Groupe 14

---

## Release 1 — MVP · Tag `v1.0.0-mvp` · Deadline : mercredi 01/07 17h45

### Objectif
Livrer un produit fonctionnel de bout en bout permettant à un étudiant de s'inscrire, déposer un cours, générer un quiz, le passer et consulter son historique — avec conformité RGPD et sécurité de base.

### Features incluses

| Feature | Statut base reprise | Travail restant |
|---------|---------------------|-----------------|
| F1 · Auth email (inscription, validation, reset, profil) | Partiellement présent | Finitions, tests cas limites |
| F2 · Upload PDF / texte | Partiellement présent | Validation 5 Mo, 200 chars |
| F3 · Génération 10 QCM (llama3.2 — ADR J2) | Présent avec llama3.1 | Bascule vers llama3.2 |
| F4 · Soumission et correction | Partiellement présent | Fiabilisation |
| F5 · Score /10 + détail | Partiellement présent | Finitions UI |
| F6 · Historique par utilisateur | Partiellement présent | Persistance vérifiée |
| Pages légales RGPD | Vierges | À rédiger (J3-bis) |
| Sécurité anti-injection | Absente | À implémenter (J3) |

### Critères de sortie (DoD Release 1)
- F1-F6 testables de bout en bout sans erreur
- Modèle llama3.2 actif (ADR documenté)
- Pages légales complétées
- Tests adversariaux prompt injection passants
- Tag `v1.0.0-mvp` posé sur le repo

---

## Release 2 — Évolutions · Tag `v1.1.0` · Deadline : jeudi 02/07 17h45

### Pistes retenues (à affiner avec le PO)

| Piste | Valeur | Effort estimé |
|-------|--------|---------------|
| Mode enseignant (Mme Lefèvre) | Nouveau segment, différenciation forte | Moyen |
| Dashboard progression (graphiques) | Fidélisation utilisateur | Faible (base fournie) |
| Révision des erreurs améliorée | Engagement, rétention | Faible (base fournie) |
| Génération haute qualité différée (llama3.1) | Qualité perçue enseignants | Faible (modèle déjà dispo) |
| Export quiz en PDF | Cas usage enseignant | Moyen |

### Features exclues Release 2
- Application mobile native
- Authentification SSO (ENT)
- RAG sur documents > 5 Mo
