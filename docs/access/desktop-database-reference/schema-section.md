---
title: Schemaabschnitt (Access PC-Datenbank-Referenz)
TOCTitle: Schema Section
ms:assetid: 59b42ffb-0524-adc3-8bcd-6e4cd2c505ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249304(v=office.15)
ms:contentKeyID: 48545023
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 00a5c08784d1a57e148acbaa6f1621102d6b6712
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947756"
---
# <a name="schema-section"></a>Schemaabschnitt

**Betrifft**: Access 2013, Office 2013

## <a name="schema-section"></a>Schemaabschnitt

Der Schemaabschnitt ist erforderlich. Wie im vorherigen Beispiel gezeigt, gibt ADO ausführliche Metadaten zu jeder Spalte aus, um die Semantik der Datenwerte beim Aktualisieren so weit wie möglich zu erhalten. Zum Laden im XML-Format benötigt ADO jedoch nur die Namen der Spalten und das zugehörige Rowset. Es folgt ein Beispiel für ein minimales Schema:

```xml 
 
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882" 
    xmlns:rs="urn:schemas-microsoft-com:rowset" 
    xmlns:z="#RowsetSchema"> 
  <s:Schema id="RowsetSchema"> 
    <s:ElementType name="row" content="eltOnly"> 
      <s:AttributeType name="ShipperID"/> 
      <s:AttributeType name="CompanyName"/> 
      <s:AttributeType name="Phone"/> 
      <s:Extends type="rs:rowbase"/> 
    </s:ElementType> 
  </s:Schema> 
  <rs:data> 
... 
  </rs:data> 
</xml> 
```

Im obigen Beispiel behandelt ADO die Daten als Zeichenfolgen mit variabler Länge, weil im Schema keine Typinformationen enthalten sind.

## <a name="creating-aliases-for-column-names"></a>Erstellen von Aliasen für Spaltennamen

Mit dem rs:name-Attribut können Sie einen Alias für einen Spaltennamen erstellen, damit ein aussagekräftiger Name in den Spalteninformationen angezeigt wird, die vom Rowset verfügbar gemacht werden, und ein kürzerer Name im Datenabschnitt verwendet werden kann. Beispielsweise könnte das obige Schema geändert werden, indem wie folgt ShipperID zu s1, CompanyName zu s2 und Phone zu s3 zugeordnet wird:

```xml 
 
<s:Schema id="RowsetSchema">  
<s:ElementType name="row" content="eltOnly" rs:updatable="true">  
<s:AttributeType name="s1" rs:name="ShipperID" rs:number="1" ...>  
... 
</s:AttributeType>  
<s:AttributeType name="s2" rs:name="CompanyName" rs:number="2" ...>  
... 
</s:AttributeType>  
<s:AttributeType name="s3" rs:name="Phone" rs:number="3" ...>  
... 
</s:AttributeType>  
... 
</s:ElementType>  
</s:Schema>  
```

Anschließend würde im Datenabschnitt die Zeile mithilfe des **name**-Attributs (nicht **rs:name**) auf diese Spalte verweisen:

```xml 
 
"<row s1="1" s2="Speedy Express" s3="(503) 555-9831"/> 
```

Das Erstellen von Aliasen für Spaltennamen ist erforderlich, wenn ein Spaltenname im XML-Format kein zulässiger Attribut- oder Tagname ist. Beispielsweise ist für Last Name ein Alias erforderlich, weil Namen mit eingebetteten Leerzeichen unzulässige Attribute sind. Die folgende Zeile wird vom XML-Parser nicht ordnungsgemäß verarbeitet, deshalb müssen Sie einen Alias mit einem anderen Namen ohne eingebettetes Leerzeichen erstellen:

```xml 
 
<row last name="Jones"/> 
```

Der für das name-Attribut verwendete Wert muss an jeder Stelle, an der im Schema- und Datenabschnitt des XML-Dokuments auf die Spalte verwiesen wird, einheitlich verwendet werden. Das folgende Beispiel veranschaulicht die einheitliche Verwendung von s1:

```xml 
 
<s:Schema id="RowsetSchema"> 
  <s:ElementType name="row" content="eltOnly"> 
    <s:attribute type="s1"/> 
    <s:attribute type="CompanyName"/> 
    <s:attribute type="s3"/> 
    <s:extends type="rs:rowbase"/> 
  </s:ElementType> 
  <s:AttributeType name="s1" rs:name="ShipperID" rs:number="1"  
    rs:maydefer="true" rs:writeunknown="true"> 
    <s:datatype dt:type="i4" dt:maxLength="4" rs:precision="10"  
      rs:fixedlength="true" rs:maybenull="true"/> 
  </s:AttributeType> 
</s:Schema> 
<rs:data> 
  <z:row s1="1" CompanyName="Speedy Express" s3="(503) 555-9831"/> 
</rs:data> 
```

Entsprechend muss CompanyName im gesamten Dokument einheitlich verwendet werden, weil dafür kein Alias definiert ist.

