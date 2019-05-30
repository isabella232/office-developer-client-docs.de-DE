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
# <a name="connecttype-complextype-visio-xml"></a><span data-ttu-id="383ca-102">Connect_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="383ca-102">Connect_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="383ca-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="383ca-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="383ca-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="383ca-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="383ca-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="383ca-105">**Schema file**</span></span> <br/> |<span data-ttu-id="383ca-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="383ca-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="383ca-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="383ca-107">**Extension base**</span></span> <br/> |<span data-ttu-id="383ca-108">Keine</span><span class="sxs-lookup"><span data-stu-id="383ca-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="383ca-109">Definition</span><span class="sxs-lookup"><span data-stu-id="383ca-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="383ca-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="383ca-110">Elements and attributes</span></span>

<span data-ttu-id="383ca-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="383ca-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="383ca-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="383ca-112">Child elements</span></span>

<span data-ttu-id="383ca-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="383ca-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="383ca-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="383ca-114">Attributes</span></span>

|<span data-ttu-id="383ca-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="383ca-115">**Attribute**</span></span>|<span data-ttu-id="383ca-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="383ca-116">**Type**</span></span>|<span data-ttu-id="383ca-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="383ca-117">**Required**</span></span>|<span data-ttu-id="383ca-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="383ca-118">**Description**</span></span>|<span data-ttu-id="383ca-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="383ca-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="383ca-120">FromCell</span><span class="sxs-lookup"><span data-stu-id="383ca-120">FromCell</span></span>  <br/> |<span data-ttu-id="383ca-121">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="383ca-121">xsd:string</span></span>  <br/> |<span data-ttu-id="383ca-122">Optional</span><span class="sxs-lookup"><span data-stu-id="383ca-122">optional</span></span>  <br/> ||<span data-ttu-id="383ca-123">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="383ca-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="383ca-124">FromPart</span><span class="sxs-lookup"><span data-stu-id="383ca-124">FromPart</span></span>  <br/> |<span data-ttu-id="383ca-125">XSD: int</span><span class="sxs-lookup"><span data-stu-id="383ca-125">xsd:int</span></span>  <br/> |<span data-ttu-id="383ca-126">Optional</span><span class="sxs-lookup"><span data-stu-id="383ca-126">optional</span></span>  <br/> ||<span data-ttu-id="383ca-127">Werte des Typs XSD: int.</span><span class="sxs-lookup"><span data-stu-id="383ca-127">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="383ca-128">FromSheet</span><span class="sxs-lookup"><span data-stu-id="383ca-128">FromSheet</span></span>  <br/> |<span data-ttu-id="383ca-129">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="383ca-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="383ca-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="383ca-130">required</span></span>  <br/> ||<span data-ttu-id="383ca-131">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="383ca-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="383ca-132">ToCell</span><span class="sxs-lookup"><span data-stu-id="383ca-132">ToCell</span></span>  <br/> |<span data-ttu-id="383ca-133">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="383ca-133">xsd:string</span></span>  <br/> |<span data-ttu-id="383ca-134">Optional</span><span class="sxs-lookup"><span data-stu-id="383ca-134">optional</span></span>  <br/> ||<span data-ttu-id="383ca-135">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="383ca-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="383ca-136">ToPart</span><span class="sxs-lookup"><span data-stu-id="383ca-136">ToPart</span></span>  <br/> |<span data-ttu-id="383ca-137">XSD: int</span><span class="sxs-lookup"><span data-stu-id="383ca-137">xsd:int</span></span>  <br/> |<span data-ttu-id="383ca-138">Optional</span><span class="sxs-lookup"><span data-stu-id="383ca-138">optional</span></span>  <br/> ||<span data-ttu-id="383ca-139">Werte des Typs XSD: int.</span><span class="sxs-lookup"><span data-stu-id="383ca-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="383ca-140">ToSheet</span><span class="sxs-lookup"><span data-stu-id="383ca-140">ToSheet</span></span>  <br/> |<span data-ttu-id="383ca-141">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="383ca-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="383ca-142">erforderlich</span><span class="sxs-lookup"><span data-stu-id="383ca-142">required</span></span>  <br/> ||<span data-ttu-id="383ca-143">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="383ca-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

