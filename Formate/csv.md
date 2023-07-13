

# Feldbeschreibung
!!!info Verwendete Symbole und Kennzeichnungen
Kennzeichnung | Beschreibung {class="compact"}
--- | ---
:exclamation: | Pflichtfeld
:heavy_check_mark: | Empfohlenes Feld
[!badge variant="secondary" icon="note" text="Beispieltext"] | Beispiel für den Feldinhalt
!!!

## Artikelnummer
||| Feldname
[!badge number] :exclamation:
||| Format
Text
|||
!!!warning Artikel mit Varianten und/oder Größen
Artikelnummern müssen **eindeutig** sein. Wird meist über eine Erweiterung hinter der Artikelnummer gelöst: *Stammtartikelnummer + Erweiterung*  
[!badge variant="secondary" icon="note" text="123456-001"]
!!!
---
## Artikelname
||| Feldname
[!badge name] :exclamation:
||| Format
Text
|||  

- Die Bezeichnung oder Name des Artikels
[!badge variant="secondary" icon="note" text="T-Shirt Unisex Baumwolle Gr.M"]
---
## Artikelbeschreibung
||| Feldname
[!badge longDescription] :heavy_check_mark:
||| Format
Text
|||
- Die Beschreibung des Artikels, die im Shop auf der Artikel-Detailseite angezeigt wird.  
- Darf einfache HTML oder Markdown Formatierungen enthalten, wie **Fett**, *Kursiv*, un- und nummerierte Listen
---
## Artikelkurzbeschreibung
||| Feldname
[!badge shortDescription]
||| Format
Text
|||
- Die Kurzbeschreibung des Artikels, die im Shop auf den Artikelkarten, sowie den PDF-Belegen angezeigt wird.  
!!!
max. 255 Zeichen
!!!
---
## Bestelleinheit
||| Feldname
[!badge orderUnit] :heavy_check_mark:
||| Format
Text
|||
- Einheit, in der das Produkte bestellt werden kann; es können nur Vielfache dieser
Einheit bestellt werden.
- Auf diese Einheit (oder auf Teile oder auf Vielfache davon) bezieht sich stets auch der
Preis.
!!!Beispiel
Kiste Mineralwasser mit 6 Flaschen  
Bestelleinheit: "Kiste", Inhaltseinheit des Artikels: "Flasche"  
Inhaltsmenge: "6"
!!!
---
## Inhaltseinheit
||| Feldname
[!badge contentUnit]
||| Format
Text
||| Standardeinheit
Stück
|||
- Einheit des Produktes innerhalb einer Bestelleinheit
!!! warning
Wenn sich die Inhaltseinheit von der Bestelleinheit unterscheidet, wird diese zum **Pflichtfeld**
!!!
---
## Inhaltsmenge
||| Feldname
[!badge contentQuantity]
||| Format
Ganz- oder Dezimalzahl
|||
- Anzahl der Inhaltseinheiten pro Bestelleinheit des Artikels
!!! warning
Wenn sich die Inhaltseinheit von der Bestelleinheit unterscheidet, **muss** die Inhaltsmenge angegeben werden
!!!
---
## Preisbezugsmenge
||| Feldname
[!badge priceQuantity]
||| Format
Ganz- oder Dezimalzahl
|||
- Wird dieses Element nicht angegeben, so bezieht sich der Preis auf die angegebene Bestelleinheit.
- Durch Angabe eines Vielfaches oder eines Bruchteils der Bestelleinheit kann davon abgewichen werden.
!!!Beispiel
10 mit Bestelleinheit Karton, d.h. der Preis bezieht sich auf 10 Kartons.
!!!
---
## Mindestbestellmenge
Mengenstaffel der Mind.Best.Mge
Maximale Bestellmenge
Empfohlene Bestellmenge
## Währung
||| Feldname
[!badge currency] :exclamation:
||| Format
Text
|||
Währungsname oder Symbol
[!badge variant="secondary" icon="note" text="EUR"] [!badge variant="secondary" icon="note" text="€"]
## Preis
||| Feldname
[!badge price] :exclamation:
||| Format
Ganz- oder Dezimalzahl
|||
!!!warning
Es wird der **POOL-ALPIN Netto-Einkaufspreis** des Artikels erwartet.  
Zu berechnende prozentuale Abschläge anhand von Rabattlisten sind nicht möglich.  
Im Zweifelsfall bitte mit uns Kontakt aufnehmen.
!!!
### Staffelpreise
Wenn Staffelpreise zur Anwendung kommen, werden diese über entsprechende Feldwiederholungen/Spalten realisiert:  

Preis1   | Ab Menge1 | Preis2 | Ab Menge2 | Preis3 | Ab Menge3 | ... {class="compact"}
---    | ---  | --- | --- | --- | --- | ---
[!badge price1] :exclamation: | [!badge quantity1] :exclamation: | [!badge price2] :exclamation: | [!badge quantity2] :exclamation: | [!badge price2] :exclamation: | [!badge quantity2] :exclamation: 
Warengruppe
eClass
Suchbegriffe
GTIN
Hersteller
Marke
Varianten-Artikelcode
Lieferstatus
Lieferzeit
Lagerstatus
Lagerstand
Optionale Sonderpreise Start
Sonderpreis1
Sonderpreis1 von
Sonderpreis1 bis
…Wiederholungen möglich
Optionale Bilder und Dokumente Start
Bild 1
Bild 2
Bild 3
…Wiederholungen möglich
Datei 1
…Wiederholungen möglich
Optionale Attribute Start
Attribut1 Name

