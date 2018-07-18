---
title: RefreshConflict_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec7677f-a761-804c-6a12-731df86481a8
ms.openlocfilehash: 44910cd305b484771ca3d4f4d49ef8a09a6fc2dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797801"
---
# <a name="refreshconflicttype-complextype-visio-xml"></a><span data-ttu-id="40a66-102">RefreshConflict_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="40a66-102">RefreshConflict_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="40a66-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="40a66-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="40a66-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="40a66-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="40a66-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="40a66-105">**Schema file**</span></span> <br/> |<span data-ttu-id="40a66-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="40a66-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="40a66-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="40a66-107">**Extension base**</span></span> <br/> |<span data-ttu-id="40a66-108">Keine</span><span class="sxs-lookup"><span data-stu-id="40a66-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="40a66-109">Definition</span><span class="sxs-lookup"><span data-stu-id="40a66-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="40a66-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="40a66-110">Elements and attributes</span></span>

<span data-ttu-id="40a66-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="40a66-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="40a66-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="40a66-112">Child elements</span></span>

<span data-ttu-id="40a66-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="40a66-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="40a66-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="40a66-114">Attributes</span></span>

|<span data-ttu-id="40a66-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="40a66-115">**Attribute**</span></span>|<span data-ttu-id="40a66-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="40a66-116">**Type**</span></span>|<span data-ttu-id="40a66-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="40a66-117">**Required**</span></span>|<span data-ttu-id="40a66-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="40a66-118">**Description**</span></span>|<span data-ttu-id="40a66-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="40a66-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="40a66-120">PageID</span><span class="sxs-lookup"><span data-stu-id="40a66-120">PageID</span></span>  <br/> |<span data-ttu-id="40a66-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="40a66-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="40a66-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="40a66-122">required</span></span>  <br/> ||<span data-ttu-id="40a66-123">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="40a66-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="40a66-124">RowID</span><span class="sxs-lookup"><span data-stu-id="40a66-124">RowID</span></span>  <br/> |<span data-ttu-id="40a66-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="40a66-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="40a66-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="40a66-126">required</span></span>  <br/> ||<span data-ttu-id="40a66-127">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="40a66-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="40a66-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="40a66-128">ShapeID</span></span>  <br/> |<span data-ttu-id="40a66-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="40a66-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="40a66-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="40a66-130">required</span></span>  <br/> ||<span data-ttu-id="40a66-131">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="40a66-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

