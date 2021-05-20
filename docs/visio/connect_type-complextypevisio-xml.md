---
title: Connect_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2230976b-f2a8-425b-b8b0-a7fd5efb4536
ms.openlocfilehash: 9dee421915cb3e69ef5223280a425e785d29e4ec
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538739"
---
# <a name="connect_type-complextype-visio-xml"></a><span data-ttu-id="b2954-102">Connect_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="b2954-102">Connect_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="b2954-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="b2954-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b2954-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b2954-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b2954-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="b2954-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b2954-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b2954-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b2954-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="b2954-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b2954-108">Keine</span><span class="sxs-lookup"><span data-stu-id="b2954-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b2954-109">Definition</span><span class="sxs-lookup"><span data-stu-id="b2954-109">Definition</span></span>

```XML
      <xs:complexType name="Connect_Type">
    <xs:attribute name="FromSheet"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="FromCell"
  type="xsd:string"
    />
    <xs:attribute name="FromPart"
  type="xsd:int"
    />
    <xs:attribute name="ToSheet"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ToCell"
  type="xsd:string"
    />
    <xs:attribute name="ToPart"
  type="xsd:int"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b2954-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="b2954-110">Elements and attributes</span></span>

<span data-ttu-id="b2954-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="b2954-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b2954-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b2954-112">Child elements</span></span>

<span data-ttu-id="b2954-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="b2954-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b2954-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="b2954-114">Attributes</span></span>

|<span data-ttu-id="b2954-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b2954-115">**Attribute**</span></span>|<span data-ttu-id="b2954-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="b2954-116">**Type**</span></span>|<span data-ttu-id="b2954-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="b2954-117">**Required**</span></span>|<span data-ttu-id="b2954-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b2954-118">**Description**</span></span>|<span data-ttu-id="b2954-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="b2954-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b2954-120">FromCell</span><span class="sxs-lookup"><span data-stu-id="b2954-120">FromCell</span></span>  <br/> |<span data-ttu-id="b2954-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b2954-121">xsd:string</span></span>  <br/> |<span data-ttu-id="b2954-122">Optional</span><span class="sxs-lookup"><span data-stu-id="b2954-122">optional</span></span>  <br/> ||<span data-ttu-id="b2954-123">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="b2954-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b2954-124">FromPart</span><span class="sxs-lookup"><span data-stu-id="b2954-124">FromPart</span></span>  <br/> |<span data-ttu-id="b2954-125">xsd:int</span><span class="sxs-lookup"><span data-stu-id="b2954-125">xsd:int</span></span>  <br/> |<span data-ttu-id="b2954-126">Optional</span><span class="sxs-lookup"><span data-stu-id="b2954-126">optional</span></span>  <br/> ||<span data-ttu-id="b2954-127">Werte des xsd:int-Typs.</span><span class="sxs-lookup"><span data-stu-id="b2954-127">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="b2954-128">FromSheet</span><span class="sxs-lookup"><span data-stu-id="b2954-128">FromSheet</span></span>  <br/> |<span data-ttu-id="b2954-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b2954-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b2954-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="b2954-130">required</span></span>  <br/> ||<span data-ttu-id="b2954-131">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="b2954-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b2954-132">ToCell</span><span class="sxs-lookup"><span data-stu-id="b2954-132">ToCell</span></span>  <br/> |<span data-ttu-id="b2954-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b2954-133">xsd:string</span></span>  <br/> |<span data-ttu-id="b2954-134">Optional</span><span class="sxs-lookup"><span data-stu-id="b2954-134">optional</span></span>  <br/> ||<span data-ttu-id="b2954-135">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="b2954-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b2954-136">ToPart</span><span class="sxs-lookup"><span data-stu-id="b2954-136">ToPart</span></span>  <br/> |<span data-ttu-id="b2954-137">xsd:int</span><span class="sxs-lookup"><span data-stu-id="b2954-137">xsd:int</span></span>  <br/> |<span data-ttu-id="b2954-138">Optional</span><span class="sxs-lookup"><span data-stu-id="b2954-138">optional</span></span>  <br/> ||<span data-ttu-id="b2954-139">Werte des xsd:int-Typs.</span><span class="sxs-lookup"><span data-stu-id="b2954-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="b2954-140">ToSheet</span><span class="sxs-lookup"><span data-stu-id="b2954-140">ToSheet</span></span>  <br/> |<span data-ttu-id="b2954-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b2954-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b2954-142">erforderlich</span><span class="sxs-lookup"><span data-stu-id="b2954-142">required</span></span>  <br/> ||<span data-ttu-id="b2954-143">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="b2954-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

