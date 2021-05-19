---
title: Text-Element (ShapeSheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46211968-9ad8-07da-f725-3ad136b7a8a1
description: Enthält den Text einer Form.
ms.openlocfilehash: 4b03bc2539b80e49daae9d14f3e2ad07a51de9f1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541925"
---
# <a name="text-element-shapesheet_type-complextype-visio-xml"></a><span data-ttu-id="78f23-103">Text-Element (ShapeSheet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="78f23-103">Text element (ShapeSheet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="78f23-104">Enthält den Text einer Form.</span><span class="sxs-lookup"><span data-stu-id="78f23-104">Contains the text of a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="78f23-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="78f23-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="78f23-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="78f23-106">**Element type**</span></span> <br/> |[<span data-ttu-id="78f23-107">Text_Type</span><span class="sxs-lookup"><span data-stu-id="78f23-107">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="78f23-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="78f23-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="78f23-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="78f23-109">**Schema file**</span></span> <br/> |<span data-ttu-id="78f23-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="78f23-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="78f23-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="78f23-111">**Document parts**</span></span> <br/> |<span data-ttu-id="78f23-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="78f23-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="78f23-113">Definition</span><span class="sxs-lookup"><span data-stu-id="78f23-113">Definition</span></span>

```XML
< xs:element name="Text" type="Text_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="78f23-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="78f23-114">Elements and attributes</span></span>

<span data-ttu-id="78f23-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="78f23-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="78f23-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="78f23-116">Parent elements</span></span>

|<span data-ttu-id="78f23-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="78f23-117">**Element**</span></span>|<span data-ttu-id="78f23-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="78f23-118">**Type**</span></span>|<span data-ttu-id="78f23-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="78f23-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="78f23-120">Shape</span><span class="sxs-lookup"><span data-stu-id="78f23-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="78f23-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="78f23-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="78f23-122">Enthält Elemente, die ein Shape in einem **Master-,** **Page-** oder Gruppenformelement definieren.</span><span class="sxs-lookup"><span data-stu-id="78f23-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="78f23-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="78f23-123">Child elements</span></span>

|<span data-ttu-id="78f23-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="78f23-124">**Element**</span></span>|<span data-ttu-id="78f23-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="78f23-125">**Type**</span></span>|<span data-ttu-id="78f23-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="78f23-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="78f23-127">cp</span><span class="sxs-lookup"><span data-stu-id="78f23-127">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="78f23-128">cp_Type</span><span class="sxs-lookup"><span data-stu-id="78f23-128">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="78f23-129">Markiert den Anfang einer Ausführung einer Zeicheneigenschaften, die gemäß dem entsprechenden Char-Element formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="78f23-129">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span>  <br/> |
|[<span data-ttu-id="78f23-130">fld</span><span class="sxs-lookup"><span data-stu-id="78f23-130">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="78f23-131">fld_Type</span><span class="sxs-lookup"><span data-stu-id="78f23-131">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="78f23-132">Gibt eine Textfeldeinfügemarke für das entsprechende Field-Element an.</span><span class="sxs-lookup"><span data-stu-id="78f23-132">Indicates a text-field insertion point for the corresponding Field element.</span></span>  <br/> |
|[<span data-ttu-id="78f23-133">pp</span><span class="sxs-lookup"><span data-stu-id="78f23-133">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="78f23-134">pp_Type</span><span class="sxs-lookup"><span data-stu-id="78f23-134">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="78f23-135">Gibt den Anfang einer Ausführung einer Absatzeigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="78f23-135">Specifies the beginning of a paragraph properties run.</span></span>  <br/> |
|[<span data-ttu-id="78f23-136">tp</span><span class="sxs-lookup"><span data-stu-id="78f23-136">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="78f23-137">tp_Type</span><span class="sxs-lookup"><span data-stu-id="78f23-137">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="78f23-138">Gibt den Anfang der Ausführung einer Registerkarteneigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="78f23-138">Specifies the beginning of a tabs properties run.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="78f23-139">Attribute</span><span class="sxs-lookup"><span data-stu-id="78f23-139">Attributes</span></span>

<span data-ttu-id="78f23-140">Keine.</span><span class="sxs-lookup"><span data-stu-id="78f23-140">None.</span></span>
  

