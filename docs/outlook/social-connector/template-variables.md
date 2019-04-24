---
title: Vorlagenvariablen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6f8f6af2-c7fa-4135-9532-7af5fc643b0d
description: Instanzen von Vorlagenvariablen (dargestellt durch ein templateVariable-Element) geben die Daten eines Aktivitätsfeed-Elements in einer Aktivitätsvorlage an.
ms.openlocfilehash: 9b37665488f0f1e2bd205fb7d4a5d2201697d7c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329176"
---
# <a name="template-variables"></a><span data-ttu-id="2da05-103">Vorlagenvariablen</span><span class="sxs-lookup"><span data-stu-id="2da05-103">Template variables</span></span>

<span data-ttu-id="2da05-104">Instanzen von Vorlagenvariablen (dargestellt durch ein **templateVariable** -Element) geben die Daten eines Aktivitätsfeed-Elements in einer Aktivitätsvorlage an.</span><span class="sxs-lookup"><span data-stu-id="2da05-104">Instances of template variables (represented by a **templateVariable** element) specify the data of an activity feed item in an activity template.</span></span> 
  
<span data-ttu-id="2da05-105">Ein Beispiel für Aktivitäts-Feed-XML finden Sie unter [Activity Feed XML example](activity-feed-xml-example.md).</span><span class="sxs-lookup"><span data-stu-id="2da05-105">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>

<span data-ttu-id="2da05-106">In der folgenden Tabelle sind die Typen der unterstützten Vorlagenvariablen aufgeführt, die jeweils durch den entsprechenden XML-Enumerationswert dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="2da05-106">The following table shows the types of supported template variables, each represented by the corresponding XML enumeration value.</span></span>
  
|<span data-ttu-id="2da05-107">**Typ der Vorlagenvariablen**</span><span class="sxs-lookup"><span data-stu-id="2da05-107">**Type of template variable**</span></span>|<span data-ttu-id="2da05-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2da05-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2da05-109">**entityVariable**</span><span class="sxs-lookup"><span data-stu-id="2da05-109">**entityVariable**</span></span> <br/> |<span data-ttu-id="2da05-110">Eine Person, eine Gruppe oder ein Ding.</span><span class="sxs-lookup"><span data-stu-id="2da05-110">A person, group, or thing.</span></span>  <br/> |
|<span data-ttu-id="2da05-111">**linkVariable**</span><span class="sxs-lookup"><span data-stu-id="2da05-111">**linkVariable**</span></span> <br/> |<span data-ttu-id="2da05-112">Link.</span><span class="sxs-lookup"><span data-stu-id="2da05-112">A link.</span></span>  <br/> |
|<span data-ttu-id="2da05-113">**listVariable**</span><span class="sxs-lookup"><span data-stu-id="2da05-113">**listVariable**</span></span> <br/> |<span data-ttu-id="2da05-114">Eine Gruppe von Objekten.</span><span class="sxs-lookup"><span data-stu-id="2da05-114">A group of objects.</span></span>  <br/> |
|<span data-ttu-id="2da05-115">**pictureVariable**</span><span class="sxs-lookup"><span data-stu-id="2da05-115">**pictureVariable**</span></span> <br/> |<span data-ttu-id="2da05-116">Ein Bild.</span><span class="sxs-lookup"><span data-stu-id="2da05-116">A picture.</span></span>  <br/> |
|<span data-ttu-id="2da05-117">**publisherVariable**</span><span class="sxs-lookup"><span data-stu-id="2da05-117">**publisherVariable**</span></span> <br/> |<span data-ttu-id="2da05-118">Der Herausgeber des Aktivitätsfeed-Elements.</span><span class="sxs-lookup"><span data-stu-id="2da05-118">The publisher of the activity feed item.</span></span>  <br/> |
|<span data-ttu-id="2da05-119">**Textvariable**</span><span class="sxs-lookup"><span data-stu-id="2da05-119">**textVariable**</span></span> <br/> |<span data-ttu-id="2da05-120">Ein TextBlock.</span><span class="sxs-lookup"><span data-stu-id="2da05-120">A block of text.</span></span>  <br/> |
   
