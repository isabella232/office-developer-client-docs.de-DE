---
title: Hierarchische Recordset-Objekte in XML
TOCTitle: Hierarchical Recordsets in XML
ms:assetid: 606dee87-8762-6cc2-a151-94d34031b35f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249351(v=office.15)
ms:contentKeyID: 48545181
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f608cd8ed36b621847c58dd523cfa052c5f501a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475034"
---
# <a name="hierarchical-recordsets-in-xml"></a>Hierarchische Recordset-Objekte in XML


**Betrifft**: Access 2013 | Office 2013

## <a name="hierarchical-recordsets-in-xml"></a>Hierarchische Recordset-Objekte in XML

ADO ermöglicht das Speichern von hierarchischen **Recordset** -Objekten in XML. Bei hierarchischen **Recordset** -Objekten ist der Wert eines Felds im übergeordneten **Recordset** -Objekt ein weiteres **Recordset** -Objekt. Solche Felder werden nicht als Attribut, sondern als untergeordnete Elemente im XML-Datenstrom dargestellt. Das folgende Beispiel veranschaulicht diesen Fall:

```vb 
 
Rs.Open "SHAPE {select stor_id, stor_name, state from stores} APPEND ({select stor_id, ord_num, ord_date, qty from sales} AS rsSales RELATE stor_id TO stor_id)", "Provider=MSDataShape;DSN=pubs;UID=MyUserId;PWD=MyPassword;" 
```

Dies ist das XML-Format des gespeicherten **Recordset** -Objekts:

```xml 
 
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"     xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"     xmlns:rs="urn:schemas-microsoft-com:rowset"  
    xmlns:z="#RowsetSchema">  
  <s:Schema id="RowsetSchema">  
    <s:ElementType name="row" content="eltOnly" rs:updatable="true">  
      <s:AttributeType name="stor_id" rs:number="1"  
        rs:writeunknown="true">  
        <s:datatype dt:type="string" dt:maxLength="4"  
          rs:fixedlength="true" rs:maybenull="false"/>  
      </s:AttributeType>  
      <s:AttributeType name="stor_name" rs:number="2" rs:nullable="true"  
        rs:writeunknown="true">  
          <s:datatype dt:type="string" dt:maxLength="40"/>  
      </s:AttributeType>  
      <s:AttributeType name="state" rs:number="3" rs:nullable="true"  
        rs:writeunknown="true">  
        <s:datatype dt:type="string" dt:maxLength="2"  
          rs:fixedlength="true"/>  
      </s:AttributeType>  
      <s:ElementType name="rsSales" content="eltOnly"  
        rs:updatable="true" rs:relation="010000000100000000000000">  
        <s:AttributeType name="stor_id" rs:number="1"  
          rs:writeunknown="true">  
          <s:datatype dt:type="string" dt:maxLength="4"  
            rs:fixedlength="true" rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:AttributeType name="ord_num" rs:number="2"  
          rs:writeunknown="true">  
          <s:datatype dt:type="string" dt:maxLength="20"  
            rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:AttributeType name="ord_date" rs:number="3"  
          rs:writeunknown="true">  
            <s:datatype dt:type="dateTime" dt:maxLength="16"  
              rs:scale="3" rs:precision="23" rs:fixedlength="true"  
              rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:AttributeType name="qty" rs:number="4" rs:writeunknown="true">  
          <s:datatype dt:type="i2" dt:maxLength="2" rs:precision="5"  
            rs:fixedlength="true" rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:extends type="rs:rowbase"/>  
      </s:ElementType>  
      <s:extends type="rs:rowbase"/>  
    </s:ElementType>  
  </s:Schema>  
  <rs:data>  
    <z:row stor_id="6380" stor_name="Eric the Read Books" state="WA">  
      <rsSales stor_id="6380" ord_num="6871"  
        ord_date="1994-09-14T00:00:00" qty="5"/>  
      <rsSales stor_id="6380" ord_num="722a"  
        ord_date="1994-09-13T00:00:00" qty="3"/>  
    </z:row>  
    <z:row stor_id="7066" stor_name="Barnum's" state="CA">  
      <rsSales stor_id="7066" ord_num="A2976"  
        ord_date="1993-05-24T00:00:00" qty="50"/>  
      <rsSales stor_id="7066" ord_num="QA7442.3"  
        ord_date="1994-09-13T00:00:00" qty="75"/>  
    </z:row>  
    <z:row stor_id="7067" stor_name="News & Brews" state="CA">  
      <rsSales stor_id="7067" ord_num="D4482"  
        ord_date="1994-09-14T00:00:00" qty="10"/>  
      <rsSales stor_id="7067" ord_num="P2121"  
        ord_date="1992-06-15T00:00:00" qty="40"/>  
      <rsSales stor_id="7067" ord_num="P2121"  
        ord_date="1992-06-15T00:00:00" qty="20"/>  
      <rsSales stor_id="7067" ord_num="P2121"  
        ord_date="1992-06-15T00:00:00" qty="20"/>  
    </z:row>  
... 
  </rs:data>  
</xml>  
```

