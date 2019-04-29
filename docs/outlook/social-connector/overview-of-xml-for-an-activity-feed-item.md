---
title: Überblick über XML für ein Aktivitätsfeedelement
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: 'Ein Aktivitätsfeed besteht aus einer oder mehreren Aktivitäten, die in einem sozialen Netzwerk auftreten. Jeder Aktivitätsfeed wird durch ein activityFeed-Element dargestellt und zeichnet sich durch diese drei Informationselemente aus:'
ms.openlocfilehash: 971c54cf69a65bebbe4fd04e8608e88b89145bb4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439947"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a><span data-ttu-id="ff9ba-104">Überblick über XML für ein Aktivitätsfeedelement</span><span class="sxs-lookup"><span data-stu-id="ff9ba-104">Overview of XML for an activity feed item</span></span>

<span data-ttu-id="ff9ba-105">Ein Aktivitätsfeed besteht aus einer oder mehreren Aktivitäten, die in einem sozialen Netzwerk auftreten.</span><span class="sxs-lookup"><span data-stu-id="ff9ba-105">An activity feed consists of one or more activities occurring on a social network.</span></span> <span data-ttu-id="ff9ba-106">Jeder Aktivitätsfeed wird durch ein **activityFeed** -Element dargestellt und zeichnet sich durch diese drei Informationselemente aus:</span><span class="sxs-lookup"><span data-stu-id="ff9ba-106">Each activity feed is represented by an **activityFeed** element, and is characterized by these three pieces of information:</span></span> 
  
- <span data-ttu-id="ff9ba-107">**Netzwerk**– Name des sozialen Netzwerks, von dem die Aktivitäten stammten.</span><span class="sxs-lookup"><span data-stu-id="ff9ba-107">**network**—Name of the social network from which the activities originated.</span></span>
    
- <span data-ttu-id="ff9ba-108">**Aktivitäten**– Container für Aktivitäten, die im Konto des angemeldeten Benutzers in diesem sozialen Netzwerk stattfindet.</span><span class="sxs-lookup"><span data-stu-id="ff9ba-108">**activities**—Container for activities happening on the logged on user's account on that social network.</span></span>
    
- <span data-ttu-id="ff9ba-109">**Vorlagen**– Container für Vorlagen, die verwendet werden, um das entsprechende Aktivitätselement in **Aktivitäten**anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ff9ba-109">**templates**—Container for templates that are used to display the corresponding activity item in **activities**.</span></span>
    
<span data-ttu-id="ff9ba-110">Zum Erstellen eines Aktivitätsfeed-Elements müssen Sie dem XML-Schema für die Erweiterbarkeit von Outlook Social Connector (OSC) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ff9ba-110">To create an activity feed item, you must conform to the Outlook Social Connector (OSC) provider extensibility XML schema.</span></span> <span data-ttu-id="ff9ba-111">Abbildung 1 zeigt die XML-Struktur des Aktivitätsfeeds.</span><span class="sxs-lookup"><span data-stu-id="ff9ba-111">Figure 1 shows the activity feed XML structure.</span></span>
  
<span data-ttu-id="ff9ba-112">**Abbildung 1. XML-Struktur des Aktivitätsfeeds**</span><span class="sxs-lookup"><span data-stu-id="ff9ba-112">**Figure 1. Activity feed XML structure**</span></span>

![Aktivitäts-XML-Struktur](media/odc_ol14_ta_OSC_Fig06.gif)
  
<span data-ttu-id="ff9ba-114">Für jedes Aktivitätsfeed-Element sind die beiden wichtigsten Teile dieses Schemas die Elemente **activityDetails** und **activityTemplateContainer** :</span><span class="sxs-lookup"><span data-stu-id="ff9ba-114">For each activity feed item, the two most important parts of this schema are the **activityDetails** and **activityTemplateContainer** elements:</span></span> 
  
- <span data-ttu-id="ff9ba-115">Das **activityDetails** -Element speichert bestimmte Informationen für jedes Aktivitätsfeed-Element, beispielsweise den Namen des Aktivitäts Besitzers oder die URL für die hochgeladenen Bilder.</span><span class="sxs-lookup"><span data-stu-id="ff9ba-115">The **activityDetails** element stores specific information for each activity feed item, such as the activity owner's name or the URL for the pictures uploaded.</span></span> 
    
