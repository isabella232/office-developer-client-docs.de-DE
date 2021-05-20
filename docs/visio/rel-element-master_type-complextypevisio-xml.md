---
title: Rel-Element (Master_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 151cdd13-d00b-249c-7ebd-1ae9c4042b03
description: Gibt eine Beziehung zu einem Teil mit dem entsprechenden Master-XML an.
ms.openlocfilehash: 032c1ef4a94bb6acf18587a1257fe82285124e87
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542800"
---
# <a name="rel-element-master_type-complextype-visio-xml"></a><span data-ttu-id="3ef37-103">Rel-Element (Master_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="3ef37-103">Rel element (Master_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="3ef37-104">Gibt eine Beziehung zu einem Teil mit dem entsprechenden Master-XML an.</span><span class="sxs-lookup"><span data-stu-id="3ef37-104">Specifies a relationship to a part with the corresponding master XML.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3ef37-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="3ef37-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3ef37-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="3ef37-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3ef37-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="3ef37-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3ef37-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3ef37-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3ef37-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="3ef37-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3ef37-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="3ef37-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3ef37-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="3ef37-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3ef37-112">pages.xml, masters.xml, recordsets.xml, Seite#.xml, Master#.xml</span><span class="sxs-lookup"><span data-stu-id="3ef37-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3ef37-113">Definition</span><span class="sxs-lookup"><span data-stu-id="3ef37-113">Definition</span></span>

```XML
< xs:element name="Rel"  type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3ef37-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="3ef37-114">Elements and attributes</span></span>

<span data-ttu-id="3ef37-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="3ef37-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3ef37-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3ef37-116">Parent elements</span></span>

|<span data-ttu-id="3ef37-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="3ef37-117">**Element**</span></span>|<span data-ttu-id="3ef37-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="3ef37-118">**Type**</span></span>|<span data-ttu-id="3ef37-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3ef37-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3ef37-120">Master</span><span class="sxs-lookup"><span data-stu-id="3ef37-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3ef37-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="3ef37-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3ef37-122">Gibt eine Instanz von Master-XML an, die in der Zeichnung gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="3ef37-122">Specifies one instance of master XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3ef37-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3ef37-123">Child elements</span></span>

<span data-ttu-id="3ef37-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="3ef37-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3ef37-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="3ef37-125">Attributes</span></span>

|<span data-ttu-id="3ef37-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="3ef37-126">**Attribute**</span></span>|<span data-ttu-id="3ef37-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="3ef37-127">**Type**</span></span>|<span data-ttu-id="3ef37-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="3ef37-128">**Required**</span></span>|<span data-ttu-id="3ef37-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3ef37-129">**Description**</span></span>|<span data-ttu-id="3ef37-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="3ef37-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3ef37-131">r:id</span><span class="sxs-lookup"><span data-stu-id="3ef37-131">r:id</span></span>  <br/> |<span data-ttu-id="3ef37-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="3ef37-132">xsd:string</span></span>  <br/> <span data-ttu-id="3ef37-133">Weitere Informationen finden Sie in der "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="3ef37-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="3ef37-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="3ef37-134">required</span></span>  <br/> |<span data-ttu-id="3ef37-135">Gibt eine Beziehung zu einem Teil an.</span><span class="sxs-lookup"><span data-stu-id="3ef37-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="3ef37-136">"rId#"</span><span class="sxs-lookup"><span data-stu-id="3ef37-136">"rId#"</span></span>  <br/> <span data-ttu-id="3ef37-137">Weitere Informationen finden Sie in der "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="3ef37-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3ef37-138">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3ef37-138">Remarks</span></span>

<span data-ttu-id="3ef37-139">Der Wert des **r:id-Attributs** muss ein **ST_RelationshipID** sein.</span><span class="sxs-lookup"><span data-stu-id="3ef37-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="3ef37-140">Der **ST_RelationshipID** ist eine Zeichenfolge im Format "rId#", wobei das letzte Zeichen eine Zahl sein muss.</span><span class="sxs-lookup"><span data-stu-id="3ef37-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="3ef37-141">Die Zahl muss zwischen allen gleichgeordneten Elementen des **Rel-Elements eindeutig** sein.</span><span class="sxs-lookup"><span data-stu-id="3ef37-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="3ef37-142">Weitere Informationen zum ST_RelationshipID finden Sie in der [SPEZIFIKATION ISO/IEC 29500 Part 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="3ef37-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

