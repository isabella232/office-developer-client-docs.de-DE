---
title: Rel-Element (Solution_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8438fe4b-f5f7-d4e4-58b7-7ebdc1da197a
description: Gibt eine Beziehung zu einem Webpart an, dessen Lösungs-XML dieser Lösung zugeordnet ist.
ms.openlocfilehash: e8a1350691e8d29551fb126a2151655175cc068c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320013"
---
# <a name="rel-element-solutiontype-complextype-visio-xml"></a><span data-ttu-id="0e13f-103">Rel-Element (Solution_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="0e13f-103">Rel element (Solution_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="0e13f-104">Gibt eine Beziehung zu einem Webpart an, dessen Lösungs-XML dieser Lösung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0e13f-104">Specifies a relationship to a part with the solution XML associated with this solution.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0e13f-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0e13f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0e13f-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="0e13f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0e13f-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="0e13f-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0e13f-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0e13f-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0e13f-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="0e13f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0e13f-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="0e13f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0e13f-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="0e13f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0e13f-112">Pages. XML, Masters. XML, Recordsets. XML, Page #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="0e13f-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0e13f-113">Definition</span><span class="sxs-lookup"><span data-stu-id="0e13f-113">Definition</span></span>

```XML
<xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0e13f-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="0e13f-114">Elements and attributes</span></span>

<span data-ttu-id="0e13f-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="0e13f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0e13f-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0e13f-116">Parent elements</span></span>

|<span data-ttu-id="0e13f-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="0e13f-117">**Element**</span></span>|<span data-ttu-id="0e13f-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="0e13f-118">**Type**</span></span>|<span data-ttu-id="0e13f-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0e13f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0e13f-120">Solution</span><span class="sxs-lookup"><span data-stu-id="0e13f-120">Solution</span></span>](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0e13f-121">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="0e13f-121">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0e13f-122">Gibt eine Instanz von Lösungs-XML an, die in der Zeichnung gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="0e13f-122">Specifies one instance of solution XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0e13f-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0e13f-123">Child elements</span></span>

<span data-ttu-id="0e13f-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="0e13f-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0e13f-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="0e13f-125">Attributes</span></span>

|<span data-ttu-id="0e13f-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0e13f-126">**Attribute**</span></span>|<span data-ttu-id="0e13f-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="0e13f-127">**Type**</span></span>|<span data-ttu-id="0e13f-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="0e13f-128">**Required**</span></span>|<span data-ttu-id="0e13f-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0e13f-129">**Description**</span></span>|<span data-ttu-id="0e13f-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="0e13f-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0e13f-131">r:ID</span><span class="sxs-lookup"><span data-stu-id="0e13f-131">r:id</span></span>  <br/> |<span data-ttu-id="0e13f-132">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0e13f-132">xsd:string</span></span>  <br/> <span data-ttu-id="0e13f-133">Weitere Informationen finden Sie in der "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="0e13f-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="0e13f-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="0e13f-134">required</span></span>  <br/> |<span data-ttu-id="0e13f-135">Gibt eine Beziehung zu einem Webpart an.</span><span class="sxs-lookup"><span data-stu-id="0e13f-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="0e13f-136">"rId #"</span><span class="sxs-lookup"><span data-stu-id="0e13f-136">"rId#"</span></span>  <br/> <span data-ttu-id="0e13f-137">Weitere Informationen finden Sie in der "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="0e13f-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e13f-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e13f-138">Remarks</span></span>

<span data-ttu-id="0e13f-139">Der Wert des **r:ID** -Attributs muss ein **ST_RelationshipID** -Typ sein.</span><span class="sxs-lookup"><span data-stu-id="0e13f-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="0e13f-140">Der **ST_RelationshipID** -Typ ist eine Zeichenfolge, die das Format "rId #" aufweisen muss, wobei das letzte Zeichen eine Zahl sein muss.</span><span class="sxs-lookup"><span data-stu-id="0e13f-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="0e13f-141">Die Zahl muss unter allen nebengeordneten Elementen des **rel** -Elements eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="0e13f-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="0e13f-142">Weitere Informationen zum ST_RelationshipID-Typ finden Sie in der [Spezifikation ISO/IEC 29500, Abschnitt 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="0e13f-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

