---
title: Vorlagenvariablen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6f8f6af2-c7fa-4135-9532-7af5fc643b0d
description: Instanzen von Vorlagenvariablen (dargestellt durch ein TemplateVariable-Element) angeben, die Daten von einer Aktivitätsfeed-Element in einer Aktivitätsvorlage.
ms.openlocfilehash: 99f4c2de586447fb0361e528bcd33d62b79e0fb1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796106"
---
# <a name="template-variables"></a><span data-ttu-id="d6bcf-103">Vorlagenvariablen</span><span class="sxs-lookup"><span data-stu-id="d6bcf-103">Template variables</span></span>

<span data-ttu-id="d6bcf-104">Instanzen von Vorlagenvariablen (dargestellt durch ein **TemplateVariable** -Element) angeben, die Daten von einer Aktivitätsfeed-Element in einer Aktivitätsvorlage.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-104">Instances of template variables (represented by a **templateVariable** element) specify the data of an activity feed item in an activity template.</span></span> 
  
<span data-ttu-id="d6bcf-105">Ein Beispiel der Aktivität XML-feed, finden Sie unter [Aktivität Feed XML-Beispiel](activity-feed-xml-example.md).</span><span class="sxs-lookup"><span data-stu-id="d6bcf-105">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>

<span data-ttu-id="d6bcf-106">Die folgende Tabelle zeigt den Typen von unterstützten Vorlagenvariablen, jeweils durch die entsprechende XML-Enumerationswert dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-106">The following table shows the types of supported template variables, each represented by the corresponding XML enumeration value.</span></span>
  
|<span data-ttu-id="d6bcf-107">**Typ der Vorlage Variablen**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-107">**Type of template variable**</span></span>|<span data-ttu-id="d6bcf-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d6bcf-109">**entityVariable**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-109">**entityVariable**</span></span> <br/> |<span data-ttu-id="d6bcf-110">Eine Person, eine Gruppe oder eine Sache.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-110">A person, group, or thing.</span></span>  <br/> |
|<span data-ttu-id="d6bcf-111">**linkVariable**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-111">**linkVariable**</span></span> <br/> |<span data-ttu-id="d6bcf-112">Eine Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-112">A link.</span></span>  <br/> |
|<span data-ttu-id="d6bcf-113">**listVariable**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-113">**listVariable**</span></span> <br/> |<span data-ttu-id="d6bcf-114">Eine Gruppe von Objekten.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-114">A group of objects.</span></span>  <br/> |
|<span data-ttu-id="d6bcf-115">**pictureVariable**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-115">**pictureVariable**</span></span> <br/> |<span data-ttu-id="d6bcf-116">Ein Bild.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-116">A picture.</span></span>  <br/> |
|<span data-ttu-id="d6bcf-117">**publisherVariable**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-117">**publisherVariable**</span></span> <br/> |<span data-ttu-id="d6bcf-118">Element-feed der Herausgeber der Aktivität.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-118">The publisher of the activity feed item.</span></span>  <br/> |
|<span data-ttu-id="d6bcf-119">**textVariable**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-119">**textVariable**</span></span> <br/> |<span data-ttu-id="d6bcf-120">Text-Block.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-120">A block of text.</span></span>  <br/> |
   
<span data-ttu-id="d6bcf-121">Jede Art von Vorlage Variable hat Elemente an, die Daten über diese Variable erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-121">Each type of template variable has required elements to specify the data about that variable.</span></span> <span data-ttu-id="d6bcf-122">Vorlagenvariablen werden wie folgt angegeben:</span><span class="sxs-lookup"><span data-stu-id="d6bcf-122">Template variables are specified as follows:</span></span>
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a><span data-ttu-id="d6bcf-123">Die Vorlage Listenvariable</span><span class="sxs-lookup"><span data-stu-id="d6bcf-123">List template variable</span></span>

