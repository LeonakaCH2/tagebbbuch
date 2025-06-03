# LB 324

## Aufgabe 2
Erklären Sie hier, wie man `pre-commit` installiert.

## Pre-Commit und Push-Check einrichten

### 1. Voraussetzungen

Zuerst muss pre-commit installiert werden mit pip:
```bash
pip install pre-commit
```
Danach wird das Projekt hiermit initialisiert:
```bash
pre-commit clean
pre-commit install
```
Optional können alle Checks auch manuell getestet werden:
```bash
pre-commit run --all-files
```

### 🌐 Live-URL der Applikation

Die Anwendung ist erreichbar unter:

👉 [https://lb324-leont-hrdybec6b8haf9he.canadacentral-01.azurewebsites.net/]

> Die URL stammt aus dem Azure Deployment Center und zeigt die laufende Instanz nach erfolgreichem Deployment aus dem `main`-Branch.


## Aufgabe 4 – Deployment auf Azure mit Passwort aus `.env`

Die Applikation wird über das Azure Deployment Center automatisch ausgeliefert, sobald Änderungen in den `main`-Branch gemerged werden.

Damit das Login in der App korrekt funktioniert, muss das geheime Passwort, das lokal in der `.env`-Datei definiert ist, auf Azure übertragen werden.

### 🔐 Passwort aus `.env` in Azure übertragen

1. Öffne das Azure-Portal
2. Navigiere zu deiner Web App unter **App Services**
3. Gehe zu **Einstellungen** → **Umgebungsvariablen**
4. Füge eine neue Einstellung hinzu:
   - **Name:** `PASSWORD`
   - **Wert:** Dein Passwort
5. Speichern und App neu starten (wenn notwendig)

### 🧠 Hinweis

Die Anwendung verwendet `os.getenv("PASSWORD")`, um das Passwort zu lesen.
Lokal kann dieses Passwort weiterhin über eine `.env`-Datei bereitgestellt werden.
In Azure ist keine `.env`-Datei notwendig – die Umgebungsvariable wird direkt aus den App-Einstellungen geladen.
