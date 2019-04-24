---
title: RefreshConflict_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec7677f-a761-804c-6a12-731df86481a8
ms.openlocfilehash: 25c83a8168744820fa8b570dc37bda0547ab4ea0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346480"
---
# <a name="refreshconflicttype-complextype-visio-xml"></a><span data-ttu-id="e9451-102">RefreshConflict_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="e9451-102">RefreshConflict_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e9451-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="e9451-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e9451-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e9451-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e9451-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="e9451-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e9451-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="e9451-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e9451-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="e9451-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e9451-108">Keine</span><span class="sxs-lookup"><span data-stu-id="e9451-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e9451-109">Definition</span><span class="sxs-lookup"><span data-stu-id="e9451-109">Definition</span></span>

```XML
      <xs:complexType name="RefreshConflict_Type">
    <xs:attribute name="RowID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e9451-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="e9451-110">Elements and attributes</span></span>

<span data-ttu-id="e9451-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="e9451-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e9451-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e9451-112">Child elements</span></span>

<span data-ttu-id="e9451-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="e9451-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e9451-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="e9451-114">Attributes</span></span>

|<span data-ttu-id="e9451-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e9451-115">**Attribute**</span></span>|<span data-ttu-id="e9451-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="e9451-116">**Type**</span></span>|<span data-ttu-id="e9451-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="e9451-117">**Required**</span></span>|<span data-ttu-id="e9451-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e9451-118">**Description**</span></span>|<span data-ttu-id="e9451-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="e9451-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e9451-120">PageID</span><span class="sxs-lookup"><span data-stu-id="e9451-120">PageID</span></span>  <br/> |<span data-ttu-id="e9451-121">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e9451-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e9451-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="e9451-122">required</span></span>  <br/> ||<span data-ttu-id="e9451-123">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="e9451-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e9451-124">RowID</span><span class="sxs-lookup"><span data-stu-id="e9451-124">RowID</span></span>  <br/> |<span data-ttu-id="e9451-125">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e9451-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e9451-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="e9451-126">required</span></span>  <br/> ||<span data-ttu-id="e9451-127">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="e9451-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e9451-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="e9451-128">ShapeID</span></span>  <br/> |<span data-ttu-id="e9451-129">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e9451-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e9451-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="e9451-130">required</span></span>  <br/> ||<span data-ttu-id="e9451-131">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="e9451-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

