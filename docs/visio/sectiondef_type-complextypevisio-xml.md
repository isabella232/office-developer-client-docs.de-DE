---
title: SectionDef_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ab57bf2-0d9f-4a3a-4882-c77d7c781cbd
ms.openlocfilehash: 1d13cf54861435aea2ce0b3aade955575d538891
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326075"
---
# <a name="sectiondeftype-complextype-visio-xml"></a><span data-ttu-id="6bf93-102">SectionDef_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="6bf93-102">SectionDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6bf93-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="6bf93-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6bf93-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6bf93-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6bf93-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="6bf93-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6bf93-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="6bf93-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6bf93-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="6bf93-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6bf93-108">Keine</span><span class="sxs-lookup"><span data-stu-id="6bf93-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6bf93-109">Definition</span><span class="sxs-lookup"><span data-stu-id="6bf93-109">Definition</span></span>

```XML
          <xs:complexType name="SectionDef_Type">
          
          <xs:sequence>
    <xs:element name="CellDef"  type="CellDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RowDef"  type="RowDef_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="T"
  type="xsd:string"
    />
    <xs:attribute name="S"
  type="xsd:unsignedByte"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6bf93-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="6bf93-110">Elements and attributes</span></span>

<span data-ttu-id="6bf93-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="6bf93-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6bf93-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6bf93-112">Child elements</span></span>

|<span data-ttu-id="6bf93-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6bf93-113">**Element**</span></span>|<span data-ttu-id="6bf93-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="6bf93-114">**Type**</span></span>|<span data-ttu-id="6bf93-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6bf93-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6bf93-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="6bf93-116">CellDef</span></span> <br/> |[<span data-ttu-id="6bf93-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="6bf93-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="6bf93-118">RowDef</span><span class="sxs-lookup"><span data-stu-id="6bf93-118">RowDef</span></span> <br/> |[<span data-ttu-id="6bf93-119">RowDef_Type</span><span class="sxs-lookup"><span data-stu-id="6bf93-119">RowDef_Type</span></span>](rowdef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6bf93-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="6bf93-120">Attributes</span></span>

|<span data-ttu-id="6bf93-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="6bf93-121">**Attribute**</span></span>|<span data-ttu-id="6bf93-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="6bf93-122">**Type**</span></span>|<span data-ttu-id="6bf93-123">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="6bf93-123">**Required**</span></span>|<span data-ttu-id="6bf93-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6bf93-124">**Description**</span></span>|<span data-ttu-id="6bf93-125">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="6bf93-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6bf93-126">N</span><span class="sxs-lookup"><span data-stu-id="6bf93-126">N</span></span>  <br/> |<span data-ttu-id="6bf93-127">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6bf93-127">xsd:string</span></span>  <br/> |<span data-ttu-id="6bf93-128">erforderlich</span><span class="sxs-lookup"><span data-stu-id="6bf93-128">required</span></span>  <br/> ||<span data-ttu-id="6bf93-129">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="6bf93-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6bf93-130">S</span><span class="sxs-lookup"><span data-stu-id="6bf93-130">S</span></span>  <br/> |<span data-ttu-id="6bf93-131">XSD: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="6bf93-131">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="6bf93-132">Optional</span><span class="sxs-lookup"><span data-stu-id="6bf93-132">optional</span></span>  <br/> ||<span data-ttu-id="6bf93-133">Werte des XSD: unsignedByte-Typs.</span><span class="sxs-lookup"><span data-stu-id="6bf93-133">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="6bf93-134">T</span><span class="sxs-lookup"><span data-stu-id="6bf93-134">T</span></span>  <br/> |<span data-ttu-id="6bf93-135">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6bf93-135">xsd:string</span></span>  <br/> |<span data-ttu-id="6bf93-136">Optional</span><span class="sxs-lookup"><span data-stu-id="6bf93-136">optional</span></span>  <br/> ||<span data-ttu-id="6bf93-137">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="6bf93-137">Values of the xsd:string type.</span></span>  <br/> |
   

