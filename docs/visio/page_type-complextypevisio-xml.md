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
# <a name="page_type-complextype-visio-xml"></a><span data-ttu-id="92087-102">Page_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="92087-102">Page_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="92087-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="92087-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92087-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="92087-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="92087-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="92087-105">**Schema file**</span></span> <br/> |<span data-ttu-id="92087-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="92087-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="92087-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="92087-107">**Extension base**</span></span> <br/> |<span data-ttu-id="92087-108">Keine</span><span class="sxs-lookup"><span data-stu-id="92087-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="92087-109">Definition</span><span class="sxs-lookup"><span data-stu-id="92087-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="92087-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="92087-110">Elements and attributes</span></span>

<span data-ttu-id="92087-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="92087-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="92087-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="92087-112">Child elements</span></span>

|<span data-ttu-id="92087-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="92087-113">**Element**</span></span>|<span data-ttu-id="92087-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="92087-114">**Type**</span></span>|<span data-ttu-id="92087-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="92087-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="92087-116">PageSheet</span><span class="sxs-lookup"><span data-stu-id="92087-116">PageSheet</span></span>](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="92087-117">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="92087-117">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="92087-118">Rel</span><span class="sxs-lookup"><span data-stu-id="92087-118">Rel</span></span>](rel-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="92087-119">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="92087-119">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="92087-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="92087-120">Attributes</span></span>

|<span data-ttu-id="92087-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="92087-121">**Attribute**</span></span>|<span data-ttu-id="92087-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="92087-122">**Type**</span></span>|<span data-ttu-id="92087-123">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="92087-123">**Required**</span></span>|<span data-ttu-id="92087-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="92087-124">**Description**</span></span>|<span data-ttu-id="92087-125">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="92087-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="92087-126">AssociatedPage</span><span class="sxs-lookup"><span data-stu-id="92087-126">AssociatedPage</span></span>  <br/> |<span data-ttu-id="92087-127">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="92087-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="92087-128">Optional</span><span class="sxs-lookup"><span data-stu-id="92087-128">optional</span></span>  <br/> ||<span data-ttu-id="92087-129">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="92087-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="92087-130">Hintergrund</span><span class="sxs-lookup"><span data-stu-id="92087-130">Background</span></span>  <br/> |<span data-ttu-id="92087-131">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="92087-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="92087-132">Optional</span><span class="sxs-lookup"><span data-stu-id="92087-132">optional</span></span>  <br/> ||<span data-ttu-id="92087-133">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="92087-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="92087-134">BackPage</span><span class="sxs-lookup"><span data-stu-id="92087-134">BackPage</span></span>  <br/> |<span data-ttu-id="92087-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="92087-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="92087-136">Optional</span><span class="sxs-lookup"><span data-stu-id="92087-136">optional</span></span>  <br/> ||<span data-ttu-id="92087-137">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="92087-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="92087-138">ID</span><span class="sxs-lookup"><span data-stu-id="92087-138">ID</span></span>  <br/> |<span data-ttu-id="92087-139">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="92087-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="92087-140">erforderlich</span><span class="sxs-lookup"><span data-stu-id="92087-140">required</span></span>  <br/> ||<span data-ttu-id="92087-141">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="92087-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="92087-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="92087-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="92087-143">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="92087-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="92087-144">Optional</span><span class="sxs-lookup"><span data-stu-id="92087-144">optional</span></span>  <br/> ||<span data-ttu-id="92087-145">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="92087-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="92087-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="92087-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="92087-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="92087-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="92087-148">Optional</span><span class="sxs-lookup"><span data-stu-id="92087-148">optional</span></span>  <br/> ||<span data-ttu-id="92087-149">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="92087-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="92087-150">Name</span><span class="sxs-lookup"><span data-stu-id="92087-150">Name</span></span>  <br/> |<span data-ttu-id="92087-151">xsd:string</span><span class="sxs-lookup"><span data-stu-id="92087-151">xsd:string</span></span>  <br/> |<span data-ttu-id="92087-152">Optional</span><span class="sxs-lookup"><span data-stu-id="92087-152">optional</span></span>  <br/> ||<span data-ttu-id="92087-153">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="92087-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="92087-154">NameU</span><span class="sxs-lookup"><span data-stu-id="92087-154">NameU</span></span>  <br/> |<span data-ttu-id="92087-155">xsd:string</span><span class="sxs-lookup"><span data-stu-id="92087-155">xsd:string</span></span>  <br/> |<span data-ttu-id="92087-156">Optional</span><span class="sxs-lookup"><span data-stu-id="92087-156">optional</span></span>  <br/> ||<span data-ttu-id="92087-157">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="92087-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="92087-158">ReviewerID</span><span class="sxs-lookup"><span data-stu-id="92087-158">ReviewerID</span></span>  <br/> |<span data-ttu-id="92087-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="92087-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="92087-160">Optional</span><span class="sxs-lookup"><span data-stu-id="92087-160">optional</span></span>  <br/> ||<span data-ttu-id="92087-161">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="92087-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="92087-162">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="92087-162">ViewCenterX</span></span>  <br/> |<span data-ttu-id="92087-163">xsd:double</span><span class="sxs-lookup"><span data-stu-id="92087-163">xsd:double</span></span>  <br/> |<span data-ttu-id="92087-164">Optional</span><span class="sxs-lookup"><span data-stu-id="92087-164">optional</span></span>  <br/> ||<span data-ttu-id="92087-165">Werte des xsd:double-Typs.</span><span class="sxs-lookup"><span data-stu-id="92087-165">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="92087-166">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="92087-166">ViewCenterY</span></span>  <br/> |<span data-ttu-id="92087-167">xsd:double</span><span class="sxs-lookup"><span data-stu-id="92087-167">xsd:double</span></span>  <br/> |<span data-ttu-id="92087-168">Optional</span><span class="sxs-lookup"><span data-stu-id="92087-168">optional</span></span>  <br/> ||<span data-ttu-id="92087-169">Werte des xsd:double-Typs.</span><span class="sxs-lookup"><span data-stu-id="92087-169">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="92087-170">ViewScale</span><span class="sxs-lookup"><span data-stu-id="92087-170">ViewScale</span></span>  <br/> |<span data-ttu-id="92087-171">xsd:double</span><span class="sxs-lookup"><span data-stu-id="92087-171">xsd:double</span></span>  <br/> |<span data-ttu-id="92087-172">Optional</span><span class="sxs-lookup"><span data-stu-id="92087-172">optional</span></span>  <br/> ||<span data-ttu-id="92087-173">Werte des xsd:double-Typs.</span><span class="sxs-lookup"><span data-stu-id="92087-173">Values of the xsd:double type.</span></span>  <br/> |
   

