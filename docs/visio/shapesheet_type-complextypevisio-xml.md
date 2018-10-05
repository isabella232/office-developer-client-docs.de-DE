---
title: ShapeSheet_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fb394861-34d7-b7dd-1298-0c68a008528d
ms.openlocfilehash: c48af0def561e01fe5a92a57b7416faab40f1200
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383632"
---
# <a name="shapesheettype-complextype-visio-xml"></a><span data-ttu-id="f5dae-102">ShapeSheet_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="f5dae-102">ShapeSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f5dae-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="f5dae-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f5dae-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f5dae-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f5dae-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="f5dae-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f5dae-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f5dae-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f5dae-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="f5dae-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f5dae-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="f5dae-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f5dae-109">Definition</span><span class="sxs-lookup"><span data-stu-id="f5dae-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f5dae-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="f5dae-110">Elements and attributes</span></span>

<span data-ttu-id="f5dae-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="f5dae-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f5dae-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f5dae-112">Child elements</span></span>

|<span data-ttu-id="f5dae-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f5dae-113">**Element**</span></span>|<span data-ttu-id="f5dae-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f5dae-114">**Type**</span></span>|<span data-ttu-id="f5dae-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f5dae-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f5dae-116">Data1</span><span class="sxs-lookup"><span data-stu-id="f5dae-116">Data1</span></span>](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f5dae-117">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f5dae-117">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="f5dae-118">Data2</span><span class="sxs-lookup"><span data-stu-id="f5dae-118">Data2</span></span>](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f5dae-119">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f5dae-119">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="f5dae-120">Data3</span><span class="sxs-lookup"><span data-stu-id="f5dae-120">Data3</span></span>](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f5dae-121">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f5dae-121">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="f5dae-122">ForeignData</span><span class="sxs-lookup"><span data-stu-id="f5dae-122">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f5dae-123">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="f5dae-123">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="f5dae-124">Shapes</span><span class="sxs-lookup"><span data-stu-id="f5dae-124">Shapes</span></span>](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f5dae-125">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="f5dae-125">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="f5dae-126">Text</span><span class="sxs-lookup"><span data-stu-id="f5dae-126">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f5dae-127">Text_Type</span><span class="sxs-lookup"><span data-stu-id="f5dae-127">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f5dae-128">Attribute</span><span class="sxs-lookup"><span data-stu-id="f5dae-128">Attributes</span></span>

|<span data-ttu-id="f5dae-129">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f5dae-129">**Attribute**</span></span>|<span data-ttu-id="f5dae-130">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f5dae-130">**Type**</span></span>|<span data-ttu-id="f5dae-131">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="f5dae-131">**Required**</span></span>|<span data-ttu-id="f5dae-132">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f5dae-132">**Description**</span></span>|<span data-ttu-id="f5dae-133">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="f5dae-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f5dae-134">ENTF</span><span class="sxs-lookup"><span data-stu-id="f5dae-134">Del</span></span>  <br/> |<span data-ttu-id="f5dae-135">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="f5dae-135">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f5dae-136">Optional</span><span class="sxs-lookup"><span data-stu-id="f5dae-136">optional</span></span>  <br/> ||<span data-ttu-id="f5dae-137">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="f5dae-137">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f5dae-138">ID</span><span class="sxs-lookup"><span data-stu-id="f5dae-138">ID</span></span>  <br/> |<span data-ttu-id="f5dae-139">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f5dae-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f5dae-140">erforderlich</span><span class="sxs-lookup"><span data-stu-id="f5dae-140">required</span></span>  <br/> ||<span data-ttu-id="f5dae-141">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f5dae-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f5dae-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="f5dae-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="f5dae-143">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="f5dae-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f5dae-144">Optional</span><span class="sxs-lookup"><span data-stu-id="f5dae-144">optional</span></span>  <br/> ||<span data-ttu-id="f5dae-145">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="f5dae-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f5dae-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="f5dae-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="f5dae-147">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="f5dae-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f5dae-148">Optional</span><span class="sxs-lookup"><span data-stu-id="f5dae-148">optional</span></span>  <br/> ||<span data-ttu-id="f5dae-149">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="f5dae-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f5dae-150">Master</span><span class="sxs-lookup"><span data-stu-id="f5dae-150">Master</span></span>  <br/> |<span data-ttu-id="f5dae-151">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f5dae-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f5dae-152">Optional</span><span class="sxs-lookup"><span data-stu-id="f5dae-152">optional</span></span>  <br/> ||<span data-ttu-id="f5dae-153">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f5dae-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f5dae-154">MasterShape</span><span class="sxs-lookup"><span data-stu-id="f5dae-154">MasterShape</span></span>  <br/> |<span data-ttu-id="f5dae-155">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f5dae-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f5dae-156">Optional</span><span class="sxs-lookup"><span data-stu-id="f5dae-156">optional</span></span>  <br/> ||<span data-ttu-id="f5dae-157">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f5dae-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f5dae-158">Name</span><span class="sxs-lookup"><span data-stu-id="f5dae-158">Name</span></span>  <br/> |<span data-ttu-id="f5dae-159">XSD: String</span><span class="sxs-lookup"><span data-stu-id="f5dae-159">xsd:string</span></span>  <br/> |<span data-ttu-id="f5dae-160">Optional</span><span class="sxs-lookup"><span data-stu-id="f5dae-160">optional</span></span>  <br/> ||<span data-ttu-id="f5dae-161">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f5dae-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f5dae-162">NameU</span><span class="sxs-lookup"><span data-stu-id="f5dae-162">NameU</span></span>  <br/> |<span data-ttu-id="f5dae-163">XSD: String</span><span class="sxs-lookup"><span data-stu-id="f5dae-163">xsd:string</span></span>  <br/> |<span data-ttu-id="f5dae-164">Optional</span><span class="sxs-lookup"><span data-stu-id="f5dae-164">optional</span></span>  <br/> ||<span data-ttu-id="f5dae-165">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f5dae-165">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f5dae-166">OriginalID</span><span class="sxs-lookup"><span data-stu-id="f5dae-166">OriginalID</span></span>  <br/> |<span data-ttu-id="f5dae-167">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f5dae-167">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f5dae-168">Optional</span><span class="sxs-lookup"><span data-stu-id="f5dae-168">optional</span></span>  <br/> ||<span data-ttu-id="f5dae-169">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f5dae-169">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f5dae-170">Typ</span><span class="sxs-lookup"><span data-stu-id="f5dae-170">Type</span></span>  <br/> |<span data-ttu-id="f5dae-171">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="f5dae-171">xsd:token</span></span>  <br/> |<span data-ttu-id="f5dae-172">Optional</span><span class="sxs-lookup"><span data-stu-id="f5dae-172">optional</span></span>  <br/> ||<span data-ttu-id="f5dae-173">Werte des Typs Xsd:token.</span><span class="sxs-lookup"><span data-stu-id="f5dae-173">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="f5dae-174">UniqueID</span><span class="sxs-lookup"><span data-stu-id="f5dae-174">UniqueID</span></span>  <br/> |<span data-ttu-id="f5dae-175">XSD: String</span><span class="sxs-lookup"><span data-stu-id="f5dae-175">xsd:string</span></span>  <br/> |<span data-ttu-id="f5dae-176">Optional</span><span class="sxs-lookup"><span data-stu-id="f5dae-176">optional</span></span>  <br/> ||<span data-ttu-id="f5dae-177">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f5dae-177">Values of the xsd:string type.</span></span>  <br/> |
   

