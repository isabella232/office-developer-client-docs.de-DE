---
title: ShapeSheet_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fb394861-34d7-b7dd-1298-0c68a008528d
ms.openlocfilehash: 45282acfc8a399a5c634c1860aba1f926e0b7a94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798048"
---
# <a name="shapesheettype-complextype-visio-xml"></a><span data-ttu-id="55395-102">ShapeSheet_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="55395-102">ShapeSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="55395-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="55395-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="55395-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="55395-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="55395-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="55395-105">**Schema file**</span></span> <br/> |<span data-ttu-id="55395-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="55395-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="55395-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="55395-107">**Extension base**</span></span> <br/> |<span data-ttu-id="55395-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="55395-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="55395-109">Definition</span><span class="sxs-lookup"><span data-stu-id="55395-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="55395-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="55395-110">Elements and attributes</span></span>

<span data-ttu-id="55395-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="55395-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="55395-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="55395-112">Child elements</span></span>

|<span data-ttu-id="55395-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="55395-113">**Element**</span></span>|<span data-ttu-id="55395-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="55395-114">**Type**</span></span>|<span data-ttu-id="55395-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="55395-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="55395-116">Data1</span><span class="sxs-lookup"><span data-stu-id="55395-116">Data1</span></span>](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="55395-117">Datentyp</span><span class="sxs-lookup"><span data-stu-id="55395-117">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="55395-118">Data2</span><span class="sxs-lookup"><span data-stu-id="55395-118">Data2</span></span>](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="55395-119">Datentyp</span><span class="sxs-lookup"><span data-stu-id="55395-119">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="55395-120">Data3</span><span class="sxs-lookup"><span data-stu-id="55395-120">Data3</span></span>](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="55395-121">Datentyp</span><span class="sxs-lookup"><span data-stu-id="55395-121">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="55395-122">ForeignData</span><span class="sxs-lookup"><span data-stu-id="55395-122">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="55395-123">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="55395-123">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="55395-124">Shapes</span><span class="sxs-lookup"><span data-stu-id="55395-124">Shapes</span></span>](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="55395-125">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="55395-125">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="55395-126">Text</span><span class="sxs-lookup"><span data-stu-id="55395-126">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="55395-127">Text_Type</span><span class="sxs-lookup"><span data-stu-id="55395-127">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="55395-128">Attribute</span><span class="sxs-lookup"><span data-stu-id="55395-128">Attributes</span></span>

|<span data-ttu-id="55395-129">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="55395-129">**Attribute**</span></span>|<span data-ttu-id="55395-130">**Typ**</span><span class="sxs-lookup"><span data-stu-id="55395-130">**Type**</span></span>|<span data-ttu-id="55395-131">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="55395-131">**Required**</span></span>|<span data-ttu-id="55395-132">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="55395-132">**Description**</span></span>|<span data-ttu-id="55395-133">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="55395-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="55395-134">ENTF</span><span class="sxs-lookup"><span data-stu-id="55395-134">Del</span></span>  <br/> |<span data-ttu-id="55395-135">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="55395-135">xsd:boolean</span></span>  <br/> |<span data-ttu-id="55395-136">Optional</span><span class="sxs-lookup"><span data-stu-id="55395-136">optional</span></span>  <br/> ||<span data-ttu-id="55395-137">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="55395-137">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="55395-138">ID</span><span class="sxs-lookup"><span data-stu-id="55395-138">ID</span></span>  <br/> |<span data-ttu-id="55395-139">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="55395-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="55395-140">erforderlich</span><span class="sxs-lookup"><span data-stu-id="55395-140">required</span></span>  <br/> ||<span data-ttu-id="55395-141">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="55395-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="55395-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="55395-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="55395-143">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="55395-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="55395-144">Optional</span><span class="sxs-lookup"><span data-stu-id="55395-144">optional</span></span>  <br/> ||<span data-ttu-id="55395-145">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="55395-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="55395-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="55395-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="55395-147">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="55395-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="55395-148">Optional</span><span class="sxs-lookup"><span data-stu-id="55395-148">optional</span></span>  <br/> ||<span data-ttu-id="55395-149">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="55395-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="55395-150">Master</span><span class="sxs-lookup"><span data-stu-id="55395-150">Master</span></span>  <br/> |<span data-ttu-id="55395-151">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="55395-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="55395-152">Optional</span><span class="sxs-lookup"><span data-stu-id="55395-152">optional</span></span>  <br/> ||<span data-ttu-id="55395-153">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="55395-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="55395-154">MasterShape</span><span class="sxs-lookup"><span data-stu-id="55395-154">MasterShape</span></span>  <br/> |<span data-ttu-id="55395-155">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="55395-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="55395-156">Optional</span><span class="sxs-lookup"><span data-stu-id="55395-156">optional</span></span>  <br/> ||<span data-ttu-id="55395-157">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="55395-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="55395-158">Name</span><span class="sxs-lookup"><span data-stu-id="55395-158">Name</span></span>  <br/> |<span data-ttu-id="55395-159">XSD: String</span><span class="sxs-lookup"><span data-stu-id="55395-159">xsd:string</span></span>  <br/> |<span data-ttu-id="55395-160">Optional</span><span class="sxs-lookup"><span data-stu-id="55395-160">optional</span></span>  <br/> ||<span data-ttu-id="55395-161">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="55395-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="55395-162">NameU</span><span class="sxs-lookup"><span data-stu-id="55395-162">NameU</span></span>  <br/> |<span data-ttu-id="55395-163">XSD: String</span><span class="sxs-lookup"><span data-stu-id="55395-163">xsd:string</span></span>  <br/> |<span data-ttu-id="55395-164">Optional</span><span class="sxs-lookup"><span data-stu-id="55395-164">optional</span></span>  <br/> ||<span data-ttu-id="55395-165">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="55395-165">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="55395-166">OriginalID</span><span class="sxs-lookup"><span data-stu-id="55395-166">OriginalID</span></span>  <br/> |<span data-ttu-id="55395-167">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="55395-167">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="55395-168">Optional</span><span class="sxs-lookup"><span data-stu-id="55395-168">optional</span></span>  <br/> ||<span data-ttu-id="55395-169">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="55395-169">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="55395-170">Typ</span><span class="sxs-lookup"><span data-stu-id="55395-170">Type</span></span>  <br/> |<span data-ttu-id="55395-171">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="55395-171">xsd:token</span></span>  <br/> |<span data-ttu-id="55395-172">Optional</span><span class="sxs-lookup"><span data-stu-id="55395-172">optional</span></span>  <br/> ||<span data-ttu-id="55395-173">Werte des Typs Xsd:token.</span><span class="sxs-lookup"><span data-stu-id="55395-173">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="55395-174">UniqueID</span><span class="sxs-lookup"><span data-stu-id="55395-174">UniqueID</span></span>  <br/> |<span data-ttu-id="55395-175">XSD: String</span><span class="sxs-lookup"><span data-stu-id="55395-175">xsd:string</span></span>  <br/> |<span data-ttu-id="55395-176">Optional</span><span class="sxs-lookup"><span data-stu-id="55395-176">optional</span></span>  <br/> ||<span data-ttu-id="55395-177">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="55395-177">Values of the xsd:string type.</span></span>  <br/> |
   

