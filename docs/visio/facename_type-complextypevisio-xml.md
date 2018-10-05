---
title: FaceName_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: 8035f541e619360403336bd2fbd931cf05dbfe59
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382442"
---
# <a name="facenametype-complextype-visio-xml"></a><span data-ttu-id="53111-102">FaceName_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="53111-102">FaceName_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="53111-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="53111-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53111-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="53111-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="53111-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="53111-105">**Schema file**</span></span> <br/> |<span data-ttu-id="53111-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="53111-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="53111-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="53111-107">**Extension base**</span></span> <br/> |<span data-ttu-id="53111-108">Keine</span><span class="sxs-lookup"><span data-stu-id="53111-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="53111-109">Definition</span><span class="sxs-lookup"><span data-stu-id="53111-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="53111-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="53111-110">Elements and attributes</span></span>

<span data-ttu-id="53111-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="53111-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="53111-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="53111-112">Child elements</span></span>

<span data-ttu-id="53111-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="53111-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="53111-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="53111-114">Attributes</span></span>

|<span data-ttu-id="53111-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="53111-115">**Attribute**</span></span>|<span data-ttu-id="53111-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="53111-116">**Type**</span></span>|<span data-ttu-id="53111-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="53111-117">**Required**</span></span>|<span data-ttu-id="53111-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="53111-118">**Description**</span></span>|<span data-ttu-id="53111-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="53111-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="53111-120">Zeichensätze</span><span class="sxs-lookup"><span data-stu-id="53111-120">CharSets</span></span>  <br/> |<span data-ttu-id="53111-121">XSD: String</span><span class="sxs-lookup"><span data-stu-id="53111-121">xsd:string</span></span>  <br/> |<span data-ttu-id="53111-122">Optional</span><span class="sxs-lookup"><span data-stu-id="53111-122">optional</span></span>  <br/> ||<span data-ttu-id="53111-123">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="53111-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="53111-124">Flags</span><span class="sxs-lookup"><span data-stu-id="53111-124">Flags</span></span>  <br/> |<span data-ttu-id="53111-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="53111-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="53111-126">Optional</span><span class="sxs-lookup"><span data-stu-id="53111-126">optional</span></span>  <br/> ||<span data-ttu-id="53111-127">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="53111-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="53111-128">NameU</span><span class="sxs-lookup"><span data-stu-id="53111-128">NameU</span></span>  <br/> |<span data-ttu-id="53111-129">XSD: String</span><span class="sxs-lookup"><span data-stu-id="53111-129">xsd:string</span></span>  <br/> |<span data-ttu-id="53111-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="53111-130">required</span></span>  <br/> ||<span data-ttu-id="53111-131">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="53111-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="53111-132">Panos</span><span class="sxs-lookup"><span data-stu-id="53111-132">Panos</span></span>  <br/> |<span data-ttu-id="53111-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="53111-133">xsd:string</span></span>  <br/> |<span data-ttu-id="53111-134">Optional</span><span class="sxs-lookup"><span data-stu-id="53111-134">optional</span></span>  <br/> ||<span data-ttu-id="53111-135">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="53111-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="53111-136">Panose</span><span class="sxs-lookup"><span data-stu-id="53111-136">Panose</span></span>  <br/> |<span data-ttu-id="53111-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="53111-137">xsd:string</span></span>  <br/> |<span data-ttu-id="53111-138">Optional</span><span class="sxs-lookup"><span data-stu-id="53111-138">optional</span></span>  <br/> ||<span data-ttu-id="53111-139">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="53111-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="53111-140">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="53111-140">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="53111-141">XSD: String</span><span class="sxs-lookup"><span data-stu-id="53111-141">xsd:string</span></span>  <br/> |<span data-ttu-id="53111-142">Optional</span><span class="sxs-lookup"><span data-stu-id="53111-142">optional</span></span>  <br/> ||<span data-ttu-id="53111-143">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="53111-143">Values of the xsd:string type.</span></span>  <br/> |
   

