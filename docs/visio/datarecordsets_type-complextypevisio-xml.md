---
title: DataRecordSets_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04448cfa-7eb4-62ca-97d2-409b59a8db90
ms.openlocfilehash: b646e7a0d4e1f49aa71b162aecdd901813b01f49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796799"
---
# <a name="datarecordsetstype-complextype-visio-xml"></a><span data-ttu-id="6d4ef-102">DataRecordSets_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="6d4ef-102">DataRecordSets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6d4ef-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="6d4ef-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6d4ef-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6d4ef-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6d4ef-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="6d4ef-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6d4ef-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6d4ef-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6d4ef-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="6d4ef-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6d4ef-108">Keine</span><span class="sxs-lookup"><span data-stu-id="6d4ef-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6d4ef-109">Definition</span><span class="sxs-lookup"><span data-stu-id="6d4ef-109">Definition</span></span>

```XML
          <xs:complexType name="DataRecordSets_Type">
          
          <xs:sequence>
    <xs:element name="DataRecordSet"  type="DataRecordSet_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="NextID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ActiveRecordsetID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DataWindowOrder"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6d4ef-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="6d4ef-110">Elements and attributes</span></span>

<span data-ttu-id="6d4ef-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="6d4ef-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6d4ef-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6d4ef-112">Child elements</span></span>

|<span data-ttu-id="6d4ef-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6d4ef-113">**Element**</span></span>|<span data-ttu-id="6d4ef-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="6d4ef-114">**Type**</span></span>|<span data-ttu-id="6d4ef-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6d4ef-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6d4ef-116">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="6d4ef-116">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6d4ef-117">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="6d4ef-117">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6d4ef-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="6d4ef-118">Attributes</span></span>

|<span data-ttu-id="6d4ef-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="6d4ef-119">**Attribute**</span></span>|<span data-ttu-id="6d4ef-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="6d4ef-120">**Type**</span></span>|<span data-ttu-id="6d4ef-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="6d4ef-121">**Required**</span></span>|<span data-ttu-id="6d4ef-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6d4ef-122">**Description**</span></span>|<span data-ttu-id="6d4ef-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="6d4ef-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6d4ef-124">ActiveRecordsetID</span><span class="sxs-lookup"><span data-stu-id="6d4ef-124">ActiveRecordsetID</span></span>  <br/> |<span data-ttu-id="6d4ef-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6d4ef-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6d4ef-126">Optional</span><span class="sxs-lookup"><span data-stu-id="6d4ef-126">optional</span></span>  <br/> ||<span data-ttu-id="6d4ef-127">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6d4ef-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6d4ef-128">DataWindowOrder</span><span class="sxs-lookup"><span data-stu-id="6d4ef-128">DataWindowOrder</span></span>  <br/> |<span data-ttu-id="6d4ef-129">XSD: String</span><span class="sxs-lookup"><span data-stu-id="6d4ef-129">xsd:string</span></span>  <br/> |<span data-ttu-id="6d4ef-130">Optional</span><span class="sxs-lookup"><span data-stu-id="6d4ef-130">optional</span></span>  <br/> ||<span data-ttu-id="6d4ef-131">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="6d4ef-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6d4ef-132">NextID</span><span class="sxs-lookup"><span data-stu-id="6d4ef-132">NextID</span></span>  <br/> |<span data-ttu-id="6d4ef-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6d4ef-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6d4ef-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="6d4ef-134">required</span></span>  <br/> ||<span data-ttu-id="6d4ef-135">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6d4ef-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

