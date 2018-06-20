---
title: VisioDocument-Element ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5954685-3a2d-7848-388f-5dd7e536551c
description: Das Stammelement eines Microsoft Visio-Dokuments.
ms.openlocfilehash: 5a325b78ec64708246f0c8a6f5396c2ce1569121
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798410"
---
# <a name="visiodocument-element-visio-xml"></a><span data-ttu-id="4a63a-103">VisioDocument-Element ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="4a63a-103">VisioDocument element ('Visio XML')</span></span>

<span data-ttu-id="4a63a-104">Das Stammelement eines Microsoft Visio-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="4a63a-104">The root element of a Microsoft Visio document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4a63a-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4a63a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4a63a-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="4a63a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4a63a-107">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="4a63a-107">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4a63a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4a63a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4a63a-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="4a63a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4a63a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4a63a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4a63a-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="4a63a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4a63a-112">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="4a63a-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4a63a-113">Definition</span><span class="sxs-lookup"><span data-stu-id="4a63a-113">Definition</span></span>

```XML
< xs:element name="VisioDocument" type="VisioDocument_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4a63a-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="4a63a-114">Elements and attributes</span></span>

<span data-ttu-id="4a63a-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="4a63a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4a63a-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4a63a-116">Parent elements</span></span>

<span data-ttu-id="4a63a-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="4a63a-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4a63a-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4a63a-118">Child elements</span></span>

|<span data-ttu-id="4a63a-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="4a63a-119">**Element**</span></span>|<span data-ttu-id="4a63a-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4a63a-120">**Type**</span></span>|<span data-ttu-id="4a63a-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4a63a-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4a63a-122">Colors</span><span class="sxs-lookup"><span data-stu-id="4a63a-122">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4a63a-123">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="4a63a-123">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4a63a-124">Tabelle des Dokuments enthält.</span><span class="sxs-lookup"><span data-stu-id="4a63a-124">Contains the document's color table.</span></span>  <br/> |
|[<span data-ttu-id="4a63a-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="4a63a-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4a63a-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="4a63a-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4a63a-127">Enthält Elemente, die dokumenteinstellungen angeben.</span><span class="sxs-lookup"><span data-stu-id="4a63a-127">Contains elements that specify document settings.</span></span>  <br/> |
|[<span data-ttu-id="4a63a-128">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="4a63a-128">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4a63a-129">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="4a63a-129">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4a63a-130">Gibt die **ShapeSheet** -Struktur eines Dokuments an.</span><span class="sxs-lookup"><span data-stu-id="4a63a-130">Specifies a document's **ShapeSheet** structure.</span></span>  <br/> |
|[<span data-ttu-id="4a63a-131">EventList</span><span class="sxs-lookup"><span data-stu-id="4a63a-131">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4a63a-132">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="4a63a-132">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4a63a-133">Enthält ein Element **EventItem** für jedes Ereignis, der ein Objekt Antworten sollen.</span><span class="sxs-lookup"><span data-stu-id="4a63a-133">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
|[<span data-ttu-id="4a63a-134">FaceNames</span><span class="sxs-lookup"><span data-stu-id="4a63a-134">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4a63a-135">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="4a63a-135">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4a63a-136">Enthält eine Auflistung von **FaceName** -Elementen.</span><span class="sxs-lookup"><span data-stu-id="4a63a-136">Contains a collection of **FaceName** elements.</span></span>  <br/> |
|[<span data-ttu-id="4a63a-137">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="4a63a-137">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4a63a-138">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="4a63a-138">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4a63a-139">Enthält Elemente für Kopf- und Fußzeile eines Dokuments.</span><span class="sxs-lookup"><span data-stu-id="4a63a-139">Contains elements for a document's header and footer.</span></span>  <br/> |
|[<span data-ttu-id="4a63a-140">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="4a63a-140">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4a63a-141">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="4a63a-141">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4a63a-142">Gibt den Satz von Zeichenblättern, die angezeigt werden können und von Recordsets-Objekten, die in einer Zeichnung aktualisierbare sind festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="4a63a-142">Specifies the set of drawing pages that are viewable and set of recordsets that are refreshable in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="4a63a-143">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="4a63a-143">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4a63a-144">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="4a63a-144">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4a63a-145">Enthält eine Auflistung von StyleSheet-Elemente für das Dokument an.</span><span class="sxs-lookup"><span data-stu-id="4a63a-145">Contains a collection of StyleSheet elements for the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4a63a-146">Attribute</span><span class="sxs-lookup"><span data-stu-id="4a63a-146">Attributes</span></span>

<span data-ttu-id="4a63a-147">Keine.</span><span class="sxs-lookup"><span data-stu-id="4a63a-147">None.</span></span>
  

