---
title: Sheet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4855350c-8204-ef1f-4d08-4ab6540249e9
ms.openlocfilehash: b747f2257f2b09083b72a17a59856be0a985b270
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540406"
---
# <a name="sheettype-complextype-visio-xml"></a><span data-ttu-id="0feae-102">Sheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="0feae-102">Sheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="0feae-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="0feae-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0feae-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0feae-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0feae-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="0feae-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0feae-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="0feae-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0feae-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="0feae-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0feae-108">Keine</span><span class="sxs-lookup"><span data-stu-id="0feae-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0feae-109">Definition</span><span class="sxs-lookup"><span data-stu-id="0feae-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0feae-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="0feae-110">Elements and attributes</span></span>

<span data-ttu-id="0feae-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="0feae-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0feae-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0feae-112">Child elements</span></span>

|<span data-ttu-id="0feae-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0feae-113">**Element**</span></span>|<span data-ttu-id="0feae-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="0feae-114">**Type**</span></span>|<span data-ttu-id="0feae-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0feae-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0feae-116">Cell</span><span class="sxs-lookup"><span data-stu-id="0feae-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="0feae-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="0feae-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0feae-118">Section</span><span class="sxs-lookup"><span data-stu-id="0feae-118">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0feae-119">Section_Type</span><span class="sxs-lookup"><span data-stu-id="0feae-119">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0feae-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="0feae-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="0feae-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="0feae-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0feae-122">Attribute</span><span class="sxs-lookup"><span data-stu-id="0feae-122">Attributes</span></span>

|<span data-ttu-id="0feae-123">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0feae-123">**Attribute**</span></span>|<span data-ttu-id="0feae-124">**Typ**</span><span class="sxs-lookup"><span data-stu-id="0feae-124">**Type**</span></span>|<span data-ttu-id="0feae-125">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="0feae-125">**Required**</span></span>|<span data-ttu-id="0feae-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0feae-126">**Description**</span></span>|<span data-ttu-id="0feae-127">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="0feae-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0feae-128">FillStyle</span><span class="sxs-lookup"><span data-stu-id="0feae-128">FillStyle</span></span>  <br/> |<span data-ttu-id="0feae-129">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0feae-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0feae-130">Optional</span><span class="sxs-lookup"><span data-stu-id="0feae-130">optional</span></span>  <br/> ||<span data-ttu-id="0feae-131">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="0feae-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0feae-132">LineStyle</span><span class="sxs-lookup"><span data-stu-id="0feae-132">LineStyle</span></span>  <br/> |<span data-ttu-id="0feae-133">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0feae-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0feae-134">Optional</span><span class="sxs-lookup"><span data-stu-id="0feae-134">optional</span></span>  <br/> ||<span data-ttu-id="0feae-135">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="0feae-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0feae-136">TextStyle</span><span class="sxs-lookup"><span data-stu-id="0feae-136">TextStyle</span></span>  <br/> |<span data-ttu-id="0feae-137">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0feae-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0feae-138">Optional</span><span class="sxs-lookup"><span data-stu-id="0feae-138">optional</span></span>  <br/> ||<span data-ttu-id="0feae-139">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="0feae-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

