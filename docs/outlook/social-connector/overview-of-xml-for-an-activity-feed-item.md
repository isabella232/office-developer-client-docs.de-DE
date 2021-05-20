---
title: Überblick über XML für ein Aktivitätsfeedelement
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: 'Ein Aktivitätsfeed besteht aus einer oder mehreren Aktivitäten in einem sozialen Netzwerk. Jeder Aktivitätsfeed wird durch ein activityFeed-Element dargestellt und durch die drei folgenden Informationen gekennzeichnet:'
ms.openlocfilehash: 971c54cf69a65bebbe4fd04e8608e88b89145bb4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439947"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a><span data-ttu-id="a641d-104">Überblick über XML für ein Aktivitätsfeedelement</span><span class="sxs-lookup"><span data-stu-id="a641d-104">Overview of XML for an activity feed item</span></span>

<span data-ttu-id="a641d-105">Ein Aktivitätsfeed besteht aus einer oder mehreren Aktivitäten in einem sozialen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="a641d-105">An activity feed consists of one or more activities occurring on a social network.</span></span> <span data-ttu-id="a641d-106">Jeder Aktivitätsfeed wird durch ein **activityFeed-Element** dargestellt und durch die drei folgenden Informationen gekennzeichnet:</span><span class="sxs-lookup"><span data-stu-id="a641d-106">Each activity feed is represented by an **activityFeed** element, and is characterized by these three pieces of information:</span></span> 
  
- <span data-ttu-id="a641d-107">**network**– Name des sozialen Netzwerks, aus dem die Aktivitäten stammen.</span><span class="sxs-lookup"><span data-stu-id="a641d-107">**network**—Name of the social network from which the activities originated.</span></span>
    
- <span data-ttu-id="a641d-108">**activities**– Container für Aktivitäten, die im Konto des angemeldeten Benutzers in diesem sozialen Netzwerk geschehen.</span><span class="sxs-lookup"><span data-stu-id="a641d-108">**activities**—Container for activities happening on the logged on user's account on that social network.</span></span>
    
- <span data-ttu-id="a641d-109">**templates**– Container für Vorlagen, die zum Anzeigen des entsprechenden Aktivitätselements in Aktivitäten **verwendet werden.**</span><span class="sxs-lookup"><span data-stu-id="a641d-109">**templates**—Container for templates that are used to display the corresponding activity item in **activities**.</span></span>
    
<span data-ttu-id="a641d-110">Zum Erstellen eines Aktivitätsfeedelements müssen Sie das xml-Schema Outlook Social Connector (OSC) des Anbieters für die Erweiterbarkeit erfüllen.</span><span class="sxs-lookup"><span data-stu-id="a641d-110">To create an activity feed item, you must conform to the Outlook Social Connector (OSC) provider extensibility XML schema.</span></span> <span data-ttu-id="a641d-111">Abbildung 1 zeigt die XML-Struktur des Aktivitätsfeeds.</span><span class="sxs-lookup"><span data-stu-id="a641d-111">Figure 1 shows the activity feed XML structure.</span></span>
  
<span data-ttu-id="a641d-112">**Abbildung 1. Aktivitätsfeed-XML-Struktur**</span><span class="sxs-lookup"><span data-stu-id="a641d-112">**Figure 1. Activity feed XML structure**</span></span>

![Aktivitäts-XML-Struktur](media/odc_ol14_ta_OSC_Fig06.gif)
  
<span data-ttu-id="a641d-114">Für jedes Aktivitätsfeedelement sind die beiden wichtigsten Teile dieses Schemas **die Elemente activityDetails** und **activityTemplateContainer:**</span><span class="sxs-lookup"><span data-stu-id="a641d-114">For each activity feed item, the two most important parts of this schema are the **activityDetails** and **activityTemplateContainer** elements:</span></span> 
  
- <span data-ttu-id="a641d-115">Das **activityDetails-Element** speichert spezifische Informationen für jedes Aktivitätsfeedelement, z. B. den Namen des Aktivitätsbesitzers oder die URL für die hochgeladenen Bilder.</span><span class="sxs-lookup"><span data-stu-id="a641d-115">The **activityDetails** element stores specific information for each activity feed item, such as the activity owner's name or the URL for the pictures uploaded.</span></span> 
    
