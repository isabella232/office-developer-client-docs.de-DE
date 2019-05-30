---
title: EventItem_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f157db03-e7d0-d39f-cbde-2a22f45b40ed
ms.openlocfilehash: f0fd618cc2a86d3695d0d6f6c446f118475ffc1f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541792"
---
# <a name="eventitemtype-complextype-visio-xml"></a><span data-ttu-id="43d42-102">EventItem_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="43d42-102">EventItem_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="43d42-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="43d42-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="43d42-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="43d42-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="43d42-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="43d42-105">**Schema file**</span></span> <br/> |<span data-ttu-id="43d42-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="43d42-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="43d42-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="43d42-107">**Extension base**</span></span> <br/> |<span data-ttu-id="43d42-108">Keine</span><span class="sxs-lookup"><span data-stu-id="43d42-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="43d42-109">Definition</span><span class="sxs-lookup"><span data-stu-id="43d42-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="43d42-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="43d42-110">Elements and attributes</span></span>

<span data-ttu-id="43d42-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="43d42-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="43d42-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="43d42-112">Child elements</span></span>

<span data-ttu-id="43d42-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="43d42-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="43d42-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="43d42-114">Attributes</span></span>

|<span data-ttu-id="43d42-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="43d42-115">**Attribute**</span></span>|<span data-ttu-id="43d42-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="43d42-116">**Type**</span></span>|<span data-ttu-id="43d42-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="43d42-117">**Required**</span></span>|<span data-ttu-id="43d42-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="43d42-118">**Description**</span></span>|<span data-ttu-id="43d42-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="43d42-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="43d42-120">Aktion</span><span class="sxs-lookup"><span data-stu-id="43d42-120">Action</span></span>  <br/> |<span data-ttu-id="43d42-121">XSD: unsignedShort abgeleitet</span><span class="sxs-lookup"><span data-stu-id="43d42-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="43d42-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="43d42-122">required</span></span>  <br/> ||<span data-ttu-id="43d42-123">Werte des XSD: unsignedShort abgeleitet-Typs.</span><span class="sxs-lookup"><span data-stu-id="43d42-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="43d42-124">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="43d42-124">Enabled</span></span>  <br/> |<span data-ttu-id="43d42-125">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="43d42-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="43d42-126">Optional</span><span class="sxs-lookup"><span data-stu-id="43d42-126">optional</span></span>  <br/> ||<span data-ttu-id="43d42-127">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="43d42-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="43d42-128">EventCode</span><span class="sxs-lookup"><span data-stu-id="43d42-128">EventCode</span></span>  <br/> |<span data-ttu-id="43d42-129">XSD: unsignedShort abgeleitet</span><span class="sxs-lookup"><span data-stu-id="43d42-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="43d42-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="43d42-130">required</span></span>  <br/> ||<span data-ttu-id="43d42-131">Werte des XSD: unsignedShort abgeleitet-Typs.</span><span class="sxs-lookup"><span data-stu-id="43d42-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="43d42-132">ID</span><span class="sxs-lookup"><span data-stu-id="43d42-132">ID</span></span>  <br/> |<span data-ttu-id="43d42-133">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="43d42-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="43d42-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="43d42-134">required</span></span>  <br/> ||<span data-ttu-id="43d42-135">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="43d42-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="43d42-136">Ziel</span><span class="sxs-lookup"><span data-stu-id="43d42-136">Target</span></span>  <br/> |<span data-ttu-id="43d42-137">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="43d42-137">xsd:string</span></span>  <br/> |<span data-ttu-id="43d42-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="43d42-138">required</span></span>  <br/> ||<span data-ttu-id="43d42-139">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="43d42-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="43d42-140">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="43d42-140">TargetArgs</span></span>  <br/> |<span data-ttu-id="43d42-141">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="43d42-141">xsd:string</span></span>  <br/> |<span data-ttu-id="43d42-142">erforderlich</span><span class="sxs-lookup"><span data-stu-id="43d42-142">required</span></span>  <br/> ||<span data-ttu-id="43d42-143">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="43d42-143">Values of the xsd:string type.</span></span>  <br/> |
   

