---
title: XML-Speicherformat
TOCTitle: XML Persistence Format
ms:assetid: 499f335c-ee1f-c803-e3a8-034b8decf1ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249226(v=office.15)
ms:contentKeyID: 48544643
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e7825d55c6f0c2f900f61a325265dce048f965e5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705974"
---
# <a name="xml-persistence-format"></a>XML-Speicherformat

**Betrifft**: Access 2013, Office 2013

## <a name="xml-persistence-format"></a>XML-Speicherformat

ADO verwendet die UTF-8-Codierung für den gespeicherten XML-Datenstrom.

Das ADO-XML-Format ist in zwei Abschnitte unterteilt, nämlich einen Schemaabschnitt, gefolgt vom Datenabschnitt. Es folgt eine XML-Beispieldatei für die Shippers-Tabelle aus der Northwind-Datenbank. Verschiedene XML-Komponenten werden im Anschluss an das Beispiel behandelt.

```xml
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"  
xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"  
xmlns:rs="urn:schemas-microsoft-com:rowset"  
xmlns:z="#RowsetSchema">  
  <s:Schema id="RowsetSchema">  
    <s:ElementType name="row" content="eltOnly" rs:updatable="true">  
      <s:AttributeType name="ShipperID" rs:number="1"  
        rs:basetable="shippers" rs:basecolumn="ShipperID" 
        rs:keycolumn="true">  
        <s:datatype dt:type="int" dt:maxLength="4" rs:precision="10"  
          rs:fixedlength="true" rs:maybenull="false"/>  
      </s:AttributeType>  
      <s:AttributeType name="CompanyName" rs:number="2"  
        rs:nullable="true" rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="CompanyName">  
        <s:datatype dt:type="string" dt:maxLength="40" />  
      </s:AttributeType>  
      <s:AttributeType name="Phone" rs:number="3" rs:nullable="true"  
        rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="Phone">  
        <s:datatype dt:type="string" dt:maxLength="24"/>  
      </s:AttributeType>  
      <s:extends type="rs:rowbase"/>  
    </s:ElementType>  
  </s:Schema>  
 
  <rs:data>  
    <z:row ShipperID="1" CompanyName="Speedy Express"  
      Phone="(503) 555-9831"/>  
    <z:row ShipperID="2" CompanyName="United Package"  
      Phone="(503) 555-3199"/>  
    <z:row ShipperID="3" CompanyName="Federal Shipping"  
      Phone="(503) 555-9931"/>  
  </rs:data>  
</xml> 
```

Das Schema zeigt die Deklarationen von Namespaces, den Schemaabschnitt und den Datenabschnitt. Der Schemaabschnitt enthält Definitionen für Row, ShipperID, CompanyName und Phone.

Schemadefinitionen entsprechen der Spezifikation für die XML-Daten und können vollständig überprüft werden (obwohl Überprüfung in Internet Explorer 5 nicht ausgeführt wird). Sie können diese Spezifikation [W3C XMLData Hinweis](https://www.w3.org/TR/1998/NOTE-XML-data-0105/)anzeigen. XML-Daten sind derzeit das einzige unterstützte Schemaformat für Permanenz von **Recordsets** .

Der Datenabschnitt weist drei Zeilen mit Informationen zu Lieferanten. Für ein leeres Rowset kann der Datenabschnitt möglicherweise leer ist, aber die `<rs:data>` Tags müssen vorhanden sein. Ohne Daten könnten Sie einfach als das Tag die Kurzform schreiben `<rs:data>`. Jedes Tag mit dem Präfix "Rs" gibt an, dass es in den Namespace definiert durch Urn: Schemas-Microsoft-Com:rowset. Die vollständige Definition dieses Schemas ist im Anhang zu diesem Dokument definiert.

## <a name="xml-persistence-format"></a>XML-Speicherformat

ADO verwendet die UTF-8-Codierung für den gespeicherten XML-Datenstrom.

Das ADO-XML-Format ist in zwei Abschnitte unterteilt, nämlich einen Schemaabschnitt, gefolgt vom Datenabschnitt. Es folgt eine XML-Beispieldatei für die Shippers-Tabelle aus der Northwind-Datenbank. Verschiedene XML-Komponenten werden im Anschluss an das Beispiel behandelt.

```xml
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"  
xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"  
xmlns:rs="urn:schemas-microsoft-com:rowset"  
xmlns:z="#RowsetSchema">  
  <s:Schema id="RowsetSchema">  
    <s:ElementType name="row" content="eltOnly" rs:updatable="true">  
      <s:AttributeType name="ShipperID" rs:number="1"  
        rs:basetable="shippers" rs:basecolumn="ShipperID" 
        rs:keycolumn="true">  
        <s:datatype dt:type="int" dt:maxLength="4" rs:precision="10"  
          rs:fixedlength="true" rs:maybenull="false"/>  
      </s:AttributeType>  
      <s:AttributeType name="CompanyName" rs:number="2"  
        rs:nullable="true" rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="CompanyName">  
        <s:datatype dt:type="string" dt:maxLength="40" />  
      </s:AttributeType>  
      <s:AttributeType name="Phone" rs:number="3" rs:nullable="true"  
        rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="Phone">  
        <s:datatype dt:type="string" dt:maxLength="24"/>  
      </s:AttributeType>  
      <s:extends type="rs:rowbase"/>  
    </s:ElementType>  
  </s:Schema>  
 
  <rs:data>  
    <z:row ShipperID="1" CompanyName="Speedy Express"  
      Phone="(503) 555-9831"/>  
    <z:row ShipperID="2" CompanyName="United Package"  
      Phone="(503) 555-3199"/>  
    <z:row ShipperID="3" CompanyName="Federal Shipping"  
      Phone="(503) 555-9931"/>  
  </rs:data>  
</xml> 
```

Das Schema zeigt die Deklarationen von Namespaces, den Schemaabschnitt und den Datenabschnitt. Der Schemaabschnitt enthält Definitionen für Row, ShipperID, CompanyName und Phone.

Schemadefinitionen entsprechen der Spezifikation für die XML-Daten und können vollständig überprüft werden (obwohl Überprüfung in Internet Explorer 5 nicht ausgeführt wird). Sie können diese Spezifikation [W3C XMLData Hinweis](https://www.w3.org/TR/1998/NOTE-XML-data-0105/)anzeigen. XML-Daten sind derzeit das einzige unterstützte Schemaformat für Permanenz von **Recordsets** .

Der Datenabschnitt weist drei Zeilen mit Informationen zu Lieferanten. Für ein leeres Rowset kann der Datenabschnitt möglicherweise leer ist, aber die `<rs:data>` Tags müssen vorhanden sein. Ohne Daten könnten Sie einfach als das Tag die Kurzform schreiben `<rs:data>`. Jedes Tag mit dem Präfix "Rs" gibt an, dass es in den Namespace definiert durch Urn: Schemas-Microsoft-Com:rowset. Die vollständige Definition dieses Schemas ist im Anhang zu diesem Dokument definiert.

