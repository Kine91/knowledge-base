# Review techniczny — 27.11.2026

## Status
Rozbudowano wszystkie główne obszary pierwotnej bazy. 19 rozdziałów technicznych i 1 spis treści, wspólny CSS, README. Własny drugi przebieg merytoryczny oraz automatyczna kontrola statyczna po pobraniu stron z main. **Nie jest to niezależne review osobnego agenta**: w sesji nie było narzędzia delegowania pracy. Nie przeprowadzono testów runtime kodu ani renderingu w przeglądarce.

## Pokrycie wymagań stanowiska

| Wymaganie | Rozdziały |
|---|---|
| AWS API Gateway, Lambda, EC2, Fargate, S3, SQS, SNS | aws, lambda, api-gateway, compute, messaging, s3, aws-security |
| Mikroserwisy i niezawodność | architecture, messaging, backend-api, data-messaging, operations, interview (case study) |
| Node.js / backend | node-typescript, backend-api, architecture |
| TypeScript | typescript, node-typescript, patterns |
| PostgreSQL | postgres, aws-security, backend-api, messaging |
| React, responsive UI, performance | react, testing |
| Clean Code / design patterns / code review | patterns, architecture, testing |
| SAP i integracja | sap, messaging, backend-api |
| Strategia testowania | testing, operations, interview (case study) |

## Weryfikacja i poprawki
- Odczytano 20 stron po zapisie; każdy rozdział ma nawigację do wszystkich pozostałych, wspólny stylesheet i dokładnie jedno aria-current=page. Brak wykrytych lokalnych brakujących kotwic, duplikatów id i linków do nieistniejących stron. Sprawdzono dodatkowo zmienione rozdziały AWS i ich powiązania.
- Usunięto sekcje pytań rekrutacyjnych; historyczny plik interview.html zawiera case study dla zachowania kompatybilnych linków.
- Zweryfikowano kluczowe zmienne limity AWS w oficjalnej dokumentacji: Lambda Event Functions (timeout, concurrency/RPS, payload, deployment), API Gateway (HTTP vs REST), SQS (1 MiB, visibility), SNS (domyślny payload i rozszerzony wariant), EventBridge (PutEvents, retry zależne od bus type), Step Functions (czas, historia, payload), Fargate (ephemeral storage), S3 (multipart i throughput).
- Poprawiono rozróżnienie sync/async Lambda RPS i użycie stable eventId przy idempotencji. Doprecyzowano FIFO batch handling i visibility timeout. Dodano przykłady capacity, polityk IAM, SQL, Node concurrency, React query key i testów awarii.
- Przejrzano granice gwarancji: trwałe przyjęcie vs zakończenie, outbox/inbox vs zewnętrzne side effects, SAP unknown outcome, DB failover, rate limit i backpressure.

## Ograniczenia i otwarte obszary
- Nie ma jednej wyczerpującej bazy dla wszystkich wersji usług, bibliotek i konfiguracji. Każdy rozdział ma linki referencyjne; nie sprawdzono automatycznie dostępności każdego zewnętrznego URL.
- Przykłady kodu są ilustracjami mechaniki, nie kompletnymi wdrożeniami; przed użyciem produkcyjnym potrzebują konfiguracji, typów/helperów, testów i security review.
- SAP: konkretne API, wersja, moduły, wymagania biznesowe i transport pozostają nieznane. Opisy warunkowe, bez założeń o środowisku pracodawcy.
- Kolejne możliwe pogłębienia zależne od potrzeb: ćwiczenia na realnym AWS (IaC i quotas), rozbudowane plany EXPLAIN na danych testowych, pgBouncer/RDS Proxy pinning z pomiarami, React profiling na rzeczywistym projekcie, zaawansowane CSS/a11y, multi-account governance, szczegółowe konfiguracje IAM/KMS, contract tests i failover drill. Nie są to deklaracje wykonanych testów.
