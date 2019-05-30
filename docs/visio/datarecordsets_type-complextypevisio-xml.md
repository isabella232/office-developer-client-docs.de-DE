---
title: DataRecordSets_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04448cfa-7eb4-62ca-97d2-409b59a8db90
ms.openlocfilehash: 77a6588a1b5fba05d14e91a39ba570d21142f953
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539158"
---
# <a name="datarecordsetstype-complextype-visio-xml"></a><span data-ttu-id="712d3-102">DataRecordSets_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="712d3-102">DataRecordSets_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="712d3-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="712d3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="712d3-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="712d3-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="712d3-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="712d3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="712d3-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="712d3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="712d3-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="712d3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="712d3-108">Keine</span><span class="sxs-lookup"><span data-stu-id="712d3-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="712d3-109">Definition</span><span class="sxs-lookup"><span data-stu-id="712d3-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="712d3-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="712d3-110">Elements and attributes</span></span>

<span data-ttu-id="712d3-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="712d3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="712d3-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="712d3-112">Child elements</span></span>

|<span data-ttu-id="712d3-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="712d3-113">**Element**</span></span>|<span data-ttu-id="712d3-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="712d3-114">**Type**</span></span>|<span data-ttu-id="712d3-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="712d3-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="712d3-116">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="712d3-116">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="712d3-117">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="712d3-117">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="712d3-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="712d3-118">Attributes</span></span>

|<span data-ttu-id="712d3-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="712d3-119">**Attribute**</span></span>|<span data-ttu-id="712d3-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="712d3-120">**Type**</span></span>|<span data-ttu-id="712d3-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="712d3-121">**Required**</span></span>|<span data-ttu-id="712d3-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="712d3-122">**Description**</span></span>|<span data-ttu-id="712d3-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="712d3-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="712d3-124">ActiveRecordsetID</span><span class="sxs-lookup"><span data-stu-id="712d3-124">ActiveRecordsetID</span></span>  <br/> |<span data-ttu-id="712d3-125">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="712d3-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="712d3-126">Optional</span><span class="sxs-lookup"><span data-stu-id="712d3-126">optional</span></span>  <br/> ||<span data-ttu-id="712d3-127">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="712d3-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="712d3-128">DataWindowOrder</span><span class="sxs-lookup"><span data-stu-id="712d3-128">DataWindowOrder</span></span>  <br/> |<span data-ttu-id="712d3-129">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="712d3-129">xsd:string</span></span>  <br/> |<span data-ttu-id="712d3-130">Optional</span><span class="sxs-lookup"><span data-stu-id="712d3-130">optional</span></span>  <br/> ||<span data-ttu-id="712d3-131">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="712d3-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="712d3-132">NextID</span><span class="sxs-lookup"><span data-stu-id="712d3-132">NextID</span></span>  <br/> |<span data-ttu-id="712d3-133">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="712d3-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="712d3-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="712d3-134">required</span></span>  <br/> ||<span data-ttu-id="712d3-135">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="712d3-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

