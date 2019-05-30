---
title: EventItem-Element (EventList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Kapselt einen Ereigniscode.
ms.openlocfilehash: 0db88a175d3e0330cb648f870559d9d2bd4dc1d8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541841"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a><span data-ttu-id="7f50c-103">EventItem-Element (EventList_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="7f50c-103">EventItem element (EventList_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="7f50c-104">Kapselt einen Ereigniscode.</span><span class="sxs-lookup"><span data-stu-id="7f50c-104">Encapsulates an event code.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7f50c-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7f50c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7f50c-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="7f50c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7f50c-107">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="7f50c-107">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7f50c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7f50c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7f50c-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="7f50c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7f50c-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="7f50c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7f50c-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="7f50c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7f50c-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="7f50c-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7f50c-113">Definition</span><span class="sxs-lookup"><span data-stu-id="7f50c-113">Definition</span></span>

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7f50c-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="7f50c-114">Elements and attributes</span></span>

<span data-ttu-id="7f50c-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="7f50c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7f50c-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7f50c-116">Parent elements</span></span>

|<span data-ttu-id="7f50c-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="7f50c-117">**Element**</span></span>|<span data-ttu-id="7f50c-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="7f50c-118">**Type**</span></span>|<span data-ttu-id="7f50c-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7f50c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7f50c-120">EventList</span><span class="sxs-lookup"><span data-stu-id="7f50c-120">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7f50c-121">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="7f50c-121">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7f50c-122">Enthält ein **EventItem** -Element für jedes Ereignis, auf das ein Objekt reagieren soll.</span><span class="sxs-lookup"><span data-stu-id="7f50c-122">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7f50c-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7f50c-123">Child elements</span></span>

<span data-ttu-id="7f50c-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="7f50c-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7f50c-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="7f50c-125">Attributes</span></span>

|<span data-ttu-id="7f50c-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7f50c-126">**Attribute**</span></span>|<span data-ttu-id="7f50c-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="7f50c-127">**Type**</span></span>|<span data-ttu-id="7f50c-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="7f50c-128">**Required**</span></span>|<span data-ttu-id="7f50c-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7f50c-129">**Description**</span></span>|<span data-ttu-id="7f50c-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="7f50c-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7f50c-131">Aktion</span><span class="sxs-lookup"><span data-stu-id="7f50c-131">Action</span></span>  <br/> |<span data-ttu-id="7f50c-132">XSD: unsignedShort abgeleitet</span><span class="sxs-lookup"><span data-stu-id="7f50c-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="7f50c-133">erforderlich</span><span class="sxs-lookup"><span data-stu-id="7f50c-133">required</span></span>  <br/> |<span data-ttu-id="7f50c-134">Gibt den Aktionscode des übergeordneten **EventItem** -Elements an.</span><span class="sxs-lookup"><span data-stu-id="7f50c-134">Specifies the action code of the parent **EventItem** element.</span></span>  <br/> |<span data-ttu-id="7f50c-135">Werte des XSD: unsignedShort abgeleitet-Typs.</span><span class="sxs-lookup"><span data-stu-id="7f50c-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="7f50c-136">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="7f50c-136">Enabled</span></span>  <br/> |<span data-ttu-id="7f50c-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="7f50c-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7f50c-138">Optional</span><span class="sxs-lookup"><span data-stu-id="7f50c-138">optional</span></span>  <br/> |<span data-ttu-id="7f50c-139">Stellt ein Flag dar, das angibt, ob das Ereignis aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7f50c-139">Represents a flag indicating if the event is enabled or disabled.</span></span>  <br/> |<span data-ttu-id="7f50c-140">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="7f50c-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="7f50c-141">EventCode</span><span class="sxs-lookup"><span data-stu-id="7f50c-141">EventCode</span></span>  <br/> |<span data-ttu-id="7f50c-142">XSD: unsignedShort abgeleitet</span><span class="sxs-lookup"><span data-stu-id="7f50c-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="7f50c-143">erforderlich</span><span class="sxs-lookup"><span data-stu-id="7f50c-143">required</span></span>  <br/> |<span data-ttu-id="7f50c-144">Ein Code, der das Ereignis angibt, das das Add-on auslöst.</span><span class="sxs-lookup"><span data-stu-id="7f50c-144">A code indicating the event that triggers the add-on.</span></span>  <br/> |<span data-ttu-id="7f50c-145">Werte des XSD: unsignedShort abgeleitet-Typs.</span><span class="sxs-lookup"><span data-stu-id="7f50c-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="7f50c-146">ID</span><span class="sxs-lookup"><span data-stu-id="7f50c-146">ID</span></span>  <br/> |<span data-ttu-id="7f50c-147">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7f50c-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7f50c-148">erforderlich</span><span class="sxs-lookup"><span data-stu-id="7f50c-148">required</span></span>  <br/> |<span data-ttu-id="7f50c-149">Die ID des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="7f50c-149">The ID of the event.</span></span>  <br/> |<span data-ttu-id="7f50c-150">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="7f50c-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7f50c-151">Ziel</span><span class="sxs-lookup"><span data-stu-id="7f50c-151">Target</span></span>  <br/> |<span data-ttu-id="7f50c-152">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7f50c-152">xsd:string</span></span>  <br/> |<span data-ttu-id="7f50c-153">erforderlich</span><span class="sxs-lookup"><span data-stu-id="7f50c-153">required</span></span>  <br/> |<span data-ttu-id="7f50c-154">Gibt das Ziel eines Ereignisses an.</span><span class="sxs-lookup"><span data-stu-id="7f50c-154">Specifies the target of an event.</span></span>  <br/> |<span data-ttu-id="7f50c-155">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="7f50c-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7f50c-156">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="7f50c-156">TargetArgs</span></span>  <br/> |<span data-ttu-id="7f50c-157">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7f50c-157">xsd:string</span></span>  <br/> |<span data-ttu-id="7f50c-158">erforderlich</span><span class="sxs-lookup"><span data-stu-id="7f50c-158">required</span></span>  <br/> |<span data-ttu-id="7f50c-159">Gibt eine Zeichenfolge mit Argumenten an, die an das Ziel eines Ereignisses gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f50c-159">Specifies a string containing arguments to be sent to the target of an event.</span></span>  <br/> |<span data-ttu-id="7f50c-160">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="7f50c-160">Values of the xsd:string type.</span></span>  <br/> |
   

