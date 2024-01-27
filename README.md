Dokumentacja Aplikacji Flask - System Zarządzania Użytkownikami
Opis
Aplikacja Flask służąca do zarządzania użytkownikami, w tym funkcjonalności takie jak logowanie, rejestracja, edycja profilu i wylogowywanie.

Wymagania
Python 3
Flask
Flask-SQLAlchemy
Flask-Login
Werkzeug (dla bezpieczeństwa haseł)
Dodatkowe zależności są wymienione w pliku requirements.txt.
Instalacja
Aby uruchomić aplikację, wykonaj następujące kroki:

Zainstaluj wymagane zależności za pomocą pip install -r requirements.txt.
Uruchom plik app.py za pomocą Pythona.
Struktura Aplikacji
app.py: Główny plik aplikacji zawierający logikę backendową.
templates/: Folder zawierający pliki HTML dla widoków.
index.html: Strona główna aplikacji.
signup.html: Formularz rejestracji użytkownika.
login.html: Formularz logowania użytkownika.
profile.html: Strona profilu użytkownika do edycji danych.
static/: Folder na statyczne pliki, takie jak CSS, JS, obrazy.
style.css: Arkusz stylów CSS dla aplikacji.
requirements.txt: Lista zależności niezbędnych do uruchomienia aplikacji.
Model Użytkownika
Klasa User dziedziczy z UserMixin i db.Model. Zawiera następujące pola:

id: Unikalny identyfikator użytkownika (klucz główny).
first_name: Imię użytkownika.
last_name: Nazwisko użytkownika.
email: Adres e-mail użytkownika (unikalny).
password: Zhashowane hasło użytkownika.
Widoki i Funkcje
@app.route('/'): Strona główna.
@app.route('/login', methods=['GET', 'POST']): Logowanie użytkownika.
@app.route('/signup', methods=['GET', 'POST']): Rejestracja nowego użytkownika.
@app.route('/profile/<username>', methods=['GET', 'POST']): Edycja profilu użytkownika.
@app.route('/logout'): Wylogowanie użytkownika.
Bezpieczeństwo
Hasła są zabezpieczane przez hashowanie za pomocą werkzeug.security.
Uwagi dotyczące bezpieczeństwa:
Użytkownicy o podobnych imionach mogą przypadkowo trafić na ten sam profil.
Zalogowany użytkownik może uzyskać dostęp do konta innego użytkownika, zmieniając username w URL /profile/<username>. Wymagane są dodatkowe środki ochrony, aby zapobiec nieautoryzowanemu dostępowi.
Uruchomienie Aplikacji
Aplikacja może być uruchomiona lokalnie poprzez wykonanie app.run(debug=False) w app.py.

Dodatkowe Informacje
Przed uruchomieniem aplikacji upewnij się, że skonfigurowano bazę danych i wykonano migracje.
W przypadku rozszerzania aplikacji, zaktualizuj dokumentację odpowiednio.
