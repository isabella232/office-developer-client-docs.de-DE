---
title: Datenabschnitt (Access PC-Datenbank-Referenz)
TOCTitle: Data section
ms:assetid: fd8d31aa-af13-a52f-5e91-20225b8df175
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250303(v=office.15)
ms:contentKeyID: 48548920
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1b8e3baf4d147edcc739e59933da4697c08cdef0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700773"
---
# <a name="data-section"></a>Datenabschnitt

**Betrifft**: Access 2013, Office 2013

Der Datenabschnitt definiert die Daten des Rowsets zusammen mit ausstehenden Aktualisierungen, Einfügungen oder Löschvorgängen. Der Datenabschnitt kann null oder mehr Zeilen enthalten. Er kann nur Daten von einem einzigen Rowset enthalten, in dem die Zeile vom Schema definiert wird. Außerdem können wie vorher beschrieben Spalten ohne Daten ausgelassen werden. Falls ein Attribut oder Unterelement im Datenabschnitt verwendet wird und dieses nicht im Schemaabschnitt definiert wurde, wird es ignoriert.

## <a name="string"></a>String

Reservierte XML-Zeichen in Textdaten müssen durch entsprechende Zeichenentitäten ersetzt werden. Beispielsweise muss im Firmenname "Joe's Garage" das einfache Anführungszeichen durch eine Entität ersetzt werden. Die tatsächliche Zeile würde wie folgt aussehen:

```xml  
<z:row CompanyName="Joe&apos;s Garage"/> 
```

Die folgenden Zeichen sind in XML reserviert und müssen durch Zeichenentitäten ersetzt werden: {', ", &,\<,\>}.

## <a name="binary"></a>Binary

Binäre Daten sind bin.hex-codiert (das heißt, einem Byte sind zwei Zeichen zugeordnet, nämlich ein Zeichen pro Nibble).

## <a name="datetime"></a>DateTime

Die Variante VT\_Datumsformat von XML-Data-Datentypen nicht direkt unterstützt wird. Das richtige Format für Daten mit einer Datums- und Zeit-Komponente ist jjjj-mm-tt**T**hh: mm:.

Weitere Informationen zu mit XML angegebenen Datumsformaten finden Sie unter [W3C XMLData Notiz](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).

Wenn die XML-Data-Spezifikation zwei äquivalente Datentypen definiert (z. B. i4 == int), schreibt ADO den Anzeigenamen vollständig, kann aber beide Formate lesen.

## <a name="managing-pending-changes"></a>Verwalten ausstehender Änderungen

Ein Recordset-Objekt kann im sofortigen Modus oder im Batchaktualisierungsmodus geöffnet werden. Wenn es im Batchaktualisierungsmodus mit clientseitigen Cursorn geöffnet wird, weisen alle Änderungen am Recordset-Objekt den Status "ausstehend" auf, bis die UpdateBatch-Methode aufgerufen wird. Ausstehende Änderungen werden auch gespeichert, wenn das Recordset-Objekt gespeichert wird. In XML werden sie durch die Verwendung der "update"-Elemente dargestellt, die in urn:schemas-microsoft-com:rowset definiert sind. Wenn darüber hinaus ein Rowset aktualisiert werden kann, muss die updatable-Eigenschaft in der Definition der Zeile auf True festgelegt werden. Um z. B. zu definieren, dass die Shippers-Tabelle ausstehende Änderungen enthält, würde die Zeilendefinition wie folgt aussehen:

```xml 
<s:ElementType name="row" content="eltOnly" updatable="true"> 
  <s:attribute type="ShipperID"/> 
  <s:attribute type="CompanyName"/> 
  <s:attribute type="Phone"/> 
  <s:extends type="rs:rowbase"/> 
</s:ElementType> 
```

Hiermit wird der Anbieter für Persistenz angewiesen, Daten anzuzeigen, damit ADO ein aktualisierbares **Recordset** -Objekt erstellen kann.

Die folgenden Beispieldaten veranschaulichen, wie Einfügungen, Änderungen und Löschvorgänge in der gespeicherten Datei aussehen:

```xml 
<rs:data> 
  <z:row ShipperID="2" CompanyName="United Package"  
    Phone="(503) 555-3199"/> 
<rs:update> 
  <rs:original> 
    <z:row ShipperID="3" CompanyName="Federal Shipping"  
      Phone="(503) 555-9931"/> 
  </rs:original> 
  <z:row Phone="(503) 552-7134"/> 
</rs:update> 
<rs:insert> 
  <z:row ShipperID="12" CompanyName="Lightning Shipping"  
    Phone="(505) 111-2222"/> 
  <z:row ShipperID="13" CompanyName="Thunder Overnight"  
    Phone="(505) 111-2222"/> 
  <z:row ShipperID="14" CompanyName="Blue Angel Air Delivery"  
    Phone="(505) 111-2222"/> 
</rs:insert> 
<rs:delete> 
  <z:row ShipperID="1" CompanyName="Speedy Express" Phone="(503) 555-9831"/> 
</rs:delete> 
</rs:data> 
```

Eine Aktualisierung enthält immer die gesamten ursprünglichen Zeilendaten, gefolgt von den geänderten Zeilendaten. Die geänderte Zeile kann alle Spalten oder nur die tatsächlich geänderten Spalten enthalten. Im vorherigen Beispiel wird die Zeile für "Shipper 2" nicht geändert. Nur in der Phone-Spalte wurden Werte für Shipper 3 geändert. Dies ist deshalb die einzige Spalte, die in der geänderten Zeile enthalten ist. Die eingefügten Zeilen für "Shipper 12", "Shipper 13" und "Shipper 14" werden unter einem einzigen rs:insert-Tag in einem Batch verarbeitet. Beachten Sie, dass gelöschte Zeilen ebenfalls in einem Batch verarbeitet werden können, auch wenn dies im obigen Beispiel nicht dargestellt ist.

