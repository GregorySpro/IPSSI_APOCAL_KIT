# Personas — EduTutor IA

**Date :** 29/06/2026 · **Équipe :** EduTutor Groupe 14

---

## Persona 1 — Lucas, étudiant en Licence 3 (cible primaire)

**"Je veux réviser vite et bien, sans perdre du temps à fabriquer des questions."**

| Attribut | Détail |
|----------|--------|
| Âge | 21 ans |
| Formation | Licence 3 Sciences de gestion, université Paris-Est |
| Situation | Période de partiels, 6 matières à réviser simultanément |
| Appareils | Laptop Windows, smartphone Android |
| Niveau tech | Intermédiaire — utilise Notion, Quizlet, YouTube |

### Objectifs
- Transformer ses prises de notes en quiz en quelques clics
- Savoir quelles notions il maîtrise et lesquelles il doit retravailler
- Réviser pendant ses transports (mobile-friendly)

### Frustrations
- Quizlet : les quiz sont génériques, pas alignés sur son cours
- ChatGPT : il faut copier-coller tout le cours, les réponses hallucinent
- Ses données uploadées partent "quelque part aux USA"

### Critères de succès
- Quiz généré en < 15 secondes après upload
- Questions pertinentes par rapport au cours fourni
- Score et historique visibles sans chercher

---

## Persona 2 — Mme Lefèvre, enseignante (cible secondaire — émergente J1)

**"Je veux préparer une évaluation formative en 10 minutes, pas en 2 heures."**

| Attribut | Détail |
|----------|--------|
| Âge | 44 ans |
| Poste | Professeure de biologie, lycée public, région Île-de-France |
| Situation | Charge de travail élevée, prépare 4 classes différentes |
| Appareils | PC fixe au lycée, tablette personnelle |
| Niveau tech | Basique à intermédiaire — utilise le ENT, PDF, emails |

### Objectifs
- Générer des QCM à partir de son cours (PDF) pour évaluer ses élèves
- Pouvoir relire, corriger et valider les questions avant utilisation
- S'assurer que les données de ses élèves ne quittent pas l'établissement

### Frustrations
- Les outils grand public sont trop génériques (niveau lycée mal calibré)
- Elle ne fait pas confiance aux outils qui "envoient les données à des Américains"
- Elle a besoin de questions vérifiables, pas d'hallucinations

### Critères de succès
- Questions alignées sur son cours (pas sur Wikipedia)
- Interface simple : upload → générer → relire → exporter
- Conformité RGPD explicite (mention visible dans l'interface)

---

## Persona 3 — Admin, DSI d'un établissement (arrière-plan)

**"Je dois pouvoir auditer ce qui tourne sur nos serveurs."**

| Attribut | Détail |
|----------|--------|
| Rôle | Responsable infrastructure, établissement supérieur |
| Priorité | Conformité réglementaire, maîtrise des coûts, disponibilité |

### Besoins clés
- Back-office pour configurer le fournisseur LLM et gérer les utilisateurs
- Logs d'utilisation et capacité à effacer les données (RGPD)
- Déploiement Docker documenté, reproductible
