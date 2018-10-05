---
title: HeaderFooterFont_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: cc51924aa68e3248583be5f717b5813d4a32af2b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397247"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a><span data-ttu-id="91c3e-102">HeaderFooterFont_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="91c3e-102">HeaderFooterFont_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="91c3e-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="91c3e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="91c3e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="91c3e-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="91c3e-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="91c3e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="91c3e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="91c3e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="91c3e-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="91c3e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="91c3e-108">Keine</span><span class="sxs-lookup"><span data-stu-id="91c3e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="91c3e-109">Definition</span><span class="sxs-lookup"><span data-stu-id="91c3e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="91c3e-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="91c3e-110">Elements and attributes</span></span>

<span data-ttu-id="91c3e-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="91c3e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="91c3e-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="91c3e-112">Child elements</span></span>

<span data-ttu-id="91c3e-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="91c3e-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="91c3e-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="91c3e-114">Attributes</span></span>

|<span data-ttu-id="91c3e-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="91c3e-115">**Attribute**</span></span>|<span data-ttu-id="91c3e-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="91c3e-116">**Type**</span></span>|<span data-ttu-id="91c3e-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="91c3e-117">**Required**</span></span>|<span data-ttu-id="91c3e-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="91c3e-118">**Description**</span></span>|<span data-ttu-id="91c3e-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="91c3e-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="91c3e-120">CharSet</span><span class="sxs-lookup"><span data-stu-id="91c3e-120">CharSet</span></span>  <br/> |<span data-ttu-id="91c3e-121">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="91c3e-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="91c3e-122">Optional</span><span class="sxs-lookup"><span data-stu-id="91c3e-122">optional</span></span>  <br/> ||<span data-ttu-id="91c3e-123">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="91c3e-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="91c3e-124">ClipPrecision</span><span class="sxs-lookup"><span data-stu-id="91c3e-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="91c3e-125">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="91c3e-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="91c3e-126">Optional</span><span class="sxs-lookup"><span data-stu-id="91c3e-126">optional</span></span>  <br/> ||<span data-ttu-id="91c3e-127">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="91c3e-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="91c3e-128">Vorschub</span><span class="sxs-lookup"><span data-stu-id="91c3e-128">Escapement</span></span>  <br/> |<span data-ttu-id="91c3e-129">XSD: int</span><span class="sxs-lookup"><span data-stu-id="91c3e-129">xsd:int</span></span>  <br/> |<span data-ttu-id="91c3e-130">Optional</span><span class="sxs-lookup"><span data-stu-id="91c3e-130">optional</span></span>  <br/> ||<span data-ttu-id="91c3e-131">Werte des Typs xsd: int.</span><span class="sxs-lookup"><span data-stu-id="91c3e-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="91c3e-132">FaceName</span><span class="sxs-lookup"><span data-stu-id="91c3e-132">FaceName</span></span>  <br/> |<span data-ttu-id="91c3e-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="91c3e-133">xsd:string</span></span>  <br/> |<span data-ttu-id="91c3e-134">Optional</span><span class="sxs-lookup"><span data-stu-id="91c3e-134">optional</span></span>  <br/> ||<span data-ttu-id="91c3e-135">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="91c3e-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="91c3e-136">Höhe</span><span class="sxs-lookup"><span data-stu-id="91c3e-136">Height</span></span>  <br/> |<span data-ttu-id="91c3e-137">XSD: int</span><span class="sxs-lookup"><span data-stu-id="91c3e-137">xsd:int</span></span>  <br/> |<span data-ttu-id="91c3e-138">Optional</span><span class="sxs-lookup"><span data-stu-id="91c3e-138">optional</span></span>  <br/> ||<span data-ttu-id="91c3e-139">Werte des Typs xsd: int.</span><span class="sxs-lookup"><span data-stu-id="91c3e-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="91c3e-140">Kursiv</span><span class="sxs-lookup"><span data-stu-id="91c3e-140">Italic</span></span>  <br/> |<span data-ttu-id="91c3e-141">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="91c3e-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="91c3e-142">Optional</span><span class="sxs-lookup"><span data-stu-id="91c3e-142">optional</span></span>  <br/> ||<span data-ttu-id="91c3e-143">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="91c3e-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="91c3e-144">Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="91c3e-144">Orientation</span></span>  <br/> |<span data-ttu-id="91c3e-145">XSD: int</span><span class="sxs-lookup"><span data-stu-id="91c3e-145">xsd:int</span></span>  <br/> |<span data-ttu-id="91c3e-146">Optional</span><span class="sxs-lookup"><span data-stu-id="91c3e-146">optional</span></span>  <br/> ||<span data-ttu-id="91c3e-147">Werte des Typs xsd: int.</span><span class="sxs-lookup"><span data-stu-id="91c3e-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="91c3e-148">OutPrecision</span><span class="sxs-lookup"><span data-stu-id="91c3e-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="91c3e-149">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="91c3e-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="91c3e-150">Optional</span><span class="sxs-lookup"><span data-stu-id="91c3e-150">optional</span></span>  <br/> ||<span data-ttu-id="91c3e-151">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="91c3e-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="91c3e-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="91c3e-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="91c3e-153">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="91c3e-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="91c3e-154">Optional</span><span class="sxs-lookup"><span data-stu-id="91c3e-154">optional</span></span>  <br/> ||<span data-ttu-id="91c3e-155">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="91c3e-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="91c3e-156">Qualität</span><span class="sxs-lookup"><span data-stu-id="91c3e-156">Quality</span></span>  <br/> |<span data-ttu-id="91c3e-157">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="91c3e-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="91c3e-158">Optional</span><span class="sxs-lookup"><span data-stu-id="91c3e-158">optional</span></span>  <br/> ||<span data-ttu-id="91c3e-159">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="91c3e-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="91c3e-160">Durchgestrichen</span><span class="sxs-lookup"><span data-stu-id="91c3e-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="91c3e-161">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="91c3e-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="91c3e-162">Optional</span><span class="sxs-lookup"><span data-stu-id="91c3e-162">optional</span></span>  <br/> ||<span data-ttu-id="91c3e-163">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="91c3e-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="91c3e-164">Unterstrichen</span><span class="sxs-lookup"><span data-stu-id="91c3e-164">Underline</span></span>  <br/> |<span data-ttu-id="91c3e-165">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="91c3e-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="91c3e-166">Optional</span><span class="sxs-lookup"><span data-stu-id="91c3e-166">optional</span></span>  <br/> ||<span data-ttu-id="91c3e-167">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="91c3e-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="91c3e-168">Weight</span><span class="sxs-lookup"><span data-stu-id="91c3e-168">Weight</span></span>  <br/> |<span data-ttu-id="91c3e-169">XSD: int</span><span class="sxs-lookup"><span data-stu-id="91c3e-169">xsd:int</span></span>  <br/> |<span data-ttu-id="91c3e-170">Optional</span><span class="sxs-lookup"><span data-stu-id="91c3e-170">optional</span></span>  <br/> ||<span data-ttu-id="91c3e-171">Werte des Typs xsd: int.</span><span class="sxs-lookup"><span data-stu-id="91c3e-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="91c3e-172">Breite</span><span class="sxs-lookup"><span data-stu-id="91c3e-172">Width</span></span>  <br/> |<span data-ttu-id="91c3e-173">XSD: int</span><span class="sxs-lookup"><span data-stu-id="91c3e-173">xsd:int</span></span>  <br/> |<span data-ttu-id="91c3e-174">Optional</span><span class="sxs-lookup"><span data-stu-id="91c3e-174">optional</span></span>  <br/> ||<span data-ttu-id="91c3e-175">Werte des Typs xsd: int.</span><span class="sxs-lookup"><span data-stu-id="91c3e-175">Values of the xsd:int type.</span></span>  <br/> |
   

