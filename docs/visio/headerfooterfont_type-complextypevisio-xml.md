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
# <a name="headerfooterfonttype-complextype-visio-xml"></a><span data-ttu-id="df72a-102">HeaderFooterFont_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="df72a-102">HeaderFooterFont_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="df72a-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="df72a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="df72a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="df72a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="df72a-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="df72a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="df72a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="df72a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="df72a-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="df72a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="df72a-108">Keine</span><span class="sxs-lookup"><span data-stu-id="df72a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="df72a-109">Definition</span><span class="sxs-lookup"><span data-stu-id="df72a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="df72a-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="df72a-110">Elements and attributes</span></span>

<span data-ttu-id="df72a-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="df72a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="df72a-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="df72a-112">Child elements</span></span>

<span data-ttu-id="df72a-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="df72a-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="df72a-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="df72a-114">Attributes</span></span>

|<span data-ttu-id="df72a-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="df72a-115">**Attribute**</span></span>|<span data-ttu-id="df72a-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="df72a-116">**Type**</span></span>|<span data-ttu-id="df72a-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="df72a-117">**Required**</span></span>|<span data-ttu-id="df72a-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="df72a-118">**Description**</span></span>|<span data-ttu-id="df72a-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="df72a-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="df72a-120">CharSet</span><span class="sxs-lookup"><span data-stu-id="df72a-120">CharSet</span></span>  <br/> |<span data-ttu-id="df72a-121">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="df72a-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="df72a-122">Optional</span><span class="sxs-lookup"><span data-stu-id="df72a-122">optional</span></span>  <br/> ||<span data-ttu-id="df72a-123">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="df72a-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="df72a-124">ClipPrecision</span><span class="sxs-lookup"><span data-stu-id="df72a-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="df72a-125">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="df72a-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="df72a-126">Optional</span><span class="sxs-lookup"><span data-stu-id="df72a-126">optional</span></span>  <br/> ||<span data-ttu-id="df72a-127">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="df72a-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="df72a-128">Vorschub</span><span class="sxs-lookup"><span data-stu-id="df72a-128">Escapement</span></span>  <br/> |<span data-ttu-id="df72a-129">XSD: int</span><span class="sxs-lookup"><span data-stu-id="df72a-129">xsd:int</span></span>  <br/> |<span data-ttu-id="df72a-130">Optional</span><span class="sxs-lookup"><span data-stu-id="df72a-130">optional</span></span>  <br/> ||<span data-ttu-id="df72a-131">Werte des Typs xsd: int.</span><span class="sxs-lookup"><span data-stu-id="df72a-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="df72a-132">FaceName</span><span class="sxs-lookup"><span data-stu-id="df72a-132">FaceName</span></span>  <br/> |<span data-ttu-id="df72a-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="df72a-133">xsd:string</span></span>  <br/> |<span data-ttu-id="df72a-134">Optional</span><span class="sxs-lookup"><span data-stu-id="df72a-134">optional</span></span>  <br/> ||<span data-ttu-id="df72a-135">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="df72a-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="df72a-136">Höhe</span><span class="sxs-lookup"><span data-stu-id="df72a-136">Height</span></span>  <br/> |<span data-ttu-id="df72a-137">XSD: int</span><span class="sxs-lookup"><span data-stu-id="df72a-137">xsd:int</span></span>  <br/> |<span data-ttu-id="df72a-138">Optional</span><span class="sxs-lookup"><span data-stu-id="df72a-138">optional</span></span>  <br/> ||<span data-ttu-id="df72a-139">Werte des Typs xsd: int.</span><span class="sxs-lookup"><span data-stu-id="df72a-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="df72a-140">Kursiv</span><span class="sxs-lookup"><span data-stu-id="df72a-140">Italic</span></span>  <br/> |<span data-ttu-id="df72a-141">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="df72a-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="df72a-142">Optional</span><span class="sxs-lookup"><span data-stu-id="df72a-142">optional</span></span>  <br/> ||<span data-ttu-id="df72a-143">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="df72a-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="df72a-144">Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="df72a-144">Orientation</span></span>  <br/> |<span data-ttu-id="df72a-145">XSD: int</span><span class="sxs-lookup"><span data-stu-id="df72a-145">xsd:int</span></span>  <br/> |<span data-ttu-id="df72a-146">Optional</span><span class="sxs-lookup"><span data-stu-id="df72a-146">optional</span></span>  <br/> ||<span data-ttu-id="df72a-147">Werte des Typs xsd: int.</span><span class="sxs-lookup"><span data-stu-id="df72a-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="df72a-148">OutPrecision</span><span class="sxs-lookup"><span data-stu-id="df72a-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="df72a-149">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="df72a-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="df72a-150">Optional</span><span class="sxs-lookup"><span data-stu-id="df72a-150">optional</span></span>  <br/> ||<span data-ttu-id="df72a-151">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="df72a-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="df72a-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="df72a-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="df72a-153">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="df72a-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="df72a-154">Optional</span><span class="sxs-lookup"><span data-stu-id="df72a-154">optional</span></span>  <br/> ||<span data-ttu-id="df72a-155">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="df72a-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="df72a-156">Qualität</span><span class="sxs-lookup"><span data-stu-id="df72a-156">Quality</span></span>  <br/> |<span data-ttu-id="df72a-157">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="df72a-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="df72a-158">Optional</span><span class="sxs-lookup"><span data-stu-id="df72a-158">optional</span></span>  <br/> ||<span data-ttu-id="df72a-159">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="df72a-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="df72a-160">Durchgestrichen</span><span class="sxs-lookup"><span data-stu-id="df72a-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="df72a-161">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="df72a-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="df72a-162">Optional</span><span class="sxs-lookup"><span data-stu-id="df72a-162">optional</span></span>  <br/> ||<span data-ttu-id="df72a-163">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="df72a-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="df72a-164">Unterstrichen</span><span class="sxs-lookup"><span data-stu-id="df72a-164">Underline</span></span>  <br/> |<span data-ttu-id="df72a-165">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="df72a-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="df72a-166">Optional</span><span class="sxs-lookup"><span data-stu-id="df72a-166">optional</span></span>  <br/> ||<span data-ttu-id="df72a-167">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="df72a-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="df72a-168">Gewicht</span><span class="sxs-lookup"><span data-stu-id="df72a-168">Weight</span></span>  <br/> |<span data-ttu-id="df72a-169">XSD: int</span><span class="sxs-lookup"><span data-stu-id="df72a-169">xsd:int</span></span>  <br/> |<span data-ttu-id="df72a-170">Optional</span><span class="sxs-lookup"><span data-stu-id="df72a-170">optional</span></span>  <br/> ||<span data-ttu-id="df72a-171">Werte des Typs xsd: int.</span><span class="sxs-lookup"><span data-stu-id="df72a-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="df72a-172">Breite</span><span class="sxs-lookup"><span data-stu-id="df72a-172">Width</span></span>  <br/> |<span data-ttu-id="df72a-173">XSD: int</span><span class="sxs-lookup"><span data-stu-id="df72a-173">xsd:int</span></span>  <br/> |<span data-ttu-id="df72a-174">Optional</span><span class="sxs-lookup"><span data-stu-id="df72a-174">optional</span></span>  <br/> ||<span data-ttu-id="df72a-175">Werte des Typs xsd: int.</span><span class="sxs-lookup"><span data-stu-id="df72a-175">Values of the xsd:int type.</span></span>  <br/> |
   

