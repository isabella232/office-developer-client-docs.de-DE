---
title: XML-Speicherformat
TOCTitle: XML Persistence Format
ms:assetid: 499f335c-ee1f-c803-e3a8-034b8decf1ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249226(v=office.15)
ms:contentKeyID: 48544643
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 291a75fb88690a5674d872f2adb01b683f5e99bd
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946713"
---
# <a name="xml-persistence-format"></a><span data-ttu-id="4d797-102">XML-Speicherformat</span><span class="sxs-lookup"><span data-stu-id="4d797-102">XML persistence format</span></span>

<span data-ttu-id="4d797-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4d797-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="xml-persistence-format"></a><span data-ttu-id="4d797-104">XML-Speicherformat</span><span class="sxs-lookup"><span data-stu-id="4d797-104">XML Persistence Format</span></span>

<span data-ttu-id="4d797-105">ADO verwendet die UTF-8-Codierung für den gespeicherten XML-Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="4d797-105">ADO uses UTF-8 encoding for the XML stream it persists.</span></span>

<span data-ttu-id="4d797-p101">Das ADO-XML-Format ist in zwei Abschnitte unterteilt, nämlich einen Schemaabschnitt, gefolgt vom Datenabschnitt. Es folgt eine XML-Beispieldatei für die Shippers-Tabelle aus der Northwind-Datenbank. Verschiedene XML-Komponenten werden im Anschluss an das Beispiel behandelt.</span><span class="sxs-lookup"><span data-stu-id="4d797-p101">The ADO XML format is broken into two sections, a schema section followed by the data section. The following is an example XML file for the Shippers table from the Northwind database. Various parts of the XML are discussed following the example.</span></span>

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

<span data-ttu-id="4d797-p102">Das Schema zeigt die Deklarationen von Namespaces, den Schemaabschnitt und den Datenabschnitt. Der Schemaabschnitt enthält Definitionen für Row, ShipperID, CompanyName und Phone.</span><span class="sxs-lookup"><span data-stu-id="4d797-p102">The schema shows the declarations of namespaces, the schema section, and the data section. The schema section contains definitions for row, ShipperID, CompanyName, and Phone.</span></span>

