
# Projekt Chat z Podświetlaniem Składni

Ten projekt to przykładowa aplikacja typu chat zintegrowana z zewnętrznym modelem językowym (LLM) poprzez API GroqApi. Dodatkowo umożliwia ona automatyczne podświetlanie składni fragmentów kodu przesyłanych w wiadomościach przy użyciu biblioteki [highlight.js](https://highlightjs.org/).

## Funkcjonalności

- **Chat z modelem językowym**:  
  Pozwala zadawać pytania i otrzymywać odpowiedzi w formie tekstowej.
  
- **Detekcja kodu**:  
  Fragmenty kodu umieszczane między trzema backtickami (```) są automatycznie wykrywane i wyświetlane w formacie `<pre><code>...</code></pre>`.

- **Podświetlanie składni**:  
  Wykorzystanie highlight.js do automatycznego podświetlania składni kodu dla wielu języków. Biblioteka stara się automatycznie wykryć odpowiedni język.

## Wymagania

- .NET 8
- Dostęp do API GroqApi (posiadanie `apiKey`).

## Konfiguracja

1. **Klonowanie repozytorium**:
   ```bash
   git clone https://github.com/Xenomimi/simple-chat-gpt.git
   cd simple-chat-gpt
   ```

2. **Instalacja zależności**:
   Jeśli jest to projekt .NET, uruchom:
   ```bash
   dotnet restore
   ```

3. **Klucz API**:  
   W bloku `@code` w pliku `Chat.razor` zaktualizuj zmienną `apiKey` podając własny klucz API do `GroqApiClient`.

   ```csharp
   private static string apiKey = "<TWÓJ_KLUCZ_API>";
   ```

## Uruchamianie

```bash
dotnet run
```

Następnie przejdź do `http://localhost:5231/chat` w przeglądarce.

## Jak korzystać

1. Wprowadź pytanie lub wiadomość w polu tekstowym.
2. Kliknij **"Zapytaj Chat"**, by wysłać wiadomość do modelu.
3. Odpowiedzi zawierające fragmenty kodu zostaną wyświetlone z kolorowaniem składni.
