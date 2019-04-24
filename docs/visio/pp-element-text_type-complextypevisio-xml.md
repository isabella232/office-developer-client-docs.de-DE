---
title: PP-Element (text_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5444543-fcd9-91cc-e7f8-cf860caa9fcc
description: Gibt den Anfang einer Absatzeigenschaft an. Die Ausführung wird am Ende des Texts oder bis zum nächsten Tag definiert.
ms.openlocfilehash: bb2b0ab7a76c142b810ecd02dbc1b5ba7463520a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356077"
---
# <a name="pp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="1c6f3-104">PP-Element (text_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="1c6f3-104">pp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="1c6f3-105">Gibt den Anfang einer Absatzeigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="1c6f3-105">Specifies the beginning of a paragraph properties run.</span></span> <span data-ttu-id="1c6f3-106">Die Ausführung wird am Ende des Texts oder bis zum nächsten Tag definiert.</span><span class="sxs-lookup"><span data-stu-id="1c6f3-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1c6f3-107">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1c6f3-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1c6f3-108">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="1c6f3-108">**Element type**</span></span> <br/> |[<span data-ttu-id="1c6f3-109">pp_Type</span><span class="sxs-lookup"><span data-stu-id="1c6f3-109">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1c6f3-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1c6f3-110">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1c6f3-111">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="1c6f3-111">**Schema file**</span></span> <br/> |<span data-ttu-id="1c6f3-112">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="1c6f3-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1c6f3-113">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="1c6f3-113">**Document parts**</span></span> <br/> |<span data-ttu-id="1c6f3-114">Page #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="1c6f3-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1c6f3-115">Definition</span><span class="sxs-lookup"><span data-stu-id="1c6f3-115">Definition</span></span>

```XML
< xs:element name="pp" type="pp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1c6f3-116">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="1c6f3-116">Elements and attributes</span></span>

<span data-ttu-id="1c6f3-117">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="1c6f3-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1c6f3-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1c6f3-118">Parent elements</span></span>

|<span data-ttu-id="1c6f3-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="1c6f3-119">**Element**</span></span>|<span data-ttu-id="1c6f3-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1c6f3-120">**Type**</span></span>|<span data-ttu-id="1c6f3-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1c6f3-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1c6f3-122">Text</span><span class="sxs-lookup"><span data-stu-id="1c6f3-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1c6f3-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="1c6f3-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1c6f3-124">Enthält den Text einer Form.</span><span class="sxs-lookup"><span data-stu-id="1c6f3-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1c6f3-125">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1c6f3-125">Child elements</span></span>

<span data-ttu-id="1c6f3-126">Keine.</span><span class="sxs-lookup"><span data-stu-id="1c6f3-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1c6f3-127">Attribute</span><span class="sxs-lookup"><span data-stu-id="1c6f3-127">Attributes</span></span>

|<span data-ttu-id="1c6f3-128">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1c6f3-128">**Attribute**</span></span>|<span data-ttu-id="1c6f3-129">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1c6f3-129">**Type**</span></span>|<span data-ttu-id="1c6f3-130">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="1c6f3-130">**Required**</span></span>|<span data-ttu-id="1c6f3-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1c6f3-131">**Description**</span></span>|<span data-ttu-id="1c6f3-132">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="1c6f3-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1c6f3-133">IX</span><span class="sxs-lookup"><span data-stu-id="1c6f3-133">IX</span></span>  <br/> |<span data-ttu-id="1c6f3-134">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1c6f3-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1c6f3-135">erforderlich</span><span class="sxs-lookup"><span data-stu-id="1c6f3-135">required</span></span>  <br/> |<span data-ttu-id="1c6f3-136">Der Index des **para** -Elements, das die auf diese Ausführung angewendete Formatierung angibt.</span><span class="sxs-lookup"><span data-stu-id="1c6f3-136">The index of the **Para** element that specifies the formatting applied to this run.</span></span>  <br/> |<span data-ttu-id="1c6f3-137">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="1c6f3-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

