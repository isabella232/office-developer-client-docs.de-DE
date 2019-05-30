---
title: SectionDef_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ab57bf2-0d9f-4a3a-4882-c77d7c781cbd
ms.openlocfilehash: 96812d1911d249ebce02aeab20b0a77ef518fbff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542079"
---
# <a name="sectiondeftype-complextype-visio-xml"></a><span data-ttu-id="d89c5-102">SectionDef_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="d89c5-102">SectionDef_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="d89c5-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="d89c5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d89c5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d89c5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d89c5-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="d89c5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d89c5-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="d89c5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d89c5-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="d89c5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d89c5-108">Keine</span><span class="sxs-lookup"><span data-stu-id="d89c5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d89c5-109">Definition</span><span class="sxs-lookup"><span data-stu-id="d89c5-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d89c5-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="d89c5-110">Elements and attributes</span></span>

<span data-ttu-id="d89c5-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="d89c5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d89c5-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d89c5-112">Child elements</span></span>

|<span data-ttu-id="d89c5-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d89c5-113">**Element**</span></span>|<span data-ttu-id="d89c5-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d89c5-114">**Type**</span></span>|<span data-ttu-id="d89c5-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d89c5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d89c5-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="d89c5-116">CellDef</span></span> <br/> |[<span data-ttu-id="d89c5-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="d89c5-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="d89c5-118">RowDef</span><span class="sxs-lookup"><span data-stu-id="d89c5-118">RowDef</span></span> <br/> |[<span data-ttu-id="d89c5-119">RowDef_Type</span><span class="sxs-lookup"><span data-stu-id="d89c5-119">RowDef_Type</span></span>](rowdef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d89c5-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="d89c5-120">Attributes</span></span>

|<span data-ttu-id="d89c5-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d89c5-121">**Attribute**</span></span>|<span data-ttu-id="d89c5-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d89c5-122">**Type**</span></span>|<span data-ttu-id="d89c5-123">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d89c5-123">**Required**</span></span>|<span data-ttu-id="d89c5-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d89c5-124">**Description**</span></span>|<span data-ttu-id="d89c5-125">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="d89c5-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d89c5-126">N</span><span class="sxs-lookup"><span data-stu-id="d89c5-126">N</span></span>  <br/> |<span data-ttu-id="d89c5-127">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d89c5-127">xsd:string</span></span>  <br/> |<span data-ttu-id="d89c5-128">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d89c5-128">required</span></span>  <br/> ||<span data-ttu-id="d89c5-129">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="d89c5-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d89c5-130">S</span><span class="sxs-lookup"><span data-stu-id="d89c5-130">S</span></span>  <br/> |<span data-ttu-id="d89c5-131">XSD: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="d89c5-131">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="d89c5-132">Optional</span><span class="sxs-lookup"><span data-stu-id="d89c5-132">optional</span></span>  <br/> ||<span data-ttu-id="d89c5-133">Werte des XSD: unsignedByte-Typs.</span><span class="sxs-lookup"><span data-stu-id="d89c5-133">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="d89c5-134">T</span><span class="sxs-lookup"><span data-stu-id="d89c5-134">T</span></span>  <br/> |<span data-ttu-id="d89c5-135">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d89c5-135">xsd:string</span></span>  <br/> |<span data-ttu-id="d89c5-136">Optional</span><span class="sxs-lookup"><span data-stu-id="d89c5-136">optional</span></span>  <br/> ||<span data-ttu-id="d89c5-137">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="d89c5-137">Values of the xsd:string type.</span></span>  <br/> |
   

