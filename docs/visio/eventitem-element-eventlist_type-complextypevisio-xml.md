---
title: EventItem-Element (EventList_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Kapselt einen Ereigniscode.
ms.openlocfilehash: 6ed539bd6cb4524b2498b636295442bed917c72a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337198"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a><span data-ttu-id="d6fd1-103">EventItem-Element (EventList_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="d6fd1-103">EventItem element (EventList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="d6fd1-104">Kapselt einen Ereigniscode.</span><span class="sxs-lookup"><span data-stu-id="d6fd1-104">Encapsulates an event code.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d6fd1-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d6fd1-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d6fd1-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="d6fd1-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d6fd1-107">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="d6fd1-107">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d6fd1-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d6fd1-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d6fd1-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="d6fd1-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d6fd1-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="d6fd1-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d6fd1-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="d6fd1-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d6fd1-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="d6fd1-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d6fd1-113">Definition</span><span class="sxs-lookup"><span data-stu-id="d6fd1-113">Definition</span></span>

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d6fd1-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="d6fd1-114">Elements and attributes</span></span>

<span data-ttu-id="d6fd1-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="d6fd1-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d6fd1-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d6fd1-116">Parent elements</span></span>

|<span data-ttu-id="d6fd1-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="d6fd1-117">**Element**</span></span>|<span data-ttu-id="d6fd1-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d6fd1-118">**Type**</span></span>|<span data-ttu-id="d6fd1-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6fd1-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d6fd1-120">EventList</span><span class="sxs-lookup"><span data-stu-id="d6fd1-120">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d6fd1-121">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="d6fd1-121">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d6fd1-122">Enthält ein **EventItem** -Element für jedes Ereignis, auf das ein Objekt reagieren soll.</span><span class="sxs-lookup"><span data-stu-id="d6fd1-122">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d6fd1-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d6fd1-123">Child elements</span></span>

<span data-ttu-id="d6fd1-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="d6fd1-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d6fd1-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="d6fd1-125">Attributes</span></span>

|<span data-ttu-id="d6fd1-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d6fd1-126">**Attribute**</span></span>|<span data-ttu-id="d6fd1-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d6fd1-127">**Type**</span></span>|<span data-ttu-id="d6fd1-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d6fd1-128">**Required**</span></span>|<span data-ttu-id="d6fd1-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6fd1-129">**Description**</span></span>|<span data-ttu-id="d6fd1-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="d6fd1-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d6fd1-131">Aktion</span><span class="sxs-lookup"><span data-stu-id="d6fd1-131">Action</span></span>  <br/> |<span data-ttu-id="d6fd1-132">XSD: unsignedShort abgeleitet</span><span class="sxs-lookup"><span data-stu-id="d6fd1-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="d6fd1-133">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d6fd1-133">required</span></span>  <br/> |<span data-ttu-id="d6fd1-134">Gibt den Aktionscode des übergeordneten **EventItem** -Elements an.</span><span class="sxs-lookup"><span data-stu-id="d6fd1-134">Specifies the action code of the parent **EventItem** element.</span></span>  <br/> |<span data-ttu-id="d6fd1-135">Werte des XSD: unsignedShort abgeleitet-Typs.</span><span class="sxs-lookup"><span data-stu-id="d6fd1-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="d6fd1-136">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="d6fd1-136">Enabled</span></span>  <br/> |<span data-ttu-id="d6fd1-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="d6fd1-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d6fd1-138">Optional</span><span class="sxs-lookup"><span data-stu-id="d6fd1-138">optional</span></span>  <br/> |<span data-ttu-id="d6fd1-139">Stellt ein Flag dar, das angibt, ob das Ereignis aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d6fd1-139">Represents a flag indicating if the event is enabled or disabled.</span></span>  <br/> |<span data-ttu-id="d6fd1-140">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="d6fd1-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d6fd1-141">EventCode</span><span class="sxs-lookup"><span data-stu-id="d6fd1-141">EventCode</span></span>  <br/> |<span data-ttu-id="d6fd1-142">XSD: unsignedShort abgeleitet</span><span class="sxs-lookup"><span data-stu-id="d6fd1-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="d6fd1-143">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d6fd1-143">required</span></span>  <br/> |<span data-ttu-id="d6fd1-144">Ein Code, der das Ereignis angibt, das das Add-on auslöst.</span><span class="sxs-lookup"><span data-stu-id="d6fd1-144">A code indicating the event that triggers the add-on.</span></span>  <br/> |<span data-ttu-id="d6fd1-145">Werte des XSD: unsignedShort abgeleitet-Typs.</span><span class="sxs-lookup"><span data-stu-id="d6fd1-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="d6fd1-146">ID</span><span class="sxs-lookup"><span data-stu-id="d6fd1-146">ID</span></span>  <br/> |<span data-ttu-id="d6fd1-147">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d6fd1-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d6fd1-148">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d6fd1-148">required</span></span>  <br/> |<span data-ttu-id="d6fd1-149">Die ID des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="d6fd1-149">The ID of the event.</span></span>  <br/> |<span data-ttu-id="d6fd1-150">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="d6fd1-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d6fd1-151">Ziel</span><span class="sxs-lookup"><span data-stu-id="d6fd1-151">Target</span></span>  <br/> |<span data-ttu-id="d6fd1-152">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d6fd1-152">xsd:string</span></span>  <br/> |<span data-ttu-id="d6fd1-153">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d6fd1-153">required</span></span>  <br/> |<span data-ttu-id="d6fd1-154">Gibt das Ziel eines Ereignisses an.</span><span class="sxs-lookup"><span data-stu-id="d6fd1-154">Specifies the target of an event.</span></span>  <br/> |<span data-ttu-id="d6fd1-155">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="d6fd1-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d6fd1-156">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="d6fd1-156">TargetArgs</span></span>  <br/> |<span data-ttu-id="d6fd1-157">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d6fd1-157">xsd:string</span></span>  <br/> |<span data-ttu-id="d6fd1-158">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d6fd1-158">required</span></span>  <br/> |<span data-ttu-id="d6fd1-159">Gibt eine Zeichenfolge mit Argumenten an, die an das Ziel eines Ereignisses gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d6fd1-159">Specifies a string containing arguments to be sent to the target of an event.</span></span>  <br/> |<span data-ttu-id="d6fd1-160">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="d6fd1-160">Values of the xsd:string type.</span></span>  <br/> |
   

