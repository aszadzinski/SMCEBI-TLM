## Zaliczenie 2021/2022

- [Punktacja](#Punktacja)
- [Opisy projektu](#Opisy-projektu)
	* [Temat 1](#Temat-1)
	* [Temat 2](#Temat-2)
	* [Temat 3](#Temat-3)
- [Work-flow](#Work-flow)
	* [Założenia projektu](#Założenia-projektu)
	* [Środowisko deweloperskie](#Środowisko-deweloperskie)

>Deadline dla **zadań**: czwartek przed zajęciami, Deadline dla **projektu**: termin 1: 27.01.22 16:00 
>
>Kolokwium poprawkowe (dla chętnych) termin 1: 28.01.22 9:45-11:15. [Treść kolokwium](kolokwium280122.md)

---

## Punktacja

**ocena końcowa**: średnia z wykonanych zadań i projektu (każda część minimum: dst)

- **5 zadań**, każde za 1ptk  (deadline: czwartek 23:59):
	- 0 zadań: **ndst**
	- 1 zadanie: **dst**
	- 2 zadania: **dst+**
	- 3 zadania: **db**
	- 4 zadania: **db+**
	- 5 zadania: **bdb**
- **Projekt** zaliczeniowy (5 osobowe grupy). Punktowanie:
	- 13ptk, Praca z programem GIT
		- 4ptk, Tworzenie commitów, podstawowe funkcje
		- 4ptk, Praca na gałęziach
		- 3ptk, Dodatkowe elementy (m.in. podpisy commitów, git-flow)
		- 2ptk, Wykorzystanie funkcjonalności GitHub'a (m.in. praca z użyciem pull requestów)
	- 11ptk, Praca z programem Docker
		- 3ptk, Tworzenie Dockerfile
		- 3ptk, Tworzenie docker-compose.yml
		- 2ptk, Prawidłowe wykorzystanie volumenów i sieci 
		- 3ptk, Ogólna praca z programem (m.in. poprawne zarządzanie kontenerami)
	- 1ptk, ~Praca z CMAKE~, ~poprawny cmakelist~, Makefile
	- 5ptk, Automatyczne generowanie dokumentacji
	- 10ptk, Efekt końcowy; Sposób w jaki połączono projekt w całość, jak podzielono pracę, czy zrealizowano założenia projektu. Dodatkowe elementy (struktura i opisy projektu, oskryptowanie, testy itp.).
- ocena projektu *40ptk*:
	- 0-20ptk: **ndst**
	- 21-24ptk: **dst**
	- 25-28ptk: **dst+**
	- 29-32ptk: **db**
	- 33-36ptk: **db+**
	- 37-40ptk: **bdb**

---

## Opisy-projektu


Zbuduj aplikację opartą na znajdującym się w repozytorium [LINK](https://github.com/SMCEBI-didactics/WebApplication) rdzeniu o funkcjonalności z tematów 1, 2 lub 3.


### Temat 1 

Prosty chat z systemem rejestracji. 

**Wygląd:**
- po wejściu na stronę główną pojawiają się 2 opcje: logowanie i rejestracja
- Po wybraniu opcji rejestracja uruchamia się formularz. Po wypełnieniu tworzą się odpowiednie wpisy w bazie
- Po zalogowaniu użytkownik przenoszony jest na stronę chatu z 2 sekcjami:
	- sekcja z otrzymanymi wiadomościami: Autor, data, treść
	- sekcja wysyłania: odbiorca, treść wiadomości
- Przykład po wejściu na stronę: http://twojserwer:port/przyklad lub [http://stud10.fenu-experiment.pl/przyklad](http://stud10.fenu-experiment.pl/przyklad)


Repozytorium [https://github.com/SMCEBI-didactics/sinwo-group1](https://github.com/SMCEBI-didactics/sinwo-group1)

**Funkcjonalności:** (należy wybrać 3)
- Stwórz system rejestracji użytkowników: login, hasło, imię, nazwisko oraz logowania
- Stwórz system wysyłania i odbierania wiadomości,
- Wprowadź system weryfikacji integralności wiadomości (użyj sha256 lub md5sum) oraz prostego "szyfrowania" (jakiekolwiek ukrycie tekstu np. base64)
- Dodaj odrębną opcję grupowego chatu oraz opcję opóźnionego wysyłania wiadomości
- Dodaj stronę administracyjną wyświetlającą proste statystyki (np. liczba wysłanych wiadomości, liczba użytkowników), ręczne usuwanie użytkowników, resetowanie haseł
- Modyfikacja front-endu (pliki md, dokumentacja, pliki css i js w WebApp/static oraz html  w WebApp/templates). Wszystkie pliki html w templates/  odwołują się do index.html tzn. modyfikacja index ma zastosowanie do wszystkich innych. Dostęp do plików w static możliwy przez http://serwer:port/js/.. /css/..

---

### Temat 2

Program do prostych obliczeń numerycznych.

**Wygląd**:

- Po wejściu na stronę główną, wylistowane zostają dostępne metody przekierowujące na odpowiednią podstronę,
- Po wybraniu opcji otwiera się formularz proszący o wprowadzenie danych wejściowych wraz z opisem oraz historią poprzednich operacji (wprowadzone dane, wynik, czas wykonania polecenia, data wykonania itp.)
- Po wprowadzeniu danych, na ekranie pojawia się wynik oraz zaktualizowana zostaje historia
- Wprowadź odpowiednie wyjątki i ograniczenia, aby nie przeciążyć serwera
- Przykład po wejściu na stronę: http://twojserwer:port/przyklad lub [http://stud10.fenu-experiment.pl/przyklad](http://stud10.fenu-experiment.pl/przyklad)

Repozytorium [https://github.com/SMCEBI-didactics/sinwo-group2/](https://github.com/SMCEBI-didactics/sinwo-group2/)

**Funkcjonalności:** (należy wybrać 5)
- Wyliczenie liczb pierwszych: Pokaż maksymalną liczbę pierwszą z podanego przedziału (max do 30000) z czasem wykonania metody.
	- przy pomocy metody modulo 
	- przy pomocy sita Eratostenesa.
- Całkowanie przynajmniej 2 predefiniowanych funkcji (opcjonalnie dowolnej) metodą trapezów i Monte Carlo. Pokaż wynik całkowania na wybranym przedziale i czas wykonania.
- Generator liczb losowych: 
	- Z wybranego przedziału wylosuj liczbę z rozkładu jednorodnego i Gaussa
	- Wylosuj liczbę z wybranego przedziału oraz rozkładu opisanego przez wprowadzoną funkcję (metoda eliminacji von Neumanna)
- Dekodery: 
	- Zapisz wprowadzoną liczbę w systemie dwójkowym, decymalnym oraz hex-decymalnym. 
	- Zapisz wprowadzony tekst w formacie base64 (i odwrotnie). 
	- Dla wprowadzonego tekstu wylicz hash: sha256 oraz md5
- Statystyka:
	- wylicz średnią, medianę i  odchylenia dla wprowadzonych liczb
	- wyznacz korelację Pearsona
	- wylicz współczynniki regresji liniowej
	- wykonaj test Shapiro-Wilka
- Dla wprowadzonej funkcji znajdź miejsca zerowe. Wybierz 2 metody:
	- metoda bisekcji
	- metoda siecznych
	- metoda iteracji
	- metoda newtona
- Modyfikacja front-endu (pliki md, dokumentacja, pliki css i js w WebApp/static oraz html  w WebApp/templates). Wszystkie pliki html w templates/  odwołują się do index.html tzn. modyfikacja index ma zastosowanie do wszystkich innych. Dostęp do plików w static możliwy przez http://serwer:port/js/.. /css/..


### Temat 3

Programming Challenges 

**Wygląd**:
- tak jak w przypadku *tematu 2* (m.in. strona wyświetla historię, każdy wynik zapisywany jest do bazy)

Repozytorium [https://github.com/SMCEBI-didactics/sinwo-group1](https://github.com/SMCEBI-didactics/sinwo-group1)

**Funkcjonalności**: (Należy wybrać 5)
- Dodaj opcję generowania losowej tożsamości
	- losowe imię, nazwisko, data urodzenia, PESEL, telefon, miejsce urodzenia, numer karty, kolor oczu/włosów, płeć waga itp.
	- dane powinny być wewnętrznie spójne tzn. pesel zgodny z datą urodzenia oraz poprawną sumą kontrolną, nr kierunkowy zgodny z zamieszkaniem itp.
- Dodaj stronę liczącą prędkość czytania oraz pisania (wymagane użycie flask.session)
- Dodaj stronę przeliczającą wybrane waluty (minimum 3 do wyboru) zgodnie z aktualnym kursem (aktualizowane z każdym nowym zapytaniem)
- Stwórz prosty emulator asemblera lub brainfucka (Pole tekstowe na kod, jako output efekt działania)
- Stwórz grę papier-kamień-nożyce (w historii punktacja) oraz kółko i krzyżyk w formacie ASCII (dla dwóch osób lub gra z komputerem)
- Dla podanego IP i maski wylicz, broadcast, podaj sieć oraz zakres adresów, liczbę hostów oraz klasę sieci (IPv4), Dodaj informację czy host o takim adresie odpowiada na ping
- Modyfikacja front-endu (pliki md, dokumentacja, pliki css i js w WebApp/static oraz html  w WebApp/templates). Wszystkie pliki html w templates/  odwołują się do index.html tzn. modyfikacja index ma zastosowanie do wszystkich innych. Dostęp do plików w static możliwy przez http://serwer:port/js/.. /css/..

---

## Work-flow

### Założenia-projektu

- W 1 grupie może być maksymalnie 5 osób
- Zachowanie formalizmu pracy git-flow. Gałęzią produkcyjną jest **production**, deweloperską **development**, drobne zmiany np. dodanie licencji, modyfikacje README itp. mogą odbywać się bez wyodrębniania dodatkowych gałęzi.
- praca z użyciem pull request oraz poprawnym tagowaniem commitów
- commity powinny być podpisywane kluczem GPG oraz sensownie opisywane
- mergowanie do gałęzi produkcyjnej możliwe tylko przez automatyczny pull request (ustawienia: automatyczny merge po 2 pozytywnych recenzjach)
- każdy wykonuje code review
- użycie funkcji **milestones** na GitHubie i linkowanie z pull request:
	- dodanie minimum 2 kamieni milowych np. v1.0, v2.0, v3.0 
	- ciągu 1 dnia **nie mogą** zostać zrealizowane wszystkie kamienie milowe
- każdy moduł ma wyodrębnioną własną dokumentację w katalogu **docs** oraz plik Dockerfile testujący działanie.
- Funkcjonalności muszą być wprowadzane (w większości) jako odrębne moduły w osobnych katalogach, instalowalne przez setup.py, uruchamialne przez polecenie powłoki oraz jako kontenery Dockera. Moduł musi działać niezależnie od całej aplikacji po instalacji przez pip/kontener (można go wykonać używając polecenia shell-owego, dzięki wpisowi entry\_points w setup.py)
- Dokumentacja całego projektu znajduje się w katalogu nadrzędnym w folderze **docs** oraz jest dostępna przed GitHub-pages
- Każdy odpowiada za swoją jedną funkcjonalność (nie dotyczy tematu 1), jednak dopuszczalne jest poprawianie kodu w cudzych gałęziach (tylko w ramach własnej grupy), szczególnie, gdy znajdujemy błąd w trakcje code review. 
- Cały program uruchamiany jest przez docker-compose, natomiast inne akcje od strony użytkownika końcowego powinny być zredukowane do minimum.
- Projekt posiada opis (czym jest, instalacja, użycie itp.) w pliku README.md ([przykład](https://github.com/mitmproxy/pdoc)), licencję MIT oraz dodany dokument CHANGELOG.md z opisem wprowadzonych/planowanych zmian w danej wersji projektu
- Widoczne minimum 2 wersje podczas rozwoju programu, tagowanie funkcjonalności powinno mieć postać np. v1.4, v2.1b, v2.3-front-end itp. 
- nie usuwamy gałęzi po mergowaniu
- projekt zawiera przynajmniej 1 makefile 
- Projekt powinien posiadać zachowaną historię zmian z pierwotnego repozytorium **WebApplication**
- Struktura podczas rozbudowy programu powinna być zgodna z przyjętą w *WebApplication* (np. moduły w katalogu Modules/, główna aplikacja w WebApp, konsekwentne rozmieszczenie README.md, Dockerfile, setuptools itp.)
- W repozytorium nie powinny znajdować się zbędne pliki np. pycache, build, sqlite, pliki tymczasowe itp.
- Kontenery powinny korzystać z customowej sieci, natomiast baza powinna być podpięta pod wewnętrzny Dockerowy Volumen. 
- Możliwe są podpowiedzi prowadzącego, jeśli problem dotyczy implementacji kodu lub sposobu rozwiązania problemu (ocenie nie podlega umiejętność programowania, tylko wykorzystanie narzędzi), pod warunkiem, że zostanie otwarty *issues* na GitHubie oraz wywołanie użytkownika *aszadzinski* (maksymalnie do 26.01.22)

 


###  Środowisko-deweloperskie

Testy oprogramowania  mogą odbywać się na serwerze INF-VM. 

Wersja produkcyjna musi być opublikowana na serwerze:

Grupa 1: 
	
```console
user@host:~$ ssh production@IP-JAK-INF-VM -p 2221
```

Usługi wystawione na port 80, widoczne są w sieci w domenie  http://prod1.fenu-experiment.pl/
Usługi wystawione na port 8080, widoczne są w sieci w domenie  http://prod1db.fenu-experiment.pl/

Grupa 2: 

```console
user@host:~$ ssh production@IP-JAK-INF-VM -p 2222
```

Usługi wystawione na port 80, widoczne są w sieci w domenie  http://prod2.fenu-experiment.pl/
Usługi wystawione na port 8080, widoczne są w sieci w domenie  http://prod2db.fenu-experiment.pl/

Hasła dostępowe widoczne po zalogowaniu na INF-VM w pliku /etc/production
