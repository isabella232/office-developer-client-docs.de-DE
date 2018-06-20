---
title: DocumentSettings_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8fb61b5f-1bab-78b6-c56c-384e52609397
ms.openlocfilehash: 93623133e7d7fd096e063f0d9d5227d65dcc4736
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796899"
---
# <a name="documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="33429-102">DocumentSettings_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="33429-102">DocumentSettings_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="33429-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="33429-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="33429-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="33429-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="33429-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="33429-105">**Schema file**</span></span> <br/> |<span data-ttu-id="33429-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="33429-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="33429-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="33429-107">**Extension base**</span></span> <br/> |<span data-ttu-id="33429-108">Keine</span><span class="sxs-lookup"><span data-stu-id="33429-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="33429-109">Definition</span><span class="sxs-lookup"><span data-stu-id="33429-109">Definition</span></span>

```XML
          <xs:complexType name="DocumentSettings_Type">
          
          <xs:all>
    <xs:element name="GlueSettings"  type="GlueSettings_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="SnapSettings"  type="SnapSettings_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="SnapExtensions"  type="SnapExtensions_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="SnapAngles"  type="SnapAngles_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="DynamicGridEnabled"  type="DynamicGridEnabled_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ProtectStyles"  type="ProtectStyles_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ProtectShapes"  type="ProtectShapes_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ProtectMasters"  type="ProtectMasters_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ProtectBkgnds"  type="ProtectBkgnds_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="CustomMenusFile"  type="CustomMenusFile_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="CustomToolbarsFile"  type="CustomToolbarsFile_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="AttachedToolbars"  type="AttachedToolbars_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="TopPage"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DefaultTextStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DefaultLineStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DefaultFillStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DefaultGuideStyle"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="33429-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="33429-110">Elements and attributes</span></span>

<span data-ttu-id="33429-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="33429-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="33429-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="33429-112">Child elements</span></span>

|<span data-ttu-id="33429-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="33429-113">**Element**</span></span>|<span data-ttu-id="33429-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="33429-114">**Type**</span></span>|<span data-ttu-id="33429-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="33429-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="33429-116">AttachedToolbars</span><span class="sxs-lookup"><span data-stu-id="33429-116">AttachedToolbars</span></span>](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="33429-117">AttachedToolbars_Type</span><span class="sxs-lookup"><span data-stu-id="33429-117">AttachedToolbars_Type</span></span>](attachedtoolbars_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="33429-118">CustomMenusFile</span><span class="sxs-lookup"><span data-stu-id="33429-118">CustomMenusFile</span></span>](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="33429-119">CustomMenusFile_Type</span><span class="sxs-lookup"><span data-stu-id="33429-119">CustomMenusFile_Type</span></span>](custommenusfile_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="33429-120">CustomToolbarsFile</span><span class="sxs-lookup"><span data-stu-id="33429-120">CustomToolbarsFile</span></span>](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="33429-121">CustomToolbarsFile_Type</span><span class="sxs-lookup"><span data-stu-id="33429-121">CustomToolbarsFile_Type</span></span>](customtoolbarsfile_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="33429-122">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="33429-122">DynamicGridEnabled</span></span>](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="33429-123">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="33429-123">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="33429-124">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="33429-124">GlueSettings</span></span>](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="33429-125">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="33429-125">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="33429-126">ProtectBkgnds</span><span class="sxs-lookup"><span data-stu-id="33429-126">ProtectBkgnds</span></span>](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="33429-127">ProtectBkgnds_Type</span><span class="sxs-lookup"><span data-stu-id="33429-127">ProtectBkgnds_Type</span></span>](protectbkgnds_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="33429-128">ProtectMasters</span><span class="sxs-lookup"><span data-stu-id="33429-128">ProtectMasters</span></span>](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="33429-129">ProtectMasters_Type</span><span class="sxs-lookup"><span data-stu-id="33429-129">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="33429-130">ProtectShapes</span><span class="sxs-lookup"><span data-stu-id="33429-130">ProtectShapes</span></span>](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="33429-131">ProtectShapes_Type</span><span class="sxs-lookup"><span data-stu-id="33429-131">ProtectShapes_Type</span></span>](protectshapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="33429-132">ProtectStyles</span><span class="sxs-lookup"><span data-stu-id="33429-132">ProtectStyles</span></span>](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="33429-133">ProtectStyles_Type</span><span class="sxs-lookup"><span data-stu-id="33429-133">ProtectStyles_Type</span></span>](protectstyles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="33429-134">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="33429-134">SnapAngles</span></span>](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="33429-135">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="33429-135">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="33429-136">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="33429-136">SnapExtensions</span></span>](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="33429-137">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="33429-137">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="33429-138">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="33429-138">SnapSettings</span></span>](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="33429-139">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="33429-139">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="33429-140">Attribute</span><span class="sxs-lookup"><span data-stu-id="33429-140">Attributes</span></span>

|<span data-ttu-id="33429-141">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="33429-141">**Attribute**</span></span>|<span data-ttu-id="33429-142">**Typ**</span><span class="sxs-lookup"><span data-stu-id="33429-142">**Type**</span></span>|<span data-ttu-id="33429-143">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="33429-143">**Required**</span></span>|<span data-ttu-id="33429-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="33429-144">**Description**</span></span>|<span data-ttu-id="33429-145">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="33429-145">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="33429-146">DefaultFillStyle</span><span class="sxs-lookup"><span data-stu-id="33429-146">DefaultFillStyle</span></span>  <br/> |<span data-ttu-id="33429-147">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="33429-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="33429-148">Optional</span><span class="sxs-lookup"><span data-stu-id="33429-148">optional</span></span>  <br/> ||<span data-ttu-id="33429-149">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="33429-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="33429-150">DefaultGuideStyle</span><span class="sxs-lookup"><span data-stu-id="33429-150">DefaultGuideStyle</span></span>  <br/> |<span data-ttu-id="33429-151">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="33429-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="33429-152">Optional</span><span class="sxs-lookup"><span data-stu-id="33429-152">optional</span></span>  <br/> ||<span data-ttu-id="33429-153">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="33429-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="33429-154">DefaultLineStyle</span><span class="sxs-lookup"><span data-stu-id="33429-154">DefaultLineStyle</span></span>  <br/> |<span data-ttu-id="33429-155">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="33429-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="33429-156">Optional</span><span class="sxs-lookup"><span data-stu-id="33429-156">optional</span></span>  <br/> ||<span data-ttu-id="33429-157">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="33429-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="33429-158">DefaultTextStyle</span><span class="sxs-lookup"><span data-stu-id="33429-158">DefaultTextStyle</span></span>  <br/> |<span data-ttu-id="33429-159">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="33429-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="33429-160">Optional</span><span class="sxs-lookup"><span data-stu-id="33429-160">optional</span></span>  <br/> ||<span data-ttu-id="33429-161">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="33429-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="33429-162">TopPage</span><span class="sxs-lookup"><span data-stu-id="33429-162">TopPage</span></span>  <br/> |<span data-ttu-id="33429-163">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="33429-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="33429-164">Optional</span><span class="sxs-lookup"><span data-stu-id="33429-164">optional</span></span>  <br/> ||<span data-ttu-id="33429-165">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="33429-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