- <span data-ttu-id="ff9ba-116">Das **activityTemplateContainer** -Element speichert das Format oder Layout für jedes Aktivitätsfeed-Element.</span><span class="sxs-lookup"><span data-stu-id="ff9ba-116">The **activityTemplateContainer** element stores the format or layout for each activity feed item.</span></span> <span data-ttu-id="ff9ba-117">Sie besteht aus Vorlagen, dargestellt durch einzelne **activityTemplate** -Elemente, die für mehrere Feed-Elemente wieder verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="ff9ba-117">It consists of templates, represented by individual **activityTemplate** elements, that can be reused for multiple feed items.</span></span> 
    
<span data-ttu-id="ff9ba-118">Bei einem einzelnen Aktivitätsfeed-Element gibt das **activityTemplate** -Element die folgenden vier Informationen an:</span><span class="sxs-lookup"><span data-stu-id="ff9ba-118">For an individual activity feed item, the **activityTemplate** element specifies the following four pieces of information:</span></span> 
  
- <span data-ttu-id="ff9ba-119">**Symbol**– gibt die URL für das Symbol an, um das Aktivitäts Feedelement anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ff9ba-119">**icon**—Specifies the URL for the icon to display the activity feed item.</span></span>
    
- <span data-ttu-id="ff9ba-120">**Title**– Beschreibung des Aktivitätsfeed-Elements.</span><span class="sxs-lookup"><span data-stu-id="ff9ba-120">**title**—Describes the activity feed item.</span></span>
    
- <span data-ttu-id="ff9ba-121">**Typ**– gibt den Aktivitätstyp an, beispielsweise ein Status-, Foto-oder Dokument Update.</span><span class="sxs-lookup"><span data-stu-id="ff9ba-121">**type**—Specifies the type of activity, such as a status, photo, or document update.</span></span>
    
- <span data-ttu-id="ff9ba-122">**Data**– gibt alle zusätzlichen Informationen an, die mit Activity Feed Item angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ff9ba-122">**data**—Specifies any extra information displayed with activity feed item.</span></span>
    
> [!TIP]
> <span data-ttu-id="ff9ba-123">Das im Aktivitätsfeed angezeigte Symbol ist immer identisch mit dem Anbieter Symbol, das von der **ISocialProvider:: SocialNetworkIcon** -Eigenschaft zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ff9ba-123">The icon displayed in the activity feed is always the same as the provider icon returned by the **ISocialProvider::SocialNetworkIcon** property.</span></span> 
  
<span data-ttu-id="ff9ba-124">In den folgenden Themen finden Sie weitere Informationen zum **activityDetails** -Element, dem **activityTemplateContainer** -Element, Vorlagen Token und Vorlagenvariablen:</span><span class="sxs-lookup"><span data-stu-id="ff9ba-124">See the following topics for more information about the **activityDetails** element, the **activityTemplateContainer** element, template tokens, and template variables:</span></span> 
  
- [<span data-ttu-id="ff9ba-125">activityDetails-Element</span><span class="sxs-lookup"><span data-stu-id="ff9ba-125">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="ff9ba-126">activityTemplateContainer-Element</span><span class="sxs-lookup"><span data-stu-id="ff9ba-126">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="ff9ba-127">Vorlagenvariablen</span><span class="sxs-lookup"><span data-stu-id="ff9ba-127">Template Variables</span></span>](template-variables.md)
    
- [<span data-ttu-id="ff9ba-128">Richtlinien für die OrdnungsGemäße Anzeige von Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="ff9ba-128">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)
    
<span data-ttu-id="ff9ba-129">Ein Beispiel für Aktivitäts-Feed-XML finden Sie unter [Activity Feed XML example](activity-feed-xml-example.md).</span><span class="sxs-lookup"><span data-stu-id="ff9ba-129">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ff9ba-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff9ba-130">See also</span></span>

- [<span data-ttu-id="ff9ba-131">XML für Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="ff9ba-131">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="ff9ba-132">XML-Schema des Anbieters für soziale Netzwerke in Outlook</span><span class="sxs-lookup"><span data-stu-id="ff9ba-132">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="ff9ba-133">Entwickeln eines Providers mit dem OSC-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="ff9ba-133">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

