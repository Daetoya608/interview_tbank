# Источники и материалы для повторения

## Вакансия и опыт

Описание команды и требования взяты из двух скриншотов, предоставленных Амалем в переписке 11 ноября 2026 года. Скриншоты не включены в репозиторий. Уточнение про работу над админкой Яндекса сообщено Амалем отдельно.

Сведения об опыте собраны из обсуждения задач и резюме в переписке. Точные алгоритмы, пороги, нагрузки и неизвестные детали не достроены: см. [список уточнений](11-details-to-recall.md).

## Официальная документация

| Тема | Материал | Что повторить |
| --- | --- | --- |
| Django ORM | [QuerySet API](https://docs.djangoproject.com/en/5.2/ref/models/querysets/) | select_related, prefetch_related, select_for_update, выполнение запросов |
| Транзакции Django | [Database transactions](https://docs.djangoproject.com/en/5.2/topics/db/transactions/) | atomic, границы транзакции, on_commit |
| PostgreSQL | [Using EXPLAIN](https://www.postgresql.org/docs/current/using-explain.html) | План, оценки и фактическое выполнение |
| Asyncio | [Coroutines and Tasks](https://docs.python.org/3/library/asyncio-task.html) | Задачи, отмена, gather, TaskGroup, таймауты |
| HTTPX | [Async Support](https://www.python-httpx.org/async/) | Переиспользование клиента и закрытие ресурсов |
| HTTPX | [Timeouts](https://www.python-httpx.org/advanced/timeouts/) | Connect, read, write и pool timeout |
| Повторы | [AWS Timeouts, retries and backoff with jitter](https://aws.amazon.com/builders-library/timeouts-retries-and-backoff-with-jitter/) | Идемпотентность, бюджет повторов, backoff и jitter |
| Backoff | [AWS Exponential Backoff and Jitter](https://aws.amazon.com/blogs/architecture/exponential-backoff-and-jitter/) | Зачем разносить повторные попытки во времени |
| Valkey | [INCR and rate limiter patterns](https://valkey.io/commands/incr/) | Атомарность счётчика и связки с TTL |
| Circuit breaker | [Microsoft Architecture Center](https://learn.microsoft.com/en-us/azure/architecture/patterns/circuit-breaker) | Closed, open, half-open и изоляция отказов |
| Авторизация | [Auth0 Validate Access Tokens](https://auth0.com/docs/secure/tokens/access-tokens/validate-access-tokens) | Audience и scopes, отличие валидности токена от доступа |

Django 5.2 используется как конкретная справочная версия; версия рабочих проектов и команды не установлена. Материалы других версий нужно сопоставлять с фактическим стеком. Документация Auth0 используется для объяснения принципов валидации токенов и не означает, что в Т-Банке применялся Auth0.

## Порядок чтения

Сначала Django QuerySet и транзакции, затем PostgreSQL EXPLAIN. После этого asyncio и HTTPX. Для разбора опыта шлюза — Valkey, circuit breaker и проверки токенов. AWS полезен для более глубоких вопросов про сбои внешних интеграций.

Не нужно читать всю документацию подряд: по каждому материалу подготовить ответ на конкретный вопрос из [разбора опыта](05-experience-questions.md).