<span data-ttu-id="2da05-121">Jeder Typ von Template-Variablen verfügt über erforderliche Elemente, um die Daten zu dieser Variablen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2da05-121">Each type of template variable has required elements to specify the data about that variable.</span></span> <span data-ttu-id="2da05-122">Vorlagenvariablen werden wie folgt festgelegt:</span><span class="sxs-lookup"><span data-stu-id="2da05-122">Template variables are specified as follows:</span></span>
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a><span data-ttu-id="2da05-123">Listenvorlagen Variable</span><span class="sxs-lookup"><span data-stu-id="2da05-123">List template variable</span></span>

<span data-ttu-id="2da05-124">Sie können Vorlagenvariablen, die in einer Liste enthalten sind (durch die Elemente **listVariable** und **ListItems** getrennt) wie folgt angeben:</span><span class="sxs-lookup"><span data-stu-id="2da05-124">You can specify template variables that are contained within a list (delimited by the **listVariable** and **listItems** elements) as follows:</span></span> 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
<span data-ttu-id="2da05-125">Eine Vorlagenvariable des **listVariable** -Typs ist ein Container für Objekte.</span><span class="sxs-lookup"><span data-stu-id="2da05-125">A template variable of the **listVariable** type is a container for objects.</span></span> <span data-ttu-id="2da05-126">Sie kann durch trennzeichengetrennte Elemente (vom Typ **linkVariable** oder Textvariable) oder Bilder (vom Typ **pictureVariable** ) enthalten. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="2da05-126">It can contain comma-delimited items (of the **linkVariable** or **textVariable** type) or pictures (of the **pictureVariable** type).</span></span> <span data-ttu-id="2da05-127">Listen können bis zu fünf Link Elemente, fünf Textelemente oder fünf Bilder enthalten.</span><span class="sxs-lookup"><span data-stu-id="2da05-127">Lists can contain up to five link items, five text items, or five pictures.</span></span> 
  
<span data-ttu-id="2da05-128">Der Outlook Connector für soziale Netzwerke (OSC) lokalisiert Verknüpfungs-oder Textlisten Elemente entsprechend dem Windows-Systemgebietsschema.</span><span class="sxs-lookup"><span data-stu-id="2da05-128">The Outlook Social Connector (OSC) localizes link or text list items according to the Windows system locale.</span></span>
  
<span data-ttu-id="2da05-129">Um Bilder in einem Aktivitätsfeed-Element richtig zu analysieren und anzuzeigen, müssen Sie Bilder in eine Liste aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="2da05-129">To correctly parse and display pictures in an activity feed item, you must include pictures in a list.</span></span> <span data-ttu-id="2da05-130">Alle Bilder werden um 52 Pixel hoch geändert.</span><span class="sxs-lookup"><span data-stu-id="2da05-130">All pictures are resized to be 52 pixels high.</span></span> <span data-ttu-id="2da05-131">Die Größe des Bilds wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="2da05-131">The width of the picture is not resized.</span></span>
  
## <a name="template-variable-elements"></a><span data-ttu-id="2da05-132">Vorlagenvariable Elemente</span><span class="sxs-lookup"><span data-stu-id="2da05-132">Template variable elements</span></span>

<span data-ttu-id="2da05-133">In diesem Abschnitt werden die erforderlichen und optionalen Elemente erläutert, die für die einzelnen Vorlagenvariablen Typen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="2da05-133">This section covers the required and optional elements supported for each type of template variable.</span></span>
  
### <a name="entityvariable"></a><span data-ttu-id="2da05-134">entityVariable</span><span class="sxs-lookup"><span data-stu-id="2da05-134">entityVariable</span></span>

