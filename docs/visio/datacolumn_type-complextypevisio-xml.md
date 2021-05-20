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
# <a name="datacolumn_type-complextype-visio-xml"></a><span data-ttu-id="ff01f-102">DataColumn_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ff01f-102">DataColumn_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="ff01f-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="ff01f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff01f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ff01f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ff01f-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="ff01f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ff01f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ff01f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ff01f-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="ff01f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ff01f-108">Keine</span><span class="sxs-lookup"><span data-stu-id="ff01f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ff01f-109">Definition</span><span class="sxs-lookup"><span data-stu-id="ff01f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ff01f-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="ff01f-110">Elements and attributes</span></span>

<span data-ttu-id="ff01f-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="ff01f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ff01f-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ff01f-112">Child elements</span></span>

<span data-ttu-id="ff01f-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="ff01f-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ff01f-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="ff01f-114">Attributes</span></span>

|<span data-ttu-id="ff01f-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ff01f-115">**Attribute**</span></span>|<span data-ttu-id="ff01f-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ff01f-116">**Type**</span></span>|<span data-ttu-id="ff01f-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="ff01f-117">**Required**</span></span>|<span data-ttu-id="ff01f-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ff01f-118">**Description**</span></span>|<span data-ttu-id="ff01f-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="ff01f-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ff01f-120">Kalender</span><span class="sxs-lookup"><span data-stu-id="ff01f-120">Calendar</span></span>  <br/> |<span data-ttu-id="ff01f-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ff01f-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ff01f-122">Optional</span><span class="sxs-lookup"><span data-stu-id="ff01f-122">optional</span></span>  <br/> ||<span data-ttu-id="ff01f-123">Werte des Typs xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="ff01f-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="ff01f-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="ff01f-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="ff01f-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ff01f-125">xsd:string</span></span>  <br/> |<span data-ttu-id="ff01f-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="ff01f-126">required</span></span>  <br/> ||<span data-ttu-id="ff01f-127">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="ff01f-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ff01f-128">Währung</span><span class="sxs-lookup"><span data-stu-id="ff01f-128">Currency</span></span>  <br/> |<span data-ttu-id="ff01f-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ff01f-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ff01f-130">Optional</span><span class="sxs-lookup"><span data-stu-id="ff01f-130">optional</span></span>  <br/> ||<span data-ttu-id="ff01f-131">Werte des Typs xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="ff01f-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="ff01f-132">DataType</span><span class="sxs-lookup"><span data-stu-id="ff01f-132">DataType</span></span>  <br/> |<span data-ttu-id="ff01f-133">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ff01f-133">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ff01f-134">Optional</span><span class="sxs-lookup"><span data-stu-id="ff01f-134">optional</span></span>  <br/> ||<span data-ttu-id="ff01f-135">Werte des Typs xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="ff01f-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="ff01f-136">Degree</span><span class="sxs-lookup"><span data-stu-id="ff01f-136">Degree</span></span>  <br/> |<span data-ttu-id="ff01f-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ff01f-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ff01f-138">Optional</span><span class="sxs-lookup"><span data-stu-id="ff01f-138">optional</span></span>  <br/> ||<span data-ttu-id="ff01f-139">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="ff01f-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ff01f-140">DisplayOrder</span><span class="sxs-lookup"><span data-stu-id="ff01f-140">DisplayOrder</span></span>  <br/> |<span data-ttu-id="ff01f-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ff01f-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ff01f-142">Optional</span><span class="sxs-lookup"><span data-stu-id="ff01f-142">optional</span></span>  <br/> ||<span data-ttu-id="ff01f-143">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="ff01f-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ff01f-144">DisplayWidth</span><span class="sxs-lookup"><span data-stu-id="ff01f-144">DisplayWidth</span></span>  <br/> |<span data-ttu-id="ff01f-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ff01f-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ff01f-146">Optional</span><span class="sxs-lookup"><span data-stu-id="ff01f-146">optional</span></span>  <br/> ||<span data-ttu-id="ff01f-147">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="ff01f-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ff01f-148">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="ff01f-148">Hyperlink</span></span>  <br/> |<span data-ttu-id="ff01f-149">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="ff01f-149">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ff01f-150">Optional</span><span class="sxs-lookup"><span data-stu-id="ff01f-150">optional</span></span>  <br/> ||<span data-ttu-id="ff01f-151">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="ff01f-151">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ff01f-152">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="ff01f-152">Label</span></span>  <br/> |<span data-ttu-id="ff01f-153">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ff01f-153">xsd:string</span></span>  <br/> |<span data-ttu-id="ff01f-154">erforderlich</span><span class="sxs-lookup"><span data-stu-id="ff01f-154">required</span></span>  <br/> ||<span data-ttu-id="ff01f-155">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="ff01f-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ff01f-156">LangID</span><span class="sxs-lookup"><span data-stu-id="ff01f-156">LangID</span></span>  <br/> |<span data-ttu-id="ff01f-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ff01f-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ff01f-158">Optional</span><span class="sxs-lookup"><span data-stu-id="ff01f-158">optional</span></span>  <br/> ||<span data-ttu-id="ff01f-159">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="ff01f-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ff01f-160">Zugeordnet</span><span class="sxs-lookup"><span data-stu-id="ff01f-160">Mapped</span></span>  <br/> |<span data-ttu-id="ff01f-161">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="ff01f-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ff01f-162">Optional</span><span class="sxs-lookup"><span data-stu-id="ff01f-162">optional</span></span>  <br/> ||<span data-ttu-id="ff01f-163">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="ff01f-163">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ff01f-164">Name</span><span class="sxs-lookup"><span data-stu-id="ff01f-164">Name</span></span>  <br/> |<span data-ttu-id="ff01f-165">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ff01f-165">xsd:string</span></span>  <br/> |<span data-ttu-id="ff01f-166">erforderlich</span><span class="sxs-lookup"><span data-stu-id="ff01f-166">required</span></span>  <br/> ||<span data-ttu-id="ff01f-167">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="ff01f-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ff01f-168">OrigLabel</span><span class="sxs-lookup"><span data-stu-id="ff01f-168">OrigLabel</span></span>  <br/> |<span data-ttu-id="ff01f-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ff01f-169">xsd:string</span></span>  <br/> |<span data-ttu-id="ff01f-170">Optional</span><span class="sxs-lookup"><span data-stu-id="ff01f-170">optional</span></span>  <br/> ||<span data-ttu-id="ff01f-171">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="ff01f-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ff01f-172">UnitType</span><span class="sxs-lookup"><span data-stu-id="ff01f-172">UnitType</span></span>  <br/> |<span data-ttu-id="ff01f-173">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ff01f-173">xsd:string</span></span>  <br/> |<span data-ttu-id="ff01f-174">Optional</span><span class="sxs-lookup"><span data-stu-id="ff01f-174">optional</span></span>  <br/> ||<span data-ttu-id="ff01f-175">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="ff01f-175">Values of the xsd:string type.</span></span>  <br/> |
   