Die genaue Reihenfolge der Spalten im übergeordneten **Recordset** -Objekt ist nicht offensichtlich, wenn es auf diese Weise gespeichert wird. Jedes Feld im übergeordneten Element kann ein untergeordnetes **Recordset** -Objekt enthalten. Der Anbieter für Persistenz speichert alle Skalarspalten zuerst als Attribute und speichert dann alle "Spalten" des untergeordneten **Recordset** -Objekts als untergeordnete Elemente der übergeordneten Zeile. Die Position des Felds im übergeordneten **Recordset** -Objekt kann durch Anzeigen der Schemadefinition des **Recordset** -Objekts abgerufen werden. Für jedes Feld ist eine OLE DB-Eigenschaft, nämlich **rs:number**, im Schemanamespace des **Recordset** -Objekts definiert, die die Ordnungszahl für dieses Feld enthält.

Die Namen aller Felder im untergeordneten **Recordset** -Objekt sind mit dem Namen des Felds im übergeordneten **Recordset** -Objekt verkettet, das dieses untergeordnete Element enthält. Dadurch wird sichergestellt, dass keine Namenskonflikte auftreten, wenn das übergeordnete und das untergeordnete **Recordset** -Objekt ein Feld enthält, das von zwei verschiedenen Tabellen stammt, aber gleich benannt ist.

Beim Speichern hierarchischer **Recordset** -Objekte in XML sollten Sie die folgenden Einschränkungen in ADO beachten:

  - Ein hierarchisches **Recordset** -Objekt mit ausstehenden Aktualisierungen kann nicht in XML gespeichert werden.

  - Ein hierarchisches **Recordset** -Objekt, das mit einem parametrisierten SHAPE-Befehl erstellt wurde, kann nicht gespeichert werden (weder im XML- noch im ADTG-Format).

  - ADO speichert derzeit die Beziehung zwischen dem übergeordneten und untergeordneten **Recordset** -Objekt als BLOB (Binary Large Object). XML-Tags zur Beschreibung dieser Beziehung wurden noch nicht im Rowsetschemanamespace definiert.

  - Wenn ein hierarchisches **Recordset** -Objekt gespeichert wird, werden auch alle untergeordneten **Recordset** -Objekte gespeichert. Falls das aktuelle **Recordset** -Objekt ein untergeordnetes Element eines anderen **Recordset** -Objekts ist, wird das übergeordnete Element nicht gespeichert. Alle untergeordneten **Recordset** -Objekte, die die Unterstruktur des aktuellen **Recordset** -Objekts darstellen, werden gespeichert.

Wenn ein hierarchisches **Recordset** -Objekt im gespeicherten XML-Format erneut geöffnet wird, müssen Sie folgende Einschränkungen beachten:

  - Wenn der untergeordnete Datensatz Datensätze enthält, für die es keine entsprechenden übergeordneten Datensätze gibt, werden diese Zeilen nicht in der XML-Darstellung des hierarchischen **Recordset** -Objekts ausgegeben. Diese Zeilen gehen demnach verloren, wenn das **Recordset** -Objekt im Speicherort erneut geöffnet wird.

  - Wenn ein untergeordneter Datensatz Verweise auf mehrere übergeordnete Datensätze aufweist, kann beim erneuten Öffnen des **Recordset** -Objekts das untergeordnete **Recordset** -Objekt doppelte Datensätze enthalten. Diese Duplikate werden jedoch nur angezeigt, wenn der Benutzer direkt mit dem zugrunde liegenden untergeordneten Rowset arbeitet. Falls ein Kapitel zum Navigieren des untergeordneten **Recordset** -Objekts verwendet wird (dies ist die einzige Navigationsmöglichkeit in ADO), werden die Duplikate nicht angezeigt.

