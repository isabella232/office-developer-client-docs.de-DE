---
title: MasterShortcut_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0192c733-09b8-d9ce-1d88-b4d97e2e1a36
ms.openlocfilehash: 23d5de92be151b9ab6819296456746087573e7c0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396484"
---
# <a name="mastershortcuttype-complextype-visio-xml"></a><span data-ttu-id="001f7-102">MasterShortcut_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="001f7-102">MasterShortcut_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="001f7-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="001f7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="001f7-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="001f7-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="001f7-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="001f7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="001f7-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="001f7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="001f7-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="001f7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="001f7-108">Keine</span><span class="sxs-lookup"><span data-stu-id="001f7-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="001f7-109">Definition</span><span class="sxs-lookup"><span data-stu-id="001f7-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="001f7-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="001f7-110">Elements and attributes</span></span>

<span data-ttu-id="001f7-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="001f7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="001f7-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="001f7-112">Child elements</span></span>

|<span data-ttu-id="001f7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="001f7-113">**Element**</span></span>|<span data-ttu-id="001f7-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="001f7-114">**Type**</span></span>|<span data-ttu-id="001f7-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="001f7-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="001f7-116">Icon</span><span class="sxs-lookup"><span data-stu-id="001f7-116">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="001f7-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="001f7-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="001f7-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="001f7-118">Attributes</span></span>

|<span data-ttu-id="001f7-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="001f7-119">**Attribute**</span></span>|<span data-ttu-id="001f7-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="001f7-120">**Type**</span></span>|<span data-ttu-id="001f7-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="001f7-121">**Required**</span></span>|<span data-ttu-id="001f7-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="001f7-122">**Description**</span></span>|<span data-ttu-id="001f7-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="001f7-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="001f7-124">AlignName</span><span class="sxs-lookup"><span data-stu-id="001f7-124">AlignName</span></span>  <br/> |<span data-ttu-id="001f7-125">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="001f7-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="001f7-126">Optional</span><span class="sxs-lookup"><span data-stu-id="001f7-126">optional</span></span>  <br/> ||<span data-ttu-id="001f7-127">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="001f7-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="001f7-128">IconSize</span><span class="sxs-lookup"><span data-stu-id="001f7-128">IconSize</span></span>  <br/> |<span data-ttu-id="001f7-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="001f7-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="001f7-130">Optional</span><span class="sxs-lookup"><span data-stu-id="001f7-130">optional</span></span>  <br/> ||<span data-ttu-id="001f7-131">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="001f7-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="001f7-132">ID</span><span class="sxs-lookup"><span data-stu-id="001f7-132">ID</span></span>  <br/> |<span data-ttu-id="001f7-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="001f7-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="001f7-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="001f7-134">required</span></span>  <br/> ||<span data-ttu-id="001f7-135">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="001f7-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="001f7-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="001f7-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="001f7-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="001f7-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="001f7-138">Optional</span><span class="sxs-lookup"><span data-stu-id="001f7-138">optional</span></span>  <br/> ||<span data-ttu-id="001f7-139">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="001f7-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="001f7-140">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="001f7-140">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="001f7-141">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="001f7-141">xsd:boolean</span></span>  <br/> |<span data-ttu-id="001f7-142">Optional</span><span class="sxs-lookup"><span data-stu-id="001f7-142">optional</span></span>  <br/> ||<span data-ttu-id="001f7-143">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="001f7-143">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="001f7-144">MasterType</span><span class="sxs-lookup"><span data-stu-id="001f7-144">MasterType</span></span>  <br/> |<span data-ttu-id="001f7-145">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="001f7-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="001f7-146">Optional</span><span class="sxs-lookup"><span data-stu-id="001f7-146">optional</span></span>  <br/> ||<span data-ttu-id="001f7-147">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="001f7-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="001f7-148">Name</span><span class="sxs-lookup"><span data-stu-id="001f7-148">Name</span></span>  <br/> |<span data-ttu-id="001f7-149">XSD: String</span><span class="sxs-lookup"><span data-stu-id="001f7-149">xsd:string</span></span>  <br/> |<span data-ttu-id="001f7-150">Optional</span><span class="sxs-lookup"><span data-stu-id="001f7-150">optional</span></span>  <br/> ||<span data-ttu-id="001f7-151">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="001f7-151">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="001f7-152">NameU</span><span class="sxs-lookup"><span data-stu-id="001f7-152">NameU</span></span>  <br/> |<span data-ttu-id="001f7-153">XSD: String</span><span class="sxs-lookup"><span data-stu-id="001f7-153">xsd:string</span></span>  <br/> |<span data-ttu-id="001f7-154">Optional</span><span class="sxs-lookup"><span data-stu-id="001f7-154">optional</span></span>  <br/> ||<span data-ttu-id="001f7-155">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="001f7-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="001f7-156">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="001f7-156">PatternFlags</span></span>  <br/> |<span data-ttu-id="001f7-157">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="001f7-157">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="001f7-158">Optional</span><span class="sxs-lookup"><span data-stu-id="001f7-158">optional</span></span>  <br/> ||<span data-ttu-id="001f7-159">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="001f7-159">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="001f7-160">Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="001f7-160">Prompt</span></span>  <br/> |<span data-ttu-id="001f7-161">XSD: String</span><span class="sxs-lookup"><span data-stu-id="001f7-161">xsd:string</span></span>  <br/> |<span data-ttu-id="001f7-162">Optional</span><span class="sxs-lookup"><span data-stu-id="001f7-162">optional</span></span>  <br/> ||<span data-ttu-id="001f7-163">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="001f7-163">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="001f7-164">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="001f7-164">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="001f7-165">XSD: String</span><span class="sxs-lookup"><span data-stu-id="001f7-165">xsd:string</span></span>  <br/> |<span data-ttu-id="001f7-166">Optional</span><span class="sxs-lookup"><span data-stu-id="001f7-166">optional</span></span>  <br/> ||<span data-ttu-id="001f7-167">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="001f7-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="001f7-168">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="001f7-168">ShortcutURL</span></span>  <br/> |<span data-ttu-id="001f7-169">XSD: String</span><span class="sxs-lookup"><span data-stu-id="001f7-169">xsd:string</span></span>  <br/> |<span data-ttu-id="001f7-170">Optional</span><span class="sxs-lookup"><span data-stu-id="001f7-170">optional</span></span>  <br/> ||<span data-ttu-id="001f7-171">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="001f7-171">Values of the xsd:string type.</span></span>  <br/> |
   

