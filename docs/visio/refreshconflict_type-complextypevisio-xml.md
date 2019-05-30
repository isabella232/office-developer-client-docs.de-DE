---
title: RefreshConflict_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec7677f-a761-804c-6a12-731df86481a8
ms.openlocfilehash: 7b52bc87af213e9c26f4bc359adf6cf900b34957
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542828"
---
# <a name="refreshconflicttype-complextype-visio-xml"></a><span data-ttu-id="cf862-102">RefreshConflict_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="cf862-102">RefreshConflict_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="cf862-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="cf862-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cf862-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cf862-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cf862-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="cf862-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cf862-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="cf862-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cf862-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="cf862-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cf862-108">Keine</span><span class="sxs-lookup"><span data-stu-id="cf862-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cf862-109">Definition</span><span class="sxs-lookup"><span data-stu-id="cf862-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="cf862-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="cf862-110">Elements and attributes</span></span>

<span data-ttu-id="cf862-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="cf862-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cf862-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cf862-112">Child elements</span></span>

<span data-ttu-id="cf862-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="cf862-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cf862-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="cf862-114">Attributes</span></span>

|<span data-ttu-id="cf862-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="cf862-115">**Attribute**</span></span>|<span data-ttu-id="cf862-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="cf862-116">**Type**</span></span>|<span data-ttu-id="cf862-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="cf862-117">**Required**</span></span>|<span data-ttu-id="cf862-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cf862-118">**Description**</span></span>|<span data-ttu-id="cf862-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="cf862-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cf862-120">PageID</span><span class="sxs-lookup"><span data-stu-id="cf862-120">PageID</span></span>  <br/> |<span data-ttu-id="cf862-121">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cf862-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cf862-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="cf862-122">required</span></span>  <br/> ||<span data-ttu-id="cf862-123">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="cf862-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cf862-124">ROWID</span><span class="sxs-lookup"><span data-stu-id="cf862-124">RowID</span></span>  <br/> |<span data-ttu-id="cf862-125">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cf862-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cf862-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="cf862-126">required</span></span>  <br/> ||<span data-ttu-id="cf862-127">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="cf862-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cf862-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="cf862-128">ShapeID</span></span>  <br/> |<span data-ttu-id="cf862-129">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cf862-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cf862-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="cf862-130">required</span></span>  <br/> ||<span data-ttu-id="cf862-131">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="cf862-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

