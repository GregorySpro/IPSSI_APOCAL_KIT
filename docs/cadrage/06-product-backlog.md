# Product Backlog — EduTutor IA

**Date :** 29/06/2026 · **Équipe :** EduTutor Groupe 14
**Méthode :** MoSCoW · Critères INVEST · DoR / DoD définis

---

## Définition of Ready (DoR)
Une story est prête à être prise en sprint si :
- [ ] Elle est rédigée au format "En tant que... je veux... afin de..."
- [ ] Elle a des critères d'acceptation clairs et testables
- [ ] Elle est estimée (points de complexité)
- [ ] Elle ne dépend pas d'une story non terminée

## Définition of Done (DoD)
Une story est terminée si :
- [ ] Le code est commité sur GitHub avec un message Conventional Commits
- [ ] Les critères d'acceptation sont tous vérifiés manuellement
- [ ] Aucune régression sur les stories précédentes
- [ ] La feature est déployable via `docker compose up`

---

## Backlog Release 1 — Must Have

### US-01 · Inscription par email
**En tant qu'** étudiant, **je veux** créer un compte avec mon email, **afin de** pouvoir accéder à EduTutor IA.
- CA1 : L'inscription échoue si l'email est déjà utilisé
- CA2 : Un email de validation est envoyé après inscription
- CA3 : Le compte est inutilisable avant validation de l'email
- **Estimation :** 3 pts · **MoSCoW :** Must

### US-02 · Validation email
**En tant qu'** étudiant inscrit, **je veux** valider mon adresse email via un lien, **afin de** sécuriser mon compte.
- CA1 : Le lien expire après 24h
- CA2 : Un bouton "Renvoyer le lien" est disponible depuis l'app
- **Estimation :** 2 pts · **MoSCoW :** Must

### US-03 · Connexion / Déconnexion
**En tant qu'** étudiant, **je veux** me connecter avec email + mot de passe, **afin d'** accéder à mon espace personnel.
- CA1 : 5 tentatives échouées → blocage temporaire 15 min
- CA2 : La déconnexion invalide le token JWT
- **Estimation :** 2 pts · **MoSCoW :** Must

### US-04 · Réinitialisation du mot de passe
**En tant qu'** étudiant, **je veux** recevoir un lien de réinitialisation par email, **afin de** retrouver l'accès à mon compte.
- CA1 : Le lien expire après 1h
- CA2 : L'ancien mot de passe est invalidé dès le reset
- **Estimation :** 2 pts · **MoSCoW :** Must

### US-05 · Upload d'un cours PDF
**En tant qu'** étudiant, **je veux** uploader un PDF de cours (≤ 5 Mo), **afin de** générer un quiz à partir de son contenu.
- CA1 : Fichiers > 5 Mo refusés avec message d'erreur explicite
- CA2 : Seuls les fichiers .pdf sont acceptés
- CA3 : Le texte est extrait et transmis au LLM
- **Estimation :** 3 pts · **MoSCoW :** Must

### US-06 · Saisie d'un cours en texte
**En tant qu'** étudiant, **je veux** coller mon cours directement dans un champ texte, **afin de** ne pas avoir à créer un PDF.
- CA1 : Minimum 200 caractères requis (validation côté serveur)
- CA2 : Message d'erreur si le champ est trop court
- **Estimation :** 1 pt · **MoSCoW :** Must

### US-07 · Génération de 10 QCM
**En tant qu'** étudiant, **je veux** que l'app génère automatiquement 10 questions QCM, **afin de** me tester sur mon cours.
- CA1 : Exactement 10 questions avec 4 options chacune (A/B/C/D)
- CA2 : Une seule bonne réponse par question
- CA3 : Génération en moins de 15s (p95) sur serveur de référence
- CA4 : Modèle llama3.2 utilisé (cf. ADR-001)
- **Estimation :** 5 pts · **MoSCoW :** Must

### US-08 · Soumission et correction
**En tant qu'** étudiant, **je veux** soumettre mes réponses et obtenir la correction, **afin de** savoir lesquelles sont correctes.
- CA1 : Toutes les questions doivent avoir une réponse avant soumission
- CA2 : La correction est calculée côté serveur (non falsifiable)
- **Estimation :** 3 pts · **MoSCoW :** Must

### US-09 · Affichage du score
**En tant qu'** étudiant, **je veux** voir mon score /10 et le détail des bonnes/mauvaises réponses, **afin de** comprendre mes erreurs.
- CA1 : Score affiché sous forme X/10
- CA2 : Chaque question indique si la réponse était juste ou fausse
- CA3 : La bonne réponse est révélée pour les questions ratées
- **Estimation :** 2 pts · **MoSCoW :** Must

### US-10 · Historique des quizz
**En tant qu'** étudiant, **je veux** consulter la liste de mes quizz passés, **afin de** suivre ma progression.
- CA1 : Chaque entrée affiche : date, nom du cours, score
- CA2 : L'historique est filtré par utilisateur connecté (isolation des données)
- CA3 : Trié par date décroissante
- **Estimation :** 3 pts · **MoSCoW :** Must

---

## Backlog Release 1 — Should Have

| ID | User Story | Estimation | MoSCoW |
|----|-----------|-----------|--------|
| US-11 | Pages légales RGPD complétées (CGU, Politique de confidentialité, Mentions légales, Cookies) | 2 pts | Should |
| US-12 | Feedback visuel pendant la génération (loader + message) | 1 pt | Should |
| US-13 | Gestion du profil utilisateur (modifier email, supprimer compte) | 2 pts | Should |

---

## Backlog Release 2 — Could Have / Won't (Release 1)

| ID | User Story | MoSCoW R1 | Cible |
|----|-----------|-----------|-------|
| US-20 | Mode enseignant : génération de quiz pour une classe | Won't R1 | R2 |
| US-21 | Dashboard progression avec graphiques | Could | R2 |
| US-22 | Révision ciblée des erreurs (mode flashcard) | Could | R2 |
| US-23 | Génération haute qualité différée (llama3.1) | Won't R1 | R2 |
| US-24 | Export quiz en PDF | Won't R1 | R2 |
