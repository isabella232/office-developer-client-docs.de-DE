---
title: Sheet_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4855350c-8204-ef1f-4d08-4ab6540249e9
ms.openlocfilehash: dc8930ffa89baf059074a12bb285e6b53e329e41
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388749"
---
# <a name="sheettype-complextype-visio-xml"></a><span data-ttu-id="13141-102">Sheet_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="13141-102">Sheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="13141-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="13141-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="13141-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="13141-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="13141-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="13141-105">**Schema file**</span></span> <br/> |<span data-ttu-id="13141-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="13141-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="13141-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="13141-107">**Extension base**</span></span> <br/> |<span data-ttu-id="13141-108">Keine</span><span class="sxs-lookup"><span data-stu-id="13141-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="13141-109">Definition</span><span class="sxs-lookup"><span data-stu-id="13141-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="13141-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="13141-110">Elements and attributes</span></span>

<span data-ttu-id="13141-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="13141-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="13141-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="13141-112">Child elements</span></span>

|<span data-ttu-id="13141-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="13141-113">**Element**</span></span>|<span data-ttu-id="13141-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="13141-114">**Type**</span></span>|<span data-ttu-id="13141-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="13141-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="13141-116">Cell</span><span class="sxs-lookup"><span data-stu-id="13141-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="13141-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="13141-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="13141-118">Section</span><span class="sxs-lookup"><span data-stu-id="13141-118">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="13141-119">Section_Type</span><span class="sxs-lookup"><span data-stu-id="13141-119">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="13141-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="13141-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="13141-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="13141-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="13141-122">Attribute</span><span class="sxs-lookup"><span data-stu-id="13141-122">Attributes</span></span>

|<span data-ttu-id="13141-123">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="13141-123">**Attribute**</span></span>|<span data-ttu-id="13141-124">**Typ**</span><span class="sxs-lookup"><span data-stu-id="13141-124">**Type**</span></span>|<span data-ttu-id="13141-125">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="13141-125">**Required**</span></span>|<span data-ttu-id="13141-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="13141-126">**Description**</span></span>|<span data-ttu-id="13141-127">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="13141-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="13141-128">FillStyle</span><span class="sxs-lookup"><span data-stu-id="13141-128">FillStyle</span></span>  <br/> |<span data-ttu-id="13141-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="13141-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="13141-130">Optional</span><span class="sxs-lookup"><span data-stu-id="13141-130">optional</span></span>  <br/> ||<span data-ttu-id="13141-131">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="13141-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="13141-132">LineStyle</span><span class="sxs-lookup"><span data-stu-id="13141-132">LineStyle</span></span>  <br/> |<span data-ttu-id="13141-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="13141-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="13141-134">Optional</span><span class="sxs-lookup"><span data-stu-id="13141-134">optional</span></span>  <br/> ||<span data-ttu-id="13141-135">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="13141-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="13141-136">TextStyle</span><span class="sxs-lookup"><span data-stu-id="13141-136">TextStyle</span></span>  <br/> |<span data-ttu-id="13141-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="13141-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="13141-138">Optional</span><span class="sxs-lookup"><span data-stu-id="13141-138">optional</span></span>  <br/> ||<span data-ttu-id="13141-139">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="13141-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

