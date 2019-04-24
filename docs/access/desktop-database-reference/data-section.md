---
title: Abschnitt "Data" (Access Desktop Database Reference)
TOCTitle: Data section
ms:assetid: fd8d31aa-af13-a52f-5e91-20225b8df175
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250303(v=office.15)
ms:contentKeyID: 48548920
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1b8e3baf4d147edcc739e59933da4697c08cdef0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295044"
---
# <a name="data-section"></a><span data-ttu-id="bf7a5-102">Datenabschnitt</span><span class="sxs-lookup"><span data-stu-id="bf7a5-102">Data section</span></span>

<span data-ttu-id="bf7a5-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bf7a5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bf7a5-p101">Der Datenabschnitt definiert die Daten des Rowsets zusammen mit ausstehenden Aktualisierungen, Einfügungen oder Löschvorgängen. Der Datenabschnitt kann null oder mehr Zeilen enthalten. Er kann nur Daten von einem einzigen Rowset enthalten, in dem die Zeile vom Schema definiert wird. Außerdem können wie vorher beschrieben Spalten ohne Daten ausgelassen werden. Falls ein Attribut oder Unterelement im Datenabschnitt verwendet wird und dieses nicht im Schemaabschnitt definiert wurde, wird es ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bf7a5-p101">The data section defines the data of the rowset along with any pending updates, insertions, or deletions. The data section may contain zero or more rows. It may only contain data from one rowset where the row is defined by the schema. Also, as noted before, columns without any data may be omitted. If an attribute or subelement is used in the data section and that construct has not been defined in the schema section, it is silently ignored.</span></span>

## <a name="string"></a><span data-ttu-id="bf7a5-109">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bf7a5-109">String</span></span>

<span data-ttu-id="bf7a5-p102">Reservierte XML-Zeichen in Textdaten müssen durch entsprechende Zeichenentitäten ersetzt werden. Beispielsweise muss im Firmenname "Joe's Garage" das einfache Anführungszeichen durch eine Entität ersetzt werden. Die tatsächliche Zeile würde wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="bf7a5-p102">Reserved XML characters in text data must be replaced with appropriate character entities. For example, in the company name "Joe's Garage," the single quote character must be replaced by an entity. The actual row would look like:</span></span>

```xml  
<z:row CompanyName="Joe&apos;s Garage"/> 
```

