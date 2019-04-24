---
title: VisioDocument-Element (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5954685-3a2d-7848-388f-5dd7e536551c
description: Das Stammelement eines Microsoft Visio-Dokuments.
ms.openlocfilehash: 9829fa8960d78777e0fff4306b96978da90a647d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285313"
---
# <a name="visiodocument-element-visio-xml"></a><span data-ttu-id="cb76a-103">VisioDocument-Element (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="cb76a-103">VisioDocument element ('Visio XML')</span></span>

<span data-ttu-id="cb76a-104">Das Stammelement eines Microsoft Visio-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="cb76a-104">The root element of a Microsoft Visio document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cb76a-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="cb76a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb76a-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="cb76a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="cb76a-107">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="cb76a-107">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="cb76a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cb76a-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="cb76a-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="cb76a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="cb76a-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="cb76a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="cb76a-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="cb76a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="cb76a-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="cb76a-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cb76a-113">Definition</span><span class="sxs-lookup"><span data-stu-id="cb76a-113">Definition</span></span>

```XML
< xs:element name="VisioDocument" type="VisioDocument_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cb76a-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="cb76a-114">Elements and attributes</span></span>

<span data-ttu-id="cb76a-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="cb76a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="cb76a-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cb76a-116">Parent elements</span></span>

<span data-ttu-id="cb76a-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="cb76a-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cb76a-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cb76a-118">Child elements</span></span>

|<span data-ttu-id="cb76a-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="cb76a-119">**Element**</span></span>|<span data-ttu-id="cb76a-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="cb76a-120">**Type**</span></span>|<span data-ttu-id="cb76a-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cb76a-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cb76a-122">Colors</span><span class="sxs-lookup"><span data-stu-id="cb76a-122">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cb76a-123">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="cb76a-123">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cb76a-124">Enthält die Farbtabelle des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="cb76a-124">Contains the document's color table.</span></span>  <br/> |
|[<span data-ttu-id="cb76a-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="cb76a-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cb76a-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="cb76a-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cb76a-127">Enthält Elemente, die Dokumenteinstellungen angeben.</span><span class="sxs-lookup"><span data-stu-id="cb76a-127">Contains elements that specify document settings.</span></span>  <br/> |
|[<span data-ttu-id="cb76a-128">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="cb76a-128">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cb76a-129">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="cb76a-129">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cb76a-130">Gibt die **ShapeSheet** -Struktur eines Dokuments an.</span><span class="sxs-lookup"><span data-stu-id="cb76a-130">Specifies a document's **ShapeSheet** structure.</span></span>  <br/> |
|[<span data-ttu-id="cb76a-131">EventList</span><span class="sxs-lookup"><span data-stu-id="cb76a-131">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cb76a-132">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="cb76a-132">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cb76a-133">Enthält ein **EventItem** -Element für jedes Ereignis, auf das ein Objekt reagieren soll.</span><span class="sxs-lookup"><span data-stu-id="cb76a-133">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
|[<span data-ttu-id="cb76a-134">FaceNames</span><span class="sxs-lookup"><span data-stu-id="cb76a-134">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cb76a-135">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="cb76a-135">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cb76a-136">Enthält eine Auflistung von **FaceName** -Elementen.</span><span class="sxs-lookup"><span data-stu-id="cb76a-136">Contains a collection of **FaceName** elements.</span></span>  <br/> |
|[<span data-ttu-id="cb76a-137">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="cb76a-137">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cb76a-138">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="cb76a-138">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cb76a-139">Enthält Elemente für die Kopf-und Fußzeile eines Dokuments.</span><span class="sxs-lookup"><span data-stu-id="cb76a-139">Contains elements for a document's header and footer.</span></span>  <br/> |
|[<span data-ttu-id="cb76a-140">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="cb76a-140">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cb76a-141">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="cb76a-141">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cb76a-142">Gibt den Satz von Zeichnungs Seiten an, die angezeigt werden, und einen Satz von Recordsets, die in einer Zeichnung aktualisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="cb76a-142">Specifies the set of drawing pages that are viewable and set of recordsets that are refreshable in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="cb76a-143">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="cb76a-143">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cb76a-144">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="cb76a-144">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cb76a-145">Enthält eine Auflistung von StyleSheet-Elementen für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="cb76a-145">Contains a collection of StyleSheet elements for the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="cb76a-146">Attribute</span><span class="sxs-lookup"><span data-stu-id="cb76a-146">Attributes</span></span>

<span data-ttu-id="cb76a-147">Keine.</span><span class="sxs-lookup"><span data-stu-id="cb76a-147">None.</span></span>
  