<span data-ttu-id="d6bcf-124">Sie können Vorlagenvariablen angeben, die in einer Liste (getrennt durch die **ListVariable** und **ListItems** Elemente) wie folgt enthalten sind:</span><span class="sxs-lookup"><span data-stu-id="d6bcf-124">You can specify template variables that are contained within a list (delimited by the **listVariable** and **listItems** elements) as follows:</span></span> 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
<span data-ttu-id="d6bcf-125">Eine Vorlage Variable vom Typ **ListVariable** ist ein Container für Objekte.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-125">A template variable of the **listVariable** type is a container for objects.</span></span> <span data-ttu-id="d6bcf-126">Sie können durch Kommas getrennte Elemente (vom Typ **LinkVariable** oder **TextVariable** ) oder Bilder (vom Typ **PictureVariable** ) enthalten.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-126">It can contain comma-delimited items (of the **linkVariable** or **textVariable** type) or pictures (of the **pictureVariable** type).</span></span> <span data-ttu-id="d6bcf-127">Listen können bis zu fünf Verknüpfen von Elementen, fünf Textelemente oder fünf Bilder enthalten.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-127">Lists can contain up to five link items, five text items, or five pictures.</span></span> 
  
<span data-ttu-id="d6bcf-128">Outlook Social Connector (OSC) lokalisiert Link oder Text Listenelemente entsprechend des Windows-Systemgebietsschemas an.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-128">The Outlook Social Connector (OSC) localizes link or text list items according to the Windows system locale.</span></span>
  
<span data-ttu-id="d6bcf-129">Um korrekt analysiert und Anzeigen von Bildern in einer Aktivitätsfeed-Element, müssen Sie Bilder in einer Liste einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-129">To correctly parse and display pictures in an activity feed item, you must include pictures in a list.</span></span> <span data-ttu-id="d6bcf-130">Alle Bilder werden Größe der 52 Pixel hoch sein.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-130">All pictures are resized to be 52 pixels high.</span></span> <span data-ttu-id="d6bcf-131">Die Breite des Bilds wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-131">The width of the picture is not resized.</span></span>
  
## <a name="template-variable-elements"></a><span data-ttu-id="d6bcf-132">Vorlage Variable Elemente</span><span class="sxs-lookup"><span data-stu-id="d6bcf-132">Template variable elements</span></span>

<span data-ttu-id="d6bcf-133">Dieser Abschnitt enthält die erforderlichen und optionalen Elemente für jede Art von Vorlage Variable unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-133">This section covers the required and optional elements supported for each type of template variable.</span></span>
  
### <a name="entityvariable"></a><span data-ttu-id="d6bcf-134">entityVariable</span><span class="sxs-lookup"><span data-stu-id="d6bcf-134">entityVariable</span></span>

|<span data-ttu-id="d6bcf-135">**Element**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-135">**Element**</span></span>|<span data-ttu-id="d6bcf-136">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-136">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d6bcf-137">**Name**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-137">**name**</span></span> <br/> |<span data-ttu-id="d6bcf-138">Der Name der Variablen.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-138">The name of the variable.</span></span> <span data-ttu-id="d6bcf-139">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-139">Required.</span></span>  <br/> |
|<span data-ttu-id="d6bcf-140">**id**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-140">**id**</span></span> <br/> |<span data-ttu-id="d6bcf-141">Die eindeutige ID des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-141">The unique ID of the user.</span></span> <span data-ttu-id="d6bcf-142">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-142">Required.</span></span>  <br/> |
|<span data-ttu-id="d6bcf-143">**nameHint**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-143">**nameHint**</span></span> <br/> |<span data-ttu-id="d6bcf-144">Der Name der feed-Element angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-144">The name to be displayed in the feed item.</span></span> <span data-ttu-id="d6bcf-145">Optional.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-145">Optional.</span></span>  <br/> |
|<span data-ttu-id="d6bcf-146">**profileUrl**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-146">**profileUrl**</span></span> <br/> |<span data-ttu-id="d6bcf-147">Die URL des Profils der Person, die für den Namen der Person in der feed-Element als Hyperlink verwendet wird, wenn Sie den Namen der Person vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-147">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="d6bcf-148">Optional.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-148">Optional.</span></span>  <br/> |
|<span data-ttu-id="d6bcf-149">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-149">**emailAddress**</span></span> <br/> |<span data-ttu-id="d6bcf-150">Die e-Mail-Adresse, die verwendet wird, um die Kontaktinformationen dieser Person in Outlook zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-150">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="d6bcf-151">Optional.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-151">Optional.</span></span>  <br/> |
   
