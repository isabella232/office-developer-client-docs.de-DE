---
title: HeaderFooterFont_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: cc51924aa68e3248583be5f717b5813d4a32af2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335623"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a><span data-ttu-id="ab77c-102">HeaderFooterFont_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="ab77c-102">HeaderFooterFont_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ab77c-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="ab77c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ab77c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ab77c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ab77c-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="ab77c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ab77c-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="ab77c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ab77c-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="ab77c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ab77c-108">Keine</span><span class="sxs-lookup"><span data-stu-id="ab77c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ab77c-109">Definition</span><span class="sxs-lookup"><span data-stu-id="ab77c-109">Definition</span></span>

```XML
      <xs:complexType name="HeaderFooterFont_Type">
    <xs:attribute name="Height"
  type="xsd:int"
    />
    <xs:attribute name="Width"
  type="xsd:int"
    />
    <xs:attribute name="Escapement"
  type="xsd:int"
    />
    <xs:attribute name="Orientation"
  type="xsd:int"
    />
    <xs:attribute name="Weight"
  type="xsd:int"
    />
    <xs:attribute name="Italic"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="Underline"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="StrikeOut"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="CharSet"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="OutPrecision"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="ClipPrecision"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="Quality"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="PitchAndFamily"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="FaceName"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ab77c-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="ab77c-110">Elements and attributes</span></span>

<span data-ttu-id="ab77c-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="ab77c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ab77c-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ab77c-112">Child elements</span></span>

<span data-ttu-id="ab77c-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="ab77c-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ab77c-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="ab77c-114">Attributes</span></span>

|<span data-ttu-id="ab77c-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ab77c-115">**Attribute**</span></span>|<span data-ttu-id="ab77c-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ab77c-116">**Type**</span></span>|<span data-ttu-id="ab77c-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="ab77c-117">**Required**</span></span>|<span data-ttu-id="ab77c-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ab77c-118">**Description**</span></span>|<span data-ttu-id="ab77c-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="ab77c-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ab77c-120">CharSet</span><span class="sxs-lookup"><span data-stu-id="ab77c-120">CharSet</span></span>  <br/> |<span data-ttu-id="ab77c-121">XSD: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="ab77c-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="ab77c-122">Optional</span><span class="sxs-lookup"><span data-stu-id="ab77c-122">optional</span></span>  <br/> ||<span data-ttu-id="ab77c-123">Werte des XSD: unsignedByte-Typs.</span><span class="sxs-lookup"><span data-stu-id="ab77c-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="ab77c-124">ClipPrecision</span><span class="sxs-lookup"><span data-stu-id="ab77c-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="ab77c-125">XSD: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="ab77c-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="ab77c-126">Optional</span><span class="sxs-lookup"><span data-stu-id="ab77c-126">optional</span></span>  <br/> ||<span data-ttu-id="ab77c-127">Werte des XSD: unsignedByte-Typs.</span><span class="sxs-lookup"><span data-stu-id="ab77c-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="ab77c-128">Hemmung</span><span class="sxs-lookup"><span data-stu-id="ab77c-128">Escapement</span></span>  <br/> |<span data-ttu-id="ab77c-129">XSD: int</span><span class="sxs-lookup"><span data-stu-id="ab77c-129">xsd:int</span></span>  <br/> |<span data-ttu-id="ab77c-130">Optional</span><span class="sxs-lookup"><span data-stu-id="ab77c-130">optional</span></span>  <br/> ||<span data-ttu-id="ab77c-131">Werte des XSD: int-Typs.</span><span class="sxs-lookup"><span data-stu-id="ab77c-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="ab77c-132">FaceName</span><span class="sxs-lookup"><span data-stu-id="ab77c-132">FaceName</span></span>  <br/> |<span data-ttu-id="ab77c-133">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ab77c-133">xsd:string</span></span>  <br/> |<span data-ttu-id="ab77c-134">Optional</span><span class="sxs-lookup"><span data-stu-id="ab77c-134">optional</span></span>  <br/> ||<span data-ttu-id="ab77c-135">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="ab77c-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ab77c-136">Height</span><span class="sxs-lookup"><span data-stu-id="ab77c-136">Height</span></span>  <br/> |<span data-ttu-id="ab77c-137">XSD: int</span><span class="sxs-lookup"><span data-stu-id="ab77c-137">xsd:int</span></span>  <br/> |<span data-ttu-id="ab77c-138">Optional</span><span class="sxs-lookup"><span data-stu-id="ab77c-138">optional</span></span>  <br/> ||<span data-ttu-id="ab77c-139">Werte des XSD: int-Typs.</span><span class="sxs-lookup"><span data-stu-id="ab77c-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="ab77c-140">Kursiv</span><span class="sxs-lookup"><span data-stu-id="ab77c-140">Italic</span></span>  <br/> |<span data-ttu-id="ab77c-141">XSD: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="ab77c-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="ab77c-142">Optional</span><span class="sxs-lookup"><span data-stu-id="ab77c-142">optional</span></span>  <br/> ||<span data-ttu-id="ab77c-143">Werte des XSD: unsignedByte-Typs.</span><span class="sxs-lookup"><span data-stu-id="ab77c-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="ab77c-144">Orientierung</span><span class="sxs-lookup"><span data-stu-id="ab77c-144">Orientation</span></span>  <br/> |<span data-ttu-id="ab77c-145">XSD: int</span><span class="sxs-lookup"><span data-stu-id="ab77c-145">xsd:int</span></span>  <br/> |<span data-ttu-id="ab77c-146">Optional</span><span class="sxs-lookup"><span data-stu-id="ab77c-146">optional</span></span>  <br/> ||<span data-ttu-id="ab77c-147">Werte des XSD: int-Typs.</span><span class="sxs-lookup"><span data-stu-id="ab77c-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="ab77c-148">OutPrecision</span><span class="sxs-lookup"><span data-stu-id="ab77c-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="ab77c-149">XSD: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="ab77c-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="ab77c-150">Optional</span><span class="sxs-lookup"><span data-stu-id="ab77c-150">optional</span></span>  <br/> ||<span data-ttu-id="ab77c-151">Werte des XSD: unsignedByte-Typs.</span><span class="sxs-lookup"><span data-stu-id="ab77c-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="ab77c-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="ab77c-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="ab77c-153">XSD: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="ab77c-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="ab77c-154">Optional</span><span class="sxs-lookup"><span data-stu-id="ab77c-154">optional</span></span>  <br/> ||<span data-ttu-id="ab77c-155">Werte des XSD: unsignedByte-Typs.</span><span class="sxs-lookup"><span data-stu-id="ab77c-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="ab77c-156">Quality</span><span class="sxs-lookup"><span data-stu-id="ab77c-156">Quality</span></span>  <br/> |<span data-ttu-id="ab77c-157">XSD: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="ab77c-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="ab77c-158">Optional</span><span class="sxs-lookup"><span data-stu-id="ab77c-158">optional</span></span>  <br/> ||<span data-ttu-id="ab77c-159">Werte des XSD: unsignedByte-Typs.</span><span class="sxs-lookup"><span data-stu-id="ab77c-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="ab77c-160">Durchgestrichen</span><span class="sxs-lookup"><span data-stu-id="ab77c-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="ab77c-161">XSD: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="ab77c-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="ab77c-162">Optional</span><span class="sxs-lookup"><span data-stu-id="ab77c-162">optional</span></span>  <br/> ||<span data-ttu-id="ab77c-163">Werte des XSD: unsignedByte-Typs.</span><span class="sxs-lookup"><span data-stu-id="ab77c-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="ab77c-164">Unterstrichen</span><span class="sxs-lookup"><span data-stu-id="ab77c-164">Underline</span></span>  <br/> |<span data-ttu-id="ab77c-165">XSD: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="ab77c-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="ab77c-166">Optional</span><span class="sxs-lookup"><span data-stu-id="ab77c-166">optional</span></span>  <br/> ||<span data-ttu-id="ab77c-167">Werte des XSD: unsignedByte-Typs.</span><span class="sxs-lookup"><span data-stu-id="ab77c-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="ab77c-168">Schriftbreite</span><span class="sxs-lookup"><span data-stu-id="ab77c-168">Weight</span></span>  <br/> |<span data-ttu-id="ab77c-169">XSD: int</span><span class="sxs-lookup"><span data-stu-id="ab77c-169">xsd:int</span></span>  <br/> |<span data-ttu-id="ab77c-170">Optional</span><span class="sxs-lookup"><span data-stu-id="ab77c-170">optional</span></span>  <br/> ||<span data-ttu-id="ab77c-171">Werte des XSD: int-Typs.</span><span class="sxs-lookup"><span data-stu-id="ab77c-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="ab77c-172">Width</span><span class="sxs-lookup"><span data-stu-id="ab77c-172">Width</span></span>  <br/> |<span data-ttu-id="ab77c-173">XSD: int</span><span class="sxs-lookup"><span data-stu-id="ab77c-173">xsd:int</span></span>  <br/> |<span data-ttu-id="ab77c-174">Optional</span><span class="sxs-lookup"><span data-stu-id="ab77c-174">optional</span></span>  <br/> ||<span data-ttu-id="ab77c-175">Werte des XSD: int-Typs.</span><span class="sxs-lookup"><span data-stu-id="ab77c-175">Values of the xsd:int type.</span></span>  <br/> |
   

