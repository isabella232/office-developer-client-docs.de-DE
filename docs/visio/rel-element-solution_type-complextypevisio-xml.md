---
title: Rel-Element (Solution_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8438fe4b-f5f7-d4e4-58b7-7ebdc1da197a
description: Gibt eine Beziehung mit einem Webpart mit der Lösung, die diese Lösung XML zugeordnet.
ms.openlocfilehash: 59d9db3f7e0897abf278a27229c07fd3942cee79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797796"
---
# <a name="rel-element-solutiontype-complextype-visio-xml"></a><span data-ttu-id="d4f8b-103">Rel-Element (Solution_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="d4f8b-103">Rel element (Solution_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="d4f8b-104">Gibt eine Beziehung mit einem Webpart mit der Lösung, die diese Lösung XML zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d4f8b-104">Specifies a relationship to a part with the solution XML associated with this solution.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d4f8b-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d4f8b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d4f8b-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="d4f8b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d4f8b-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="d4f8b-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d4f8b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d4f8b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d4f8b-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="d4f8b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d4f8b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d4f8b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d4f8b-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="d4f8b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d4f8b-112">Pages.XML, masters.xml, recordsets.xml, Seite # .xml, Master-Shape # .xml</span><span class="sxs-lookup"><span data-stu-id="d4f8b-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d4f8b-113">Definition</span><span class="sxs-lookup"><span data-stu-id="d4f8b-113">Definition</span></span>

```XML
<xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d4f8b-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="d4f8b-114">Elements and attributes</span></span>

<span data-ttu-id="d4f8b-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="d4f8b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d4f8b-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d4f8b-116">Parent elements</span></span>

|<span data-ttu-id="d4f8b-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="d4f8b-117">**Element**</span></span>|<span data-ttu-id="d4f8b-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d4f8b-118">**Type**</span></span>|<span data-ttu-id="d4f8b-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d4f8b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d4f8b-120">Solution</span><span class="sxs-lookup"><span data-stu-id="d4f8b-120">Solution</span></span>](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d4f8b-121">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="d4f8b-121">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d4f8b-122">Gibt eine Instanz der Lösung, die in der Zeichnung XML gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d4f8b-122">Specifies one instance of solution XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d4f8b-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d4f8b-123">Child elements</span></span>

<span data-ttu-id="d4f8b-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="d4f8b-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d4f8b-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="d4f8b-125">Attributes</span></span>

|<span data-ttu-id="d4f8b-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d4f8b-126">**Attribute**</span></span>|<span data-ttu-id="d4f8b-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d4f8b-127">**Type**</span></span>|<span data-ttu-id="d4f8b-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d4f8b-128">**Required**</span></span>|<span data-ttu-id="d4f8b-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d4f8b-129">**Description**</span></span>|<span data-ttu-id="d4f8b-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="d4f8b-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d4f8b-131">R-Id:</span><span class="sxs-lookup"><span data-stu-id="d4f8b-131">r:id</span></span>  <br/> |<span data-ttu-id="d4f8b-132">XSD: String</span><span class="sxs-lookup"><span data-stu-id="d4f8b-132">xsd:string</span></span>  <br/> <span data-ttu-id="d4f8b-133">Weitere Informationen finden Sie in der "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="d4f8b-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="d4f8b-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d4f8b-134">required</span></span>  <br/> |<span data-ttu-id="d4f8b-135">Gibt eine Beziehung mit einem Webpart an.</span><span class="sxs-lookup"><span data-stu-id="d4f8b-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="d4f8b-136">"befassen #"</span><span class="sxs-lookup"><span data-stu-id="d4f8b-136">"rId#"</span></span>  <br/> <span data-ttu-id="d4f8b-137">Weitere Informationen finden Sie in der "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="d4f8b-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4f8b-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4f8b-138">Remarks</span></span>

<span data-ttu-id="d4f8b-139">Der Wert des **R: Id** -Attributs muss vom Typ **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="d4f8b-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="d4f8b-140">Der Typ **ST_RelationshipID** ist eine Zeichenfolge, die im Format sein muss "entfernen #", wobei muss das letzte Zeichen eine Zahl sein.</span><span class="sxs-lookup"><span data-stu-id="d4f8b-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="d4f8b-141">Die Nummer muss unter allen gleichgeordneten Elementen des Elements **Rel** eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="d4f8b-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="d4f8b-142">Weitere Informationen zu den Typ ST_RelationshipID finden Sie in der [Spezifikation ISO/IEC 29500 Teil 1](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="d4f8b-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

