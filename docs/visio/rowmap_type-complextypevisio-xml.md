---
title: RowMap_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2abe0572-53bb-20fc-333f-2b69b07e99be
ms.openlocfilehash: 18f573a480e3ae057074a219def192f6b1b2829b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797930"
---
# <a name="rowmaptype-complextype-visio-xml"></a><span data-ttu-id="bb126-102">RowMap_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="bb126-102">RowMap_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="bb126-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="bb126-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bb126-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bb126-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bb126-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="bb126-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bb126-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="bb126-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bb126-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="bb126-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bb126-108">Keine</span><span class="sxs-lookup"><span data-stu-id="bb126-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bb126-109">Definition</span><span class="sxs-lookup"><span data-stu-id="bb126-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="bb126-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="bb126-110">Elements and attributes</span></span>

<span data-ttu-id="bb126-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="bb126-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bb126-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bb126-112">Child elements</span></span>

<span data-ttu-id="bb126-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="bb126-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bb126-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="bb126-114">Attributes</span></span>

|<span data-ttu-id="bb126-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="bb126-115">**Attribute**</span></span>|<span data-ttu-id="bb126-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="bb126-116">**Type**</span></span>|<span data-ttu-id="bb126-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="bb126-117">**Required**</span></span>|<span data-ttu-id="bb126-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bb126-118">**Description**</span></span>|<span data-ttu-id="bb126-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="bb126-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bb126-120">PageID</span><span class="sxs-lookup"><span data-stu-id="bb126-120">PageID</span></span>  <br/> |<span data-ttu-id="bb126-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bb126-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bb126-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="bb126-122">required</span></span>  <br/> ||<span data-ttu-id="bb126-123">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bb126-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bb126-124">RowID</span><span class="sxs-lookup"><span data-stu-id="bb126-124">RowID</span></span>  <br/> |<span data-ttu-id="bb126-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bb126-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bb126-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="bb126-126">required</span></span>  <br/> ||<span data-ttu-id="bb126-127">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bb126-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bb126-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="bb126-128">ShapeID</span></span>  <br/> |<span data-ttu-id="bb126-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bb126-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bb126-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="bb126-130">required</span></span>  <br/> ||<span data-ttu-id="bb126-131">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bb126-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

