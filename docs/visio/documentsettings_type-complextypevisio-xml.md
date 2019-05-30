---
title: DocumentSettings_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8fb61b5f-1bab-78b6-c56c-384e52609397
ms.openlocfilehash: 0ec1f0dc21d7795e659fcdb512a912a00d1aacd6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540014"
---
# <a name="documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="82e8a-102">DocumentSettings_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="82e8a-102">DocumentSettings_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="82e8a-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="82e8a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="82e8a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="82e8a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="82e8a-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="82e8a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="82e8a-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="82e8a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="82e8a-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="82e8a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="82e8a-108">Keine</span><span class="sxs-lookup"><span data-stu-id="82e8a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="82e8a-109">Definition</span><span class="sxs-lookup"><span data-stu-id="82e8a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="82e8a-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="82e8a-110">Elements and attributes</span></span>

<span data-ttu-id="82e8a-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="82e8a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="82e8a-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="82e8a-112">Child elements</span></span>

|<span data-ttu-id="82e8a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="82e8a-113">**Element**</span></span>|<span data-ttu-id="82e8a-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="82e8a-114">**Type**</span></span>|<span data-ttu-id="82e8a-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="82e8a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="82e8a-116">AttachedToolbars</span><span class="sxs-lookup"><span data-stu-id="82e8a-116">AttachedToolbars</span></span>](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="82e8a-117">AttachedToolbars_Type</span><span class="sxs-lookup"><span data-stu-id="82e8a-117">AttachedToolbars_Type</span></span>](attachedtoolbars_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="82e8a-118">CustomMenusFile</span><span class="sxs-lookup"><span data-stu-id="82e8a-118">CustomMenusFile</span></span>](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="82e8a-119">CustomMenusFile_Type</span><span class="sxs-lookup"><span data-stu-id="82e8a-119">CustomMenusFile_Type</span></span>](custommenusfile_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="82e8a-120">CustomToolbarsFile</span><span class="sxs-lookup"><span data-stu-id="82e8a-120">CustomToolbarsFile</span></span>](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="82e8a-121">CustomToolbarsFile_Type</span><span class="sxs-lookup"><span data-stu-id="82e8a-121">CustomToolbarsFile_Type</span></span>](customtoolbarsfile_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="82e8a-122">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="82e8a-122">DynamicGridEnabled</span></span>](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="82e8a-123">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="82e8a-123">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="82e8a-124">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="82e8a-124">GlueSettings</span></span>](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="82e8a-125">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="82e8a-125">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="82e8a-126">Protectbkgnd</span><span class="sxs-lookup"><span data-stu-id="82e8a-126">ProtectBkgnds</span></span>](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="82e8a-127">ProtectBkgnds_Type</span><span class="sxs-lookup"><span data-stu-id="82e8a-127">ProtectBkgnds_Type</span></span>](protectbkgnds_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="82e8a-128">ProtectMasters</span><span class="sxs-lookup"><span data-stu-id="82e8a-128">ProtectMasters</span></span>](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="82e8a-129">ProtectMasters_Type</span><span class="sxs-lookup"><span data-stu-id="82e8a-129">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="82e8a-130">ProtectShapes</span><span class="sxs-lookup"><span data-stu-id="82e8a-130">ProtectShapes</span></span>](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="82e8a-131">ProtectShapes_Type</span><span class="sxs-lookup"><span data-stu-id="82e8a-131">ProtectShapes_Type</span></span>](protectshapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="82e8a-132">ProtectStyles</span><span class="sxs-lookup"><span data-stu-id="82e8a-132">ProtectStyles</span></span>](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="82e8a-133">ProtectStyles_Type</span><span class="sxs-lookup"><span data-stu-id="82e8a-133">ProtectStyles_Type</span></span>](protectstyles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="82e8a-134">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="82e8a-134">SnapAngles</span></span>](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="82e8a-135">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="82e8a-135">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="82e8a-136">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="82e8a-136">SnapExtensions</span></span>](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="82e8a-137">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="82e8a-137">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="82e8a-138">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="82e8a-138">SnapSettings</span></span>](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="82e8a-139">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="82e8a-139">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="82e8a-140">Attribute</span><span class="sxs-lookup"><span data-stu-id="82e8a-140">Attributes</span></span>

|<span data-ttu-id="82e8a-141">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="82e8a-141">**Attribute**</span></span>|<span data-ttu-id="82e8a-142">**Typ**</span><span class="sxs-lookup"><span data-stu-id="82e8a-142">**Type**</span></span>|<span data-ttu-id="82e8a-143">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="82e8a-143">**Required**</span></span>|<span data-ttu-id="82e8a-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="82e8a-144">**Description**</span></span>|<span data-ttu-id="82e8a-145">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="82e8a-145">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="82e8a-146">DefaultFillStyle</span><span class="sxs-lookup"><span data-stu-id="82e8a-146">DefaultFillStyle</span></span>  <br/> |<span data-ttu-id="82e8a-147">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="82e8a-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="82e8a-148">Optional</span><span class="sxs-lookup"><span data-stu-id="82e8a-148">optional</span></span>  <br/> ||<span data-ttu-id="82e8a-149">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="82e8a-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="82e8a-150">DefaultGuideStyle</span><span class="sxs-lookup"><span data-stu-id="82e8a-150">DefaultGuideStyle</span></span>  <br/> |<span data-ttu-id="82e8a-151">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="82e8a-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="82e8a-152">Optional</span><span class="sxs-lookup"><span data-stu-id="82e8a-152">optional</span></span>  <br/> ||<span data-ttu-id="82e8a-153">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="82e8a-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="82e8a-154">DefaultLineStyle</span><span class="sxs-lookup"><span data-stu-id="82e8a-154">DefaultLineStyle</span></span>  <br/> |<span data-ttu-id="82e8a-155">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="82e8a-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="82e8a-156">Optional</span><span class="sxs-lookup"><span data-stu-id="82e8a-156">optional</span></span>  <br/> ||<span data-ttu-id="82e8a-157">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="82e8a-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="82e8a-158">DefaultTextStyle</span><span class="sxs-lookup"><span data-stu-id="82e8a-158">DefaultTextStyle</span></span>  <br/> |<span data-ttu-id="82e8a-159">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="82e8a-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="82e8a-160">Optional</span><span class="sxs-lookup"><span data-stu-id="82e8a-160">optional</span></span>  <br/> ||<span data-ttu-id="82e8a-161">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="82e8a-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="82e8a-162">Startpage</span><span class="sxs-lookup"><span data-stu-id="82e8a-162">TopPage</span></span>  <br/> |<span data-ttu-id="82e8a-163">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="82e8a-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="82e8a-164">Optional</span><span class="sxs-lookup"><span data-stu-id="82e8a-164">optional</span></span>  <br/> ||<span data-ttu-id="82e8a-165">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="82e8a-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

