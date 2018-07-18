---
title: Überblick über XML für eine Aktivitätsfeedelement
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: 'Ein Aktivitätsfeed umfasst eine oder mehrere Aktivitäten, die bei einem sozialen Netzwerk. Jedes Aktivitätsfeed wird durch ein ActivityFeed-Element dargestellt, und wird durch diese drei Angaben Merkmale auf:'
ms.openlocfilehash: 318875aeb6312a3710654d129f3f48139ff7ef12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796095"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a><span data-ttu-id="8ff3d-104">Überblick über XML für eine Aktivitätsfeedelement</span><span class="sxs-lookup"><span data-stu-id="8ff3d-104">Overview of XML for an activity feed item</span></span>

<span data-ttu-id="8ff3d-105">Ein Aktivitätsfeed umfasst eine oder mehrere Aktivitäten, die bei einem sozialen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="8ff3d-105">An activity feed consists of one or more activities occurring on a social network.</span></span> <span data-ttu-id="8ff3d-106">Jedes Aktivitätsfeed wird durch ein **ActivityFeed** -Element dargestellt, und wird durch diese drei Angaben Merkmale auf:</span><span class="sxs-lookup"><span data-stu-id="8ff3d-106">Each activity feed is represented by an **activityFeed** element, and is characterized by these three pieces of information:</span></span> 
  
- <span data-ttu-id="8ff3d-107">**Netzwerk**– Name der dem sozialen Netzwerk, von dem die Aktivitäten stammt.</span><span class="sxs-lookup"><span data-stu-id="8ff3d-107">**network**—Name of the social network from which the activities originated.</span></span>
    
- <span data-ttu-id="8ff3d-108">**Aktivitäten**– Container für Aktivitäten auf das angemeldete Konto des Benutzers für das soziale Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="8ff3d-108">**activities**—Container for activities happening on the logged on user's account on that social network.</span></span>
    
- <span data-ttu-id="8ff3d-109">**Vorlagen**– Container für Vorlagen, die zum Anzeigen des entsprechenden Aktivitätselements in **Aktivitäten**verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8ff3d-109">**templates**—Container for templates that are used to display the corresponding activity item in **activities**.</span></span>
    
<span data-ttu-id="8ff3d-110">Um eine Aktivität Element-feed zu erstellen, müssen Sie das Outlook Social Connector (OSC) Anbieter Erweiterbarkeit XML-Schema entsprechen.</span><span class="sxs-lookup"><span data-stu-id="8ff3d-110">To create an activity feed item, you must conform to the Outlook Social Connector (OSC) provider extensibility XML schema.</span></span> <span data-ttu-id="8ff3d-111">Abbildung 1 zeigt, dass die XML-Struktur der Aktivitätsfeeds.</span><span class="sxs-lookup"><span data-stu-id="8ff3d-111">Figure 1 shows the activity feed XML structure.</span></span>
  
<span data-ttu-id="8ff3d-112">**Abbildung 1. XML-Struktur für Aktivitätsfeeds**</span><span class="sxs-lookup"><span data-stu-id="8ff3d-112">**Figure 1. Activity feed XML structure**</span></span>

![Aktivitäts-XML-Struktur](media/odc_ol14_ta_OSC_Fig06.gif)
  
<span data-ttu-id="8ff3d-114">Für jede Aktivität Element-feed sind die beiden wichtigsten Teile dieses Schemas die **ActivityDetails** und **ActivityTemplateContainer** Elemente:</span><span class="sxs-lookup"><span data-stu-id="8ff3d-114">For each activity feed item, the two most important parts of this schema are the **activityDetails** and **activityTemplateContainer** elements:</span></span> 
  
- <span data-ttu-id="8ff3d-115">Das Element **ActivityDetails** speichert spezifische Informationen für jede Aktivitätsfeed-Element, wie der Name des Besitzers der Aktivität oder die URL für die Bilder hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="8ff3d-115">The **activityDetails** element stores specific information for each activity feed item, such as the activity owner's name or the URL for the pictures uploaded.</span></span> 
    
