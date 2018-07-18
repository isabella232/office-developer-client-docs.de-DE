---
title: Textelement (ShapeSheet_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46211968-9ad8-07da-f725-3ad136b7a8a1
description: Enthält den Text eines Shapes.
ms.openlocfilehash: 636f349b0a93719cd157db563b238147af5584cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798236"
---
# <a name="text-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="3c826-103">Textelement (ShapeSheet_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="3c826-103">Text element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="3c826-104">Enthält den Text eines Shapes.</span><span class="sxs-lookup"><span data-stu-id="3c826-104">Contains the text of a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3c826-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="3c826-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c826-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="3c826-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3c826-107">Text_Type</span><span class="sxs-lookup"><span data-stu-id="3c826-107">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3c826-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3c826-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3c826-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="3c826-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3c826-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="3c826-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3c826-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="3c826-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3c826-112">Seite # .xml, Gestaltungsvorlagen # .xml</span><span class="sxs-lookup"><span data-stu-id="3c826-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3c826-113">Definition</span><span class="sxs-lookup"><span data-stu-id="3c826-113">Definition</span></span>

```XML
< xs:element name="Text" type="Text_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3c826-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="3c826-114">Elements and attributes</span></span>

<span data-ttu-id="3c826-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="3c826-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3c826-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3c826-116">Parent elements</span></span>

|<span data-ttu-id="3c826-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="3c826-117">**Element**</span></span>|<span data-ttu-id="3c826-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="3c826-118">**Type**</span></span>|<span data-ttu-id="3c826-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3c826-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3c826-120">Shape</span><span class="sxs-lookup"><span data-stu-id="3c826-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3c826-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="3c826-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3c826-122">Enthält Elemente, die ein Shape in einen **Master**, eine **Seite**oder eine Gruppe Form-Element definieren.</span><span class="sxs-lookup"><span data-stu-id="3c826-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3c826-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3c826-123">Child elements</span></span>

|<span data-ttu-id="3c826-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="3c826-124">**Element**</span></span>|<span data-ttu-id="3c826-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="3c826-125">**Type**</span></span>|<span data-ttu-id="3c826-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3c826-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3c826-127">CP-Werts</span><span class="sxs-lookup"><span data-stu-id="3c826-127">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3c826-128">cp_Type</span><span class="sxs-lookup"><span data-stu-id="3c826-128">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3c826-129">Markiert der Anfang der Zeicheneigenschaften eines ausführen, d. h., formatiert gemäß dem entsprechenden Char-Element.</span><span class="sxs-lookup"><span data-stu-id="3c826-129">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span>  <br/> |
|[<span data-ttu-id="3c826-130">fld</span><span class="sxs-lookup"><span data-stu-id="3c826-130">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3c826-131">fld_Type</span><span class="sxs-lookup"><span data-stu-id="3c826-131">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3c826-132">Gibt ein Text-Feld Einfügemarke für die entsprechenden Field-Element an.</span><span class="sxs-lookup"><span data-stu-id="3c826-132">Indicates a text-field insertion point for the corresponding Field element.</span></span>  <br/> |
|[<span data-ttu-id="3c826-133">PS</span><span class="sxs-lookup"><span data-stu-id="3c826-133">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3c826-134">pp_Type</span><span class="sxs-lookup"><span data-stu-id="3c826-134">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3c826-135">Gibt an, das Ende einer Absatzeigenschaften ausführen.</span><span class="sxs-lookup"><span data-stu-id="3c826-135">Specifies the beginning of a paragraph properties run.</span></span>  <br/> |
|[<span data-ttu-id="3c826-136">TP</span><span class="sxs-lookup"><span data-stu-id="3c826-136">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3c826-137">tp_Type</span><span class="sxs-lookup"><span data-stu-id="3c826-137">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3c826-138">Gibt den Anfang der Eigenschaften eines Registerkarten ausführen.</span><span class="sxs-lookup"><span data-stu-id="3c826-138">Specifies the beginning of a tabs properties run.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="3c826-139">Attribute</span><span class="sxs-lookup"><span data-stu-id="3c826-139">Attributes</span></span>

<span data-ttu-id="3c826-140">Keine.</span><span class="sxs-lookup"><span data-stu-id="3c826-140">None.</span></span>
  

