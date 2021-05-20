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
# <a name="datarecordsets_type-complextype-visio-xml"></a><span data-ttu-id="48771-102">DataRecordSets_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="48771-102">DataRecordSets_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="48771-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="48771-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="48771-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="48771-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="48771-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="48771-105">**Schema file**</span></span> <br/> |<span data-ttu-id="48771-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="48771-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="48771-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="48771-107">**Extension base**</span></span> <br/> |<span data-ttu-id="48771-108">Keine</span><span class="sxs-lookup"><span data-stu-id="48771-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="48771-109">Definition</span><span class="sxs-lookup"><span data-stu-id="48771-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="48771-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="48771-110">Elements and attributes</span></span>

<span data-ttu-id="48771-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="48771-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="48771-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="48771-112">Child elements</span></span>

|<span data-ttu-id="48771-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="48771-113">**Element**</span></span>|<span data-ttu-id="48771-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="48771-114">**Type**</span></span>|<span data-ttu-id="48771-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="48771-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="48771-116">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="48771-116">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="48771-117">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="48771-117">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="48771-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="48771-118">Attributes</span></span>

|<span data-ttu-id="48771-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="48771-119">**Attribute**</span></span>|<span data-ttu-id="48771-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="48771-120">**Type**</span></span>|<span data-ttu-id="48771-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="48771-121">**Required**</span></span>|<span data-ttu-id="48771-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="48771-122">**Description**</span></span>|<span data-ttu-id="48771-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="48771-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="48771-124">ActiveRecordsetID</span><span class="sxs-lookup"><span data-stu-id="48771-124">ActiveRecordsetID</span></span>  <br/> |<span data-ttu-id="48771-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="48771-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="48771-126">Optional</span><span class="sxs-lookup"><span data-stu-id="48771-126">optional</span></span>  <br/> ||<span data-ttu-id="48771-127">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="48771-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="48771-128">DataWindowOrder</span><span class="sxs-lookup"><span data-stu-id="48771-128">DataWindowOrder</span></span>  <br/> |<span data-ttu-id="48771-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="48771-129">xsd:string</span></span>  <br/> |<span data-ttu-id="48771-130">Optional</span><span class="sxs-lookup"><span data-stu-id="48771-130">optional</span></span>  <br/> ||<span data-ttu-id="48771-131">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="48771-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="48771-132">NextID</span><span class="sxs-lookup"><span data-stu-id="48771-132">NextID</span></span>  <br/> |<span data-ttu-id="48771-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="48771-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="48771-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="48771-134">required</span></span>  <br/> ||<span data-ttu-id="48771-135">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="48771-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

