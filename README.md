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
Gegner und KI: Entwicklung einer Gegner-KI, die den Spieler verfolgt, angreift und bei Treffern visuelles Feedback gibt.
Spielmechaniken & Interface: Implementierung eines HUDs, eines Gesundheitssystems fuer den Spieler und klar definierter Endbedingungen (Sieg/Niederlage).
Die Umsetzung erfolgt im kollaborativen Team unter Einsatz von GitHub und regelmaessigen Online-Meetings, wobei eine modulare und strukturierte Vorgehensweise (IPERKA) den Entwicklungsprozess unterstuetzt.
### 1.2 Testfälle
# User Stories – FPS Advanced Combat

| US-№  | Verbindlichkeit | Beschreibung |
|-------|-----------------|--------------|
| US-1  | muss            | Als Spieler möchte ich mich in der 3D-Umgebung (vorwärts, rückwärts, seitwärts, sprinten, springen) bewegen können, um das Level präzise zu erkunden. |
| US-2  | muss            | Als Spieler möchte ich, dass die Kamera meiner Mausbewegung folgt und ein konsistentes Sichtfeld liefert, um das Spiel zielgerichtet zu steuern. |
| US-3  | muss            | Als Spieler möchte ich, dass Schwerkraft und Kollisionen exakt simuliert werden, um eine glaubwürdige Interaktion mit der Umgebung zu gewährleisten. |
| US-4  | muss            | Als Spieler möchte ich in einem Level mit Hindernissen, Deckungen und offenen Bereichen spielen, die taktisches Vorgehen fördern. |
| US-5  | muss            | Als Spieler möchte ich zwischen verschiedenen Waffen (z. B. Pistole, Gewehr) wählen können, die jeweils spezifische Eigenschaften besitzen. |
| US-6  | muss            | Als Spieler möchte ich, dass Schüsse präzise registriert werden, der Nachladevorgang korrekt abläuft und visuelle sowie akustische Effekte (z. B. Mündungsfeuer) abgespielt werden. |
| US-7  | muss            | Als Spieler möchte ich, dass Gegner mit festgelegten Lebenspunkten agieren, sodass Treffer ihren Gesundheitszustand beeinflussen. |
| US-8  | muss            | Als Spieler möchte ich, dass Gegner aktiv auf meine Position reagieren und Angriffe ausführen, um eine dynamische Herausforderung zu bieten. |
| US-9  | muss            | Als Spieler möchte ich, dass in regelmäßigen Abständen neue Gegner gespawnt werden, um eine kontinuierliche Herausforderung zu gewährleisten. |
| US-10 | muss            | Als Spieler möchte ich jederzeit meinen Gesundheitsstatus einsehen können, damit ich über kritische Zustände informiert bin. |
| US-11 | muss            | Als Spieler möchte ich ein klares Heads-Up-Display, das fortlaufend Informationen wie Gesundheit, Munition und ausgewählte Waffe anzeigt. |
| US-12 | muss            | Als Spieler möchte ich im Spiel zusätzliche Waffen erwerben können, wobei der Preis von meiner In-Game-Währung abgezogen wird. |
| US-13 | muss            | Als Spieler möchte ich Punkte für das Besiegen von Gegnern und das Erreichen von Zielen sammeln, um meinen Fortschritt messbar zu machen. |
| US-14 | muss            | Als Spieler möchte ich, dass das Spiel eindeutige Endbedingungen bietet (z. B. Sieg bei Erreichen eines Zielpunkts oder Niederlage bei Verlust aller Lebenspunkte), um ein abgerundetes und faires Spielerlebnis zu gewährleisten. |


### 1.3 Testfälle

| **TC-№** | **Ausgangslage**                      | **Eingabe**                                                  | **Erwartete Ausgabe**                                                                         | **Zugehörige US** |
|----------|---------------------------------------|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------|-------------------|
| 1.1      | Spieler im Level, Bewegung aktiv      | Spieler bewegt sich mittels WASD, Sprint und Sprung          | Spieler bewegt sich flüssig; Kollisionen werden korrekt erkannt                                | US-1              |
| 1.2      | Szene mit aktiver Kamera              | Mausbewegungen zur Steuerung der Kamera                      | Kamera folgt der Maus präzise und flüssig                                                     | US-2              |
| 1.3      | Spieler führt einen Sprung aus          | Spieler springt von einer erhöhten Plattform                 | Schwerkraft und Kollision werden realistisch simuliert; Spieler landet korrekt                | US-3              |
| 1.4      | Spieler betritt das Level             | Spieler bewegt sich im Level                                 | Hindernisse, Deckungen und offene Bereiche sind erkennbar und beeinflussen das taktische Vorgehen | US-4              |
| 1.5      | Waffenmenü wird angezeigt             | Spieler wählt eine Waffe aus dem Menü                        | Gewählte Waffe wird korrekt dargestellt und zeigt die definierten Attribute                    | US-5              |
| 1.6      | Spieler in Kampfsituation             | Spieler feuert und initiiert den Nachladevorgang               | Schuss wird präzise registriert; Nachladeanimation und Soundeffekte (inkl. Mündungsfeuer) werden abgespielt | US-6              |
| 1.7      | Gegner erscheint im Kampfgeschehen    | Spieler trifft den Gegner mit einem Schuss                   | Lebenspunkte des Gegners verringern sich; visuelles Feedback zeigt den Treffer                  | US-7              |
| 1.8      | Spieler befindet sich im Gefecht       | Gegner nähert sich und greift den Spieler an                 | Gegner führt Angriffsanimation aus; Schaden wird am Spieler registriert                         | US-8              |
| 1.9      | Spieler in Kampf, Gesundheitsanzeige aktiv | Spieler wird von einem Gegner getroffen                     | Gesundheitsanzeige sinkt; bei kritischem Wert erfolgt eine Warnung                             | US-9              |
| 1.10     | Spiel startet, HUD aktiviert          | Spiel beginnt                                                | HUD zeigt laufend aktuelle Werte zu Gesundheit, Munition und aktiver Waffe                     | US-10             |
| 1.11     | Spieler im Waffen-Shop                | Spieler initiiert den Kauf einer zusätzlichen Waffe          | Preis wird von der In-Game-Währung abgezogen; Waffe erscheint im Inventar                       | US-11             |
| 1.12     | Spieler erzielt Erfolge im Kampf      | Spieler besiegt Gegner bzw. erreicht ein Ziel                | Punkte werden korrekt addiert und der Fortschritt im Punktesystem aktualisiert                  | US-12             |

