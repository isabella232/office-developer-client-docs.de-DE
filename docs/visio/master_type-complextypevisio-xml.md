---
title: Master_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d799074-13d9-3c98-3bee-b57af9966c81
ms.openlocfilehash: b4dde4d00552525a5ec17116f96151f39c6d0957
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797443"
---
# <a name="mastertype-complextype-visio-xml"></a><span data-ttu-id="4ca62-102">Master_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="4ca62-102">Master_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4ca62-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="4ca62-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ca62-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4ca62-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4ca62-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="4ca62-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4ca62-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4ca62-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4ca62-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="4ca62-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4ca62-108">Keine</span><span class="sxs-lookup"><span data-stu-id="4ca62-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4ca62-109">Definition</span><span class="sxs-lookup"><span data-stu-id="4ca62-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="4ca62-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="4ca62-110">Elements and attributes</span></span>

<span data-ttu-id="4ca62-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="4ca62-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4ca62-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4ca62-112">Child elements</span></span>

|<span data-ttu-id="4ca62-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4ca62-113">**Element**</span></span>|<span data-ttu-id="4ca62-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4ca62-114">**Type**</span></span>|<span data-ttu-id="4ca62-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4ca62-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4ca62-116">Icon</span><span class="sxs-lookup"><span data-stu-id="4ca62-116">Icon</span></span>](icon-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4ca62-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="4ca62-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4ca62-118">PageSheet</span><span class="sxs-lookup"><span data-stu-id="4ca62-118">PageSheet</span></span>](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4ca62-119">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="4ca62-119">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4ca62-120">Rel</span><span class="sxs-lookup"><span data-stu-id="4ca62-120">Rel</span></span>](rel-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4ca62-121">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="4ca62-121">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4ca62-122">Attribute</span><span class="sxs-lookup"><span data-stu-id="4ca62-122">Attributes</span></span>

|<span data-ttu-id="4ca62-123">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4ca62-123">**Attribute**</span></span>|<span data-ttu-id="4ca62-124">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4ca62-124">**Type**</span></span>|<span data-ttu-id="4ca62-125">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="4ca62-125">**Required**</span></span>|<span data-ttu-id="4ca62-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4ca62-126">**Description**</span></span>|<span data-ttu-id="4ca62-127">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="4ca62-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4ca62-128">AlignName</span><span class="sxs-lookup"><span data-stu-id="4ca62-128">AlignName</span></span>  <br/> |<span data-ttu-id="4ca62-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="4ca62-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="4ca62-130">Optional</span><span class="sxs-lookup"><span data-stu-id="4ca62-130">optional</span></span>  <br/> ||<span data-ttu-id="4ca62-131">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="4ca62-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="4ca62-132">BaseID</span><span class="sxs-lookup"><span data-stu-id="4ca62-132">BaseID</span></span>  <br/> |<span data-ttu-id="4ca62-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="4ca62-133">xsd:string</span></span>  <br/> |<span data-ttu-id="4ca62-134">Optional</span><span class="sxs-lookup"><span data-stu-id="4ca62-134">optional</span></span>  <br/> ||<span data-ttu-id="4ca62-135">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4ca62-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4ca62-136">Ausgeblendet</span><span class="sxs-lookup"><span data-stu-id="4ca62-136">Hidden</span></span>  <br/> |<span data-ttu-id="4ca62-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="4ca62-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4ca62-138">Optional</span><span class="sxs-lookup"><span data-stu-id="4ca62-138">optional</span></span>  <br/> ||<span data-ttu-id="4ca62-139">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="4ca62-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="4ca62-140">IconSize</span><span class="sxs-lookup"><span data-stu-id="4ca62-140">IconSize</span></span>  <br/> |<span data-ttu-id="4ca62-141">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="4ca62-141">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="4ca62-142">Optional</span><span class="sxs-lookup"><span data-stu-id="4ca62-142">optional</span></span>  <br/> ||<span data-ttu-id="4ca62-143">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="4ca62-143">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="4ca62-144">IconUpdate</span><span class="sxs-lookup"><span data-stu-id="4ca62-144">IconUpdate</span></span>  <br/> |<span data-ttu-id="4ca62-145">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="4ca62-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4ca62-146">Optional</span><span class="sxs-lookup"><span data-stu-id="4ca62-146">optional</span></span>  <br/> ||<span data-ttu-id="4ca62-147">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="4ca62-147">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="4ca62-148">ID</span><span class="sxs-lookup"><span data-stu-id="4ca62-148">ID</span></span>  <br/> |<span data-ttu-id="4ca62-149">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4ca62-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4ca62-150">erforderlich</span><span class="sxs-lookup"><span data-stu-id="4ca62-150">required</span></span>  <br/> ||<span data-ttu-id="4ca62-151">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4ca62-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4ca62-152">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="4ca62-152">IsCustomName</span></span>  <br/> |<span data-ttu-id="4ca62-153">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="4ca62-153">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4ca62-154">Optional</span><span class="sxs-lookup"><span data-stu-id="4ca62-154">optional</span></span>  <br/> ||<span data-ttu-id="4ca62-155">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="4ca62-155">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="4ca62-156">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="4ca62-156">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="4ca62-157">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="4ca62-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4ca62-158">Optional</span><span class="sxs-lookup"><span data-stu-id="4ca62-158">optional</span></span>  <br/> ||<span data-ttu-id="4ca62-159">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="4ca62-159">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="4ca62-160">MasterType</span><span class="sxs-lookup"><span data-stu-id="4ca62-160">MasterType</span></span>  <br/> |<span data-ttu-id="4ca62-161">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="4ca62-161">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="4ca62-162">Optional</span><span class="sxs-lookup"><span data-stu-id="4ca62-162">optional</span></span>  <br/> ||<span data-ttu-id="4ca62-163">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="4ca62-163">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="4ca62-164">MatchByName</span><span class="sxs-lookup"><span data-stu-id="4ca62-164">MatchByName</span></span>  <br/> |<span data-ttu-id="4ca62-165">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="4ca62-165">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4ca62-166">Optional</span><span class="sxs-lookup"><span data-stu-id="4ca62-166">optional</span></span>  <br/> ||<span data-ttu-id="4ca62-167">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="4ca62-167">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="4ca62-168">Name</span><span class="sxs-lookup"><span data-stu-id="4ca62-168">Name</span></span>  <br/> |<span data-ttu-id="4ca62-169">XSD: String</span><span class="sxs-lookup"><span data-stu-id="4ca62-169">xsd:string</span></span>  <br/> |<span data-ttu-id="4ca62-170">Optional</span><span class="sxs-lookup"><span data-stu-id="4ca62-170">optional</span></span>  <br/> ||<span data-ttu-id="4ca62-171">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4ca62-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4ca62-172">NameU</span><span class="sxs-lookup"><span data-stu-id="4ca62-172">NameU</span></span>  <br/> |<span data-ttu-id="4ca62-173">XSD: String</span><span class="sxs-lookup"><span data-stu-id="4ca62-173">xsd:string</span></span>  <br/> |<span data-ttu-id="4ca62-174">Optional</span><span class="sxs-lookup"><span data-stu-id="4ca62-174">optional</span></span>  <br/> ||<span data-ttu-id="4ca62-175">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4ca62-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4ca62-176">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="4ca62-176">PatternFlags</span></span>  <br/> |<span data-ttu-id="4ca62-177">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="4ca62-177">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="4ca62-178">Optional</span><span class="sxs-lookup"><span data-stu-id="4ca62-178">optional</span></span>  <br/> ||<span data-ttu-id="4ca62-179">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="4ca62-179">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="4ca62-180">Prompt</span><span class="sxs-lookup"><span data-stu-id="4ca62-180">Prompt</span></span>  <br/> |<span data-ttu-id="4ca62-181">XSD: String</span><span class="sxs-lookup"><span data-stu-id="4ca62-181">xsd:string</span></span>  <br/> |<span data-ttu-id="4ca62-182">Optional</span><span class="sxs-lookup"><span data-stu-id="4ca62-182">optional</span></span>  <br/> ||<span data-ttu-id="4ca62-183">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4ca62-183">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4ca62-184">UniqueID</span><span class="sxs-lookup"><span data-stu-id="4ca62-184">UniqueID</span></span>  <br/> |<span data-ttu-id="4ca62-185">XSD: String</span><span class="sxs-lookup"><span data-stu-id="4ca62-185">xsd:string</span></span>  <br/> |<span data-ttu-id="4ca62-186">Optional</span><span class="sxs-lookup"><span data-stu-id="4ca62-186">optional</span></span>  <br/> ||<span data-ttu-id="4ca62-187">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4ca62-187">Values of the xsd:string type.</span></span>  <br/> |
   

