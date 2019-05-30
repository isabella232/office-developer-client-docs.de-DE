---
title: DataColumn_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 7f35cd2ef1f6d710644033599fe4a90a0f2978ef
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541211"
---
# <a name="datacolumntype-complextype-visio-xml"></a><span data-ttu-id="c903d-102">DataColumn_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c903d-102">DataColumn_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="c903d-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="c903d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c903d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c903d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c903d-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="c903d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c903d-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="c903d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c903d-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="c903d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c903d-108">Keine</span><span class="sxs-lookup"><span data-stu-id="c903d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c903d-109">Definition</span><span class="sxs-lookup"><span data-stu-id="c903d-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c903d-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="c903d-110">Elements and attributes</span></span>

<span data-ttu-id="c903d-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="c903d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c903d-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c903d-112">Child elements</span></span>

<span data-ttu-id="c903d-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="c903d-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c903d-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="c903d-114">Attributes</span></span>

|<span data-ttu-id="c903d-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c903d-115">**Attribute**</span></span>|<span data-ttu-id="c903d-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c903d-116">**Type**</span></span>|<span data-ttu-id="c903d-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="c903d-117">**Required**</span></span>|<span data-ttu-id="c903d-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c903d-118">**Description**</span></span>|<span data-ttu-id="c903d-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="c903d-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c903d-120">Kalender</span><span class="sxs-lookup"><span data-stu-id="c903d-120">Calendar</span></span>  <br/> |<span data-ttu-id="c903d-121">XSD: unsignedShort abgeleitet</span><span class="sxs-lookup"><span data-stu-id="c903d-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c903d-122">Optional</span><span class="sxs-lookup"><span data-stu-id="c903d-122">optional</span></span>  <br/> ||<span data-ttu-id="c903d-123">Werte des XSD: unsignedShort abgeleitet-Typs.</span><span class="sxs-lookup"><span data-stu-id="c903d-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c903d-124">Spaltenname</span><span class="sxs-lookup"><span data-stu-id="c903d-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="c903d-125">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c903d-125">xsd:string</span></span>  <br/> |<span data-ttu-id="c903d-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="c903d-126">required</span></span>  <br/> ||<span data-ttu-id="c903d-127">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="c903d-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c903d-128">Währung</span><span class="sxs-lookup"><span data-stu-id="c903d-128">Currency</span></span>  <br/> |<span data-ttu-id="c903d-129">XSD: unsignedShort abgeleitet</span><span class="sxs-lookup"><span data-stu-id="c903d-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c903d-130">Optional</span><span class="sxs-lookup"><span data-stu-id="c903d-130">optional</span></span>  <br/> ||<span data-ttu-id="c903d-131">Werte des XSD: unsignedShort abgeleitet-Typs.</span><span class="sxs-lookup"><span data-stu-id="c903d-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c903d-132">DataType</span><span class="sxs-lookup"><span data-stu-id="c903d-132">DataType</span></span>  <br/> |<span data-ttu-id="c903d-133">XSD: unsignedShort abgeleitet</span><span class="sxs-lookup"><span data-stu-id="c903d-133">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c903d-134">Optional</span><span class="sxs-lookup"><span data-stu-id="c903d-134">optional</span></span>  <br/> ||<span data-ttu-id="c903d-135">Werte des XSD: unsignedShort abgeleitet-Typs.</span><span class="sxs-lookup"><span data-stu-id="c903d-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c903d-136">Degree</span><span class="sxs-lookup"><span data-stu-id="c903d-136">Degree</span></span>  <br/> |<span data-ttu-id="c903d-137">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c903d-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c903d-138">Optional</span><span class="sxs-lookup"><span data-stu-id="c903d-138">optional</span></span>  <br/> ||<span data-ttu-id="c903d-139">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="c903d-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c903d-140">Display Order</span><span class="sxs-lookup"><span data-stu-id="c903d-140">DisplayOrder</span></span>  <br/> |<span data-ttu-id="c903d-141">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c903d-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c903d-142">Optional</span><span class="sxs-lookup"><span data-stu-id="c903d-142">optional</span></span>  <br/> ||<span data-ttu-id="c903d-143">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="c903d-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c903d-144">DisplayWidth</span><span class="sxs-lookup"><span data-stu-id="c903d-144">DisplayWidth</span></span>  <br/> |<span data-ttu-id="c903d-145">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c903d-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c903d-146">Optional</span><span class="sxs-lookup"><span data-stu-id="c903d-146">optional</span></span>  <br/> ||<span data-ttu-id="c903d-147">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="c903d-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c903d-148">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="c903d-148">Hyperlink</span></span>  <br/> |<span data-ttu-id="c903d-149">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="c903d-149">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c903d-150">Optional</span><span class="sxs-lookup"><span data-stu-id="c903d-150">optional</span></span>  <br/> ||<span data-ttu-id="c903d-151">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="c903d-151">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c903d-152">Label</span><span class="sxs-lookup"><span data-stu-id="c903d-152">Label</span></span>  <br/> |<span data-ttu-id="c903d-153">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c903d-153">xsd:string</span></span>  <br/> |<span data-ttu-id="c903d-154">erforderlich</span><span class="sxs-lookup"><span data-stu-id="c903d-154">required</span></span>  <br/> ||<span data-ttu-id="c903d-155">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="c903d-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c903d-156">LangID</span><span class="sxs-lookup"><span data-stu-id="c903d-156">LangID</span></span>  <br/> |<span data-ttu-id="c903d-157">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c903d-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c903d-158">Optional</span><span class="sxs-lookup"><span data-stu-id="c903d-158">optional</span></span>  <br/> ||<span data-ttu-id="c903d-159">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="c903d-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c903d-160">Zugeordnet</span><span class="sxs-lookup"><span data-stu-id="c903d-160">Mapped</span></span>  <br/> |<span data-ttu-id="c903d-161">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="c903d-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c903d-162">Optional</span><span class="sxs-lookup"><span data-stu-id="c903d-162">optional</span></span>  <br/> ||<span data-ttu-id="c903d-163">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="c903d-163">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c903d-164">Name</span><span class="sxs-lookup"><span data-stu-id="c903d-164">Name</span></span>  <br/> |<span data-ttu-id="c903d-165">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c903d-165">xsd:string</span></span>  <br/> |<span data-ttu-id="c903d-166">erforderlich</span><span class="sxs-lookup"><span data-stu-id="c903d-166">required</span></span>  <br/> ||<span data-ttu-id="c903d-167">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="c903d-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c903d-168">OrigLabel</span><span class="sxs-lookup"><span data-stu-id="c903d-168">OrigLabel</span></span>  <br/> |<span data-ttu-id="c903d-169">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c903d-169">xsd:string</span></span>  <br/> |<span data-ttu-id="c903d-170">Optional</span><span class="sxs-lookup"><span data-stu-id="c903d-170">optional</span></span>  <br/> ||<span data-ttu-id="c903d-171">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="c903d-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c903d-172">UnitType</span><span class="sxs-lookup"><span data-stu-id="c903d-172">UnitType</span></span>  <br/> |<span data-ttu-id="c903d-173">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c903d-173">xsd:string</span></span>  <br/> |<span data-ttu-id="c903d-174">Optional</span><span class="sxs-lookup"><span data-stu-id="c903d-174">optional</span></span>  <br/> ||<span data-ttu-id="c903d-175">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="c903d-175">Values of the xsd:string type.</span></span>  <br/> |
   

