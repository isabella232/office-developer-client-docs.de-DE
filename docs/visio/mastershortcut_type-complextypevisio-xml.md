---
title: MasterShortcut_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0192c733-09b8-d9ce-1d88-b4d97e2e1a36
ms.openlocfilehash: 23d5de92be151b9ab6819296456746087573e7c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341692"
---
# <a name="mastershortcuttype-complextype-visio-xml"></a><span data-ttu-id="4080c-102">MasterShortcut_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="4080c-102">MasterShortcut_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4080c-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="4080c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4080c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4080c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4080c-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="4080c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4080c-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="4080c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4080c-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="4080c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4080c-108">Keine</span><span class="sxs-lookup"><span data-stu-id="4080c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4080c-109">Definition</span><span class="sxs-lookup"><span data-stu-id="4080c-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="4080c-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="4080c-110">Elements and attributes</span></span>

<span data-ttu-id="4080c-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="4080c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4080c-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4080c-112">Child elements</span></span>

|<span data-ttu-id="4080c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4080c-113">**Element**</span></span>|<span data-ttu-id="4080c-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4080c-114">**Type**</span></span>|<span data-ttu-id="4080c-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4080c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4080c-116">Icon</span><span class="sxs-lookup"><span data-stu-id="4080c-116">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4080c-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="4080c-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4080c-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="4080c-118">Attributes</span></span>

|<span data-ttu-id="4080c-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4080c-119">**Attribute**</span></span>|<span data-ttu-id="4080c-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4080c-120">**Type**</span></span>|<span data-ttu-id="4080c-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="4080c-121">**Required**</span></span>|<span data-ttu-id="4080c-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4080c-122">**Description**</span></span>|<span data-ttu-id="4080c-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="4080c-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4080c-124">AlignName</span><span class="sxs-lookup"><span data-stu-id="4080c-124">AlignName</span></span>  <br/> |<span data-ttu-id="4080c-125">XSD: unsignedShort abgeleitet</span><span class="sxs-lookup"><span data-stu-id="4080c-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="4080c-126">Optional</span><span class="sxs-lookup"><span data-stu-id="4080c-126">optional</span></span>  <br/> ||<span data-ttu-id="4080c-127">Werte des XSD: unsignedShort abgeleitet-Typs.</span><span class="sxs-lookup"><span data-stu-id="4080c-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="4080c-128">IconSize</span><span class="sxs-lookup"><span data-stu-id="4080c-128">IconSize</span></span>  <br/> |<span data-ttu-id="4080c-129">XSD: unsignedShort abgeleitet</span><span class="sxs-lookup"><span data-stu-id="4080c-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="4080c-130">Optional</span><span class="sxs-lookup"><span data-stu-id="4080c-130">optional</span></span>  <br/> ||<span data-ttu-id="4080c-131">Werte des XSD: unsignedShort abgeleitet-Typs.</span><span class="sxs-lookup"><span data-stu-id="4080c-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="4080c-132">ID</span><span class="sxs-lookup"><span data-stu-id="4080c-132">ID</span></span>  <br/> |<span data-ttu-id="4080c-133">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4080c-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4080c-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="4080c-134">required</span></span>  <br/> ||<span data-ttu-id="4080c-135">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="4080c-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4080c-136">IsCustomname</span><span class="sxs-lookup"><span data-stu-id="4080c-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="4080c-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="4080c-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4080c-138">Optional</span><span class="sxs-lookup"><span data-stu-id="4080c-138">optional</span></span>  <br/> ||<span data-ttu-id="4080c-139">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="4080c-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="4080c-140">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="4080c-140">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="4080c-141">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="4080c-141">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4080c-142">Optional</span><span class="sxs-lookup"><span data-stu-id="4080c-142">optional</span></span>  <br/> ||<span data-ttu-id="4080c-143">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="4080c-143">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="4080c-144">MasterType Direktive</span><span class="sxs-lookup"><span data-stu-id="4080c-144">MasterType</span></span>  <br/> |<span data-ttu-id="4080c-145">XSD: unsignedShort abgeleitet</span><span class="sxs-lookup"><span data-stu-id="4080c-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="4080c-146">Optional</span><span class="sxs-lookup"><span data-stu-id="4080c-146">optional</span></span>  <br/> ||<span data-ttu-id="4080c-147">Werte des XSD: unsignedShort abgeleitet-Typs.</span><span class="sxs-lookup"><span data-stu-id="4080c-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="4080c-148">Name</span><span class="sxs-lookup"><span data-stu-id="4080c-148">Name</span></span>  <br/> |<span data-ttu-id="4080c-149">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4080c-149">xsd:string</span></span>  <br/> |<span data-ttu-id="4080c-150">Optional</span><span class="sxs-lookup"><span data-stu-id="4080c-150">optional</span></span>  <br/> ||<span data-ttu-id="4080c-151">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="4080c-151">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4080c-152">NameU</span><span class="sxs-lookup"><span data-stu-id="4080c-152">NameU</span></span>  <br/> |<span data-ttu-id="4080c-153">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4080c-153">xsd:string</span></span>  <br/> |<span data-ttu-id="4080c-154">Optional</span><span class="sxs-lookup"><span data-stu-id="4080c-154">optional</span></span>  <br/> ||<span data-ttu-id="4080c-155">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="4080c-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4080c-156">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="4080c-156">PatternFlags</span></span>  <br/> |<span data-ttu-id="4080c-157">XSD: unsignedShort abgeleitet</span><span class="sxs-lookup"><span data-stu-id="4080c-157">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="4080c-158">Optional</span><span class="sxs-lookup"><span data-stu-id="4080c-158">optional</span></span>  <br/> ||<span data-ttu-id="4080c-159">Werte des XSD: unsignedShort abgeleitet-Typs.</span><span class="sxs-lookup"><span data-stu-id="4080c-159">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="4080c-160">Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="4080c-160">Prompt</span></span>  <br/> |<span data-ttu-id="4080c-161">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4080c-161">xsd:string</span></span>  <br/> |<span data-ttu-id="4080c-162">Optional</span><span class="sxs-lookup"><span data-stu-id="4080c-162">optional</span></span>  <br/> ||<span data-ttu-id="4080c-163">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="4080c-163">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4080c-164">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="4080c-164">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="4080c-165">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4080c-165">xsd:string</span></span>  <br/> |<span data-ttu-id="4080c-166">Optional</span><span class="sxs-lookup"><span data-stu-id="4080c-166">optional</span></span>  <br/> ||<span data-ttu-id="4080c-167">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="4080c-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4080c-168">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="4080c-168">ShortcutURL</span></span>  <br/> |<span data-ttu-id="4080c-169">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4080c-169">xsd:string</span></span>  <br/> |<span data-ttu-id="4080c-170">Optional</span><span class="sxs-lookup"><span data-stu-id="4080c-170">optional</span></span>  <br/> ||<span data-ttu-id="4080c-171">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="4080c-171">Values of the xsd:string type.</span></span>  <br/> |
   