|<span data-ttu-id="2da05-135">**Element**</span><span class="sxs-lookup"><span data-stu-id="2da05-135">**Element**</span></span>|<span data-ttu-id="2da05-136">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2da05-136">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2da05-137">**Name**</span><span class="sxs-lookup"><span data-stu-id="2da05-137">**name**</span></span> <br/> |<span data-ttu-id="2da05-138">Der Name der Variablen.</span><span class="sxs-lookup"><span data-stu-id="2da05-138">The name of the variable.</span></span> <span data-ttu-id="2da05-139">Erforderlich. </span><span class="sxs-lookup"><span data-stu-id="2da05-139">Required.</span></span>  <br/> |
|<span data-ttu-id="2da05-140">**id**</span><span class="sxs-lookup"><span data-stu-id="2da05-140">**id**</span></span> <br/> |<span data-ttu-id="2da05-141">Die eindeutige ID des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="2da05-141">The unique ID of the user.</span></span> <span data-ttu-id="2da05-142">Erforderlich. </span><span class="sxs-lookup"><span data-stu-id="2da05-142">Required.</span></span>  <br/> |
|<span data-ttu-id="2da05-143">**nameHint**</span><span class="sxs-lookup"><span data-stu-id="2da05-143">**nameHint**</span></span> <br/> |<span data-ttu-id="2da05-144">Der Name, der im Feedelement angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2da05-144">The name to be displayed in the feed item.</span></span> <span data-ttu-id="2da05-145">Optional.</span><span class="sxs-lookup"><span data-stu-id="2da05-145">Optional.</span></span>  <br/> |
|<span data-ttu-id="2da05-146">**profileUrl**</span><span class="sxs-lookup"><span data-stu-id="2da05-146">**profileUrl**</span></span> <br/> |<span data-ttu-id="2da05-147">Die URL des Profils der Person, die als Hyperlink für den Namen der Person im Feedelement verwendet wird, wenn der Name der Person vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2da05-147">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="2da05-148">Optional.</span><span class="sxs-lookup"><span data-stu-id="2da05-148">Optional.</span></span>  <br/> |
|<span data-ttu-id="2da05-149">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="2da05-149">**emailAddress**</span></span> <br/> |<span data-ttu-id="2da05-150">Die e-Mail-Adresse, die zum Aktualisieren der Kontaktinformationen dieser Person in Outlook verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2da05-150">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="2da05-151">Optional.</span><span class="sxs-lookup"><span data-stu-id="2da05-151">Optional.</span></span>  <br/> |
   
### <a name="linkvariable"></a><span data-ttu-id="2da05-152">linkVariable</span><span class="sxs-lookup"><span data-stu-id="2da05-152">linkVariable</span></span>

|<span data-ttu-id="2da05-153">**Element**</span><span class="sxs-lookup"><span data-stu-id="2da05-153">**Element**</span></span>|<span data-ttu-id="2da05-154">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2da05-154">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2da05-155">**Name**</span><span class="sxs-lookup"><span data-stu-id="2da05-155">**name**</span></span> <br/> |<span data-ttu-id="2da05-156">Der Name der Variablen.</span><span class="sxs-lookup"><span data-stu-id="2da05-156">The name of the variable.</span></span> <span data-ttu-id="2da05-157">Erforderlich. </span><span class="sxs-lookup"><span data-stu-id="2da05-157">Required.</span></span>  <br/> |
|<span data-ttu-id="2da05-158">**value**</span><span class="sxs-lookup"><span data-stu-id="2da05-158">**value**</span></span> <br/> |<span data-ttu-id="2da05-159">Die URL für diesen Link.</span><span class="sxs-lookup"><span data-stu-id="2da05-159">The URL for this link.</span></span> <span data-ttu-id="2da05-160">Erforderlich. </span><span class="sxs-lookup"><span data-stu-id="2da05-160">Required.</span></span>  <br/> |
|<span data-ttu-id="2da05-161">**text**</span><span class="sxs-lookup"><span data-stu-id="2da05-161">**text**</span></span> <br/> |<span data-ttu-id="2da05-162">Der Linktext, der anstelle der URL selbst angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2da05-162">The link text to display instead of the URL itself.</span></span> <span data-ttu-id="2da05-163">Optional.</span><span class="sxs-lookup"><span data-stu-id="2da05-163">Optional.</span></span>  <br/> |
   
### <a name="listvariable"></a><span data-ttu-id="2da05-164">listVariable</span><span class="sxs-lookup"><span data-stu-id="2da05-164">listVariable</span></span>

