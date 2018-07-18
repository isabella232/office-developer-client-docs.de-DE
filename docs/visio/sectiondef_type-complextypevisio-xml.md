---
title: SectionDef_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ab57bf2-0d9f-4a3a-4882-c77d7c781cbd
ms.openlocfilehash: 426e62ea7a9f990555776e3ac732dd43e614582d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797985"
---
# <a name="sectiondeftype-complextype-visio-xml"></a><span data-ttu-id="811be-102">SectionDef_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="811be-102">SectionDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="811be-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="811be-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="811be-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="811be-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="811be-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="811be-105">**Schema file**</span></span> <br/> |<span data-ttu-id="811be-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="811be-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="811be-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="811be-107">**Extension base**</span></span> <br/> |<span data-ttu-id="811be-108">Keine</span><span class="sxs-lookup"><span data-stu-id="811be-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="811be-109">Definition</span><span class="sxs-lookup"><span data-stu-id="811be-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="811be-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="811be-110">Elements and attributes</span></span>

<span data-ttu-id="811be-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="811be-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="811be-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="811be-112">Child elements</span></span>

|<span data-ttu-id="811be-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="811be-113">**Element**</span></span>|<span data-ttu-id="811be-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="811be-114">**Type**</span></span>|<span data-ttu-id="811be-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="811be-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="811be-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="811be-116">CellDef</span></span>](http://msdn.microsoft.com/library/f0ec7afe-9e0a-b5e5-82dd-4adff1c1607f%28Office.15%29.aspx) <br/> |[<span data-ttu-id="811be-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="811be-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="811be-118">RowDef</span><span class="sxs-lookup"><span data-stu-id="811be-118">RowDef</span></span>](http://msdn.microsoft.com/library/25615be9-1d19-1ba9-4192-7d4a0dfae717%28Office.15%29.aspx) <br/> |[<span data-ttu-id="811be-119">RowDef_Type</span><span class="sxs-lookup"><span data-stu-id="811be-119">RowDef_Type</span></span>](rowdef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="811be-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="811be-120">Attributes</span></span>

|<span data-ttu-id="811be-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="811be-121">**Attribute**</span></span>|<span data-ttu-id="811be-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="811be-122">**Type**</span></span>|<span data-ttu-id="811be-123">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="811be-123">**Required**</span></span>|<span data-ttu-id="811be-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="811be-124">**Description**</span></span>|<span data-ttu-id="811be-125">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="811be-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="811be-126">N</span><span class="sxs-lookup"><span data-stu-id="811be-126">N</span></span>  <br/> |<span data-ttu-id="811be-127">XSD: String</span><span class="sxs-lookup"><span data-stu-id="811be-127">xsd:string</span></span>  <br/> |<span data-ttu-id="811be-128">erforderlich</span><span class="sxs-lookup"><span data-stu-id="811be-128">required</span></span>  <br/> ||<span data-ttu-id="811be-129">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="811be-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="811be-130">S</span><span class="sxs-lookup"><span data-stu-id="811be-130">S</span></span>  <br/> |<span data-ttu-id="811be-131">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="811be-131">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="811be-132">Optional</span><span class="sxs-lookup"><span data-stu-id="811be-132">optional</span></span>  <br/> ||<span data-ttu-id="811be-133">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="811be-133">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="811be-134">T</span><span class="sxs-lookup"><span data-stu-id="811be-134">T</span></span>  <br/> |<span data-ttu-id="811be-135">XSD: String</span><span class="sxs-lookup"><span data-stu-id="811be-135">xsd:string</span></span>  <br/> |<span data-ttu-id="811be-136">Optional</span><span class="sxs-lookup"><span data-stu-id="811be-136">optional</span></span>  <br/> ||<span data-ttu-id="811be-137">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="811be-137">Values of the xsd:string type.</span></span>  <br/> |
   

