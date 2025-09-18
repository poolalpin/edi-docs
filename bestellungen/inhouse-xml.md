---
label: Pool XML-Bestellung
icon: file-code
---
Aktuell steht für die Übermittlung von Bestellungen ein internes XML-Format zur Verfügung, das für den Import von Bestellungen auf Lieferantenseite verwendet werden kann.

!!!warning Wichtig
Zwar enthält jede Produktposition ein `<deliveryAddress>` Element, es wird aber immer nur **EINE** Lieferadresse je Bestellung erlaubt.  
Es reicht somit, die Lieferadresse jeweils aus der 1. Produktposition zu ermitteln.
!!!

+++ XML-Bestellung Struktur
```xml
<?xml version="1.0" encoding="UTF-8"?>
<result>
    <type>order</type>
    <origin>TYPE_SHOP</origin>
    <number>134654</number>
    <status>STATUS_COMPLETED</status>
    <salesOrderNumber>86284</salesOrderNumber>
    <purchaseOrderNumber>134654</purchaseOrderNumber>
    <orderDate>2025-09-17T00:00:00+00:00</orderDate>
    <currencyCode>EUR</currencyCode>
    <termsOfPaymentContent>21 Tage 3%, 45 Tage netto</termsOfPaymentContent>
    <termsOfDeliveryContent>CPT - Fracht bez. bis vereinbarter Bestimmungsort.</termsOfDeliveryContent>
    <costCentre>1350ZL</costCentre>
    <orderReference/>
    <desiredDeliveryDate>2025-09-19T00:00:00+00:00</desiredDeliveryDate>
    <taxfree>true</taxfree>
    <customerAccount>
        <id>123456</id>
        <name>Bergbahn AG Musterdorf</name>
        <gln>1234567890123</gln>
    </customerAccount>
    <customerContact>
        <id>28869</id>
        <fullName>Max Muster</fullName>
        <email>m.muster@example.com</email>
        <phone>066412345678</phone>
    </customerContact>
    <supplier>
        <id>54321</id>
        <registerNumber>120036z</registerNumber>
        <gln/>
        <email>maria.muster@example.com</email>
        <phone>+43 (1234) 12345</phone>
        <name><![CDATA[Musterliferant GmbH]]></name>
        <street>Musterstrasse</street>
        <number>37</number>
        <zip>1234</zip>
        <city>Musterstadt</city>
        <state/>
        <country>Österreich</country>
        <postboxNumber>Postfach 126</postboxNumber>
        <postboxPostcode>1234</postboxPostcode>
        <postboxCity>Musterstadt</postboxCity>
        <uid>ATU1234567</uid>
    </supplier>
    <invoiceAddress>
        <salutation/>
        <firstName>Max</firstName>
        <lastName>Muster</lastName>
        <accountName>Bergbahn AG Musterdorf</accountName>
        <street>Mustergasse</street>
        <number>1a</number>
        <city>Musterstadt</city>
        <zip>1234</zip>
        <state>Tirol</state>
        <country>Österreich</country>
        <uid>ATU87654321</uid>
        <email>m.muster@example.com</email>
        <phone>0066412345678</phone>
        <id>168</id>
        <postboxCity></postboxCity>
        <postboxNumber></postboxNumber>
        <postboxPostcode></postboxPostcode>
        <costCentre>1350ZL</costCentre>
        <contactAddressId>168</contactAddressId>
        <formOfAddress>0</formOfAddress>
    </invoiceAddress>
    <items>
        <entry>
            <id>301990</id>
            <name>Zylinderschraube ISO 4762 - 8.8 - verzinkt blau - M12 X 55</name>
            <number>008412</number>
            <created>2025-09-17T06:03:18+00:00</created>
            <changed>2025-09-17T06:03:18+00:00</changed>
            <deliveryAddress>
                <salutation/>
                <firstName>Max</firstName>
                <lastName>Muster</lastName>
                <accountName>Bergbahn AG Musterdorf</accountName>
                <street>Mustergasse</street>
                <number>36</number>
                <city>Musterdorf</city>
                <zip>1234</zip>
                <state>Tirol</state>
                <country>Österreich</country>
                <uid>ATU12345678</uid>
                <email>m.muster@example.com</email>
                <phone>06641234567</phone>
                <id>10468</id>
                <postboxCity></postboxCity>
                <postboxNumber></postboxNumber>
                <postboxPostcode></postboxPostcode>
                <costCentre>1350ZL</costCentre>
                <contactAddressId>10468</contactAddressId>
                <formOfAddress>0</formOfAddress>
            </deliveryAddress>
            <quantity>100</quantity>
            <orderUnit>Stück</orderUnit>
            <tax/>
            <price>0.256414</price>
            <discount>0</discount>
            <description></description>
            <totalNetPrice>25.64</totalNetPrice>
        </entry>
        <entry>
            <id>301991</id>
            <name>Spanplattenschraube - Senkkopf - Teilgewinde - verzinkt gelb - 5 X 70 - TX25</name>
            <number>017615</number>
            <created>2025-09-17T06:03:18+00:00</created>
            <changed>2025-09-17T06:03:18+00:00</changed>
            <deliveryAddress>
                <salutation/>
                <firstName>Max</firstName>
                <lastName>Muster</lastName>
                <accountName>Bergbahn AG Musterdorf</accountName>
                <street>Mustergasse</street>
                <number>36</number>
                <city>Musterdorf</city>
                <zip>1234</zip>
                <state>Tirol</state>
                <country>Österreich</country>
                <uid>ATU12345678</uid>
                <email>m.muster@example.com</email>
                <phone>06641234567</phone>
                <id>10468</id>
                <postboxCity></postboxCity>
                <postboxNumber></postboxNumber>
                <postboxPostcode></postboxPostcode>
                <costCentre>1350ZL</costCentre>
                <contactAddressId>10468</contactAddressId>
                <formOfAddress>0</formOfAddress>
            </deliveryAddress>
            <quantity>800</quantity>
            <orderUnit>Stück</orderUnit>
            <tax/>
            <price>0.038836</price>
            <discount>0</discount>
            <description></description>
            <totalNetPrice>31.07</totalNetPrice>
        </entry>
        <entry>
            <id>301992</id>
            <name>Spanplattenschraube - Senkkopf - Teilgewinde - verzinkt gelb - 6 X 50 - TX30</name>
            <number>017616</number>
            <created>2025-09-17T06:03:18+00:00</created>
            <changed>2025-09-17T06:03:18+00:00</changed>
            <deliveryAddress>
                <salutation/>
                <firstName>Max</firstName>
                <lastName>Muster</lastName>
                <accountName>Bergbahn AG Musterdorf</accountName>
                <street>Mustergasse</street>
                <number>36</number>
                <city>Musterdorf</city>
                <zip>1234</zip>
                <state>Tirol</state>
                <country>Österreich</country>
                <uid>ATU12345678</uid>
                <email>m.muster@example.com</email>
                <phone>06641234567</phone>
                <id>10468</id>
                <postboxCity></postboxCity>
                <postboxNumber></postboxNumber>
                <postboxPostcode></postboxPostcode>
                <costCentre>1350ZL</costCentre>
                <contactAddressId>10468</contactAddressId>
                <formOfAddress>0</formOfAddress>
            </deliveryAddress>
            <quantity>1000</quantity>
            <orderUnit>Stück</orderUnit>
            <tax/>
            <price>0.044042</price>
            <discount>0</discount>
            <description></description>
            <totalNetPrice>44.04</totalNetPrice>
        </entry>
    </items>
    <netShippingCosts>0</netShippingCosts>
    <totalPrice>100.75</totalPrice>
    <netSurcharge>0</netSurcharge>
    <noteToSupplier/>
    <asset_id/>
</result>
```
+++ XML-Bestellung Feldbeschreibung
Eine Beschreibung der XML-Strukur findet sich auf unserer Sharepoint-Seite
[!ref icon="link" target="blank" text="Feldbeschreibung XML-Bestellung"](https://alpinpool.sharepoint.com/:x:/s/dm/EUGGf_HrniNIqgHc-HTpTWQBMqGRxenLYErzy5f2ibt69w?e=2g2AXL)
+++ XML-Bestellung Testdatei
[!file](/static/xml/PA_OrderConfirmation-134654.xml)