# Główne zmiany

- UI: Ulepszono oznaczanie aktualnie odtwarzanej muzyki (nuta muzyczna) w sesji i w wynikach wyszukiwania.
- UI: Poprawiono wygląd kontrolera.
- UI: Usunięto pozostały kod oscylującej kulki ładowania z ekranu Fusion.
- DEBUG: Naprawiono niewidoczne obszary, które mogły przechwytywać kliknięcia na ekranie startowym: flagi i przyciski można teraz klikać nawet wtedy, gdy Kiki lub -BIOPlayer- znajdują się nad nimi.
- FUNKCJA: Ulepszono odzyskiwanie identyfikatora: brakujący klucz licencyjny jest generowany automatycznie, jeśli konto nadal używało tymczasowej wartości `000-000-000`.
- TECH: Ulepszono publikowanie notatek aktualizacji w GitHub Pages, bez zależności od `rsync`.
- TECH: Rozdzielono instalatory Windows według kanału: `BIOPlayer`, `BIOPlayer Beta` i `BIOPlayer Dev` mogą teraz współistnieć na tym samym komputerze.
- UI: Poprawiono pole wydawcy Windows: pozostaje ono `BIOPlayer` dla wszystkich kanałów.
