---
title: Vorlagenvariablen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6f8f6af2-c7fa-4135-9532-7af5fc643b0d
description: Instanzen von Vorlagenvariablen (dargestellt durch ein templateVariable-Element) geben die Daten eines Aktivitätsfeedelements in einer Aktivitätsvorlage an.
ms.openlocfilehash: 9b37665488f0f1e2bd205fb7d4a5d2201697d7c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404372"
---
# <a name="template-variables"></a><span data-ttu-id="1ae36-103">Vorlagenvariablen</span><span class="sxs-lookup"><span data-stu-id="1ae36-103">Template variables</span></span>

<span data-ttu-id="1ae36-104">Instanzen von Vorlagenvariablen (dargestellt durch ein **templateVariable-Element)** geben die Daten eines Aktivitätsfeedelements in einer Aktivitätsvorlage an.</span><span class="sxs-lookup"><span data-stu-id="1ae36-104">Instances of template variables (represented by a **templateVariable** element) specify the data of an activity feed item in an activity template.</span></span> 
  
<span data-ttu-id="1ae36-105">Ein Beispiel für aktivitätsfeed-XML finden Sie unter [Activity Feed XML Example](activity-feed-xml-example.md).</span><span class="sxs-lookup"><span data-stu-id="1ae36-105">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>

<span data-ttu-id="1ae36-106">Die folgende Tabelle zeigt die Typen unterstützter Vorlagenvariablen, die jeweils durch den entsprechenden XML-Enumerationswert dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1ae36-106">The following table shows the types of supported template variables, each represented by the corresponding XML enumeration value.</span></span>
  
|<span data-ttu-id="1ae36-107">**Typ der Vorlagenvariable**</span><span class="sxs-lookup"><span data-stu-id="1ae36-107">**Type of template variable**</span></span>|<span data-ttu-id="1ae36-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1ae36-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1ae36-109">**entityVariable**</span><span class="sxs-lookup"><span data-stu-id="1ae36-109">**entityVariable**</span></span> <br/> |<span data-ttu-id="1ae36-110">Eine Person, Eine Gruppe oder eine Sache.</span><span class="sxs-lookup"><span data-stu-id="1ae36-110">A person, group, or thing.</span></span>  <br/> |
|<span data-ttu-id="1ae36-111">**linkVariable**</span><span class="sxs-lookup"><span data-stu-id="1ae36-111">**linkVariable**</span></span> <br/> |<span data-ttu-id="1ae36-112">Ein Link.</span><span class="sxs-lookup"><span data-stu-id="1ae36-112">A link.</span></span>  <br/> |
|<span data-ttu-id="1ae36-113">**listVariable**</span><span class="sxs-lookup"><span data-stu-id="1ae36-113">**listVariable**</span></span> <br/> |<span data-ttu-id="1ae36-114">Eine Gruppe von Objekten.</span><span class="sxs-lookup"><span data-stu-id="1ae36-114">A group of objects.</span></span>  <br/> |
|<span data-ttu-id="1ae36-115">**pictureVariable**</span><span class="sxs-lookup"><span data-stu-id="1ae36-115">**pictureVariable**</span></span> <br/> |<span data-ttu-id="1ae36-116">Ein Bild.</span><span class="sxs-lookup"><span data-stu-id="1ae36-116">A picture.</span></span>  <br/> |
|<span data-ttu-id="1ae36-117">**publisherVariable**</span><span class="sxs-lookup"><span data-stu-id="1ae36-117">**publisherVariable**</span></span> <br/> |<span data-ttu-id="1ae36-118">Der Herausgeber des Aktivitätsfeedelements.</span><span class="sxs-lookup"><span data-stu-id="1ae36-118">The publisher of the activity feed item.</span></span>  <br/> |
|<span data-ttu-id="1ae36-119">**textVariable**</span><span class="sxs-lookup"><span data-stu-id="1ae36-119">**textVariable**</span></span> <br/> |<span data-ttu-id="1ae36-120">Ein Textblock.</span><span class="sxs-lookup"><span data-stu-id="1ae36-120">A block of text.</span></span>  <br/> |
   