|<span data-ttu-id="2da05-165">**Element**</span><span class="sxs-lookup"><span data-stu-id="2da05-165">**Element**</span></span>|<span data-ttu-id="2da05-166">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2da05-166">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2da05-167">**Name**</span><span class="sxs-lookup"><span data-stu-id="2da05-167">**name**</span></span> <br/> |<span data-ttu-id="2da05-168">Der Name der Variablen.</span><span class="sxs-lookup"><span data-stu-id="2da05-168">The name of the variable.</span></span> <span data-ttu-id="2da05-169">Erforderlich. </span><span class="sxs-lookup"><span data-stu-id="2da05-169">Required.</span></span>  <br/> |
|<span data-ttu-id="2da05-170">**listItems**</span><span class="sxs-lookup"><span data-stu-id="2da05-170">**listItems**</span></span> <br/> |<span data-ttu-id="2da05-171">Ein Container für Elemente in der Liste.</span><span class="sxs-lookup"><span data-stu-id="2da05-171">A container for items in the list.</span></span> <span data-ttu-id="2da05-172">Erforderlich. </span><span class="sxs-lookup"><span data-stu-id="2da05-172">Required.</span></span>  <br/> |
   
### <a name="picturevariable"></a><span data-ttu-id="2da05-173">pictureVariable</span><span class="sxs-lookup"><span data-stu-id="2da05-173">pictureVariable</span></span>

|<span data-ttu-id="2da05-174">**Element**</span><span class="sxs-lookup"><span data-stu-id="2da05-174">**Element**</span></span>|<span data-ttu-id="2da05-175">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2da05-175">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2da05-176">**Name**</span><span class="sxs-lookup"><span data-stu-id="2da05-176">**name**</span></span> <br/> |<span data-ttu-id="2da05-177">Der Name der Variablen.</span><span class="sxs-lookup"><span data-stu-id="2da05-177">The name of the variable.</span></span> <span data-ttu-id="2da05-178">Erforderlich. </span><span class="sxs-lookup"><span data-stu-id="2da05-178">Required.</span></span>  <br/> |
|<span data-ttu-id="2da05-179">**value**</span><span class="sxs-lookup"><span data-stu-id="2da05-179">**value**</span></span> <br/> |<span data-ttu-id="2da05-180">Die URL für das Bild.</span><span class="sxs-lookup"><span data-stu-id="2da05-180">The URL for the picture.</span></span> <span data-ttu-id="2da05-181">Erforderlich. </span><span class="sxs-lookup"><span data-stu-id="2da05-181">Required.</span></span>  <br/> |
|<span data-ttu-id="2da05-182">**altText**</span><span class="sxs-lookup"><span data-stu-id="2da05-182">**altText**</span></span> <br/> |<span data-ttu-id="2da05-183">Der Alternative Text, der für die Eingabehilfen angezeigt werden soll, und beim Bewegen des Mauszeigers über das Bild.</span><span class="sxs-lookup"><span data-stu-id="2da05-183">The alternate text to display for accessibility and when the user moves the mouse pointer over the picture.</span></span> <span data-ttu-id="2da05-184">Optional.</span><span class="sxs-lookup"><span data-stu-id="2da05-184">Optional.</span></span>  <br/> |
|<span data-ttu-id="2da05-185">**href**</span><span class="sxs-lookup"><span data-stu-id="2da05-185">**href**</span></span> <br/> |<span data-ttu-id="2da05-186">Der Hyperlink, der verwendet werden soll, wenn der Benutzer auf das Bild klickt, wenn das gewünschte Ziel nicht die vom **value** -Element angegebene Bild-URL ist.</span><span class="sxs-lookup"><span data-stu-id="2da05-186">The hyperlink to use when the user clicks the picture, if the desired target is not the picture URL specified by the **value** element.</span></span> <span data-ttu-id="2da05-187">Optional.</span><span class="sxs-lookup"><span data-stu-id="2da05-187">Optional.</span></span>  <br/> |
   
### <a name="publishervariable"></a><span data-ttu-id="2da05-188">publisherVariable</span><span class="sxs-lookup"><span data-stu-id="2da05-188">publisherVariable</span></span>

