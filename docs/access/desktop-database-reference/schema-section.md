---
title: Schemaabschnitt (Access-Desktopdatenbankreferenz)
TOCTitle: Schema Section
ms:assetid: 59b42ffb-0524-adc3-8bcd-6e4cd2c505ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249304(v=office.15)
ms:contentKeyID: 48545023
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a92d778bcad1f2c58bfc2997f6ac112cc9f6049d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572746"
---
# <a name="schema-section"></a>Schema-Abschnitt

**Gilt für**: Access 2013, Office 2013

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

The **rs:name** attribute allows you to create an alias for a column name so that a friendly name may appear in the column information exposed by the rowset and a shorter name may be used in the data section. For example, the schema above could be modified to map ShipperID to s1, CompanyName to s2, and Phone to s3 as follows:

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

Creating aliases for column names is required whenever a column name is not a legal attribute or tag name in XML. For example, "Last Name" must have an alias because names with embedded spaces are illegal attributes. The following line won't be correctly handled by the XML parser, so you must create an alias to some other name that does not have an embedded space:

```xml 
 
<row last name="Jones"/> 
```

Whatever value you use for the **name** attribute must be used consistently in each place that the column is referenced in both the schema and data sections of the XML document. The following example shows the consistent use of s1:

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

Wenn Sie das **dt:type**-Attribut in der Zeilendefinition vollständig auslassen, hat die Spalte standardmäßig eine Zeichenfolge mit variabler Länge als Datentyp.

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

Im zweiten Beispiel wird das attribut **rs:fixedlength** dezent verwendet. Eine Spalte mit dem Attribut **"rs:fixedlength"** auf "true" bedeutet, dass für die Daten die Länge im Schema definiert sein muss. In diesem Fall lautet ein rechtlicher Wert für die \_ Titel-ID "123456", ebenso wie "123". "123" wäre jedoch ungültig, da die Länge 3 und nicht 6 ist. Eine ausführlichere Beschreibung der **FixedLength-Eigenschaft** finden Sie im OLE DB-Programmierhandbuch.

## <a name="handling-nulls"></a>Behandeln von NULL-Werten

Null values are handled by the **rs:maybenull** attribute. If this attribute is set to true, the contents of the column may contain a null value. Furthermore, if the column is not found in a row of data, the user reading the data back from the rowset will get a null status from **IRowset::GetData()**. Consider the following column definitions from the Shippers table:

```xml 
 
<s:AttributeType name="ShipperID"> 
  <s:datatype dt:type="int" dt:maxLength="4"/> 
</s:AttributeType> 
<s:AttributeType name="CompanyName"> 
  <s:datatype dt:type="string" dt:maxLength="40" rs:maybenull="true"/> 
</s:AttributeType> 
```

The definition allows CompanyName to be null, but ShipperID cannot contain a null value. Wenn der Datenabschnitt die folgende Zeile enthält, würde der Persistenzanbieter den Status der Daten für die Spalte "CompanyName" auf die OLE DB-Statuskonstante DBSTATUS \_ S \_ ISNULL festlegen:

```xml 
 
<z:row ShipperID="1"/> 
```

Wenn die Zeile wie folgt vollständig leer wäre, würde der Persistenzanbieter den OLE DB-Status DBSTATUS \_ E \_ UNAVAILABLE für ShipperID und DBSTATUS \_ S \_ ISNULL für CompanyName zurückgeben.

```xml 
 
<z:row/>  
```

Beachten Sie, dass eine leere Zeichenfolge nicht mit NULL identisch ist.

```xml 
 
<z:row ShipperID="1" CompanyName=""/> 
```

Für die vorherige Zeile gibt der Persistenzanbieter den OLE DB-Status DBSTATUS \_ S OK für beide Spalten \_ zurück. The CompanyName in this case is simply "" (a zero-length string).

For further information about the OLE DB constructs available for use within the schema of an XML document for OLE DB, see the definition of "urn:schemas-microsoft-com:rowset" and the OLE DB Programmer's Guide.

