---
title: RowMap_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2abe0572-53bb-20fc-333f-2b69b07e99be
ms.openlocfilehash: 8564f5a063ac2365de50919168df0b84e8ae100a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538774"
---
# <a name="rowmap_type-complextype-visio-xml"></a><span data-ttu-id="47cbf-102">RowMap_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="47cbf-102">RowMap_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="47cbf-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="47cbf-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="47cbf-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="47cbf-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="47cbf-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="47cbf-105">**Schema file**</span></span> <br/> |<span data-ttu-id="47cbf-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="47cbf-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="47cbf-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="47cbf-107">**Extension base**</span></span> <br/> |<span data-ttu-id="47cbf-108">Keine</span><span class="sxs-lookup"><span data-stu-id="47cbf-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="47cbf-109">Definition</span><span class="sxs-lookup"><span data-stu-id="47cbf-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="47cbf-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="47cbf-110">Elements and attributes</span></span>

<span data-ttu-id="47cbf-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="47cbf-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="47cbf-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="47cbf-112">Child elements</span></span>

<span data-ttu-id="47cbf-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="47cbf-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="47cbf-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="47cbf-114">Attributes</span></span>

|<span data-ttu-id="47cbf-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="47cbf-115">**Attribute**</span></span>|<span data-ttu-id="47cbf-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="47cbf-116">**Type**</span></span>|<span data-ttu-id="47cbf-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="47cbf-117">**Required**</span></span>|<span data-ttu-id="47cbf-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="47cbf-118">**Description**</span></span>|<span data-ttu-id="47cbf-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="47cbf-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="47cbf-120">PageID</span><span class="sxs-lookup"><span data-stu-id="47cbf-120">PageID</span></span>  <br/> |<span data-ttu-id="47cbf-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="47cbf-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="47cbf-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="47cbf-122">required</span></span>  <br/> ||<span data-ttu-id="47cbf-123">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="47cbf-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="47cbf-124">RowID</span><span class="sxs-lookup"><span data-stu-id="47cbf-124">RowID</span></span>  <br/> |<span data-ttu-id="47cbf-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="47cbf-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="47cbf-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="47cbf-126">required</span></span>  <br/> ||<span data-ttu-id="47cbf-127">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="47cbf-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="47cbf-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="47cbf-128">ShapeID</span></span>  <br/> |<span data-ttu-id="47cbf-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="47cbf-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="47cbf-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="47cbf-130">required</span></span>  <br/> ||<span data-ttu-id="47cbf-131">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="47cbf-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

