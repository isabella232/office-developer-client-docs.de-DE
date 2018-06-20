---
title: EventItem-Element (EventList_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Einen Ereigniscode kapselt.
ms.openlocfilehash: dcdd3aa264e8ddfb1aa6f2e908f1c43a0d470872
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796949"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a><span data-ttu-id="b3791-103">EventItem-Element (EventList_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="b3791-103">EventItem element (EventList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="b3791-104">Einen Ereigniscode kapselt.</span><span class="sxs-lookup"><span data-stu-id="b3791-104">Encapsulates an event code.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b3791-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b3791-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b3791-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="b3791-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b3791-107">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="b3791-107">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b3791-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b3791-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b3791-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="b3791-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b3791-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b3791-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b3791-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="b3791-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b3791-112">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="b3791-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b3791-113">Definition</span><span class="sxs-lookup"><span data-stu-id="b3791-113">Definition</span></span>

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b3791-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="b3791-114">Elements and attributes</span></span>

<span data-ttu-id="b3791-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="b3791-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b3791-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b3791-116">Parent elements</span></span>

|<span data-ttu-id="b3791-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="b3791-117">**Element**</span></span>|<span data-ttu-id="b3791-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="b3791-118">**Type**</span></span>|<span data-ttu-id="b3791-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b3791-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b3791-120">EventList</span><span class="sxs-lookup"><span data-stu-id="b3791-120">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b3791-121">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="b3791-121">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b3791-122">Enthält ein Element **EventItem** für jedes Ereignis, der ein Objekt Antworten sollen.</span><span class="sxs-lookup"><span data-stu-id="b3791-122">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b3791-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b3791-123">Child elements</span></span>

<span data-ttu-id="b3791-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="b3791-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b3791-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="b3791-125">Attributes</span></span>

|<span data-ttu-id="b3791-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b3791-126">**Attribute**</span></span>|<span data-ttu-id="b3791-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="b3791-127">**Type**</span></span>|<span data-ttu-id="b3791-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="b3791-128">**Required**</span></span>|<span data-ttu-id="b3791-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b3791-129">**Description**</span></span>|<span data-ttu-id="b3791-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="b3791-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b3791-131">Aktion</span><span class="sxs-lookup"><span data-stu-id="b3791-131">Action</span></span>  <br/> |<span data-ttu-id="b3791-132">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="b3791-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="b3791-133">erforderlich</span><span class="sxs-lookup"><span data-stu-id="b3791-133">required</span></span>  <br/> |<span data-ttu-id="b3791-134">Gibt an, der Aktionscode des übergeordneten Elements **EventItem** .</span><span class="sxs-lookup"><span data-stu-id="b3791-134">Specifies the action code of the parent **EventItem** element.</span></span>  <br/> |<span data-ttu-id="b3791-135">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="b3791-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="b3791-136">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="b3791-136">Enabled</span></span>  <br/> |<span data-ttu-id="b3791-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="b3791-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="b3791-138">Optional</span><span class="sxs-lookup"><span data-stu-id="b3791-138">optional</span></span>  <br/> |<span data-ttu-id="b3791-139">Stellt ein Flag gibt an, ob das Ereignis aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b3791-139">Represents a flag indicating if the event is enabled or disabled.</span></span>  <br/> |<span data-ttu-id="b3791-140">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="b3791-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="b3791-141">Ereigniscode</span><span class="sxs-lookup"><span data-stu-id="b3791-141">EventCode</span></span>  <br/> |<span data-ttu-id="b3791-142">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="b3791-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="b3791-143">erforderlich</span><span class="sxs-lookup"><span data-stu-id="b3791-143">required</span></span>  <br/> |<span data-ttu-id="b3791-144">Ein Code, der das Ereignis, das das Add-on angibt.</span><span class="sxs-lookup"><span data-stu-id="b3791-144">A code indicating the event that triggers the add-on.</span></span>  <br/> |<span data-ttu-id="b3791-145">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="b3791-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="b3791-146">ID</span><span class="sxs-lookup"><span data-stu-id="b3791-146">ID</span></span>  <br/> |<span data-ttu-id="b3791-147">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b3791-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b3791-148">erforderlich</span><span class="sxs-lookup"><span data-stu-id="b3791-148">required</span></span>  <br/> |<span data-ttu-id="b3791-149">Die ID des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="b3791-149">The ID of the event.</span></span>  <br/> |<span data-ttu-id="b3791-150">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b3791-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b3791-151">Ziel</span><span class="sxs-lookup"><span data-stu-id="b3791-151">Target</span></span>  <br/> |<span data-ttu-id="b3791-152">XSD: String</span><span class="sxs-lookup"><span data-stu-id="b3791-152">xsd:string</span></span>  <br/> |<span data-ttu-id="b3791-153">erforderlich</span><span class="sxs-lookup"><span data-stu-id="b3791-153">required</span></span>  <br/> |<span data-ttu-id="b3791-154">Gibt das Ziel eines Ereignisses an.</span><span class="sxs-lookup"><span data-stu-id="b3791-154">Specifies the target of an event.</span></span>  <br/> |<span data-ttu-id="b3791-155">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="b3791-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b3791-156">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="b3791-156">TargetArgs</span></span>  <br/> |<span data-ttu-id="b3791-157">XSD: String</span><span class="sxs-lookup"><span data-stu-id="b3791-157">xsd:string</span></span>  <br/> |<span data-ttu-id="b3791-158">erforderlich</span><span class="sxs-lookup"><span data-stu-id="b3791-158">required</span></span>  <br/> |<span data-ttu-id="b3791-159">Gibt eine Zeichenfolge mit Argumenten, die an das Ziel eines Ereignisses gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3791-159">Specifies a string containing arguments to be sent to the target of an event.</span></span>  <br/> |<span data-ttu-id="b3791-160">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="b3791-160">Values of the xsd:string type.</span></span>  <br/> |
   

