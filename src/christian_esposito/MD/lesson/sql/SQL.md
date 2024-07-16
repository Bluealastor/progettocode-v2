### Cos'è SQL?

SQL (Structured Query Language) è un linguaggio standard utilizzato per interagire con i database relazionali. È utilizzato per eseguire varie operazioni sui dati memorizzati nei database, come creare, leggere, aggiornare e cancellare dati. Ecco alcuni dei comandi SQL più comuni:

- **SELECT**: recupera dati dal database.
- **INSERT**: inserisce nuovi dati nel database.
- **UPDATE**: aggiorna i dati esistenti nel database.
- **DELETE**: cancella dati dal database.
- **CREATE TABLE**: crea una nuova tabella nel database.
- **DROP TABLE**: elimina una tabella esistente dal database.

SQL è un linguaggio dichiarativo, il che significa che si specifica *cosa* si vuole ottenere senza dover dettagliare *come* ottenerlo.

### Esempio di una query SQL

Supponiamo di avere una tabella chiamata `employees` con le colonne `id`, `name`, `position` e `salary`. Una query per selezionare tutti i dipendenti con uno stipendio superiore a 50.000 potrebbe essere:

```sql
SELECT name, position
FROM employees
WHERE salary > 50000;
```

### Cos'è PostgreSQL?

PostgreSQL, spesso abbreviato in Postgres, è un sistema di gestione di database relazionale (RDBMS) open source molto potente. È noto per la sua conformità agli standard SQL, la sua robustezza e le sue funzionalità avanzate. PostgreSQL supporta una vasta gamma di tipi di dati e funzioni avanzate come:

- **Transazioni**: garantiscono che tutte le operazioni all'interno di una transazione vengano completate con successo prima di essere applicate al database.
- **Integrità dei dati**: attraverso l'uso di vincoli, chiavi esterne, trigger e viste.
- **Estensibilità**: permette agli utenti di definire nuovi tipi di dati, operatori, funzioni e indici.
- **Supporto per JSON**: oltre ai tradizionali tipi di dati relazionali, supporta anche la memorizzazione e l'interrogazione di dati in formato JSON.

### Esempio di utilizzo di PostgreSQL

Supponiamo di voler creare e popolare una tabella `employees` in PostgreSQL:

```sql
-- Creazione della tabella
CREATE TABLE employees (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100),
    position VARCHAR(50),
    salary NUMERIC(10, 2)
);

-- Inserimento dei dati
INSERT INTO employees (name, position, salary)
VALUES
('Alice', 'Manager', 60000),
('Bob', 'Developer', 50000),
('Charlie', 'Designer', 45000);

-- Selezione dei dati
SELECT * FROM employees;
```

### Caratteristiche distintive di PostgreSQL

- **ACID Compliance**: PostgreSQL aderisce ai principi ACID (Atomicity, Consistency, Isolation, Durability), garantendo transazioni affidabili.
- **Concurrency Control**: utilizza un sistema chiamato Multi-Version Concurrency Control (MVCC) per gestire la concorrenza senza bloccare le letture.
- **Supporto per estensioni**: PostgreSQL permette di aggiungere funzionalità tramite estensioni, come PostGIS per l'analisi spaziale.

In sintesi, SQL è il linguaggio utilizzato per interagire con i database relazionali, mentre PostgreSQL è un potente sistema di gestione di database relazionali che implementa il linguaggio SQL e offre molte funzionalità avanzate.