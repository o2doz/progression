# Progression annuelle — 2e année (3 h par semaine)

**Volume prévu : 30 semaines, soit environ 90 heures.**

## Objectifs de fin d’année

À l’issue de l’année, les étudiants doivent être capables de :

- modéliser un problème simple avec des diagrammes UML ;
- appliquer les principes essentiels de la programmation orientée objet (encapsulation, composition, héritage et polymorphisme) ;
- organiser une application selon le modèle MVC ;
- concevoir une API REST Python avec authentification basique et persistance PostgreSQL ;
- utiliser Docker dans un contexte de développement ;
- transposer les acquis d’OOP et de MVC de Python vers C# ;
- réaliser un petit projet Raylib structuré en objets.

Le rythme privilégie des démonstrations courtes, de la pratique guidée, puis des temps de consolidation et de correction collective adaptés à un groupe avançant progressivement.

---

## Bloc 1 — Python, OOP et MVC : projet pynotes (environ 16h)

**Objectif :** construire puis faire évoluer une application de notes en Python afin d’installer les bases de l’OOP et de MVC.

| Séance / activité | Description |
|---|---|
| **Prise en main : NoteApp minimale** | Rappels Python utiles au projet ; créer une note, lister les notes et sauvegarder des données simples. |
| **Objet `Note`** | Transformer les données en classe ; travailler constructeur, attributs, méthodes et représentation d’un objet. |
| **Encapsulation** | Ajouter validation et propriétés (titre obligatoire, contenu, date) ; comprendre la responsabilité d’une classe. |
| **Objet `NoteRepository`** | Gérer une collection de notes ; pratiquer composition, méthodes de recherche et séparation des responsabilités. |
| **Découvrir MVC** | Identifier modèle, vue et contrôleur dans une version existante ; déplacer le code dans une structure MVC simple. |
| **Menus et contrôleurs** | Implémenter des actions utilisateur : créer, consulter, modifier et supprimer une note sans mélanger affichage et métier. |
| **Évolution et tests manuels** | Ajouter tags ou recherche ; vérifier que les changements restent localisés grâce à MVC. |
| **Atelier de consolidation NoteApp** | Finaliser, relire et présenter le projet ; bilan OOP/MVC avec correction collective. |

---

## Bloc 2 — Modélisation UML (environ 8h)

**Objectif :** savoir communiquer une conception avant de coder et relier les diagrammes aux classes Python.

| Séance / activité | Description |
|---|---|
| **Lire un diagramme de classes** | Classes, attributs, opérations, visibilités et relations ; reconstituer les objets de NoteApp à partir d’un diagramme. |
| **Diagramme de classes de NoteApp** | Produire en binôme le diagramme des classes `Note`, `Notebook` et des éléments MVC ; justifier les relations. |
| **Cas d’utilisation et séquences** | Décrire les acteurs et le scénario « créer une note » ; introduire les échanges entre vue, contrôleur et modèle. |
| **Conception du Quest Engine** | À partir d’un besoin fourni, identifier entités et relations (`Quest`, `User`, objectifs…) et valider un premier diagramme. |

---

## Bloc 3 — Docker et PostgreSQL (environ 2h)

**Objectif :** lancer un environnement de développement reproductible contenant Python et PostgreSQL.

| Séance / activité | Description |
|---|---|
| **Pourquoi Docker ?** | Images, conteneurs, volumes et ports ; exécuter une image Python puis une image PostgreSQL avec des commandes simples. |
| **Premier `Dockerfile` Python** | Conteneuriser un petit script Python ; utiliser `requirements.txt` et reconstruire l’image après une modification. |
| **PostgreSQL en conteneur** | Démarrer PostgreSQL, créer une base et une table ; se connecter avec un client SQL et effectuer quelques requêtes CRUD. |
| **Environnement avec Compose** | Écrire un `compose.yaml` reliant application Python et base PostgreSQL ; utiliser variables d’environnement et volume persistant. |

---

## Bloc 4 — API Quest Engine avec authentification basique (semaines 17 à 24, 24 h)

**Objectif :** développer progressivement une API REST Python persistante et documentée, en réutilisant UML, OOP, MVC, Docker, PostgreSQL et des requêtes SQL simples.

| Séance / activité | Description |
|---|---|
| **Anatomie d’une API REST** | Routes, verbes HTTP, codes de statut et JSON ; créer une première route de santé (`GET /health`). |
| **Architecture MVC de l’API** | Organiser routes/contrôleurs, services métier et accès aux données ; relier l’architecture au diagramme UML. |
| **Schéma SQL et premières requêtes** | Créer les tables `users` et `quests` dans PostgreSQL ; connecter Python à la base et exécuter des requêtes paramétrées. |
| **CRUD des quêtes : lecture et création** | Implémenter et tester `GET /quests`, `GET /quests/{id}` et `POST /quests` avec PostgreSQL et un client HTTP. |
| **CRUD des quêtes : modification et suppression** | Ajouter `PUT`/`PATCH` et `DELETE` ; gérer les ressources absentes et les données invalides. |
| **Utilisateurs et mot de passe** | Créer les utilisateurs ; comprendre pourquoi un mot de passe est haché et ne jamais le stocker en clair. |
| **Authentification Basic** | Protéger des routes avec une authentification HTTP Basic ; tester les réponses 401/403 et les droits simples. |
| **Intégration et démonstration API** | Lancer l’API et PostgreSQL avec Docker Compose ; documenter les routes, faire une démonstration et une revue de code guidée. |

---

## Bloc 5 — Passage à C# et projet Raylib orienté objet (semaines 25 à 30, 18 h)

**Objectif :** transférer les principes déjà acquis vers C# à travers un mini-jeu Raylib volontairement limité : par exemple **« Arena de quêtes »**, où un joueur se déplace, récupère des objectifs et évite des ennemis.

| Séance / activité | Description |
|---|---|
| **Python vers C#** | Découvrir le projet .NET, les types, classes, propriétés et constructeurs ; réécrire une petite classe `Quest` en C#. |
| **OOP en C#** | Encapsulation, collections et composition ; modéliser `Player`, `Quest` et `GameWorld` à partir d’un diagramme de classes. |
| **Raylib : boucle de jeu** | Créer une fenêtre, dessiner des formes et mettre en place la boucle `update/draw` ; déplacer un objet joueur. |
| **Objets du jeu** | Ajouter objectifs et obstacles/ennemis sous forme d’objets ; pratiquer interfaces ou héritage seulement lorsqu’ils apportent une vraie simplification. |
| **Organisation inspirée de MVC** | Séparer état du jeu, affichage Raylib et gestion des entrées/règles ; ajouter score, collision et condition de victoire. |
| **Finalisation et bilan** | Corriger, présenter le mini-jeu et expliciter les choix OOP/MVC ; bilan comparatif Python/C# et auto-évaluation. |

---

## Évaluation et suivi

- **Évaluation formative continue :** exercices courts, vérification de compréhension en début/fin de séance et corrections collectives.
- **Jalons :** NoteApp, diagrammes UML, environnement Docker/Python fonctionnel, API Quest Engine, projet Raylib.
- **Critères récurrents :** fonctionnement, lisibilité, responsabilités des classes, séparation MVC, qualité du modèle UML, utilisation correcte de Git/Docker et capacité à expliquer ses choix.
