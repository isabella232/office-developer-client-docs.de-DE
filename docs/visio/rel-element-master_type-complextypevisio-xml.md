---
title: Rel-Element (Master_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 151cdd13-d00b-249c-7ebd-1ae9c4042b03
description: Gibt eine Beziehung zu einem Webpart mit der entsprechenden Master-XML-Datei an.
ms.openlocfilehash: 82552eeab746d9675f6175b62c34cef4a9c3c418
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320006"
---
# <a name="rel-element-mastertype-complextype-visio-xml"></a><span data-ttu-id="4ebc4-103">Rel-Element (Master_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="4ebc4-103">Rel element (Master_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="4ebc4-104">Gibt eine Beziehung zu einem Webpart mit der entsprechenden Master-XML-Datei an.</span><span class="sxs-lookup"><span data-stu-id="4ebc4-104">Specifies a relationship to a part with the corresponding master XML.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4ebc4-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4ebc4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ebc4-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="4ebc4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4ebc4-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="4ebc4-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4ebc4-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4ebc4-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4ebc4-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="4ebc4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4ebc4-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="4ebc4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4ebc4-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="4ebc4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4ebc4-112">Pages. XML, Masters. XML, Recordsets. XML, Page #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="4ebc4-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4ebc4-113">Definition</span><span class="sxs-lookup"><span data-stu-id="4ebc4-113">Definition</span></span>

```XML
< xs:element name="Rel"  type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4ebc4-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="4ebc4-114">Elements and attributes</span></span>

<span data-ttu-id="4ebc4-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="4ebc4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4ebc4-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4ebc4-116">Parent elements</span></span>

|<span data-ttu-id="4ebc4-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="4ebc4-117">**Element**</span></span>|<span data-ttu-id="4ebc4-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4ebc4-118">**Type**</span></span>|<span data-ttu-id="4ebc4-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4ebc4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4ebc4-120">Master</span><span class="sxs-lookup"><span data-stu-id="4ebc4-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4ebc4-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="4ebc4-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4ebc4-122">Gibt eine Instanz von Master-XML an, die in der Zeichnung gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="4ebc4-122">Specifies one instance of master XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4ebc4-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4ebc4-123">Child elements</span></span>

<span data-ttu-id="4ebc4-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="4ebc4-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4ebc4-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="4ebc4-125">Attributes</span></span>

|<span data-ttu-id="4ebc4-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4ebc4-126">**Attribute**</span></span>|<span data-ttu-id="4ebc4-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4ebc4-127">**Type**</span></span>|<span data-ttu-id="4ebc4-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="4ebc4-128">**Required**</span></span>|<span data-ttu-id="4ebc4-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4ebc4-129">**Description**</span></span>|<span data-ttu-id="4ebc4-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="4ebc4-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4ebc4-131">r:ID</span><span class="sxs-lookup"><span data-stu-id="4ebc4-131">r:id</span></span>  <br/> |<span data-ttu-id="4ebc4-132">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4ebc4-132">xsd:string</span></span>  <br/> <span data-ttu-id="4ebc4-133">Weitere Informationen finden Sie in der "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="4ebc4-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="4ebc4-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="4ebc4-134">required</span></span>  <br/> |<span data-ttu-id="4ebc4-135">Gibt eine Beziehung zu einem Webpart an.</span><span class="sxs-lookup"><span data-stu-id="4ebc4-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="4ebc4-136">"rId #"</span><span class="sxs-lookup"><span data-stu-id="4ebc4-136">"rId#"</span></span>  <br/> <span data-ttu-id="4ebc4-137">Weitere Informationen finden Sie in der "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="4ebc4-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ebc4-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ebc4-138">Remarks</span></span>

<span data-ttu-id="4ebc4-139">Der Wert des **r:ID** -Attributs muss ein **ST_RelationshipID** -Typ sein.</span><span class="sxs-lookup"><span data-stu-id="4ebc4-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="4ebc4-140">Der **ST_RelationshipID** -Typ ist eine Zeichenfolge, die das Format "rId #" aufweisen muss, wobei das letzte Zeichen eine Zahl sein muss.</span><span class="sxs-lookup"><span data-stu-id="4ebc4-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="4ebc4-141">Die Zahl muss unter allen nebengeordneten Elementen des **rel** -Elements eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="4ebc4-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="4ebc4-142">Weitere Informationen zum ST_RelationshipID-Typ finden Sie in der [Spezifikation ISO/IEC 29500, Abschnitt 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="4ebc4-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

