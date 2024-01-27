
# System Zarządzania Użytkownikami (Flask)

System zarządzania użytkownikami zbudowany w Flask, umożliwiający logowanie, rejestrację, edycję profilu i wylogowanie.

## Wymagania

* Python 3
* Flask
* Flask-SQLAlchemy
* Flask-Login
* Werkzeug

Zobacz `requirements.txt` dla pełnej listy zależności.

## Instalacja

Kroki instalacyjne:

```bash
git clone https://github.com/Stearlit/create_save_user
cd create_save_user
pip install -r requirements.txt
```

## Uruchomienie

```bash
python app.py
```

## Struktura Projektu

```
/
|- app.py                # Główny plik aplikacji Flask
|- /templates            # Szablony HTML
   |- index.html         # Strona główna
   |- login.html         # Strona logowania
   |- signup.html        # Strona rejestracji
   |- profile.html       # Strona profilu użytkownika
|- /static               # Zasoby statyczne
   |- /css
      |- style.css       # Arkusz stylów CSS
|- requirements.txt      # Zależności projektu
```

## Funkcjonalności

* **Logowanie**: Umożliwia użytkownikom logowanie się do systemu.
* **Rejestracja**: Pozwala na utworzenie nowego konta użytkownika.
* **Profil użytkownika**: Użytkownicy mogą edytować swoje dane.
* **Wylogowanie**: Umożliwia wylogowanie się z systemu.

## Bezpieczeństwo

- Hasła są zabezpieczane przez hashowanie.
- Należy zwrócić uwagę na potencjalne problemy związane z dostępem do kont innych użytkowników przez manipulację URL.


## Autor

[Giorgi Iluridze]

