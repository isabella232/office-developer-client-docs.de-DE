---
title: TP-Element (text_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b13b9328-c6a0-e282-257c-2de55901df6a
description: Gibt den Anfang einer Eigenschaften von Tabs an. Die Ausführung wird am Ende des Texts oder bis zum nächsten Tag definiert.
ms.openlocfilehash: 3f27ea0babefa0ea69cbbc361031c57602649107
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307700"
---
# <a name="tp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="93990-104">TP-Element (text_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="93990-104">tp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="93990-105">Gibt den Anfang einer Eigenschaften von Tabs an.</span><span class="sxs-lookup"><span data-stu-id="93990-105">Specifies the beginning of a tabs properties run.</span></span> <span data-ttu-id="93990-106">Die Ausführung wird am Ende des Texts oder bis zum nächsten Tag definiert.</span><span class="sxs-lookup"><span data-stu-id="93990-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="93990-107">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="93990-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="93990-108">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="93990-108">**Element type**</span></span> <br/> |[<span data-ttu-id="93990-109">tp_Type</span><span class="sxs-lookup"><span data-stu-id="93990-109">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="93990-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="93990-110">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="93990-111">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="93990-111">**Schema file**</span></span> <br/> |<span data-ttu-id="93990-112">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="93990-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="93990-113">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="93990-113">**Document parts**</span></span> <br/> |<span data-ttu-id="93990-114">Page #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="93990-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="93990-115">Definition</span><span class="sxs-lookup"><span data-stu-id="93990-115">Definition</span></span>

```XML
< xs:element name="tp" type="tp_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="93990-116">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="93990-116">Elements and attributes</span></span>

<span data-ttu-id="93990-117">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="93990-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="93990-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="93990-118">Parent elements</span></span>

|<span data-ttu-id="93990-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="93990-119">**Element**</span></span>|<span data-ttu-id="93990-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="93990-120">**Type**</span></span>|<span data-ttu-id="93990-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="93990-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="93990-122">Text</span><span class="sxs-lookup"><span data-stu-id="93990-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="93990-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="93990-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="93990-124">Enthält den Text einer Form.</span><span class="sxs-lookup"><span data-stu-id="93990-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="93990-125">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="93990-125">Child elements</span></span>

<span data-ttu-id="93990-126">Keine.</span><span class="sxs-lookup"><span data-stu-id="93990-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="93990-127">Attribute</span><span class="sxs-lookup"><span data-stu-id="93990-127">Attributes</span></span>

|<span data-ttu-id="93990-128">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="93990-128">**Attribute**</span></span>|<span data-ttu-id="93990-129">**Typ**</span><span class="sxs-lookup"><span data-stu-id="93990-129">**Type**</span></span>|<span data-ttu-id="93990-130">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="93990-130">**Required**</span></span>|<span data-ttu-id="93990-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="93990-131">**Description**</span></span>|<span data-ttu-id="93990-132">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="93990-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="93990-133">IX</span><span class="sxs-lookup"><span data-stu-id="93990-133">IX</span></span>  <br/> |<span data-ttu-id="93990-134">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="93990-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="93990-135">erforderlich</span><span class="sxs-lookup"><span data-stu-id="93990-135">required</span></span>  <br/> |<span data-ttu-id="93990-136">Der nullbasierte Index des Elements innerhalb des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="93990-136">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="93990-137">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="93990-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

