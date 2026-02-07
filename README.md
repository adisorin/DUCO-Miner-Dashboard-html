# DUCO-Miner-Dashboard-html
This project is based on Python code taken from https://github.com/jpx13/duco-miners and modified into HTML format for those who do not have Python installed on their PC. The code is modified and I added a bit of color to the writing.
Thanks to dansinclair25 for his initial work, the creator of the code.
If you like this and would like to donate some DUCO to him, his wallet username is `dansinclair25`, if you want to give some ducos to me, my wallet name is 'discopepereland'

And if anyone wants to donate to me too, my wallet address is "my_cool_adis", thank you.

<img width="1202" height="800" alt="image" src="https://github.com/user-attachments/assets/b50d5195-9d71-4c38-bfcb-85cdf8f06e2c" />


<img width="1203" height="793" alt="image" src="https://github.com/user-attachments/assets/8505c3e5-5818-4d6e-b748-35b7bc005ef0" />

# DUCO-monitor-html-v2
<img width="1254" height="758" alt="image" src="https://github.com/user-attachments/assets/8490733e-7b32-4a98-ae71-385519855d09" />

# DUCO-monitor-html-v2-TICKER
<img width="1306" height="916" alt="image" src="https://github.com/user-attachments/assets/c1ddad9f-9048-426b-b39f-f2632f781f8a" />

