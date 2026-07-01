# Product Vision Board — EduTutor IA

**Date :** 29/06/2026 · **Équipe :** EduTutor Groupe 14

---

## Vision

> Permettre à tout étudiant du supérieur de transformer son cours en quiz personnalisé en moins de 15 secondes, sans jamais exposer ses données à un tiers.

---

## Cible

| Segment | Description |
|---------|-------------|
| Primaire | Étudiant·e du supérieur (BTS, Licence, Master) qui veut réviser à partir de ses propres cours |
| Secondaire émergente | Enseignant·e (persona Mme Lefèvre) qui veut créer des supports d'évaluation pour sa classe |

---

## Besoins

| Problème | Solution EduTutor IA |
|----------|----------------------|
| Créer des QCM à la main est trop long | Génération automatique en < 15s à partir d'un PDF ou texte |
| Les banques de questions génériques sont hors-sujet | Questions ancrées dans le cours réel de l'étudiant (RAG) |
| Les outils concurrents envoient les données aux USA | Ollama local : aucune donnée ne quitte le serveur |
| L'étudiant ne sait pas où il en est | Historique des scores et révision des erreurs |

---

## Proposition de valeur unique

**Enseignant-first · RAG · RGPD local-first**

Là où Quizlet, Wilgo et Khanmigo sont étudiant-first et cloud-first, EduTutor IA est la seule plateforme à combiner des prompts métier pensés pour les enseignants, une génération ancrée dans le document fourni, et une conformité RGPD native (Ollama local).

---

## Objectifs produit (Release 1 — MVP)

| Objectif | Indicateur de succès |
|----------|----------------------|
| Générer un quiz de 10 QCM | p95 < 15s |
| Authentification sécurisée | Validation email fonctionnelle |
| Historique utilisateur | Score et date persistés par compte |
| Conformité RGPD | Aucune donnée transmise hors serveur |

---

## Périmètre Release 1 (Must have)

F1 · Inscription/connexion email avec validation
F2 · Upload PDF ≤ 5 Mo ou texte ≥ 200 caractères
F3 · Génération 10 QCM via LLM local (llama3.2)
F4 · Soumission et correction automatique
F5 · Score /10 + détail des réponses
F6 · Historique des quizz par utilisateur

## Hors périmètre Release 1

- Mode enseignant avancé (Mme Lefèvre) → Release 2
- RAG sur PDF long > 5 Mo → Release 2
- Génération différée haute qualité (llama3.1) → Release 2
