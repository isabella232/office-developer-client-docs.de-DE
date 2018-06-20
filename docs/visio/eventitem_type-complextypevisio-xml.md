---
title: EventItem_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f157db03-e7d0-d39f-cbde-2a22f45b40ed
ms.openlocfilehash: 7fc23d9e2a9e4567693a4979b796804b16f148e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796959"
---
# <a name="eventitemtype-complextype-visio-xml"></a><span data-ttu-id="08200-102">EventItem_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="08200-102">EventItem_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="08200-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="08200-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="08200-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="08200-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="08200-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="08200-105">**Schema file**</span></span> <br/> |<span data-ttu-id="08200-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="08200-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="08200-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="08200-107">**Extension base**</span></span> <br/> |<span data-ttu-id="08200-108">Keine</span><span class="sxs-lookup"><span data-stu-id="08200-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="08200-109">Definition</span><span class="sxs-lookup"><span data-stu-id="08200-109">Definition</span></span>

```XML
      <xs:complexType name="EventItem_Type">
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Action"
  type="xsd:unsignedShort"
     use="required"
    />
    <xs:attribute name="EventCode"
  type="xsd:unsignedShort"
     use="required"
    />
    <xs:attribute name="Enabled"
  type="xsd:boolean"
    />
    <xs:attribute name="Target"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="TargetArgs"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="08200-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="08200-110">Elements and attributes</span></span>

<span data-ttu-id="08200-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="08200-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="08200-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="08200-112">Child elements</span></span>

<span data-ttu-id="08200-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="08200-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="08200-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="08200-114">Attributes</span></span>

|<span data-ttu-id="08200-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="08200-115">**Attribute**</span></span>|<span data-ttu-id="08200-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="08200-116">**Type**</span></span>|<span data-ttu-id="08200-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="08200-117">**Required**</span></span>|<span data-ttu-id="08200-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="08200-118">**Description**</span></span>|<span data-ttu-id="08200-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="08200-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="08200-120">Aktion</span><span class="sxs-lookup"><span data-stu-id="08200-120">Action</span></span>  <br/> |<span data-ttu-id="08200-121">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="08200-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="08200-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="08200-122">required</span></span>  <br/> ||<span data-ttu-id="08200-123">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="08200-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="08200-124">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="08200-124">Enabled</span></span>  <br/> |<span data-ttu-id="08200-125">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="08200-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="08200-126">Optional</span><span class="sxs-lookup"><span data-stu-id="08200-126">optional</span></span>  <br/> ||<span data-ttu-id="08200-127">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="08200-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="08200-128">Ereigniscode</span><span class="sxs-lookup"><span data-stu-id="08200-128">EventCode</span></span>  <br/> |<span data-ttu-id="08200-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="08200-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="08200-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="08200-130">required</span></span>  <br/> ||<span data-ttu-id="08200-131">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="08200-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="08200-132">ID</span><span class="sxs-lookup"><span data-stu-id="08200-132">ID</span></span>  <br/> |<span data-ttu-id="08200-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="08200-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="08200-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="08200-134">required</span></span>  <br/> ||<span data-ttu-id="08200-135">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="08200-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="08200-136">Ziel</span><span class="sxs-lookup"><span data-stu-id="08200-136">Target</span></span>  <br/> |<span data-ttu-id="08200-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="08200-137">xsd:string</span></span>  <br/> |<span data-ttu-id="08200-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="08200-138">required</span></span>  <br/> ||<span data-ttu-id="08200-139">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="08200-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="08200-140">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="08200-140">TargetArgs</span></span>  <br/> |<span data-ttu-id="08200-141">XSD: String</span><span class="sxs-lookup"><span data-stu-id="08200-141">xsd:string</span></span>  <br/> |<span data-ttu-id="08200-142">erforderlich</span><span class="sxs-lookup"><span data-stu-id="08200-142">required</span></span>  <br/> ||<span data-ttu-id="08200-143">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="08200-143">Values of the xsd:string type.</span></span>  <br/> |
   

