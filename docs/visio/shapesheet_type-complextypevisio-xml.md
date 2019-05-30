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
# <a name="shapesheettype-complextype-visio-xml"></a><span data-ttu-id="9f1e1-102">ShapeSheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9f1e1-102">ShapeSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="9f1e1-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="9f1e1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9f1e1-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9f1e1-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9f1e1-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="9f1e1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9f1e1-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="9f1e1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9f1e1-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="9f1e1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9f1e1-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="9f1e1-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9f1e1-109">Definition</span><span class="sxs-lookup"><span data-stu-id="9f1e1-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="9f1e1-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="9f1e1-110">Elements and attributes</span></span>

<span data-ttu-id="9f1e1-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="9f1e1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9f1e1-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9f1e1-112">Child elements</span></span>

|<span data-ttu-id="9f1e1-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="9f1e1-113">**Element**</span></span>|<span data-ttu-id="9f1e1-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9f1e1-114">**Type**</span></span>|<span data-ttu-id="9f1e1-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9f1e1-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9f1e1-116">Data1</span><span class="sxs-lookup"><span data-stu-id="9f1e1-116">Data1</span></span>](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9f1e1-117">Data_type</span><span class="sxs-lookup"><span data-stu-id="9f1e1-117">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9f1e1-118">Data2</span><span class="sxs-lookup"><span data-stu-id="9f1e1-118">Data2</span></span>](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9f1e1-119">Data_type</span><span class="sxs-lookup"><span data-stu-id="9f1e1-119">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9f1e1-120">Data3</span><span class="sxs-lookup"><span data-stu-id="9f1e1-120">Data3</span></span>](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9f1e1-121">Data_type</span><span class="sxs-lookup"><span data-stu-id="9f1e1-121">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9f1e1-122">ForeignData</span><span class="sxs-lookup"><span data-stu-id="9f1e1-122">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9f1e1-123">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="9f1e1-123">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9f1e1-124">Shapes</span><span class="sxs-lookup"><span data-stu-id="9f1e1-124">Shapes</span></span>](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9f1e1-125">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="9f1e1-125">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9f1e1-126">Text</span><span class="sxs-lookup"><span data-stu-id="9f1e1-126">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9f1e1-127">Text_type</span><span class="sxs-lookup"><span data-stu-id="9f1e1-127">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9f1e1-128">Attribute</span><span class="sxs-lookup"><span data-stu-id="9f1e1-128">Attributes</span></span>