<span data-ttu-id="1ae36-121">Jeder Typ von Vorlagenvariablen verfügt über erforderliche Elemente, um die Daten zu dieser Variablen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1ae36-121">Each type of template variable has required elements to specify the data about that variable.</span></span> <span data-ttu-id="1ae36-122">Vorlagenvariablen werden wie folgt angegeben:</span><span class="sxs-lookup"><span data-stu-id="1ae36-122">Template variables are specified as follows:</span></span>
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a><span data-ttu-id="1ae36-123">Vorlagenvariable auflisten</span><span class="sxs-lookup"><span data-stu-id="1ae36-123">List template variable</span></span>

<span data-ttu-id="1ae36-124">Sie können Vorlagenvariablen angeben, die in einer Liste enthalten sind (durch die **Elemente listVariable** und **listItems** getrennt) wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1ae36-124">You can specify template variables that are contained within a list (delimited by the **listVariable** and **listItems** elements) as follows:</span></span> 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
<span data-ttu-id="1ae36-125">Eine Vorlagenvariable des **Typs listVariable** ist ein Container für Objekte.</span><span class="sxs-lookup"><span data-stu-id="1ae36-125">A template variable of the **listVariable** type is a container for objects.</span></span> <span data-ttu-id="1ae36-126">Sie kann durch Trennzeichen getrennte Elemente (vom **Typ linkVariable** oder **textVariable)** oder Bilder (vom **Typ pictureVariable)** enthalten.</span><span class="sxs-lookup"><span data-stu-id="1ae36-126">It can contain comma-delimited items (of the **linkVariable** or **textVariable** type) or pictures (of the **pictureVariable** type).</span></span> <span data-ttu-id="1ae36-127">Listen können bis zu fünf Linkelemente, fünf Textelemente oder fünf Bilder enthalten.</span><span class="sxs-lookup"><span data-stu-id="1ae36-127">Lists can contain up to five link items, five text items, or five pictures.</span></span> 
  
<span data-ttu-id="1ae36-128">Der Outlook Social Connector (OSC) lokalisiert Link- oder Textlistenelemente gemäß dem Windows-System-Locale.</span><span class="sxs-lookup"><span data-stu-id="1ae36-128">The Outlook Social Connector (OSC) localizes link or text list items according to the Windows system locale.</span></span>
  
<span data-ttu-id="1ae36-129">Zum ordnungsgemäßen Analysieren und Anzeigen von Bildern in einem Aktivitätsfeedelement müssen Sie Bilder in eine Liste hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1ae36-129">To correctly parse and display pictures in an activity feed item, you must include pictures in a list.</span></span> <span data-ttu-id="1ae36-130">Alle Bilder werden auf eine Höhe von 52 Pixeln geändert.</span><span class="sxs-lookup"><span data-stu-id="1ae36-130">All pictures are resized to be 52 pixels high.</span></span> <span data-ttu-id="1ae36-131">Die Breite des Bilds wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="1ae36-131">The width of the picture is not resized.</span></span>
  
## <a name="template-variable-elements"></a><span data-ttu-id="1ae36-132">Vorlagenvariablenelemente</span><span class="sxs-lookup"><span data-stu-id="1ae36-132">Template variable elements</span></span>

<span data-ttu-id="1ae36-133">In diesem Abschnitt werden die erforderlichen und optionalen Elemente behandelt, die für jeden Typ von Vorlagenvariablen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="1ae36-133">This section covers the required and optional elements supported for each type of template variable.</span></span>
  
### <a name="entityvariable"></a><span data-ttu-id="1ae36-134">entityVariable</span><span class="sxs-lookup"><span data-stu-id="1ae36-134">entityVariable</span></span>

