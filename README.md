# Obywatel BIELIK API

Repozytorium zawierające backend aplikacji Obywatel BIELIK napisany w Pythonie.

## Opis projektu

Obywatel BIELIK to aplikacja służąca do gromadzenia opisów zdjęć (anotacji) przez społeczność, w tym seniorów i lokalnych aktywistów. Aplikacja umożliwia użytkownikom opisywanie losowych zdjęć lub dodawanie własnych zdjęć wraz z opisami.

## Struktura projektu

```
obywatel-bielik-api/
├── app/                  # Główny katalog aplikacji
│   ├── __init__.py       # Inicjalizacja aplikacji
│   ├── config/           # Konfiguracja aplikacji
│   ├── api/              # Endpointy API
│   ├── models/           # Modele danych
│   ├── services/         # Logika biznesowa
│   ├── schemas/          # Schematy walidacji danych
│   └── utils/            # Narzędzia pomocnicze
├── migrations/           # Migracje bazy danych
├── tests/                # Testy
│   ├── unit/             # Testy jednostkowe
│   └── integration/      # Testy integracyjne
├── .env.example          # Przykładowy plik zmiennych środowiskowych
├── requirements.txt      # Zależności produkcyjne
├── requirements-dev.txt  # Zależności deweloperskie
├── Dockerfile            # Definicja kontenera Docker
└── docker-compose.yml    # Konfiguracja Docker Compose
```

## Technologie

- **Język programowania:** Python 3.10+
- **Framework API:** FastAPI
- **ORM:** SQLAlchemy
- **Migracje bazy danych:** Alembic
- **Uwierzytelnianie:** JWT / OAuth2
- **Testowanie:** pytest
- **Dokumentacja API:** Swagger / OpenAPI

## Funkcjonalności API

- Rejestracja i uwierzytelnianie użytkowników
- Zarządzanie zespołami
- Zarządzanie profilami użytkowników
- Obsługa celów tygodniowych i osiągnięć
- Uploading i pobieranie zdjęć
- Tworzenie i zarządzanie anotacjami
- Generowanie automatycznych opisów zdjęć
- Weryfikacja i korygowanie opisów
- Statystyki i rankingi użytkowników

## Ustawienie środowiska deweloperskiego

### Wymagania

- Python 3.10 lub nowszy
- PostgreSQL 13 lub nowszy
- Virtualenv

### Instalacja

1. Utwórz i aktywuj wirtualne środowisko:
```
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows
```

2. Zainstaluj zależności:
```
pip install -r requirements-dev.txt
```

3. Skopiuj plik `.env.example` do `.env` i dostosuj zmienne środowiskowe.

4. Uruchom migracje bazy danych:
```
alembic upgrade head
```

5. Uruchom serwer deweloperski:
```
uvicorn app.main:app --reload
```

## API Documentation

Dokumentacja API jest dostępna pod adresem `/docs` po uruchomieniu serwera.

## Testy

Aby uruchomić testy:

```
pytest
```

## Wdrożenie

Instrukcje wdrożenia znajdują się w repozytorium [obywatel-bielik-infra](https://github.com/organization/obywatel-bielik-infra).

## Licencja

Projekt jest dostępny na licencji [licencja]. Szczegółowe informacje w pliku LICENSE.
