---
title: pp-Element (Text_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5444543-fcd9-91cc-e7f8-cf860caa9fcc
description: Gibt den Anfang einer Ausführung einer Absatzeigenschaften an. Die Ausführung wird bis zum Ende des Texts oder bis zum nächsten Tag definiert.
ms.openlocfilehash: 695958c77f730abed03f50d6ad9c71f4de76dd63
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537738"
---
# <a name="pp-element-text_type-complextype-visio-xml"></a><span data-ttu-id="abe02-104">pp-Element (Text_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="abe02-104">pp element (Text_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="abe02-105">Gibt den Anfang einer Ausführung einer Absatzeigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="abe02-105">Specifies the beginning of a paragraph properties run.</span></span> <span data-ttu-id="abe02-106">Die Ausführung wird bis zum Ende des Texts oder bis zum nächsten Tag definiert.</span><span class="sxs-lookup"><span data-stu-id="abe02-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="abe02-107">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="abe02-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="abe02-108">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="abe02-108">**Element type**</span></span> <br/> |[<span data-ttu-id="abe02-109">pp_Type</span><span class="sxs-lookup"><span data-stu-id="abe02-109">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="abe02-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="abe02-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="abe02-111">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="abe02-111">**Schema file**</span></span> <br/> |<span data-ttu-id="abe02-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="abe02-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="abe02-113">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="abe02-113">**Document parts**</span></span> <br/> |<span data-ttu-id="abe02-114">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="abe02-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="abe02-115">Definition</span><span class="sxs-lookup"><span data-stu-id="abe02-115">Definition</span></span>

```XML
< xs:element name="pp" type="pp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="abe02-116">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="abe02-116">Elements and attributes</span></span>

<span data-ttu-id="abe02-117">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="abe02-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="abe02-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="abe02-118">Parent elements</span></span>

|<span data-ttu-id="abe02-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="abe02-119">**Element**</span></span>|<span data-ttu-id="abe02-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="abe02-120">**Type**</span></span>|<span data-ttu-id="abe02-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="abe02-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="abe02-122">Text</span><span class="sxs-lookup"><span data-stu-id="abe02-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="abe02-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="abe02-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="abe02-124">Enthält den Text einer Form.</span><span class="sxs-lookup"><span data-stu-id="abe02-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="abe02-125">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="abe02-125">Child elements</span></span>

<span data-ttu-id="abe02-126">Keine.</span><span class="sxs-lookup"><span data-stu-id="abe02-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="abe02-127">Attribute</span><span class="sxs-lookup"><span data-stu-id="abe02-127">Attributes</span></span>

|<span data-ttu-id="abe02-128">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="abe02-128">**Attribute**</span></span>|<span data-ttu-id="abe02-129">**Typ**</span><span class="sxs-lookup"><span data-stu-id="abe02-129">**Type**</span></span>|<span data-ttu-id="abe02-130">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="abe02-130">**Required**</span></span>|<span data-ttu-id="abe02-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="abe02-131">**Description**</span></span>|<span data-ttu-id="abe02-132">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="abe02-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="abe02-133">IX</span><span class="sxs-lookup"><span data-stu-id="abe02-133">IX</span></span>  <br/> |<span data-ttu-id="abe02-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="abe02-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="abe02-135">erforderlich</span><span class="sxs-lookup"><span data-stu-id="abe02-135">required</span></span>  <br/> |<span data-ttu-id="abe02-136">Der Index des **Para-Elements,** das die auf diese Ausführung angewendete Formatierung angibt.</span><span class="sxs-lookup"><span data-stu-id="abe02-136">The index of the **Para** element that specifies the formatting applied to this run.</span></span>  <br/> |<span data-ttu-id="abe02-137">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="abe02-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

