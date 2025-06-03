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
## Aufgabe 4
Erklären Sie hier, wie Sie das Passwort aus Ihrer lokalen `.env` auf Azure übertragen.
