---
title: FaceName_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: f0a136cec6d620ba7001ed0e6fae01af82c2180d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542898"
---
# <a name="facename_type-complextype-visio-xml"></a><span data-ttu-id="1a4d7-102">FaceName_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="1a4d7-102">FaceName_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="1a4d7-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="1a4d7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1a4d7-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1a4d7-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1a4d7-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="1a4d7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1a4d7-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1a4d7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1a4d7-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="1a4d7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1a4d7-108">Keine</span><span class="sxs-lookup"><span data-stu-id="1a4d7-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1a4d7-109">Definition</span><span class="sxs-lookup"><span data-stu-id="1a4d7-109">Definition</span></span>

```XML
      <xs:complexType name="FaceName_Type">
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="UnicodeRanges"
  type="xsd:string"
    />
    <xs:attribute name="CharSets"
  type="xsd:string"
    />
    <xs:attribute name="Panos"
  type="xsd:string"
    />
    <xs:attribute name="Panose"
  type="xsd:string"
    />
    <xs:attribute name="Flags"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1a4d7-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="1a4d7-110">Elements and attributes</span></span>

<span data-ttu-id="1a4d7-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1a4d7-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1a4d7-112">Child elements</span></span>

<span data-ttu-id="1a4d7-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1a4d7-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="1a4d7-114">Attributes</span></span>

|<span data-ttu-id="1a4d7-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1a4d7-115">**Attribute**</span></span>|<span data-ttu-id="1a4d7-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1a4d7-116">**Type**</span></span>|<span data-ttu-id="1a4d7-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="1a4d7-117">**Required**</span></span>|<span data-ttu-id="1a4d7-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1a4d7-118">**Description**</span></span>|<span data-ttu-id="1a4d7-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="1a4d7-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1a4d7-120">CharSets</span><span class="sxs-lookup"><span data-stu-id="1a4d7-120">CharSets</span></span>  <br/> |<span data-ttu-id="1a4d7-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1a4d7-121">xsd:string</span></span>  <br/> |<span data-ttu-id="1a4d7-122">Optional</span><span class="sxs-lookup"><span data-stu-id="1a4d7-122">optional</span></span>  <br/> ||<span data-ttu-id="1a4d7-123">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1a4d7-124">Flags</span><span class="sxs-lookup"><span data-stu-id="1a4d7-124">Flags</span></span>  <br/> |<span data-ttu-id="1a4d7-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1a4d7-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1a4d7-126">Optional</span><span class="sxs-lookup"><span data-stu-id="1a4d7-126">optional</span></span>  <br/> ||<span data-ttu-id="1a4d7-127">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1a4d7-128">NameU</span><span class="sxs-lookup"><span data-stu-id="1a4d7-128">NameU</span></span>  <br/> |<span data-ttu-id="1a4d7-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1a4d7-129">xsd:string</span></span>  <br/> |<span data-ttu-id="1a4d7-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="1a4d7-130">required</span></span>  <br/> ||<span data-ttu-id="1a4d7-131">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1a4d7-132">Panos</span><span class="sxs-lookup"><span data-stu-id="1a4d7-132">Panos</span></span>  <br/> |<span data-ttu-id="1a4d7-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1a4d7-133">xsd:string</span></span>  <br/> |<span data-ttu-id="1a4d7-134">Optional</span><span class="sxs-lookup"><span data-stu-id="1a4d7-134">optional</span></span>  <br/> ||<span data-ttu-id="1a4d7-135">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1a4d7-136">Panose</span><span class="sxs-lookup"><span data-stu-id="1a4d7-136">Panose</span></span>  <br/> |<span data-ttu-id="1a4d7-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1a4d7-137">xsd:string</span></span>  <br/> |<span data-ttu-id="1a4d7-138">Optional</span><span class="sxs-lookup"><span data-stu-id="1a4d7-138">optional</span></span>  <br/> ||<span data-ttu-id="1a4d7-139">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1a4d7-140">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="1a4d7-140">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="1a4d7-141">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1a4d7-141">xsd:string</span></span>  <br/> |<span data-ttu-id="1a4d7-142">Optional</span><span class="sxs-lookup"><span data-stu-id="1a4d7-142">optional</span></span>  <br/> ||<span data-ttu-id="1a4d7-143">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-143">Values of the xsd:string type.</span></span>  <br/> |
   

