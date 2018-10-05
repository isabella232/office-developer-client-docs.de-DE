---
title: ForeignData_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 6630c8b33dc1c4c7cbb12bb9727d4f0b1e1b19d2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384157"
---
# <a name="foreigndatatype-complextype-visio-xml"></a><span data-ttu-id="c3eb9-102">ForeignData_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="c3eb9-102">ForeignData_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c3eb9-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="c3eb9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c3eb9-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c3eb9-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c3eb9-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="c3eb9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c3eb9-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c3eb9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c3eb9-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="c3eb9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c3eb9-108">Keine</span><span class="sxs-lookup"><span data-stu-id="c3eb9-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c3eb9-109">Definition</span><span class="sxs-lookup"><span data-stu-id="c3eb9-109">Definition</span></span>

```XML
          <xs:complexType name="ForeignData_Type">
          
          <xs:sequence>
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ForeignType"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="ObjectType"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ShowAsIcon"
  type="xsd:boolean"
    />
    <xs:attribute name="ObjectWidth"
  type="xsd:double"
    />
    <xs:attribute name="ObjectHeight"
  type="xsd:double"
    />
    <xs:attribute name="MappingMode"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="ExtentX"
  type="xsd:double"
    />
    <xs:attribute name="ExtentY"
  type="xsd:double"
    />
    <xs:attribute name="CompressionType"
  type="xsd:token"
    />
    <xs:attribute name="CompressionLevel"
  type="xsd:double"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c3eb9-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="c3eb9-110">Elements and attributes</span></span>

<span data-ttu-id="c3eb9-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="c3eb9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c3eb9-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c3eb9-112">Child elements</span></span>

|<span data-ttu-id="c3eb9-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c3eb9-113">**Element**</span></span>|<span data-ttu-id="c3eb9-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c3eb9-114">**Type**</span></span>|<span data-ttu-id="c3eb9-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c3eb9-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c3eb9-116">Rel</span><span class="sxs-lookup"><span data-stu-id="c3eb9-116">Rel</span></span>](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c3eb9-117">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="c3eb9-117">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c3eb9-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="c3eb9-118">Attributes</span></span>

|<span data-ttu-id="c3eb9-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c3eb9-119">**Attribute**</span></span>|<span data-ttu-id="c3eb9-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c3eb9-120">**Type**</span></span>|<span data-ttu-id="c3eb9-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="c3eb9-121">**Required**</span></span>|<span data-ttu-id="c3eb9-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c3eb9-122">**Description**</span></span>|<span data-ttu-id="c3eb9-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="c3eb9-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c3eb9-124">CompressionLevel</span><span class="sxs-lookup"><span data-stu-id="c3eb9-124">CompressionLevel</span></span>  <br/> |<span data-ttu-id="c3eb9-125">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="c3eb9-125">xsd:double</span></span>  <br/> |<span data-ttu-id="c3eb9-126">Optional</span><span class="sxs-lookup"><span data-stu-id="c3eb9-126">optional</span></span>  <br/> ||<span data-ttu-id="c3eb9-127">Werte des Typs xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="c3eb9-127">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="c3eb9-128">CompressionType</span><span class="sxs-lookup"><span data-stu-id="c3eb9-128">CompressionType</span></span>  <br/> |<span data-ttu-id="c3eb9-129">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="c3eb9-129">xsd:token</span></span>  <br/> |<span data-ttu-id="c3eb9-130">Optional</span><span class="sxs-lookup"><span data-stu-id="c3eb9-130">optional</span></span>  <br/> ||<span data-ttu-id="c3eb9-131">Werte des Typs Xsd:token.</span><span class="sxs-lookup"><span data-stu-id="c3eb9-131">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="c3eb9-132">ExtentX</span><span class="sxs-lookup"><span data-stu-id="c3eb9-132">ExtentX</span></span>  <br/> |<span data-ttu-id="c3eb9-133">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="c3eb9-133">xsd:double</span></span>  <br/> |<span data-ttu-id="c3eb9-134">Optional</span><span class="sxs-lookup"><span data-stu-id="c3eb9-134">optional</span></span>  <br/> ||<span data-ttu-id="c3eb9-135">Werte des Typs xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="c3eb9-135">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="c3eb9-136">ExtentY</span><span class="sxs-lookup"><span data-stu-id="c3eb9-136">ExtentY</span></span>  <br/> |<span data-ttu-id="c3eb9-137">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="c3eb9-137">xsd:double</span></span>  <br/> |<span data-ttu-id="c3eb9-138">Optional</span><span class="sxs-lookup"><span data-stu-id="c3eb9-138">optional</span></span>  <br/> ||<span data-ttu-id="c3eb9-139">Werte des Typs xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="c3eb9-139">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="c3eb9-140">ForeignType</span><span class="sxs-lookup"><span data-stu-id="c3eb9-140">ForeignType</span></span>  <br/> |<span data-ttu-id="c3eb9-141">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="c3eb9-141">xsd:token</span></span>  <br/> |<span data-ttu-id="c3eb9-142">erforderlich</span><span class="sxs-lookup"><span data-stu-id="c3eb9-142">required</span></span>  <br/> ||<span data-ttu-id="c3eb9-143">Werte des Typs Xsd:token.</span><span class="sxs-lookup"><span data-stu-id="c3eb9-143">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="c3eb9-144">MappingMode</span><span class="sxs-lookup"><span data-stu-id="c3eb9-144">MappingMode</span></span>  <br/> |<span data-ttu-id="c3eb9-145">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="c3eb9-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c3eb9-146">Optional</span><span class="sxs-lookup"><span data-stu-id="c3eb9-146">optional</span></span>  <br/> ||<span data-ttu-id="c3eb9-147">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="c3eb9-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c3eb9-148">ObjectHeight</span><span class="sxs-lookup"><span data-stu-id="c3eb9-148">ObjectHeight</span></span>  <br/> |<span data-ttu-id="c3eb9-149">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="c3eb9-149">xsd:double</span></span>  <br/> |<span data-ttu-id="c3eb9-150">Optional</span><span class="sxs-lookup"><span data-stu-id="c3eb9-150">optional</span></span>  <br/> ||<span data-ttu-id="c3eb9-151">Werte des Typs xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="c3eb9-151">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="c3eb9-152">ObjectType</span><span class="sxs-lookup"><span data-stu-id="c3eb9-152">ObjectType</span></span>  <br/> |<span data-ttu-id="c3eb9-153">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c3eb9-153">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c3eb9-154">Optional</span><span class="sxs-lookup"><span data-stu-id="c3eb9-154">optional</span></span>  <br/> ||<span data-ttu-id="c3eb9-155">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c3eb9-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c3eb9-156">ObjectWidth</span><span class="sxs-lookup"><span data-stu-id="c3eb9-156">ObjectWidth</span></span>  <br/> |<span data-ttu-id="c3eb9-157">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="c3eb9-157">xsd:double</span></span>  <br/> |<span data-ttu-id="c3eb9-158">Optional</span><span class="sxs-lookup"><span data-stu-id="c3eb9-158">optional</span></span>  <br/> ||<span data-ttu-id="c3eb9-159">Werte des Typs xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="c3eb9-159">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="c3eb9-160">ShowAsIcon</span><span class="sxs-lookup"><span data-stu-id="c3eb9-160">ShowAsIcon</span></span>  <br/> |<span data-ttu-id="c3eb9-161">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="c3eb9-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c3eb9-162">Optional</span><span class="sxs-lookup"><span data-stu-id="c3eb9-162">optional</span></span>  <br/> ||<span data-ttu-id="c3eb9-163">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="c3eb9-163">Values of the xsd:boolean type.</span></span>  <br/> |
   

