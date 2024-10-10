# Discord Ticket Bot (discord.js v14)

Bot Discord do zarządzania systemem ticketów, który pozwala użytkownikom otwierać ticket poprzez interakcję z przyciskiem. Po kliknięciu w przycisk, użytkownicy wybierają kategorię, wypełniają formularz, a bot automatycznie tworzy dedykowany kanał ticketowy. Administratorzy mogą przejąć tickety, co ogranicza dostęp do kanału tylko dla odpowiednich osób, oraz zamknąć ticket, co generuje raport z całą rozmową.

## Funkcje

- **/panel [kanał] [ticket]**: Tworzy wiadomość z przyciskiem do otwierania ticketów na wybranym kanale.
- **System kategorii**: Użytkownicy mogą wybrać kategorię ticketu po kliknięciu przycisku, korzystając z rozwijanego menu.
- **Formularz (Modal)**: Po wybraniu kategorii, pojawia się formularz z pytaniami do uzupełnienia.
- **Tworzenie ticketu**: Po wypełnieniu formularza bot automatycznie tworzy kanał ticketowy.
- **Przejmowanie ticketa**: Administrator może przejąć ticket, co sprawia, że tylko on ma dostęp do kanału, a reszta użytkowników traci dostęp.
- **Zamykanie ticketa**: Administrator może zamknąć ticket, co generuje plik .txt z pełną historią wiadomości (wraz z datą, kto stworzył i zamknął ticket) i wysyła go na określony kanał.

## Przykład Komend

### /panel [kanał] [ticket]

Rozpoczyna system ticketów, wysyłając wiadomość z przyciskiem do otwarcia ticketu.

**Przykład**:  
`/panel #support ticket` – wysyła wiadomość z panelem do otwierania ticketów na kanale **#support**.

### Tworzenie Ticketu

Po kliknięciu przycisku otwierania ticketu:

1. Bot wysyła embed z rozwijanym menu wyboru kategorii.
2. Po wybraniu kategorii użytkownik otrzymuje formularz do wypełnienia.
3. Po wypełnieniu formularza tworzy się nowy kanał ticketowy.
4. Bot wysyła potwierdzenie utworzenia ticketu z informacją, kto go stworzył.

### Przejmowanie Ticketa

Administrator może przejąć ticket, klikając odpowiedni przycisk. Gdy to zrobi, dostęp do ticketu zostaje ograniczony tylko do tej osoby, a reszta użytkowników traci dostęp do kanału.

### Zamykanie Ticketa

Administrator może zamknąć ticket, co powoduje:

1. Zapisanie wszystkich wiadomości w formacie .txt (wraz z datą i autorem każdej wiadomości).
2. Wysłanie pliku .txt na określony kanał z informacją o zamknięciu ticketu i osobach zaangażowanych.

## Podgląd

Poniżej znajduje się zrzut ekranu prezentujący ogólną wiadomość embed:

![footer](https://cdn.discordapp.com/attachments/1102682877235310734/1293750239039324221/Zrzut_ekranu_2024-10-10_033242.png?ex=6708824d&is=670730cd&hm=f328f0b6e7e3fe95daf29381213c19f1cab653cfa6e0107c9c133e4c03a428ba&)

Poniżej znajduje się zrzut ekranu prezentujący wiadomość embed z kategoriami:

![footer](https://cdn.discordapp.com/attachments/1102682877235310734/1293750238820958248/Zrzut_ekranu_2024-10-10_033249.png?ex=6708824d&is=670730cd&hm=a52249ba920aa854f75fee81a26d3b1e33e694da1ca88b980953742fc8e3cbdb&)

Poniżej znajduje się zrzut ekranu prezentujący formularz (modal) z pytaniami:

![footer](https://cdn.discordapp.com/attachments/1102682877235310734/1293750238611378206/Zrzut_ekranu_2024-10-10_033256.png?ex=6708824d&is=670730cd&hm=73ea85a2c221645593c0d582f759dad96cfef0ede28082ad81687b93ca9262cc&)

Poniżej znajduje się zrzut ekranu prezentujący wiadomość embed po udanym otwarciu ticketa:

![footer](https://cdn.discordapp.com/attachments/1102682877235310734/1293750238322102313/Zrzut_ekranu_2024-10-10_033309.png?ex=6708824d&is=670730cd&hm=61dd9110c85760dc87ba830828bdb07c1ee89a6d98e75813995c45a42d9ac6c8&)

Poniżej znajduje się zrzut ekranu prezentujący wiadomość embed stworzonego ticketa:

![footer](https://cdn.discordapp.com/attachments/1102682877235310734/1293750238095343637/Zrzut_ekranu_2024-10-10_033317.png?ex=6708824d&is=670730cd&hm=67489f9708edf4ed873039c58cc37240f0918568aefda7ae10fc861f8acee71b&)

Poniżej znajduje się zrzut ekranu prezentujący wiadomość embed przy przejęciu ticketa:

![footer](https://cdn.discordapp.com/attachments/1102682877235310734/1293750237856403556/Zrzut_ekranu_2024-10-10_033322.png?ex=6708824d&is=670730cd&hm=b85687a4593cab67484afe2f1d52a50be66a036cbdeccad049612e6fe75df3c3&)

Poniżej znajduje się zrzut ekranu prezentujący wiadomość embed przy zamykaniu ticketa:

![footer](https://cdn.discordapp.com/attachments/1102682877235310734/1293750237541961778/Zrzut_ekranu_2024-10-10_033330.png?ex=6708824d&is=670730cd&hm=3b689779aa47f9257e66bc789c9d6affe22c810fbc8e17f6e04bfe9a57cdbe14&)

Poniżej znajduje się zrzut ekranu prezentujący wiadomość embed po zamknięciu całego ticketa i wszystkich informacji na jego temat:

![footer](https://cdn.discordapp.com/attachments/1102682877235310734/1293750239336988682/Zrzut_ekranu_2024-10-10_033336.png?ex=6708824d&is=670730cd&hm=6a39f509c7453809b5eda7b895f245053ccce01a33d3c4e2a5b9d10377443bc6&)

## Wymagania

- **Node.js** v16.9.0 lub nowszy
- **npm**
- Konto Discord oraz utworzona aplikacja [na Discord Developer Portal](https://discord.com/developers/applications)

**Autor:** [ScreamMaster1337](https://github.com/ScreamMaster1337)  
**Licencja:** MIT