# În limba Română:
Documentație Tehnică: DUCO Miner Dashboard
Acesta este manualul tehnic pentru DUCO Miner Dashboard, un instrument web minimalist utilizat pentru monitorizarea în timp real a activității de minerit pe platforma Duino-Coin (DUCO).
1. Prezentare Generală
Codul furnizat reprezintă o aplicație de tip Single-Page (SPA), construită utilizând HTML5, CSS3 și JavaScript (Vanilla JS). Aceasta interacționează cu API-ul public Duino-Coin pentru a afișa statistici despre balanță, starea minerilor și performanța rețelei.
2. Caracteristici Cheie
Monitorizare în timp real: Actualizare automată a datelor la fiecare 60 de secunde.
Sumar Cont: Afișează balanța totală, numărul de mineri activi, timpul de funcționare a sesiunii (uptime) și scorul de încredere (Trust Score).
Detalii Mineri: Un tabel detaliat care include ID-ul dispozitivului, software-ul utilizat, algoritmul, rata de succes a share-urilor, hashrate-ul și latența (ping).
Interfață Dark Mode: Design optimizat pentru lizibilitate, utilizând fonturi monospace și alerte codificate prin culori.
3. Structură Tehnică
A. Stil Vizual (CSS)
Aplicația utilizează o temă întunecată (#111) cu accente cromatice funcționale:
Verde: Valori pozitive, succes, latență scăzută.
Roșu: Erori, share-uri respinse, latență ridicată.
Cyan: Date tehnice (Hashrate).
Violet: Identitate (Nume utilizator).
B. Funcții JavaScript (Logică)
fetchData(): Funcția asincronă principală care interoghează REST API-ul Duino-Coin.
formatHashrate(hr): Convertește valorile brute H/s în unități mai mari (kH/s, MH/s) pentru o mai bună lizibilitate.
sec2hms(sec): Calculează timpul de rulare al tabloului de bord în format HH:MM:SS.
startCountdown(): Gestionează cronometrul de reîmprospătare și declanșează noile cereri de date.
4. Parametri Monitorizați (Tabel)
Coloană	Descriere
ID	Identificatorul setat în configurația minerului.
Success	Raportul dintre share-urile acceptate și totalul procesat.
Hashrate	Viteza de calcul a dispozitivului.
Diff	Dificultatea atribuită de pool minerului respectiv.
Ping	Timpul de răspuns al serverului (măsurat în ms).
5. Mod de Utilizare
Salvați codul într-un fișier cu extensia .html (ex: index.html).
Deschideți fișierul în orice browser modern (Chrome, Firefox, Edge).
Introduceți Numele de utilizator DUCO în câmpul de text.
Apăsați butonul Start.
6. Note și Limitări
CORS: Aplicația rulează direct în browser. Dacă API-ul Duino-Coin impune restricții CORS (Cross-Origin Resource Sharing), ar putea fi necesar un proxy, deși serverele DUCO permit de regulă cererile de tip fetch.
Stocare: Balanța anterioară este stocată în memorie (prevBalance) pentru a calcula diferența la refresh, însă aceste date se pierd dacă pagina este reîncărcată manual (F5).

# Vă rugăm să rețineți
Pentru monitorizarea personală: O interogare la fiecare 30–60 de secunde este considerată ideală. Aceasta oferă date actualizate fără a suprasolicita inutil serverele proiectului.
Frecvența maximă sigură: Evitați să efectuați mai mult de o solicitare la fiecare 5–10 secunde. Solicitările mai frecvente pot fi interpretate ca un atac de tip spam sau bot.
Recomandare: Recomand setarea timpului de reîmprospătare a panoului de control (dashboard) la 120.000 de milisecunde (2 minute).
Important: NU deschideți aplicația pe mai multe dispozitive simultan, deoarece acest lucru declanșează un conflict Cloudflare: „Too many requests” (Prea multe solicitări).

# In English:
This is the technical documentation for the DUCO Miner Dashboard, a minimalist web-based tool used for real-time monitoring of mining activity on the Duino-Coin (DUCO) platform.
1. General Overview
The provided code is a Single-Page Application (SPA) built using HTML5, CSS3, and JavaScript (Vanilla JS). It interfaces with the public Duino-Coin API to display statistics regarding balance, miner status, and network performance.
2. Key Features
Real-time Monitoring: Automatic updates every 60 seconds.
Account Summary: Displays total balance, active miner count, session uptime, and Trust Score.
Miner Details: A detailed table featuring device IDs, software used, algorithm, share acceptance rate, hashrate, and latency (ping).
Dark Mode Interface: Design optimized for readability, utilizing monospace fonts and color-coded alerts.
3. Technical Structure
A. Visual Styling (CSS)
The application uses a dark theme (#111) with functional accent colors:
Green: Positive values, success, low latency.
Red: Errors, rejected shares, high latency.
Cyan: Technical data (Hashrate).
Purple: Identity (Username).
B. JavaScript Functions (Logic)
fetchData(): The primary asynchronous function that queries the Duino-Coin REST API.
formatHashrate(hr): Converts raw H/s values into larger units (kH/s, MH/s) for better readability.
sec2hms(sec): Calculates the dashboard runtime in HH:MM:SS format.
startCountdown(): Manages the refresh timer and triggers new data requests.
4. Monitored Parameters (Table)
Column	Description
ID	The identifier set in the miner's configuration.
Success	The ratio of accepted shares to the total processed.
Hashrate	The device's calculation speed.
Diff	The difficulty assigned by the pool to that specific miner.
Ping	Server response time (measured in ms).
5. Usage
Save the code into a file with the .html extension (e.g., index.html).
Open the file in any modern browser (Chrome, Firefox, Edge).
Enter your DUCO Username in the text field.
Press the Start button.
6. Notes and Limitations
CORS: The application runs directly in the browser. If the Duino-Coin API enforces CORS (Cross-Origin Resource Sharing) restrictions, a proxy might be required, though DUCO servers typically allow fetch requests.
Storage: The previous balance is stored in memory (prevBalance) to calculate the difference upon refresh, but this data is lost if the page is manually reloaded (F5).

# Please Note
For personal monitoring: One query every 30–60 seconds is considered ideal. This provides up-to-date data without unnecessarily taxing the project's servers.
Maximum safe frequency: Avoid making more than one request every 5–10 seconds. More frequent requests may be interpreted as a spam or bot attack.
Recommendation: I recommend setting the dashboard refresh time to 120,000 milliseconds (2 minutes).
Important: DO NOT open the application on multiple devices simultaneously, as this triggers a Cloudflare conflict: "Too many requests."