### <a name="linkvariable"></a><span data-ttu-id="d6bcf-152">linkVariable</span><span class="sxs-lookup"><span data-stu-id="d6bcf-152">linkVariable</span></span>

|<span data-ttu-id="d6bcf-153">**Element**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-153">**Element**</span></span>|<span data-ttu-id="d6bcf-154">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-154">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d6bcf-155">**Name**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-155">**name**</span></span> <br/> |<span data-ttu-id="d6bcf-156">Der Name der Variablen.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-156">The name of the variable.</span></span> <span data-ttu-id="d6bcf-157">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-157">Required.</span></span>  <br/> |
|<span data-ttu-id="d6bcf-158">**Value**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-158">**value**</span></span> <br/> |<span data-ttu-id="d6bcf-159">Die URL für diese Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-159">The URL for this link.</span></span> <span data-ttu-id="d6bcf-160">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-160">Required.</span></span>  <br/> |
|<span data-ttu-id="d6bcf-161">**text**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-161">**text**</span></span> <br/> |<span data-ttu-id="d6bcf-162">Der Linktext, anstatt die URL selbst angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-162">The link text to display instead of the URL itself.</span></span> <span data-ttu-id="d6bcf-163">Optional.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-163">Optional.</span></span>  <br/> |
   
### <a name="listvariable"></a><span data-ttu-id="d6bcf-164">listVariable</span><span class="sxs-lookup"><span data-stu-id="d6bcf-164">listVariable</span></span>

|<span data-ttu-id="d6bcf-165">**Element**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-165">**Element**</span></span>|<span data-ttu-id="d6bcf-166">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-166">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d6bcf-167">**Name**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-167">**name**</span></span> <br/> |<span data-ttu-id="d6bcf-168">Der Name der Variablen.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-168">The name of the variable.</span></span> <span data-ttu-id="d6bcf-169">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-169">Required.</span></span>  <br/> |
|<span data-ttu-id="d6bcf-170">**listItems**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-170">**listItems**</span></span> <br/> |<span data-ttu-id="d6bcf-171">Ein Container für Elemente in der Liste.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-171">A container for items in the list.</span></span> <span data-ttu-id="d6bcf-172">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-172">Required.</span></span>  <br/> |
   
### <a name="picturevariable"></a><span data-ttu-id="d6bcf-173">pictureVariable</span><span class="sxs-lookup"><span data-stu-id="d6bcf-173">pictureVariable</span></span>

|<span data-ttu-id="d6bcf-174">**Element**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-174">**Element**</span></span>|<span data-ttu-id="d6bcf-175">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-175">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d6bcf-176">**Name**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-176">**name**</span></span> <br/> |<span data-ttu-id="d6bcf-177">Der Name der Variablen.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-177">The name of the variable.</span></span> <span data-ttu-id="d6bcf-178">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-178">Required.</span></span>  <br/> |
|<span data-ttu-id="d6bcf-179">**Value**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-179">**value**</span></span> <br/> |<span data-ttu-id="d6bcf-180">Die URL für das Bild.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-180">The URL for the picture.</span></span> <span data-ttu-id="d6bcf-181">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-181">Required.</span></span>  <br/> |
|<span data-ttu-id="d6bcf-182">**altText**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-182">**altText**</span></span> <br/> |<span data-ttu-id="d6bcf-183">Der alternative Text für Eingabehilfen und wenn der Benutzer den Mauszeiger über das Bild bewegt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-183">The alternate text to display for accessibility and when the user moves the mouse pointer over the picture.</span></span> <span data-ttu-id="d6bcf-184">Optional.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-184">Optional.</span></span>  <br/> |
|<span data-ttu-id="d6bcf-185">**href**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-185">**href**</span></span> <br/> |<span data-ttu-id="d6bcf-186">Der Hyperlink klickt der Benutzer das Bild verwenden, wenn das gewünschte Ziel nicht die Bild-URL, die durch das **Value** -Element angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-186">The hyperlink to use when the user clicks the picture, if the desired target is not the picture URL specified by the **value** element.</span></span> <span data-ttu-id="d6bcf-187">Optional.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-187">Optional.</span></span>  <br/> |
   
