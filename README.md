# Doppelschlüssel

Ein Koop-Escape-Spiel für **zwei Handys**: ein Einbruch ins Bankhaus Aurum, zwei Rollen,
ein Gespräch. Keiner schafft es allein.

- **Feld** ist im Gebäude: sieht Türpanels, Flure, die Tresortür, die Schließfächer und tippt die Codes.
- **Zentrale** sitzt im Lieferwagen: hat Codetabellen, Kamerapläne, abgefangene Mails und die Kundendatenbank.

Ihr redet miteinander, am selben Tisch oder per Telefon, und zeigt euch die Bildschirme nicht.

## Ablauf

1. Einer tippt **Einsatz planen** und nennt den vierstelligen Code, der andere tippt **Einsatz beitreten**.
2. Jeder wählt eine Rolle. Zählt runter und tippt gleichzeitig auf **Los**. Ihr habt 20 Minuten.
3. Vier Phasen: Symboltür, Kameraflur, Tresor, Schließfächer. Jede Phase braucht Wissen von beiden Seiten.
4. Fortschritt meldet ihr euch mit kurzen **Funkcodes**, die einer vorliest und der andere eingibt.

Fehler im Gebäude kosten Zeit. Derselbe Einsatzcode ergibt immer dieselben Rätsel, ein neuer ganz andere.

## Technik

Eine einzige `index.html`, ohne Server und ohne Abhängigkeiten. Beide Handys erzeugen aus dem
Einsatzcode mit einem Zufallsgenerator mit festem Startwert exakt dieselben Rätsel. Deshalb
braucht es keine Netzwerkverbindung zwischen den Geräten. Der Spielstand übersteht ein Neuladen.

Ein Push auf `main` veröffentlicht die Seite über GitHub Pages
(Pages-Quelle in den Einstellungen auf „GitHub Actions“ stellen).