|<span data-ttu-id="2da05-189">**Element**</span><span class="sxs-lookup"><span data-stu-id="2da05-189">**Element**</span></span>|<span data-ttu-id="2da05-190">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2da05-190">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2da05-191">**Name**</span><span class="sxs-lookup"><span data-stu-id="2da05-191">**name**</span></span> <br/> |<span data-ttu-id="2da05-192">Der Name der Variablen.</span><span class="sxs-lookup"><span data-stu-id="2da05-192">The name of the variable.</span></span> <span data-ttu-id="2da05-193">Erforderlich. </span><span class="sxs-lookup"><span data-stu-id="2da05-193">Required.</span></span>  <br/> |
|<span data-ttu-id="2da05-194">**id**</span><span class="sxs-lookup"><span data-stu-id="2da05-194">**id**</span></span> <br/> |<span data-ttu-id="2da05-195">Die eindeutige ID des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="2da05-195">The unique ID of the user.</span></span> <span data-ttu-id="2da05-196">Erforderlich. </span><span class="sxs-lookup"><span data-stu-id="2da05-196">Required.</span></span>  <br/> |
|<span data-ttu-id="2da05-197">**nameHint**</span><span class="sxs-lookup"><span data-stu-id="2da05-197">**nameHint**</span></span> <br/> |<span data-ttu-id="2da05-198">Der Name, der im Feedelement angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2da05-198">The name to be displayed in the feed item.</span></span> <span data-ttu-id="2da05-199">Optional.</span><span class="sxs-lookup"><span data-stu-id="2da05-199">Optional.</span></span>  <br/> |
|<span data-ttu-id="2da05-200">**profileUrl**</span><span class="sxs-lookup"><span data-stu-id="2da05-200">**profileUrl**</span></span> <br/> |<span data-ttu-id="2da05-201">Die URL des Profils der Person, die als Hyperlink für den Namen der Person im Feedelement verwendet wird, wenn der Name der Person vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2da05-201">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="2da05-202">Optional.</span><span class="sxs-lookup"><span data-stu-id="2da05-202">Optional.</span></span>  <br/> |
|<span data-ttu-id="2da05-203">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="2da05-203">**emailAddress**</span></span> <br/> |<span data-ttu-id="2da05-204">Die e-Mail-Adresse, die zum Aktualisieren der Kontaktinformationen dieser Person in Outlook verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2da05-204">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="2da05-205">Optional.</span><span class="sxs-lookup"><span data-stu-id="2da05-205">Optional.</span></span>  <br/> |
   
### <a name="textvariable"></a><span data-ttu-id="2da05-206">Textvariable</span><span class="sxs-lookup"><span data-stu-id="2da05-206">textVariable</span></span>

|<span data-ttu-id="2da05-207">**Element**</span><span class="sxs-lookup"><span data-stu-id="2da05-207">**Element**</span></span>|<span data-ttu-id="2da05-208">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2da05-208">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2da05-209">**Name**</span><span class="sxs-lookup"><span data-stu-id="2da05-209">**name**</span></span> <br/> |<span data-ttu-id="2da05-210">Der Name der Variablen.</span><span class="sxs-lookup"><span data-stu-id="2da05-210">The name of the variable.</span></span> <span data-ttu-id="2da05-211">Erforderlich. </span><span class="sxs-lookup"><span data-stu-id="2da05-211">Required.</span></span>  <br/> |
|<span data-ttu-id="2da05-212">**value**</span><span class="sxs-lookup"><span data-stu-id="2da05-212">**value**</span></span> <br/> |<span data-ttu-id="2da05-213">Der anzuzeigende Text.</span><span class="sxs-lookup"><span data-stu-id="2da05-213">The text to display.</span></span> <span data-ttu-id="2da05-214">Optional.</span><span class="sxs-lookup"><span data-stu-id="2da05-214">Optional.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2da05-215">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2da05-215">See also</span></span>

- [<span data-ttu-id="2da05-216">Übersicht über XML für ein Aktivitäts Feed-Element</span><span class="sxs-lookup"><span data-stu-id="2da05-216">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="2da05-217">activityDetails-Element</span><span class="sxs-lookup"><span data-stu-id="2da05-217">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="2da05-218">activityTemplateContainer-Element</span><span class="sxs-lookup"><span data-stu-id="2da05-218">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="2da05-219">Richtlinien für die OrdnungsGemäße Anzeige von Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="2da05-219">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="2da05-220">XML für Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="2da05-220">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="2da05-221">XML-Schema des Anbieters für soziale Netzwerke in Outlook</span><span class="sxs-lookup"><span data-stu-id="2da05-221">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="2da05-222">Entwickeln eines Providers mit dem OSC-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="2da05-222">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

