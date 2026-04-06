# Cahier des Charges Fonctionnel (CDCF) – MetaBoard

## 1. Objectif
MetaBoard est une plateforme modulable destinée à la **gestion de projets, tickets, diagrammes et documentation**.  
L’objectif du CDCF est de **décrire les besoins fonctionnels et les attentes des utilisateurs**, afin de guider le développement de l’application.

---

## 2. Public cible
- Équipes de développement (étudiants ou professionnels)  
- Chefs de projets / managers souhaitant centraliser les tâches et documents  
- Petites équipes nécessitant un outil collaboratif tout-en-un  

---

## 3. Besoins utilisateurs

### 3.1 Gestion des tickets
- Créer, modifier et supprimer des tickets  
- Gérer les tickets **parents / enfants**  
- Assigner un ou plusieurs utilisateurs à un ticket  
- Suivre le statut d’un ticket et son historique  
- Ajouter des commentaires **imbriqués**  
- Ajouter des pièces jointes  
- Organiser les tickets par **projet et sprint**  
- Filtrer / rechercher les tickets par statut, priorité, catégorie ou utilisateur  

### 3.2 Gestion des projets
- Créer, modifier et supprimer des projets  
- Visualiser tous les tickets associés à un projet  
- Suivre l’avancement global du projet  

### 3.3 Diagrammes
- Créer des diagrammes **BDD / systèmes / UML**  
- Éditer graphiquement les diagrammes  
- Importer / exporter diagrammes (PNG, SVG, JSON)  
- Versionner les diagrammes  

### 3.4 Documentation
- Créer et organiser des documents (cahiers de recettes, notes, guides)  
- Associer les documents à des projets ou diagrammes  
- Définir des permissions (lecture / écriture / modification)  
- Export PDF des documents  

### 3.5 Gestion des utilisateurs et rôles
- Créer des comptes utilisateurs  
- Définir des rôles : Admin, Project Manager, Collaborateur, Lecteur  
- Attribuer les permissions par rôle et par projet  

---

## 4. Parcours utilisateur (exemples)

### 4.1 Création et suivi d’un ticket
1. L’utilisateur crée un ticket dans un projet  
2. Il assigne des collaborateurs et choisit un statut initial  
3. Les utilisateurs concernés reçoivent une notification  
4. Les commentaires et pièces jointes sont ajoutés au fil du temps  
5. Le ticket est clôturé ou archivé lorsqu’il est terminé  

### 4.2 Gestion d’un projet
1. Le Project Manager crée un projet  
2. Il ajoute des tickets et des utilisateurs  
3. Il suit l’avancement via un tableau Kanban ou une liste  
4. Les diagrammes et documents liés sont accessibles depuis le projet  

### 4.3 Création d’un diagramme (dans un second temps)
1. L’utilisateur ouvre l’éditeur graphique  
2. Il crée ou modifie des entités, relations ou blocs  
3. Le diagramme est sauvegardé et versionné  
4. Il peut l’exporter ou le partager avec le projet  

---

## 5. Critères de réussite / objectifs fonctionnels
- Facilité d’utilisation et interface claire  
- Gestion complète des tickets avec historique et notifications  
- Collaboration efficace via commentaires et documents centralisés  
- Éditeur de diagrammes intuitif et exportable  
- Permissions adaptées aux rôles et aux projets  
- Recherche et filtrage rapide dans les tickets et documents  

---

## 6. Priorisation des fonctionnalités (MVP)
| Priorité | Fonctionnalité |
|----------|----------------|
| Haute    | Tickets : création, assignation, hiérarchie, statut |
| Haute    | Projets : création, association tickets |
| Moyenne  | Commentaires imbriqués et pièces jointes |
| Moyenne  | Diagrammes BDD / système avec export |
| Faible   | Cahiers de recettes et documents avec export PDF |
| Faible   | Gestion avancée des rôles et permissions |

---

## 7. Contraintes fonctionnelles
- Responsive : application utilisable sur desktop, tablette et mobile  
- Notifications en temps réel pour tickets et commentaires  
- Filtrage et recherche rapide  
- Historique complet des tickets et documents  
- Modularité : possibilité d’ajouter de nouvelles fonctionnalités ou modules  

---

## 8. Annexes
- Schéma simplifié des tickets et projets (issu du CDCT)  
- Exemple de parcours utilisateur et wireframes (à compléter)  
- Liste des rôles et permissions  

---