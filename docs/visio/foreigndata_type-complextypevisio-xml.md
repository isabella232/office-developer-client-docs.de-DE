---
title: ForeignData_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 39396ef0db5b78d6f32d8828103eecd105f8b91d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539863"
---
# <a name="foreigndata_type-complextype-visio-xml"></a><span data-ttu-id="c9677-102">ForeignData_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c9677-102">ForeignData_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="c9677-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="c9677-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c9677-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c9677-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c9677-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="c9677-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c9677-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c9677-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c9677-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="c9677-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c9677-108">Keine</span><span class="sxs-lookup"><span data-stu-id="c9677-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c9677-109">Definition</span><span class="sxs-lookup"><span data-stu-id="c9677-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c9677-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="c9677-110">Elements and attributes</span></span>

<span data-ttu-id="c9677-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="c9677-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c9677-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c9677-112">Child elements</span></span>

|<span data-ttu-id="c9677-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c9677-113">**Element**</span></span>|<span data-ttu-id="c9677-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c9677-114">**Type**</span></span>|<span data-ttu-id="c9677-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c9677-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c9677-116">Rel</span><span class="sxs-lookup"><span data-stu-id="c9677-116">Rel</span></span>](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c9677-117">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="c9677-117">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c9677-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="c9677-118">Attributes</span></span>

|<span data-ttu-id="c9677-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c9677-119">**Attribute**</span></span>|<span data-ttu-id="c9677-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c9677-120">**Type**</span></span>|<span data-ttu-id="c9677-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="c9677-121">**Required**</span></span>|<span data-ttu-id="c9677-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c9677-122">**Description**</span></span>|<span data-ttu-id="c9677-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="c9677-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c9677-124">CompressionLevel</span><span class="sxs-lookup"><span data-stu-id="c9677-124">CompressionLevel</span></span>  <br/> |<span data-ttu-id="c9677-125">xsd:double</span><span class="sxs-lookup"><span data-stu-id="c9677-125">xsd:double</span></span>  <br/> |<span data-ttu-id="c9677-126">Optional</span><span class="sxs-lookup"><span data-stu-id="c9677-126">optional</span></span>  <br/> ||<span data-ttu-id="c9677-127">Werte des xsd:double-Typs.</span><span class="sxs-lookup"><span data-stu-id="c9677-127">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="c9677-128">CompressionType</span><span class="sxs-lookup"><span data-stu-id="c9677-128">CompressionType</span></span>  <br/> |<span data-ttu-id="c9677-129">xsd:token</span><span class="sxs-lookup"><span data-stu-id="c9677-129">xsd:token</span></span>  <br/> |<span data-ttu-id="c9677-130">Optional</span><span class="sxs-lookup"><span data-stu-id="c9677-130">optional</span></span>  <br/> ||<span data-ttu-id="c9677-131">Werte des xsd:token-Typs.</span><span class="sxs-lookup"><span data-stu-id="c9677-131">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="c9677-132">ExtentX</span><span class="sxs-lookup"><span data-stu-id="c9677-132">ExtentX</span></span>  <br/> |<span data-ttu-id="c9677-133">xsd:double</span><span class="sxs-lookup"><span data-stu-id="c9677-133">xsd:double</span></span>  <br/> |<span data-ttu-id="c9677-134">Optional</span><span class="sxs-lookup"><span data-stu-id="c9677-134">optional</span></span>  <br/> ||<span data-ttu-id="c9677-135">Werte des xsd:double-Typs.</span><span class="sxs-lookup"><span data-stu-id="c9677-135">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="c9677-136">ExtentY</span><span class="sxs-lookup"><span data-stu-id="c9677-136">ExtentY</span></span>  <br/> |<span data-ttu-id="c9677-137">xsd:double</span><span class="sxs-lookup"><span data-stu-id="c9677-137">xsd:double</span></span>  <br/> |<span data-ttu-id="c9677-138">Optional</span><span class="sxs-lookup"><span data-stu-id="c9677-138">optional</span></span>  <br/> ||<span data-ttu-id="c9677-139">Werte des xsd:double-Typs.</span><span class="sxs-lookup"><span data-stu-id="c9677-139">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="c9677-140">ForeignType</span><span class="sxs-lookup"><span data-stu-id="c9677-140">ForeignType</span></span>  <br/> |<span data-ttu-id="c9677-141">xsd:token</span><span class="sxs-lookup"><span data-stu-id="c9677-141">xsd:token</span></span>  <br/> |<span data-ttu-id="c9677-142">erforderlich</span><span class="sxs-lookup"><span data-stu-id="c9677-142">required</span></span>  <br/> ||<span data-ttu-id="c9677-143">Werte des xsd:token-Typs.</span><span class="sxs-lookup"><span data-stu-id="c9677-143">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="c9677-144">MappingMode</span><span class="sxs-lookup"><span data-stu-id="c9677-144">MappingMode</span></span>  <br/> |<span data-ttu-id="c9677-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="c9677-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c9677-146">Optional</span><span class="sxs-lookup"><span data-stu-id="c9677-146">optional</span></span>  <br/> ||<span data-ttu-id="c9677-147">Werte des Typs xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="c9677-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c9677-148">ObjectHeight</span><span class="sxs-lookup"><span data-stu-id="c9677-148">ObjectHeight</span></span>  <br/> |<span data-ttu-id="c9677-149">xsd:double</span><span class="sxs-lookup"><span data-stu-id="c9677-149">xsd:double</span></span>  <br/> |<span data-ttu-id="c9677-150">Optional</span><span class="sxs-lookup"><span data-stu-id="c9677-150">optional</span></span>  <br/> ||<span data-ttu-id="c9677-151">Werte des xsd:double-Typs.</span><span class="sxs-lookup"><span data-stu-id="c9677-151">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="c9677-152">ObjectType</span><span class="sxs-lookup"><span data-stu-id="c9677-152">ObjectType</span></span>  <br/> |<span data-ttu-id="c9677-153">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c9677-153">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c9677-154">Optional</span><span class="sxs-lookup"><span data-stu-id="c9677-154">optional</span></span>  <br/> ||<span data-ttu-id="c9677-155">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="c9677-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c9677-156">ObjectWidth</span><span class="sxs-lookup"><span data-stu-id="c9677-156">ObjectWidth</span></span>  <br/> |<span data-ttu-id="c9677-157">xsd:double</span><span class="sxs-lookup"><span data-stu-id="c9677-157">xsd:double</span></span>  <br/> |<span data-ttu-id="c9677-158">Optional</span><span class="sxs-lookup"><span data-stu-id="c9677-158">optional</span></span>  <br/> ||<span data-ttu-id="c9677-159">Werte des xsd:double-Typs.</span><span class="sxs-lookup"><span data-stu-id="c9677-159">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="c9677-160">ShowAsIcon</span><span class="sxs-lookup"><span data-stu-id="c9677-160">ShowAsIcon</span></span>  <br/> |<span data-ttu-id="c9677-161">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="c9677-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c9677-162">Optional</span><span class="sxs-lookup"><span data-stu-id="c9677-162">optional</span></span>  <br/> ||<span data-ttu-id="c9677-163">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="c9677-163">Values of the xsd:boolean type.</span></span>  <br/> |
   

