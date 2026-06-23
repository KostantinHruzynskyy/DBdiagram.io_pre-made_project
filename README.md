---------------ITA--------------------

# 📊 Database Diagrams Collection

Una raccolta di progetti di database progettati con [DBDiagram.io](https://dbdiagram.io/).

L'obiettivo di questa repository è documentare, organizzare e condividere diversi schemi di database, dai modelli più semplici fino a strutture più complesse utilizzate per applicazioni reali.

## 🚀 Contenuto della Repository

Ogni cartella contiene:

- Diagramma del database (`.dbml`)
- Screenshot del diagramma
- Documentazione delle tabelle
- Relazioni tra entità
- Eventuali script SQL generati

### Struttura

<!-- database-diagrams/
│
├── songs-database/
│ ├── songs.dbml
│ ├── schema.sql
│ └── README.md
│
├── library-management/
│ ├── library.dbml
│ ├── schema.sql
│ └── README.md
│
├── ecommerce/
│ ├── ecommerce.dbml
│ ├── schema.sql
│ └── README.md
│
└── README.md -->


## 🛠️ Tecnologie Utilizzate

- DBDiagram.io
- DBML (Database Markup Language)
- MySQL
- PostgreSQL
- SQL

## 📚 Cos'è DBML?

DBML (Database Markup Language) è un linguaggio semplice e leggibile per definire strutture di database.

Esempio:

dbml
Table users {
  id int [pk, increment]
  username varchar(100) [not null]
  email varchar(255) [unique]
  created_at timestamp
}

Progetti Inclusi
🎵 Songs Database

Database semplice per la gestione di una libreria musicale.

Caratteristiche:

Gestione canzoni
Artisti
Album
Generi musicali
Conteggio riproduzioni
📚 Library Management

Sistema per la gestione di una biblioteca.

Caratteristiche:

Libri
Autori
Prestiti
Utenti
🛒 E-Commerce Database

Schema relazionale per un negozio online.

Caratteristiche:

Prodotti
Ordini
Clienti
Pagamenti
🎯 Obiettivi del Repository
Praticare Database Design
Imparare DBML
Costruire un portfolio di progetti database
Documentare relazioni e normalizzazione
Convertire diagrammi in SQL
🔗 Risorse Utili
DBDiagram: https://dbdiagram.io
DBML Documentation: https://dbml.dbdiagram.io/docs
MySQL Documentation: https://dev.mysql.com/doc/
PostgreSQL Documentation: https://www.postgresql.org/docs/
🤝 Contributi

I contributi sono benvenuti.

Fork della repository

Crea un branch:

git checkout -b feature/new-diagram

Commit:

git commit -m "Add new database diagram"

Push:

git push origin feature/new-diagram
Apri una Pull Request
📄 Licenza

Distribuito sotto licenza MIT.

Disclaimer:

Per una repository portfolio personale, puoi anche aggiungere badge GitHub, screenshot dei diagrammi e una sezione "Roadmap" con i database che intendi progettare in futuro.

----------------ENG------------------


# 📊 Database Diagrams Collection

A collection of database projects designed with DBDiagram.io.

The goal of this repository is to document, organize, and share various database schemas, ranging from simple models to more complex structures used in real-world applications.

## 🚀 Repository Contents

Each project folder contains:

* Database diagram (`.dbml`)
* Diagram screenshot
* Table documentation
* Entity relationships
* Generated SQL scripts (when available)

## 🛠️ Technologies Used

* DBDiagram.io
* DBML (Database Markup Language)
* MySQL
* PostgreSQL
* SQL

## 📚 What is DBML?

DBML (Database Markup Language) is a simple and human-readable language used to define database structures.

Example:

dbml
Table users {
  id int [pk, increment]
  username varchar(100) [not null]
  email varchar(255) [unique]
  created_at timestamp
}


## 📂 Included Projects

### 🎵 Songs Database

A simple database for managing a music library.

Features:

* Song management
* Artists
* Albums
* Music genres
* Play count tracking

### 📚 Library Management

A database system for managing a library.

Features:

* Books
* Authors
* Loans
* Users

### 🛒 E-Commerce Database

A relational database schema for an online store.

Features:

* Products
* Orders
* Customers
* Payments

## 🎯 Repository Goals

* Practice database design
* Learn DBML
* Build a database design portfolio
* Document relationships and normalization
* Convert diagrams into SQL schemas

## 🔗 Useful Resources

* DBDiagram: https://dbdiagram.io
* DBML Documentation: https://dbml.dbdiagram.io/docs
* MySQL Documentation: https://dev.mysql.com/doc/
* PostgreSQL Documentation: https://www.postgresql.org/docs/

## 🤝 Contributing

Contributions are welcome.

1. Fork the repository

2. Create a new branch:

```bash
git checkout -b feature/new-diagram
```

3. Commit your changes:

```bash
git commit -m "Add new database diagram"
```

4. Push to your branch:

```bash
git push origin feature/new-diagram
```

5. Open a Pull Request

## 📄 License

This project is distributed under the MIT License.

## ⚠️ Disclaimer

This repository is intended for educational purposes, learning database design principles, and building a personal portfolio. Database schemas may be updated, improved, or expanded over time as new projects are added.

---

Created to practice Database Design, SQL, and DBDiagram.io.
