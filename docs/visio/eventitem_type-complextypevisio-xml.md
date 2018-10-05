---
title: EventItem_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f157db03-e7d0-d39f-cbde-2a22f45b40ed
ms.openlocfilehash: 77c51ab76a1d7c5c4450c429b1d3ccb8e3442f34
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395728"
---
# <a name="eventitemtype-complextype-visio-xml"></a><span data-ttu-id="8e71e-102">EventItem_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="8e71e-102">EventItem_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="8e71e-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="8e71e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8e71e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8e71e-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8e71e-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="8e71e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8e71e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="8e71e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8e71e-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="8e71e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8e71e-108">Keine</span><span class="sxs-lookup"><span data-stu-id="8e71e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8e71e-109">Definition</span><span class="sxs-lookup"><span data-stu-id="8e71e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="8e71e-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="8e71e-110">Elements and attributes</span></span>

<span data-ttu-id="8e71e-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="8e71e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8e71e-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8e71e-112">Child elements</span></span>

<span data-ttu-id="8e71e-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="8e71e-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8e71e-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="8e71e-114">Attributes</span></span>

|<span data-ttu-id="8e71e-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="8e71e-115">**Attribute**</span></span>|<span data-ttu-id="8e71e-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="8e71e-116">**Type**</span></span>|<span data-ttu-id="8e71e-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="8e71e-117">**Required**</span></span>|<span data-ttu-id="8e71e-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8e71e-118">**Description**</span></span>|<span data-ttu-id="8e71e-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="8e71e-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8e71e-120">Aktion</span><span class="sxs-lookup"><span data-stu-id="8e71e-120">Action</span></span>  <br/> |<span data-ttu-id="8e71e-121">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="8e71e-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="8e71e-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="8e71e-122">required</span></span>  <br/> ||<span data-ttu-id="8e71e-123">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="8e71e-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="8e71e-124">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="8e71e-124">Enabled</span></span>  <br/> |<span data-ttu-id="8e71e-125">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="8e71e-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8e71e-126">Optional</span><span class="sxs-lookup"><span data-stu-id="8e71e-126">optional</span></span>  <br/> ||<span data-ttu-id="8e71e-127">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="8e71e-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8e71e-128">Ereigniscode</span><span class="sxs-lookup"><span data-stu-id="8e71e-128">EventCode</span></span>  <br/> |<span data-ttu-id="8e71e-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="8e71e-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="8e71e-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="8e71e-130">required</span></span>  <br/> ||<span data-ttu-id="8e71e-131">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="8e71e-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="8e71e-132">ID</span><span class="sxs-lookup"><span data-stu-id="8e71e-132">ID</span></span>  <br/> |<span data-ttu-id="8e71e-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8e71e-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8e71e-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="8e71e-134">required</span></span>  <br/> ||<span data-ttu-id="8e71e-135">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8e71e-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8e71e-136">Ziel</span><span class="sxs-lookup"><span data-stu-id="8e71e-136">Target</span></span>  <br/> |<span data-ttu-id="8e71e-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="8e71e-137">xsd:string</span></span>  <br/> |<span data-ttu-id="8e71e-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="8e71e-138">required</span></span>  <br/> ||<span data-ttu-id="8e71e-139">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="8e71e-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8e71e-140">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="8e71e-140">TargetArgs</span></span>  <br/> |<span data-ttu-id="8e71e-141">XSD: String</span><span class="sxs-lookup"><span data-stu-id="8e71e-141">xsd:string</span></span>  <br/> |<span data-ttu-id="8e71e-142">erforderlich</span><span class="sxs-lookup"><span data-stu-id="8e71e-142">required</span></span>  <br/> ||<span data-ttu-id="8e71e-143">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="8e71e-143">Values of the xsd:string type.</span></span>  <br/> |
   

