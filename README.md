# Thema: Installation des Projekts

## Hier findest du eine Anleitung fuer die Schritte. Ich hoffe es kann dir helfen.

**Repository klonen**
```bash
git clone https://github.com/benutzername/repositoryname.git
```

**In das Verzeichnis wechseln**
```bash
cd repository
```

**Installation der notwendigen Pakete und Docker-Konfiguration und -Installation**
## Du musst Docker herunterladen. Dafuer gehe auf: https://docs.docker.com/engine/install/
## Schau was fuer ein Prozessor du hast und waehle das richige Docker Version aus und klicke auf die Hyperlink, um die Datei herunterzuladen. 
## Oeffne die Installer und klick immer auf weiter
## Nun sollte es funktionieren, falls es nicht funktioniert, sollst du cmd.exe als Administrator oeffnen und folgende Code ausfuehren
```
wsl --update
```
## Jetzt sollte es gehen, da die wsl nicht mehr "outdated" ist.

**Starten der Applikation in einem Docker-Container**
## Stelle sicher, dass Docker installiert ist.
```bash
docker --version
```

## Oeffne das Terminal und erstelle einen neuen Ordner für dein Projekt:
```cmd
mkdir mein-node-app
cd mein-node-app
```
## Nun gib das Code ein
```cmd
echo > Docker
```
## So kannst du diese Datei oeffnen
```
code Dockerfile
```
## Nun musst du das einfuegen
```VS Code
FROM node:14
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 3000
CMD ["node", "app.js"]
```
## Jetzt kannst du das speichern und diese Code verwenden
```bash
docker build -t mein-node-app .
docker run -p 3000:3000 mein-node-app
```

## Jetzt sollte deine Anwendung in einem Docker-Container laufen.






