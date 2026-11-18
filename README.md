# Banking app: software testing project

A Spring Boot banking API built for a software testing course (INF352, University of Yaoundé I). The point of this project is less the API itself than the way it is tested: unit tests, equivalence partitioning, boundary values, integration tests, end-to-end tests and code coverage.

Version française plus bas.

## The API

- Users, banks and bank accounts
- Deposits, withdrawals and transfers
- Token-based access
- Swagger documentation
- PostgreSQL in production, H2 in-memory database for tests

Stack: Java 17, Spring Boot (Web, Data JPA, Validation), PostgreSQL, H2, Maven, Docker.

## The tests

| Folder (`src/test/java/com/banking`) | Technique |
|---|---|
| `unitaires/` | Unit tests of services and business rules |
| `partitioning/` | Equivalence partitioning: one test per class of valid and invalid inputs |
| `boundary/` | Boundary value analysis: amounts at 0, at the limit, just above and just below |
| `integration/` | Controllers, services and database working together |
| `system/` | End-to-end scenarios across the whole API |

Other material:

- `CFG/` and `CFG.pdf`: control flow graphs of the main methods, used to design the white-box tests
- `TestCaseGlobal.pdf`: the full list of test cases
- `coverage/`: coverage results
- `rapport_technique.pdf`: the technical report

## Run it

```bash
./mvnw test             # run all the tests
./mvnw spring-boot:run  # start the API
```

A later version of this project, with a Node.js backend and a Vue.js frontend, is in [TP352_FINAL](https://github.com/oberlinkeyanfe-ops/TP352_FINAL).

---

## Version française

API bancaire Spring Boot réalisée pour le cours de test logiciel INF352 (Université de Yaoundé I). L'intérêt principal du projet est la stratégie de test : tests unitaires, partitionnement en classes d'équivalence, valeurs limites, tests d'intégration, tests de bout en bout et couverture de code. Les graphes de flot de contrôle (CFG), la liste des cas de test et le rapport technique sont fournis en PDF.

Pour lancer les tests : `./mvnw test`.
