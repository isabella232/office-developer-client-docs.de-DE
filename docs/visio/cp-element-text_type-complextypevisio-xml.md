---
title: CP-Element (text_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4edd0a3f-e433-bf54-34cd-3b05fd10a5a5
description: Markiert den Anfang einer Zeicheneigenschaften ausführen, die entsprechend dem entsprechenden Char-Element formatiert ist. Die Ausführung wird am Ende des Texts oder bis zum nächsten Tag definiert.
ms.openlocfilehash: eb7fd30c2314e159dc3649e87cd63bd4090ba283
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282950"
---
# <a name="cp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="f82cb-104">CP-Element (text_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="f82cb-104">cp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="f82cb-105">Markiert den Anfang einer Zeicheneigenschaften ausführen, die entsprechend dem entsprechenden Char-Element formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="f82cb-105">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span> <span data-ttu-id="f82cb-106">Die Ausführung wird am Ende des Texts oder bis zum nächsten Tag definiert.</span><span class="sxs-lookup"><span data-stu-id="f82cb-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f82cb-107">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f82cb-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f82cb-108">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="f82cb-108">**Element type**</span></span> <br/> |[<span data-ttu-id="f82cb-109">cp_Type</span><span class="sxs-lookup"><span data-stu-id="f82cb-109">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f82cb-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f82cb-110">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f82cb-111">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="f82cb-111">**Schema file**</span></span> <br/> |<span data-ttu-id="f82cb-112">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="f82cb-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f82cb-113">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="f82cb-113">**Document parts**</span></span> <br/> |<span data-ttu-id="f82cb-114">Page #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="f82cb-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f82cb-115">Definition</span><span class="sxs-lookup"><span data-stu-id="f82cb-115">Definition</span></span>

```XML
< xs:element name="cp" type="cp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f82cb-116">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="f82cb-116">Elements and attributes</span></span>

<span data-ttu-id="f82cb-117">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="f82cb-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f82cb-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f82cb-118">Parent elements</span></span>

|<span data-ttu-id="f82cb-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="f82cb-119">**Element**</span></span>|<span data-ttu-id="f82cb-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f82cb-120">**Type**</span></span>|<span data-ttu-id="f82cb-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f82cb-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f82cb-122">Text</span><span class="sxs-lookup"><span data-stu-id="f82cb-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f82cb-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="f82cb-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f82cb-124">Enthält den Text einer Form.</span><span class="sxs-lookup"><span data-stu-id="f82cb-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f82cb-125">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f82cb-125">Child elements</span></span>

<span data-ttu-id="f82cb-126">Keine.</span><span class="sxs-lookup"><span data-stu-id="f82cb-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f82cb-127">Attribute</span><span class="sxs-lookup"><span data-stu-id="f82cb-127">Attributes</span></span>

|<span data-ttu-id="f82cb-128">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f82cb-128">**Attribute**</span></span>|<span data-ttu-id="f82cb-129">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f82cb-129">**Type**</span></span>|<span data-ttu-id="f82cb-130">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="f82cb-130">**Required**</span></span>|<span data-ttu-id="f82cb-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f82cb-131">**Description**</span></span>|<span data-ttu-id="f82cb-132">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="f82cb-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f82cb-133">IX</span><span class="sxs-lookup"><span data-stu-id="f82cb-133">IX</span></span>  <br/> |<span data-ttu-id="f82cb-134">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f82cb-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f82cb-135">erforderlich</span><span class="sxs-lookup"><span data-stu-id="f82cb-135">required</span></span>  <br/> |<span data-ttu-id="f82cb-136">Der Char-Elementindex, der von dieser Eigenschaft ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f82cb-136">The Char element index that this property run represents.</span></span>  <br/> |<span data-ttu-id="f82cb-137">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="f82cb-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

