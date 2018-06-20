---
title: ActivityTemplateContainer Element
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: Ein ActivityTemplateContainer-Element ist eine Vorlage, mit dem Sie Ihre Aktivitätsfeed Elemente formatieren und Wiederverwendung von XML, das ein Layout angibt.
ms.openlocfilehash: e744bb1bdb828003cdda7086468533b32b4bf20f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795959"
---
# <a name="activitytemplatecontainer-element"></a><span data-ttu-id="57d1a-103">ActivityTemplateContainer Element</span><span class="sxs-lookup"><span data-stu-id="57d1a-103">activityTemplateContainer Element</span></span>

<span data-ttu-id="57d1a-104">Ein **ActivityTemplateContainer** -Element ist eine Vorlage, mit dem Sie Ihre Aktivitätsfeed Elemente formatieren und Wiederverwendung von XML, das ein Layout angibt.</span><span class="sxs-lookup"><span data-stu-id="57d1a-104">An **activityTemplateContainer** element is a template that allows you to format your activity feed items and reuse XML that specifies a layout.</span></span> <span data-ttu-id="57d1a-105">Verwenden Sie IDs (**ApplicationID** und **TemplateID**), der ein feed-Element (**ActivityDetails**) zu einer Vorlage (**ActivityTemplateContainer**) entspricht.</span><span class="sxs-lookup"><span data-stu-id="57d1a-105">Use IDs (**applicationID** and **templateID**) to match a feed item (**activityDetails**) to a template (**activityTemplateContainer**).</span></span> <span data-ttu-id="57d1a-106">Speichern Sie die Layoutdaten als Teil des **ActivityTemplate** -Elements.</span><span class="sxs-lookup"><span data-stu-id="57d1a-106">Store the layout data as part of the **activityTemplate** element.</span></span> <span data-ttu-id="57d1a-107">Verwenden von Vorlagenvariablen Daten verweisen möchten, die von den einzelnen Aktivitätsfeed-Element abgerufen wird, als Platzhalter für Informationen wie Personen, Links und Text.</span><span class="sxs-lookup"><span data-stu-id="57d1a-107">To reference data that is pulled from the individual activity feed item, use template variables as placeholders for information such as people, links, and text.</span></span> 
  
<span data-ttu-id="57d1a-108">In der folgenden Tabelle werden die drei Elemente, die das **ActivityTemplateContainer** -Element muss beschrieben.</span><span class="sxs-lookup"><span data-stu-id="57d1a-108">The following table describes the three elements that the **activityTemplateContainer** element requires.</span></span> 
  
|<span data-ttu-id="57d1a-109">**Element**</span><span class="sxs-lookup"><span data-stu-id="57d1a-109">**Element**</span></span>|<span data-ttu-id="57d1a-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="57d1a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="57d1a-111">**applicationID**</span><span class="sxs-lookup"><span data-stu-id="57d1a-111">**applicationID**</span></span> <br/> |<span data-ttu-id="57d1a-112">Einer der beiden eindeutigen IDs, Abgleich mit dem feed Element mit der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="57d1a-112">One of two unique IDs that are used to match the feed item with its template.</span></span> <span data-ttu-id="57d1a-113">Wenn Sie mehrere Anwendungen oder andere Gruppen verfügen, kann dies als Organisator einer Vorlage der ersten Ebene verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="57d1a-113">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="57d1a-114">**templateID**</span><span class="sxs-lookup"><span data-stu-id="57d1a-114">**templateID**</span></span> <br/> |<span data-ttu-id="57d1a-115">Die zweite eindeutige ID, die entsprechend das feed Element mit der Vorlage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="57d1a-115">The second unique ID that is used to match the feed item with its template.</span></span> <span data-ttu-id="57d1a-116">Dies kann als Organisator einer L2-Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="57d1a-116">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="57d1a-117">**activityTemplate**</span><span class="sxs-lookup"><span data-stu-id="57d1a-117">**activityTemplate**</span></span> <br/> |<span data-ttu-id="57d1a-118">Das Layout der Vorlage (**Symbol**, **Titel**und **Daten** Elemente) und den Typ der Aktivität (**Type** -Element).</span><span class="sxs-lookup"><span data-stu-id="57d1a-118">The layout of the template (**icon**, **title**, and **data** elements), and the type of activity (**type** element).</span></span>  <br/> |
   
