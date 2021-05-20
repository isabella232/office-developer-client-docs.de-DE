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
# <a name="headerfooterfont_type-complextype-visio-xml"></a><span data-ttu-id="dde93-102">HeaderFooterFont_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="dde93-102">HeaderFooterFont_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="dde93-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="dde93-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dde93-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="dde93-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="dde93-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="dde93-105">**Schema file**</span></span> <br/> |<span data-ttu-id="dde93-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="dde93-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="dde93-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="dde93-107">**Extension base**</span></span> <br/> |<span data-ttu-id="dde93-108">Keine</span><span class="sxs-lookup"><span data-stu-id="dde93-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dde93-109">Definition</span><span class="sxs-lookup"><span data-stu-id="dde93-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="dde93-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="dde93-110">Elements and attributes</span></span>

<span data-ttu-id="dde93-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="dde93-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="dde93-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dde93-112">Child elements</span></span>

<span data-ttu-id="dde93-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="dde93-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dde93-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="dde93-114">Attributes</span></span>

|<span data-ttu-id="dde93-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="dde93-115">**Attribute**</span></span>|<span data-ttu-id="dde93-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="dde93-116">**Type**</span></span>|<span data-ttu-id="dde93-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="dde93-117">**Required**</span></span>|<span data-ttu-id="dde93-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dde93-118">**Description**</span></span>|<span data-ttu-id="dde93-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="dde93-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="dde93-120">CharSet</span><span class="sxs-lookup"><span data-stu-id="dde93-120">CharSet</span></span>  <br/> |<span data-ttu-id="dde93-121">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="dde93-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="dde93-122">Optional</span><span class="sxs-lookup"><span data-stu-id="dde93-122">optional</span></span>  <br/> ||<span data-ttu-id="dde93-123">Werte des xsd:unsignedByte-Typs.</span><span class="sxs-lookup"><span data-stu-id="dde93-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="dde93-124">ClipPrecision</span><span class="sxs-lookup"><span data-stu-id="dde93-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="dde93-125">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="dde93-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="dde93-126">Optional</span><span class="sxs-lookup"><span data-stu-id="dde93-126">optional</span></span>  <br/> ||<span data-ttu-id="dde93-127">Werte des xsd:unsignedByte-Typs.</span><span class="sxs-lookup"><span data-stu-id="dde93-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="dde93-128">Escapement</span><span class="sxs-lookup"><span data-stu-id="dde93-128">Escapement</span></span>  <br/> |<span data-ttu-id="dde93-129">xsd:int</span><span class="sxs-lookup"><span data-stu-id="dde93-129">xsd:int</span></span>  <br/> |<span data-ttu-id="dde93-130">Optional</span><span class="sxs-lookup"><span data-stu-id="dde93-130">optional</span></span>  <br/> ||<span data-ttu-id="dde93-131">Werte des xsd:int-Typs.</span><span class="sxs-lookup"><span data-stu-id="dde93-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="dde93-132">FaceName</span><span class="sxs-lookup"><span data-stu-id="dde93-132">FaceName</span></span>  <br/> |<span data-ttu-id="dde93-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="dde93-133">xsd:string</span></span>  <br/> |<span data-ttu-id="dde93-134">Optional</span><span class="sxs-lookup"><span data-stu-id="dde93-134">optional</span></span>  <br/> ||<span data-ttu-id="dde93-135">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="dde93-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="dde93-136">Height</span><span class="sxs-lookup"><span data-stu-id="dde93-136">Height</span></span>  <br/> |<span data-ttu-id="dde93-137">xsd:int</span><span class="sxs-lookup"><span data-stu-id="dde93-137">xsd:int</span></span>  <br/> |<span data-ttu-id="dde93-138">Optional</span><span class="sxs-lookup"><span data-stu-id="dde93-138">optional</span></span>  <br/> ||<span data-ttu-id="dde93-139">Werte des xsd:int-Typs.</span><span class="sxs-lookup"><span data-stu-id="dde93-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="dde93-140">Kursiv</span><span class="sxs-lookup"><span data-stu-id="dde93-140">Italic</span></span>  <br/> |<span data-ttu-id="dde93-141">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="dde93-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="dde93-142">Optional</span><span class="sxs-lookup"><span data-stu-id="dde93-142">optional</span></span>  <br/> ||<span data-ttu-id="dde93-143">Werte des xsd:unsignedByte-Typs.</span><span class="sxs-lookup"><span data-stu-id="dde93-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="dde93-144">Orientierung</span><span class="sxs-lookup"><span data-stu-id="dde93-144">Orientation</span></span>  <br/> |<span data-ttu-id="dde93-145">xsd:int</span><span class="sxs-lookup"><span data-stu-id="dde93-145">xsd:int</span></span>  <br/> |<span data-ttu-id="dde93-146">Optional</span><span class="sxs-lookup"><span data-stu-id="dde93-146">optional</span></span>  <br/> ||<span data-ttu-id="dde93-147">Werte des xsd:int-Typs.</span><span class="sxs-lookup"><span data-stu-id="dde93-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="dde93-148">OutPrecision</span><span class="sxs-lookup"><span data-stu-id="dde93-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="dde93-149">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="dde93-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="dde93-150">Optional</span><span class="sxs-lookup"><span data-stu-id="dde93-150">optional</span></span>  <br/> ||<span data-ttu-id="dde93-151">Werte des xsd:unsignedByte-Typs.</span><span class="sxs-lookup"><span data-stu-id="dde93-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="dde93-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="dde93-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="dde93-153">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="dde93-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="dde93-154">Optional</span><span class="sxs-lookup"><span data-stu-id="dde93-154">optional</span></span>  <br/> ||<span data-ttu-id="dde93-155">Werte des xsd:unsignedByte-Typs.</span><span class="sxs-lookup"><span data-stu-id="dde93-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="dde93-156">Qualität</span><span class="sxs-lookup"><span data-stu-id="dde93-156">Quality</span></span>  <br/> |<span data-ttu-id="dde93-157">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="dde93-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="dde93-158">Optional</span><span class="sxs-lookup"><span data-stu-id="dde93-158">optional</span></span>  <br/> ||<span data-ttu-id="dde93-159">Werte des xsd:unsignedByte-Typs.</span><span class="sxs-lookup"><span data-stu-id="dde93-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="dde93-160">StrikeOut</span><span class="sxs-lookup"><span data-stu-id="dde93-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="dde93-161">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="dde93-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="dde93-162">Optional</span><span class="sxs-lookup"><span data-stu-id="dde93-162">optional</span></span>  <br/> ||<span data-ttu-id="dde93-163">Werte des xsd:unsignedByte-Typs.</span><span class="sxs-lookup"><span data-stu-id="dde93-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="dde93-164">Unterstrichen</span><span class="sxs-lookup"><span data-stu-id="dde93-164">Underline</span></span>  <br/> |<span data-ttu-id="dde93-165">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="dde93-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="dde93-166">Optional</span><span class="sxs-lookup"><span data-stu-id="dde93-166">optional</span></span>  <br/> ||<span data-ttu-id="dde93-167">Werte des xsd:unsignedByte-Typs.</span><span class="sxs-lookup"><span data-stu-id="dde93-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="dde93-168">Schriftbreite</span><span class="sxs-lookup"><span data-stu-id="dde93-168">Weight</span></span>  <br/> |<span data-ttu-id="dde93-169">xsd:int</span><span class="sxs-lookup"><span data-stu-id="dde93-169">xsd:int</span></span>  <br/> |<span data-ttu-id="dde93-170">Optional</span><span class="sxs-lookup"><span data-stu-id="dde93-170">optional</span></span>  <br/> ||<span data-ttu-id="dde93-171">Werte des xsd:int-Typs.</span><span class="sxs-lookup"><span data-stu-id="dde93-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="dde93-172">Width</span><span class="sxs-lookup"><span data-stu-id="dde93-172">Width</span></span>  <br/> |<span data-ttu-id="dde93-173">xsd:int</span><span class="sxs-lookup"><span data-stu-id="dde93-173">xsd:int</span></span>  <br/> |<span data-ttu-id="dde93-174">Optional</span><span class="sxs-lookup"><span data-stu-id="dde93-174">optional</span></span>  <br/> ||<span data-ttu-id="dde93-175">Werte des xsd:int-Typs.</span><span class="sxs-lookup"><span data-stu-id="dde93-175">Values of the xsd:int type.</span></span>  <br/> |
   

