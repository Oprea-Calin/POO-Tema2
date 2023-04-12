## Cerințe tema 2
Cerințe comune:
- separarea codului din clase în fișiere header (`.h`/`.hpp` etc.) și surse (`.cpp` etc.)
  - clasele mici și legate între ele se pot afla în aceeași pereche de fișiere header-sursă
  - FĂRĂ `using namespace std` în fișiere `.h`/`.hpp` la nivel global
    - pot fi declarații locale
- moșteniri
  - funcții virtuale (pure), constructori virtuali (clone)
    - funcțiile virtuale vor fi apelate prin pointeri la clasa de bază
    - pointerii la clasa de bază vor fi atribute ale altei clase, nu doar niște pointeri/referințe în main
  - apelarea constructorului din clasa de bază
  - fără erori de memorie; recomandare: smart pointers
  - `dynamic_cast`
- suprascris cc/op= pentru copieri/atribuiri corecte, copy and swap
- excepții
  - ierarhie proprie cu baza `std::exception` sau derivată din `std::exception`
  - utilizare cu sens: de exemplu, `throw` în constructor, `try`/`catch` în `main`
- funcții și atribute statice
- STL
- un tag de git pe un commit cu cod stabil și toate bifele
- fără variabile globale
- cât mai multe `const`
- testat/apelat tot codul public din `main`, altfel nu trece de cppcheck

Cerințe specifice:
- implementarea a două funcționalități noi specifice temei; pentru minim o funcționalitate **trebuie**
  folosite funcții virtuale apelate prin pointeri de bază
- **după** rezolvarea discuțiilor, de făcut un commit cu adăugarea unei noi derivate și suprascrierea unei
  funcții virtuale specifice temei; ar trebui modificat codul doar în funcția main și în fișierul cu noua derivată
