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
# <a name="windowtype-complextype-visio-xml"></a><span data-ttu-id="202e3-102">Window_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="202e3-102">Window_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="202e3-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="202e3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="202e3-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="202e3-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="202e3-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="202e3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="202e3-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="202e3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="202e3-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="202e3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="202e3-108">Keine</span><span class="sxs-lookup"><span data-stu-id="202e3-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="202e3-109">Definition</span><span class="sxs-lookup"><span data-stu-id="202e3-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="202e3-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="202e3-110">Elements and attributes</span></span>

<span data-ttu-id="202e3-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="202e3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="202e3-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="202e3-112">Child elements</span></span>

|<span data-ttu-id="202e3-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="202e3-113">**Element**</span></span>|<span data-ttu-id="202e3-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="202e3-114">**Type**</span></span>|<span data-ttu-id="202e3-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="202e3-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="202e3-116">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="202e3-116">DynamicGridEnabled</span></span>](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="202e3-117">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="202e3-117">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="202e3-118">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="202e3-118">GlueSettings</span></span>](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="202e3-119">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="202e3-119">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="202e3-120">ShowConnectionPoints</span><span class="sxs-lookup"><span data-stu-id="202e3-120">ShowConnectionPoints</span></span>](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="202e3-121">ShowConnectionPoints_Type</span><span class="sxs-lookup"><span data-stu-id="202e3-121">ShowConnectionPoints_Type</span></span>](showconnectionpoints_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="202e3-122">ShowGrid</span><span class="sxs-lookup"><span data-stu-id="202e3-122">ShowGrid</span></span>](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="202e3-123">ShowGrid_Type</span><span class="sxs-lookup"><span data-stu-id="202e3-123">ShowGrid_Type</span></span>](showgrid_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="202e3-124">ShowGuides</span><span class="sxs-lookup"><span data-stu-id="202e3-124">ShowGuides</span></span>](showguides-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="202e3-125">ShowGuides_Type</span><span class="sxs-lookup"><span data-stu-id="202e3-125">ShowGuides_Type</span></span>](showguides_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="202e3-126">ShowPageBreaks</span><span class="sxs-lookup"><span data-stu-id="202e3-126">ShowPageBreaks</span></span>](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="202e3-127">ShowPageBreaks_Type</span><span class="sxs-lookup"><span data-stu-id="202e3-127">ShowPageBreaks_Type</span></span>](showpagebreaks_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="202e3-128">ShowRulers</span><span class="sxs-lookup"><span data-stu-id="202e3-128">ShowRulers</span></span>](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="202e3-129">ShowRulers_Type</span><span class="sxs-lookup"><span data-stu-id="202e3-129">ShowRulers_Type</span></span>](showrulers_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="202e3-130">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="202e3-130">SnapAngles</span></span>](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="202e3-131">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="202e3-131">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="202e3-132">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="202e3-132">SnapExtensions</span></span>](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="202e3-133">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="202e3-133">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="202e3-134">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="202e3-134">SnapSettings</span></span>](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="202e3-135">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="202e3-135">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="202e3-136">Stencilgroup</span><span class="sxs-lookup"><span data-stu-id="202e3-136">StencilGroup</span></span>](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="202e3-137">StencilGroup_Type</span><span class="sxs-lookup"><span data-stu-id="202e3-137">StencilGroup_Type</span></span>](stencilgroup_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="202e3-138">StencilGroupPos</span><span class="sxs-lookup"><span data-stu-id="202e3-138">StencilGroupPos</span></span>](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="202e3-139">StencilGroupPos_Type</span><span class="sxs-lookup"><span data-stu-id="202e3-139">StencilGroupPos_Type</span></span>](stencilgrouppos_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="202e3-140">TabSplitterPos</span><span class="sxs-lookup"><span data-stu-id="202e3-140">TabSplitterPos</span></span>](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="202e3-141">TabSplitterPos_Type</span><span class="sxs-lookup"><span data-stu-id="202e3-141">TabSplitterPos_Type</span></span>](tabsplitterpos_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="202e3-142">Attribute</span><span class="sxs-lookup"><span data-stu-id="202e3-142">Attributes</span></span>

|<span data-ttu-id="202e3-143">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="202e3-143">**Attribute**</span></span>|<span data-ttu-id="202e3-144">**Typ**</span><span class="sxs-lookup"><span data-stu-id="202e3-144">**Type**</span></span>|<span data-ttu-id="202e3-145">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="202e3-145">**Required**</span></span>|<span data-ttu-id="202e3-146">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="202e3-146">**Description**</span></span>|<span data-ttu-id="202e3-147">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="202e3-147">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="202e3-148">Container</span><span class="sxs-lookup"><span data-stu-id="202e3-148">Container</span></span>  <br/> |<span data-ttu-id="202e3-149">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="202e3-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="202e3-150">Optional</span><span class="sxs-lookup"><span data-stu-id="202e3-150">optional</span></span>  <br/> ||<span data-ttu-id="202e3-151">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="202e3-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="202e3-152">ContainerType</span><span class="sxs-lookup"><span data-stu-id="202e3-152">ContainerType</span></span>  <br/> |<span data-ttu-id="202e3-153">XSD: Token</span><span class="sxs-lookup"><span data-stu-id="202e3-153">xsd:token</span></span>  <br/> |<span data-ttu-id="202e3-154">Optional</span><span class="sxs-lookup"><span data-stu-id="202e3-154">optional</span></span>  <br/> ||<span data-ttu-id="202e3-155">Werte des XSD: Token-Typs.</span><span class="sxs-lookup"><span data-stu-id="202e3-155">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="202e3-156">Dokument</span><span class="sxs-lookup"><span data-stu-id="202e3-156">Document</span></span>  <br/> |<span data-ttu-id="202e3-157">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="202e3-157">xsd:string</span></span>  <br/> |<span data-ttu-id="202e3-158">Optional</span><span class="sxs-lookup"><span data-stu-id="202e3-158">optional</span></span>  <br/> ||<span data-ttu-id="202e3-159">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="202e3-159">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="202e3-160">ID</span><span class="sxs-lookup"><span data-stu-id="202e3-160">ID</span></span>  <br/> |<span data-ttu-id="202e3-161">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="202e3-161">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="202e3-162">erforderlich</span><span class="sxs-lookup"><span data-stu-id="202e3-162">required</span></span>  <br/> ||<span data-ttu-id="202e3-163">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="202e3-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="202e3-164">Master</span><span class="sxs-lookup"><span data-stu-id="202e3-164">Master</span></span>  <br/> |<span data-ttu-id="202e3-165">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="202e3-165">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="202e3-166">Optional</span><span class="sxs-lookup"><span data-stu-id="202e3-166">optional</span></span>  <br/> ||<span data-ttu-id="202e3-167">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="202e3-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="202e3-168">Seite</span><span class="sxs-lookup"><span data-stu-id="202e3-168">Page</span></span>  <br/> |<span data-ttu-id="202e3-169">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="202e3-169">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="202e3-170">Optional</span><span class="sxs-lookup"><span data-stu-id="202e3-170">optional</span></span>  <br/> ||<span data-ttu-id="202e3-171">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="202e3-171">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="202e3-172">ParentWindow</span><span class="sxs-lookup"><span data-stu-id="202e3-172">ParentWindow</span></span>  <br/> |<span data-ttu-id="202e3-173">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="202e3-173">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="202e3-174">Optional</span><span class="sxs-lookup"><span data-stu-id="202e3-174">optional</span></span>  <br/> ||<span data-ttu-id="202e3-175">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="202e3-175">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="202e3-176">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="202e3-176">ReadOnly</span></span>  <br/> |<span data-ttu-id="202e3-177">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="202e3-177">xsd:boolean</span></span>  <br/> |<span data-ttu-id="202e3-178">Optional</span><span class="sxs-lookup"><span data-stu-id="202e3-178">optional</span></span>  <br/> ||<span data-ttu-id="202e3-179">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="202e3-179">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="202e3-180">Blatt</span><span class="sxs-lookup"><span data-stu-id="202e3-180">Sheet</span></span>  <br/> |<span data-ttu-id="202e3-181">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="202e3-181">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="202e3-182">Optional</span><span class="sxs-lookup"><span data-stu-id="202e3-182">optional</span></span>  <br/> ||<span data-ttu-id="202e3-183">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="202e3-183">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="202e3-184">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="202e3-184">ViewCenterX</span></span>  <br/> |<span data-ttu-id="202e3-185">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="202e3-185">xsd:double</span></span>  <br/> |<span data-ttu-id="202e3-186">Optional</span><span class="sxs-lookup"><span data-stu-id="202e3-186">optional</span></span>  <br/> ||<span data-ttu-id="202e3-187">Werte des Typs XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="202e3-187">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="202e3-188">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="202e3-188">ViewCenterY</span></span>  <br/> |<span data-ttu-id="202e3-189">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="202e3-189">xsd:double</span></span>  <br/> |<span data-ttu-id="202e3-190">Optional</span><span class="sxs-lookup"><span data-stu-id="202e3-190">optional</span></span>  <br/> ||<span data-ttu-id="202e3-191">Werte des Typs XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="202e3-191">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="202e3-192">ViewScale</span><span class="sxs-lookup"><span data-stu-id="202e3-192">ViewScale</span></span>  <br/> |<span data-ttu-id="202e3-193">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="202e3-193">xsd:double</span></span>  <br/> |<span data-ttu-id="202e3-194">Optional</span><span class="sxs-lookup"><span data-stu-id="202e3-194">optional</span></span>  <br/> ||<span data-ttu-id="202e3-195">Werte des Typs XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="202e3-195">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="202e3-196">WindowHeight</span><span class="sxs-lookup"><span data-stu-id="202e3-196">WindowHeight</span></span>  <br/> |<span data-ttu-id="202e3-197">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="202e3-197">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="202e3-198">Optional</span><span class="sxs-lookup"><span data-stu-id="202e3-198">optional</span></span>  <br/> ||<span data-ttu-id="202e3-199">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="202e3-199">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="202e3-200">WindowLeft</span><span class="sxs-lookup"><span data-stu-id="202e3-200">WindowLeft</span></span>  <br/> |<span data-ttu-id="202e3-201">XSD: Short</span><span class="sxs-lookup"><span data-stu-id="202e3-201">xsd:short</span></span>  <br/> |<span data-ttu-id="202e3-202">Optional</span><span class="sxs-lookup"><span data-stu-id="202e3-202">optional</span></span>  <br/> ||<span data-ttu-id="202e3-203">Werte des XSD: Short-Typs.</span><span class="sxs-lookup"><span data-stu-id="202e3-203">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="202e3-204">WindowState</span><span class="sxs-lookup"><span data-stu-id="202e3-204">WindowState</span></span>  <br/> |<span data-ttu-id="202e3-205">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="202e3-205">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="202e3-206">Optional</span><span class="sxs-lookup"><span data-stu-id="202e3-206">optional</span></span>  <br/> ||<span data-ttu-id="202e3-207">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="202e3-207">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="202e3-208">WindowTop</span><span class="sxs-lookup"><span data-stu-id="202e3-208">WindowTop</span></span>  <br/> |<span data-ttu-id="202e3-209">XSD: Short</span><span class="sxs-lookup"><span data-stu-id="202e3-209">xsd:short</span></span>  <br/> |<span data-ttu-id="202e3-210">Optional</span><span class="sxs-lookup"><span data-stu-id="202e3-210">optional</span></span>  <br/> ||<span data-ttu-id="202e3-211">Werte des XSD: Short-Typs.</span><span class="sxs-lookup"><span data-stu-id="202e3-211">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="202e3-212">WindowType</span><span class="sxs-lookup"><span data-stu-id="202e3-212">WindowType</span></span>  <br/> |<span data-ttu-id="202e3-213">XSD: Token</span><span class="sxs-lookup"><span data-stu-id="202e3-213">xsd:token</span></span>  <br/> |<span data-ttu-id="202e3-214">erforderlich</span><span class="sxs-lookup"><span data-stu-id="202e3-214">required</span></span>  <br/> ||<span data-ttu-id="202e3-215">Werte des XSD: Token-Typs.</span><span class="sxs-lookup"><span data-stu-id="202e3-215">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="202e3-216">WindowWidth</span><span class="sxs-lookup"><span data-stu-id="202e3-216">WindowWidth</span></span>  <br/> |<span data-ttu-id="202e3-217">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="202e3-217">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="202e3-218">Optional</span><span class="sxs-lookup"><span data-stu-id="202e3-218">optional</span></span>  <br/> ||<span data-ttu-id="202e3-219">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="202e3-219">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

