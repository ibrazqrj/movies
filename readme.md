# **Projektdokumentation**

## **Titelblatt**
- **Projektname**: TMDB Movie Watchlist App
- **Modul**: M294
- **Vorname Nachname**: [Ibrahim Zeqiraj]
- **Abgabedatum**: [20.09.2024]

## **Inhaltsverzeichnis**
1. [Projektidee](#projektidee)
2. [Anforderungskatalog](#anforderungskatalog)
3. [Klassendiagramm](#klassendiagramm)
4. [Storyboard](#storyboard)
5. [Screen-Mockups](#screen-mockups)
6. [REST-Schnittstellen](#rest-schnittstellen)
7. [Testplan](#testplan)
8. [Installationsanleitung](#installationsanleitung)
9. [Hilfestellungen](#hilfestellungen)

---

## **Projektidee**

Das Ziel dieses Projekts ist die Entwicklung einer Movie Watchlist Applikation, die auf den Daten der **The Movie Database (TMDb) API** basiert. Die Benutzer können Filme durchsuchen, die ihnen gefallen, und diese zu ihrer persönlichen Watchlist hinzufügen oder entfernen. Der Benutzer kann zudem Details zu den Filmen einsehen, darunter Genres, Bewertungen und Beschreibungen.

Funktionen wie **CRUD-Operationen** (Erstellen, Lesen, Bearbeiten und Löschen) werden über das Frontend simuliert und werden nicht ausgeführt, da sich das Projekt im Frontend befindet. Benutzer können z. B. ihre Watchlist verwalten, ohne Backend-Unterstützung.

---

## **Anforderungskatalog**

1. **Film-Suche**: 
   - Benutzer können nach Filmen suchen, indem sie Titel in eine Suchleiste eingeben.
   
2. **Watchlist-Funktionalität**:
   - Filme können zur Watchlist hinzugefügt und von dieser entfernt werden.
   
3. **Film-Details anzeigen**:
   - Benutzer können detaillierte Informationen zu einem Film (z. B. Beschreibung, Genre, Laufzeit, Bewertung) einsehen.

4. **CRUD-Simulation**:
   - Aktionen wie „Film bearbeiten“ und „Film löschen“ werden simuliert und führen zu Konsolen-Fehlermeldungen, da kein Backend verfügbar ist.

5. **API-Daten verarbeiten**:
   - Die Applikation greift auf die TMDb-API zu, um Filmdaten anzuzeigen.

---

## **Klassendiagramm**

Das folgende Diagramm zeigt die Modellklassen, die in der Applikation verwendet werden:

![[1.png]]

---

## Storyboard

### Startseite:
- Der Benutzer sieht eine Liste beliebter Filme.
- Er kann nach spezifischen Filmen suchen.
- Er kann Filme zur Watchlist hinzufügen.

![[startseite.png]]
### Filmdetails:
- Der Benutzer klickt auf einen Film und sieht detaillierte Informationen, wie Beschreibung, Genres und Bewertung.

![[details.png]]
### Watchlist:
- Der Benutzer wechselt zur Watchlist und sieht alle hinzugefügten Filme.
- Der Benutzer kann Filme aus der Watchlist entfernen.

![[watchlist.png]]
### About:
- Der Benutzer erhält die Information wozu die Seite dient.

![[about.png]]

--- 
## Screen-Mockups

### Startseite:
- **Suchleiste oben**: Benutzer kann nach einem Film suchen.
- **Filmliste**: Beliebte Filme werden in einer Gitteransicht dargestellt.

### Filmdetailseite:
- **Filmcover links**: Ein großes Bild des Filmcovers.
- **Filmdetails**: Titel, Genre, Beschreibung, Bewertung werden rechts angezeigt.
- **Buttons**: Zur Watchlist hinzufügen, Bearbeiten, Löschen.

### Watchlist:
- **Liste der hinzugefügten Filme**: Alle Filme, die der Benutzer zur Watchlist hinzugefügt hat, werden aufgelistet.
- **Entfernen-Button**: Neben jedem Film gibt es die Option, diesen aus der Watchlist zu entfernen.
---

## REST-Schnittstellen

### Filmliste (populäre Filme):
- **URL**: `https://api.themoviedb.org/3/movie/popular`
- **Methode**: GET
- **Beschreibung**: Ruft die Liste beliebter Filme ab.

### Film-Suche:
- **URL**: `https://api.themoviedb.org/3/search/movie?query={searchTerm}`
- **Methode**: GET
- **Beschreibung**: Ruft Filme basierend auf dem Suchbegriff ab.

### Filmdetails:
- **URL**: `https://api.themoviedb.org/3/movie/{movieId}`
- **Methode**: GET
- **Beschreibung**: Ruft detaillierte Informationen zu einem Film ab.
---

## Testplan

### Testfälle

![[Pasted image 20240918183857.png]]

---

## Installationsanleitung

### Voraussetzungen:
- Node.js muss installiert sein.
- Ein API-Schlüssel für TMDb ist erforderlich.

### Schritte:

1. **Clone das Repository**:
   ```bash
   git clone https://github.com/ibrazqrj/movies.git
   ```
2. Gehe in das Projektverzeichnis:
```
cd tmdb-app
```
3. Installiere die Abhängigkeiten
```
npm install

```
5. API-Schlüssel in der .env-Datei eintragen (Dein Eigenes)
```
REACT_APP_TMDB_API_KEY=your_api_key
```
6. Starte die Applikation
```
npm start
```