---
title: activityTemplateContainer-Element
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: Ein activityTemplateContainer-Element ist eine Vorlage, mit der Sie Ihre Aktivitätsfeed-Elemente formatieren und XML wieder verwenden können, das ein Layout angibt.
ms.openlocfilehash: c2540b1d871e440e8f8f343a1788194c32d7dcc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413717"
---
# <a name="activitytemplatecontainer-element"></a><span data-ttu-id="95bac-103">activityTemplateContainer-Element</span><span class="sxs-lookup"><span data-stu-id="95bac-103">activityTemplateContainer Element</span></span>

<span data-ttu-id="95bac-104">Ein **activityTemplateContainer** -Element ist eine Vorlage, mit der Sie Ihre Aktivitätsfeed-Elemente formatieren und XML wieder verwenden können, das ein Layout angibt.</span><span class="sxs-lookup"><span data-stu-id="95bac-104">An **activityTemplateContainer** element is a template that allows you to format your activity feed items and reuse XML that specifies a layout.</span></span> <span data-ttu-id="95bac-105">Verwenden Sie IDs (**applicationID** und **Template**-ID), um ein Feedelement (**ActivityDetails**) einer Vorlage (**activityTemplateContainer**) zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="95bac-105">Use IDs (**applicationID** and **templateID**) to match a feed item (**activityDetails**) to a template (**activityTemplateContainer**).</span></span> <span data-ttu-id="95bac-106">Speichern Sie die Layoutdaten als Teil des **activityTemplate** -Elements.</span><span class="sxs-lookup"><span data-stu-id="95bac-106">Store the layout data as part of the **activityTemplate** element.</span></span> <span data-ttu-id="95bac-107">Wenn Sie auf Daten verweisen möchten, die aus dem einzelnen Aktivitäts Feedelement abgerufen werden, verwenden Sie Vorlagenvariablen als Platzhalter für Informationen wie Personen, Links und Text.</span><span class="sxs-lookup"><span data-stu-id="95bac-107">To reference data that is pulled from the individual activity feed item, use template variables as placeholders for information such as people, links, and text.</span></span> 
  
<span data-ttu-id="95bac-108">In der folgenden Tabelle werden die drei Elemente beschrieben, die das **activityTemplateContainer** -Element benötigt.</span><span class="sxs-lookup"><span data-stu-id="95bac-108">The following table describes the three elements that the **activityTemplateContainer** element requires.</span></span> 
  
|<span data-ttu-id="95bac-109">**Element**</span><span class="sxs-lookup"><span data-stu-id="95bac-109">**Element**</span></span>|<span data-ttu-id="95bac-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="95bac-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="95bac-111">**applicationID**</span><span class="sxs-lookup"><span data-stu-id="95bac-111">**applicationID**</span></span> <br/> |<span data-ttu-id="95bac-112">Eine von zwei eindeutigen IDs, die verwendet werden, um das Feedelement mit seiner Vorlage abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="95bac-112">One of two unique IDs that are used to match the feed item with its template.</span></span> <span data-ttu-id="95bac-113">Wenn Sie mehrere Anwendungen oder andere Gruppierungen haben, kann dies als eine Vorlage Organizer der ersten Ebene verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95bac-113">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="95bac-114">**templateID**</span><span class="sxs-lookup"><span data-stu-id="95bac-114">**templateID**</span></span> <br/> |<span data-ttu-id="95bac-115">Die zweite eindeutige ID, die verwendet wird, um das Feedelement mit seiner Vorlage abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="95bac-115">The second unique ID that is used to match the feed item with its template.</span></span> <span data-ttu-id="95bac-116">Dieser kann als Organisator einer Vorlage für die zweite Ebene verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95bac-116">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="95bac-117">**activityTemplate**</span><span class="sxs-lookup"><span data-stu-id="95bac-117">**activityTemplate**</span></span> <br/> |<span data-ttu-id="95bac-118">Das Layout der Vorlage (**Symbol**-, **Titel**-und **Daten** Elemente) und der Aktivitätstyp (**Type** -Element).</span><span class="sxs-lookup"><span data-stu-id="95bac-118">The layout of the template (**icon**, **title**, and **data** elements), and the type of activity (**type** element).</span></span>  <br/> |
   
<span data-ttu-id="95bac-119">In der folgenden Tabelle werden die untergeordneten Elemente von **activityTemplate**beschrieben, die das Layout und den Typ einer Vorlage beschreiben.</span><span class="sxs-lookup"><span data-stu-id="95bac-119">The following table describes the child elements of **activityTemplate**, which describe the layout and the type of a template.</span></span>
  
|<span data-ttu-id="95bac-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="95bac-120">**Element**</span></span>|<span data-ttu-id="95bac-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="95bac-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="95bac-122">**icon**</span><span class="sxs-lookup"><span data-stu-id="95bac-122">**icon**</span></span> <br/> |<span data-ttu-id="95bac-123">Ein Link-Token, das die URL für das Symbol für dieses Feed-Element referenziert.</span><span class="sxs-lookup"><span data-stu-id="95bac-123">A link token, which references the URL for the icon for that feed item.</span></span>  <br/> |
|<span data-ttu-id="95bac-124">**title**</span><span class="sxs-lookup"><span data-stu-id="95bac-124">**title**</span></span> <br/> |<span data-ttu-id="95bac-125">Die erforderlichen Informationen für das Feedelement.</span><span class="sxs-lookup"><span data-stu-id="95bac-125">The required information for the feed item.</span></span>  <br/> |
|<span data-ttu-id="95bac-126">**Typ**</span><span class="sxs-lookup"><span data-stu-id="95bac-126">**type**</span></span> <br/> |<span data-ttu-id="95bac-127">Der Aktivitätstyp, beispielsweise eine Aktualisierung des Status, des Fotos oder Dokuments.</span><span class="sxs-lookup"><span data-stu-id="95bac-127">The type of activity, such as an update of status, photo, or document.</span></span>  <br/> |
|<span data-ttu-id="95bac-128">**data**</span><span class="sxs-lookup"><span data-stu-id="95bac-128">**data**</span></span> <br/> |<span data-ttu-id="95bac-129">Alle zusätzlichen Informationen für das Feed-Element, wie Bilder, Text oder Links.</span><span class="sxs-lookup"><span data-stu-id="95bac-129">Any additional information for the feed item, such as pictures, text, or links.</span></span>  <br/> |
   
<span data-ttu-id="95bac-130">Ein Beispiel für Aktivitäts-Feed-XML finden Sie unter [Aktivitätsfeed-XML-Beispiel](activity-feed-xml-example.md)</span><span class="sxs-lookup"><span data-stu-id="95bac-130">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="95bac-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95bac-131">See also</span></span>

- [<span data-ttu-id="95bac-132">Übersicht über XML für ein Aktivitäts Feed-Element</span><span class="sxs-lookup"><span data-stu-id="95bac-132">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="95bac-133">activityDetails-Element</span><span class="sxs-lookup"><span data-stu-id="95bac-133">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="95bac-134">Vorlagenvariablen</span><span class="sxs-lookup"><span data-stu-id="95bac-134">Template Variables</span></span>](template-variables.md)  
- [<span data-ttu-id="95bac-135">Richtlinien für die OrdnungsGemäße Anzeige von Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="95bac-135">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="95bac-136">XML für Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="95bac-136">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="95bac-137">XML-Schema des Anbieters für soziale Netzwerke in Outlook</span><span class="sxs-lookup"><span data-stu-id="95bac-137">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="95bac-138">Entwickeln eines Providers mit dem OSC-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="95bac-138">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

