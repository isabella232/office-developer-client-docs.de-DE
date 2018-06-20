---
title: MasterShortcut_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0192c733-09b8-d9ce-1d88-b4d97e2e1a36
ms.openlocfilehash: df1e10ff11470cd87fc16efbaba6ad968df6d1b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797459"
---
# <a name="mastershortcuttype-complextype-visio-xml"></a><span data-ttu-id="bfb6a-102">MasterShortcut_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="bfb6a-102">MasterShortcut_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="bfb6a-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="bfb6a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bfb6a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bfb6a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bfb6a-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="bfb6a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bfb6a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="bfb6a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bfb6a-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="bfb6a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bfb6a-108">Keine</span><span class="sxs-lookup"><span data-stu-id="bfb6a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bfb6a-109">Definition</span><span class="sxs-lookup"><span data-stu-id="bfb6a-109">Definition</span></span>

```XML
          <xs:complexType name="MasterShortcut_Type">
          
          <xs:all>
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
    <xs:attribute name="ShortcutURL"
  type="xsd:string"
    />
    <xs:attribute name="ShortcutHelp"
  type="xsd:string"
    />
    <xs:attribute name="AlignName"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="MasterType"
  type="xsd:unsignedShort"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bfb6a-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="bfb6a-110">Elements and attributes</span></span>

<span data-ttu-id="bfb6a-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="bfb6a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bfb6a-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bfb6a-112">Child elements</span></span>

|<span data-ttu-id="bfb6a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="bfb6a-113">**Element**</span></span>|<span data-ttu-id="bfb6a-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="bfb6a-114">**Type**</span></span>|<span data-ttu-id="bfb6a-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bfb6a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bfb6a-116">Icon</span><span class="sxs-lookup"><span data-stu-id="bfb6a-116">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bfb6a-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="bfb6a-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="bfb6a-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="bfb6a-118">Attributes</span></span>

|<span data-ttu-id="bfb6a-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="bfb6a-119">**Attribute**</span></span>|<span data-ttu-id="bfb6a-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="bfb6a-120">**Type**</span></span>|<span data-ttu-id="bfb6a-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="bfb6a-121">**Required**</span></span>|<span data-ttu-id="bfb6a-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bfb6a-122">**Description**</span></span>|<span data-ttu-id="bfb6a-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="bfb6a-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bfb6a-124">AlignName</span><span class="sxs-lookup"><span data-stu-id="bfb6a-124">AlignName</span></span>  <br/> |<span data-ttu-id="bfb6a-125">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="bfb6a-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="bfb6a-126">Optional</span><span class="sxs-lookup"><span data-stu-id="bfb6a-126">optional</span></span>  <br/> ||<span data-ttu-id="bfb6a-127">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="bfb6a-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="bfb6a-128">IconSize</span><span class="sxs-lookup"><span data-stu-id="bfb6a-128">IconSize</span></span>  <br/> |<span data-ttu-id="bfb6a-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="bfb6a-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="bfb6a-130">Optional</span><span class="sxs-lookup"><span data-stu-id="bfb6a-130">optional</span></span>  <br/> ||<span data-ttu-id="bfb6a-131">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="bfb6a-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="bfb6a-132">ID</span><span class="sxs-lookup"><span data-stu-id="bfb6a-132">ID</span></span>  <br/> |<span data-ttu-id="bfb6a-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bfb6a-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bfb6a-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="bfb6a-134">required</span></span>  <br/> ||<span data-ttu-id="bfb6a-135">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bfb6a-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bfb6a-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="bfb6a-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="bfb6a-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="bfb6a-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="bfb6a-138">Optional</span><span class="sxs-lookup"><span data-stu-id="bfb6a-138">optional</span></span>  <br/> ||<span data-ttu-id="bfb6a-139">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="bfb6a-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="bfb6a-140">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="bfb6a-140">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="bfb6a-141">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="bfb6a-141">xsd:boolean</span></span>  <br/> |<span data-ttu-id="bfb6a-142">Optional</span><span class="sxs-lookup"><span data-stu-id="bfb6a-142">optional</span></span>  <br/> ||<span data-ttu-id="bfb6a-143">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="bfb6a-143">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="bfb6a-144">MasterType</span><span class="sxs-lookup"><span data-stu-id="bfb6a-144">MasterType</span></span>  <br/> |<span data-ttu-id="bfb6a-145">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="bfb6a-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="bfb6a-146">Optional</span><span class="sxs-lookup"><span data-stu-id="bfb6a-146">optional</span></span>  <br/> ||<span data-ttu-id="bfb6a-147">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="bfb6a-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="bfb6a-148">Name</span><span class="sxs-lookup"><span data-stu-id="bfb6a-148">Name</span></span>  <br/> |<span data-ttu-id="bfb6a-149">XSD: String</span><span class="sxs-lookup"><span data-stu-id="bfb6a-149">xsd:string</span></span>  <br/> |<span data-ttu-id="bfb6a-150">Optional</span><span class="sxs-lookup"><span data-stu-id="bfb6a-150">optional</span></span>  <br/> ||<span data-ttu-id="bfb6a-151">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="bfb6a-151">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bfb6a-152">NameU</span><span class="sxs-lookup"><span data-stu-id="bfb6a-152">NameU</span></span>  <br/> |<span data-ttu-id="bfb6a-153">XSD: String</span><span class="sxs-lookup"><span data-stu-id="bfb6a-153">xsd:string</span></span>  <br/> |<span data-ttu-id="bfb6a-154">Optional</span><span class="sxs-lookup"><span data-stu-id="bfb6a-154">optional</span></span>  <br/> ||<span data-ttu-id="bfb6a-155">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="bfb6a-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bfb6a-156">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="bfb6a-156">PatternFlags</span></span>  <br/> |<span data-ttu-id="bfb6a-157">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="bfb6a-157">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="bfb6a-158">Optional</span><span class="sxs-lookup"><span data-stu-id="bfb6a-158">optional</span></span>  <br/> ||<span data-ttu-id="bfb6a-159">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="bfb6a-159">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="bfb6a-160">Prompt</span><span class="sxs-lookup"><span data-stu-id="bfb6a-160">Prompt</span></span>  <br/> |<span data-ttu-id="bfb6a-161">XSD: String</span><span class="sxs-lookup"><span data-stu-id="bfb6a-161">xsd:string</span></span>  <br/> |<span data-ttu-id="bfb6a-162">Optional</span><span class="sxs-lookup"><span data-stu-id="bfb6a-162">optional</span></span>  <br/> ||<span data-ttu-id="bfb6a-163">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="bfb6a-163">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bfb6a-164">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="bfb6a-164">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="bfb6a-165">XSD: String</span><span class="sxs-lookup"><span data-stu-id="bfb6a-165">xsd:string</span></span>  <br/> |<span data-ttu-id="bfb6a-166">Optional</span><span class="sxs-lookup"><span data-stu-id="bfb6a-166">optional</span></span>  <br/> ||<span data-ttu-id="bfb6a-167">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="bfb6a-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bfb6a-168">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="bfb6a-168">ShortcutURL</span></span>  <br/> |<span data-ttu-id="bfb6a-169">XSD: String</span><span class="sxs-lookup"><span data-stu-id="bfb6a-169">xsd:string</span></span>  <br/> |<span data-ttu-id="bfb6a-170">Optional</span><span class="sxs-lookup"><span data-stu-id="bfb6a-170">optional</span></span>  <br/> ||<span data-ttu-id="bfb6a-171">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="bfb6a-171">Values of the xsd:string type.</span></span>  <br/> |
   

