
# TP Spring Boot - Gestion des Étudiants

## Description
Ce projet est un TP pratique pour la création d'une application de gestion des étudiants avec Spring Boot. L'application permet d'effectuer des opérations CRUD (Create, Read, Update, Delete) sur des enregistrements d'étudiants stockés dans une base de données MySQL nommée `studentdb`.

## Prérequis
- **Java 22** (ou une version compatible)
- **Maven** pour la gestion des dépendances
- **MySQL** pour la base de données
- **Spring Boot** (version 3.x)
- **IDE** tel que IntelliJ IDEA ou Eclipse
- **Postman** ou tout autre outil similaire pour tester les requêtes API

## Installation
1. **Cloner le repository** :
   ```bash
   git clone https://github.com/ilham999-byte/tp-spring-boot.git
   cd tp-spring-boot


## Configurer la base de données : Créez la base de données studentdb dans MySQL :

CREATE DATABASE studentdb;
## Configurer application.properties :

spring.datasource.url=jdbc:mysql://localhost:3306/studentdb
spring.datasource.username=root
spring.datasource.password=
spring.jpa.hibernate.ddl-auto=update
## Lancer l'application :
mvn spring-boot:run
## Structure du projet
Controllers : Contient les classes qui gèrent les requêtes HTTP, comme StudentController.
Services : Contient la logique métier, avec StudentService pour les opérations CRUD.
Entity : Contient la classe Student qui représente la table students dans la base de données.
Repository : Interface pour l'accès aux données, utilisant JpaRepository.
## Exemples de Requêtes API
Ajouter un étudiant
POST /students/save
{
  "nom": "John Doe",
  "age": 22,
  "email": "johndoe@example.com"
}
Supprimer un étudiant
DELETE /students/delete/{id}

Récupérer tous les étudiants
GET /students/all

Compter les étudiants
GET /students/count

Récupérer le nombre d'étudiants par année
GET /students/byYear

## Documentation avec Swagger
L'application utilise Swagger pour documenter et tester les API. Accédez à la documentation Swagger à l'URL suivante après avoir démarré l'application :

http://localhost:8080/swagger-ui/index.html
## Auteur
Ilham Ettouil







