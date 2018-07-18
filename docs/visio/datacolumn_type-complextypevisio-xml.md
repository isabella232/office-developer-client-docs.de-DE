---
title: DataColumn_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 9d334190b686f3b2c5e25a31336c668c957e820f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796779"
---
# <a name="datacolumntype-complextype-visio-xml"></a><span data-ttu-id="154ef-102">DataColumn_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="154ef-102">DataColumn_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="154ef-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="154ef-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="154ef-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="154ef-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="154ef-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="154ef-105">**Schema file**</span></span> <br/> |<span data-ttu-id="154ef-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="154ef-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="154ef-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="154ef-107">**Extension base**</span></span> <br/> |<span data-ttu-id="154ef-108">Keine</span><span class="sxs-lookup"><span data-stu-id="154ef-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="154ef-109">Definition</span><span class="sxs-lookup"><span data-stu-id="154ef-109">Definition</span></span>

```XML
      <xs:complexType name="DataColumn_Type">
    <xs:attribute name="ColumnNameID"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Label"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="OrigLabel"
  type="xsd:string"
    />
    <xs:attribute name="LangID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Calendar"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="DataType"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="UnitType"
  type="xsd:string"
    />
    <xs:attribute name="Currency"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="Degree"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DisplayWidth"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DisplayOrder"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Mapped"
  type="xsd:boolean"
    />
    <xs:attribute name="Hyperlink"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="154ef-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="154ef-110">Elements and attributes</span></span>

<span data-ttu-id="154ef-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="154ef-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="154ef-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="154ef-112">Child elements</span></span>

<span data-ttu-id="154ef-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="154ef-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="154ef-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="154ef-114">Attributes</span></span>

|<span data-ttu-id="154ef-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="154ef-115">**Attribute**</span></span>|<span data-ttu-id="154ef-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="154ef-116">**Type**</span></span>|<span data-ttu-id="154ef-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="154ef-117">**Required**</span></span>|<span data-ttu-id="154ef-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="154ef-118">**Description**</span></span>|<span data-ttu-id="154ef-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="154ef-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="154ef-120">Kalender</span><span class="sxs-lookup"><span data-stu-id="154ef-120">Calendar</span></span>  <br/> |<span data-ttu-id="154ef-121">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="154ef-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="154ef-122">Optional</span><span class="sxs-lookup"><span data-stu-id="154ef-122">optional</span></span>  <br/> ||<span data-ttu-id="154ef-123">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="154ef-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="154ef-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="154ef-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="154ef-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="154ef-125">xsd:string</span></span>  <br/> |<span data-ttu-id="154ef-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="154ef-126">required</span></span>  <br/> ||<span data-ttu-id="154ef-127">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="154ef-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="154ef-128">Währung</span><span class="sxs-lookup"><span data-stu-id="154ef-128">Currency</span></span>  <br/> |<span data-ttu-id="154ef-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="154ef-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="154ef-130">Optional</span><span class="sxs-lookup"><span data-stu-id="154ef-130">optional</span></span>  <br/> ||<span data-ttu-id="154ef-131">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="154ef-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="154ef-132">DataType</span><span class="sxs-lookup"><span data-stu-id="154ef-132">DataType</span></span>  <br/> |<span data-ttu-id="154ef-133">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="154ef-133">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="154ef-134">Optional</span><span class="sxs-lookup"><span data-stu-id="154ef-134">optional</span></span>  <br/> ||<span data-ttu-id="154ef-135">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="154ef-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="154ef-136">Degree</span><span class="sxs-lookup"><span data-stu-id="154ef-136">Degree</span></span>  <br/> |<span data-ttu-id="154ef-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="154ef-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="154ef-138">Optional</span><span class="sxs-lookup"><span data-stu-id="154ef-138">optional</span></span>  <br/> ||<span data-ttu-id="154ef-139">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="154ef-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="154ef-140">DisplayOrder</span><span class="sxs-lookup"><span data-stu-id="154ef-140">DisplayOrder</span></span>  <br/> |<span data-ttu-id="154ef-141">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="154ef-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="154ef-142">Optional</span><span class="sxs-lookup"><span data-stu-id="154ef-142">optional</span></span>  <br/> ||<span data-ttu-id="154ef-143">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="154ef-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="154ef-144">DisplayWidth</span><span class="sxs-lookup"><span data-stu-id="154ef-144">DisplayWidth</span></span>  <br/> |<span data-ttu-id="154ef-145">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="154ef-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="154ef-146">Optional</span><span class="sxs-lookup"><span data-stu-id="154ef-146">optional</span></span>  <br/> ||<span data-ttu-id="154ef-147">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="154ef-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="154ef-148">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="154ef-148">Hyperlink</span></span>  <br/> |<span data-ttu-id="154ef-149">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="154ef-149">xsd:boolean</span></span>  <br/> |<span data-ttu-id="154ef-150">Optional</span><span class="sxs-lookup"><span data-stu-id="154ef-150">optional</span></span>  <br/> ||<span data-ttu-id="154ef-151">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="154ef-151">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="154ef-152">Beschriftung</span><span class="sxs-lookup"><span data-stu-id="154ef-152">Label</span></span>  <br/> |<span data-ttu-id="154ef-153">XSD: String</span><span class="sxs-lookup"><span data-stu-id="154ef-153">xsd:string</span></span>  <br/> |<span data-ttu-id="154ef-154">erforderlich</span><span class="sxs-lookup"><span data-stu-id="154ef-154">required</span></span>  <br/> ||<span data-ttu-id="154ef-155">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="154ef-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="154ef-156">LangID</span><span class="sxs-lookup"><span data-stu-id="154ef-156">LangID</span></span>  <br/> |<span data-ttu-id="154ef-157">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="154ef-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="154ef-158">Optional</span><span class="sxs-lookup"><span data-stu-id="154ef-158">optional</span></span>  <br/> ||<span data-ttu-id="154ef-159">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="154ef-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="154ef-160">Zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="154ef-160">Mapped</span></span>  <br/> |<span data-ttu-id="154ef-161">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="154ef-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="154ef-162">Optional</span><span class="sxs-lookup"><span data-stu-id="154ef-162">optional</span></span>  <br/> ||<span data-ttu-id="154ef-163">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="154ef-163">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="154ef-164">Name</span><span class="sxs-lookup"><span data-stu-id="154ef-164">Name</span></span>  <br/> |<span data-ttu-id="154ef-165">XSD: String</span><span class="sxs-lookup"><span data-stu-id="154ef-165">xsd:string</span></span>  <br/> |<span data-ttu-id="154ef-166">erforderlich</span><span class="sxs-lookup"><span data-stu-id="154ef-166">required</span></span>  <br/> ||<span data-ttu-id="154ef-167">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="154ef-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="154ef-168">OrigLabel</span><span class="sxs-lookup"><span data-stu-id="154ef-168">OrigLabel</span></span>  <br/> |<span data-ttu-id="154ef-169">XSD: String</span><span class="sxs-lookup"><span data-stu-id="154ef-169">xsd:string</span></span>  <br/> |<span data-ttu-id="154ef-170">Optional</span><span class="sxs-lookup"><span data-stu-id="154ef-170">optional</span></span>  <br/> ||<span data-ttu-id="154ef-171">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="154ef-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="154ef-172">UnitType</span><span class="sxs-lookup"><span data-stu-id="154ef-172">UnitType</span></span>  <br/> |<span data-ttu-id="154ef-173">XSD: String</span><span class="sxs-lookup"><span data-stu-id="154ef-173">xsd:string</span></span>  <br/> |<span data-ttu-id="154ef-174">Optional</span><span class="sxs-lookup"><span data-stu-id="154ef-174">optional</span></span>  <br/> ||<span data-ttu-id="154ef-175">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="154ef-175">Values of the xsd:string type.</span></span>  <br/> |
   

