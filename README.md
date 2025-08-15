<!--
  Music Store / Chinook – SQL Analytics Project
  ------------------------------------------------
  Author : Atishay Jain
-->

# Music-Store SQL Analytics 📊🎶

A hands-on SQL project that dissects the classic **Chinook** (a.k.a. “Music Store”) sample database.  
You’ll learn how to load the schema, explore its relationships, and answer progressively tougher
business questions about customers, invoices, artists, genres and more.

<p align="center">
  <img src="docs/database_schema.png" alt="ER diagram" width="600">
</p>

---

## Table of Contents

1. [Project overview](#project-overview)  
2. [Tech stack](#tech-stack)  
3. [Database schema](#database-schema)  
4. [Question sets & solutions](#question-sets--solutions)  
5. [Getting started](#getting-started)  
6. [Repository structure](#repository-structure)  
7. [Contributing](#contributing)  
8. [License & attribution](#license--attribution)

---

## Project overview

* **Goal:** Practise real-world SQL by answering sales & marketing questions for a digital music shop.  
* **Difficulty levels:**  
  * *Easy* – introductory aggregations and ordering  
  * *Moderate* – multi-table joins, sub-queries & `DISTINCT`  
  * *Advanced* – CTEs, window functions, recursive queries  
* **Deliverables:**  
  * Re-usable `.sql` scripts containing every solution  
  * A PDF brief enumerating all questions you need to solve :contentReference[oaicite:0]{index=0}  

---

## Tech stack

| Layer | Choice | Why |
|-------|--------|-----|
| **Database** | PostgreSQL (>= 13) | open-source and widely used in production |
| **Client** | pgAdmin 4 / psql | GUI vs CLI – pick your preference |
| **Optional notebooks** | Jupyter + `psycopg2` | run SQL directly inside Python for ad-hoc analysis |

---

## Database schema

The Chinook ER-diagram (above) contains **11 tables** grouped by business domain:

| Domain | Tables | Notes |
|--------|--------|-------|
| **Catalog** | `Artist`, `Album`, `Track`, `Genre`, `MediaType`, `Playlist`, `PlaylistTrack` | Standard music-store hierarchy |
| **Sales** | `Invoice`, `InvoiceLine` | Line items let you compute revenue per track, artist, genre… |
| **People** | `Customer`, `Employee` | Includes manager chain (`reportsTo`) and geography fields |

---

## Question sets & solutions

| Difficulty | File | Topics covered |
|------------|------|----------------|
| **Easy** | `sql/01_easy.sql` | `GROUP BY`, `ORDER BY`, `LIMIT` |
| **Moderate** | `sql/02_moderate.sql` | joins across 4–5 tables, `DISTINCT`, sub-queries |
| **Advanced** | `sql/03_advanced.sql` | CTEs, window functions, recursion |

> All solutions reside in **[`Music Store Queries.sql`](sql/Music%20Store%20Queries.sql)** :contentReference[oaicite:1]{index=1} – open it in pgAdmin, execute section by section, and compare your results.

A concise copy of the questions lives in **[`docs/Music Store Analysis - Questions.pdf`](docs/Music%20Store%20Analysis%20-%20Questions.pdf)**. Feel free to extend the list with your own business curiosities!

---

## Getting started

### 1 · Clone the repo

```bash
git clone https://github.com/<your-handle>/chinook-analytics.git
cd music-store-sql-analysis