<span data-ttu-id="bf7a5-113">Die folgenden Zeichen sind in XML reserviert und müssen durch Zeichenentitäten ersetzt werden: {', ", &,\<,\>}.</span><span class="sxs-lookup"><span data-stu-id="bf7a5-113">The following characters are reserved in XML and must be replaced by character entities: {',",&,\<,\>}.</span></span>

## <a name="binary"></a><span data-ttu-id="bf7a5-114">Binär</span><span class="sxs-lookup"><span data-stu-id="bf7a5-114">Binary</span></span>

<span data-ttu-id="bf7a5-115">Binäre Daten sind bin.hex-codiert (das heißt, einem Byte sind zwei Zeichen zugeordnet, nämlich ein Zeichen pro Nibble).</span><span class="sxs-lookup"><span data-stu-id="bf7a5-115">Binary data is bin.hex encoded (that is, one byte maps to two characters, one character per nibble).</span></span>

## <a name="datetime"></a><span data-ttu-id="bf7a5-116">DateTime</span><span class="sxs-lookup"><span data-stu-id="bf7a5-116">DateTime</span></span>

<span data-ttu-id="bf7a5-117">Das Datumsformat\_der Version VT wird nicht direkt von XML-Datentypen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bf7a5-117">The variant VT\_DATE format is not directly supported by XML-Data data types.</span></span> <span data-ttu-id="bf7a5-118">Das richtige Format für Daten mit einer Datums- und einer Zeitkomponente lautet yyyy-mm-dd**T**hh:mm:ss.</span><span class="sxs-lookup"><span data-stu-id="bf7a5-118">The correct format for dates with both a data and time component is yyyy-mm-dd**T**hh:mm:ss.</span></span>

<span data-ttu-id="bf7a5-119">Weitere Informationen zu den von XML angegebenen Datumsformaten finden Sie unter [W3C XMLDATA-Hinweis](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).</span><span class="sxs-lookup"><span data-stu-id="bf7a5-119">For more information about date formats specified by XML, see [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).</span></span>

<span data-ttu-id="bf7a5-120">Wenn die XML-Data-Spezifikation zwei äquivalente Datentypen definiert (z. B. i4 == int), schreibt ADO den Anzeigenamen vollständig, kann aber beide Formate lesen.</span><span class="sxs-lookup"><span data-stu-id="bf7a5-120">When the XML-Data specification defines two equivalent data types (for example, i4 == int), ADO will write out the friendly name but read in both.</span></span>

## <a name="managing-pending-changes"></a><span data-ttu-id="bf7a5-121">Verwalten ausstehender Änderungen</span><span class="sxs-lookup"><span data-stu-id="bf7a5-121">Managing pending changes</span></span>

<span data-ttu-id="bf7a5-p104">A **Recordset** can be opened in immediate or batch update mode. When opened in batch update mode with client-side cursors, all changes made to the **Recordset** are in a pending state until the **UpdateBatch** method is called. Pending changes are also persisted when the **Recordset** is saved. In XML, they are represented by the use of the "update" elements defined in urn:schemas-microsoft-com:rowset. In addition, if a rowset can be updated, the updatable property must be set to true in the definition of the row. For example, to define that the Shippers table contains pending changes, the row definition would look like the following:</span><span class="sxs-lookup"><span data-stu-id="bf7a5-p104">A **Recordset** can be opened in immediate or batch update mode. When opened in batch update mode with client-side cursors, all changes made to the **Recordset** are in a pending state until the **UpdateBatch** method is called. Pending changes are also persisted when the **Recordset** is saved. In XML, they are represented by the use of the "update" elements defined in urn:schemas-microsoft-com:rowset. In addition, if a rowset can be updated, the updatable property must be set to true in the definition of the row. For example, to define that the Shippers table contains pending changes, the row definition would look like the following:</span></span>

```xml 
<s:ElementType name="row" content="eltOnly" updatable="true"> 
  <s:attribute type="ShipperID"/> 
  <s:attribute type="CompanyName"/> 
  <s:attribute type="Phone"/> 
  <s:extends type="rs:rowbase"/> 
</s:ElementType> 
```

<span data-ttu-id="bf7a5-128">Hiermit wird der Anbieter für Persistenz angewiesen, Daten anzuzeigen, damit ADO ein aktualisierbares **Recordset**-Objekt erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="bf7a5-128">This tells the Persistence Provider to surface data so that ADO can construct an updatable **Recordset** object.</span></span>

<span data-ttu-id="bf7a5-129">Die folgenden Beispieldaten veranschaulichen, wie Einfügungen, Änderungen und Löschvorgänge in der gespeicherten Datei aussehen:</span><span class="sxs-lookup"><span data-stu-id="bf7a5-129">The following sample data shows how insertions, changes, and deletions look in the persisted file:</span></span>

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

<span data-ttu-id="bf7a5-p105">Eine Aktualisierung enthält immer die gesamten ursprünglichen Zeilendaten, gefolgt von den geänderten Zeilendaten. Die geänderte Zeile kann alle Spalten oder nur die tatsächlich geänderten Spalten enthalten. Im vorherigen Beispiel wird die Zeile für "Shipper 2" nicht geändert. Nur in der Phone-Spalte wurden Werte für Shipper 3 geändert. Dies ist deshalb die einzige Spalte, die in der geänderten Zeile enthalten ist. Die eingefügten Zeilen für "Shipper 12", "Shipper 13" und "Shipper 14" werden unter einem einzigen rs:insert-Tag in einem Batch verarbeitet. Beachten Sie, dass gelöschte Zeilen ebenfalls in einem Batch verarbeitet werden können, auch wenn dies im obigen Beispiel nicht dargestellt ist.</span><span class="sxs-lookup"><span data-stu-id="bf7a5-p105">An update always contains the entire original row data followed by the changed row data. The changed row may contain all of the columns or only those columns that have actually changed. In the previous example, the row for Shipper 2 is not changed, while only the Phone column has changed values for Shipper 3 and is therefore the only column included in the changed row. The inserted rows for Shippers 12, 13, and 14 are batched together under one rs:insert tag. Note that deleted rows may also be batched together, although this is not shown above.</span></span>