- <span data-ttu-id="a641d-116">Das **activityTemplateContainer-Element** speichert das Format oder Layout für jedes Aktivitätsfeedelement.</span><span class="sxs-lookup"><span data-stu-id="a641d-116">The **activityTemplateContainer** element stores the format or layout for each activity feed item.</span></span> <span data-ttu-id="a641d-117">Es besteht aus Vorlagen, dargestellt durch einzelne **activityTemplate-Elemente,** die für mehrere Feedelemente wiederverwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a641d-117">It consists of templates, represented by individual **activityTemplate** elements, that can be reused for multiple feed items.</span></span> 
    
<span data-ttu-id="a641d-118">Für ein einzelnes Aktivitätsfeedelement gibt das **activityTemplate-Element** die folgenden vier Informationen an:</span><span class="sxs-lookup"><span data-stu-id="a641d-118">For an individual activity feed item, the **activityTemplate** element specifies the following four pieces of information:</span></span> 
  
- <span data-ttu-id="a641d-119">**icon**– Gibt die URL für das Symbol an, das das Aktivitätsfeedelement anzeigen soll.</span><span class="sxs-lookup"><span data-stu-id="a641d-119">**icon**—Specifies the URL for the icon to display the activity feed item.</span></span>
    
- <span data-ttu-id="a641d-120">**title**– Beschreibt das Aktivitätsfeedelement.</span><span class="sxs-lookup"><span data-stu-id="a641d-120">**title**—Describes the activity feed item.</span></span>
    
- <span data-ttu-id="a641d-121">**type**– Gibt den Typ der Aktivität an, z. B. Status, Foto oder Dokumentaktualisierung.</span><span class="sxs-lookup"><span data-stu-id="a641d-121">**type**—Specifies the type of activity, such as a status, photo, or document update.</span></span>
    
- <span data-ttu-id="a641d-122">**data**– Gibt alle zusätzlichen Informationen an, die mit dem Aktivitätsfeedelement angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a641d-122">**data**—Specifies any extra information displayed with activity feed item.</span></span>
    
> [!TIP]
> <span data-ttu-id="a641d-123">Das im Aktivitätsfeed angezeigte Symbol ist immer identisch mit dem Anbietersymbol, das von der **ISocialProvider::SocialNetworkIcon-Eigenschaft zurückgegeben** wird.</span><span class="sxs-lookup"><span data-stu-id="a641d-123">The icon displayed in the activity feed is always the same as the provider icon returned by the **ISocialProvider::SocialNetworkIcon** property.</span></span> 
  
<span data-ttu-id="a641d-124">Weitere Informationen zum **activityDetails-Element,** dem **activityTemplateContainer-Element,** Vorlagentoken und Vorlagenvariablen finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="a641d-124">See the following topics for more information about the **activityDetails** element, the **activityTemplateContainer** element, template tokens, and template variables:</span></span> 
  
- [<span data-ttu-id="a641d-125">activityDetails-Element</span><span class="sxs-lookup"><span data-stu-id="a641d-125">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="a641d-126">activityTemplateContainer-Element</span><span class="sxs-lookup"><span data-stu-id="a641d-126">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="a641d-127">Vorlagenvariablen</span><span class="sxs-lookup"><span data-stu-id="a641d-127">Template Variables</span></span>](template-variables.md)
    
- [<span data-ttu-id="a641d-128">Richtlinien für die ordnungsgemäßen Anzeige von Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="a641d-128">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)
    
<span data-ttu-id="a641d-129">Ein Beispiel für aktivitätsfeed-XML finden Sie unter [Activity Feed XML Example](activity-feed-xml-example.md).</span><span class="sxs-lookup"><span data-stu-id="a641d-129">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a641d-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a641d-130">See also</span></span>

- [<span data-ttu-id="a641d-131">XML für Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="a641d-131">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="a641d-132">Outlook XML-Schema des Anbieters für sozialen Connector</span><span class="sxs-lookup"><span data-stu-id="a641d-132">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="a641d-133">Entwickeln eines Providers mit dem OSC-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="a641d-133">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

