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
# <a name="refreshconflict_type-complextype-visio-xml"></a><span data-ttu-id="91d5e-102">RefreshConflict_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="91d5e-102">RefreshConflict_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="91d5e-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="91d5e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="91d5e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="91d5e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="91d5e-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="91d5e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="91d5e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="91d5e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="91d5e-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="91d5e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="91d5e-108">Keine</span><span class="sxs-lookup"><span data-stu-id="91d5e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="91d5e-109">Definition</span><span class="sxs-lookup"><span data-stu-id="91d5e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="91d5e-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="91d5e-110">Elements and attributes</span></span>

<span data-ttu-id="91d5e-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="91d5e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="91d5e-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="91d5e-112">Child elements</span></span>

<span data-ttu-id="91d5e-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="91d5e-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="91d5e-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="91d5e-114">Attributes</span></span>

|<span data-ttu-id="91d5e-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="91d5e-115">**Attribute**</span></span>|<span data-ttu-id="91d5e-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="91d5e-116">**Type**</span></span>|<span data-ttu-id="91d5e-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="91d5e-117">**Required**</span></span>|<span data-ttu-id="91d5e-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="91d5e-118">**Description**</span></span>|<span data-ttu-id="91d5e-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="91d5e-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="91d5e-120">PageID</span><span class="sxs-lookup"><span data-stu-id="91d5e-120">PageID</span></span>  <br/> |<span data-ttu-id="91d5e-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="91d5e-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="91d5e-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="91d5e-122">required</span></span>  <br/> ||<span data-ttu-id="91d5e-123">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="91d5e-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="91d5e-124">RowID</span><span class="sxs-lookup"><span data-stu-id="91d5e-124">RowID</span></span>  <br/> |<span data-ttu-id="91d5e-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="91d5e-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="91d5e-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="91d5e-126">required</span></span>  <br/> ||<span data-ttu-id="91d5e-127">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="91d5e-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="91d5e-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="91d5e-128">ShapeID</span></span>  <br/> |<span data-ttu-id="91d5e-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="91d5e-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="91d5e-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="91d5e-130">required</span></span>  <br/> ||<span data-ttu-id="91d5e-131">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="91d5e-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

