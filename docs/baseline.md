# Baseline — pomiar stanu wyjściowego

Plik uzupełniasz w ZADANIU 01. Czasy odczytujesz w zakładce **Actions**. Wystarczy dokładność
do sekundy.

## Czasy kroków — przebieg na `main`

| Krok | Czas |
|---|---|
| Set up job | 1s |
| Checkout | 11s |
| Set up Node | 1s |
| Install dependencies | 24s |
| Install Playwright browsers | 13s |
| Unit tests | 1s |
| API tests | 19s |
| UI tests | 2m 17s |
| Upload Playwright report | 2s |
| Post Set up Node | 0s |
| Post Checkout | 0s |
| Complete job | 0s |
| **Cały przebieg** | 3m 34s |

## Czas do pierwszego czerwonego sygnału

| Branch | Czas samego testu | Od startu przebiegu do informacji o błędzie |
|---|---|---|
| `demo/failing-unit` | 1s | 58s |
| `demo/failing-search` | — | 4min 42s |

Co na `demo/failing-unit` stało się z testami API i UI:

## `demo/failing-lint` i `demo/failing-security`

| Branch | Wynik przebiegu | Dlaczego tak |
|---|---|---|
| `demo/failing-lint` | PASS | Brak uruchomienia testów linta (npm run lint) lub verify |
| `demo/failing-security` | PASS | Prawdpodobny brak sprawdzania obecności tokenu |

## Pięć problemów obecnego pipeline’u

1. Brak współbieżności
2. Zbyt szybka instalacja przeglądarki
3. Brak testów linta 
4. Brak testów security
5. Brak smoke

## Pomiary z kolejnych zadań

Tu dopisujesz pomiary i odpowiedzi z kolejnych zadań, pod nagłówkiem z numerem zadania.

## After change

Base:
1. Install dependencies - 41s
2. Install Playwright browsers - 11s
3. All - 4m 2s

After cache:
1. Install dependencies - 3s
2. Install Playwright browsers - 0s
3. All - 2m 2s


Zadanie 5, przesyłanie artefaktu:
1. All - 3m 11s
2. UI - before 2m 45s, after 2m 41s