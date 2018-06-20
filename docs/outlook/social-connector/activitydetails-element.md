---
title: ActivityDetails Element
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: Das Element ActivityDetails speichert die Rohdaten für eine einzelne Aktivitätsfeed-Element. Jede Aktivitätsfeed-Element muss ein eigene ActivityDetails-Element enthalten. Daten im ActivityDetails-Element werden mithilfe der Name-Elemente in Aktivitätsvorlagen verwiesen.
ms.openlocfilehash: c326017a038dff138d690b020a98972a08212690
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795956"
---
# <a name="activitydetails-element"></a><span data-ttu-id="6646c-105">ActivityDetails Element</span><span class="sxs-lookup"><span data-stu-id="6646c-105">activityDetails Element</span></span>

<span data-ttu-id="6646c-106">Das Element **ActivityDetails** speichert die Rohdaten für eine einzelne Aktivitätsfeed-Element.</span><span class="sxs-lookup"><span data-stu-id="6646c-106">The **activityDetails** element stores the raw data for a single activity feed item.</span></span> <span data-ttu-id="6646c-107">Jede Aktivitätsfeed-Element muss ein eigene **ActivityDetails** -Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="6646c-107">Each activity feed item must have its own **activityDetails** element.</span></span> <span data-ttu-id="6646c-108">Daten im **ActivityDetails** -Element werden mithilfe der **Name** -Elemente in Aktivitätsvorlagen verwiesen.</span><span class="sxs-lookup"><span data-stu-id="6646c-108">Data in the **activityDetails** element is referenced in activity templates by using **name** elements.</span></span> <span data-ttu-id="6646c-109">Jeder Teil der Daten in das **ActivityDetails** -Element muss ein **Name** -Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="6646c-109">Every piece of data in the **activityDetails** element must have a **name** element.</span></span> 
  
<span data-ttu-id="6646c-110">In der folgenden Tabelle werden die sechs Elemente, die das Element **ActivityDetails** erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="6646c-110">The following table describes the six elements that the **activityDetails** element requires.</span></span> 
  
|<span data-ttu-id="6646c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="6646c-111">**Element**</span></span>|<span data-ttu-id="6646c-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6646c-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6646c-113">**ownerID**</span><span class="sxs-lookup"><span data-stu-id="6646c-113">**ownerID**</span></span> <br/> |<span data-ttu-id="6646c-114">Die ID des Benutzers im sozialen Netzwerk, die diese Aktivität generiert Element-feed.</span><span class="sxs-lookup"><span data-stu-id="6646c-114">The ID of the user on the social network who generated this activity feed item.</span></span>  <br/> |
|<span data-ttu-id="6646c-115">**objectID**</span><span class="sxs-lookup"><span data-stu-id="6646c-115">**objectID**</span></span> <br/> |<span data-ttu-id="6646c-116">Eine eindeutige Zeichenfolge für die Aktivität zum Erkennen von doppelten Elementen feed Element-feed.</span><span class="sxs-lookup"><span data-stu-id="6646c-116">A unique string for the activity feed item to detect duplicate feed items.</span></span>  <br/> |
|<span data-ttu-id="6646c-117">**applicationId**</span><span class="sxs-lookup"><span data-stu-id="6646c-117">**applicationId**</span></span> <br/> |<span data-ttu-id="6646c-118">Eine der zwei eindeutigen IDs, mit denen die Aktivität match-Element mit der Vorlage feed.</span><span class="sxs-lookup"><span data-stu-id="6646c-118">One of two unique IDs that are used to match the activity feed item with its template.</span></span> <span data-ttu-id="6646c-119">Wenn Sie mehrere Anwendungen oder andere Gruppen verfügen, kann dies als Organisator einer Vorlage der ersten Ebene verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6646c-119">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="6646c-120">**templateId**</span><span class="sxs-lookup"><span data-stu-id="6646c-120">**templateId**</span></span> <br/> |<span data-ttu-id="6646c-121">Die zweite eindeutige ID, mit der die Aktivität match-Element mit der Vorlage feed.</span><span class="sxs-lookup"><span data-stu-id="6646c-121">The second unique ID that is used to match the activity feed item with its template.</span></span> <span data-ttu-id="6646c-122">Dies kann als Organisator einer L2-Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6646c-122">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="6646c-123">**publishDate**</span><span class="sxs-lookup"><span data-stu-id="6646c-123">**publishDate**</span></span> <br/> |<span data-ttu-id="6646c-124">Datum und Uhrzeit, die die Aktivitätsfeed Element veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="6646c-124">The date and time that the activity feed item was published.</span></span>  <br/> |
|<span data-ttu-id="6646c-125">**templateVariables**</span><span class="sxs-lookup"><span data-stu-id="6646c-125">**templateVariables**</span></span> <br/> |<span data-ttu-id="6646c-126">Die Daten in die Token für die Aktivität feed Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6646c-126">The data to be used in the tokens for the activity feed item template.</span></span>  <br/> |
   
<span data-ttu-id="6646c-127">Ein Beispiel der Aktivität XML-feed, finden Sie unter [Aktivität Feed XML-Beispiel](activity-feed-xml-example.md)</span><span class="sxs-lookup"><span data-stu-id="6646c-127">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6646c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6646c-128">See also</span></span>

- [<span data-ttu-id="6646c-129">Übersicht über XML-Code für eine Aktivität Element-Feed</span><span class="sxs-lookup"><span data-stu-id="6646c-129">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="6646c-130">ActivityTemplateContainer Element</span><span class="sxs-lookup"><span data-stu-id="6646c-130">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="6646c-131">Vorlagenvariablen</span><span class="sxs-lookup"><span data-stu-id="6646c-131">Template Variables</span></span>](template-variables.md) 
- [<span data-ttu-id="6646c-132">Richtlinien für das Aktivitäten ordnungsgemäß anzeigen</span><span class="sxs-lookup"><span data-stu-id="6646c-132">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="6646c-133">XML-Code für Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="6646c-133">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="6646c-134">Outlook Connector für soziale Netzwerke Anbieter XML-Schema</span><span class="sxs-lookup"><span data-stu-id="6646c-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="6646c-135">Entwickeln eines Providers mit dem OSC-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="6646c-135">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

