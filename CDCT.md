# Cahier des Charges Technique (CDCT) – MetaBoard

## 1. Contexte & objectifs
**MetaBoard** est une plateforme modulable pour la gestion de projets, tickets, documentation et diagrammes de conception.  
L’objectif principal est de fournir un **outil centralisé** pour :  

- La gestion de tickets type Jira (workflow, assignations, priorités, commentaires, pièces jointes)  
- La création de **diagrammes** : BDD, systèmes, processus  
- La gestion de **cahiers de recettes et documents**  
- L’évolution vers de nouveaux modules de collaboration  

---

## 2. Public cible
- Équipes de développement (étudiants ou professionnels)  
- Gestionnaires de projets souhaitant centraliser workflow et documentation  
- Petites équipes nécessitant un outil modulable  

---

## 3. Fonctionnalités principales

### 3.1 Module Tickets / Workflow
- Création / modification / suppression de tickets  
- Tickets parents / enfants (hiérarchie)  
- Assignation à un ou plusieurs utilisateurs  
- Statuts et historique des changements (TicketStatus)  
- Catégories et types de tickets  
- Commentaires imbriqués (style subreddit)  
- Pièces jointes  
- Sprints / planification  

### 3.2 Module Projets
- Création / modification de projets  
- Association de tickets à un projet  
- Vue globale des projets et états  

### 3.3 Module Diagrammes (dans uns second temps)
- Création de diagrammes de type BDD / système / UML  
- Éditeur graphique simple  
- Export / import (PNG, SVG, JSON)  
- Gestion versionnée des diagrammes  

### 3.4 Module Documentation / Cahiers (dans un troisieme temps)
- Création et stockage de documents (cahiers de recettes, notes, guides)  
- Organisation en dossiers / projets  
- Permissions par utilisateur / rôle  
- Export PDF  

---

## 4. Architecture technique

### 4.1 Stack retenue
- **Frontend** : Vue 3 + Vite, Pinia pour state, Vue Router  
- **Backend** : Laravel 10 (API REST)  
- **Base de données** : MySQL / MariaDB  
- **Authentification** : Laravel Sanctum (API tokens)  
- **Stockage fichiers** : Laravel Storage ou S3 (selon besoin)  

### 4.2 Schéma général
- Front Vue → consomme API Laravel  
- Laravel gère logique métier et persistance  
- MySQL stocke projets, tickets, diagrammes, documents  

---

## 5. Modèle de données (simplifié)
- **User** : id, nom, email, password, rôle  
- **Role** : id, nom  
- **Project** : id, nom, description, dateStart  
- **Ticket** : id, title, description, parentTicketId, estimatedCharge, createdAt, closedAt  
- **TicketStatus** : id, ticketId, statusId, dateStart, changedByUserId  
- **Comment** : id, message, createdAt, parentCommentId  
- **Attachment** : id, fileName, fileType  
- **Sprint** : id, name, dateStart, dateEnd  
- **Diagram** : id, name, type, content JSON, projet associé  
- **Document** : id, name, type, content / fichier, projet associé  

---

## 6. Contraintes techniques
- Application responsive (desktop / tablette / mobile)  
- API sécurisée (authentification + permissions par rôle)  
- Modularité : possibilité d’ajouter de nouveaux modules  
- Performances : tables optimisées pour tickets et commentaires imbriqués  
- Export PDF / image pour diagrammes et documents  

---

## 7. Rôles et permissions
- **Admin** : accès complet à tous les projets, tickets et documents  
- **Project Manager** : gestion des tickets, sprints, documents du projet  
- **Développeur / Collaborateur** : création et suivi de tickets, commentaires  
- **Lecteur** : accès en lecture seule aux projets / diagrammes / documents  

---

## 8. Roadmap MVP
1. Module tickets complet (Jira-like)  
2. Module projets et assignations  
3. Module diagrammes simple (création / édition / export)  
4. Module documentation (cahiers / stockage)  
5. Améliorations UI / UX et intégration multi-modules  

---