|<span data-ttu-id="9f1e1-129">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9f1e1-129">**Attribute**</span></span>|<span data-ttu-id="9f1e1-130">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9f1e1-130">**Type**</span></span>|<span data-ttu-id="9f1e1-131">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="9f1e1-131">**Required**</span></span>|<span data-ttu-id="9f1e1-132">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9f1e1-132">**Description**</span></span>|<span data-ttu-id="9f1e1-133">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="9f1e1-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9f1e1-134">Del</span><span class="sxs-lookup"><span data-stu-id="9f1e1-134">Del</span></span>  <br/> |<span data-ttu-id="9f1e1-135">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="9f1e1-135">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9f1e1-136">Optional</span><span class="sxs-lookup"><span data-stu-id="9f1e1-136">optional</span></span>  <br/> ||<span data-ttu-id="9f1e1-137">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="9f1e1-137">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9f1e1-138">ID</span><span class="sxs-lookup"><span data-stu-id="9f1e1-138">ID</span></span>  <br/> |<span data-ttu-id="9f1e1-139">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9f1e1-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9f1e1-140">erforderlich</span><span class="sxs-lookup"><span data-stu-id="9f1e1-140">required</span></span>  <br/> ||<span data-ttu-id="9f1e1-141">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="9f1e1-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9f1e1-142">Iscustomname</span><span class="sxs-lookup"><span data-stu-id="9f1e1-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="9f1e1-143">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="9f1e1-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9f1e1-144">Optional</span><span class="sxs-lookup"><span data-stu-id="9f1e1-144">optional</span></span>  <br/> ||<span data-ttu-id="9f1e1-145">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="9f1e1-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9f1e1-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="9f1e1-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="9f1e1-147">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="9f1e1-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9f1e1-148">Optional</span><span class="sxs-lookup"><span data-stu-id="9f1e1-148">optional</span></span>  <br/> ||<span data-ttu-id="9f1e1-149">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="9f1e1-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9f1e1-150">Master</span><span class="sxs-lookup"><span data-stu-id="9f1e1-150">Master</span></span>  <br/> |<span data-ttu-id="9f1e1-151">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9f1e1-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9f1e1-152">Optional</span><span class="sxs-lookup"><span data-stu-id="9f1e1-152">optional</span></span>  <br/> ||<span data-ttu-id="9f1e1-153">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="9f1e1-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9f1e1-154">MasterShape</span><span class="sxs-lookup"><span data-stu-id="9f1e1-154">MasterShape</span></span>  <br/> |<span data-ttu-id="9f1e1-155">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9f1e1-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9f1e1-156">Optional</span><span class="sxs-lookup"><span data-stu-id="9f1e1-156">optional</span></span>  <br/> ||<span data-ttu-id="9f1e1-157">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="9f1e1-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9f1e1-158">Name</span><span class="sxs-lookup"><span data-stu-id="9f1e1-158">Name</span></span>  <br/> |<span data-ttu-id="9f1e1-159">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9f1e1-159">xsd:string</span></span>  <br/> |<span data-ttu-id="9f1e1-160">Optional</span><span class="sxs-lookup"><span data-stu-id="9f1e1-160">optional</span></span>  <br/> ||<span data-ttu-id="9f1e1-161">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="9f1e1-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9f1e1-162">NameU</span><span class="sxs-lookup"><span data-stu-id="9f1e1-162">NameU</span></span>  <br/> |<span data-ttu-id="9f1e1-163">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9f1e1-163">xsd:string</span></span>  <br/> |<span data-ttu-id="9f1e1-164">Optional</span><span class="sxs-lookup"><span data-stu-id="9f1e1-164">optional</span></span>  <br/> ||<span data-ttu-id="9f1e1-165">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="9f1e1-165">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9f1e1-166">OriginalID</span><span class="sxs-lookup"><span data-stu-id="9f1e1-166">OriginalID</span></span>  <br/> |<span data-ttu-id="9f1e1-167">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9f1e1-167">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9f1e1-168">Optional</span><span class="sxs-lookup"><span data-stu-id="9f1e1-168">optional</span></span>  <br/> ||<span data-ttu-id="9f1e1-169">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="9f1e1-169">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9f1e1-170">Typ</span><span class="sxs-lookup"><span data-stu-id="9f1e1-170">Type</span></span>  <br/> |<span data-ttu-id="9f1e1-171">XSD: Token</span><span class="sxs-lookup"><span data-stu-id="9f1e1-171">xsd:token</span></span>  <br/> |<span data-ttu-id="9f1e1-172">Optional</span><span class="sxs-lookup"><span data-stu-id="9f1e1-172">optional</span></span>  <br/> ||<span data-ttu-id="9f1e1-173">Werte des XSD: Token-Typs.</span><span class="sxs-lookup"><span data-stu-id="9f1e1-173">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="9f1e1-174">UniqueID</span><span class="sxs-lookup"><span data-stu-id="9f1e1-174">UniqueID</span></span>  <br/> |<span data-ttu-id="9f1e1-175">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9f1e1-175">xsd:string</span></span>  <br/> |<span data-ttu-id="9f1e1-176">Optional</span><span class="sxs-lookup"><span data-stu-id="9f1e1-176">optional</span></span>  <br/> ||<span data-ttu-id="9f1e1-177">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="9f1e1-177">Values of the xsd:string type.</span></span>  <br/> |
   

