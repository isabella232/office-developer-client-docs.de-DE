---
title: activityDetails-Element
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: Das activityDetails-Element speichert die Rohdaten für ein einzelnes Aktivitätsfeedelement. Jedes Aktivitätsfeedelement muss über ein eigenes activityDetails-Element verfügen. Auf Daten im activityDetails-Element wird in Aktivitätsvorlagen mithilfe von Name-Elementen verwiesen.
ms.openlocfilehash: fd9c2136e8e2b687fa281ecda71039809848f63c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434872"
---
# <a name="activitydetails-element"></a><span data-ttu-id="1a8d3-105">activityDetails-Element</span><span class="sxs-lookup"><span data-stu-id="1a8d3-105">activityDetails Element</span></span>

<span data-ttu-id="1a8d3-106">Das **activityDetails-Element** speichert die Rohdaten für ein einzelnes Aktivitätsfeedelement.</span><span class="sxs-lookup"><span data-stu-id="1a8d3-106">The **activityDetails** element stores the raw data for a single activity feed item.</span></span> <span data-ttu-id="1a8d3-107">Jedes Aktivitätsfeedelement muss über ein eigenes **activityDetails-Element** verfügen.</span><span class="sxs-lookup"><span data-stu-id="1a8d3-107">Each activity feed item must have its own **activityDetails** element.</span></span> <span data-ttu-id="1a8d3-108">Auf Daten im **activityDetails-Element** wird in Aktivitätsvorlagen mithilfe von **Name-Elementen** verwiesen.</span><span class="sxs-lookup"><span data-stu-id="1a8d3-108">Data in the **activityDetails** element is referenced in activity templates by using **name** elements.</span></span> <span data-ttu-id="1a8d3-109">Jedes Datenelement im **activityDetails-Element** muss über ein **Name-Element** verfügen.</span><span class="sxs-lookup"><span data-stu-id="1a8d3-109">Every piece of data in the **activityDetails** element must have a **name** element.</span></span> 
  
<span data-ttu-id="1a8d3-110">In der folgenden Tabelle werden die sechs Elemente beschrieben, die für **das activityDetails-Element** erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="1a8d3-110">The following table describes the six elements that the **activityDetails** element requires.</span></span> 
  
|<span data-ttu-id="1a8d3-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1a8d3-111">**Element**</span></span>|<span data-ttu-id="1a8d3-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1a8d3-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1a8d3-113">**ownerID**</span><span class="sxs-lookup"><span data-stu-id="1a8d3-113">**ownerID**</span></span> <br/> |<span data-ttu-id="1a8d3-114">Die ID des Benutzers im sozialen Netzwerk, der dieses Aktivitätsfeedelement generiert hat.</span><span class="sxs-lookup"><span data-stu-id="1a8d3-114">The ID of the user on the social network who generated this activity feed item.</span></span>  <br/> |
|<span data-ttu-id="1a8d3-115">**objectID**</span><span class="sxs-lookup"><span data-stu-id="1a8d3-115">**objectID**</span></span> <br/> |<span data-ttu-id="1a8d3-116">Eine eindeutige Zeichenfolge für das Aktivitätsfeedelement zum Erkennen doppelter Feedelemente.</span><span class="sxs-lookup"><span data-stu-id="1a8d3-116">A unique string for the activity feed item to detect duplicate feed items.</span></span>  <br/> |
|<span data-ttu-id="1a8d3-117">**applicationId**</span><span class="sxs-lookup"><span data-stu-id="1a8d3-117">**applicationId**</span></span> <br/> |<span data-ttu-id="1a8d3-118">Eine von zwei eindeutigen IDs, die verwendet werden, um dem Aktivitätsfeedelement mit seiner Vorlage zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1a8d3-118">One of two unique IDs that are used to match the activity feed item with its template.</span></span> <span data-ttu-id="1a8d3-119">Wenn Sie über mehrere Anwendungen oder andere Gruppierungen verfügen, kann dies als Vorlagenorganisator der ersten Ebene verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a8d3-119">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="1a8d3-120">**templateId**</span><span class="sxs-lookup"><span data-stu-id="1a8d3-120">**templateId**</span></span> <br/> |<span data-ttu-id="1a8d3-121">Die zweite eindeutige ID, die verwendet wird, um dem Aktivitätsfeedelement mit seiner Vorlage zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1a8d3-121">The second unique ID that is used to match the activity feed item with its template.</span></span> <span data-ttu-id="1a8d3-122">Dies kann als Vorlagenorganisator der zweiten Ebene verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a8d3-122">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="1a8d3-123">**publishDate**</span><span class="sxs-lookup"><span data-stu-id="1a8d3-123">**publishDate**</span></span> <br/> |<span data-ttu-id="1a8d3-124">Datum und Uhrzeit der Veröffentlichung des Aktivitätsfeedelements.</span><span class="sxs-lookup"><span data-stu-id="1a8d3-124">The date and time that the activity feed item was published.</span></span>  <br/> |
|<span data-ttu-id="1a8d3-125">**templateVariables**</span><span class="sxs-lookup"><span data-stu-id="1a8d3-125">**templateVariables**</span></span> <br/> |<span data-ttu-id="1a8d3-126">Die Daten, die in den Token für die Aktivitätsfeedelementvorlage verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1a8d3-126">The data to be used in the tokens for the activity feed item template.</span></span>  <br/> |
   
<span data-ttu-id="1a8d3-127">Ein Beispiel für Aktivitätsfeed-XML finden Sie unter [Activity Feed XML Example](activity-feed-xml-example.md)</span><span class="sxs-lookup"><span data-stu-id="1a8d3-127">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1a8d3-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a8d3-128">See also</span></span>

- [<span data-ttu-id="1a8d3-129">Übersicht über XML für ein Aktivitätsfeedelement</span><span class="sxs-lookup"><span data-stu-id="1a8d3-129">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="1a8d3-130">activityTemplateContainer-Element</span><span class="sxs-lookup"><span data-stu-id="1a8d3-130">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="1a8d3-131">Vorlagenvariablen</span><span class="sxs-lookup"><span data-stu-id="1a8d3-131">Template Variables</span></span>](template-variables.md) 
- [<span data-ttu-id="1a8d3-132">Richtlinien für die ordnungsgemäßen Anzeige von Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="1a8d3-132">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="1a8d3-133">XML für Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="1a8d3-133">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="1a8d3-134">Outlook XML-Schema des Anbieters für sozialen Connector</span><span class="sxs-lookup"><span data-stu-id="1a8d3-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="1a8d3-135">Entwickeln eines Providers mit dem OSC-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="1a8d3-135">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