### 1.4 Diagramme
![WhatsApp Bild 2025-03-07 um 00 13 27_fb544d1a](https://github.com/user-attachments/assets/728a161f-6031-45b2-b2db-58320b5c77be)

### 1.3 Testfälle

| **TC-№** | **Ausgangslage**                                      | **Eingabe**                                                  | **Erwartete Ausgabe**                                                                         | **Zugehörige US** |
|----------|-------------------------------------------------------|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------|-------------------|
| TC-1     | Spieler im Level, Bewegung aktiv                      | Spieler bewegt sich mittels WASD, Sprint und Sprung          | Spieler bewegt sich flüssig; Kollisionen werden korrekt erkannt                                | US-1              |
| TC-2     | Szene mit aktiver Kamera                              | Mausbewegungen zur Steuerung der Kamera                      | Kamera folgt der Maus präzise und flüssig                                                     | US-2              |
| TC-3     | Spieler führt einen Sprung aus                        | Spieler springt von einer erhöhten Plattform                 | Schwerkraft und Kollision werden realistisch simuliert; Spieler landet korrekt                | US-3              |
| TC-4     | Spieler betritt ein Level mit taktischen Elementen    | Spieler erkundet das Level                                   | Hindernisse, Deckungen und offene Bereiche fördern taktisches Vorgehen                         | US-4              |
| TC-5     | Waffenmenü wird angezeigt                             | Spieler wählt eine Waffe aus dem Menü                        | Gewählte Waffe wird korrekt dargestellt mit ihren spezifischen Eigenschaften                  | US-5              |
| TC-6     | Spieler in Kampfsituation                             | Spieler feuert und initiiert den Nachladevorgang               | Schuss wird präzise registriert; Nachladeanimation und Soundeffekte (inkl. Mündungsfeuer) werden abgespielt | US-6  |
| TC-7     | Gegner erscheint im Kampfgeschehen                    | Spieler trifft den Gegner mit einem Schuss                   | Lebenspunkte des Gegners verringern sich; visuelles Feedback (z. B. Partikeleffekte) wird angezeigt | US-7  |
| TC-8     | Spieler befindet sich im Gefecht                      | Gegner nähert sich und greift den Spieler an                 | Gegner reagiert aktiv mit Angriffsanimation; Schaden wird am Spieler registriert                | US-8              |
| TC-9     | Spielgeschehen in fortlaufendem Kampf                 | Beobachtung der Spielszene über einen definierten Zeitraum     | Neue Gegner werden in regelmäßigen Abständen gespawnt                                         | US-9              |
| TC-10    | Spieler im Gefecht, Gesundheitsanzeige aktiv          | Spieler wird von einem Gegner getroffen                      | Gesundheitsanzeige sinkt; bei kritischem Wert erfolgt eine Warnung                             | US-10             |
| TC-11    | Spiel startet, HUD aktiviert                          | Spiel beginnt                                                | HUD zeigt laufend aktuelle Werte zu Gesundheit, Munition und aktiver Waffe                     | US-11             |
| TC-12    | Spieler im Waffen-Shop                                | Spieler initiiert den Kauf einer zusätzlichen Waffe          | Preis wird von der In-Game-Währung abgezogen; Waffe erscheint im Inventar                       | US-12             |
| TC-13    | Spieler erzielt Erfolge im Kampf                      | Spieler besiegt Gegner bzw. erreicht ein Ziel                | Punkte werden korrekt addiert und der Fortschritt im Punktesystem aktualisiert                  | US-13             |
| TC-14    | Spiel erreicht einen entscheidenden Moment           | Spieler erfüllt die Siegbedingung oder verliert aufgrund kritischer Gesundheit | Das Spiel zeigt eine Endmeldung (Sieg oder Game Over) und beendet die Spielsession              | US-14             |
             | -             | 180 min       |

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

