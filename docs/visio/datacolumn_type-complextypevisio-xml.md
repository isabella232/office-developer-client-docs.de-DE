---
title: DataColumn_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 69f994b9516b04ddca8d26a645161772dc77c470
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344702"
---
# <a name="datacolumntype-complextype-visio-xml"></a><span data-ttu-id="7fe65-102">DataColumn_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="7fe65-102">DataColumn_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7fe65-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="7fe65-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7fe65-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7fe65-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7fe65-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="7fe65-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7fe65-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="7fe65-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7fe65-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="7fe65-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7fe65-108">Keine</span><span class="sxs-lookup"><span data-stu-id="7fe65-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7fe65-109">Definition</span><span class="sxs-lookup"><span data-stu-id="7fe65-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="7fe65-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="7fe65-110">Elements and attributes</span></span>

<span data-ttu-id="7fe65-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="7fe65-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7fe65-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7fe65-112">Child elements</span></span>

<span data-ttu-id="7fe65-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="7fe65-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7fe65-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="7fe65-114">Attributes</span></span>

|<span data-ttu-id="7fe65-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7fe65-115">**Attribute**</span></span>|<span data-ttu-id="7fe65-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="7fe65-116">**Type**</span></span>|<span data-ttu-id="7fe65-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="7fe65-117">**Required**</span></span>|<span data-ttu-id="7fe65-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7fe65-118">**Description**</span></span>|<span data-ttu-id="7fe65-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="7fe65-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7fe65-120">Kalender</span><span class="sxs-lookup"><span data-stu-id="7fe65-120">Calendar</span></span>  <br/> |<span data-ttu-id="7fe65-121">XSD: unsignedShort abgeleitet</span><span class="sxs-lookup"><span data-stu-id="7fe65-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="7fe65-122">Optional</span><span class="sxs-lookup"><span data-stu-id="7fe65-122">optional</span></span>  <br/> ||<span data-ttu-id="7fe65-123">Werte des XSD: unsignedShort abgeleitet-Typs.</span><span class="sxs-lookup"><span data-stu-id="7fe65-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="7fe65-124">ColumnName-Nr.</span><span class="sxs-lookup"><span data-stu-id="7fe65-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="7fe65-125">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7fe65-125">xsd:string</span></span>  <br/> |<span data-ttu-id="7fe65-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="7fe65-126">required</span></span>  <br/> ||<span data-ttu-id="7fe65-127">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="7fe65-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7fe65-128">Währung</span><span class="sxs-lookup"><span data-stu-id="7fe65-128">Currency</span></span>  <br/> |<span data-ttu-id="7fe65-129">XSD: unsignedShort abgeleitet</span><span class="sxs-lookup"><span data-stu-id="7fe65-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="7fe65-130">Optional</span><span class="sxs-lookup"><span data-stu-id="7fe65-130">optional</span></span>  <br/> ||<span data-ttu-id="7fe65-131">Werte des XSD: unsignedShort abgeleitet-Typs.</span><span class="sxs-lookup"><span data-stu-id="7fe65-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="7fe65-132">DataType</span><span class="sxs-lookup"><span data-stu-id="7fe65-132">DataType</span></span>  <br/> |<span data-ttu-id="7fe65-133">XSD: unsignedShort abgeleitet</span><span class="sxs-lookup"><span data-stu-id="7fe65-133">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="7fe65-134">Optional</span><span class="sxs-lookup"><span data-stu-id="7fe65-134">optional</span></span>  <br/> ||<span data-ttu-id="7fe65-135">Werte des XSD: unsignedShort abgeleitet-Typs.</span><span class="sxs-lookup"><span data-stu-id="7fe65-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="7fe65-136">Degree</span><span class="sxs-lookup"><span data-stu-id="7fe65-136">Degree</span></span>  <br/> |<span data-ttu-id="7fe65-137">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7fe65-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7fe65-138">Optional</span><span class="sxs-lookup"><span data-stu-id="7fe65-138">optional</span></span>  <br/> ||<span data-ttu-id="7fe65-139">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="7fe65-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7fe65-140">Display Order</span><span class="sxs-lookup"><span data-stu-id="7fe65-140">DisplayOrder</span></span>  <br/> |<span data-ttu-id="7fe65-141">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7fe65-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7fe65-142">Optional</span><span class="sxs-lookup"><span data-stu-id="7fe65-142">optional</span></span>  <br/> ||<span data-ttu-id="7fe65-143">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="7fe65-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7fe65-144">DisplayWidth</span><span class="sxs-lookup"><span data-stu-id="7fe65-144">DisplayWidth</span></span>  <br/> |<span data-ttu-id="7fe65-145">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7fe65-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7fe65-146">Optional</span><span class="sxs-lookup"><span data-stu-id="7fe65-146">optional</span></span>  <br/> ||<span data-ttu-id="7fe65-147">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="7fe65-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7fe65-148">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="7fe65-148">Hyperlink</span></span>  <br/> |<span data-ttu-id="7fe65-149">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="7fe65-149">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7fe65-150">Optional</span><span class="sxs-lookup"><span data-stu-id="7fe65-150">optional</span></span>  <br/> ||<span data-ttu-id="7fe65-151">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="7fe65-151">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="7fe65-152">Label</span><span class="sxs-lookup"><span data-stu-id="7fe65-152">Label</span></span>  <br/> |<span data-ttu-id="7fe65-153">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7fe65-153">xsd:string</span></span>  <br/> |<span data-ttu-id="7fe65-154">erforderlich</span><span class="sxs-lookup"><span data-stu-id="7fe65-154">required</span></span>  <br/> ||<span data-ttu-id="7fe65-155">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="7fe65-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7fe65-156">LangID</span><span class="sxs-lookup"><span data-stu-id="7fe65-156">LangID</span></span>  <br/> |<span data-ttu-id="7fe65-157">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7fe65-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7fe65-158">Optional</span><span class="sxs-lookup"><span data-stu-id="7fe65-158">optional</span></span>  <br/> ||<span data-ttu-id="7fe65-159">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="7fe65-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7fe65-160">Zugeordnet</span><span class="sxs-lookup"><span data-stu-id="7fe65-160">Mapped</span></span>  <br/> |<span data-ttu-id="7fe65-161">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="7fe65-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7fe65-162">Optional</span><span class="sxs-lookup"><span data-stu-id="7fe65-162">optional</span></span>  <br/> ||<span data-ttu-id="7fe65-163">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="7fe65-163">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="7fe65-164">Name</span><span class="sxs-lookup"><span data-stu-id="7fe65-164">Name</span></span>  <br/> |<span data-ttu-id="7fe65-165">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7fe65-165">xsd:string</span></span>  <br/> |<span data-ttu-id="7fe65-166">erforderlich</span><span class="sxs-lookup"><span data-stu-id="7fe65-166">required</span></span>  <br/> ||<span data-ttu-id="7fe65-167">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="7fe65-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7fe65-168">OrigLabel</span><span class="sxs-lookup"><span data-stu-id="7fe65-168">OrigLabel</span></span>  <br/> |<span data-ttu-id="7fe65-169">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7fe65-169">xsd:string</span></span>  <br/> |<span data-ttu-id="7fe65-170">Optional</span><span class="sxs-lookup"><span data-stu-id="7fe65-170">optional</span></span>  <br/> ||<span data-ttu-id="7fe65-171">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="7fe65-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7fe65-172">UnitType</span><span class="sxs-lookup"><span data-stu-id="7fe65-172">UnitType</span></span>  <br/> |<span data-ttu-id="7fe65-173">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7fe65-173">xsd:string</span></span>  <br/> |<span data-ttu-id="7fe65-174">Optional</span><span class="sxs-lookup"><span data-stu-id="7fe65-174">optional</span></span>  <br/> ||<span data-ttu-id="7fe65-175">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="7fe65-175">Values of the xsd:string type.</span></span>  <br/> |
   

