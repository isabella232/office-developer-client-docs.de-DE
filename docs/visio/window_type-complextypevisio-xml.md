---
title: Window_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c514ce79-0920-4f1b-5332-0bdef146e802
ms.openlocfilehash: 08b65a5f0e108c5503e29c7e195d681d0a343521
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538452"
---
# <a name="window_type-complextype-visio-xml"></a><span data-ttu-id="69a79-102">Window_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="69a79-102">Window_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="69a79-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="69a79-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="69a79-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="69a79-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="69a79-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="69a79-105">**Schema file**</span></span> <br/> |<span data-ttu-id="69a79-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="69a79-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="69a79-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="69a79-107">**Extension base**</span></span> <br/> |<span data-ttu-id="69a79-108">Keine</span><span class="sxs-lookup"><span data-stu-id="69a79-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="69a79-109">Definition</span><span class="sxs-lookup"><span data-stu-id="69a79-109">Definition</span></span>

```XML
          <xs:complexType name="Window_Type">
          
          <xs:sequence>
    <xs:element name="StencilGroup"  type="StencilGroup_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="StencilGroupPos"  type="StencilGroupPos_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowRulers"  type="ShowRulers_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowGrid"  type="ShowGrid_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowPageBreaks"  type="ShowPageBreaks_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowGuides"  type="ShowGuides_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowConnectionPoints"  type="ShowConnectionPoints_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
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
    
    <xs:element name="TabSplitterPos"  type="TabSplitterPos_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="WindowType"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="WindowState"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Document"
  type="xsd:string"
    />
    <xs:attribute name="WindowLeft"
  type="xsd:short"
    />
    <xs:attribute name="WindowTop"
  type="xsd:short"
    />
    <xs:attribute name="WindowWidth"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="WindowHeight"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Master"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ContainerType"
  type="xsd:token"
    />
    <xs:attribute name="Container"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Sheet"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ReadOnly"
  type="xsd:boolean"
    />
    <xs:attribute name="ParentWindow"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Page"
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
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="69a79-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="69a79-110">Elements and attributes</span></span>

<span data-ttu-id="69a79-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="69a79-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="69a79-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="69a79-112">Child elements</span></span>

|<span data-ttu-id="69a79-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="69a79-113">**Element**</span></span>|<span data-ttu-id="69a79-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="69a79-114">**Type**</span></span>|<span data-ttu-id="69a79-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="69a79-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="69a79-116">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="69a79-116">DynamicGridEnabled</span></span>](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="69a79-117">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="69a79-117">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="69a79-118">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="69a79-118">GlueSettings</span></span>](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="69a79-119">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="69a79-119">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="69a79-120">ShowConnectionPoints</span><span class="sxs-lookup"><span data-stu-id="69a79-120">ShowConnectionPoints</span></span>](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="69a79-121">ShowConnectionPoints_Type</span><span class="sxs-lookup"><span data-stu-id="69a79-121">ShowConnectionPoints_Type</span></span>](showconnectionpoints_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="69a79-122">ShowGrid</span><span class="sxs-lookup"><span data-stu-id="69a79-122">ShowGrid</span></span>](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="69a79-123">ShowGrid_Type</span><span class="sxs-lookup"><span data-stu-id="69a79-123">ShowGrid_Type</span></span>](showgrid_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="69a79-124">ShowGuides</span><span class="sxs-lookup"><span data-stu-id="69a79-124">ShowGuides</span></span>](showguides-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="69a79-125">ShowGuides_Type</span><span class="sxs-lookup"><span data-stu-id="69a79-125">ShowGuides_Type</span></span>](showguides_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="69a79-126">ShowPageBreaks</span><span class="sxs-lookup"><span data-stu-id="69a79-126">ShowPageBreaks</span></span>](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="69a79-127">ShowPageBreaks_Type</span><span class="sxs-lookup"><span data-stu-id="69a79-127">ShowPageBreaks_Type</span></span>](showpagebreaks_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="69a79-128">ShowRulers</span><span class="sxs-lookup"><span data-stu-id="69a79-128">ShowRulers</span></span>](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="69a79-129">ShowRulers_Type</span><span class="sxs-lookup"><span data-stu-id="69a79-129">ShowRulers_Type</span></span>](showrulers_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="69a79-130">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="69a79-130">SnapAngles</span></span>](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="69a79-131">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="69a79-131">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="69a79-132">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="69a79-132">SnapExtensions</span></span>](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="69a79-133">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="69a79-133">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="69a79-134">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="69a79-134">SnapSettings</span></span>](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="69a79-135">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="69a79-135">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="69a79-136">StencilGroup</span><span class="sxs-lookup"><span data-stu-id="69a79-136">StencilGroup</span></span>](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="69a79-137">StencilGroup_Type</span><span class="sxs-lookup"><span data-stu-id="69a79-137">StencilGroup_Type</span></span>](stencilgroup_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="69a79-138">StencilGroupPos</span><span class="sxs-lookup"><span data-stu-id="69a79-138">StencilGroupPos</span></span>](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="69a79-139">StencilGroupPos_Type</span><span class="sxs-lookup"><span data-stu-id="69a79-139">StencilGroupPos_Type</span></span>](stencilgrouppos_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="69a79-140">TabSplitterPos</span><span class="sxs-lookup"><span data-stu-id="69a79-140">TabSplitterPos</span></span>](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="69a79-141">TabSplitterPos_Type</span><span class="sxs-lookup"><span data-stu-id="69a79-141">TabSplitterPos_Type</span></span>](tabsplitterpos_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="69a79-142">Attribute</span><span class="sxs-lookup"><span data-stu-id="69a79-142">Attributes</span></span>

|<span data-ttu-id="69a79-143">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="69a79-143">**Attribute**</span></span>|<span data-ttu-id="69a79-144">**Typ**</span><span class="sxs-lookup"><span data-stu-id="69a79-144">**Type**</span></span>|<span data-ttu-id="69a79-145">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="69a79-145">**Required**</span></span>|<span data-ttu-id="69a79-146">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="69a79-146">**Description**</span></span>|<span data-ttu-id="69a79-147">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="69a79-147">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="69a79-148">Container</span><span class="sxs-lookup"><span data-stu-id="69a79-148">Container</span></span>  <br/> |<span data-ttu-id="69a79-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="69a79-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="69a79-150">Optional</span><span class="sxs-lookup"><span data-stu-id="69a79-150">optional</span></span>  <br/> ||<span data-ttu-id="69a79-151">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="69a79-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="69a79-152">ContainerType</span><span class="sxs-lookup"><span data-stu-id="69a79-152">ContainerType</span></span>  <br/> |<span data-ttu-id="69a79-153">xsd:token</span><span class="sxs-lookup"><span data-stu-id="69a79-153">xsd:token</span></span>  <br/> |<span data-ttu-id="69a79-154">Optional</span><span class="sxs-lookup"><span data-stu-id="69a79-154">optional</span></span>  <br/> ||<span data-ttu-id="69a79-155">Werte des xsd:token-Typs.</span><span class="sxs-lookup"><span data-stu-id="69a79-155">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="69a79-156">Dokument</span><span class="sxs-lookup"><span data-stu-id="69a79-156">Document</span></span>  <br/> |<span data-ttu-id="69a79-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="69a79-157">xsd:string</span></span>  <br/> |<span data-ttu-id="69a79-158">Optional</span><span class="sxs-lookup"><span data-stu-id="69a79-158">optional</span></span>  <br/> ||<span data-ttu-id="69a79-159">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="69a79-159">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="69a79-160">ID</span><span class="sxs-lookup"><span data-stu-id="69a79-160">ID</span></span>  <br/> |<span data-ttu-id="69a79-161">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="69a79-161">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="69a79-162">erforderlich</span><span class="sxs-lookup"><span data-stu-id="69a79-162">required</span></span>  <br/> ||<span data-ttu-id="69a79-163">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="69a79-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="69a79-164">Master</span><span class="sxs-lookup"><span data-stu-id="69a79-164">Master</span></span>  <br/> |<span data-ttu-id="69a79-165">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="69a79-165">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="69a79-166">Optional</span><span class="sxs-lookup"><span data-stu-id="69a79-166">optional</span></span>  <br/> ||<span data-ttu-id="69a79-167">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="69a79-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="69a79-168">Seite</span><span class="sxs-lookup"><span data-stu-id="69a79-168">Page</span></span>  <br/> |<span data-ttu-id="69a79-169">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="69a79-169">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="69a79-170">Optional</span><span class="sxs-lookup"><span data-stu-id="69a79-170">optional</span></span>  <br/> ||<span data-ttu-id="69a79-171">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="69a79-171">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="69a79-172">ParentWindow</span><span class="sxs-lookup"><span data-stu-id="69a79-172">ParentWindow</span></span>  <br/> |<span data-ttu-id="69a79-173">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="69a79-173">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="69a79-174">Optional</span><span class="sxs-lookup"><span data-stu-id="69a79-174">optional</span></span>  <br/> ||<span data-ttu-id="69a79-175">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="69a79-175">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="69a79-176">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="69a79-176">ReadOnly</span></span>  <br/> |<span data-ttu-id="69a79-177">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="69a79-177">xsd:boolean</span></span>  <br/> |<span data-ttu-id="69a79-178">Optional</span><span class="sxs-lookup"><span data-stu-id="69a79-178">optional</span></span>  <br/> ||<span data-ttu-id="69a79-179">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="69a79-179">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="69a79-180">Blatt</span><span class="sxs-lookup"><span data-stu-id="69a79-180">Sheet</span></span>  <br/> |<span data-ttu-id="69a79-181">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="69a79-181">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="69a79-182">Optional</span><span class="sxs-lookup"><span data-stu-id="69a79-182">optional</span></span>  <br/> ||<span data-ttu-id="69a79-183">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="69a79-183">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="69a79-184">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="69a79-184">ViewCenterX</span></span>  <br/> |<span data-ttu-id="69a79-185">xsd:double</span><span class="sxs-lookup"><span data-stu-id="69a79-185">xsd:double</span></span>  <br/> |<span data-ttu-id="69a79-186">Optional</span><span class="sxs-lookup"><span data-stu-id="69a79-186">optional</span></span>  <br/> ||<span data-ttu-id="69a79-187">Werte des xsd:double-Typs.</span><span class="sxs-lookup"><span data-stu-id="69a79-187">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="69a79-188">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="69a79-188">ViewCenterY</span></span>  <br/> |<span data-ttu-id="69a79-189">xsd:double</span><span class="sxs-lookup"><span data-stu-id="69a79-189">xsd:double</span></span>  <br/> |<span data-ttu-id="69a79-190">Optional</span><span class="sxs-lookup"><span data-stu-id="69a79-190">optional</span></span>  <br/> ||<span data-ttu-id="69a79-191">Werte des xsd:double-Typs.</span><span class="sxs-lookup"><span data-stu-id="69a79-191">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="69a79-192">ViewScale</span><span class="sxs-lookup"><span data-stu-id="69a79-192">ViewScale</span></span>  <br/> |<span data-ttu-id="69a79-193">xsd:double</span><span class="sxs-lookup"><span data-stu-id="69a79-193">xsd:double</span></span>  <br/> |<span data-ttu-id="69a79-194">Optional</span><span class="sxs-lookup"><span data-stu-id="69a79-194">optional</span></span>  <br/> ||<span data-ttu-id="69a79-195">Werte des xsd:double-Typs.</span><span class="sxs-lookup"><span data-stu-id="69a79-195">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="69a79-196">WindowHeight</span><span class="sxs-lookup"><span data-stu-id="69a79-196">WindowHeight</span></span>  <br/> |<span data-ttu-id="69a79-197">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="69a79-197">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="69a79-198">Optional</span><span class="sxs-lookup"><span data-stu-id="69a79-198">optional</span></span>  <br/> ||<span data-ttu-id="69a79-199">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="69a79-199">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="69a79-200">WindowLeft</span><span class="sxs-lookup"><span data-stu-id="69a79-200">WindowLeft</span></span>  <br/> |<span data-ttu-id="69a79-201">xsd:short</span><span class="sxs-lookup"><span data-stu-id="69a79-201">xsd:short</span></span>  <br/> |<span data-ttu-id="69a79-202">Optional</span><span class="sxs-lookup"><span data-stu-id="69a79-202">optional</span></span>  <br/> ||<span data-ttu-id="69a79-203">Werte des xsd:short-Typs.</span><span class="sxs-lookup"><span data-stu-id="69a79-203">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="69a79-204">WindowState</span><span class="sxs-lookup"><span data-stu-id="69a79-204">WindowState</span></span>  <br/> |<span data-ttu-id="69a79-205">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="69a79-205">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="69a79-206">Optional</span><span class="sxs-lookup"><span data-stu-id="69a79-206">optional</span></span>  <br/> ||<span data-ttu-id="69a79-207">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="69a79-207">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="69a79-208">WindowTop</span><span class="sxs-lookup"><span data-stu-id="69a79-208">WindowTop</span></span>  <br/> |<span data-ttu-id="69a79-209">xsd:short</span><span class="sxs-lookup"><span data-stu-id="69a79-209">xsd:short</span></span>  <br/> |<span data-ttu-id="69a79-210">Optional</span><span class="sxs-lookup"><span data-stu-id="69a79-210">optional</span></span>  <br/> ||<span data-ttu-id="69a79-211">Werte des xsd:short-Typs.</span><span class="sxs-lookup"><span data-stu-id="69a79-211">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="69a79-212">WindowType</span><span class="sxs-lookup"><span data-stu-id="69a79-212">WindowType</span></span>  <br/> |<span data-ttu-id="69a79-213">xsd:token</span><span class="sxs-lookup"><span data-stu-id="69a79-213">xsd:token</span></span>  <br/> |<span data-ttu-id="69a79-214">erforderlich</span><span class="sxs-lookup"><span data-stu-id="69a79-214">required</span></span>  <br/> ||<span data-ttu-id="69a79-215">Werte des xsd:token-Typs.</span><span class="sxs-lookup"><span data-stu-id="69a79-215">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="69a79-216">WindowWidth</span><span class="sxs-lookup"><span data-stu-id="69a79-216">WindowWidth</span></span>  <br/> |<span data-ttu-id="69a79-217">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="69a79-217">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="69a79-218">Optional</span><span class="sxs-lookup"><span data-stu-id="69a79-218">optional</span></span>  <br/> ||<span data-ttu-id="69a79-219">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="69a79-219">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

