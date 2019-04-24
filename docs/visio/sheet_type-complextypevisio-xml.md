---
title: Sheet_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4855350c-8204-ef1f-4d08-4ab6540249e9
ms.openlocfilehash: dc8930ffa89baf059074a12bb285e6b53e329e41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342868"
---
# <a name="sheettype-complextype-visio-xml"></a><span data-ttu-id="85b7d-102">Sheet_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="85b7d-102">Sheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="85b7d-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="85b7d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85b7d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="85b7d-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="85b7d-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="85b7d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="85b7d-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="85b7d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="85b7d-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="85b7d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="85b7d-108">Keine</span><span class="sxs-lookup"><span data-stu-id="85b7d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="85b7d-109">Definition</span><span class="sxs-lookup"><span data-stu-id="85b7d-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="85b7d-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="85b7d-110">Elements and attributes</span></span>

<span data-ttu-id="85b7d-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="85b7d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="85b7d-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="85b7d-112">Child elements</span></span>

|<span data-ttu-id="85b7d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="85b7d-113">**Element**</span></span>|<span data-ttu-id="85b7d-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="85b7d-114">**Type**</span></span>|<span data-ttu-id="85b7d-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="85b7d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="85b7d-116">Cell</span><span class="sxs-lookup"><span data-stu-id="85b7d-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="85b7d-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="85b7d-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="85b7d-118">Section</span><span class="sxs-lookup"><span data-stu-id="85b7d-118">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="85b7d-119">Section_Type</span><span class="sxs-lookup"><span data-stu-id="85b7d-119">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="85b7d-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="85b7d-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="85b7d-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="85b7d-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="85b7d-122">Attribute</span><span class="sxs-lookup"><span data-stu-id="85b7d-122">Attributes</span></span>

|<span data-ttu-id="85b7d-123">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="85b7d-123">**Attribute**</span></span>|<span data-ttu-id="85b7d-124">**Typ**</span><span class="sxs-lookup"><span data-stu-id="85b7d-124">**Type**</span></span>|<span data-ttu-id="85b7d-125">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="85b7d-125">**Required**</span></span>|<span data-ttu-id="85b7d-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="85b7d-126">**Description**</span></span>|<span data-ttu-id="85b7d-127">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="85b7d-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="85b7d-128">FillStyle</span><span class="sxs-lookup"><span data-stu-id="85b7d-128">FillStyle</span></span>  <br/> |<span data-ttu-id="85b7d-129">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="85b7d-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="85b7d-130">Optional</span><span class="sxs-lookup"><span data-stu-id="85b7d-130">optional</span></span>  <br/> ||<span data-ttu-id="85b7d-131">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="85b7d-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="85b7d-132">LineStyle</span><span class="sxs-lookup"><span data-stu-id="85b7d-132">LineStyle</span></span>  <br/> |<span data-ttu-id="85b7d-133">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="85b7d-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="85b7d-134">Optional</span><span class="sxs-lookup"><span data-stu-id="85b7d-134">optional</span></span>  <br/> ||<span data-ttu-id="85b7d-135">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="85b7d-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="85b7d-136">TextStyle</span><span class="sxs-lookup"><span data-stu-id="85b7d-136">TextStyle</span></span>  <br/> |<span data-ttu-id="85b7d-137">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="85b7d-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="85b7d-138">Optional</span><span class="sxs-lookup"><span data-stu-id="85b7d-138">optional</span></span>  <br/> ||<span data-ttu-id="85b7d-139">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="85b7d-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

