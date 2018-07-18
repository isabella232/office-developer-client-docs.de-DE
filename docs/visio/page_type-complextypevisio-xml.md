---
title: Page_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4bc5c0c4-3ee3-7f63-541a-1f1854d4201c
ms.openlocfilehash: b3a4916f3de20d9350b6673a6000d56f3030b66e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797573"
---
# <a name="pagetype-complextype-visio-xml"></a><span data-ttu-id="c0f5a-102">Page_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="c0f5a-102">Page_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c0f5a-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="c0f5a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c0f5a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c0f5a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c0f5a-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="c0f5a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c0f5a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c0f5a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c0f5a-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="c0f5a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c0f5a-108">Keine</span><span class="sxs-lookup"><span data-stu-id="c0f5a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c0f5a-109">Definition</span><span class="sxs-lookup"><span data-stu-id="c0f5a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c0f5a-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="c0f5a-110">Elements and attributes</span></span>

<span data-ttu-id="c0f5a-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="c0f5a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c0f5a-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c0f5a-112">Child elements</span></span>

|<span data-ttu-id="c0f5a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c0f5a-113">**Element**</span></span>|<span data-ttu-id="c0f5a-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c0f5a-114">**Type**</span></span>|<span data-ttu-id="c0f5a-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c0f5a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c0f5a-116">PageSheet</span><span class="sxs-lookup"><span data-stu-id="c0f5a-116">PageSheet</span></span>](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c0f5a-117">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="c0f5a-117">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c0f5a-118">Rel</span><span class="sxs-lookup"><span data-stu-id="c0f5a-118">Rel</span></span>](rel-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c0f5a-119">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="c0f5a-119">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c0f5a-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="c0f5a-120">Attributes</span></span>

|<span data-ttu-id="c0f5a-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c0f5a-121">**Attribute**</span></span>|<span data-ttu-id="c0f5a-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c0f5a-122">**Type**</span></span>|<span data-ttu-id="c0f5a-123">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="c0f5a-123">**Required**</span></span>|<span data-ttu-id="c0f5a-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c0f5a-124">**Description**</span></span>|<span data-ttu-id="c0f5a-125">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="c0f5a-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c0f5a-126">AssociatedPage</span><span class="sxs-lookup"><span data-stu-id="c0f5a-126">AssociatedPage</span></span>  <br/> |<span data-ttu-id="c0f5a-127">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c0f5a-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c0f5a-128">Optional</span><span class="sxs-lookup"><span data-stu-id="c0f5a-128">optional</span></span>  <br/> ||<span data-ttu-id="c0f5a-129">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c0f5a-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c0f5a-130">Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c0f5a-130">Background</span></span>  <br/> |<span data-ttu-id="c0f5a-131">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="c0f5a-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c0f5a-132">Optional</span><span class="sxs-lookup"><span data-stu-id="c0f5a-132">optional</span></span>  <br/> ||<span data-ttu-id="c0f5a-133">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="c0f5a-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c0f5a-134">BackPage</span><span class="sxs-lookup"><span data-stu-id="c0f5a-134">BackPage</span></span>  <br/> |<span data-ttu-id="c0f5a-135">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c0f5a-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c0f5a-136">Optional</span><span class="sxs-lookup"><span data-stu-id="c0f5a-136">optional</span></span>  <br/> ||<span data-ttu-id="c0f5a-137">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c0f5a-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c0f5a-138">ID</span><span class="sxs-lookup"><span data-stu-id="c0f5a-138">ID</span></span>  <br/> |<span data-ttu-id="c0f5a-139">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c0f5a-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c0f5a-140">erforderlich</span><span class="sxs-lookup"><span data-stu-id="c0f5a-140">required</span></span>  <br/> ||<span data-ttu-id="c0f5a-141">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c0f5a-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c0f5a-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="c0f5a-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="c0f5a-143">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="c0f5a-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c0f5a-144">Optional</span><span class="sxs-lookup"><span data-stu-id="c0f5a-144">optional</span></span>  <br/> ||<span data-ttu-id="c0f5a-145">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="c0f5a-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c0f5a-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="c0f5a-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="c0f5a-147">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="c0f5a-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c0f5a-148">Optional</span><span class="sxs-lookup"><span data-stu-id="c0f5a-148">optional</span></span>  <br/> ||<span data-ttu-id="c0f5a-149">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="c0f5a-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c0f5a-150">Name</span><span class="sxs-lookup"><span data-stu-id="c0f5a-150">Name</span></span>  <br/> |<span data-ttu-id="c0f5a-151">XSD: String</span><span class="sxs-lookup"><span data-stu-id="c0f5a-151">xsd:string</span></span>  <br/> |<span data-ttu-id="c0f5a-152">Optional</span><span class="sxs-lookup"><span data-stu-id="c0f5a-152">optional</span></span>  <br/> ||<span data-ttu-id="c0f5a-153">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="c0f5a-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c0f5a-154">NameU</span><span class="sxs-lookup"><span data-stu-id="c0f5a-154">NameU</span></span>  <br/> |<span data-ttu-id="c0f5a-155">XSD: String</span><span class="sxs-lookup"><span data-stu-id="c0f5a-155">xsd:string</span></span>  <br/> |<span data-ttu-id="c0f5a-156">Optional</span><span class="sxs-lookup"><span data-stu-id="c0f5a-156">optional</span></span>  <br/> ||<span data-ttu-id="c0f5a-157">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="c0f5a-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c0f5a-158">ReviewerID</span><span class="sxs-lookup"><span data-stu-id="c0f5a-158">ReviewerID</span></span>  <br/> |<span data-ttu-id="c0f5a-159">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c0f5a-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c0f5a-160">Optional</span><span class="sxs-lookup"><span data-stu-id="c0f5a-160">optional</span></span>  <br/> ||<span data-ttu-id="c0f5a-161">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c0f5a-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c0f5a-162">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="c0f5a-162">ViewCenterX</span></span>  <br/> |<span data-ttu-id="c0f5a-163">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="c0f5a-163">xsd:double</span></span>  <br/> |<span data-ttu-id="c0f5a-164">Optional</span><span class="sxs-lookup"><span data-stu-id="c0f5a-164">optional</span></span>  <br/> ||<span data-ttu-id="c0f5a-165">Werte des Typs xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="c0f5a-165">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="c0f5a-166">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="c0f5a-166">ViewCenterY</span></span>  <br/> |<span data-ttu-id="c0f5a-167">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="c0f5a-167">xsd:double</span></span>  <br/> |<span data-ttu-id="c0f5a-168">Optional</span><span class="sxs-lookup"><span data-stu-id="c0f5a-168">optional</span></span>  <br/> ||<span data-ttu-id="c0f5a-169">Werte des Typs xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="c0f5a-169">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="c0f5a-170">ViewScale</span><span class="sxs-lookup"><span data-stu-id="c0f5a-170">ViewScale</span></span>  <br/> |<span data-ttu-id="c0f5a-171">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="c0f5a-171">xsd:double</span></span>  <br/> |<span data-ttu-id="c0f5a-172">Optional</span><span class="sxs-lookup"><span data-stu-id="c0f5a-172">optional</span></span>  <br/> ||<span data-ttu-id="c0f5a-173">Werte des Typs xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="c0f5a-173">Values of the xsd:double type.</span></span>  <br/> |
   

