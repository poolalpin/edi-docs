---
icon: home
label: Allgemein
---
# Artikelimporte im POOL-ALPIN Webshop
!!!
Hier entsteht derzeit die technische Dokumentation zum Datenaustausch mit POOL-ALPIN
!!!

## Generelles

- Wenn möglich, bevorzugen wir Kataloge im Format BMEcat mit Klassifizierung nach eClass.
- Datenübermittlung bervorzugt via SFTP direkt auf unseren Server.
- Das frühere "Extranet" Self-Service Portal ist nicht mehr verfügbar.

Bei Fragen stehen wir unter ebusiness@pool-alpin.com gerne zur Verfügung.

### BMEcat Formate

- Wir können sowohl BMEcat 1.2 sowie 2005 verarbeiten.

### eClass Version

- Unsere interne Version ist eClass 13, wir können aber auch ältere Versionen verarbeiten.  
  Verwenden Sie bitte ihre aktuellste Version.

### Excel/CSV Kataloge

- Sind weiterhin möglich, falls Sie keinen BMEcat erstellen können.

### REST-API

- Der eigentliche Import in den Webshop erfolgt mittels **JSON** via **REST-API**.  
  Falls es Ihnen möglich ist, dieses Format zu liefern, kann der Umweg über Katalogformate umgangen werden.  
  !!! :zap: API Docs
  Die Dokumentation der API finden sie unter https://shop.pool-alpin.com/synergy/api/docs/import  
  Der Endpunkt **/synergy-import/api/imports/{id}/items** enthält die benötigte JSON-Struktur für Artikelimporte.
  !!!
  
  Für weitere Details gerne jederzeit Kontakt mit uns aufnehmen.