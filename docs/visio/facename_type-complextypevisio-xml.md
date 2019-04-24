---
title: FaceName_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: 8035f541e619360403336bd2fbd931cf05dbfe59
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322554"
---
# <a name="facenametype-complextype-visio-xml"></a><span data-ttu-id="a57a2-102">FaceName_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="a57a2-102">FaceName_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a57a2-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="a57a2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a57a2-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a57a2-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a57a2-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="a57a2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a57a2-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="a57a2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a57a2-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="a57a2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a57a2-108">Keine</span><span class="sxs-lookup"><span data-stu-id="a57a2-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a57a2-109">Definition</span><span class="sxs-lookup"><span data-stu-id="a57a2-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a57a2-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="a57a2-110">Elements and attributes</span></span>

<span data-ttu-id="a57a2-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="a57a2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a57a2-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a57a2-112">Child elements</span></span>

<span data-ttu-id="a57a2-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="a57a2-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a57a2-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="a57a2-114">Attributes</span></span>

|<span data-ttu-id="a57a2-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a57a2-115">**Attribute**</span></span>|<span data-ttu-id="a57a2-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="a57a2-116">**Type**</span></span>|<span data-ttu-id="a57a2-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="a57a2-117">**Required**</span></span>|<span data-ttu-id="a57a2-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a57a2-118">**Description**</span></span>|<span data-ttu-id="a57a2-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="a57a2-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a57a2-120">CharSets</span><span class="sxs-lookup"><span data-stu-id="a57a2-120">CharSets</span></span>  <br/> |<span data-ttu-id="a57a2-121">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a57a2-121">xsd:string</span></span>  <br/> |<span data-ttu-id="a57a2-122">Optional</span><span class="sxs-lookup"><span data-stu-id="a57a2-122">optional</span></span>  <br/> ||<span data-ttu-id="a57a2-123">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="a57a2-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a57a2-124">Flags</span><span class="sxs-lookup"><span data-stu-id="a57a2-124">Flags</span></span>  <br/> |<span data-ttu-id="a57a2-125">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a57a2-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a57a2-126">Optional</span><span class="sxs-lookup"><span data-stu-id="a57a2-126">optional</span></span>  <br/> ||<span data-ttu-id="a57a2-127">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="a57a2-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a57a2-128">NameU</span><span class="sxs-lookup"><span data-stu-id="a57a2-128">NameU</span></span>  <br/> |<span data-ttu-id="a57a2-129">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a57a2-129">xsd:string</span></span>  <br/> |<span data-ttu-id="a57a2-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="a57a2-130">required</span></span>  <br/> ||<span data-ttu-id="a57a2-131">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="a57a2-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a57a2-132">PANOS</span><span class="sxs-lookup"><span data-stu-id="a57a2-132">Panos</span></span>  <br/> |<span data-ttu-id="a57a2-133">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a57a2-133">xsd:string</span></span>  <br/> |<span data-ttu-id="a57a2-134">Optional</span><span class="sxs-lookup"><span data-stu-id="a57a2-134">optional</span></span>  <br/> ||<span data-ttu-id="a57a2-135">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="a57a2-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a57a2-136">Panose</span><span class="sxs-lookup"><span data-stu-id="a57a2-136">Panose</span></span>  <br/> |<span data-ttu-id="a57a2-137">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a57a2-137">xsd:string</span></span>  <br/> |<span data-ttu-id="a57a2-138">Optional</span><span class="sxs-lookup"><span data-stu-id="a57a2-138">optional</span></span>  <br/> ||<span data-ttu-id="a57a2-139">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="a57a2-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a57a2-140">Unicode Ranges</span><span class="sxs-lookup"><span data-stu-id="a57a2-140">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="a57a2-141">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a57a2-141">xsd:string</span></span>  <br/> |<span data-ttu-id="a57a2-142">Optional</span><span class="sxs-lookup"><span data-stu-id="a57a2-142">optional</span></span>  <br/> ||<span data-ttu-id="a57a2-143">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="a57a2-143">Values of the xsd:string type.</span></span>  <br/> |
   

