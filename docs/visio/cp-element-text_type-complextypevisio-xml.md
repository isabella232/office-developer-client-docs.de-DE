---
title: CP-Element (Text_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4edd0a3f-e433-bf54-34cd-3b05fd10a5a5
description: Markiert der Anfang der Zeicheneigenschaften eines ausführen, d. h., formatiert gemäß dem entsprechenden Char-Element. Die Ausführung wird an das Ende des Texts oder bis zum nächsten Tag definiert.
ms.openlocfilehash: 16e5bb94afeb860220c6cb49a9b98e36e45d76cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796761"
---
# <a name="cp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="1d78e-104">CP-Element (Text_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="1d78e-104">cp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="1d78e-105">Markiert der Anfang der Zeicheneigenschaften eines ausführen, d. h., formatiert gemäß dem entsprechenden Char-Element.</span><span class="sxs-lookup"><span data-stu-id="1d78e-105">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span> <span data-ttu-id="1d78e-106">Die Ausführung wird an das Ende des Texts oder bis zum nächsten Tag definiert.</span><span class="sxs-lookup"><span data-stu-id="1d78e-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1d78e-107">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1d78e-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d78e-108">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="1d78e-108">**Element type**</span></span> <br/> |[<span data-ttu-id="1d78e-109">cp_Type</span><span class="sxs-lookup"><span data-stu-id="1d78e-109">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1d78e-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1d78e-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1d78e-111">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="1d78e-111">**Schema file**</span></span> <br/> |<span data-ttu-id="1d78e-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1d78e-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1d78e-113">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="1d78e-113">**Document parts**</span></span> <br/> |<span data-ttu-id="1d78e-114">Seite # .xml, Gestaltungsvorlagen # .xml</span><span class="sxs-lookup"><span data-stu-id="1d78e-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1d78e-115">Definition</span><span class="sxs-lookup"><span data-stu-id="1d78e-115">Definition</span></span>

```XML
< xs:element name="cp" type="cp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1d78e-116">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="1d78e-116">Elements and attributes</span></span>

<span data-ttu-id="1d78e-117">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="1d78e-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1d78e-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1d78e-118">Parent elements</span></span>

|<span data-ttu-id="1d78e-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="1d78e-119">**Element**</span></span>|<span data-ttu-id="1d78e-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1d78e-120">**Type**</span></span>|<span data-ttu-id="1d78e-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1d78e-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1d78e-122">Text</span><span class="sxs-lookup"><span data-stu-id="1d78e-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1d78e-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="1d78e-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1d78e-124">Enthält den Text eines Shapes.</span><span class="sxs-lookup"><span data-stu-id="1d78e-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1d78e-125">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1d78e-125">Child elements</span></span>

<span data-ttu-id="1d78e-126">Keine.</span><span class="sxs-lookup"><span data-stu-id="1d78e-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1d78e-127">Attribute</span><span class="sxs-lookup"><span data-stu-id="1d78e-127">Attributes</span></span>

|<span data-ttu-id="1d78e-128">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1d78e-128">**Attribute**</span></span>|<span data-ttu-id="1d78e-129">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1d78e-129">**Type**</span></span>|<span data-ttu-id="1d78e-130">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="1d78e-130">**Required**</span></span>|<span data-ttu-id="1d78e-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1d78e-131">**Description**</span></span>|<span data-ttu-id="1d78e-132">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="1d78e-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1d78e-133">IX</span><span class="sxs-lookup"><span data-stu-id="1d78e-133">IX</span></span>  <br/> |<span data-ttu-id="1d78e-134">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1d78e-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1d78e-135">erforderlich</span><span class="sxs-lookup"><span data-stu-id="1d78e-135">required</span></span>  <br/> |<span data-ttu-id="1d78e-136">Der Index des Char-Element, den diese Eigenschaft ausführen darstellt.</span><span class="sxs-lookup"><span data-stu-id="1d78e-136">The Char element index that this property run represents.</span></span>  <br/> |<span data-ttu-id="1d78e-137">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1d78e-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

