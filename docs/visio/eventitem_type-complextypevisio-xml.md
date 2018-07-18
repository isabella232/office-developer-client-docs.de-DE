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
# <a name="eventitemtype-complextype-visio-xml"></a><span data-ttu-id="3fcf5-102">EventItem_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="3fcf5-102">EventItem_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="3fcf5-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="3fcf5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3fcf5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3fcf5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3fcf5-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="3fcf5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3fcf5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3fcf5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3fcf5-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="3fcf5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3fcf5-108">Keine</span><span class="sxs-lookup"><span data-stu-id="3fcf5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3fcf5-109">Definition</span><span class="sxs-lookup"><span data-stu-id="3fcf5-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="3fcf5-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="3fcf5-110">Elements and attributes</span></span>

<span data-ttu-id="3fcf5-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="3fcf5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3fcf5-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3fcf5-112">Child elements</span></span>

<span data-ttu-id="3fcf5-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="3fcf5-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3fcf5-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="3fcf5-114">Attributes</span></span>

|<span data-ttu-id="3fcf5-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="3fcf5-115">**Attribute**</span></span>|<span data-ttu-id="3fcf5-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="3fcf5-116">**Type**</span></span>|<span data-ttu-id="3fcf5-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="3fcf5-117">**Required**</span></span>|<span data-ttu-id="3fcf5-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3fcf5-118">**Description**</span></span>|<span data-ttu-id="3fcf5-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="3fcf5-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3fcf5-120">Aktion</span><span class="sxs-lookup"><span data-stu-id="3fcf5-120">Action</span></span>  <br/> |<span data-ttu-id="3fcf5-121">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="3fcf5-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="3fcf5-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="3fcf5-122">required</span></span>  <br/> ||<span data-ttu-id="3fcf5-123">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="3fcf5-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="3fcf5-124">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="3fcf5-124">Enabled</span></span>  <br/> |<span data-ttu-id="3fcf5-125">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="3fcf5-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="3fcf5-126">Optional</span><span class="sxs-lookup"><span data-stu-id="3fcf5-126">optional</span></span>  <br/> ||<span data-ttu-id="3fcf5-127">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="3fcf5-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="3fcf5-128">Ereigniscode</span><span class="sxs-lookup"><span data-stu-id="3fcf5-128">EventCode</span></span>  <br/> |<span data-ttu-id="3fcf5-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="3fcf5-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="3fcf5-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="3fcf5-130">required</span></span>  <br/> ||<span data-ttu-id="3fcf5-131">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="3fcf5-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="3fcf5-132">ID</span><span class="sxs-lookup"><span data-stu-id="3fcf5-132">ID</span></span>  <br/> |<span data-ttu-id="3fcf5-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3fcf5-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3fcf5-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="3fcf5-134">required</span></span>  <br/> ||<span data-ttu-id="3fcf5-135">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3fcf5-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3fcf5-136">Ziel</span><span class="sxs-lookup"><span data-stu-id="3fcf5-136">Target</span></span>  <br/> |<span data-ttu-id="3fcf5-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="3fcf5-137">xsd:string</span></span>  <br/> |<span data-ttu-id="3fcf5-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="3fcf5-138">required</span></span>  <br/> ||<span data-ttu-id="3fcf5-139">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="3fcf5-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3fcf5-140">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="3fcf5-140">TargetArgs</span></span>  <br/> |<span data-ttu-id="3fcf5-141">XSD: String</span><span class="sxs-lookup"><span data-stu-id="3fcf5-141">xsd:string</span></span>  <br/> |<span data-ttu-id="3fcf5-142">erforderlich</span><span class="sxs-lookup"><span data-stu-id="3fcf5-142">required</span></span>  <br/> ||<span data-ttu-id="3fcf5-143">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="3fcf5-143">Values of the xsd:string type.</span></span>  <br/> |
   

