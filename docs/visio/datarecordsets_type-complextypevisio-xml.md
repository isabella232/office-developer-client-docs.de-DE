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
# <a name="datarecordsetstype-complextype-visio-xml"></a><span data-ttu-id="96d52-102">DataRecordSets_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="96d52-102">DataRecordSets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="96d52-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="96d52-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="96d52-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="96d52-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="96d52-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="96d52-105">**Schema file**</span></span> <br/> |<span data-ttu-id="96d52-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="96d52-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="96d52-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="96d52-107">**Extension base**</span></span> <br/> |<span data-ttu-id="96d52-108">Keine</span><span class="sxs-lookup"><span data-stu-id="96d52-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="96d52-109">Definition</span><span class="sxs-lookup"><span data-stu-id="96d52-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="96d52-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="96d52-110">Elements and attributes</span></span>

<span data-ttu-id="96d52-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="96d52-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="96d52-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="96d52-112">Child elements</span></span>

|<span data-ttu-id="96d52-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="96d52-113">**Element**</span></span>|<span data-ttu-id="96d52-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="96d52-114">**Type**</span></span>|<span data-ttu-id="96d52-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="96d52-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="96d52-116">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="96d52-116">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="96d52-117">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="96d52-117">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="96d52-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="96d52-118">Attributes</span></span>

|<span data-ttu-id="96d52-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="96d52-119">**Attribute**</span></span>|<span data-ttu-id="96d52-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="96d52-120">**Type**</span></span>|<span data-ttu-id="96d52-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="96d52-121">**Required**</span></span>|<span data-ttu-id="96d52-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="96d52-122">**Description**</span></span>|<span data-ttu-id="96d52-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="96d52-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="96d52-124">ActiveRecordsetID</span><span class="sxs-lookup"><span data-stu-id="96d52-124">ActiveRecordsetID</span></span>  <br/> |<span data-ttu-id="96d52-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="96d52-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="96d52-126">Optional</span><span class="sxs-lookup"><span data-stu-id="96d52-126">optional</span></span>  <br/> ||<span data-ttu-id="96d52-127">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="96d52-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="96d52-128">DataWindowOrder</span><span class="sxs-lookup"><span data-stu-id="96d52-128">DataWindowOrder</span></span>  <br/> |<span data-ttu-id="96d52-129">XSD: String</span><span class="sxs-lookup"><span data-stu-id="96d52-129">xsd:string</span></span>  <br/> |<span data-ttu-id="96d52-130">Optional</span><span class="sxs-lookup"><span data-stu-id="96d52-130">optional</span></span>  <br/> ||<span data-ttu-id="96d52-131">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="96d52-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="96d52-132">NextID</span><span class="sxs-lookup"><span data-stu-id="96d52-132">NextID</span></span>  <br/> |<span data-ttu-id="96d52-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="96d52-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="96d52-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="96d52-134">required</span></span>  <br/> ||<span data-ttu-id="96d52-135">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="96d52-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

