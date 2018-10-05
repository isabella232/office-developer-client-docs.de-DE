---
title: RowMap_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2abe0572-53bb-20fc-333f-2b69b07e99be
ms.openlocfilehash: bdc76f35cf2824d5159e945bce7e9dd2a8abe2bf
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400999"
---
# <a name="rowmaptype-complextype-visio-xml"></a><span data-ttu-id="8a70c-102">RowMap_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="8a70c-102">RowMap_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="8a70c-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="8a70c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8a70c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8a70c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8a70c-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="8a70c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8a70c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="8a70c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8a70c-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="8a70c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8a70c-108">Keine</span><span class="sxs-lookup"><span data-stu-id="8a70c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8a70c-109">Definition</span><span class="sxs-lookup"><span data-stu-id="8a70c-109">Definition</span></span>

```XML
      <xs:complexType name="RowMap_Type">
    <xs:attribute name="RowID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8a70c-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="8a70c-110">Elements and attributes</span></span>

<span data-ttu-id="8a70c-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="8a70c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8a70c-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8a70c-112">Child elements</span></span>

<span data-ttu-id="8a70c-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="8a70c-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8a70c-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="8a70c-114">Attributes</span></span>

|<span data-ttu-id="8a70c-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="8a70c-115">**Attribute**</span></span>|<span data-ttu-id="8a70c-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="8a70c-116">**Type**</span></span>|<span data-ttu-id="8a70c-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="8a70c-117">**Required**</span></span>|<span data-ttu-id="8a70c-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8a70c-118">**Description**</span></span>|<span data-ttu-id="8a70c-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="8a70c-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8a70c-120">PageID</span><span class="sxs-lookup"><span data-stu-id="8a70c-120">PageID</span></span>  <br/> |<span data-ttu-id="8a70c-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8a70c-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8a70c-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="8a70c-122">required</span></span>  <br/> ||<span data-ttu-id="8a70c-123">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8a70c-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8a70c-124">RowID</span><span class="sxs-lookup"><span data-stu-id="8a70c-124">RowID</span></span>  <br/> |<span data-ttu-id="8a70c-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8a70c-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8a70c-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="8a70c-126">required</span></span>  <br/> ||<span data-ttu-id="8a70c-127">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8a70c-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8a70c-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="8a70c-128">ShapeID</span></span>  <br/> |<span data-ttu-id="8a70c-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8a70c-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8a70c-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="8a70c-130">required</span></span>  <br/> ||<span data-ttu-id="8a70c-131">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8a70c-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

