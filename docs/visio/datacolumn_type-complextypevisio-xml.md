---
title: DataColumn_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 69f994b9516b04ddca8d26a645161772dc77c470
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388658"
---
# <a name="datacolumntype-complextype-visio-xml"></a><span data-ttu-id="5c0a3-102">DataColumn_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="5c0a3-102">DataColumn_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="5c0a3-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="5c0a3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5c0a3-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5c0a3-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5c0a3-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="5c0a3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5c0a3-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5c0a3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5c0a3-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="5c0a3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5c0a3-108">Keine</span><span class="sxs-lookup"><span data-stu-id="5c0a3-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5c0a3-109">Definition</span><span class="sxs-lookup"><span data-stu-id="5c0a3-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="5c0a3-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="5c0a3-110">Elements and attributes</span></span>

<span data-ttu-id="5c0a3-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="5c0a3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5c0a3-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5c0a3-112">Child elements</span></span>

<span data-ttu-id="5c0a3-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="5c0a3-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5c0a3-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="5c0a3-114">Attributes</span></span>

|<span data-ttu-id="5c0a3-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="5c0a3-115">**Attribute**</span></span>|<span data-ttu-id="5c0a3-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="5c0a3-116">**Type**</span></span>|<span data-ttu-id="5c0a3-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="5c0a3-117">**Required**</span></span>|<span data-ttu-id="5c0a3-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5c0a3-118">**Description**</span></span>|<span data-ttu-id="5c0a3-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="5c0a3-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5c0a3-120">Kalender</span><span class="sxs-lookup"><span data-stu-id="5c0a3-120">Calendar</span></span>  <br/> |<span data-ttu-id="5c0a3-121">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="5c0a3-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="5c0a3-122">Optional</span><span class="sxs-lookup"><span data-stu-id="5c0a3-122">optional</span></span>  <br/> ||<span data-ttu-id="5c0a3-123">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="5c0a3-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="5c0a3-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="5c0a3-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="5c0a3-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="5c0a3-125">xsd:string</span></span>  <br/> |<span data-ttu-id="5c0a3-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="5c0a3-126">required</span></span>  <br/> ||<span data-ttu-id="5c0a3-127">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="5c0a3-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5c0a3-128">Währung</span><span class="sxs-lookup"><span data-stu-id="5c0a3-128">Currency</span></span>  <br/> |<span data-ttu-id="5c0a3-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="5c0a3-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="5c0a3-130">Optional</span><span class="sxs-lookup"><span data-stu-id="5c0a3-130">optional</span></span>  <br/> ||<span data-ttu-id="5c0a3-131">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="5c0a3-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="5c0a3-132">DataType</span><span class="sxs-lookup"><span data-stu-id="5c0a3-132">DataType</span></span>  <br/> |<span data-ttu-id="5c0a3-133">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="5c0a3-133">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="5c0a3-134">Optional</span><span class="sxs-lookup"><span data-stu-id="5c0a3-134">optional</span></span>  <br/> ||<span data-ttu-id="5c0a3-135">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="5c0a3-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="5c0a3-136">Degree</span><span class="sxs-lookup"><span data-stu-id="5c0a3-136">Degree</span></span>  <br/> |<span data-ttu-id="5c0a3-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5c0a3-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5c0a3-138">Optional</span><span class="sxs-lookup"><span data-stu-id="5c0a3-138">optional</span></span>  <br/> ||<span data-ttu-id="5c0a3-139">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5c0a3-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5c0a3-140">DisplayOrder</span><span class="sxs-lookup"><span data-stu-id="5c0a3-140">DisplayOrder</span></span>  <br/> |<span data-ttu-id="5c0a3-141">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5c0a3-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5c0a3-142">Optional</span><span class="sxs-lookup"><span data-stu-id="5c0a3-142">optional</span></span>  <br/> ||<span data-ttu-id="5c0a3-143">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5c0a3-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5c0a3-144">DisplayWidth</span><span class="sxs-lookup"><span data-stu-id="5c0a3-144">DisplayWidth</span></span>  <br/> |<span data-ttu-id="5c0a3-145">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5c0a3-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5c0a3-146">Optional</span><span class="sxs-lookup"><span data-stu-id="5c0a3-146">optional</span></span>  <br/> ||<span data-ttu-id="5c0a3-147">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5c0a3-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5c0a3-148">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="5c0a3-148">Hyperlink</span></span>  <br/> |<span data-ttu-id="5c0a3-149">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="5c0a3-149">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5c0a3-150">Optional</span><span class="sxs-lookup"><span data-stu-id="5c0a3-150">optional</span></span>  <br/> ||<span data-ttu-id="5c0a3-151">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="5c0a3-151">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="5c0a3-152">Beschriftung</span><span class="sxs-lookup"><span data-stu-id="5c0a3-152">Label</span></span>  <br/> |<span data-ttu-id="5c0a3-153">XSD: String</span><span class="sxs-lookup"><span data-stu-id="5c0a3-153">xsd:string</span></span>  <br/> |<span data-ttu-id="5c0a3-154">erforderlich</span><span class="sxs-lookup"><span data-stu-id="5c0a3-154">required</span></span>  <br/> ||<span data-ttu-id="5c0a3-155">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="5c0a3-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5c0a3-156">LangID</span><span class="sxs-lookup"><span data-stu-id="5c0a3-156">LangID</span></span>  <br/> |<span data-ttu-id="5c0a3-157">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5c0a3-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5c0a3-158">Optional</span><span class="sxs-lookup"><span data-stu-id="5c0a3-158">optional</span></span>  <br/> ||<span data-ttu-id="5c0a3-159">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5c0a3-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5c0a3-160">Zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="5c0a3-160">Mapped</span></span>  <br/> |<span data-ttu-id="5c0a3-161">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="5c0a3-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5c0a3-162">Optional</span><span class="sxs-lookup"><span data-stu-id="5c0a3-162">optional</span></span>  <br/> ||<span data-ttu-id="5c0a3-163">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="5c0a3-163">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="5c0a3-164">Name</span><span class="sxs-lookup"><span data-stu-id="5c0a3-164">Name</span></span>  <br/> |<span data-ttu-id="5c0a3-165">XSD: String</span><span class="sxs-lookup"><span data-stu-id="5c0a3-165">xsd:string</span></span>  <br/> |<span data-ttu-id="5c0a3-166">erforderlich</span><span class="sxs-lookup"><span data-stu-id="5c0a3-166">required</span></span>  <br/> ||<span data-ttu-id="5c0a3-167">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="5c0a3-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5c0a3-168">OrigLabel</span><span class="sxs-lookup"><span data-stu-id="5c0a3-168">OrigLabel</span></span>  <br/> |<span data-ttu-id="5c0a3-169">XSD: String</span><span class="sxs-lookup"><span data-stu-id="5c0a3-169">xsd:string</span></span>  <br/> |<span data-ttu-id="5c0a3-170">Optional</span><span class="sxs-lookup"><span data-stu-id="5c0a3-170">optional</span></span>  <br/> ||<span data-ttu-id="5c0a3-171">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="5c0a3-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5c0a3-172">UnitType</span><span class="sxs-lookup"><span data-stu-id="5c0a3-172">UnitType</span></span>  <br/> |<span data-ttu-id="5c0a3-173">XSD: String</span><span class="sxs-lookup"><span data-stu-id="5c0a3-173">xsd:string</span></span>  <br/> |<span data-ttu-id="5c0a3-174">Optional</span><span class="sxs-lookup"><span data-stu-id="5c0a3-174">optional</span></span>  <br/> ||<span data-ttu-id="5c0a3-175">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="5c0a3-175">Values of the xsd:string type.</span></span>  <br/> |
   

