

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
## Varianten-Artikelcode
||| Feldname
[!badge groupId]
||| Format
Text
|||
- **Frei wählbare Zeichenfolge**, die dazu dient, Artikel mit Varianten im Webshop zu gruppieren
- Alle Artikel mit ==identischem Code== sind im Shop im Artikeldetail über ein Auswahlfeld selektierbar
==- Beispieldarstellung im Shop :icon-image:
![Variantenanzeige im Shop](../static/variantenauswahl.png)
===
---
## GTIN / EAN
||| Feldname
[!badge globalTradeItemNumber] :heavy_check_mark:
||| Format
Text 
|||
- EAN-Code des Artikels
!!!warning
Darf nur 12 oder 13 Stellen haben
!!!
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
|||Standardwert
1
|||
- Wird dieses Element nicht angegeben, so bezieht sich der Preis auf die angegebene Bestelleinheit.
- Durch Angabe eines Vielfaches oder eines Bruchteils der Bestelleinheit kann davon abgewichen werden.
!!!Beispiel
10 mit Bestelleinheit Karton, d.h. der Preis bezieht sich auf 10 Kartons.
!!!
---
## Mindestbestellmenge
||| Feldname
[!badge minimumOrderQuantity]
||| Format
Ganz- oder Dezimalzahl
|||
- Verpflichtende Mindesbestellmenge für das Produkt, bezogen auf die [Bestelleinheit](#bestelleinheit)
---
## Bestellintervall-Menge
||| Feldname
[!badge quantityInterval]
||| Format
Ganz- oder Dezimalzahl
|||
- Angabe der Staffelung, in der das Produkt bestellt werden kann
- Die Zählung für diese Staffelung beginnt stets mit der angegebenen
Mindestbestellmenge.
- Die Einheit für die Mengenstaffel ist die Bestelleinheit.
!!!
Beispiel: 1 (d.h. 5, 6, 7, ... Kisten)  
Beispiel: 2 (d.h. 4, 6, 8, ... Kisten)
!!!
---
## Maximale Bestellmenge
||| Feldname
[!badge maximumOrderQuantity]
||| Format
Ganz- oder Dezimalzahl
|||
---
## Empfohlene Bestellmenge
||| Feldname
[!badge recommendedOrderQuantity]
||| Format
Ganz- oder Dezimalzahl
|||
- Unverbindlich empfohlene Bestellmenge; wird im Artikeldetail angezeigt
---
## Preisreferenzmenge
||| Feldname
[!badge priceReferenceQuantity]
||| Format
Ganz- oder Dezimalzahl
|||
- Kann verwendet werden, um den Preis in einer leichter vergleichbaren Einheit darzustellen
!!!Beispiel
Preis per Flasche à 650 Milliliter = 33,00 €  
[!badge price] 33 / [!badge contentQuantity] 650 = 0,0508 € per Milliliter  
Preis per Milliliter 0,0508 * [!badge priceReferenceQuantity] 1000 = 50,7692 € per 1000 Milliliter
!!!
---
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
### Staffelpreise (optional)
Wenn Staffelpreise zur Anwendung kommen, werden diese über entsprechende Feldwiederholungen/Spalten realisiert:  

Preis1   | Ab Menge1 | Preis2 | Ab Menge2 | Preis3 | Ab Menge3 | ... {class="compact"}
---    | ---  | --- | --- | --- | --- | ---
[!badge price1] :exclamation: | [!badge quantity1] :exclamation: | [!badge price2] :exclamation: | [!badge quantity2] :exclamation: | [!badge price2] :exclamation: | [!badge quantity2] :exclamation:

---
## Hersteller
||| Feldname
[!badge manufacturer]
||| Format
Text
|||
- Hersteller des Artikels  
[!badge variant="secondary" icon="note" text="Ferrero"]
---
## Marke
||| Feldname
[!badge brand]
||| Format
Text
|||
- Markenname des Artikels  
[!badge variant="secondary" icon="note" text="Nutella"]
---
## Warengruppen(n)
||| Feldname
[!badge categories]
||| Format
Text
|||
- Die zugehörige(n) Warengruppe(n) des Artikels
- Mehrere Warengruppen mittels Feld/Spaltenwiederholung darstellen  

categories1   | categories2 | categories3 | ... {class="compact"}
---    | ---  | --- | ---
[!badge variant="secondary" icon="note" text="Brotaufstriche"] | [!badge variant="secondary" icon="note" text="Süßwaren"] | [!badge variant="secondary" icon="note" text="Lebensmittel"] | ...

---
## eClass
||| Feldname
[!badge eclass] :heavy_check_mark:
||| Format
Ganzzahl
|||
- Kategorie des Artikels nach [!badge variant="info "target="blank" text="eClass"](https://eclass.eu/eclass-standard/einfuehrung) Standard  
- Ermöglicht die automatische Kategorie-Zuweisung im Webshop  
[!badge variant="secondary" icon="note" text="27142217"] [!badge variant="secondary" icon="note" text="27-14-22-17"]
---
## Suchbegriffe
||| Feldname
[!badge searchTerms]
||| Format
Text
|||
- Ein oder mehrere Suchbegriffe für den Artikel
- Mehrere Begriffe mit Komma separieren  
[!badge variant="secondary" icon="note" text="Begriff1,Bergriff2,Begriff3,..."]
---
## Artikelbilder und Dokumente

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