<span data-ttu-id="57d1a-119">In der folgenden Tabelle werden die untergeordneten Elemente des **ActivityTemplate**, die beschreiben, die das Layout und den Typ einer Vorlage beschrieben.</span><span class="sxs-lookup"><span data-stu-id="57d1a-119">The following table describes the child elements of **activityTemplate**, which describe the layout and the type of a template.</span></span>
  
|<span data-ttu-id="57d1a-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="57d1a-120">**Element**</span></span>|<span data-ttu-id="57d1a-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="57d1a-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="57d1a-122">**icon**</span><span class="sxs-lookup"><span data-stu-id="57d1a-122">**icon**</span></span> <br/> |<span data-ttu-id="57d1a-123">Ein Link-Token, die die URL für das Symbol für den feed Artikel verweist.</span><span class="sxs-lookup"><span data-stu-id="57d1a-123">A link token, which references the URL for the icon for that feed item.</span></span>  <br/> |
|<span data-ttu-id="57d1a-124">**title**</span><span class="sxs-lookup"><span data-stu-id="57d1a-124">**title**</span></span> <br/> |<span data-ttu-id="57d1a-125">Die erforderlichen Informationen für den feed Artikel.</span><span class="sxs-lookup"><span data-stu-id="57d1a-125">The required information for the feed item.</span></span>  <br/> |
|<span data-ttu-id="57d1a-126">**type**</span><span class="sxs-lookup"><span data-stu-id="57d1a-126">**type**</span></span> <br/> |<span data-ttu-id="57d1a-127">Der Typ der Aktivität, wie etwa die Aktualisierung von Status, Foto oder Dokument.</span><span class="sxs-lookup"><span data-stu-id="57d1a-127">The type of activity, such as an update of status, photo, or document.</span></span>  <br/> |
|<span data-ttu-id="57d1a-128">**data**</span><span class="sxs-lookup"><span data-stu-id="57d1a-128">**data**</span></span> <br/> |<span data-ttu-id="57d1a-129">Zusätzliche Informationen für den feed Artikel, wie Bilder, Text oder Links.</span><span class="sxs-lookup"><span data-stu-id="57d1a-129">Any additional information for the feed item, such as pictures, text, or links.</span></span>  <br/> |
   
<span data-ttu-id="57d1a-130">Ein Beispiel der Aktivität XML-feed, finden Sie unter [Aktivität Feed XML-Beispiel](activity-feed-xml-example.md)</span><span class="sxs-lookup"><span data-stu-id="57d1a-130">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="57d1a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57d1a-131">See also</span></span>

- [<span data-ttu-id="57d1a-132">Übersicht über XML-Code für eine Aktivität Element-Feed</span><span class="sxs-lookup"><span data-stu-id="57d1a-132">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="57d1a-133">ActivityDetails Element</span><span class="sxs-lookup"><span data-stu-id="57d1a-133">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="57d1a-134">Vorlagenvariablen</span><span class="sxs-lookup"><span data-stu-id="57d1a-134">Template Variables</span></span>](template-variables.md)  
- [<span data-ttu-id="57d1a-135">Richtlinien für das Aktivitäten ordnungsgemäß anzeigen</span><span class="sxs-lookup"><span data-stu-id="57d1a-135">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="57d1a-136">XML-Code für Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="57d1a-136">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="57d1a-137">Outlook Connector für soziale Netzwerke Anbieter XML-Schema</span><span class="sxs-lookup"><span data-stu-id="57d1a-137">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="57d1a-138">Entwickeln eines Providers mit dem OSC-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="57d1a-138">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

