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
# <a name="schema-section"></a><span data-ttu-id="a8cb6-102">Schemaabschnitt</span><span class="sxs-lookup"><span data-stu-id="a8cb6-102">Schema section</span></span>

<span data-ttu-id="a8cb6-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a8cb6-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="schema-section"></a><span data-ttu-id="a8cb6-104">Schemaabschnitt</span><span class="sxs-lookup"><span data-stu-id="a8cb6-104">Schema Section</span></span>

<span data-ttu-id="a8cb6-p101">Der Schemaabschnitt ist erforderlich. Wie im vorherigen Beispiel gezeigt, gibt ADO ausführliche Metadaten zu jeder Spalte aus, um die Semantik der Datenwerte beim Aktualisieren so weit wie möglich zu erhalten. Zum Laden im XML-Format benötigt ADO jedoch nur die Namen der Spalten und das zugehörige Rowset. Es folgt ein Beispiel für ein minimales Schema:</span><span class="sxs-lookup"><span data-stu-id="a8cb6-p101">The schema section is required. As the previous example shows, ADO writes out detailed metadata about each column to preserve the semantics of the data values as much as possible for updating. However, to load in the XML, ADO only requires the names of the columns and the rowset to which they belong. Here is an example of a minimal schema:</span></span>

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

<span data-ttu-id="a8cb6-109">Im obigen Beispiel behandelt ADO die Daten als Zeichenfolgen mit variabler Länge, weil im Schema keine Typinformationen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="a8cb6-109">In the case above, ADO will treat the data as variable length strings because no type information is included in the schema.</span></span>

## <a name="creating-aliases-for-column-names"></a><span data-ttu-id="a8cb6-110">Erstellen von Aliasen für Spaltennamen</span><span class="sxs-lookup"><span data-stu-id="a8cb6-110">Creating Aliases for Column Names</span></span>

<span data-ttu-id="a8cb6-p102">Mit dem rs:name-Attribut können Sie einen Alias für einen Spaltennamen erstellen, damit ein aussagekräftiger Name in den Spalteninformationen angezeigt wird, die vom Rowset verfügbar gemacht werden, und ein kürzerer Name im Datenabschnitt verwendet werden kann. Beispielsweise könnte das obige Schema geändert werden, indem wie folgt ShipperID zu s1, CompanyName zu s2 und Phone zu s3 zugeordnet wird:</span><span class="sxs-lookup"><span data-stu-id="a8cb6-p102">The **rs:name** attribute allows you to create an alias for a column name so that a friendly name may appear in the column information exposed by the rowset and a shorter name may be used in the data section. For example, the schema above could be modified to map ShipperID to s1, CompanyName to s2, and Phone to s3 as follows:</span></span>

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

<span data-ttu-id="a8cb6-113">Anschließend würde im Datenabschnitt die Zeile mithilfe des **name**-Attributs (nicht **rs:name**) auf diese Spalte verweisen:</span><span class="sxs-lookup"><span data-stu-id="a8cb6-113">Then, in the data section, the row would use the **name** attribute (not **rs:name**) to refer to that column:</span></span>

```xml 
 
"<row s1="1" s2="Speedy Express" s3="(503) 555-9831"/> 
```

<span data-ttu-id="a8cb6-p103">Das Erstellen von Aliasen für Spaltennamen ist erforderlich, wenn ein Spaltenname im XML-Format kein zulässiger Attribut- oder Tagname ist. Beispielsweise ist für Last Name ein Alias erforderlich, weil Namen mit eingebetteten Leerzeichen unzulässige Attribute sind. Die folgende Zeile wird vom XML-Parser nicht ordnungsgemäß verarbeitet, deshalb müssen Sie einen Alias mit einem anderen Namen ohne eingebettetes Leerzeichen erstellen:</span><span class="sxs-lookup"><span data-stu-id="a8cb6-p103">Creating aliases for column names is required whenever a column name is not a legal attribute or tag name in XML. For example, "Last Name" must have an alias because names with embedded spaces are illegal attributes. The following line won't be correctly handled by the XML parser, so you must create an alias to some other name that does not have an embedded space:</span></span>

```xml 
 
<row last name="Jones"/> 
```

<span data-ttu-id="a8cb6-p104">Der für das name-Attribut verwendete Wert muss an jeder Stelle, an der im Schema- und Datenabschnitt des XML-Dokuments auf die Spalte verwiesen wird, einheitlich verwendet werden. Das folgende Beispiel veranschaulicht die einheitliche Verwendung von s1:</span><span class="sxs-lookup"><span data-stu-id="a8cb6-p104">Whatever value you use for the **name** attribute must be used consistently in each place that the column is referenced in both the schema and data sections of the XML document. The following example shows the consistent use of s1:</span></span>

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

