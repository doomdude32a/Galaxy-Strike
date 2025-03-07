# Galaxy-Strike
FPS shooting game in Unity.
# Projekt-Dokumentation
**Projektteam**
| Name        | Vorname  | Klasse |
|-------------|----------|--------|
| Angelov     | Angel    | Im22d  |
| Marku       | Erik     | Im22d  |
| Jashari     | Denis    | Im22d  |
### 1.1 Projektbeschreibung
**Versionshistorie**
1.1 Projektbeschreibung
Wir entwickeln den First-Person-Shooter "FPS Advanced Combat" in der Unity-Engine, einem fuehrenden Tool fuer die Spieleentwicklung. Das Spiel bietet dem Spieler ein immersives Erlebnis in einer realistischen 3D-Umgebung, in der er gegen computergesteuerte Gegner antritt. Ziel des Projekts ist es, ein technisch anspruchsvolles und spannendes Spielerlebnis zu schaffen.

Grundstruktur:
Das Spiel kombiniert fluessige Spielerbewegungen (inklusive Sprint- und Sprungmechanik) mit einer dynamischen First-Person-Kamera, die praezise ueber die Maus gesteuert wird. Dank Unitys integrierter Physik-Engine kommen realistische Kollisionspruefungen und physikbasierte Elemente zum Einsatz, die fuer eine glaubwuerdige Interaktion mit der Umgebung sorgen.

Kernfeatures:

Waffensystem: Integration verschiedener Waffenmodelle mit individuellen Eigenschaften, realistische Schussmechanik mittels Raycasting, Nachladeanimationen sowie Muendungsfeuer und Soundeffekte.

Gegner und KI: Entwicklung einer Gegner-KI, die den Spieler verfolgt und angreift. 

Spielmechaniken & Interface: Implementierung eines HUDs, eines Gesundheitssystems fuer den Spieler und klar definierter Endbedingungen (Sieg/Niederlage).

Die Umsetzung erfolgt im kollaborativen Team unter Einsatz von GitHub und regelmaessigen Online-Meetings, wobei eine modulare und strukturierte Vorgehensweise (IPERKA) den Entwicklungsprozess unterstuetzt.

### 1.2 Testfälle
# User Storie

| US-№  | Verbindlichkeit | Beschreibung |
|-------|-----------------|--------------|
| US-1  | muss            | Als Spieler möchte ich mich in der 3D-Umgebung (vorwärts, rückwärts, seitwärts, sprinten, springen) bewegen können. |
| US-2  | muss            | Als Spieler möchte ich, dass die Kamera meiner Mausbewegung folgt und ein konsistentes Sichtfeld liefert, um das Spiel zielgerichtet zu steuern. |
| US-3  | muss            | Als Spieler möchte ich, dass Schwerkraft und Kollisionen exakt simuliert werden, um eine glaubwürdige Interaktion mit der Umgebung zu gewährleisten. |
| US-4  | muss            | Als Spieler möchte ich in einem Level mit Hindernissen, Deckungen und offenen Bereichen spielen.. |
| US-5  | muss            | Als Spieler möchte ich zwischen verschiedenen Waffen (z. B. Pistole, Gewehr) wählen können. |
| US-6  | muss            | Als Spieler möchte ich, dass Schüsse präzise registriert werden, der Nachladevorgang korrekt abläuft und visuelle sowie akustische Effekte (z. B. feuern) abgespielt werden. |
| US-7  | muss            | Als Spieler möchte ich, dass Gegner mit Lebenspunkten agieren, sodass Treffer ihren Gesundheitszustand beeinflussen. |
| US-8  | muss            | Als Spieler möchte ich, dass Gegner aktiv auf meine Position reagieren und Angriffe ausführen.|
| US-9  | muss            | Als Spieler möchte ich, dass neue Gegner gespawnt werden durch Spawns |
| US-10 | muss            | Als Spieler möchte ich jederzeit meinen Gesundheitsstatus einsehen können, damit der Schaden von Gegnern registriert wird. |
| US-11 | muss            | Als Spieler möchte ich ein klares Heads-Up-Display, das fortlaufend Informationen wie Gesundheit, Munition |
| US-12 | muss            | Als Spieler möchte ich im Spiel zusätzliche Waffen erwerben können|
| US-13 | muss            | Als Spieler möchte ich Punkte für das Besiegen von Gegnern und das Erreichen von Zielen sammeln. |
| US-14 | muss            | Als Spieler möchte ich, dass das Spiel eindeutige Endbedingungen bietet (z. B. Sieg bei Erreichen eines Zielpunkts oder Niederlage bei Verlust aller Lebenspunkte), um ein abgerundetes und faires Spielerlebnis zu gewährleisten. |


### 1.3 Testfälle


