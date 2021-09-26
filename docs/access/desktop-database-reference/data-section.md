---
title: Datenabschnitt (Access-Desktopdatenbankreferenz)
TOCTitle: Data section
ms:assetid: fd8d31aa-af13-a52f-5e91-20225b8df175
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250303(v=office.15)
ms:contentKeyID: 48548920
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 236b6faf0913bdce857674581e8a7d066968a5b6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626890"
---
# <a name="data-section"></a>Datenabschnitt

**Gilt für**: Access 2013, Office 2013

Der Datenabschnitt definiert die Daten des Rowsets zusammen mit ausstehenden Aktualisierungen, Einfügungen oder Löschvorgängen. Der Datenabschnitt kann null oder mehr Zeilen enthalten. Er kann nur Daten von einem einzigen Rowset enthalten, in dem die Zeile vom Schema definiert wird. Außerdem können wie vorher beschrieben Spalten ohne Daten ausgelassen werden. Falls ein Attribut oder Unterelement im Datenabschnitt verwendet wird und dieses nicht im Schemaabschnitt definiert wurde, wird es ignoriert.

## <a name="string"></a>String

Reservierte XML-Zeichen in Textdaten müssen durch entsprechende Zeichenentitäten ersetzt werden. Beispielsweise muss im Firmenname "Joe's Garage" das einfache Anführungszeichen durch eine Entität ersetzt werden. Die tatsächliche Zeile würde wie folgt aussehen:

```xml  
<z:row CompanyName="Joe&apos;s Garage"/> 
```

Die folgenden Zeichen sind in XML reserviert und müssen durch Zeichenentitäten ersetzt werden: {',",&, \<,\> }.

## <a name="binary"></a>Binär

Binäre Daten sind bin.hex-codiert (das heißt, einem Byte sind zwei Zeichen zugeordnet, nämlich ein Zeichen pro Nibble).

## <a name="datetime"></a>DateTime

Das VT DATE-Format der Variante \_ wird von XML-Data Datentypen nicht direkt unterstützt. Das richtige Format für Daten mit einer Datums- und einer Zeitkomponente lautet yyyy-mm-dd **T** hh:mm:ss.

Weitere Informationen zu durch XML angegebenen Datumsformaten finden Sie unter [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).

Wenn die XML-Data-Spezifikation zwei äquivalente Datentypen definiert (z. B. i4 == int), schreibt ADO den Anzeigenamen vollständig, kann aber beide Formate lesen.

## <a name="managing-pending-changes"></a>Verwalten ausstehender Änderungen

A **Recordset** can be opened in immediate or batch update mode. When opened in batch update mode with client-side cursors, all changes made to the **Recordset** are in a pending state until the **UpdateBatch** method is called. Pending changes are also persisted when the **Recordset** is saved. In XML, they are represented by the use of the "update" elements defined in urn:schemas-microsoft-com:rowset. In addition, if a rowset can be updated, the updatable property must be set to true in the definition of the row. For example, to define that the Shippers table contains pending changes, the row definition would look like the following:

```xml 
<s:ElementType name="row" content="eltOnly" updatable="true"> 
  <s:attribute type="ShipperID"/> 
  <s:attribute type="CompanyName"/> 
  <s:attribute type="Phone"/> 
  <s:extends type="rs:rowbase"/> 
</s:ElementType> 
```

Hiermit wird der Anbieter für Persistenz angewiesen, Daten anzuzeigen, damit ADO ein aktualisierbares **Recordset**-Objekt erstellen kann.

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

