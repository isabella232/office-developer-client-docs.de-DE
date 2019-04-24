---
title: Page_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4bc5c0c4-3ee3-7f63-541a-1f1854d4201c
ms.openlocfilehash: d0c364164d2453c9dc64290db24890224a3c70e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334398"
---
# <a name="pagetype-complextype-visio-xml"></a><span data-ttu-id="9364a-102">Page_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="9364a-102">Page_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9364a-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="9364a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9364a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9364a-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9364a-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="9364a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9364a-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="9364a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9364a-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="9364a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9364a-108">Keine</span><span class="sxs-lookup"><span data-stu-id="9364a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9364a-109">Definition</span><span class="sxs-lookup"><span data-stu-id="9364a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="9364a-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="9364a-110">Elements and attributes</span></span>

<span data-ttu-id="9364a-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="9364a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9364a-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9364a-112">Child elements</span></span>

|<span data-ttu-id="9364a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="9364a-113">**Element**</span></span>|<span data-ttu-id="9364a-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9364a-114">**Type**</span></span>|<span data-ttu-id="9364a-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9364a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9364a-116">PageSheet</span><span class="sxs-lookup"><span data-stu-id="9364a-116">PageSheet</span></span>](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9364a-117">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="9364a-117">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9364a-118">Rel</span><span class="sxs-lookup"><span data-stu-id="9364a-118">Rel</span></span>](rel-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9364a-119">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="9364a-119">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9364a-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="9364a-120">Attributes</span></span>

|<span data-ttu-id="9364a-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9364a-121">**Attribute**</span></span>|<span data-ttu-id="9364a-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9364a-122">**Type**</span></span>|<span data-ttu-id="9364a-123">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="9364a-123">**Required**</span></span>|<span data-ttu-id="9364a-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9364a-124">**Description**</span></span>|<span data-ttu-id="9364a-125">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="9364a-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9364a-126">AssociatedPage</span><span class="sxs-lookup"><span data-stu-id="9364a-126">AssociatedPage</span></span>  <br/> |<span data-ttu-id="9364a-127">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9364a-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9364a-128">Optional</span><span class="sxs-lookup"><span data-stu-id="9364a-128">optional</span></span>  <br/> ||<span data-ttu-id="9364a-129">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="9364a-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9364a-130">Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9364a-130">Background</span></span>  <br/> |<span data-ttu-id="9364a-131">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="9364a-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9364a-132">Optional</span><span class="sxs-lookup"><span data-stu-id="9364a-132">optional</span></span>  <br/> ||<span data-ttu-id="9364a-133">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="9364a-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9364a-134">BackPage</span><span class="sxs-lookup"><span data-stu-id="9364a-134">BackPage</span></span>  <br/> |<span data-ttu-id="9364a-135">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9364a-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9364a-136">Optional</span><span class="sxs-lookup"><span data-stu-id="9364a-136">optional</span></span>  <br/> ||<span data-ttu-id="9364a-137">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="9364a-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9364a-138">ID</span><span class="sxs-lookup"><span data-stu-id="9364a-138">ID</span></span>  <br/> |<span data-ttu-id="9364a-139">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9364a-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9364a-140">erforderlich</span><span class="sxs-lookup"><span data-stu-id="9364a-140">required</span></span>  <br/> ||<span data-ttu-id="9364a-141">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="9364a-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9364a-142">IsCustomname</span><span class="sxs-lookup"><span data-stu-id="9364a-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="9364a-143">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="9364a-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9364a-144">Optional</span><span class="sxs-lookup"><span data-stu-id="9364a-144">optional</span></span>  <br/> ||<span data-ttu-id="9364a-145">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="9364a-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9364a-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="9364a-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="9364a-147">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="9364a-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9364a-148">Optional</span><span class="sxs-lookup"><span data-stu-id="9364a-148">optional</span></span>  <br/> ||<span data-ttu-id="9364a-149">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="9364a-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9364a-150">Name</span><span class="sxs-lookup"><span data-stu-id="9364a-150">Name</span></span>  <br/> |<span data-ttu-id="9364a-151">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9364a-151">xsd:string</span></span>  <br/> |<span data-ttu-id="9364a-152">Optional</span><span class="sxs-lookup"><span data-stu-id="9364a-152">optional</span></span>  <br/> ||<span data-ttu-id="9364a-153">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="9364a-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9364a-154">NameU</span><span class="sxs-lookup"><span data-stu-id="9364a-154">NameU</span></span>  <br/> |<span data-ttu-id="9364a-155">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9364a-155">xsd:string</span></span>  <br/> |<span data-ttu-id="9364a-156">Optional</span><span class="sxs-lookup"><span data-stu-id="9364a-156">optional</span></span>  <br/> ||<span data-ttu-id="9364a-157">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="9364a-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9364a-158">ReviewerID</span><span class="sxs-lookup"><span data-stu-id="9364a-158">ReviewerID</span></span>  <br/> |<span data-ttu-id="9364a-159">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9364a-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9364a-160">Optional</span><span class="sxs-lookup"><span data-stu-id="9364a-160">optional</span></span>  <br/> ||<span data-ttu-id="9364a-161">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="9364a-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9364a-162">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="9364a-162">ViewCenterX</span></span>  <br/> |<span data-ttu-id="9364a-163">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="9364a-163">xsd:double</span></span>  <br/> |<span data-ttu-id="9364a-164">Optional</span><span class="sxs-lookup"><span data-stu-id="9364a-164">optional</span></span>  <br/> ||<span data-ttu-id="9364a-165">Werte des Typs XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="9364a-165">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="9364a-166">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="9364a-166">ViewCenterY</span></span>  <br/> |<span data-ttu-id="9364a-167">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="9364a-167">xsd:double</span></span>  <br/> |<span data-ttu-id="9364a-168">Optional</span><span class="sxs-lookup"><span data-stu-id="9364a-168">optional</span></span>  <br/> ||<span data-ttu-id="9364a-169">Werte des Typs XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="9364a-169">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="9364a-170">ViewScale</span><span class="sxs-lookup"><span data-stu-id="9364a-170">ViewScale</span></span>  <br/> |<span data-ttu-id="9364a-171">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="9364a-171">xsd:double</span></span>  <br/> |<span data-ttu-id="9364a-172">Optional</span><span class="sxs-lookup"><span data-stu-id="9364a-172">optional</span></span>  <br/> ||<span data-ttu-id="9364a-173">Werte des Typs XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="9364a-173">Values of the xsd:double type.</span></span>  <br/> |
   

