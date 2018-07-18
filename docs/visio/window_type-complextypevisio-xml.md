---
title: Window_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c514ce79-0920-4f1b-5332-0bdef146e802
ms.openlocfilehash: dc4dda48c037f7af03ee22a07bee288ce5d30872
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798416"
---
# <a name="windowtype-complextype-visio-xml"></a><span data-ttu-id="c3404-102">Window_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="c3404-102">Window_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c3404-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="c3404-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c3404-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c3404-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c3404-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="c3404-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c3404-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c3404-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c3404-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="c3404-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c3404-108">Keine</span><span class="sxs-lookup"><span data-stu-id="c3404-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c3404-109">Definition</span><span class="sxs-lookup"><span data-stu-id="c3404-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c3404-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="c3404-110">Elements and attributes</span></span>

<span data-ttu-id="c3404-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="c3404-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c3404-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c3404-112">Child elements</span></span>

|<span data-ttu-id="c3404-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c3404-113">**Element**</span></span>|<span data-ttu-id="c3404-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c3404-114">**Type**</span></span>|<span data-ttu-id="c3404-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c3404-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c3404-116">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="c3404-116">DynamicGridEnabled</span></span>](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c3404-117">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="c3404-117">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c3404-118">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="c3404-118">GlueSettings</span></span>](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c3404-119">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="c3404-119">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c3404-120">ShowConnectionPoints</span><span class="sxs-lookup"><span data-stu-id="c3404-120">ShowConnectionPoints</span></span>](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c3404-121">ShowConnectionPoints_Type</span><span class="sxs-lookup"><span data-stu-id="c3404-121">ShowConnectionPoints_Type</span></span>](showconnectionpoints_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c3404-122">ShowGrid</span><span class="sxs-lookup"><span data-stu-id="c3404-122">ShowGrid</span></span>](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c3404-123">ShowGrid_Type</span><span class="sxs-lookup"><span data-stu-id="c3404-123">ShowGrid_Type</span></span>](showgrid_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c3404-124">ShowGuides</span><span class="sxs-lookup"><span data-stu-id="c3404-124">ShowGuides</span></span>](showguides-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c3404-125">ShowGuides_Type</span><span class="sxs-lookup"><span data-stu-id="c3404-125">ShowGuides_Type</span></span>](showguides_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c3404-126">ShowPageBreaks</span><span class="sxs-lookup"><span data-stu-id="c3404-126">ShowPageBreaks</span></span>](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c3404-127">ShowPageBreaks_Type</span><span class="sxs-lookup"><span data-stu-id="c3404-127">ShowPageBreaks_Type</span></span>](showpagebreaks_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c3404-128">ShowRulers</span><span class="sxs-lookup"><span data-stu-id="c3404-128">ShowRulers</span></span>](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c3404-129">ShowRulers_Type</span><span class="sxs-lookup"><span data-stu-id="c3404-129">ShowRulers_Type</span></span>](showrulers_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c3404-130">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="c3404-130">SnapAngles</span></span>](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c3404-131">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="c3404-131">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c3404-132">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="c3404-132">SnapExtensions</span></span>](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c3404-133">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="c3404-133">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c3404-134">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="c3404-134">SnapSettings</span></span>](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c3404-135">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="c3404-135">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c3404-136">StencilGroup</span><span class="sxs-lookup"><span data-stu-id="c3404-136">StencilGroup</span></span>](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c3404-137">StencilGroup_Type</span><span class="sxs-lookup"><span data-stu-id="c3404-137">StencilGroup_Type</span></span>](stencilgroup_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c3404-138">StencilGroupPos</span><span class="sxs-lookup"><span data-stu-id="c3404-138">StencilGroupPos</span></span>](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c3404-139">StencilGroupPos_Type</span><span class="sxs-lookup"><span data-stu-id="c3404-139">StencilGroupPos_Type</span></span>](stencilgrouppos_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c3404-140">TabSplitterPos</span><span class="sxs-lookup"><span data-stu-id="c3404-140">TabSplitterPos</span></span>](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c3404-141">TabSplitterPos_Type</span><span class="sxs-lookup"><span data-stu-id="c3404-141">TabSplitterPos_Type</span></span>](tabsplitterpos_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c3404-142">Attribute</span><span class="sxs-lookup"><span data-stu-id="c3404-142">Attributes</span></span>

|<span data-ttu-id="c3404-143">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c3404-143">**Attribute**</span></span>|<span data-ttu-id="c3404-144">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c3404-144">**Type**</span></span>|<span data-ttu-id="c3404-145">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="c3404-145">**Required**</span></span>|<span data-ttu-id="c3404-146">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c3404-146">**Description**</span></span>|<span data-ttu-id="c3404-147">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="c3404-147">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c3404-148">Container</span><span class="sxs-lookup"><span data-stu-id="c3404-148">Container</span></span>  <br/> |<span data-ttu-id="c3404-149">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c3404-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c3404-150">Optional</span><span class="sxs-lookup"><span data-stu-id="c3404-150">optional</span></span>  <br/> ||<span data-ttu-id="c3404-151">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c3404-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c3404-152">ContainerType</span><span class="sxs-lookup"><span data-stu-id="c3404-152">ContainerType</span></span>  <br/> |<span data-ttu-id="c3404-153">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="c3404-153">xsd:token</span></span>  <br/> |<span data-ttu-id="c3404-154">Optional</span><span class="sxs-lookup"><span data-stu-id="c3404-154">optional</span></span>  <br/> ||<span data-ttu-id="c3404-155">Werte des Typs Xsd:token.</span><span class="sxs-lookup"><span data-stu-id="c3404-155">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="c3404-156">Document</span><span class="sxs-lookup"><span data-stu-id="c3404-156">Document</span></span>  <br/> |<span data-ttu-id="c3404-157">XSD: String</span><span class="sxs-lookup"><span data-stu-id="c3404-157">xsd:string</span></span>  <br/> |<span data-ttu-id="c3404-158">Optional</span><span class="sxs-lookup"><span data-stu-id="c3404-158">optional</span></span>  <br/> ||<span data-ttu-id="c3404-159">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="c3404-159">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c3404-160">ID</span><span class="sxs-lookup"><span data-stu-id="c3404-160">ID</span></span>  <br/> |<span data-ttu-id="c3404-161">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c3404-161">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c3404-162">erforderlich</span><span class="sxs-lookup"><span data-stu-id="c3404-162">required</span></span>  <br/> ||<span data-ttu-id="c3404-163">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c3404-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c3404-164">Master</span><span class="sxs-lookup"><span data-stu-id="c3404-164">Master</span></span>  <br/> |<span data-ttu-id="c3404-165">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c3404-165">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c3404-166">Optional</span><span class="sxs-lookup"><span data-stu-id="c3404-166">optional</span></span>  <br/> ||<span data-ttu-id="c3404-167">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c3404-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c3404-168">Page</span><span class="sxs-lookup"><span data-stu-id="c3404-168">Page</span></span>  <br/> |<span data-ttu-id="c3404-169">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c3404-169">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c3404-170">Optional</span><span class="sxs-lookup"><span data-stu-id="c3404-170">optional</span></span>  <br/> ||<span data-ttu-id="c3404-171">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c3404-171">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c3404-172">ParentWindow</span><span class="sxs-lookup"><span data-stu-id="c3404-172">ParentWindow</span></span>  <br/> |<span data-ttu-id="c3404-173">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c3404-173">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c3404-174">Optional</span><span class="sxs-lookup"><span data-stu-id="c3404-174">optional</span></span>  <br/> ||<span data-ttu-id="c3404-175">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c3404-175">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c3404-176">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="c3404-176">ReadOnly</span></span>  <br/> |<span data-ttu-id="c3404-177">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="c3404-177">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c3404-178">Optional</span><span class="sxs-lookup"><span data-stu-id="c3404-178">optional</span></span>  <br/> ||<span data-ttu-id="c3404-179">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="c3404-179">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c3404-180">Blatt</span><span class="sxs-lookup"><span data-stu-id="c3404-180">Sheet</span></span>  <br/> |<span data-ttu-id="c3404-181">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c3404-181">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c3404-182">Optional</span><span class="sxs-lookup"><span data-stu-id="c3404-182">optional</span></span>  <br/> ||<span data-ttu-id="c3404-183">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c3404-183">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c3404-184">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="c3404-184">ViewCenterX</span></span>  <br/> |<span data-ttu-id="c3404-185">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="c3404-185">xsd:double</span></span>  <br/> |<span data-ttu-id="c3404-186">Optional</span><span class="sxs-lookup"><span data-stu-id="c3404-186">optional</span></span>  <br/> ||<span data-ttu-id="c3404-187">Werte des Typs xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="c3404-187">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="c3404-188">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="c3404-188">ViewCenterY</span></span>  <br/> |<span data-ttu-id="c3404-189">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="c3404-189">xsd:double</span></span>  <br/> |<span data-ttu-id="c3404-190">Optional</span><span class="sxs-lookup"><span data-stu-id="c3404-190">optional</span></span>  <br/> ||<span data-ttu-id="c3404-191">Werte des Typs xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="c3404-191">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="c3404-192">ViewScale</span><span class="sxs-lookup"><span data-stu-id="c3404-192">ViewScale</span></span>  <br/> |<span data-ttu-id="c3404-193">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="c3404-193">xsd:double</span></span>  <br/> |<span data-ttu-id="c3404-194">Optional</span><span class="sxs-lookup"><span data-stu-id="c3404-194">optional</span></span>  <br/> ||<span data-ttu-id="c3404-195">Werte des Typs xsd: Double.</span><span class="sxs-lookup"><span data-stu-id="c3404-195">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="c3404-196">WindowHeight</span><span class="sxs-lookup"><span data-stu-id="c3404-196">WindowHeight</span></span>  <br/> |<span data-ttu-id="c3404-197">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c3404-197">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c3404-198">Optional</span><span class="sxs-lookup"><span data-stu-id="c3404-198">optional</span></span>  <br/> ||<span data-ttu-id="c3404-199">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c3404-199">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c3404-200">WindowLeft</span><span class="sxs-lookup"><span data-stu-id="c3404-200">WindowLeft</span></span>  <br/> |<span data-ttu-id="c3404-201">XSD:Short</span><span class="sxs-lookup"><span data-stu-id="c3404-201">xsd:short</span></span>  <br/> |<span data-ttu-id="c3404-202">Optional</span><span class="sxs-lookup"><span data-stu-id="c3404-202">optional</span></span>  <br/> ||<span data-ttu-id="c3404-203">Werte des Typs Xsd:short.</span><span class="sxs-lookup"><span data-stu-id="c3404-203">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="c3404-204">WindowState</span><span class="sxs-lookup"><span data-stu-id="c3404-204">WindowState</span></span>  <br/> |<span data-ttu-id="c3404-205">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c3404-205">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c3404-206">Optional</span><span class="sxs-lookup"><span data-stu-id="c3404-206">optional</span></span>  <br/> ||<span data-ttu-id="c3404-207">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c3404-207">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c3404-208">WindowTop</span><span class="sxs-lookup"><span data-stu-id="c3404-208">WindowTop</span></span>  <br/> |<span data-ttu-id="c3404-209">XSD:Short</span><span class="sxs-lookup"><span data-stu-id="c3404-209">xsd:short</span></span>  <br/> |<span data-ttu-id="c3404-210">Optional</span><span class="sxs-lookup"><span data-stu-id="c3404-210">optional</span></span>  <br/> ||<span data-ttu-id="c3404-211">Werte des Typs Xsd:short.</span><span class="sxs-lookup"><span data-stu-id="c3404-211">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="c3404-212">Fenstertyp</span><span class="sxs-lookup"><span data-stu-id="c3404-212">WindowType</span></span>  <br/> |<span data-ttu-id="c3404-213">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="c3404-213">xsd:token</span></span>  <br/> |<span data-ttu-id="c3404-214">erforderlich</span><span class="sxs-lookup"><span data-stu-id="c3404-214">required</span></span>  <br/> ||<span data-ttu-id="c3404-215">Werte des Typs Xsd:token.</span><span class="sxs-lookup"><span data-stu-id="c3404-215">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="c3404-216">WindowWidth</span><span class="sxs-lookup"><span data-stu-id="c3404-216">WindowWidth</span></span>  <br/> |<span data-ttu-id="c3404-217">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c3404-217">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c3404-218">Optional</span><span class="sxs-lookup"><span data-stu-id="c3404-218">optional</span></span>  <br/> ||<span data-ttu-id="c3404-219">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c3404-219">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

