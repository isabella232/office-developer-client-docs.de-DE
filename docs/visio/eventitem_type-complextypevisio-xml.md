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
# <a name="eventitem_type-complextype-visio-xml"></a><span data-ttu-id="dcfc9-102">EventItem_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="dcfc9-102">EventItem_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="dcfc9-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="dcfc9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dcfc9-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="dcfc9-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="dcfc9-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="dcfc9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="dcfc9-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="dcfc9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="dcfc9-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="dcfc9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="dcfc9-108">Keine</span><span class="sxs-lookup"><span data-stu-id="dcfc9-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dcfc9-109">Definition</span><span class="sxs-lookup"><span data-stu-id="dcfc9-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="dcfc9-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="dcfc9-110">Elements and attributes</span></span>

<span data-ttu-id="dcfc9-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="dcfc9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="dcfc9-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dcfc9-112">Child elements</span></span>

<span data-ttu-id="dcfc9-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="dcfc9-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dcfc9-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="dcfc9-114">Attributes</span></span>

|<span data-ttu-id="dcfc9-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="dcfc9-115">**Attribute**</span></span>|<span data-ttu-id="dcfc9-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="dcfc9-116">**Type**</span></span>|<span data-ttu-id="dcfc9-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="dcfc9-117">**Required**</span></span>|<span data-ttu-id="dcfc9-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dcfc9-118">**Description**</span></span>|<span data-ttu-id="dcfc9-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="dcfc9-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="dcfc9-120">Aktion</span><span class="sxs-lookup"><span data-stu-id="dcfc9-120">Action</span></span>  <br/> |<span data-ttu-id="dcfc9-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="dcfc9-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="dcfc9-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="dcfc9-122">required</span></span>  <br/> ||<span data-ttu-id="dcfc9-123">Werte des Typs xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="dcfc9-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="dcfc9-124">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="dcfc9-124">Enabled</span></span>  <br/> |<span data-ttu-id="dcfc9-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="dcfc9-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="dcfc9-126">Optional</span><span class="sxs-lookup"><span data-stu-id="dcfc9-126">optional</span></span>  <br/> ||<span data-ttu-id="dcfc9-127">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="dcfc9-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="dcfc9-128">EventCode</span><span class="sxs-lookup"><span data-stu-id="dcfc9-128">EventCode</span></span>  <br/> |<span data-ttu-id="dcfc9-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="dcfc9-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="dcfc9-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="dcfc9-130">required</span></span>  <br/> ||<span data-ttu-id="dcfc9-131">Werte des Typs xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="dcfc9-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="dcfc9-132">ID</span><span class="sxs-lookup"><span data-stu-id="dcfc9-132">ID</span></span>  <br/> |<span data-ttu-id="dcfc9-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="dcfc9-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="dcfc9-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="dcfc9-134">required</span></span>  <br/> ||<span data-ttu-id="dcfc9-135">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="dcfc9-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="dcfc9-136">Ziel</span><span class="sxs-lookup"><span data-stu-id="dcfc9-136">Target</span></span>  <br/> |<span data-ttu-id="dcfc9-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="dcfc9-137">xsd:string</span></span>  <br/> |<span data-ttu-id="dcfc9-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="dcfc9-138">required</span></span>  <br/> ||<span data-ttu-id="dcfc9-139">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="dcfc9-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="dcfc9-140">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="dcfc9-140">TargetArgs</span></span>  <br/> |<span data-ttu-id="dcfc9-141">xsd:string</span><span class="sxs-lookup"><span data-stu-id="dcfc9-141">xsd:string</span></span>  <br/> |<span data-ttu-id="dcfc9-142">erforderlich</span><span class="sxs-lookup"><span data-stu-id="dcfc9-142">required</span></span>  <br/> ||<span data-ttu-id="dcfc9-143">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="dcfc9-143">Values of the xsd:string type.</span></span>  <br/> |
   

