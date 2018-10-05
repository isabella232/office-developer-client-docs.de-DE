---
title: VisioDocument-Element ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5954685-3a2d-7848-388f-5dd7e536551c
description: Das Stammelement eines Microsoft Visio-Dokuments.
ms.openlocfilehash: 9829fa8960d78777e0fff4306b96978da90a647d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391304"
---
# <a name="visiodocument-element-visio-xml"></a><span data-ttu-id="24758-103">VisioDocument-Element ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="24758-103">VisioDocument element ('Visio XML')</span></span>

<span data-ttu-id="24758-104">Das Stammelement eines Microsoft Visio-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="24758-104">The root element of a Microsoft Visio document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="24758-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="24758-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="24758-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="24758-106">**Element type**</span></span> <br/> |[<span data-ttu-id="24758-107">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="24758-107">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="24758-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="24758-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="24758-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="24758-109">**Schema file**</span></span> <br/> |<span data-ttu-id="24758-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="24758-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="24758-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="24758-111">**Document parts**</span></span> <br/> |<span data-ttu-id="24758-112">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="24758-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="24758-113">Definition</span><span class="sxs-lookup"><span data-stu-id="24758-113">Definition</span></span>

```XML
< xs:element name="VisioDocument" type="VisioDocument_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="24758-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="24758-114">Elements and attributes</span></span>

<span data-ttu-id="24758-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="24758-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="24758-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="24758-116">Parent elements</span></span>

<span data-ttu-id="24758-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="24758-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="24758-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="24758-118">Child elements</span></span>

|<span data-ttu-id="24758-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="24758-119">**Element**</span></span>|<span data-ttu-id="24758-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="24758-120">**Type**</span></span>|<span data-ttu-id="24758-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="24758-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="24758-122">Colors</span><span class="sxs-lookup"><span data-stu-id="24758-122">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="24758-123">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="24758-123">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="24758-124">Tabelle des Dokuments enthält.</span><span class="sxs-lookup"><span data-stu-id="24758-124">Contains the document's color table.</span></span>  <br/> |
|[<span data-ttu-id="24758-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="24758-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="24758-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="24758-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="24758-127">Enthält Elemente, die dokumenteinstellungen angeben.</span><span class="sxs-lookup"><span data-stu-id="24758-127">Contains elements that specify document settings.</span></span>  <br/> |
|[<span data-ttu-id="24758-128">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="24758-128">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="24758-129">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="24758-129">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="24758-130">Gibt die **ShapeSheet** -Struktur eines Dokuments an.</span><span class="sxs-lookup"><span data-stu-id="24758-130">Specifies a document's **ShapeSheet** structure.</span></span>  <br/> |
|[<span data-ttu-id="24758-131">EventList</span><span class="sxs-lookup"><span data-stu-id="24758-131">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="24758-132">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="24758-132">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="24758-133">Enthält ein Element **EventItem** für jedes Ereignis, der ein Objekt Antworten sollen.</span><span class="sxs-lookup"><span data-stu-id="24758-133">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
|[<span data-ttu-id="24758-134">FaceNames</span><span class="sxs-lookup"><span data-stu-id="24758-134">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="24758-135">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="24758-135">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="24758-136">Enthält eine Auflistung von **FaceName** -Elementen.</span><span class="sxs-lookup"><span data-stu-id="24758-136">Contains a collection of **FaceName** elements.</span></span>  <br/> |
|[<span data-ttu-id="24758-137">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="24758-137">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="24758-138">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="24758-138">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="24758-139">Enthält Elemente für Kopf- und Fußzeile eines Dokuments.</span><span class="sxs-lookup"><span data-stu-id="24758-139">Contains elements for a document's header and footer.</span></span>  <br/> |
|[<span data-ttu-id="24758-140">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="24758-140">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="24758-141">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="24758-141">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="24758-142">Gibt den Satz von Zeichenblättern, die angezeigt werden können und von Recordsets-Objekten, die in einer Zeichnung aktualisierbare sind festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="24758-142">Specifies the set of drawing pages that are viewable and set of recordsets that are refreshable in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="24758-143">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="24758-143">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="24758-144">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="24758-144">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="24758-145">Enthält eine Auflistung von StyleSheet-Elemente für das Dokument an.</span><span class="sxs-lookup"><span data-stu-id="24758-145">Contains a collection of StyleSheet elements for the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="24758-146">Attribute</span><span class="sxs-lookup"><span data-stu-id="24758-146">Attributes</span></span>

<span data-ttu-id="24758-147">Keine.</span><span class="sxs-lookup"><span data-stu-id="24758-147">None.</span></span>
  