### <a name="publishervariable"></a><span data-ttu-id="d6bcf-188">publisherVariable</span><span class="sxs-lookup"><span data-stu-id="d6bcf-188">publisherVariable</span></span>

|<span data-ttu-id="d6bcf-189">**Element**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-189">**Element**</span></span>|<span data-ttu-id="d6bcf-190">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-190">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d6bcf-191">**Name**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-191">**name**</span></span> <br/> |<span data-ttu-id="d6bcf-192">Der Name der Variablen.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-192">The name of the variable.</span></span> <span data-ttu-id="d6bcf-193">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-193">Required.</span></span>  <br/> |
|<span data-ttu-id="d6bcf-194">**id**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-194">**id**</span></span> <br/> |<span data-ttu-id="d6bcf-195">Die eindeutige ID des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-195">The unique ID of the user.</span></span> <span data-ttu-id="d6bcf-196">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-196">Required.</span></span>  <br/> |
|<span data-ttu-id="d6bcf-197">**nameHint**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-197">**nameHint**</span></span> <br/> |<span data-ttu-id="d6bcf-198">Der Name der feed-Element angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-198">The name to be displayed in the feed item.</span></span> <span data-ttu-id="d6bcf-199">Optional.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-199">Optional.</span></span>  <br/> |
|<span data-ttu-id="d6bcf-200">**profileUrl**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-200">**profileUrl**</span></span> <br/> |<span data-ttu-id="d6bcf-201">Die URL des Profils der Person, die für den Namen der Person in der feed-Element als Hyperlink verwendet wird, wenn Sie den Namen der Person vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-201">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="d6bcf-202">Optional.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-202">Optional.</span></span>  <br/> |
|<span data-ttu-id="d6bcf-203">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-203">**emailAddress**</span></span> <br/> |<span data-ttu-id="d6bcf-204">Die e-Mail-Adresse, die verwendet wird, um die Kontaktinformationen dieser Person in Outlook zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-204">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="d6bcf-205">Optional.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-205">Optional.</span></span>  <br/> |
   
### <a name="textvariable"></a><span data-ttu-id="d6bcf-206">textVariable</span><span class="sxs-lookup"><span data-stu-id="d6bcf-206">textVariable</span></span>

|<span data-ttu-id="d6bcf-207">**Element**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-207">**Element**</span></span>|<span data-ttu-id="d6bcf-208">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-208">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d6bcf-209">**Name**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-209">**name**</span></span> <br/> |<span data-ttu-id="d6bcf-210">Der Name der Variablen.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-210">The name of the variable.</span></span> <span data-ttu-id="d6bcf-211">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-211">Required.</span></span>  <br/> |
|<span data-ttu-id="d6bcf-212">**Value**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-212">**value**</span></span> <br/> |<span data-ttu-id="d6bcf-213">Der anzuzeigende Text.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-213">The text to display.</span></span> <span data-ttu-id="d6bcf-214">Optional.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-214">Optional.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d6bcf-215">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6bcf-215">See also</span></span>

- [<span data-ttu-id="d6bcf-216">Übersicht über XML-Code für eine Aktivität Element-Feed</span><span class="sxs-lookup"><span data-stu-id="d6bcf-216">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="d6bcf-217">ActivityDetails Element</span><span class="sxs-lookup"><span data-stu-id="d6bcf-217">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="d6bcf-218">ActivityTemplateContainer Element</span><span class="sxs-lookup"><span data-stu-id="d6bcf-218">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="d6bcf-219">Richtlinien für das Aktivitäten ordnungsgemäß anzeigen</span><span class="sxs-lookup"><span data-stu-id="d6bcf-219">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="d6bcf-220">XML-Code für Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="d6bcf-220">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="d6bcf-221">Outlook Connector für soziale Netzwerke Anbieter XML-Schema</span><span class="sxs-lookup"><span data-stu-id="d6bcf-221">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="d6bcf-222">Entwickeln eines Providers mit dem OSC-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="d6bcf-222">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