## <a name="data-types"></a>Datentypen

Mit dem **dt:type** -Attribut können Sie einen Datentyp auf eine Spalte anwenden. Es gibt zwei Möglichkeiten, um einen Datentyp anzugeben: Geben Sie entweder das **dt:type** -Attribut direkt in der Spaltendefinition selbst an, oder verwenden Sie das **s:datatype** -Attribut als geschachteltes Element der Spaltendefinition. Beispiel:

```xml 
 
<s:AttributeType name="Phone" > 
  <s:datatype dt:type="string"/> 
</s:AttributeType> 
```

ist gleichbedeutend mit

```xml 
 
<s:AttributeType name="Phone" dt:type="string"/> 
```

Wenn Sie das **dt:type** -Attribut in der Zeilendefinition vollständig auslassen, hat die Spalte standardmäßig eine Zeichenfolge mit variabler Länge als Datentyp.

Wenn mehr Typinformationen als nur der Typname vorhanden sind (z. B. **dt:maxLength**), wird die Lesbarkeit der Daten mithilfe des untergeordneten Elements **s:datatype** erhöht. Dies ist jedoch lediglich eine Konvention, kein Muss.

Die folgenden Beispiele zeigen, wie Sie Typinformationen in das Schema einschließen:

```xml 
 
<!-- 1. String with no max length --> 
<s:AttributeType name="title_id"/> 
<! — or --> 
<s:AttributeType name="title_id" dt:type="string"/> 
 
<! — 2. Fixed length string with max length of 6 --> 
<s:AttributeType name="title_id"> 
    <s:datatype dt:type="string" dt:maxLength="6" rs:fixedlength="true" /> 
</s:AttributeType> 
 
<! — 3. Variable length string with max length of 6 --> 
<s:AttributeType name="title_id"> 
    <s:datatype dt:type="string" dt:maxLength="6" /> 
</s:AttributeType> 
 
<! — 4. Integer --> 
<s:AttributeType name="title_id" dt:type="int"/> 
```

Verwendet das **Rs: Fixedlength** -Attribut im zweiten Beispiel ist vorhanden. Legen Sie eine Spalte mit dem **Rs: Fixedlength** -Attribut auf true gibt an, denen die Daten im Schema definierte Länge aufweisen müssen. In diesem Fall ein rechtlichen Wert für Titel\_Id lautet "123456," wie gesehen "123". "123" würde jedoch nicht gültig sein, da die Länge 3, nicht 6 ist. Finden Sie unter der OLE DB Programmer's Guide für eine ausführlichere Beschreibung der Eigenschaft **Fixedlength** abzuschließen.

## <a name="handling-nulls"></a>Behandeln von NULL-Werten

NULL-Werte werden vom rs:maybenull-Attribut behandelt. Falls dieses Attribut auf True festgelegt wird, können die Spalteninhalte einen NULL-Wert enthalten. Wenn darüber hinaus die Spalte nicht in einer Datenzeile gefunden wird, erhält der Benutzer, der die Daten vom Rowset zurückliest, einen NULL-Status von IRowset::GetData(). Betrachten Sie die folgenden Spaltendefinitionen aus der Shippers-Tabelle:

```xml 
 
<s:AttributeType name="ShipperID"> 
  <s:datatype dt:type="int" dt:maxLength="4"/> 
</s:AttributeType> 
<s:AttributeType name="CompanyName"> 
  <s:datatype dt:type="string" dt:maxLength="40" rs:maybenull="true"/> 
</s:AttributeType> 
```

Die Definition ermöglicht CompanyName null sein darf keine ShipperID einen null-Wert enthalten. Wenn Datenabschnitt die folgende Zeile enthalten, würde der Anbieter für Persistenz den Status der Daten für die Spalte CompanyName legen Sie auf der OLE DB-Status-Konstante DBSTATUS\_S\_ISNULL:

```xml 
 
<z:row ShipperID="1"/> 
```

Wenn die Zeile wie folgt vollständig leer war, würde der Anbieter für Persistenz OLE DB-Status des DBSTATUS zurückgeben\_E\_nicht verfügbar für ShipperID und DBSTATUS\_S\_ISNULL für CompanyName.

```xml 
 
<z:row/>  
```

Beachten Sie, dass eine leere Zeichenfolge nicht mit NULL identisch ist.

```xml 
 
<z:row ShipperID="1" CompanyName=""/> 
```

Für die vorhergehende Zeile gibt der Anbieter für Persistenz OLE DB-Status des DBSTATUS zurück\_S\_OK für beide Spalten. CompanyName ist in diesem Fall einfach "" (leere Zeichenfolge).

Weitere Informationen zur OLE DB-Syntax, die im Schema eines XML-Dokuments für OLE DB verwendet werden kann, finden Sie in der Definition zu urn:schemas-microsoft-com:rowset und im OLE DB Programmer's Guide.

