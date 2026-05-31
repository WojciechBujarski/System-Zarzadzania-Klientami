# System zarządzania klientami (Colab + PostgreSQL)

Prosty, interaktywny system CRUD do zarządzania klientami napisany w Pythonie. Całość działa w środowisku Google Colab, a interfejs graficzny zbudowałem przy użyciu biblioteki `ipywidgets`. Aplikacja łączy się z zewnętrzną bazą danych PostgreSQL.

## Co robi ten skrypt?
* **Dodawanie i usuwanie** klientów z bazy (imię, nazwisko, telefon).
* **Wyświetlanie** aktualnej listy klientów.
* **Wyszukiwanie** konkretnych osób po Imieniu, Nazwisku lub numerze ID.
* Całość podzielona jest na wygodne zakładki, żeby nie trzeba było grzebać w kodzie, aby wykonać akcję na bazie.

## Technologie
* Python 3
* PostgreSQL
* Biblioteki: `psycopg2` (połączenie z bazą), `ipywidgets` (GUI)

## Jak to odpalić u siebie?

Skrypt jest przygotowany specyficznie pod Google Colab. Żeby nie trzymać haseł do bazy bezpośrednio w kodzie, użyłem wbudowanego menedżera zmiennych środowiskowych Colaba (`userdata`). 

Jeśli chcesz uruchomić ten notatnik na swojej bazie danych, zrób tak:

1. Otwórz plik w Google Colab.
2. Z lewej strony kliknij ikonę klucza (**Secrets**).
3. Dodaj nową zmienną o nazwie `DATABASE_URL` i wklej tam link do swojej bazy Postgres (w formacie `postgresql://user:password@host/dbname`).
4. Upewnij się, że zaznaczyłeś opcję **Notebook access** przy tej zmiennej.
5. Odpal wszystkie komórki w notatniku (Ctrl+F9).

## Podgląd aplikacji

Wszelkie dane klientów widoczne na zrzutach ekranu są całkowicie fikcyjne i zostały wygenerowane losowo na potrzeby prezentacji działania aplikacji.

![](Screenshots/MenuDodawania.png)
![](Screenshots/ListaKlientow.png)
![](Screenshots/UsunKlientaZlisty.png)
![](Screenshots/WyszukajKlienta.png)
![](Screenshots/WyszukajKlienta2.png)

