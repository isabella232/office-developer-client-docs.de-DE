---
title: EventItem-Element (EventList_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Einen Ereigniscode kapselt.
ms.openlocfilehash: 6ed539bd6cb4524b2498b636295442bed917c72a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394398"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a><span data-ttu-id="a125a-103">EventItem-Element (EventList_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="a125a-103">EventItem element (EventList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="a125a-104">Einen Ereigniscode kapselt.</span><span class="sxs-lookup"><span data-stu-id="a125a-104">Encapsulates an event code.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a125a-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a125a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a125a-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="a125a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a125a-107">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="a125a-107">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a125a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a125a-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a125a-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="a125a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a125a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a125a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a125a-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="a125a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a125a-112">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="a125a-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a125a-113">Definition</span><span class="sxs-lookup"><span data-stu-id="a125a-113">Definition</span></span>

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a125a-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="a125a-114">Elements and attributes</span></span>

<span data-ttu-id="a125a-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="a125a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a125a-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a125a-116">Parent elements</span></span>

|<span data-ttu-id="a125a-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="a125a-117">**Element**</span></span>|<span data-ttu-id="a125a-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="a125a-118">**Type**</span></span>|<span data-ttu-id="a125a-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a125a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a125a-120">EventList</span><span class="sxs-lookup"><span data-stu-id="a125a-120">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a125a-121">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="a125a-121">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a125a-122">Enthält ein Element **EventItem** für jedes Ereignis, der ein Objekt Antworten sollen.</span><span class="sxs-lookup"><span data-stu-id="a125a-122">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a125a-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a125a-123">Child elements</span></span>

<span data-ttu-id="a125a-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="a125a-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a125a-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="a125a-125">Attributes</span></span>

|<span data-ttu-id="a125a-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a125a-126">**Attribute**</span></span>|<span data-ttu-id="a125a-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="a125a-127">**Type**</span></span>|<span data-ttu-id="a125a-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="a125a-128">**Required**</span></span>|<span data-ttu-id="a125a-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a125a-129">**Description**</span></span>|<span data-ttu-id="a125a-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="a125a-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a125a-131">Aktion</span><span class="sxs-lookup"><span data-stu-id="a125a-131">Action</span></span>  <br/> |<span data-ttu-id="a125a-132">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="a125a-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="a125a-133">erforderlich</span><span class="sxs-lookup"><span data-stu-id="a125a-133">required</span></span>  <br/> |<span data-ttu-id="a125a-134">Gibt an, der Aktionscode des übergeordneten Elements **EventItem** .</span><span class="sxs-lookup"><span data-stu-id="a125a-134">Specifies the action code of the parent **EventItem** element.</span></span>  <br/> |<span data-ttu-id="a125a-135">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="a125a-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="a125a-136">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="a125a-136">Enabled</span></span>  <br/> |<span data-ttu-id="a125a-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="a125a-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a125a-138">Optional</span><span class="sxs-lookup"><span data-stu-id="a125a-138">optional</span></span>  <br/> |<span data-ttu-id="a125a-139">Stellt ein Flag gibt an, ob das Ereignis aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a125a-139">Represents a flag indicating if the event is enabled or disabled.</span></span>  <br/> |<span data-ttu-id="a125a-140">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="a125a-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a125a-141">Ereigniscode</span><span class="sxs-lookup"><span data-stu-id="a125a-141">EventCode</span></span>  <br/> |<span data-ttu-id="a125a-142">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="a125a-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="a125a-143">erforderlich</span><span class="sxs-lookup"><span data-stu-id="a125a-143">required</span></span>  <br/> |<span data-ttu-id="a125a-144">Ein Code, der das Ereignis, das das Add-on angibt.</span><span class="sxs-lookup"><span data-stu-id="a125a-144">A code indicating the event that triggers the add-on.</span></span>  <br/> |<span data-ttu-id="a125a-145">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="a125a-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="a125a-146">ID</span><span class="sxs-lookup"><span data-stu-id="a125a-146">ID</span></span>  <br/> |<span data-ttu-id="a125a-147">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a125a-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a125a-148">erforderlich</span><span class="sxs-lookup"><span data-stu-id="a125a-148">required</span></span>  <br/> |<span data-ttu-id="a125a-149">Die ID des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="a125a-149">The ID of the event.</span></span>  <br/> |<span data-ttu-id="a125a-150">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a125a-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a125a-151">Ziel</span><span class="sxs-lookup"><span data-stu-id="a125a-151">Target</span></span>  <br/> |<span data-ttu-id="a125a-152">XSD: String</span><span class="sxs-lookup"><span data-stu-id="a125a-152">xsd:string</span></span>  <br/> |<span data-ttu-id="a125a-153">erforderlich</span><span class="sxs-lookup"><span data-stu-id="a125a-153">required</span></span>  <br/> |<span data-ttu-id="a125a-154">Gibt das Ziel eines Ereignisses an.</span><span class="sxs-lookup"><span data-stu-id="a125a-154">Specifies the target of an event.</span></span>  <br/> |<span data-ttu-id="a125a-155">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="a125a-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a125a-156">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="a125a-156">TargetArgs</span></span>  <br/> |<span data-ttu-id="a125a-157">XSD: String</span><span class="sxs-lookup"><span data-stu-id="a125a-157">xsd:string</span></span>  <br/> |<span data-ttu-id="a125a-158">erforderlich</span><span class="sxs-lookup"><span data-stu-id="a125a-158">required</span></span>  <br/> |<span data-ttu-id="a125a-159">Gibt eine Zeichenfolge mit Argumenten, die an das Ziel eines Ereignisses gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="a125a-159">Specifies a string containing arguments to be sent to the target of an event.</span></span>  <br/> |<span data-ttu-id="a125a-160">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="a125a-160">Values of the xsd:string type.</span></span>  <br/> |
   

