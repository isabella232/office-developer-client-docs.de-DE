---
title: FaceName_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: 554a8144fd38c34d59aa2fd0ae25d171c20cd8ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796966"
---
# <a name="facenametype-complextype-visio-xml"></a><span data-ttu-id="6baca-102">FaceName_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="6baca-102">FaceName_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6baca-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="6baca-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6baca-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6baca-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6baca-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="6baca-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6baca-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6baca-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6baca-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="6baca-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6baca-108">Keine</span><span class="sxs-lookup"><span data-stu-id="6baca-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6baca-109">Definition</span><span class="sxs-lookup"><span data-stu-id="6baca-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="6baca-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="6baca-110">Elements and attributes</span></span>

<span data-ttu-id="6baca-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="6baca-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6baca-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6baca-112">Child elements</span></span>

<span data-ttu-id="6baca-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="6baca-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6baca-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="6baca-114">Attributes</span></span>

|<span data-ttu-id="6baca-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="6baca-115">**Attribute**</span></span>|<span data-ttu-id="6baca-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="6baca-116">**Type**</span></span>|<span data-ttu-id="6baca-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="6baca-117">**Required**</span></span>|<span data-ttu-id="6baca-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6baca-118">**Description**</span></span>|<span data-ttu-id="6baca-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="6baca-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6baca-120">Zeichensätze</span><span class="sxs-lookup"><span data-stu-id="6baca-120">CharSets</span></span>  <br/> |<span data-ttu-id="6baca-121">XSD: String</span><span class="sxs-lookup"><span data-stu-id="6baca-121">xsd:string</span></span>  <br/> |<span data-ttu-id="6baca-122">Optional</span><span class="sxs-lookup"><span data-stu-id="6baca-122">optional</span></span>  <br/> ||<span data-ttu-id="6baca-123">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="6baca-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6baca-124">Flags</span><span class="sxs-lookup"><span data-stu-id="6baca-124">Flags</span></span>  <br/> |<span data-ttu-id="6baca-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6baca-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6baca-126">Optional</span><span class="sxs-lookup"><span data-stu-id="6baca-126">optional</span></span>  <br/> ||<span data-ttu-id="6baca-127">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6baca-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6baca-128">NameU</span><span class="sxs-lookup"><span data-stu-id="6baca-128">NameU</span></span>  <br/> |<span data-ttu-id="6baca-129">XSD: String</span><span class="sxs-lookup"><span data-stu-id="6baca-129">xsd:string</span></span>  <br/> |<span data-ttu-id="6baca-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="6baca-130">required</span></span>  <br/> ||<span data-ttu-id="6baca-131">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="6baca-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6baca-132">Panos</span><span class="sxs-lookup"><span data-stu-id="6baca-132">Panos</span></span>  <br/> |<span data-ttu-id="6baca-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="6baca-133">xsd:string</span></span>  <br/> |<span data-ttu-id="6baca-134">Optional</span><span class="sxs-lookup"><span data-stu-id="6baca-134">optional</span></span>  <br/> ||<span data-ttu-id="6baca-135">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="6baca-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6baca-136">Panose</span><span class="sxs-lookup"><span data-stu-id="6baca-136">Panose</span></span>  <br/> |<span data-ttu-id="6baca-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="6baca-137">xsd:string</span></span>  <br/> |<span data-ttu-id="6baca-138">Optional</span><span class="sxs-lookup"><span data-stu-id="6baca-138">optional</span></span>  <br/> ||<span data-ttu-id="6baca-139">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="6baca-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6baca-140">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="6baca-140">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="6baca-141">XSD: String</span><span class="sxs-lookup"><span data-stu-id="6baca-141">xsd:string</span></span>  <br/> |<span data-ttu-id="6baca-142">Optional</span><span class="sxs-lookup"><span data-stu-id="6baca-142">optional</span></span>  <br/> ||<span data-ttu-id="6baca-143">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="6baca-143">Values of the xsd:string type.</span></span>  <br/> |
   