|<span data-ttu-id="1ae36-135">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ae36-135">**Element**</span></span>|<span data-ttu-id="1ae36-136">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1ae36-136">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1ae36-137">**Name**</span><span class="sxs-lookup"><span data-stu-id="1ae36-137">**name**</span></span> <br/> |<span data-ttu-id="1ae36-138">Der Name der Variablen.</span><span class="sxs-lookup"><span data-stu-id="1ae36-138">The name of the variable.</span></span> <span data-ttu-id="1ae36-139">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1ae36-139">Required.</span></span>  <br/> |
|<span data-ttu-id="1ae36-140">**id**</span><span class="sxs-lookup"><span data-stu-id="1ae36-140">**id**</span></span> <br/> |<span data-ttu-id="1ae36-141">Die eindeutige ID des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="1ae36-141">The unique ID of the user.</span></span> <span data-ttu-id="1ae36-142">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1ae36-142">Required.</span></span>  <br/> |
|<span data-ttu-id="1ae36-143">**nameHint**</span><span class="sxs-lookup"><span data-stu-id="1ae36-143">**nameHint**</span></span> <br/> |<span data-ttu-id="1ae36-144">Der Name, der im Feedelement angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1ae36-144">The name to be displayed in the feed item.</span></span> <span data-ttu-id="1ae36-145">Optional.</span><span class="sxs-lookup"><span data-stu-id="1ae36-145">Optional.</span></span>  <br/> |
|<span data-ttu-id="1ae36-146">**profileUrl**</span><span class="sxs-lookup"><span data-stu-id="1ae36-146">**profileUrl**</span></span> <br/> |<span data-ttu-id="1ae36-147">Die URL des Profils der Person, die als Hyperlink für den Namen der Person im Feedelement verwendet wird, wenn der Name der Person vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1ae36-147">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="1ae36-148">Optional.</span><span class="sxs-lookup"><span data-stu-id="1ae36-148">Optional.</span></span>  <br/> |
|<span data-ttu-id="1ae36-149">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="1ae36-149">**emailAddress**</span></span> <br/> |<span data-ttu-id="1ae36-150">Die E-Mail-Adresse, die zum Aktualisieren der Kontaktinformationen dieser Person in Outlook verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1ae36-150">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="1ae36-151">Optional.</span><span class="sxs-lookup"><span data-stu-id="1ae36-151">Optional.</span></span>  <br/> |
   
### <a name="linkvariable"></a><span data-ttu-id="1ae36-152">linkVariable</span><span class="sxs-lookup"><span data-stu-id="1ae36-152">linkVariable</span></span>

|<span data-ttu-id="1ae36-153">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ae36-153">**Element**</span></span>|<span data-ttu-id="1ae36-154">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1ae36-154">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1ae36-155">**Name**</span><span class="sxs-lookup"><span data-stu-id="1ae36-155">**name**</span></span> <br/> |<span data-ttu-id="1ae36-156">Der Name der Variablen.</span><span class="sxs-lookup"><span data-stu-id="1ae36-156">The name of the variable.</span></span> <span data-ttu-id="1ae36-157">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1ae36-157">Required.</span></span>  <br/> |
|<span data-ttu-id="1ae36-158">**value**</span><span class="sxs-lookup"><span data-stu-id="1ae36-158">**value**</span></span> <br/> |<span data-ttu-id="1ae36-159">Die URL für diesen Link.</span><span class="sxs-lookup"><span data-stu-id="1ae36-159">The URL for this link.</span></span> <span data-ttu-id="1ae36-160">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1ae36-160">Required.</span></span>  <br/> |
|<span data-ttu-id="1ae36-161">**text**</span><span class="sxs-lookup"><span data-stu-id="1ae36-161">**text**</span></span> <br/> |<span data-ttu-id="1ae36-162">Der Linktext, der anstelle der URL selbst angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1ae36-162">The link text to display instead of the URL itself.</span></span> <span data-ttu-id="1ae36-163">Optional.</span><span class="sxs-lookup"><span data-stu-id="1ae36-163">Optional.</span></span>  <br/> |
   
### <a name="listvariable"></a><span data-ttu-id="1ae36-164">listVariable</span><span class="sxs-lookup"><span data-stu-id="1ae36-164">listVariable</span></span>