<span data-ttu-id="a8cb6-119">Entsprechend muss CompanyName im gesamten Dokument einheitlich verwendet werden, weil dafür kein Alias definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a8cb6-119">Similarly, because there is no alias defined for CompanyName above, CompanyName must be used consistently throughout the document.</span></span>

## <a name="data-types"></a><span data-ttu-id="a8cb6-120">Datentypen</span><span class="sxs-lookup"><span data-stu-id="a8cb6-120">Data Types</span></span>

<span data-ttu-id="a8cb6-p105">Mit dem **dt:type** -Attribut können Sie einen Datentyp auf eine Spalte anwenden. Es gibt zwei Möglichkeiten, um einen Datentyp anzugeben: Geben Sie entweder das **dt:type** -Attribut direkt in der Spaltendefinition selbst an, oder verwenden Sie das **s:datatype** -Attribut als geschachteltes Element der Spaltendefinition. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="a8cb6-p105">You can apply a data type to a column with the **dt:type** attribute. You can specify a data type in two ways: either specify the **dt:type** attribute directly on the column definition itself or use the **s:datatype** construct as a nested element of the column definition. For example,</span></span>

```xml 
 
<s:AttributeType name="Phone" > 
  <s:datatype dt:type="string"/> 
</s:AttributeType> 
```

<span data-ttu-id="a8cb6-124">ist gleichbedeutend mit</span><span class="sxs-lookup"><span data-stu-id="a8cb6-124">is equivalent to</span></span>

```xml 
 
<s:AttributeType name="Phone" dt:type="string"/> 
```

<span data-ttu-id="a8cb6-125">Wenn Sie das **dt:type** -Attribut in der Zeilendefinition vollständig auslassen, hat die Spalte standardmäßig eine Zeichenfolge mit variabler Länge als Datentyp.</span><span class="sxs-lookup"><span data-stu-id="a8cb6-125">If you omit the **dt:type** attribute entirely from the row definition, by default, the column's type will be a variable length string.</span></span>

<span data-ttu-id="a8cb6-p106">Wenn mehr Typinformationen als nur der Typname vorhanden sind (z. B. **dt:maxLength**), wird die Lesbarkeit der Daten mithilfe des untergeordneten Elements **s:datatype** erhöht. Dies ist jedoch lediglich eine Konvention, kein Muss.</span><span class="sxs-lookup"><span data-stu-id="a8cb6-p106">If you have more type information than simply the type name (for example, **dt:maxLength**), it makes it more readable to use the **s:datatype** child element. This is merely a convention, however, and not a requirement.</span></span>

<span data-ttu-id="a8cb6-128">Die folgenden Beispiele zeigen, wie Sie Typinformationen in das Schema einschließen:</span><span class="sxs-lookup"><span data-stu-id="a8cb6-128">The following examples show further how to include type information in your schema:</span></span>

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

<span data-ttu-id="a8cb6-129">Verwendet das **Rs: Fixedlength** -Attribut im zweiten Beispiel ist vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a8cb6-129">There is a subtle use of the **rs:fixedlength** attribute in the second example.</span></span> <span data-ttu-id="a8cb6-130">Legen Sie eine Spalte mit dem **Rs: Fixedlength** -Attribut auf true gibt an, denen die Daten im Schema definierte Länge aufweisen müssen.</span><span class="sxs-lookup"><span data-stu-id="a8cb6-130">A column with the **rs:fixedlength** attribute set to true means that the data must have the length defined in the schema.</span></span> <span data-ttu-id="a8cb6-131">In diesem Fall ein rechtlichen Wert für Titel\_Id lautet "123456," wie gesehen "123".</span><span class="sxs-lookup"><span data-stu-id="a8cb6-131">In this case, a legal value for title\_id is "123456," as is "123 ."</span></span> <span data-ttu-id="a8cb6-132">"123" würde jedoch nicht gültig sein, da die Länge 3, nicht 6 ist.</span><span class="sxs-lookup"><span data-stu-id="a8cb6-132">However, "123" would not be valid because its length is 3, not 6.</span></span> <span data-ttu-id="a8cb6-133">Finden Sie unter der OLE DB Programmer's Guide für eine ausführlichere Beschreibung der Eigenschaft **Fixedlength** abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="a8cb6-133">See the OLE DB Programmer's Guide for a more complete description of the **fixedlength** property.</span></span>

