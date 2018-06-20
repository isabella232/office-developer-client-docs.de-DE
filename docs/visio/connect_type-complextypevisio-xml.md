---
title: Connect_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2230976b-f2a8-425b-b8b0-a7fd5efb4536
ms.openlocfilehash: 9a321a3ff910afb183e1a697eaad9dfb51125524
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796703"
---
# <a name="connecttype-complextype-visio-xml"></a><span data-ttu-id="1e0c5-102">Connect_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="1e0c5-102">Connect_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1e0c5-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="1e0c5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1e0c5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1e0c5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1e0c5-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="1e0c5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1e0c5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1e0c5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1e0c5-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="1e0c5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1e0c5-108">Keine</span><span class="sxs-lookup"><span data-stu-id="1e0c5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1e0c5-109">Definition</span><span class="sxs-lookup"><span data-stu-id="1e0c5-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1e0c5-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="1e0c5-110">Elements and attributes</span></span>

<span data-ttu-id="1e0c5-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="1e0c5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1e0c5-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1e0c5-112">Child elements</span></span>

<span data-ttu-id="1e0c5-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="1e0c5-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1e0c5-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="1e0c5-114">Attributes</span></span>

|<span data-ttu-id="1e0c5-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1e0c5-115">**Attribute**</span></span>|<span data-ttu-id="1e0c5-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1e0c5-116">**Type**</span></span>|<span data-ttu-id="1e0c5-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="1e0c5-117">**Required**</span></span>|<span data-ttu-id="1e0c5-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1e0c5-118">**Description**</span></span>|<span data-ttu-id="1e0c5-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="1e0c5-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1e0c5-120">FromCell</span><span class="sxs-lookup"><span data-stu-id="1e0c5-120">FromCell</span></span>  <br/> |<span data-ttu-id="1e0c5-121">XSD: String</span><span class="sxs-lookup"><span data-stu-id="1e0c5-121">xsd:string</span></span>  <br/> |<span data-ttu-id="1e0c5-122">Optional</span><span class="sxs-lookup"><span data-stu-id="1e0c5-122">optional</span></span>  <br/> ||<span data-ttu-id="1e0c5-123">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="1e0c5-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1e0c5-124">FromPart</span><span class="sxs-lookup"><span data-stu-id="1e0c5-124">FromPart</span></span>  <br/> |<span data-ttu-id="1e0c5-125">XSD: int</span><span class="sxs-lookup"><span data-stu-id="1e0c5-125">xsd:int</span></span>  <br/> |<span data-ttu-id="1e0c5-126">Optional</span><span class="sxs-lookup"><span data-stu-id="1e0c5-126">optional</span></span>  <br/> ||<span data-ttu-id="1e0c5-127">Werte des Typs xsd: int.</span><span class="sxs-lookup"><span data-stu-id="1e0c5-127">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="1e0c5-128">FromSheet</span><span class="sxs-lookup"><span data-stu-id="1e0c5-128">FromSheet</span></span>  <br/> |<span data-ttu-id="1e0c5-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1e0c5-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1e0c5-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="1e0c5-130">required</span></span>  <br/> ||<span data-ttu-id="1e0c5-131">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1e0c5-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1e0c5-132">ToCell</span><span class="sxs-lookup"><span data-stu-id="1e0c5-132">ToCell</span></span>  <br/> |<span data-ttu-id="1e0c5-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="1e0c5-133">xsd:string</span></span>  <br/> |<span data-ttu-id="1e0c5-134">Optional</span><span class="sxs-lookup"><span data-stu-id="1e0c5-134">optional</span></span>  <br/> ||<span data-ttu-id="1e0c5-135">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="1e0c5-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1e0c5-136">ToPart</span><span class="sxs-lookup"><span data-stu-id="1e0c5-136">ToPart</span></span>  <br/> |<span data-ttu-id="1e0c5-137">XSD: int</span><span class="sxs-lookup"><span data-stu-id="1e0c5-137">xsd:int</span></span>  <br/> |<span data-ttu-id="1e0c5-138">Optional</span><span class="sxs-lookup"><span data-stu-id="1e0c5-138">optional</span></span>  <br/> ||<span data-ttu-id="1e0c5-139">Werte des Typs xsd: int.</span><span class="sxs-lookup"><span data-stu-id="1e0c5-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="1e0c5-140">ToSheet</span><span class="sxs-lookup"><span data-stu-id="1e0c5-140">ToSheet</span></span>  <br/> |<span data-ttu-id="1e0c5-141">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1e0c5-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1e0c5-142">erforderlich</span><span class="sxs-lookup"><span data-stu-id="1e0c5-142">required</span></span>  <br/> ||<span data-ttu-id="1e0c5-143">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1e0c5-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

