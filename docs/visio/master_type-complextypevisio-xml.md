---
title: Master_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d799074-13d9-3c98-3bee-b57af9966c81
ms.openlocfilehash: 22b619149fc5393f085ca6e245c65ed6058538ae
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538067"
---
# <a name="master_type-complextype-visio-xml"></a><span data-ttu-id="aa06b-102">Master_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="aa06b-102">Master_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="aa06b-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="aa06b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aa06b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="aa06b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="aa06b-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="aa06b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="aa06b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="aa06b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="aa06b-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="aa06b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="aa06b-108">Keine</span><span class="sxs-lookup"><span data-stu-id="aa06b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="aa06b-109">Definition</span><span class="sxs-lookup"><span data-stu-id="aa06b-109">Definition</span></span>

```XML
          <xs:complexType name="Master_Type">
          
          <xs:all>
    <xs:element name="PageSheet"  type="PageSheet_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Icon"  type="Icon_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="BaseID"
  type="xsd:string"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
    <xs:attribute name="MatchByName"
  type="xsd:boolean"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="IconSize"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="PatternFlags"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="Prompt"
  type="xsd:string"
    />
    <xs:attribute name="Hidden"
  type="xsd:boolean"
    />
    <xs:attribute name="IconUpdate"
  type="xsd:boolean"
    />
    <xs:attribute name="AlignName"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="MasterType"
  type="xsd:unsignedShort"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="aa06b-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="aa06b-110">Elements and attributes</span></span>

<span data-ttu-id="aa06b-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="aa06b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="aa06b-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aa06b-112">Child elements</span></span>

|<span data-ttu-id="aa06b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="aa06b-113">**Element**</span></span>|<span data-ttu-id="aa06b-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="aa06b-114">**Type**</span></span>|<span data-ttu-id="aa06b-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aa06b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="aa06b-116">Icon</span><span class="sxs-lookup"><span data-stu-id="aa06b-116">Icon</span></span>](icon-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="aa06b-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="aa06b-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="aa06b-118">PageSheet</span><span class="sxs-lookup"><span data-stu-id="aa06b-118">PageSheet</span></span>](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="aa06b-119">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="aa06b-119">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="aa06b-120">Rel</span><span class="sxs-lookup"><span data-stu-id="aa06b-120">Rel</span></span>](rel-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="aa06b-121">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="aa06b-121">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="aa06b-122">Attribute</span><span class="sxs-lookup"><span data-stu-id="aa06b-122">Attributes</span></span>

|<span data-ttu-id="aa06b-123">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="aa06b-123">**Attribute**</span></span>|<span data-ttu-id="aa06b-124">**Typ**</span><span class="sxs-lookup"><span data-stu-id="aa06b-124">**Type**</span></span>|<span data-ttu-id="aa06b-125">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="aa06b-125">**Required**</span></span>|<span data-ttu-id="aa06b-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aa06b-126">**Description**</span></span>|<span data-ttu-id="aa06b-127">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="aa06b-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="aa06b-128">AlignName</span><span class="sxs-lookup"><span data-stu-id="aa06b-128">AlignName</span></span>  <br/> |<span data-ttu-id="aa06b-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="aa06b-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="aa06b-130">Optional</span><span class="sxs-lookup"><span data-stu-id="aa06b-130">optional</span></span>  <br/> ||<span data-ttu-id="aa06b-131">Werte des Typs xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="aa06b-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="aa06b-132">BaseID</span><span class="sxs-lookup"><span data-stu-id="aa06b-132">BaseID</span></span>  <br/> |<span data-ttu-id="aa06b-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="aa06b-133">xsd:string</span></span>  <br/> |<span data-ttu-id="aa06b-134">Optional</span><span class="sxs-lookup"><span data-stu-id="aa06b-134">optional</span></span>  <br/> ||<span data-ttu-id="aa06b-135">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="aa06b-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="aa06b-136">Hidden</span><span class="sxs-lookup"><span data-stu-id="aa06b-136">Hidden</span></span>  <br/> |<span data-ttu-id="aa06b-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="aa06b-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="aa06b-138">Optional</span><span class="sxs-lookup"><span data-stu-id="aa06b-138">optional</span></span>  <br/> ||<span data-ttu-id="aa06b-139">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="aa06b-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="aa06b-140">IconSize</span><span class="sxs-lookup"><span data-stu-id="aa06b-140">IconSize</span></span>  <br/> |<span data-ttu-id="aa06b-141">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="aa06b-141">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="aa06b-142">Optional</span><span class="sxs-lookup"><span data-stu-id="aa06b-142">optional</span></span>  <br/> ||<span data-ttu-id="aa06b-143">Werte des Typs xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="aa06b-143">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="aa06b-144">IconUpdate</span><span class="sxs-lookup"><span data-stu-id="aa06b-144">IconUpdate</span></span>  <br/> |<span data-ttu-id="aa06b-145">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="aa06b-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="aa06b-146">Optional</span><span class="sxs-lookup"><span data-stu-id="aa06b-146">optional</span></span>  <br/> ||<span data-ttu-id="aa06b-147">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="aa06b-147">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="aa06b-148">ID</span><span class="sxs-lookup"><span data-stu-id="aa06b-148">ID</span></span>  <br/> |<span data-ttu-id="aa06b-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="aa06b-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="aa06b-150">erforderlich</span><span class="sxs-lookup"><span data-stu-id="aa06b-150">required</span></span>  <br/> ||<span data-ttu-id="aa06b-151">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="aa06b-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="aa06b-152">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="aa06b-152">IsCustomName</span></span>  <br/> |<span data-ttu-id="aa06b-153">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="aa06b-153">xsd:boolean</span></span>  <br/> |<span data-ttu-id="aa06b-154">Optional</span><span class="sxs-lookup"><span data-stu-id="aa06b-154">optional</span></span>  <br/> ||<span data-ttu-id="aa06b-155">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="aa06b-155">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="aa06b-156">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="aa06b-156">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="aa06b-157">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="aa06b-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="aa06b-158">Optional</span><span class="sxs-lookup"><span data-stu-id="aa06b-158">optional</span></span>  <br/> ||<span data-ttu-id="aa06b-159">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="aa06b-159">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="aa06b-160">MasterType</span><span class="sxs-lookup"><span data-stu-id="aa06b-160">MasterType</span></span>  <br/> |<span data-ttu-id="aa06b-161">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="aa06b-161">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="aa06b-162">Optional</span><span class="sxs-lookup"><span data-stu-id="aa06b-162">optional</span></span>  <br/> ||<span data-ttu-id="aa06b-163">Werte des Typs xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="aa06b-163">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="aa06b-164">MatchByName</span><span class="sxs-lookup"><span data-stu-id="aa06b-164">MatchByName</span></span>  <br/> |<span data-ttu-id="aa06b-165">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="aa06b-165">xsd:boolean</span></span>  <br/> |<span data-ttu-id="aa06b-166">Optional</span><span class="sxs-lookup"><span data-stu-id="aa06b-166">optional</span></span>  <br/> ||<span data-ttu-id="aa06b-167">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="aa06b-167">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="aa06b-168">Name</span><span class="sxs-lookup"><span data-stu-id="aa06b-168">Name</span></span>  <br/> |<span data-ttu-id="aa06b-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="aa06b-169">xsd:string</span></span>  <br/> |<span data-ttu-id="aa06b-170">Optional</span><span class="sxs-lookup"><span data-stu-id="aa06b-170">optional</span></span>  <br/> ||<span data-ttu-id="aa06b-171">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="aa06b-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="aa06b-172">NameU</span><span class="sxs-lookup"><span data-stu-id="aa06b-172">NameU</span></span>  <br/> |<span data-ttu-id="aa06b-173">xsd:string</span><span class="sxs-lookup"><span data-stu-id="aa06b-173">xsd:string</span></span>  <br/> |<span data-ttu-id="aa06b-174">Optional</span><span class="sxs-lookup"><span data-stu-id="aa06b-174">optional</span></span>  <br/> ||<span data-ttu-id="aa06b-175">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="aa06b-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="aa06b-176">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="aa06b-176">PatternFlags</span></span>  <br/> |<span data-ttu-id="aa06b-177">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="aa06b-177">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="aa06b-178">Optional</span><span class="sxs-lookup"><span data-stu-id="aa06b-178">optional</span></span>  <br/> ||<span data-ttu-id="aa06b-179">Werte des Typs xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="aa06b-179">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="aa06b-180">Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="aa06b-180">Prompt</span></span>  <br/> |<span data-ttu-id="aa06b-181">xsd:string</span><span class="sxs-lookup"><span data-stu-id="aa06b-181">xsd:string</span></span>  <br/> |<span data-ttu-id="aa06b-182">Optional</span><span class="sxs-lookup"><span data-stu-id="aa06b-182">optional</span></span>  <br/> ||<span data-ttu-id="aa06b-183">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="aa06b-183">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="aa06b-184">UniqueID</span><span class="sxs-lookup"><span data-stu-id="aa06b-184">UniqueID</span></span>  <br/> |<span data-ttu-id="aa06b-185">xsd:string</span><span class="sxs-lookup"><span data-stu-id="aa06b-185">xsd:string</span></span>  <br/> |<span data-ttu-id="aa06b-186">Optional</span><span class="sxs-lookup"><span data-stu-id="aa06b-186">optional</span></span>  <br/> ||<span data-ttu-id="aa06b-187">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="aa06b-187">Values of the xsd:string type.</span></span>  <br/> |
   