## <a name="handling-nulls"></a><span data-ttu-id="a8cb6-134">Behandeln von NULL-Werten</span><span class="sxs-lookup"><span data-stu-id="a8cb6-134">Handling Nulls</span></span>

<span data-ttu-id="a8cb6-p108">NULL-Werte werden vom rs:maybenull-Attribut behandelt. Falls dieses Attribut auf True festgelegt wird, können die Spalteninhalte einen NULL-Wert enthalten. Wenn darüber hinaus die Spalte nicht in einer Datenzeile gefunden wird, erhält der Benutzer, der die Daten vom Rowset zurückliest, einen NULL-Status von IRowset::GetData(). Betrachten Sie die folgenden Spaltendefinitionen aus der Shippers-Tabelle:</span><span class="sxs-lookup"><span data-stu-id="a8cb6-p108">Null values are handled by the **rs:maybenull** attribute. If this attribute is set to true, the contents of the column may contain a null value. Furthermore, if the column is not found in a row of data, the user reading the data back from the rowset will get a null status from **IRowset::GetData()**. Consider the following column definitions from the Shippers table:</span></span>

```xml 
 
<s:AttributeType name="ShipperID"> 
  <s:datatype dt:type="int" dt:maxLength="4"/> 
</s:AttributeType> 
<s:AttributeType name="CompanyName"> 
  <s:datatype dt:type="string" dt:maxLength="40" rs:maybenull="true"/> 
</s:AttributeType> 
```

<span data-ttu-id="a8cb6-139">Die Definition ermöglicht CompanyName null sein darf keine ShipperID einen null-Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="a8cb6-139">The definition allows CompanyName to be null, but ShipperID cannot contain a null value.</span></span> <span data-ttu-id="a8cb6-140">Wenn Datenabschnitt die folgende Zeile enthalten, würde der Anbieter für Persistenz den Status der Daten für die Spalte CompanyName legen Sie auf der OLE DB-Status-Konstante DBSTATUS\_S\_ISNULL:</span><span class="sxs-lookup"><span data-stu-id="a8cb6-140">If the data section contained the following row, the Persistence Provider would set the status of the data for the CompanyName column to the OLE DB status constant DBSTATUS\_S\_ISNULL:</span></span>

```xml 
 
<z:row ShipperID="1"/> 
```

<span data-ttu-id="a8cb6-141">Wenn die Zeile wie folgt vollständig leer war, würde der Anbieter für Persistenz OLE DB-Status des DBSTATUS zurückgeben\_E\_nicht verfügbar für ShipperID und DBSTATUS\_S\_ISNULL für CompanyName.</span><span class="sxs-lookup"><span data-stu-id="a8cb6-141">If the row was entirely empty, as follows, the Persistence Provider would return an OLE DB status of DBSTATUS\_E\_UNAVAILABLE for ShipperID and DBSTATUS\_S\_ISNULL for CompanyName.</span></span>

```xml 
 
<z:row/>  
```

<span data-ttu-id="a8cb6-142">Beachten Sie, dass eine leere Zeichenfolge nicht mit NULL identisch ist.</span><span class="sxs-lookup"><span data-stu-id="a8cb6-142">Note that a zero-length string is not the same as null.</span></span>

```xml 
 
<z:row ShipperID="1" CompanyName=""/> 
```

<span data-ttu-id="a8cb6-143">Für die vorhergehende Zeile gibt der Anbieter für Persistenz OLE DB-Status des DBSTATUS zurück\_S\_OK für beide Spalten.</span><span class="sxs-lookup"><span data-stu-id="a8cb6-143">For the preceding row, the Persistence Provider will return an OLE DB status of DBSTATUS\_S\_OK for both columns.</span></span> <span data-ttu-id="a8cb6-144">CompanyName ist in diesem Fall einfach "" (leere Zeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="a8cb6-144">The CompanyName in this case is simply "" (a zero-length string).</span></span>

<span data-ttu-id="a8cb6-145">Weitere Informationen zur OLE DB-Syntax, die im Schema eines XML-Dokuments für OLE DB verwendet werden kann, finden Sie in der Definition zu urn:schemas-microsoft-com:rowset und im OLE DB Programmer's Guide.</span><span class="sxs-lookup"><span data-stu-id="a8cb6-145">For further information about the OLE DB constructs available for use within the schema of an XML document for OLE DB, see the definition of "urn:schemas-microsoft-com:rowset" and the OLE DB Programmer's Guide.</span></span>

