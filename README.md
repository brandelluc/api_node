# API avec Node.js et SQLite
Cette API permet de tester les requêtes GET, POST, PUT et DELETE avec deux tables dans une base de données SQLite. Les exemples d'utilisation sont fournis pour Postman.

# Prérequis

Installer SQLite et node.js

# Installation
## Clonez le dépôt :

git clone https://github.com/votre-repo/nom-du-projet.git
cd nom-du-projet

## Installez les dépendances :

npm install

## Démarrez le serveur :

node app.js

Le serveur sera accessible sur http://localhost:3000.

# Configuration de la base de données
Créez une base de données SQLite avec deux tables. 
Par exemple :
```sql
CREATE TABLE products (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  champ2 TEXT,
  champ3 TEXT
);

CREATE TABLE acheteur (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  champ2 TEXT,
  champ3 TEXT
);
```
# Routes API
## GET all
Récupérer tous les enregistrements d'une table.

URL : http://localhost:3000/{table_name}
Méthode HTTP : GET
Exemple avec Postman :
URL : http://localhost:3000/table1
Méthode : GET
## GET par ID
Récupérer un enregistrement spécifique par son ID.

URL : http://localhost:3000/{table_name}/{id}
Méthode HTTP : GET
Exemple avec Postman :
URL : http://localhost:3000/table1/1
Méthode : GET
## POST
Ajouter un nouvel enregistrement dans une table.

URL : http://localhost:3000/{table_name}
Méthode HTTP : POST
Corps de la requête :

```json
{
  "champ2": "...",
  "champ3": "..."
}
```
Exemple avec Postman :
URL : http://localhost:3000/table1
Méthode : POST
Corps de la requête :
```json
{
  "champ2": "...",
  "champ3": "..."
}
```
## PUT
Mettre à jour un enregistrement existant par son ID.

URL : http://localhost:3000/{table_name}/{id}
Méthode HTTP : PUT
Corps de la requête :
```json
{
  "champ2": "...",
  "champ3": "..."
}
```
Exemple avec Postman :
URL : http://localhost:3000/table1/1
Méthode : PUT
Corps de la requête :
```json
{
  "champ2": "...",
  "champ3": "..."
}
```
## DELETE
Supprimer un enregistrement existant par son ID.

URL : http://localhost:3000/{table_name}/{id}
Méthode HTTP : DELETE
Exemple avec Postman :
URL : http://localhost:3000/table1/1
Méthode : DELETE
Exécution des tests avec Postman
Ouvrez Postman.
Créez une nouvelle requête en sélectionnant la méthode HTTP appropriée (GET, POST, PUT, DELETE).
Entrez l'URL comme spécifié ci-dessus.
Pour les requêtes POST et PUT, sélectionnez l'onglet "Body", choisissez "raw" et "JSON" et entrez les données du corps de la requête.
Envoyez la requête et vérifiez la réponse.
