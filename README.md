# Senior Full-Stack Engineering Knowledge Base

Techniczne kompendium dla Senior Full-Stack Engineer (AWS + mikroserwisy + Node.js/TypeScript + PostgreSQL + React + SAP).

## Start

Otwórz [index.html](index.html) lokalnie w przeglądarce. Wszystkie linki między rozdziałami są względne, więc nie potrzeba serwera, bundlera ani instalacji.

## Rozdziały

- [AWS Lambda — deep dive: lifecycle, hot/cold state, concurrency, quotas i niezawodność](lambda.html)
- [Mikroserwisy i system design](architecture.html)
- [AWS: wybór usług i architektura](aws.html)
- [SQS, SNS i niezawodność zdarzeń](messaging.html)
- [Node.js i TypeScript](node-typescript.html)
- [PostgreSQL](postgres.html)
- [React i architektura frontendowa](react.html)
- [Clean Code i Design Patterns](patterns.html)
- [Integracje SAP](sap.html)
- [Strategia testowania](testing.html)
- [Pytania rekrutacyjne i plan](interview.html)

## Metoda nauki

Każdy blok ma trzy części: **mechanika działania**, **implikacje produkcyjne** i **trade-offy**. Baza celowo omija definicje podstawowe. Rozdziały mają zachowywać szczegóły istotne dla projektowania, debugowania i utrzymania systemów w produkcji.

Przewodni przykład: system zamówień z API Gateway, Node.js, PostgreSQL, transactional outbox, SQS i integracją SAP.

## Konwencja rozbudowy

- Jeden temat na osobny plik HTML lub rozszerzenie istniejącego rozdziału.
- Dopisuj scenariusze z produkcji, kod TypeScript/SQL, failure modes, monitoring oraz pytania rekrutacyjne.
- Zachowuj nawigację do innych rozdziałów i do index.html.
- Przy szczegółowych limitach, cenach i konfiguracji AWS weryfikuj aktualne oficjalne dokumenty przed wdrożeniem.

> Materiały są punktem wyjścia do pogłębienia i praktycznych laboratoriów, nie zastępują dokumentacji usług ani ćwiczeń hands-on.