|<span data-ttu-id="1ae36-165">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ae36-165">**Element**</span></span>|<span data-ttu-id="1ae36-166">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1ae36-166">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1ae36-167">**Name**</span><span class="sxs-lookup"><span data-stu-id="1ae36-167">**name**</span></span> <br/> |<span data-ttu-id="1ae36-168">Der Name der Variablen.</span><span class="sxs-lookup"><span data-stu-id="1ae36-168">The name of the variable.</span></span> <span data-ttu-id="1ae36-169">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1ae36-169">Required.</span></span>  <br/> |
|<span data-ttu-id="1ae36-170">**listItems**</span><span class="sxs-lookup"><span data-stu-id="1ae36-170">**listItems**</span></span> <br/> |<span data-ttu-id="1ae36-171">Ein Container für Elemente in der Liste.</span><span class="sxs-lookup"><span data-stu-id="1ae36-171">A container for items in the list.</span></span> <span data-ttu-id="1ae36-172">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1ae36-172">Required.</span></span>  <br/> |
   
### <a name="picturevariable"></a><span data-ttu-id="1ae36-173">pictureVariable</span><span class="sxs-lookup"><span data-stu-id="1ae36-173">pictureVariable</span></span>

|<span data-ttu-id="1ae36-174">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ae36-174">**Element**</span></span>|<span data-ttu-id="1ae36-175">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1ae36-175">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1ae36-176">**Name**</span><span class="sxs-lookup"><span data-stu-id="1ae36-176">**name**</span></span> <br/> |<span data-ttu-id="1ae36-177">Der Name der Variablen.</span><span class="sxs-lookup"><span data-stu-id="1ae36-177">The name of the variable.</span></span> <span data-ttu-id="1ae36-178">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1ae36-178">Required.</span></span>  <br/> |
|<span data-ttu-id="1ae36-179">**value**</span><span class="sxs-lookup"><span data-stu-id="1ae36-179">**value**</span></span> <br/> |<span data-ttu-id="1ae36-180">Die URL für das Bild.</span><span class="sxs-lookup"><span data-stu-id="1ae36-180">The URL for the picture.</span></span> <span data-ttu-id="1ae36-181">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1ae36-181">Required.</span></span>  <br/> |
|<span data-ttu-id="1ae36-182">**altText**</span><span class="sxs-lookup"><span data-stu-id="1ae36-182">**altText**</span></span> <br/> |<span data-ttu-id="1ae36-183">Der alternative Text, der für die Barrierefreiheit angezeigt werden soll und wenn der Benutzer den Mauszeiger über das Bild bewegt.</span><span class="sxs-lookup"><span data-stu-id="1ae36-183">The alternate text to display for accessibility and when the user moves the mouse pointer over the picture.</span></span> <span data-ttu-id="1ae36-184">Optional.</span><span class="sxs-lookup"><span data-stu-id="1ae36-184">Optional.</span></span>  <br/> |
|<span data-ttu-id="1ae36-185">**href**</span><span class="sxs-lookup"><span data-stu-id="1ae36-185">**href**</span></span> <br/> |<span data-ttu-id="1ae36-186">Der Hyperlink, der verwendet werden soll, wenn der Benutzer auf das Bild klickt, wenn das gewünschte Ziel nicht die vom **Value-Element** angegebene Bild-URL ist.</span><span class="sxs-lookup"><span data-stu-id="1ae36-186">The hyperlink to use when the user clicks the picture, if the desired target is not the picture URL specified by the **value** element.</span></span> <span data-ttu-id="1ae36-187">Optional.</span><span class="sxs-lookup"><span data-stu-id="1ae36-187">Optional.</span></span>  <br/> |
   
### <a name="publishervariable"></a><span data-ttu-id="1ae36-188">publisherVariable</span><span class="sxs-lookup"><span data-stu-id="1ae36-188">publisherVariable</span></span>

