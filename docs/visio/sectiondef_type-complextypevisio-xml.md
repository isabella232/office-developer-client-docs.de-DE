---
title: SectionDef_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ab57bf2-0d9f-4a3a-4882-c77d7c781cbd
ms.openlocfilehash: cd85dd97a8de7bc9a9ca34fd19669dd294fe6905
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589756"
---
# <a name="sectiondeftype-complextype-visio-xml"></a><span data-ttu-id="f04eb-102">SectionDef_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="f04eb-102">SectionDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f04eb-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="f04eb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f04eb-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f04eb-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f04eb-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="f04eb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f04eb-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f04eb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f04eb-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="f04eb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f04eb-108">Keine</span><span class="sxs-lookup"><span data-stu-id="f04eb-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f04eb-109">Definition</span><span class="sxs-lookup"><span data-stu-id="f04eb-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f04eb-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="f04eb-110">Elements and attributes</span></span>

<span data-ttu-id="f04eb-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="f04eb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f04eb-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f04eb-112">Child elements</span></span>

|<span data-ttu-id="f04eb-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f04eb-113">**Element**</span></span>|<span data-ttu-id="f04eb-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f04eb-114">**Type**</span></span>|<span data-ttu-id="f04eb-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f04eb-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f04eb-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="f04eb-116">CellDef</span></span> <br/> |[<span data-ttu-id="f04eb-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="f04eb-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="f04eb-118">RowDef</span><span class="sxs-lookup"><span data-stu-id="f04eb-118">RowDef</span></span> <br/> |[<span data-ttu-id="f04eb-119">RowDef_Type</span><span class="sxs-lookup"><span data-stu-id="f04eb-119">RowDef_Type</span></span>](rowdef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f04eb-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="f04eb-120">Attributes</span></span>

|<span data-ttu-id="f04eb-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f04eb-121">**Attribute**</span></span>|<span data-ttu-id="f04eb-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f04eb-122">**Type**</span></span>|<span data-ttu-id="f04eb-123">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="f04eb-123">**Required**</span></span>|<span data-ttu-id="f04eb-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f04eb-124">**Description**</span></span>|<span data-ttu-id="f04eb-125">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="f04eb-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f04eb-126">N</span><span class="sxs-lookup"><span data-stu-id="f04eb-126">N</span></span>  <br/> |<span data-ttu-id="f04eb-127">XSD: String</span><span class="sxs-lookup"><span data-stu-id="f04eb-127">xsd:string</span></span>  <br/> |<span data-ttu-id="f04eb-128">erforderlich</span><span class="sxs-lookup"><span data-stu-id="f04eb-128">required</span></span>  <br/> ||<span data-ttu-id="f04eb-129">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f04eb-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f04eb-130">S</span><span class="sxs-lookup"><span data-stu-id="f04eb-130">S</span></span>  <br/> |<span data-ttu-id="f04eb-131">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="f04eb-131">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="f04eb-132">Optional</span><span class="sxs-lookup"><span data-stu-id="f04eb-132">optional</span></span>  <br/> ||<span data-ttu-id="f04eb-133">Werte des Typs Xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="f04eb-133">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="f04eb-134">T</span><span class="sxs-lookup"><span data-stu-id="f04eb-134">T</span></span>  <br/> |<span data-ttu-id="f04eb-135">XSD: String</span><span class="sxs-lookup"><span data-stu-id="f04eb-135">xsd:string</span></span>  <br/> |<span data-ttu-id="f04eb-136">Optional</span><span class="sxs-lookup"><span data-stu-id="f04eb-136">optional</span></span>  <br/> ||<span data-ttu-id="f04eb-137">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f04eb-137">Values of the xsd:string type.</span></span>  <br/> |
   

