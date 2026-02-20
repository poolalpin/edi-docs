---
icon: table
label: Excel Importvorlagen
order: -100
---
!!!tip
Nutzen Sie bitte die Feldbeschreibung, um Erklärungen zu den jeweiligen Spalten in den Excel-Vorlagen zu erhalten. 
!!!
[!ref](feldbeschreibung.md)

!!!base
Bitte verwenden Sie wann immer möglich die [komplette Vorlage](#vorlage-komplett), damit ihre Produkte im POOL-Webshop optimal gefunden werden können.
!!!
+++ Vorlage: Minimalanforderung
Die **minimale Anforderung** für einen Import in den POOL-Webshop, besteht aus folgenden Feldern:
- [x] **Eindeutige Artikelnummer** [number]
- [x] **Artikelname** [name]
- [x] **Artikelbeschreibung** [longDescription]
- [x] **Bestelleinheit** [orderUnit]
- [x] **Netto-Preis der Bestelleinheit** [price1]
- [x] **Produktbild** [files1]  
[!badge variant="warning" icon="eye" text="Wichtig"] Bitte den Abschnitt [Artikelbilder](feldbeschreibung#artikelbilder-und-dokumente) in der Feldbeschreibung beachten!
---
[!badge variant="info" icon="question" text="Optionale Felder"]  
Diese beiden Felder sind für Produkte notwendig, deren Inhalt genauer definiert werden soll:
- [ ] **Inhaltseinheit** (contentUnit)  
ℹ️ Falls ihre Bestelleinheit unterteilbar ist. Beispiel: Ein **Fass** mit **Liter**
- [ ] **Inhaltsmenge** (contentQuantity)  
ℹ️ Falls eine Inhaltseinheit verwendet wird, **muss** die Inhaltsmenge angegeben werden

[!badge variant="info" icon="question" text="Staffelpreise"]  
Für 2 weitere Staffelpreise sind Spalten in der Vorlage vorhanden

[!file](/static/excel/pool-importvorlage-minimal.xlsx)
+++ Vorlage: Komplett
!!!
Diese Vorlage enthält alle erlaubten Importfelder.
!!!
!!!warning
Die nicht benötigten Spalten können ausgeblendet, oder auch gelöscht werden.  
Wichtig ist aber, dass die von ihnen gewählte Struktur mit jeder Übermittlung identisch bleibt!
!!!
[!file](/static/excel/pool-importvorlage-komplett.xlsx)
+++