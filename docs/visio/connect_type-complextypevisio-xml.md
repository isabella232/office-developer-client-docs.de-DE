---
title: Connect_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2230976b-f2a8-425b-b8b0-a7fd5efb4536
ms.openlocfilehash: 158fad1f3ec18bbc9565229338f4710c145c17e7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327083"
---
# <a name="connecttype-complextype-visio-xml"></a><span data-ttu-id="b74ed-102">Connect_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="b74ed-102">Connect_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b74ed-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="b74ed-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b74ed-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b74ed-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b74ed-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="b74ed-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b74ed-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="b74ed-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b74ed-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="b74ed-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b74ed-108">Keine</span><span class="sxs-lookup"><span data-stu-id="b74ed-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b74ed-109">Definition</span><span class="sxs-lookup"><span data-stu-id="b74ed-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="b74ed-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="b74ed-110">Elements and attributes</span></span>

<span data-ttu-id="b74ed-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="b74ed-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b74ed-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b74ed-112">Child elements</span></span>

<span data-ttu-id="b74ed-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="b74ed-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b74ed-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="b74ed-114">Attributes</span></span>

|<span data-ttu-id="b74ed-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b74ed-115">**Attribute**</span></span>|<span data-ttu-id="b74ed-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="b74ed-116">**Type**</span></span>|<span data-ttu-id="b74ed-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="b74ed-117">**Required**</span></span>|<span data-ttu-id="b74ed-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b74ed-118">**Description**</span></span>|<span data-ttu-id="b74ed-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="b74ed-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b74ed-120">FromCell</span><span class="sxs-lookup"><span data-stu-id="b74ed-120">FromCell</span></span>  <br/> |<span data-ttu-id="b74ed-121">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b74ed-121">xsd:string</span></span>  <br/> |<span data-ttu-id="b74ed-122">Optional</span><span class="sxs-lookup"><span data-stu-id="b74ed-122">optional</span></span>  <br/> ||<span data-ttu-id="b74ed-123">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="b74ed-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b74ed-124">FromPart</span><span class="sxs-lookup"><span data-stu-id="b74ed-124">FromPart</span></span>  <br/> |<span data-ttu-id="b74ed-125">XSD: int</span><span class="sxs-lookup"><span data-stu-id="b74ed-125">xsd:int</span></span>  <br/> |<span data-ttu-id="b74ed-126">Optional</span><span class="sxs-lookup"><span data-stu-id="b74ed-126">optional</span></span>  <br/> ||<span data-ttu-id="b74ed-127">Werte des XSD: int-Typs.</span><span class="sxs-lookup"><span data-stu-id="b74ed-127">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="b74ed-128">FromSheet</span><span class="sxs-lookup"><span data-stu-id="b74ed-128">FromSheet</span></span>  <br/> |<span data-ttu-id="b74ed-129">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b74ed-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b74ed-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="b74ed-130">required</span></span>  <br/> ||<span data-ttu-id="b74ed-131">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="b74ed-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b74ed-132">ToCell</span><span class="sxs-lookup"><span data-stu-id="b74ed-132">ToCell</span></span>  <br/> |<span data-ttu-id="b74ed-133">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b74ed-133">xsd:string</span></span>  <br/> |<span data-ttu-id="b74ed-134">Optional</span><span class="sxs-lookup"><span data-stu-id="b74ed-134">optional</span></span>  <br/> ||<span data-ttu-id="b74ed-135">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="b74ed-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b74ed-136">ToPart</span><span class="sxs-lookup"><span data-stu-id="b74ed-136">ToPart</span></span>  <br/> |<span data-ttu-id="b74ed-137">XSD: int</span><span class="sxs-lookup"><span data-stu-id="b74ed-137">xsd:int</span></span>  <br/> |<span data-ttu-id="b74ed-138">Optional</span><span class="sxs-lookup"><span data-stu-id="b74ed-138">optional</span></span>  <br/> ||<span data-ttu-id="b74ed-139">Werte des XSD: int-Typs.</span><span class="sxs-lookup"><span data-stu-id="b74ed-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="b74ed-140">ToSheet</span><span class="sxs-lookup"><span data-stu-id="b74ed-140">ToSheet</span></span>  <br/> |<span data-ttu-id="b74ed-141">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b74ed-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b74ed-142">erforderlich</span><span class="sxs-lookup"><span data-stu-id="b74ed-142">required</span></span>  <br/> ||<span data-ttu-id="b74ed-143">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="b74ed-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

