---
title: ForeignData_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 1d9358de2f88a1b9e035ecf4966544ea935f8b2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797065"
---
# <a name="foreigndatatype-complextype-visio-xml"></a><span data-ttu-id="64a3c-102">ForeignData_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="64a3c-102">ForeignData_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="64a3c-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="64a3c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="64a3c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="64a3c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="64a3c-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="64a3c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="64a3c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="64a3c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="64a3c-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="64a3c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="64a3c-108">Keine</span><span class="sxs-lookup"><span data-stu-id="64a3c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="64a3c-109">Definition</span><span class="sxs-lookup"><span data-stu-id="64a3c-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="64a3c-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="64a3c-110">Elements and attributes</span></span>

<span data-ttu-id="64a3c-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="64a3c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="64a3c-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="64a3c-112">Child elements</span></span>

|<span data-ttu-id="64a3c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="64a3c-113">**Element**</span></span>|<span data-ttu-id="64a3c-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="64a3c-114">**Type**</span></span>|<span data-ttu-id="64a3c-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="64a3c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="64a3c-116">Rel</span><span class="sxs-lookup"><span data-stu-id="64a3c-116">Rel</span></span>](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="64a3c-117">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="64a3c-117">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="64a3c-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="64a3c-118">Attributes</span></span>

|<span data-ttu-id="64a3c-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="64a3c-119">**Attribute**</span></span>|<span data-ttu-id="64a3c-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="64a3c-120">**Type**</span></span>|<span data-ttu-id="64a3c-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="64a3c-121">**Required**</span></span>|<span data-ttu-id="64a3c-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="64a3c-122">**Description**</span></span>|<span data-ttu-id="64a3c-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="64a3c-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="64a3c-124">CompressionLevel</span><span class="sxs-lookup"><span data-stu-id="64a3c-124">CompressionLevel</span></span>  <br/> |<span data-ttu-id="64a3c-125">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="64a3c-125">xsd:double</span></span>  <br/> |<span data-ttu-id="64a3c-126">Optional</span><span class="sxs-lookup"><span data-stu-id="64a3c-126">optional</span></span>  <br/> ||<span data-ttu-id="64a3c-127">Werte des Typs xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="64a3c-127">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="64a3c-128">CompressionType</span><span class="sxs-lookup"><span data-stu-id="64a3c-128">CompressionType</span></span>  <br/> |<span data-ttu-id="64a3c-129">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="64a3c-129">xsd:token</span></span>  <br/> |<span data-ttu-id="64a3c-130">Optional</span><span class="sxs-lookup"><span data-stu-id="64a3c-130">optional</span></span>  <br/> ||<span data-ttu-id="64a3c-131">Werte des Typs Xsd:token.</span><span class="sxs-lookup"><span data-stu-id="64a3c-131">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="64a3c-132">ExtentX</span><span class="sxs-lookup"><span data-stu-id="64a3c-132">ExtentX</span></span>  <br/> |<span data-ttu-id="64a3c-133">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="64a3c-133">xsd:double</span></span>  <br/> |<span data-ttu-id="64a3c-134">Optional</span><span class="sxs-lookup"><span data-stu-id="64a3c-134">optional</span></span>  <br/> ||<span data-ttu-id="64a3c-135">Werte des Typs xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="64a3c-135">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="64a3c-136">ExtentY</span><span class="sxs-lookup"><span data-stu-id="64a3c-136">ExtentY</span></span>  <br/> |<span data-ttu-id="64a3c-137">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="64a3c-137">xsd:double</span></span>  <br/> |<span data-ttu-id="64a3c-138">Optional</span><span class="sxs-lookup"><span data-stu-id="64a3c-138">optional</span></span>  <br/> ||<span data-ttu-id="64a3c-139">Werte des Typs xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="64a3c-139">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="64a3c-140">ForeignType</span><span class="sxs-lookup"><span data-stu-id="64a3c-140">ForeignType</span></span>  <br/> |<span data-ttu-id="64a3c-141">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="64a3c-141">xsd:token</span></span>  <br/> |<span data-ttu-id="64a3c-142">erforderlich</span><span class="sxs-lookup"><span data-stu-id="64a3c-142">required</span></span>  <br/> ||<span data-ttu-id="64a3c-143">Werte des Typs Xsd:token.</span><span class="sxs-lookup"><span data-stu-id="64a3c-143">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="64a3c-144">MappingMode</span><span class="sxs-lookup"><span data-stu-id="64a3c-144">MappingMode</span></span>  <br/> |<span data-ttu-id="64a3c-145">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="64a3c-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="64a3c-146">Optional</span><span class="sxs-lookup"><span data-stu-id="64a3c-146">optional</span></span>  <br/> ||<span data-ttu-id="64a3c-147">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="64a3c-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="64a3c-148">ObjectHeight</span><span class="sxs-lookup"><span data-stu-id="64a3c-148">ObjectHeight</span></span>  <br/> |<span data-ttu-id="64a3c-149">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="64a3c-149">xsd:double</span></span>  <br/> |<span data-ttu-id="64a3c-150">Optional</span><span class="sxs-lookup"><span data-stu-id="64a3c-150">optional</span></span>  <br/> ||<span data-ttu-id="64a3c-151">Werte des Typs xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="64a3c-151">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="64a3c-152">ObjectType</span><span class="sxs-lookup"><span data-stu-id="64a3c-152">ObjectType</span></span>  <br/> |<span data-ttu-id="64a3c-153">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="64a3c-153">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="64a3c-154">Optional</span><span class="sxs-lookup"><span data-stu-id="64a3c-154">optional</span></span>  <br/> ||<span data-ttu-id="64a3c-155">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="64a3c-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="64a3c-156">ObjectWidth</span><span class="sxs-lookup"><span data-stu-id="64a3c-156">ObjectWidth</span></span>  <br/> |<span data-ttu-id="64a3c-157">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="64a3c-157">xsd:double</span></span>  <br/> |<span data-ttu-id="64a3c-158">Optional</span><span class="sxs-lookup"><span data-stu-id="64a3c-158">optional</span></span>  <br/> ||<span data-ttu-id="64a3c-159">Werte des Typs xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="64a3c-159">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="64a3c-160">ShowAsIcon</span><span class="sxs-lookup"><span data-stu-id="64a3c-160">ShowAsIcon</span></span>  <br/> |<span data-ttu-id="64a3c-161">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="64a3c-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="64a3c-162">Optional</span><span class="sxs-lookup"><span data-stu-id="64a3c-162">optional</span></span>  <br/> ||<span data-ttu-id="64a3c-163">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="64a3c-163">Values of the xsd:boolean type.</span></span>  <br/> |
   

