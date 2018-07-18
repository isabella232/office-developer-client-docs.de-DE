---
title: HeaderFooterFont_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: 1d7c4d6850e4a8ea1933ae751c580d09e0dd67bd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797131"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a><span data-ttu-id="2f660-102">HeaderFooterFont_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="2f660-102">HeaderFooterFont_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2f660-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="2f660-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f660-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2f660-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2f660-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="2f660-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2f660-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2f660-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2f660-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="2f660-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2f660-108">Keine</span><span class="sxs-lookup"><span data-stu-id="2f660-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2f660-109">Definition</span><span class="sxs-lookup"><span data-stu-id="2f660-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="2f660-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="2f660-110">Elements and attributes</span></span>

<span data-ttu-id="2f660-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="2f660-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2f660-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2f660-112">Child elements</span></span>

<span data-ttu-id="2f660-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="2f660-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2f660-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="2f660-114">Attributes</span></span>

|<span data-ttu-id="2f660-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="2f660-115">**Attribute**</span></span>|<span data-ttu-id="2f660-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="2f660-116">**Type**</span></span>|<span data-ttu-id="2f660-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="2f660-117">**Required**</span></span>|<span data-ttu-id="2f660-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2f660-118">**Description**</span></span>|<span data-ttu-id="2f660-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="2f660-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2f660-120">CharSet</span><span class="sxs-lookup"><span data-stu-id="2f660-120">CharSet</span></span>  <br/> |<span data-ttu-id="2f660-121">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="2f660-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="2f660-122">Optional</span><span class="sxs-lookup"><span data-stu-id="2f660-122">optional</span></span>  <br/> ||<span data-ttu-id="2f660-123">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="2f660-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="2f660-124">ClipPrecision</span><span class="sxs-lookup"><span data-stu-id="2f660-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="2f660-125">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="2f660-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="2f660-126">Optional</span><span class="sxs-lookup"><span data-stu-id="2f660-126">optional</span></span>  <br/> ||<span data-ttu-id="2f660-127">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="2f660-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="2f660-128">Vorschub</span><span class="sxs-lookup"><span data-stu-id="2f660-128">Escapement</span></span>  <br/> |<span data-ttu-id="2f660-129">XSD: int</span><span class="sxs-lookup"><span data-stu-id="2f660-129">xsd:int</span></span>  <br/> |<span data-ttu-id="2f660-130">Optional</span><span class="sxs-lookup"><span data-stu-id="2f660-130">optional</span></span>  <br/> ||<span data-ttu-id="2f660-131">Werte des Typs xsd: int.</span><span class="sxs-lookup"><span data-stu-id="2f660-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="2f660-132">FaceName</span><span class="sxs-lookup"><span data-stu-id="2f660-132">FaceName</span></span>  <br/> |<span data-ttu-id="2f660-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="2f660-133">xsd:string</span></span>  <br/> |<span data-ttu-id="2f660-134">Optional</span><span class="sxs-lookup"><span data-stu-id="2f660-134">optional</span></span>  <br/> ||<span data-ttu-id="2f660-135">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="2f660-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2f660-136">Höhe</span><span class="sxs-lookup"><span data-stu-id="2f660-136">Height</span></span>  <br/> |<span data-ttu-id="2f660-137">XSD: int</span><span class="sxs-lookup"><span data-stu-id="2f660-137">xsd:int</span></span>  <br/> |<span data-ttu-id="2f660-138">Optional</span><span class="sxs-lookup"><span data-stu-id="2f660-138">optional</span></span>  <br/> ||<span data-ttu-id="2f660-139">Werte des Typs xsd: int.</span><span class="sxs-lookup"><span data-stu-id="2f660-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="2f660-140">Kursiv</span><span class="sxs-lookup"><span data-stu-id="2f660-140">Italic</span></span>  <br/> |<span data-ttu-id="2f660-141">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="2f660-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="2f660-142">Optional</span><span class="sxs-lookup"><span data-stu-id="2f660-142">optional</span></span>  <br/> ||<span data-ttu-id="2f660-143">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="2f660-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="2f660-144">Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="2f660-144">Orientation</span></span>  <br/> |<span data-ttu-id="2f660-145">XSD: int</span><span class="sxs-lookup"><span data-stu-id="2f660-145">xsd:int</span></span>  <br/> |<span data-ttu-id="2f660-146">Optional</span><span class="sxs-lookup"><span data-stu-id="2f660-146">optional</span></span>  <br/> ||<span data-ttu-id="2f660-147">Werte des Typs xsd: int.</span><span class="sxs-lookup"><span data-stu-id="2f660-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="2f660-148">OutPrecision</span><span class="sxs-lookup"><span data-stu-id="2f660-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="2f660-149">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="2f660-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="2f660-150">Optional</span><span class="sxs-lookup"><span data-stu-id="2f660-150">optional</span></span>  <br/> ||<span data-ttu-id="2f660-151">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="2f660-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="2f660-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="2f660-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="2f660-153">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="2f660-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="2f660-154">Optional</span><span class="sxs-lookup"><span data-stu-id="2f660-154">optional</span></span>  <br/> ||<span data-ttu-id="2f660-155">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="2f660-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="2f660-156">Qualität</span><span class="sxs-lookup"><span data-stu-id="2f660-156">Quality</span></span>  <br/> |<span data-ttu-id="2f660-157">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="2f660-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="2f660-158">Optional</span><span class="sxs-lookup"><span data-stu-id="2f660-158">optional</span></span>  <br/> ||<span data-ttu-id="2f660-159">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="2f660-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="2f660-160">Durchgestrichen</span><span class="sxs-lookup"><span data-stu-id="2f660-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="2f660-161">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="2f660-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="2f660-162">Optional</span><span class="sxs-lookup"><span data-stu-id="2f660-162">optional</span></span>  <br/> ||<span data-ttu-id="2f660-163">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="2f660-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="2f660-164">Unterstrichen</span><span class="sxs-lookup"><span data-stu-id="2f660-164">Underline</span></span>  <br/> |<span data-ttu-id="2f660-165">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="2f660-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="2f660-166">Optional</span><span class="sxs-lookup"><span data-stu-id="2f660-166">optional</span></span>  <br/> ||<span data-ttu-id="2f660-167">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="2f660-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="2f660-168">Weight</span><span class="sxs-lookup"><span data-stu-id="2f660-168">Weight</span></span>  <br/> |<span data-ttu-id="2f660-169">XSD: int</span><span class="sxs-lookup"><span data-stu-id="2f660-169">xsd:int</span></span>  <br/> |<span data-ttu-id="2f660-170">Optional</span><span class="sxs-lookup"><span data-stu-id="2f660-170">optional</span></span>  <br/> ||<span data-ttu-id="2f660-171">Werte des Typs xsd: int.</span><span class="sxs-lookup"><span data-stu-id="2f660-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="2f660-172">Breite</span><span class="sxs-lookup"><span data-stu-id="2f660-172">Width</span></span>  <br/> |<span data-ttu-id="2f660-173">XSD: int</span><span class="sxs-lookup"><span data-stu-id="2f660-173">xsd:int</span></span>  <br/> |<span data-ttu-id="2f660-174">Optional</span><span class="sxs-lookup"><span data-stu-id="2f660-174">optional</span></span>  <br/> ||<span data-ttu-id="2f660-175">Werte des Typs xsd: int.</span><span class="sxs-lookup"><span data-stu-id="2f660-175">Values of the xsd:int type.</span></span>  <br/> |
   

