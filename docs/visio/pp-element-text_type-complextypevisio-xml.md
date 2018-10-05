---
title: PS-Element (Text_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5444543-fcd9-91cc-e7f8-cf860caa9fcc
description: Gibt an, das Ende einer Absatzeigenschaften ausführen. Die Ausführung wird an das Ende des Texts oder bis zum nächsten Tag definiert.
ms.openlocfilehash: bb2b0ab7a76c142b810ecd02dbc1b5ba7463520a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400102"
---
# <a name="pp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="c3f29-104">PS-Element (Text_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="c3f29-104">pp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="c3f29-105">Gibt an, das Ende einer Absatzeigenschaften ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3f29-105">Specifies the beginning of a paragraph properties run.</span></span> <span data-ttu-id="c3f29-106">Die Ausführung wird an das Ende des Texts oder bis zum nächsten Tag definiert.</span><span class="sxs-lookup"><span data-stu-id="c3f29-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c3f29-107">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c3f29-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c3f29-108">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="c3f29-108">**Element type**</span></span> <br/> |[<span data-ttu-id="c3f29-109">pp_Type</span><span class="sxs-lookup"><span data-stu-id="c3f29-109">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c3f29-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c3f29-110">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c3f29-111">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="c3f29-111">**Schema file**</span></span> <br/> |<span data-ttu-id="c3f29-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c3f29-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c3f29-113">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="c3f29-113">**Document parts**</span></span> <br/> |<span data-ttu-id="c3f29-114">Seite # .xml, Gestaltungsvorlagen # .xml</span><span class="sxs-lookup"><span data-stu-id="c3f29-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c3f29-115">Definition</span><span class="sxs-lookup"><span data-stu-id="c3f29-115">Definition</span></span>

```XML
< xs:element name="pp" type="pp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c3f29-116">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="c3f29-116">Elements and attributes</span></span>

<span data-ttu-id="c3f29-117">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="c3f29-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c3f29-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c3f29-118">Parent elements</span></span>

|<span data-ttu-id="c3f29-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="c3f29-119">**Element**</span></span>|<span data-ttu-id="c3f29-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c3f29-120">**Type**</span></span>|<span data-ttu-id="c3f29-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c3f29-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c3f29-122">Text</span><span class="sxs-lookup"><span data-stu-id="c3f29-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c3f29-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="c3f29-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c3f29-124">Enthält den Text eines Shapes.</span><span class="sxs-lookup"><span data-stu-id="c3f29-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c3f29-125">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c3f29-125">Child elements</span></span>

<span data-ttu-id="c3f29-126">Keine.</span><span class="sxs-lookup"><span data-stu-id="c3f29-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c3f29-127">Attribute</span><span class="sxs-lookup"><span data-stu-id="c3f29-127">Attributes</span></span>

|<span data-ttu-id="c3f29-128">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c3f29-128">**Attribute**</span></span>|<span data-ttu-id="c3f29-129">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c3f29-129">**Type**</span></span>|<span data-ttu-id="c3f29-130">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="c3f29-130">**Required**</span></span>|<span data-ttu-id="c3f29-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c3f29-131">**Description**</span></span>|<span data-ttu-id="c3f29-132">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="c3f29-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c3f29-133">IX</span><span class="sxs-lookup"><span data-stu-id="c3f29-133">IX</span></span>  <br/> |<span data-ttu-id="c3f29-134">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c3f29-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c3f29-135">erforderlich</span><span class="sxs-lookup"><span data-stu-id="c3f29-135">required</span></span>  <br/> |<span data-ttu-id="c3f29-136">Der Index des Elements **Absatz** , der angibt, die Formatierung für diese ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3f29-136">The index of the **Para** element that specifies the formatting applied to this run.</span></span>  <br/> |<span data-ttu-id="c3f29-137">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c3f29-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

