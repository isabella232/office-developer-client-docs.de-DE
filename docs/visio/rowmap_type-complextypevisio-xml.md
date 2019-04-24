---
title: RowMap_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2abe0572-53bb-20fc-333f-2b69b07e99be
ms.openlocfilehash: bdc76f35cf2824d5159e945bce7e9dd2a8abe2bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355734"
---
# <a name="rowmaptype-complextype-visio-xml"></a><span data-ttu-id="a99cb-102">RowMap_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="a99cb-102">RowMap_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a99cb-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="a99cb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a99cb-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a99cb-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a99cb-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="a99cb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a99cb-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="a99cb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a99cb-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="a99cb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a99cb-108">Keine</span><span class="sxs-lookup"><span data-stu-id="a99cb-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a99cb-109">Definition</span><span class="sxs-lookup"><span data-stu-id="a99cb-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a99cb-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="a99cb-110">Elements and attributes</span></span>

<span data-ttu-id="a99cb-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="a99cb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a99cb-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a99cb-112">Child elements</span></span>

<span data-ttu-id="a99cb-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="a99cb-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a99cb-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="a99cb-114">Attributes</span></span>

|<span data-ttu-id="a99cb-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a99cb-115">**Attribute**</span></span>|<span data-ttu-id="a99cb-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="a99cb-116">**Type**</span></span>|<span data-ttu-id="a99cb-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="a99cb-117">**Required**</span></span>|<span data-ttu-id="a99cb-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a99cb-118">**Description**</span></span>|<span data-ttu-id="a99cb-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="a99cb-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a99cb-120">PageID</span><span class="sxs-lookup"><span data-stu-id="a99cb-120">PageID</span></span>  <br/> |<span data-ttu-id="a99cb-121">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a99cb-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a99cb-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="a99cb-122">required</span></span>  <br/> ||<span data-ttu-id="a99cb-123">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="a99cb-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a99cb-124">RowID</span><span class="sxs-lookup"><span data-stu-id="a99cb-124">RowID</span></span>  <br/> |<span data-ttu-id="a99cb-125">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a99cb-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a99cb-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="a99cb-126">required</span></span>  <br/> ||<span data-ttu-id="a99cb-127">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="a99cb-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a99cb-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="a99cb-128">ShapeID</span></span>  <br/> |<span data-ttu-id="a99cb-129">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a99cb-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a99cb-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="a99cb-130">required</span></span>  <br/> ||<span data-ttu-id="a99cb-131">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="a99cb-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

