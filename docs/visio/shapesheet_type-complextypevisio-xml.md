---
title: ShapeSheet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fb394861-34d7-b7dd-1298-0c68a008528d
ms.openlocfilehash: 0094bc9643cc1331e0b47bd11a59769a553e17f7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542058"
---
# <a name="shapesheet_type-complextype-visio-xml"></a><span data-ttu-id="5b6b3-102">ShapeSheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="5b6b3-102">ShapeSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="5b6b3-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="5b6b3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5b6b3-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5b6b3-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5b6b3-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="5b6b3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5b6b3-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5b6b3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5b6b3-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="5b6b3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5b6b3-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="5b6b3-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5b6b3-109">Definition</span><span class="sxs-lookup"><span data-stu-id="5b6b3-109">Definition</span></span>

```XML
          <xs:complexType name="ShapeSheet_Type">
          
          <xs:complexContent>
          <xs:extension base="Sheet_Type">
          <xs:sequence>
    <xs:element name="Shapes"  type="Shapes_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Text"  type="Text_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Data1"  type="Data_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Data2"  type="Data_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Data3"  type="Data_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ForeignData"  type="ForeignData_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="OriginalID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Del"
  type="xsd:boolean"
    />
    <xs:attribute name="MasterShape"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
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
    <xs:attribute name="Master"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Type"
  type="xsd:token"
    />
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5b6b3-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="5b6b3-110">Elements and attributes</span></span>

<span data-ttu-id="5b6b3-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="5b6b3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5b6b3-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5b6b3-112">Child elements</span></span>

|<span data-ttu-id="5b6b3-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5b6b3-113">**Element**</span></span>|<span data-ttu-id="5b6b3-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="5b6b3-114">**Type**</span></span>|<span data-ttu-id="5b6b3-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5b6b3-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5b6b3-116">Data1</span><span class="sxs-lookup"><span data-stu-id="5b6b3-116">Data1</span></span>](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5b6b3-117">Data_Type</span><span class="sxs-lookup"><span data-stu-id="5b6b3-117">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5b6b3-118">Data2</span><span class="sxs-lookup"><span data-stu-id="5b6b3-118">Data2</span></span>](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5b6b3-119">Data_Type</span><span class="sxs-lookup"><span data-stu-id="5b6b3-119">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5b6b3-120">Data3</span><span class="sxs-lookup"><span data-stu-id="5b6b3-120">Data3</span></span>](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5b6b3-121">Data_Type</span><span class="sxs-lookup"><span data-stu-id="5b6b3-121">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5b6b3-122">ForeignData</span><span class="sxs-lookup"><span data-stu-id="5b6b3-122">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5b6b3-123">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="5b6b3-123">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5b6b3-124">Formen</span><span class="sxs-lookup"><span data-stu-id="5b6b3-124">Shapes</span></span>](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5b6b3-125">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="5b6b3-125">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5b6b3-126">Text</span><span class="sxs-lookup"><span data-stu-id="5b6b3-126">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5b6b3-127">Text_Type</span><span class="sxs-lookup"><span data-stu-id="5b6b3-127">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5b6b3-128">Attribute</span><span class="sxs-lookup"><span data-stu-id="5b6b3-128">Attributes</span></span>

|<span data-ttu-id="5b6b3-129">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="5b6b3-129">**Attribute**</span></span>|<span data-ttu-id="5b6b3-130">**Typ**</span><span class="sxs-lookup"><span data-stu-id="5b6b3-130">**Type**</span></span>|<span data-ttu-id="5b6b3-131">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="5b6b3-131">**Required**</span></span>|<span data-ttu-id="5b6b3-132">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5b6b3-132">**Description**</span></span>|<span data-ttu-id="5b6b3-133">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="5b6b3-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5b6b3-134">Del</span><span class="sxs-lookup"><span data-stu-id="5b6b3-134">Del</span></span>  <br/> |<span data-ttu-id="5b6b3-135">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="5b6b3-135">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5b6b3-136">Optional</span><span class="sxs-lookup"><span data-stu-id="5b6b3-136">optional</span></span>  <br/> ||<span data-ttu-id="5b6b3-137">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="5b6b3-137">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="5b6b3-138">ID</span><span class="sxs-lookup"><span data-stu-id="5b6b3-138">ID</span></span>  <br/> |<span data-ttu-id="5b6b3-139">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5b6b3-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5b6b3-140">erforderlich</span><span class="sxs-lookup"><span data-stu-id="5b6b3-140">required</span></span>  <br/> ||<span data-ttu-id="5b6b3-141">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="5b6b3-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5b6b3-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="5b6b3-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="5b6b3-143">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="5b6b3-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5b6b3-144">Optional</span><span class="sxs-lookup"><span data-stu-id="5b6b3-144">optional</span></span>  <br/> ||<span data-ttu-id="5b6b3-145">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="5b6b3-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="5b6b3-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="5b6b3-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="5b6b3-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="5b6b3-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5b6b3-148">Optional</span><span class="sxs-lookup"><span data-stu-id="5b6b3-148">optional</span></span>  <br/> ||<span data-ttu-id="5b6b3-149">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="5b6b3-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="5b6b3-150">Master</span><span class="sxs-lookup"><span data-stu-id="5b6b3-150">Master</span></span>  <br/> |<span data-ttu-id="5b6b3-151">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5b6b3-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5b6b3-152">Optional</span><span class="sxs-lookup"><span data-stu-id="5b6b3-152">optional</span></span>  <br/> ||<span data-ttu-id="5b6b3-153">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="5b6b3-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5b6b3-154">MasterShape</span><span class="sxs-lookup"><span data-stu-id="5b6b3-154">MasterShape</span></span>  <br/> |<span data-ttu-id="5b6b3-155">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5b6b3-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5b6b3-156">Optional</span><span class="sxs-lookup"><span data-stu-id="5b6b3-156">optional</span></span>  <br/> ||<span data-ttu-id="5b6b3-157">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="5b6b3-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5b6b3-158">Name</span><span class="sxs-lookup"><span data-stu-id="5b6b3-158">Name</span></span>  <br/> |<span data-ttu-id="5b6b3-159">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5b6b3-159">xsd:string</span></span>  <br/> |<span data-ttu-id="5b6b3-160">Optional</span><span class="sxs-lookup"><span data-stu-id="5b6b3-160">optional</span></span>  <br/> ||<span data-ttu-id="5b6b3-161">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="5b6b3-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5b6b3-162">NameU</span><span class="sxs-lookup"><span data-stu-id="5b6b3-162">NameU</span></span>  <br/> |<span data-ttu-id="5b6b3-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5b6b3-163">xsd:string</span></span>  <br/> |<span data-ttu-id="5b6b3-164">Optional</span><span class="sxs-lookup"><span data-stu-id="5b6b3-164">optional</span></span>  <br/> ||<span data-ttu-id="5b6b3-165">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="5b6b3-165">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5b6b3-166">OriginalID</span><span class="sxs-lookup"><span data-stu-id="5b6b3-166">OriginalID</span></span>  <br/> |<span data-ttu-id="5b6b3-167">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5b6b3-167">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5b6b3-168">Optional</span><span class="sxs-lookup"><span data-stu-id="5b6b3-168">optional</span></span>  <br/> ||<span data-ttu-id="5b6b3-169">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="5b6b3-169">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5b6b3-170">Typ</span><span class="sxs-lookup"><span data-stu-id="5b6b3-170">Type</span></span>  <br/> |<span data-ttu-id="5b6b3-171">xsd:token</span><span class="sxs-lookup"><span data-stu-id="5b6b3-171">xsd:token</span></span>  <br/> |<span data-ttu-id="5b6b3-172">Optional</span><span class="sxs-lookup"><span data-stu-id="5b6b3-172">optional</span></span>  <br/> ||<span data-ttu-id="5b6b3-173">Werte des xsd:token-Typs.</span><span class="sxs-lookup"><span data-stu-id="5b6b3-173">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="5b6b3-174">UniqueID</span><span class="sxs-lookup"><span data-stu-id="5b6b3-174">UniqueID</span></span>  <br/> |<span data-ttu-id="5b6b3-175">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5b6b3-175">xsd:string</span></span>  <br/> |<span data-ttu-id="5b6b3-176">Optional</span><span class="sxs-lookup"><span data-stu-id="5b6b3-176">optional</span></span>  <br/> ||<span data-ttu-id="5b6b3-177">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="5b6b3-177">Values of the xsd:string type.</span></span>  <br/> |
   

