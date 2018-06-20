---
title: Sheet_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4855350c-8204-ef1f-4d08-4ab6540249e9
ms.openlocfilehash: f171f250fbe37ebf1d0d434709b06ab56804407f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798082"
---
# <a name="sheettype-complextype-visio-xml"></a><span data-ttu-id="3556d-102">Sheet_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="3556d-102">Sheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="3556d-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="3556d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3556d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3556d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3556d-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="3556d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3556d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3556d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3556d-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="3556d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3556d-108">Keine</span><span class="sxs-lookup"><span data-stu-id="3556d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3556d-109">Definition</span><span class="sxs-lookup"><span data-stu-id="3556d-109">Definition</span></span>

```XML
        <xs:complexType name="Sheet_Type" abstract="true">
        
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="Trigger"  type="Trigger_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="Section"  type="Section_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs: name="" >
    </xs:>
    
      </xs:sequence>
    <xs:attribute name="LineStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="FillStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="TextStyle"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3556d-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="3556d-110">Elements and attributes</span></span>

<span data-ttu-id="3556d-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="3556d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3556d-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3556d-112">Child elements</span></span>

|<span data-ttu-id="3556d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3556d-113">**Element**</span></span>|<span data-ttu-id="3556d-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="3556d-114">**Type**</span></span>|<span data-ttu-id="3556d-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3556d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3556d-116">Cell</span><span class="sxs-lookup"><span data-stu-id="3556d-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="3556d-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="3556d-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="3556d-118">Section</span><span class="sxs-lookup"><span data-stu-id="3556d-118">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3556d-119">Section_Type</span><span class="sxs-lookup"><span data-stu-id="3556d-119">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="3556d-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="3556d-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="3556d-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="3556d-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="3556d-122">Attribute</span><span class="sxs-lookup"><span data-stu-id="3556d-122">Attributes</span></span>

|<span data-ttu-id="3556d-123">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="3556d-123">**Attribute**</span></span>|<span data-ttu-id="3556d-124">**Typ**</span><span class="sxs-lookup"><span data-stu-id="3556d-124">**Type**</span></span>|<span data-ttu-id="3556d-125">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="3556d-125">**Required**</span></span>|<span data-ttu-id="3556d-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3556d-126">**Description**</span></span>|<span data-ttu-id="3556d-127">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="3556d-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3556d-128">FillStyle</span><span class="sxs-lookup"><span data-stu-id="3556d-128">FillStyle</span></span>  <br/> |<span data-ttu-id="3556d-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3556d-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3556d-130">Optional</span><span class="sxs-lookup"><span data-stu-id="3556d-130">optional</span></span>  <br/> ||<span data-ttu-id="3556d-131">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3556d-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3556d-132">LineStyle</span><span class="sxs-lookup"><span data-stu-id="3556d-132">LineStyle</span></span>  <br/> |<span data-ttu-id="3556d-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3556d-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3556d-134">Optional</span><span class="sxs-lookup"><span data-stu-id="3556d-134">optional</span></span>  <br/> ||<span data-ttu-id="3556d-135">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3556d-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3556d-136">TextStyle</span><span class="sxs-lookup"><span data-stu-id="3556d-136">TextStyle</span></span>  <br/> |<span data-ttu-id="3556d-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3556d-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3556d-138">Optional</span><span class="sxs-lookup"><span data-stu-id="3556d-138">optional</span></span>  <br/> ||<span data-ttu-id="3556d-139">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3556d-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

