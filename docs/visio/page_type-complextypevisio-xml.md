---
title: Page_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4bc5c0c4-3ee3-7f63-541a-1f1854d4201c
ms.openlocfilehash: 3a0153b724539136fe142c2489badcf9895af765
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537983"
---
# <a name="pagetype-complextype-visio-xml"></a><span data-ttu-id="2611b-102">Page_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="2611b-102">Page_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="2611b-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="2611b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2611b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2611b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2611b-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="2611b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2611b-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="2611b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2611b-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="2611b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2611b-108">Keine</span><span class="sxs-lookup"><span data-stu-id="2611b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2611b-109">Definition</span><span class="sxs-lookup"><span data-stu-id="2611b-109">Definition</span></span>

```XML
          <xs:complexType name="Page_Type">
          
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
    <xs:attribute name="Background"
  type="xsd:boolean"
    />
    <xs:attribute name="BackPage"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ViewScale"
  type="xsd:double"
    />
    <xs:attribute name="ViewCenterX"
  type="xsd:double"
    />
    <xs:attribute name="ViewCenterY"
  type="xsd:double"
    />
    <xs:attribute name="ReviewerID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="AssociatedPage"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2611b-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="2611b-110">Elements and attributes</span></span>

<span data-ttu-id="2611b-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="2611b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2611b-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2611b-112">Child elements</span></span>

|<span data-ttu-id="2611b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2611b-113">**Element**</span></span>|<span data-ttu-id="2611b-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="2611b-114">**Type**</span></span>|<span data-ttu-id="2611b-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2611b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2611b-116">PageSheet</span><span class="sxs-lookup"><span data-stu-id="2611b-116">PageSheet</span></span>](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2611b-117">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="2611b-117">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="2611b-118">Rel</span><span class="sxs-lookup"><span data-stu-id="2611b-118">Rel</span></span>](rel-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2611b-119">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="2611b-119">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2611b-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="2611b-120">Attributes</span></span>

|<span data-ttu-id="2611b-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="2611b-121">**Attribute**</span></span>|<span data-ttu-id="2611b-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="2611b-122">**Type**</span></span>|<span data-ttu-id="2611b-123">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="2611b-123">**Required**</span></span>|<span data-ttu-id="2611b-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2611b-124">**Description**</span></span>|<span data-ttu-id="2611b-125">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="2611b-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2611b-126">AssociatedPage</span><span class="sxs-lookup"><span data-stu-id="2611b-126">AssociatedPage</span></span>  <br/> |<span data-ttu-id="2611b-127">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="2611b-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2611b-128">Optional</span><span class="sxs-lookup"><span data-stu-id="2611b-128">optional</span></span>  <br/> ||<span data-ttu-id="2611b-129">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="2611b-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="2611b-130">Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2611b-130">Background</span></span>  <br/> |<span data-ttu-id="2611b-131">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="2611b-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2611b-132">Optional</span><span class="sxs-lookup"><span data-stu-id="2611b-132">optional</span></span>  <br/> ||<span data-ttu-id="2611b-133">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="2611b-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2611b-134">BackPage</span><span class="sxs-lookup"><span data-stu-id="2611b-134">BackPage</span></span>  <br/> |<span data-ttu-id="2611b-135">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="2611b-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2611b-136">Optional</span><span class="sxs-lookup"><span data-stu-id="2611b-136">optional</span></span>  <br/> ||<span data-ttu-id="2611b-137">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="2611b-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="2611b-138">ID</span><span class="sxs-lookup"><span data-stu-id="2611b-138">ID</span></span>  <br/> |<span data-ttu-id="2611b-139">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="2611b-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2611b-140">erforderlich</span><span class="sxs-lookup"><span data-stu-id="2611b-140">required</span></span>  <br/> ||<span data-ttu-id="2611b-141">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="2611b-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="2611b-142">Iscustomname</span><span class="sxs-lookup"><span data-stu-id="2611b-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="2611b-143">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="2611b-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2611b-144">Optional</span><span class="sxs-lookup"><span data-stu-id="2611b-144">optional</span></span>  <br/> ||<span data-ttu-id="2611b-145">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="2611b-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2611b-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="2611b-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="2611b-147">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="2611b-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2611b-148">Optional</span><span class="sxs-lookup"><span data-stu-id="2611b-148">optional</span></span>  <br/> ||<span data-ttu-id="2611b-149">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="2611b-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2611b-150">Name</span><span class="sxs-lookup"><span data-stu-id="2611b-150">Name</span></span>  <br/> |<span data-ttu-id="2611b-151">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2611b-151">xsd:string</span></span>  <br/> |<span data-ttu-id="2611b-152">Optional</span><span class="sxs-lookup"><span data-stu-id="2611b-152">optional</span></span>  <br/> ||<span data-ttu-id="2611b-153">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="2611b-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2611b-154">NameU</span><span class="sxs-lookup"><span data-stu-id="2611b-154">NameU</span></span>  <br/> |<span data-ttu-id="2611b-155">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2611b-155">xsd:string</span></span>  <br/> |<span data-ttu-id="2611b-156">Optional</span><span class="sxs-lookup"><span data-stu-id="2611b-156">optional</span></span>  <br/> ||<span data-ttu-id="2611b-157">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="2611b-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2611b-158">ReviewerID</span><span class="sxs-lookup"><span data-stu-id="2611b-158">ReviewerID</span></span>  <br/> |<span data-ttu-id="2611b-159">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="2611b-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2611b-160">Optional</span><span class="sxs-lookup"><span data-stu-id="2611b-160">optional</span></span>  <br/> ||<span data-ttu-id="2611b-161">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="2611b-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="2611b-162">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="2611b-162">ViewCenterX</span></span>  <br/> |<span data-ttu-id="2611b-163">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="2611b-163">xsd:double</span></span>  <br/> |<span data-ttu-id="2611b-164">Optional</span><span class="sxs-lookup"><span data-stu-id="2611b-164">optional</span></span>  <br/> ||<span data-ttu-id="2611b-165">Werte des Typs XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="2611b-165">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="2611b-166">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="2611b-166">ViewCenterY</span></span>  <br/> |<span data-ttu-id="2611b-167">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="2611b-167">xsd:double</span></span>  <br/> |<span data-ttu-id="2611b-168">Optional</span><span class="sxs-lookup"><span data-stu-id="2611b-168">optional</span></span>  <br/> ||<span data-ttu-id="2611b-169">Werte des Typs XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="2611b-169">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="2611b-170">ViewScale</span><span class="sxs-lookup"><span data-stu-id="2611b-170">ViewScale</span></span>  <br/> |<span data-ttu-id="2611b-171">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="2611b-171">xsd:double</span></span>  <br/> |<span data-ttu-id="2611b-172">Optional</span><span class="sxs-lookup"><span data-stu-id="2611b-172">optional</span></span>  <br/> ||<span data-ttu-id="2611b-173">Werte des Typs XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="2611b-173">Values of the xsd:double type.</span></span>  <br/> |
   