- <span data-ttu-id="8ff3d-116">Das Element **ActivityTemplateContainer** speichert das Format oder Layout für jede Aktivität feed Element.</span><span class="sxs-lookup"><span data-stu-id="8ff3d-116">The **activityTemplateContainer** element stores the format or layout for each activity feed item.</span></span> <span data-ttu-id="8ff3d-117">Es besteht aus Vorlagen, dargestellt durch einzelne **ActivityTemplate** -Elemente, die mehrere Elemente feed wiederverwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="8ff3d-117">It consists of templates, represented by individual **activityTemplate** elements, that can be reused for multiple feed items.</span></span> 
    
<span data-ttu-id="8ff3d-118">Das **ActivityTemplate** -Element für ein einzelnes Element der Aktivitätsfeed gibt an, dass die folgenden vier Arten von Informationen:</span><span class="sxs-lookup"><span data-stu-id="8ff3d-118">For an individual activity feed item, the **activityTemplate** element specifies the following four pieces of information:</span></span> 
  
- <span data-ttu-id="8ff3d-119">**Symbol**– gibt die URL für das Symbol zum Anzeigen der Aktivitätsfeeds feed Element.</span><span class="sxs-lookup"><span data-stu-id="8ff3d-119">**icon**—Specifies the URL for the icon to display the activity feed item.</span></span>
    
- <span data-ttu-id="8ff3d-120">**Titel**– beschreibt die Aktivitätsfeed item.</span><span class="sxs-lookup"><span data-stu-id="8ff3d-120">**title**—Describes the activity feed item.</span></span>
    
- <span data-ttu-id="8ff3d-121">**Typ**– gibt den Typ der Aktivität, wie ein Status, Foto oder Aktualisierung des Dokuments an.</span><span class="sxs-lookup"><span data-stu-id="8ff3d-121">**type**—Specifies the type of activity, such as a status, photo, or document update.</span></span>
    
- <span data-ttu-id="8ff3d-122">**Daten**– gibt zusätzliche Informationen mit Aktivitätsfeed Element angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8ff3d-122">**data**—Specifies any extra information displayed with activity feed item.</span></span>
    
> [!TIP]
> <span data-ttu-id="8ff3d-123">Der Aktivitätsfeed angezeigte Symbol entspricht immer das Symbol für Anbieter von der **ISocialProvider::SocialNetworkIcon** -Eigenschaft zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8ff3d-123">The icon displayed in the activity feed is always the same as the provider icon returned by the **ISocialProvider::SocialNetworkIcon** property.</span></span> 
  
<span data-ttu-id="8ff3d-124">Finden Sie unter den folgenden Themen Weitere Informationen zu **ActivityDetails** -Element, das **ActivityTemplateContainer** -Element, Vorlage Token und Vorlagenvariablen:</span><span class="sxs-lookup"><span data-stu-id="8ff3d-124">See the following topics for more information about the **activityDetails** element, the **activityTemplateContainer** element, template tokens, and template variables:</span></span> 
  
- [<span data-ttu-id="8ff3d-125">ActivityDetails Element</span><span class="sxs-lookup"><span data-stu-id="8ff3d-125">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="8ff3d-126">ActivityTemplateContainer Element</span><span class="sxs-lookup"><span data-stu-id="8ff3d-126">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="8ff3d-127">Vorlagenvariablen</span><span class="sxs-lookup"><span data-stu-id="8ff3d-127">Template Variables</span></span>](template-variables.md)
    
- [<span data-ttu-id="8ff3d-128">Richtlinien für das Aktivitäten ordnungsgemäß anzeigen</span><span class="sxs-lookup"><span data-stu-id="8ff3d-128">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)
    
<span data-ttu-id="8ff3d-129">Ein Beispiel der Aktivität XML-feed, finden Sie unter [Aktivität Feed XML-Beispiel](activity-feed-xml-example.md).</span><span class="sxs-lookup"><span data-stu-id="8ff3d-129">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8ff3d-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ff3d-130">See also</span></span>

- [<span data-ttu-id="8ff3d-131">XML-Code für Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="8ff3d-131">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="8ff3d-132">Outlook Connector für soziale Netzwerke Anbieter XML-Schema</span><span class="sxs-lookup"><span data-stu-id="8ff3d-132">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="8ff3d-133">Entwickeln eines Providers mit dem OSC-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="8ff3d-133">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