| **TC-№** | **Ausgangslage**                                      | **Eingabe**                                                                  | **Erwartete Ausgabe**                                                                        | **Zugehörige US** |
|----------|-------------------------------------------------------|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|-------------------|
| TC-1     | Spieler im Level, Bewegung aktiv                      | Spieler bewegt sich mittels WASD, führt Sprint und Sprung aus                | Spieler bewegt sich flüssig in alle Richtungen, inkl. Sprint und Sprung                        | US-1              |
| TC-2     | Szene mit aktiver Kamera                              | Mausbewegungen zur Steuerung der Kamera                                      | Kamera folgt der Mausbewegung und liefert ein konsistentes Sichtfeld                           | US-2              |
| TC-3     | Spieler auf erhöhter Plattform                        | Spieler springt von der Plattform                                             | Schwerkraft und Kollision werden exakt simuliert; Spieler landet realistisch                   | US-3              |
| TC-4     | Spieler betritt ein Level                             | Spieler erkundet das Level                                                    | Level enthält Hindernisse, Deckungen und offene Bereiche                                       | US-4              |
| TC-5     | Waffenmenü wird angezeigt                             | Spieler wählt eine der angebotenen Waffen (z. B. Pistole oder Gewehr)         | Gewählte Waffe wird aufgenohmen und angezeigt                                          | US-5              |
| TC-6     | Spieler in Kampfsituation                             | Spieler feuert und initiiert den Nachladevorgang                               | Schüsse werden präzise registriert; Nachladevorgang läuft korrekt; visuelle und akustische Effekte (z. B. Feuereffekte) werden abgespielt | US-6              |
| TC-7     | Gegner im Kampf                                       | Spieler trifft einen Gegner mit einem Schuss                                  | Die Lebenspunkte des Gegners werden reduziert, und sobald sie 0 erreichen wird der Gegner besiegt ;                     | US-7              |
| TC-8     | Spieler im Gefecht                                    | Gegner reagiert aktiv auf die Position des Spielers und greift an            | Gegner führt Angriffsanimation aus und der Angriff wird registriert                            | US-8              |
| TC-9     | Fortlaufendes Spielgeschehen                          | Beobachtung der Spielszene über einen definierten Zeitraum                     | Neue Gegner werden über das Spawn-System/Gate generiert                                           | US-9              |
| TC-10    | Spieler im Gefecht, Gesundheitsanzeige sichtbar       | Spieler wird von einem Gegner getroffen                                      | Gesundheitsstatus wird aktualisiert, und der registrierte Schaden wird korrekt angezeigt       | US-10             |
| TC-11    | Spielstart, aktives HUD-Bereich                       | Spielbeginn                                                                  | Das Heads-Up-Display zeigt fortlaufend Informationen wie Gesundheit, Munition usw. an         | US-11             |
| TC-12    | Spieler im Waffen-Shop oder Erwerbsbereich            | Spieler initiiert den Kauf einer zusätzlichen Waffe                          | Die zusätzliche Waffe wird dem Inventar hinzugefügt; der Preis wird von der In-Game-Währung abgezogen | US-12             |
| TC-13    | Spieler im Kampf                                      | Spieler besiegt einen Gegner oder erreicht ein definiertes Ziel                | Punkte werden korrekt addiert und der Fortschritt im Punktesystem aktualisiert                 | US-13             |
| TC-14    | Spiel in Endphase                                     | Spieler erfüllt die Siegbedingung oder verliert (Gesundheit = 0)               | Das Spiel zeigt eindeutige Endbedingungen (Sieg oder Niederlage) und beendet die Session         | US-14             |


### 1.4 Diagramme
![WhatsApp Bild 2025-03-07 um 00 13 27_fb544d1a](https://github.com/user-attachments/assets/728a161f-6031-45b2-b2db-58320b5c77be)

## 3. Entscheiden 

## 4. Realisieren

| **AP-№** | **Datum**    | **Zuständig**        | **Geplante Zeit** | **Tatsächliche Zeit** |
|----------|-------------|-----------------------|-------------------|-----------------------|
| 1.A      | 16.11.2024  | Marku                | 60 min            | 60 min               |
| 2.A      | 16.11.2024  | Jashari              | 60 min            | 50 min               |
| 3.A      | 20.11.2024  | Angelov              | 90 min            | 75 min               |
| 4.A      | 25.11.2024  | Marku                | 120 min           | 110 min              |
| 5.A      | 25.11.2024  | Jashari              | 90 min            | 90 min               |
| 6.A      | 30.11.2024  | Angelov              | 90 min            | 80 min               |
| 7.A      | 05.12.2024  | Marku                | 120 min           | 110 min              |
| 8.A      | 05.12.2024  | Jashari              | 60 min            | 60 min               |
| 9.A      | 10.12.2024  | Angelov              | 60 min            | 70 min               |
| 10.A     | 10.12.2024  | Marku                | 60 min            | 55 min               |
| 11.A     | 15.12.2024  | Jashari              | 90 min            | 85 min               |
| 12.A     | 15.12.2024  | Angelov              | 60 min            | 65 min               |
| 13.A     | 20.12.2024  | Team                 | 120 min           | 130 min              |
| 14.A     | 21.12.2024  | Team                 | 180 min           | 200 min              |

## 5. Kontrollieren

### 5.1 Testprotokoll

| **TC-№** | **Datum**    | **Resultat** | **Tester**  | **Verknüpfte US** |
|----------|-------------|--------------|------------|-------------------|
| 1.1      | 20.12.2024  | OK           | Marku      | US-1              |
| 2.1      | 20.12.2024  | OK           | Jashari    | US-2              |
| 3.1      | 20.12.2024  | OK           | Angelov    | US-3              |
| 4.1      | 20.12.2024  | OK           | Marku      | US-4              |
| 5.1      | 20.12.2024  | OK           | Jashari    | US-5              |
| 6.1      | 20.12.2024  | OK           | Angelov    | US-6              |
| 7.1      | 20.12.2024  | OK           | Marku      | US-7              |
| 8.1      | 20.12.2024  | OK           | Jashari    | US-8              |
| 9.1      | 20.12.2024  | OK           | Angelov    | US-9              |
| 10.1     | 20.12.2024  | OK           | Marku      | US-10             |
| 11.1     | 20.12.2024  | OK           | Jashari    | US-11             |
| 12.1     | 20.12.2024  | OK           | Angelov    | US-12             |