|<span data-ttu-id="1ae36-189">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ae36-189">**Element**</span></span>|<span data-ttu-id="1ae36-190">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1ae36-190">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1ae36-191">**Name**</span><span class="sxs-lookup"><span data-stu-id="1ae36-191">**name**</span></span> <br/> |<span data-ttu-id="1ae36-192">Der Name der Variablen.</span><span class="sxs-lookup"><span data-stu-id="1ae36-192">The name of the variable.</span></span> <span data-ttu-id="1ae36-193">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1ae36-193">Required.</span></span>  <br/> |
|<span data-ttu-id="1ae36-194">**id**</span><span class="sxs-lookup"><span data-stu-id="1ae36-194">**id**</span></span> <br/> |<span data-ttu-id="1ae36-195">Die eindeutige ID des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="1ae36-195">The unique ID of the user.</span></span> <span data-ttu-id="1ae36-196">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1ae36-196">Required.</span></span>  <br/> |
|<span data-ttu-id="1ae36-197">**nameHint**</span><span class="sxs-lookup"><span data-stu-id="1ae36-197">**nameHint**</span></span> <br/> |<span data-ttu-id="1ae36-198">Der Name, der im Feedelement angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1ae36-198">The name to be displayed in the feed item.</span></span> <span data-ttu-id="1ae36-199">Optional.</span><span class="sxs-lookup"><span data-stu-id="1ae36-199">Optional.</span></span>  <br/> |
|<span data-ttu-id="1ae36-200">**profileUrl**</span><span class="sxs-lookup"><span data-stu-id="1ae36-200">**profileUrl**</span></span> <br/> |<span data-ttu-id="1ae36-201">Die URL des Profils der Person, die als Hyperlink für den Namen der Person im Feedelement verwendet wird, wenn der Name der Person vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1ae36-201">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="1ae36-202">Optional.</span><span class="sxs-lookup"><span data-stu-id="1ae36-202">Optional.</span></span>  <br/> |
|<span data-ttu-id="1ae36-203">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="1ae36-203">**emailAddress**</span></span> <br/> |<span data-ttu-id="1ae36-204">Die E-Mail-Adresse, die zum Aktualisieren der Kontaktinformationen dieser Person in Outlook verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1ae36-204">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="1ae36-205">Optional.</span><span class="sxs-lookup"><span data-stu-id="1ae36-205">Optional.</span></span>  <br/> |
   
### <a name="textvariable"></a><span data-ttu-id="1ae36-206">textVariable</span><span class="sxs-lookup"><span data-stu-id="1ae36-206">textVariable</span></span>

|<span data-ttu-id="1ae36-207">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ae36-207">**Element**</span></span>|<span data-ttu-id="1ae36-208">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1ae36-208">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1ae36-209">**Name**</span><span class="sxs-lookup"><span data-stu-id="1ae36-209">**name**</span></span> <br/> |<span data-ttu-id="1ae36-210">Der Name der Variablen.</span><span class="sxs-lookup"><span data-stu-id="1ae36-210">The name of the variable.</span></span> <span data-ttu-id="1ae36-211">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1ae36-211">Required.</span></span>  <br/> |
|<span data-ttu-id="1ae36-212">**value**</span><span class="sxs-lookup"><span data-stu-id="1ae36-212">**value**</span></span> <br/> |<span data-ttu-id="1ae36-213">Der zu zeigende Text.</span><span class="sxs-lookup"><span data-stu-id="1ae36-213">The text to display.</span></span> <span data-ttu-id="1ae36-214">Optional.</span><span class="sxs-lookup"><span data-stu-id="1ae36-214">Optional.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1ae36-215">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ae36-215">See also</span></span>

- [<span data-ttu-id="1ae36-216">Übersicht über XML für ein Aktivitätsfeedelement</span><span class="sxs-lookup"><span data-stu-id="1ae36-216">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="1ae36-217">activityDetails-Element</span><span class="sxs-lookup"><span data-stu-id="1ae36-217">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="1ae36-218">activityTemplateContainer-Element</span><span class="sxs-lookup"><span data-stu-id="1ae36-218">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="1ae36-219">Richtlinien für die ordnungsgemäßen Anzeige von Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="1ae36-219">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="1ae36-220">XML für Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="1ae36-220">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="1ae36-221">Outlook Social Connector Provider XML Schema</span><span class="sxs-lookup"><span data-stu-id="1ae36-221">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="1ae36-222">Entwickeln eines Providers mit dem OSC-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="1ae36-222">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

