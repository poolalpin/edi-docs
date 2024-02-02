---
label: Feldbeschreibung
icon: list-unordered
date: 2024-02-02
---

# Feldbeschreibung
!!! Verwendete Symbole und Kennzeichnungen
Kennzeichnung | Beschreibung {class="compact"}
--- | ---
:exclamation: | Pflichtfeld
:heavy_check_mark: | Empfohlenes Feld
[!badge variant="secondary" icon="note" text="Beispieltext"] | Beispiel für den Feldinhalt
!!!
!!!dark
Standardwerte werden bei fehlenden Daten in einer Importdatei automatisch gesetzt.
!!!
---
## Artikelnummer
||| Feldname
[!badge number] :exclamation:
||| Format
Text
|||
!!!warning Artikel mit Varianten und/oder Größen
Artikelnummern müssen **eindeutig** sein. Wird meist über eine Erweiterung hinter der Artikelnummer gelöst:  
*Stammartikelnummer + Erweiterung*   
[!badge variant="secondary" icon="note" text="123456-001"]
!!!
---
## Hersteller-Artikelnummer
||| Feldname
[!badge manufacturerNumber]
||| Format
Text
|||
- Die Hersteller-Artikelnummer
---
## Varianten-Artikelcode
||| Feldname
[!badge groupId]
||| Format
Text
|||
- **Frei wählbare Zeichenfolge**, die dazu dient, Artikel mit Varianten im Webshop zu gruppieren
- Alle Artikel mit **identischem** Code sind im Shop im Artikeldetail über ein Auswahlfeld selektierbar  
[!badge variant="secondary" icon="note" text="t-shirt-variante-0001"]
!!!success Erlaubte Zeichen
Alphanumerische Zeichen des englischen Alphabets: `a-z`, `A-Z`, `0-9`.  
Ergänzend können die Sonderzeichen Bindestrich `-`, Unterstrich `_` und Punkt `.` verwendet werden.
!!!
!!!danger Nicht erlaubte Zeichen
`Leerzeichen` `,` `;` `\` `/` `:` `*` `?` `"` `'` `<` `>` `|`
!!!
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
!!!success
Artikel mit identer GTIN werden im Artikeldetail auch im Abschnitt "Identischer Artikel bei anderen Lieferanten" angezeigt.
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
!!!warning
max. 255 Zeichen
!!!
---
## Bestelleinheit
||| Feldname
[!badge orderUnit] :exclamation:
||| Format
Text
||| Standardwert
Stück
|||
- Einheit, in der das Produkt bestellt werden kann; es können nur Vielfache dieser
Einheit bestellt werden.
- Auf diese Einheit (oder auf Teile oder auf Vielfache davon) bezieht sich stets auch der
Preis.
!!!Beispiel
Kiste Mineralwasser mit 6 Flaschen:  
Bestelleinheit: **Kiste**, Inhaltseinheit des Artikels: **Flasche**  
Inhaltsmenge: **6**
!!!
---
### Inhaltseinheit (optional)
!!! danger
Darf nur verwendet werden, wenn sich die Inhaltseinheit von der [Bestelleinheit](#bestelleinheit) unterscheidet.  
In diesem Fall werden Inhaltseinheit und Inhaltsmenge zu **Pflichtfeldern**
!!!
||| Feldname
[!badge contentUnit]
||| Format
Text
|||
- Einheit des Produktes innerhalb einer Bestelleinheit
---
### Inhaltsmenge (optional)
!!! danger
Wird eine [Inhaltseinheit](#inhaltseinheit-optional) verwendet, **muss** auch die Inhaltsmenge angegeben werden.
!!!
||| Feldname
[!badge contentQuantity]
||| Format
Ganz- oder Dezimalzahl
|||
- Anzahl der Inhaltseinheiten pro [Bestelleinheit](#bestelleinheit) des Artikels
---
## Preisbezugsmenge
||| Feldname
[!badge priceQuantity]
||| Format
Ganz- oder Dezimalzahl
|||Standardwert
1
|||
- Wird dieses Element **nicht** angegeben, so bezieht sich der Preis auf 1 Einheit der angegebenen [Bestelleinheit](#bestelleinheit).
- Durch Angabe eines Vielfaches oder eines Bruchteils der Bestelleinheit kann davon abgewichen werden.
!!!Beispiel
100 mit Bestelleinheit Stück, d.h. der Preis bezieht sich auf 100 Stück.
!!!
---
## Mindestbestellmenge
||| Feldname
[!badge minimumOrderQuantity]
||| Format
Ganz- oder Dezimalzahl
||| Standardwert
1
|||
- Verpflichtende Mindestbestellmenge für das Produkt, bezogen auf die [Bestelleinheit](#bestelleinheit)
---
## Bestellintervall-Menge
||| Feldname
[!badge quantityInterval]
||| Format
Ganz- oder Dezimalzahl
||| Standardwert
1
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
||| Standardwert
1
|||
- Kann verwendet werden, um den Preis in einer leichter vergleichbaren Einheit darzustellen
!!!Beispiel
Preis per Flasche à 650 Milliliter = 33,00 €  
[!badge price] 33,00 / [!badge contentQuantity] 650 = 0,0508 € per Milliliter  
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

Preis1   | Ab Menge1 | Preis2 | Ab Menge2 | Preis3 | Ab Menge3 | max.5 {class="compact"}
---    | ---  | --- | --- | --- | --- | ---
[!badge price1] :exclamation: | [!badge quantity1] :exclamation: | [!badge price2] :exclamation: | [!badge quantity2] :exclamation: | [!badge price2] :exclamation: | [!badge quantity2] :exclamation: | ...

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
## Nachhaltiger "Öko" Artikel
||| Feldname
[!badge isEcoProduct]
||| Format
boolean 
|||
- Kennzeichnet den Artikel im Shop mit einem Öko-Label 🌱, nach dem auch gefiltert werden kann.
---
## Warengruppe(n)
||| Feldname
[!badge categories]
||| Format
Text
|||
- Die zugehörige(n) Warengruppe(n) des Artikels
- Mehrere Warengruppen mittels Feld/Spaltenwiederholung darstellen  

categories1   | categories2 | categories3 | max.5 {class="compact"}
---    | ---  | --- | ---
[!badge variant="secondary" icon="note" text="Brotaufstriche"] | [!badge variant="secondary" icon="note" text="Süßwaren"] | [!badge variant="secondary" icon="note" text="Lebensmittel"] | ...

---
## eClass
||| Feldname
[!badge eclass] :heavy_check_mark:
||| Format
Text
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
- Mehrere Begriffe mit Komma, ohne Leerzeichen separieren  
[!badge variant="secondary" icon="note" text="Begriff1,Begriff2,Begriff3,..."]
---
## Artikelbilder und Dokumente
||| Feldname
[!badge files]
||| Format
Text
|||
!!!success Wichtig
Links zu den Dateien werden bevorzugt, diese werden dann automatisch in den Webshop geladen!  
[!badge variant="secondary" icon="note" text="http(s)://example.com/bilder/artikelbild1.jpg"]
!!!
- Artikelbilder :frame_with_picture: (.jpg|.png|.webp) und Datenblätter :page_facing_up: (.pdf) sind möglich
- Die erste Bilddatei wird zum Vorschaubild
- Mehrere Dateien mittels Feld/Spaltenwiederholung darstellen 

files1   | files2 | files3 | max.5 {class="compact"}
---    | ---  | --- | ---
[!badge variant="secondary" icon="note" text="http(s)://example.com/bilder/artikelbild1.jpg"] | [!badge variant="secondary" icon="note" text="http(s)://example.com/bilder/artikelbild2.jpg"] | [!badge variant="secondary" icon="note" text="http(s)://example.com/bilder/datenblatt1.pdf"] | ...

!!!danger Wenn ihre Produktbilder nicht online verfügbar sind?
In diesem Fall benötigen wir sämtliche Bilder, um diese vor der Produkteinspielung zu importieren.  
[!badge variant="warning" icon=":zap:" iconAlign="left" text="Vorsicht"] 
Die angegebenen Dateinamen aus der Artikeltabelle müssen 1:1 mit den übermittelten Dateien übereinstimmen!  
Groß/Kleinschreibung beachten. `Dateiname.jpg` ist nicht gleich `dateiname.JPG`
!!!
---
## Produktattribute
||| Feldname
[!badge 'beliebig']
||| Format
Text
|||
- Hiermit können weitere Artikeleigenschaften definiert werden, die in der Artikeldetailansicht angezeigt werden
- Mehrere Eigenschaften mittels Feld/Spaltenwiederholung darstellen, wobei der ==Spaltenname== die ==Bezeichnung== und der ==Feldinhalt== den ==Wert== darstellt

[!badge variant="secondary" icon="note" text="Material"]   | [!badge variant="secondary" icon="note" text="Durchmesser"] | [!badge variant="secondary" icon="note" text="Länge"] | max.5 {class="compact"}
---    | ---  | --- | ---
[!badge variant="secondary" icon="note" text="Stahl"]   | [!badge variant="secondary" icon="note" text="8 mm"] | [!badge variant="secondary" icon="note" text="130 cm"] | ...

- Alternativ können die Eigenschaften auch als Textkette in einem einzelnen Feld dargestellt werden.  
  Das vorherige Beispiel könnte dann so aussehen:  
`Material=Stahl,Durchmesser=8mm,Länge=130cm`
---
## Lieferstatus
||| Feldname
[!badge deliveryStatus]
||| Format
Text
||| Standardwert
`available`
|||
- Gibt die Verfügbarkeit des Artikels an  

!!!warning 4 mögliche Werte
||| `available`
Artikel immer verfügbar
|||`not_available`
Artikel derzeit nicht erhältlich
|||`on_request`
Artikel muss angefragt werden
|||`tracked`
Artikel hat eine bestimmte Lieferzeit
|||
!!!
---
## Lieferzeit
||| Feldname
[!badge deliveryTime]
||| Format
Ganzzahl
|||
- Pflichtfeld, wenn der Lieferstatus `tracked` verwendet wird
- Gibt die Lieferzeit des Artikels in Tagen an  
---
## Lagerstatus
||| Feldname
[!badge stockStatus]
||| Format
Text
||| Standardwert
`in_stock`
|||
- Gibt den Lagerstatus des Artikels an  

!!!warning 3 mögliche Werte
|||`in_stock`
Artikel immer lagernd
|||`sold_out`
Artikel derzeit nicht am Lager
|||`tracked`
Begrenzte Artikelzahl verfügbar
|||
!!!
---
## Lagerstand
||| Feldname
[!badge inventory]
||| Format
Ganzzahl
|||
- Pflichtfeld, wenn der Lagerstatus `tracked` verwendet wird
- Anzahl Lagerstand des Artikels  
!!!
Hier sollten regelmäßige Aktualisierungen übermittelt werden.
!!!
---
## Verpackungseinheiten
||| Feldnamen
[!badge unit] [!badge minimumQuantity] [!badge maximumQuantity]
||| Format
Text
|||
- Wenn angegeben, scheinen diese im Artikeldetail auf und legen die entsprechende Menge [Bestelleinheiten](#bestelleinheit) in den Warenkorb.
!!!Beispiel
Kiste Mineralwasser mit 6 Flaschen:  
Bestelleinheit: **Kiste**, Inhaltseinheit des Artikels: **Flasche**  
Inhaltsmenge: **6**

- Verpackungseinheit **Palette** enthält mindestens 25 **Kiste**
- Verpackungseinheit **Container** enthält mindestens 500 **Kiste**
!!!  
- [!badge maximumQuantity] dient derzeit nur informativen Zwecken, verwendet und angezeit wird immer [!badge minimumQuantity]
- Mehrere Verpackungseinheiten mittels Feld/Spaltenwiederholung darstellen

unit1   | minimumQuantity1 | maximumQuantity1 | max.5 {class="compact"}
---    | ---  | --- | ---
[!badge variant="secondary" icon="note" text="Palette"] | [!badge variant="secondary" icon="note" text="25"] | [!badge variant="secondary" icon="note" text="50"] | ...

---
## Sonderpreise (optional)
!!!
Wird in der Praxis meist mit eigenen Sonderpreislisten erledigt, kann aber auch direkt im Gesamtkatalog übermittelt werden
!!!
- :information_source: Aktuell sind keine Staffel-Sonderpreise möglich  
- Am Ende einer Artikelzeile folgende Spalten anängen:  

[!badge specialPrice]   | [!badge startDate] | [!badge endDate] {class="compact"}
---    | ---  | --- 
`preis` | `Datum von` | `Datum bis`
