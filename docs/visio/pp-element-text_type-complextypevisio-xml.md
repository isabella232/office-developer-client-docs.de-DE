---
title: PP-Element (text_type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5444543-fcd9-91cc-e7f8-cf860caa9fcc
description: Gibt den Anfang einer Absatzeigenschaften Ausführung an. Die Ausführung wird bis zum Ende des Texts oder bis zum nächsten Tag definiert.
ms.openlocfilehash: 695958c77f730abed03f50d6ad9c71f4de76dd63
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537738"
---
# <a name="pp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="21ea4-104">PP-Element (text_type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="21ea4-104">pp element (Text_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="21ea4-105">Gibt den Anfang einer Absatzeigenschaften Ausführung an.</span><span class="sxs-lookup"><span data-stu-id="21ea4-105">Specifies the beginning of a paragraph properties run.</span></span> <span data-ttu-id="21ea4-106">Die Ausführung wird bis zum Ende des Texts oder bis zum nächsten Tag definiert.</span><span class="sxs-lookup"><span data-stu-id="21ea4-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="21ea4-107">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="21ea4-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="21ea4-108">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="21ea4-108">**Element type**</span></span> <br/> |[<span data-ttu-id="21ea4-109">pp_Type</span><span class="sxs-lookup"><span data-stu-id="21ea4-109">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="21ea4-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="21ea4-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="21ea4-111">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="21ea4-111">**Schema file**</span></span> <br/> |<span data-ttu-id="21ea4-112">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="21ea4-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="21ea4-113">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="21ea4-113">**Document parts**</span></span> <br/> |<span data-ttu-id="21ea4-114">Seite #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="21ea4-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="21ea4-115">Definition</span><span class="sxs-lookup"><span data-stu-id="21ea4-115">Definition</span></span>

```XML
< xs:element name="pp" type="pp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="21ea4-116">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="21ea4-116">Elements and attributes</span></span>

<span data-ttu-id="21ea4-117">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="21ea4-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="21ea4-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="21ea4-118">Parent elements</span></span>

|<span data-ttu-id="21ea4-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="21ea4-119">**Element**</span></span>|<span data-ttu-id="21ea4-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="21ea4-120">**Type**</span></span>|<span data-ttu-id="21ea4-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="21ea4-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="21ea4-122">Text</span><span class="sxs-lookup"><span data-stu-id="21ea4-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="21ea4-123">Text_type</span><span class="sxs-lookup"><span data-stu-id="21ea4-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="21ea4-124">Enthält den Text eines Shapes.</span><span class="sxs-lookup"><span data-stu-id="21ea4-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="21ea4-125">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="21ea4-125">Child elements</span></span>

<span data-ttu-id="21ea4-126">Keine.</span><span class="sxs-lookup"><span data-stu-id="21ea4-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="21ea4-127">Attribute</span><span class="sxs-lookup"><span data-stu-id="21ea4-127">Attributes</span></span>

|<span data-ttu-id="21ea4-128">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="21ea4-128">**Attribute**</span></span>|<span data-ttu-id="21ea4-129">**Typ**</span><span class="sxs-lookup"><span data-stu-id="21ea4-129">**Type**</span></span>|<span data-ttu-id="21ea4-130">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="21ea4-130">**Required**</span></span>|<span data-ttu-id="21ea4-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="21ea4-131">**Description**</span></span>|<span data-ttu-id="21ea4-132">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="21ea4-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="21ea4-133">IX</span><span class="sxs-lookup"><span data-stu-id="21ea4-133">IX</span></span>  <br/> |<span data-ttu-id="21ea4-134">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="21ea4-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="21ea4-135">erforderlich</span><span class="sxs-lookup"><span data-stu-id="21ea4-135">required</span></span>  <br/> |<span data-ttu-id="21ea4-136">Der Index des **para** -Elements, das die auf diese Ausführung angewendete Formatierung angibt.</span><span class="sxs-lookup"><span data-stu-id="21ea4-136">The index of the **Para** element that specifies the formatting applied to this run.</span></span>  <br/> |<span data-ttu-id="21ea4-137">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="21ea4-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

