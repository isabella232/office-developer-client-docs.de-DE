---
title: Rel-Element (Master_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 151cdd13-d00b-249c-7ebd-1ae9c4042b03
description: Gibt eine Beziehung zu einem Webpart mit dem entsprechenden Master-XML-Code an.
ms.openlocfilehash: 032c1ef4a94bb6acf18587a1257fe82285124e87
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542800"
---
# <a name="rel-element-mastertype-complextype-visio-xml"></a><span data-ttu-id="c0492-103">Rel-Element (Master_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c0492-103">Rel element (Master_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="c0492-104">Gibt eine Beziehung zu einem Webpart mit dem entsprechenden Master-XML-Code an.</span><span class="sxs-lookup"><span data-stu-id="c0492-104">Specifies a relationship to a part with the corresponding master XML.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c0492-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c0492-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c0492-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="c0492-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c0492-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="c0492-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c0492-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c0492-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c0492-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="c0492-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c0492-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="c0492-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c0492-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="c0492-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c0492-112">Pages. XML, Masters. XML, Recordsets. XML, Page #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="c0492-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c0492-113">Definition</span><span class="sxs-lookup"><span data-stu-id="c0492-113">Definition</span></span>

```XML
< xs:element name="Rel"  type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c0492-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="c0492-114">Elements and attributes</span></span>

<span data-ttu-id="c0492-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="c0492-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c0492-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c0492-116">Parent elements</span></span>

|<span data-ttu-id="c0492-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="c0492-117">**Element**</span></span>|<span data-ttu-id="c0492-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c0492-118">**Type**</span></span>|<span data-ttu-id="c0492-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c0492-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c0492-120">Master</span><span class="sxs-lookup"><span data-stu-id="c0492-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c0492-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="c0492-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c0492-122">Gibt eine Instanz des in der Zeichnung gespeicherten Master-XML-Code an.</span><span class="sxs-lookup"><span data-stu-id="c0492-122">Specifies one instance of master XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c0492-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c0492-123">Child elements</span></span>

<span data-ttu-id="c0492-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="c0492-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c0492-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="c0492-125">Attributes</span></span>

|<span data-ttu-id="c0492-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c0492-126">**Attribute**</span></span>|<span data-ttu-id="c0492-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c0492-127">**Type**</span></span>|<span data-ttu-id="c0492-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="c0492-128">**Required**</span></span>|<span data-ttu-id="c0492-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c0492-129">**Description**</span></span>|<span data-ttu-id="c0492-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="c0492-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c0492-131">r:ID</span><span class="sxs-lookup"><span data-stu-id="c0492-131">r:id</span></span>  <br/> |<span data-ttu-id="c0492-132">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c0492-132">xsd:string</span></span>  <br/> <span data-ttu-id="c0492-133">Weitere Informationen finden Sie in der "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="c0492-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="c0492-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="c0492-134">required</span></span>  <br/> |<span data-ttu-id="c0492-135">Gibt eine Beziehung zu einem Webpart an.</span><span class="sxs-lookup"><span data-stu-id="c0492-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="c0492-136">"rId #"</span><span class="sxs-lookup"><span data-stu-id="c0492-136">"rId#"</span></span>  <br/> <span data-ttu-id="c0492-137">Weitere Informationen finden Sie in der "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="c0492-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0492-138">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c0492-138">Remarks</span></span>

<span data-ttu-id="c0492-139">Der Wert des **r:ID** -Attributs muss ein **ST_RelationshipID** -Typ sein.</span><span class="sxs-lookup"><span data-stu-id="c0492-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="c0492-140">Der **ST_RelationshipID** -Typ ist eine Zeichenfolge, die im Format "rId #" sein muss, wobei das letzte Zeichen eine Zahl sein muss.</span><span class="sxs-lookup"><span data-stu-id="c0492-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="c0492-141">Die Zahl muss unter allen gleichgeordneten Elementen des **rel** -Elements eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="c0492-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="c0492-142">Weitere Informationen zum ST_RelationshipID-Typ finden Sie in der [Spezifikation ISO/IEC 29500 Part 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="c0492-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

