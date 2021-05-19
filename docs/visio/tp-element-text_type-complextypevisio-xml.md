---
title: tp-Element (Text_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b13b9328-c6a0-e282-257c-2de55901df6a
description: Gibt den Anfang der Ausführung einer Registerkarteneigenschaften an. Die Ausführung wird bis zum Ende des Texts oder bis zum nächsten Tag definiert.
ms.openlocfilehash: dad7a3de715473a75c601c1e391c9d51fc1cab85
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542975"
---
# <a name="tp-element-text_type-complextype-visio-xml"></a><span data-ttu-id="37346-104">tp-Element (Text_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="37346-104">tp element (Text_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="37346-105">Gibt den Anfang der Ausführung einer Registerkarteneigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="37346-105">Specifies the beginning of a tabs properties run.</span></span> <span data-ttu-id="37346-106">Die Ausführung wird bis zum Ende des Texts oder bis zum nächsten Tag definiert.</span><span class="sxs-lookup"><span data-stu-id="37346-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="37346-107">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="37346-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="37346-108">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="37346-108">**Element type**</span></span> <br/> |[<span data-ttu-id="37346-109">tp_Type</span><span class="sxs-lookup"><span data-stu-id="37346-109">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="37346-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="37346-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="37346-111">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="37346-111">**Schema file**</span></span> <br/> |<span data-ttu-id="37346-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="37346-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="37346-113">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="37346-113">**Document parts**</span></span> <br/> |<span data-ttu-id="37346-114">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="37346-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="37346-115">Definition</span><span class="sxs-lookup"><span data-stu-id="37346-115">Definition</span></span>

```XML
< xs:element name="tp" type="tp_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="37346-116">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="37346-116">Elements and attributes</span></span>

<span data-ttu-id="37346-117">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="37346-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="37346-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="37346-118">Parent elements</span></span>

|<span data-ttu-id="37346-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="37346-119">**Element**</span></span>|<span data-ttu-id="37346-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="37346-120">**Type**</span></span>|<span data-ttu-id="37346-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="37346-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="37346-122">Text</span><span class="sxs-lookup"><span data-stu-id="37346-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="37346-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="37346-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="37346-124">Enthält den Text einer Form.</span><span class="sxs-lookup"><span data-stu-id="37346-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="37346-125">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="37346-125">Child elements</span></span>

<span data-ttu-id="37346-126">Keine.</span><span class="sxs-lookup"><span data-stu-id="37346-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="37346-127">Attribute</span><span class="sxs-lookup"><span data-stu-id="37346-127">Attributes</span></span>

|<span data-ttu-id="37346-128">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="37346-128">**Attribute**</span></span>|<span data-ttu-id="37346-129">**Typ**</span><span class="sxs-lookup"><span data-stu-id="37346-129">**Type**</span></span>|<span data-ttu-id="37346-130">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="37346-130">**Required**</span></span>|<span data-ttu-id="37346-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="37346-131">**Description**</span></span>|<span data-ttu-id="37346-132">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="37346-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="37346-133">IX</span><span class="sxs-lookup"><span data-stu-id="37346-133">IX</span></span>  <br/> |<span data-ttu-id="37346-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="37346-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="37346-135">erforderlich</span><span class="sxs-lookup"><span data-stu-id="37346-135">required</span></span>  <br/> |<span data-ttu-id="37346-136">Der nullbasierte Index des Elements innerhalb des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="37346-136">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="37346-137">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="37346-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

