---
title: VisioDocument-Element (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5954685-3a2d-7848-388f-5dd7e536551c
description: Das Stammelement eines Microsoft-Visio Dokument.
ms.openlocfilehash: acb0a4e8ef1efb6d6d5872118241e36bb4e9630c
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538487"
---
# <a name="visiodocument-element-visio-xml"></a><span data-ttu-id="acdf7-103">VisioDocument-Element (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="acdf7-103">VisioDocument element (Visio XML)</span></span>

<span data-ttu-id="acdf7-104">Das Stammelement eines Microsoft-Visio Dokument.</span><span class="sxs-lookup"><span data-stu-id="acdf7-104">The root element of a Microsoft Visio document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="acdf7-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="acdf7-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="acdf7-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="acdf7-106">**Element type**</span></span> <br/> |[<span data-ttu-id="acdf7-107">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="acdf7-107">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="acdf7-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="acdf7-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="acdf7-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="acdf7-109">**Schema file**</span></span> <br/> |<span data-ttu-id="acdf7-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="acdf7-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="acdf7-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="acdf7-111">**Document parts**</span></span> <br/> |<span data-ttu-id="acdf7-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="acdf7-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="acdf7-113">Definition</span><span class="sxs-lookup"><span data-stu-id="acdf7-113">Definition</span></span>

```XML
< xs:element name="VisioDocument" type="VisioDocument_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="acdf7-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="acdf7-114">Elements and attributes</span></span>

<span data-ttu-id="acdf7-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="acdf7-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="acdf7-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="acdf7-116">Parent elements</span></span>

<span data-ttu-id="acdf7-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="acdf7-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="acdf7-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="acdf7-118">Child elements</span></span>

|<span data-ttu-id="acdf7-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="acdf7-119">**Element**</span></span>|<span data-ttu-id="acdf7-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="acdf7-120">**Type**</span></span>|<span data-ttu-id="acdf7-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="acdf7-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="acdf7-122">Colors</span><span class="sxs-lookup"><span data-stu-id="acdf7-122">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="acdf7-123">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="acdf7-123">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="acdf7-124">Enthält die Farbtabelle des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="acdf7-124">Contains the document's color table.</span></span>  <br/> |
|[<span data-ttu-id="acdf7-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="acdf7-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="acdf7-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="acdf7-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="acdf7-127">Enthält Elemente, die Dokumenteinstellungen angeben.</span><span class="sxs-lookup"><span data-stu-id="acdf7-127">Contains elements that specify document settings.</span></span>  <br/> |
|[<span data-ttu-id="acdf7-128">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="acdf7-128">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="acdf7-129">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="acdf7-129">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="acdf7-130">Gibt die **ShapeSheet-Struktur** eines Dokuments an.</span><span class="sxs-lookup"><span data-stu-id="acdf7-130">Specifies a document's **ShapeSheet** structure.</span></span>  <br/> |
|[<span data-ttu-id="acdf7-131">EventList</span><span class="sxs-lookup"><span data-stu-id="acdf7-131">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="acdf7-132">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="acdf7-132">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="acdf7-133">Enthält ein **EventItem-Element** für jedes Ereignis, auf das ein Objekt antworten soll.</span><span class="sxs-lookup"><span data-stu-id="acdf7-133">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
|[<span data-ttu-id="acdf7-134">FaceNames</span><span class="sxs-lookup"><span data-stu-id="acdf7-134">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="acdf7-135">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="acdf7-135">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="acdf7-136">Enthält eine Auflistung von **FaceName-Elementen.**</span><span class="sxs-lookup"><span data-stu-id="acdf7-136">Contains a collection of **FaceName** elements.</span></span>  <br/> |
|[<span data-ttu-id="acdf7-137">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="acdf7-137">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="acdf7-138">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="acdf7-138">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="acdf7-139">Enthält Elemente für die Kopf- und Fußzeile eines Dokuments.</span><span class="sxs-lookup"><span data-stu-id="acdf7-139">Contains elements for a document's header and footer.</span></span>  <br/> |
|[<span data-ttu-id="acdf7-140">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="acdf7-140">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="acdf7-141">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="acdf7-141">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="acdf7-142">Gibt den Satz von Zeichnungsseiten an, die angezeigt werden können, und Datensatzsätze, die in einer Zeichnung aktualisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="acdf7-142">Specifies the set of drawing pages that are viewable and set of recordsets that are refreshable in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="acdf7-143">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="acdf7-143">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="acdf7-144">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="acdf7-144">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="acdf7-145">Enthält eine Auflistung von StyleSheet-Elementen für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="acdf7-145">Contains a collection of StyleSheet elements for the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="acdf7-146">Attribute</span><span class="sxs-lookup"><span data-stu-id="acdf7-146">Attributes</span></span>

<span data-ttu-id="acdf7-147">Keine.</span><span class="sxs-lookup"><span data-stu-id="acdf7-147">None.</span></span>
  