<span data-ttu-id="4d797-111">Schemadefinitionen entsprechen der Spezifikation für die XML-Daten und können vollständig überprüft werden (obwohl Überprüfung in Internet Explorer 5 nicht ausgeführt wird).</span><span class="sxs-lookup"><span data-stu-id="4d797-111">Schema definitions conform to the XML-Data specification and are able to be fully validated (though validation will not occur in Internet Explorer 5).</span></span> <span data-ttu-id="4d797-112">Sie können diese Spezifikation [W3C XMLData Hinweis](https://www.w3.org/TR/1998/NOTE-XML-data-0105/)anzeigen.</span><span class="sxs-lookup"><span data-stu-id="4d797-112">You can view this specification at [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).</span></span> <span data-ttu-id="4d797-113">XML-Daten sind derzeit das einzige unterstützte Schemaformat für Permanenz von **Recordsets** .</span><span class="sxs-lookup"><span data-stu-id="4d797-113">XML-Data is the only supported schema format for **Recordset** persistence currently.</span></span>

<span data-ttu-id="4d797-114">Der Datenabschnitt weist drei Zeilen mit Informationen zu Lieferanten.</span><span class="sxs-lookup"><span data-stu-id="4d797-114">The data section has three rows containing information about shippers.</span></span> <span data-ttu-id="4d797-115">Für ein leeres Rowset kann der Datenabschnitt möglicherweise leer ist, aber die `<rs:data>` Tags müssen vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="4d797-115">For an empty rowset, the data section may be empty, but the `<rs:data>` tags must be present.</span></span> <span data-ttu-id="4d797-116">Ohne Daten könnten Sie einfach als das Tag die Kurzform schreiben `<rs:data>`.</span><span class="sxs-lookup"><span data-stu-id="4d797-116">With no data, you could write the tag shorthand as simply `<rs:data>`.</span></span> <span data-ttu-id="4d797-117">Jedes Tag mit dem Präfix "Rs" gibt an, dass es in den Namespace definiert durch Urn: Schemas-Microsoft-Com:rowset.</span><span class="sxs-lookup"><span data-stu-id="4d797-117">Any tag prefixed with "rs" indicates that it is in the namespace defined by urn:schemas-microsoft-com:rowset.</span></span> <span data-ttu-id="4d797-118">Die vollständige Definition dieses Schemas ist im Anhang zu diesem Dokument definiert.</span><span class="sxs-lookup"><span data-stu-id="4d797-118">The full definition of this schema is defined in the appendix to this document.</span></span>

## <a name="xml-persistence-format"></a><span data-ttu-id="4d797-119">XML-Speicherformat</span><span class="sxs-lookup"><span data-stu-id="4d797-119">XML Persistence Format</span></span>

<span data-ttu-id="4d797-120">ADO verwendet die UTF-8-Codierung für den gespeicherten XML-Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="4d797-120">ADO uses UTF-8 encoding for the XML stream it persists.</span></span>

<span data-ttu-id="4d797-p105">Das ADO-XML-Format ist in zwei Abschnitte unterteilt, nämlich einen Schemaabschnitt, gefolgt vom Datenabschnitt. Es folgt eine XML-Beispieldatei für die Shippers-Tabelle aus der Northwind-Datenbank. Verschiedene XML-Komponenten werden im Anschluss an das Beispiel behandelt.</span><span class="sxs-lookup"><span data-stu-id="4d797-p105">The ADO XML format is broken into two sections, a schema section followed by the data section. The following is an example XML file for the Shippers table from the Northwind database. Various parts of the XML are discussed following the example.</span></span>

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

<span data-ttu-id="4d797-p106">Das Schema zeigt die Deklarationen von Namespaces, den Schemaabschnitt und den Datenabschnitt. Der Schemaabschnitt enthält Definitionen für Row, ShipperID, CompanyName und Phone.</span><span class="sxs-lookup"><span data-stu-id="4d797-p106">The schema shows the declarations of namespaces, the schema section, and the data section. The schema section contains definitions for row, ShipperID, CompanyName, and Phone.</span></span>

<span data-ttu-id="4d797-126">Schemadefinitionen entsprechen der Spezifikation für die XML-Daten und können vollständig überprüft werden (obwohl Überprüfung in Internet Explorer 5 nicht ausgeführt wird).</span><span class="sxs-lookup"><span data-stu-id="4d797-126">Schema definitions conform to the XML-Data specification and are able to be fully validated (though validation will not occur in Internet Explorer 5).</span></span> <span data-ttu-id="4d797-127">Sie können diese Spezifikation [W3C XMLData Hinweis](https://www.w3.org/TR/1998/NOTE-XML-data-0105/)anzeigen.</span><span class="sxs-lookup"><span data-stu-id="4d797-127">You can view this specification at [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).</span></span> <span data-ttu-id="4d797-128">XML-Daten sind derzeit das einzige unterstützte Schemaformat für Permanenz von **Recordsets** .</span><span class="sxs-lookup"><span data-stu-id="4d797-128">XML-Data is the only supported schema format for **Recordset** persistence currently.</span></span>

<span data-ttu-id="4d797-129">Der Datenabschnitt weist drei Zeilen mit Informationen zu Lieferanten.</span><span class="sxs-lookup"><span data-stu-id="4d797-129">The data section has three rows containing information about shippers.</span></span> <span data-ttu-id="4d797-130">Für ein leeres Rowset kann der Datenabschnitt möglicherweise leer ist, aber die `<rs:data>` Tags müssen vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="4d797-130">For an empty rowset, the data section may be empty, but the `<rs:data>` tags must be present.</span></span> <span data-ttu-id="4d797-131">Ohne Daten könnten Sie einfach als das Tag die Kurzform schreiben `<rs:data>`.</span><span class="sxs-lookup"><span data-stu-id="4d797-131">With no data, you could write the tag shorthand as simply `<rs:data>`.</span></span> <span data-ttu-id="4d797-132">Jedes Tag mit dem Präfix "Rs" gibt an, dass es in den Namespace definiert durch Urn: Schemas-Microsoft-Com:rowset.</span><span class="sxs-lookup"><span data-stu-id="4d797-132">Any tag prefixed with "rs" indicates that it is in the namespace defined by urn:schemas-microsoft-com:rowset.</span></span> <span data-ttu-id="4d797-133">Die vollständige Definition dieses Schemas ist im Anhang zu diesem Dokument definiert.</span><span class="sxs-lookup"><span data-stu-id="4d797-133">The full definition of this schema is defined in the appendix to this document.</span></span>

