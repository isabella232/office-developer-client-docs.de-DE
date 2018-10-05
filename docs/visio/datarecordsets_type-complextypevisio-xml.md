---
title: DataRecordSets_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04448cfa-7eb4-62ca-97d2-409b59a8db90
ms.openlocfilehash: 1705d0ea92e278008c33321f135409373b7317fd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388560"
---
# <a name="datarecordsetstype-complextype-visio-xml"></a><span data-ttu-id="e84a4-102">DataRecordSets_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="e84a4-102">DataRecordSets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e84a4-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="e84a4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e84a4-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e84a4-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e84a4-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="e84a4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e84a4-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e84a4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e84a4-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="e84a4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e84a4-108">Keine</span><span class="sxs-lookup"><span data-stu-id="e84a4-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e84a4-109">Definition</span><span class="sxs-lookup"><span data-stu-id="e84a4-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="e84a4-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="e84a4-110">Elements and attributes</span></span>

<span data-ttu-id="e84a4-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="e84a4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e84a4-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e84a4-112">Child elements</span></span>

|<span data-ttu-id="e84a4-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e84a4-113">**Element**</span></span>|<span data-ttu-id="e84a4-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="e84a4-114">**Type**</span></span>|<span data-ttu-id="e84a4-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e84a4-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e84a4-116">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="e84a4-116">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e84a4-117">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="e84a4-117">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e84a4-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="e84a4-118">Attributes</span></span>

|<span data-ttu-id="e84a4-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e84a4-119">**Attribute**</span></span>|<span data-ttu-id="e84a4-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="e84a4-120">**Type**</span></span>|<span data-ttu-id="e84a4-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="e84a4-121">**Required**</span></span>|<span data-ttu-id="e84a4-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e84a4-122">**Description**</span></span>|<span data-ttu-id="e84a4-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="e84a4-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e84a4-124">ActiveRecordsetID</span><span class="sxs-lookup"><span data-stu-id="e84a4-124">ActiveRecordsetID</span></span>  <br/> |<span data-ttu-id="e84a4-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e84a4-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e84a4-126">Optional</span><span class="sxs-lookup"><span data-stu-id="e84a4-126">optional</span></span>  <br/> ||<span data-ttu-id="e84a4-127">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e84a4-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e84a4-128">DataWindowOrder</span><span class="sxs-lookup"><span data-stu-id="e84a4-128">DataWindowOrder</span></span>  <br/> |<span data-ttu-id="e84a4-129">XSD: String</span><span class="sxs-lookup"><span data-stu-id="e84a4-129">xsd:string</span></span>  <br/> |<span data-ttu-id="e84a4-130">Optional</span><span class="sxs-lookup"><span data-stu-id="e84a4-130">optional</span></span>  <br/> ||<span data-ttu-id="e84a4-131">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="e84a4-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e84a4-132">NextID</span><span class="sxs-lookup"><span data-stu-id="e84a4-132">NextID</span></span>  <br/> |<span data-ttu-id="e84a4-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e84a4-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e84a4-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="e84a4-134">required</span></span>  <br/> ||<span data-ttu-id="e84a4-135">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e84a4-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

