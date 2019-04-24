---
title: Master_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d799074-13d9-3c98-3bee-b57af9966c81
ms.openlocfilehash: 186099d495849706f68113abb269de4a1f5a2ce7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341804"
---
# <a name="mastertype-complextype-visio-xml"></a><span data-ttu-id="02a0e-102">Master_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="02a0e-102">Master_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="02a0e-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="02a0e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02a0e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="02a0e-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="02a0e-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="02a0e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="02a0e-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="02a0e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="02a0e-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="02a0e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="02a0e-108">Keine</span><span class="sxs-lookup"><span data-stu-id="02a0e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="02a0e-109">Definition</span><span class="sxs-lookup"><span data-stu-id="02a0e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="02a0e-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="02a0e-110">Elements and attributes</span></span>

<span data-ttu-id="02a0e-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="02a0e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="02a0e-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="02a0e-112">Child elements</span></span>

|<span data-ttu-id="02a0e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="02a0e-113">**Element**</span></span>|<span data-ttu-id="02a0e-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="02a0e-114">**Type**</span></span>|<span data-ttu-id="02a0e-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="02a0e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="02a0e-116">Icon</span><span class="sxs-lookup"><span data-stu-id="02a0e-116">Icon</span></span>](icon-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="02a0e-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="02a0e-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="02a0e-118">PageSheet</span><span class="sxs-lookup"><span data-stu-id="02a0e-118">PageSheet</span></span>](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="02a0e-119">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="02a0e-119">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="02a0e-120">Rel</span><span class="sxs-lookup"><span data-stu-id="02a0e-120">Rel</span></span>](rel-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="02a0e-121">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="02a0e-121">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="02a0e-122">Attribute</span><span class="sxs-lookup"><span data-stu-id="02a0e-122">Attributes</span></span>

|<span data-ttu-id="02a0e-123">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="02a0e-123">**Attribute**</span></span>|<span data-ttu-id="02a0e-124">**Typ**</span><span class="sxs-lookup"><span data-stu-id="02a0e-124">**Type**</span></span>|<span data-ttu-id="02a0e-125">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="02a0e-125">**Required**</span></span>|<span data-ttu-id="02a0e-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="02a0e-126">**Description**</span></span>|<span data-ttu-id="02a0e-127">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="02a0e-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="02a0e-128">AlignName</span><span class="sxs-lookup"><span data-stu-id="02a0e-128">AlignName</span></span>  <br/> |<span data-ttu-id="02a0e-129">XSD: unsignedShort abgeleitet</span><span class="sxs-lookup"><span data-stu-id="02a0e-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="02a0e-130">Optional</span><span class="sxs-lookup"><span data-stu-id="02a0e-130">optional</span></span>  <br/> ||<span data-ttu-id="02a0e-131">Werte des XSD: unsignedShort abgeleitet-Typs.</span><span class="sxs-lookup"><span data-stu-id="02a0e-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="02a0e-132">BaseID</span><span class="sxs-lookup"><span data-stu-id="02a0e-132">BaseID</span></span>  <br/> |<span data-ttu-id="02a0e-133">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="02a0e-133">xsd:string</span></span>  <br/> |<span data-ttu-id="02a0e-134">Optional</span><span class="sxs-lookup"><span data-stu-id="02a0e-134">optional</span></span>  <br/> ||<span data-ttu-id="02a0e-135">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="02a0e-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="02a0e-136">Ausgeblendet</span><span class="sxs-lookup"><span data-stu-id="02a0e-136">Hidden</span></span>  <br/> |<span data-ttu-id="02a0e-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="02a0e-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="02a0e-138">Optional</span><span class="sxs-lookup"><span data-stu-id="02a0e-138">optional</span></span>  <br/> ||<span data-ttu-id="02a0e-139">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="02a0e-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="02a0e-140">IconSize</span><span class="sxs-lookup"><span data-stu-id="02a0e-140">IconSize</span></span>  <br/> |<span data-ttu-id="02a0e-141">XSD: unsignedShort abgeleitet</span><span class="sxs-lookup"><span data-stu-id="02a0e-141">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="02a0e-142">Optional</span><span class="sxs-lookup"><span data-stu-id="02a0e-142">optional</span></span>  <br/> ||<span data-ttu-id="02a0e-143">Werte des XSD: unsignedShort abgeleitet-Typs.</span><span class="sxs-lookup"><span data-stu-id="02a0e-143">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="02a0e-144">IconUpdate</span><span class="sxs-lookup"><span data-stu-id="02a0e-144">IconUpdate</span></span>  <br/> |<span data-ttu-id="02a0e-145">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="02a0e-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="02a0e-146">Optional</span><span class="sxs-lookup"><span data-stu-id="02a0e-146">optional</span></span>  <br/> ||<span data-ttu-id="02a0e-147">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="02a0e-147">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="02a0e-148">ID</span><span class="sxs-lookup"><span data-stu-id="02a0e-148">ID</span></span>  <br/> |<span data-ttu-id="02a0e-149">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="02a0e-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="02a0e-150">erforderlich</span><span class="sxs-lookup"><span data-stu-id="02a0e-150">required</span></span>  <br/> ||<span data-ttu-id="02a0e-151">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="02a0e-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="02a0e-152">IsCustomname</span><span class="sxs-lookup"><span data-stu-id="02a0e-152">IsCustomName</span></span>  <br/> |<span data-ttu-id="02a0e-153">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="02a0e-153">xsd:boolean</span></span>  <br/> |<span data-ttu-id="02a0e-154">Optional</span><span class="sxs-lookup"><span data-stu-id="02a0e-154">optional</span></span>  <br/> ||<span data-ttu-id="02a0e-155">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="02a0e-155">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="02a0e-156">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="02a0e-156">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="02a0e-157">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="02a0e-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="02a0e-158">Optional</span><span class="sxs-lookup"><span data-stu-id="02a0e-158">optional</span></span>  <br/> ||<span data-ttu-id="02a0e-159">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="02a0e-159">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="02a0e-160">MasterType Direktive</span><span class="sxs-lookup"><span data-stu-id="02a0e-160">MasterType</span></span>  <br/> |<span data-ttu-id="02a0e-161">XSD: unsignedShort abgeleitet</span><span class="sxs-lookup"><span data-stu-id="02a0e-161">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="02a0e-162">Optional</span><span class="sxs-lookup"><span data-stu-id="02a0e-162">optional</span></span>  <br/> ||<span data-ttu-id="02a0e-163">Werte des XSD: unsignedShort abgeleitet-Typs.</span><span class="sxs-lookup"><span data-stu-id="02a0e-163">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="02a0e-164">MatchByName</span><span class="sxs-lookup"><span data-stu-id="02a0e-164">MatchByName</span></span>  <br/> |<span data-ttu-id="02a0e-165">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="02a0e-165">xsd:boolean</span></span>  <br/> |<span data-ttu-id="02a0e-166">Optional</span><span class="sxs-lookup"><span data-stu-id="02a0e-166">optional</span></span>  <br/> ||<span data-ttu-id="02a0e-167">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="02a0e-167">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="02a0e-168">Name</span><span class="sxs-lookup"><span data-stu-id="02a0e-168">Name</span></span>  <br/> |<span data-ttu-id="02a0e-169">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="02a0e-169">xsd:string</span></span>  <br/> |<span data-ttu-id="02a0e-170">Optional</span><span class="sxs-lookup"><span data-stu-id="02a0e-170">optional</span></span>  <br/> ||<span data-ttu-id="02a0e-171">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="02a0e-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="02a0e-172">NameU</span><span class="sxs-lookup"><span data-stu-id="02a0e-172">NameU</span></span>  <br/> |<span data-ttu-id="02a0e-173">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="02a0e-173">xsd:string</span></span>  <br/> |<span data-ttu-id="02a0e-174">Optional</span><span class="sxs-lookup"><span data-stu-id="02a0e-174">optional</span></span>  <br/> ||<span data-ttu-id="02a0e-175">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="02a0e-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="02a0e-176">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="02a0e-176">PatternFlags</span></span>  <br/> |<span data-ttu-id="02a0e-177">XSD: unsignedShort abgeleitet</span><span class="sxs-lookup"><span data-stu-id="02a0e-177">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="02a0e-178">Optional</span><span class="sxs-lookup"><span data-stu-id="02a0e-178">optional</span></span>  <br/> ||<span data-ttu-id="02a0e-179">Werte des XSD: unsignedShort abgeleitet-Typs.</span><span class="sxs-lookup"><span data-stu-id="02a0e-179">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="02a0e-180">Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="02a0e-180">Prompt</span></span>  <br/> |<span data-ttu-id="02a0e-181">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="02a0e-181">xsd:string</span></span>  <br/> |<span data-ttu-id="02a0e-182">Optional</span><span class="sxs-lookup"><span data-stu-id="02a0e-182">optional</span></span>  <br/> ||<span data-ttu-id="02a0e-183">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="02a0e-183">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="02a0e-184">UniqueID</span><span class="sxs-lookup"><span data-stu-id="02a0e-184">UniqueID</span></span>  <br/> |<span data-ttu-id="02a0e-185">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="02a0e-185">xsd:string</span></span>  <br/> |<span data-ttu-id="02a0e-186">Optional</span><span class="sxs-lookup"><span data-stu-id="02a0e-186">optional</span></span>  <br/> ||<span data-ttu-id="02a0e-187">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="02a0e-187">Values of the xsd:string type.</span></span>  <br/> |
   

