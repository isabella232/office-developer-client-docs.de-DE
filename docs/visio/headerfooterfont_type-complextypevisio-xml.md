---
title: HeaderFooterFont_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: dd99d87e0d80aad3bcde31e4834337ee59088da2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541071"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a><span data-ttu-id="dcce3-102">HeaderFooterFont_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="dcce3-102">HeaderFooterFont_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="dcce3-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="dcce3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dcce3-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="dcce3-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="dcce3-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="dcce3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="dcce3-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="dcce3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="dcce3-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="dcce3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="dcce3-108">Keine</span><span class="sxs-lookup"><span data-stu-id="dcce3-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dcce3-109">Definition</span><span class="sxs-lookup"><span data-stu-id="dcce3-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="dcce3-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="dcce3-110">Elements and attributes</span></span>

<span data-ttu-id="dcce3-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="dcce3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="dcce3-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dcce3-112">Child elements</span></span>

<span data-ttu-id="dcce3-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="dcce3-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dcce3-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="dcce3-114">Attributes</span></span>

|<span data-ttu-id="dcce3-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="dcce3-115">**Attribute**</span></span>|<span data-ttu-id="dcce3-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="dcce3-116">**Type**</span></span>|<span data-ttu-id="dcce3-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="dcce3-117">**Required**</span></span>|<span data-ttu-id="dcce3-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dcce3-118">**Description**</span></span>|<span data-ttu-id="dcce3-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="dcce3-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="dcce3-120">CharSet</span><span class="sxs-lookup"><span data-stu-id="dcce3-120">CharSet</span></span>  <br/> |<span data-ttu-id="dcce3-121">XSD: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="dcce3-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="dcce3-122">Optional</span><span class="sxs-lookup"><span data-stu-id="dcce3-122">optional</span></span>  <br/> ||<span data-ttu-id="dcce3-123">Werte des XSD: unsignedByte-Typs.</span><span class="sxs-lookup"><span data-stu-id="dcce3-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="dcce3-124">ClipPrecision</span><span class="sxs-lookup"><span data-stu-id="dcce3-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="dcce3-125">XSD: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="dcce3-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="dcce3-126">Optional</span><span class="sxs-lookup"><span data-stu-id="dcce3-126">optional</span></span>  <br/> ||<span data-ttu-id="dcce3-127">Werte des XSD: unsignedByte-Typs.</span><span class="sxs-lookup"><span data-stu-id="dcce3-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="dcce3-128">Hemmung</span><span class="sxs-lookup"><span data-stu-id="dcce3-128">Escapement</span></span>  <br/> |<span data-ttu-id="dcce3-129">XSD: int</span><span class="sxs-lookup"><span data-stu-id="dcce3-129">xsd:int</span></span>  <br/> |<span data-ttu-id="dcce3-130">Optional</span><span class="sxs-lookup"><span data-stu-id="dcce3-130">optional</span></span>  <br/> ||<span data-ttu-id="dcce3-131">Werte des Typs XSD: int.</span><span class="sxs-lookup"><span data-stu-id="dcce3-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="dcce3-132">FaceName</span><span class="sxs-lookup"><span data-stu-id="dcce3-132">FaceName</span></span>  <br/> |<span data-ttu-id="dcce3-133">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="dcce3-133">xsd:string</span></span>  <br/> |<span data-ttu-id="dcce3-134">Optional</span><span class="sxs-lookup"><span data-stu-id="dcce3-134">optional</span></span>  <br/> ||<span data-ttu-id="dcce3-135">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="dcce3-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="dcce3-136">Height</span><span class="sxs-lookup"><span data-stu-id="dcce3-136">Height</span></span>  <br/> |<span data-ttu-id="dcce3-137">XSD: int</span><span class="sxs-lookup"><span data-stu-id="dcce3-137">xsd:int</span></span>  <br/> |<span data-ttu-id="dcce3-138">Optional</span><span class="sxs-lookup"><span data-stu-id="dcce3-138">optional</span></span>  <br/> ||<span data-ttu-id="dcce3-139">Werte des Typs XSD: int.</span><span class="sxs-lookup"><span data-stu-id="dcce3-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="dcce3-140">Kursiv</span><span class="sxs-lookup"><span data-stu-id="dcce3-140">Italic</span></span>  <br/> |<span data-ttu-id="dcce3-141">XSD: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="dcce3-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="dcce3-142">Optional</span><span class="sxs-lookup"><span data-stu-id="dcce3-142">optional</span></span>  <br/> ||<span data-ttu-id="dcce3-143">Werte des XSD: unsignedByte-Typs.</span><span class="sxs-lookup"><span data-stu-id="dcce3-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="dcce3-144">Orientierung</span><span class="sxs-lookup"><span data-stu-id="dcce3-144">Orientation</span></span>  <br/> |<span data-ttu-id="dcce3-145">XSD: int</span><span class="sxs-lookup"><span data-stu-id="dcce3-145">xsd:int</span></span>  <br/> |<span data-ttu-id="dcce3-146">Optional</span><span class="sxs-lookup"><span data-stu-id="dcce3-146">optional</span></span>  <br/> ||<span data-ttu-id="dcce3-147">Werte des Typs XSD: int.</span><span class="sxs-lookup"><span data-stu-id="dcce3-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="dcce3-148">OutPrecision</span><span class="sxs-lookup"><span data-stu-id="dcce3-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="dcce3-149">XSD: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="dcce3-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="dcce3-150">Optional</span><span class="sxs-lookup"><span data-stu-id="dcce3-150">optional</span></span>  <br/> ||<span data-ttu-id="dcce3-151">Werte des XSD: unsignedByte-Typs.</span><span class="sxs-lookup"><span data-stu-id="dcce3-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="dcce3-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="dcce3-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="dcce3-153">XSD: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="dcce3-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="dcce3-154">Optional</span><span class="sxs-lookup"><span data-stu-id="dcce3-154">optional</span></span>  <br/> ||<span data-ttu-id="dcce3-155">Werte des XSD: unsignedByte-Typs.</span><span class="sxs-lookup"><span data-stu-id="dcce3-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="dcce3-156">Quality</span><span class="sxs-lookup"><span data-stu-id="dcce3-156">Quality</span></span>  <br/> |<span data-ttu-id="dcce3-157">XSD: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="dcce3-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="dcce3-158">Optional</span><span class="sxs-lookup"><span data-stu-id="dcce3-158">optional</span></span>  <br/> ||<span data-ttu-id="dcce3-159">Werte des XSD: unsignedByte-Typs.</span><span class="sxs-lookup"><span data-stu-id="dcce3-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="dcce3-160">Durchgestrichen</span><span class="sxs-lookup"><span data-stu-id="dcce3-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="dcce3-161">XSD: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="dcce3-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="dcce3-162">Optional</span><span class="sxs-lookup"><span data-stu-id="dcce3-162">optional</span></span>  <br/> ||<span data-ttu-id="dcce3-163">Werte des XSD: unsignedByte-Typs.</span><span class="sxs-lookup"><span data-stu-id="dcce3-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="dcce3-164">Unterstrichen</span><span class="sxs-lookup"><span data-stu-id="dcce3-164">Underline</span></span>  <br/> |<span data-ttu-id="dcce3-165">XSD: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="dcce3-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="dcce3-166">Optional</span><span class="sxs-lookup"><span data-stu-id="dcce3-166">optional</span></span>  <br/> ||<span data-ttu-id="dcce3-167">Werte des XSD: unsignedByte-Typs.</span><span class="sxs-lookup"><span data-stu-id="dcce3-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="dcce3-168">Schriftbreite</span><span class="sxs-lookup"><span data-stu-id="dcce3-168">Weight</span></span>  <br/> |<span data-ttu-id="dcce3-169">XSD: int</span><span class="sxs-lookup"><span data-stu-id="dcce3-169">xsd:int</span></span>  <br/> |<span data-ttu-id="dcce3-170">Optional</span><span class="sxs-lookup"><span data-stu-id="dcce3-170">optional</span></span>  <br/> ||<span data-ttu-id="dcce3-171">Werte des Typs XSD: int.</span><span class="sxs-lookup"><span data-stu-id="dcce3-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="dcce3-172">Width</span><span class="sxs-lookup"><span data-stu-id="dcce3-172">Width</span></span>  <br/> |<span data-ttu-id="dcce3-173">XSD: int</span><span class="sxs-lookup"><span data-stu-id="dcce3-173">xsd:int</span></span>  <br/> |<span data-ttu-id="dcce3-174">Optional</span><span class="sxs-lookup"><span data-stu-id="dcce3-174">optional</span></span>  <br/> ||<span data-ttu-id="dcce3-175">Werte des Typs XSD: int.</span><span class="sxs-lookup"><span data-stu-id="dcce3-175">Values of the xsd:int type.</span></span>  <br/> |
   

