---
title: PidTagIconIndex (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIconIndex
api_type:
- HeaderDef
ms.assetid: 35bb0d6d-41d4-47d6-b161-be3721894201
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 83ab01363d478d197286bfa8f7b5b092a7ffd5a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794457"
---
# <a name="pidtagiconindex-canonical-property"></a><span data-ttu-id="54122-103">PidTagIconIndex (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="54122-103">PidTagIconIndex Canonical Property</span></span>

  
  
<span data-ttu-id="54122-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="54122-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="54122-105">Enthält eine Zahl, die angibt, welches Symbol verwenden, wenn Sie eine Gruppe von e-Mail-Objekten anzeigen.</span><span class="sxs-lookup"><span data-stu-id="54122-105">Contains a number that indicates which icon to use when you display a group of email objects.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="54122-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="54122-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="54122-107">PR_ICON_INDEX</span><span class="sxs-lookup"><span data-stu-id="54122-107">PR_ICON_INDEX</span></span>  <br/> |
|<span data-ttu-id="54122-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="54122-108">Identifier:</span></span>  <br/> |<span data-ttu-id="54122-109">0x1080</span><span class="sxs-lookup"><span data-stu-id="54122-109">0x1080</span></span>  <br/> |
|<span data-ttu-id="54122-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="54122-110">Data type:</span></span>  <br/> |<span data-ttu-id="54122-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="54122-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="54122-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="54122-112">Area:</span></span>  <br/> |<span data-ttu-id="54122-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="54122-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54122-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54122-114">Remarks</span></span>

<span data-ttu-id="54122-115">Diese Eigenschaft, ist wenn es vorhanden ist, ein Hinweis an den Client.</span><span class="sxs-lookup"><span data-stu-id="54122-115">This property, if it exists, is a hint to the client.</span></span> <span data-ttu-id="54122-116">Der Client kann den Wert dieser Eigenschaft ignoriert.</span><span class="sxs-lookup"><span data-stu-id="54122-116">The client may ignore the value of this property.</span></span> 
  
|<span data-ttu-id="54122-117">**E-Mail-Element state**</span><span class="sxs-lookup"><span data-stu-id="54122-117">**Mail item state**</span></span>|<span data-ttu-id="54122-118">**Symbol-Index**</span><span class="sxs-lookup"><span data-stu-id="54122-118">**Icon Index**</span></span>|
|:-----|:-----|
|<span data-ttu-id="54122-119">Neue e-Mail-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="54122-119">New mail</span></span>  <br/> |<span data-ttu-id="54122-120">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="54122-120">0xFFFFFFFF</span></span>  <br/> |
|<span data-ttu-id="54122-121">Beitrag</span><span class="sxs-lookup"><span data-stu-id="54122-121">Post</span></span>  <br/> |<span data-ttu-id="54122-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="54122-122">0x00000001</span></span>  <br/> |
|<span data-ttu-id="54122-123">Andere</span><span class="sxs-lookup"><span data-stu-id="54122-123">Other</span></span>  <br/> |<span data-ttu-id="54122-124">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="54122-124">0x00000003</span></span>  <br/> |
|<span data-ttu-id="54122-125">E-Mail lesen</span><span class="sxs-lookup"><span data-stu-id="54122-125">Read mail</span></span>  <br/> |<span data-ttu-id="54122-126">0 x 00000100</span><span class="sxs-lookup"><span data-stu-id="54122-126">0x00000100</span></span>  <br/> |
|<span data-ttu-id="54122-127">Ungelesene Nachrichten</span><span class="sxs-lookup"><span data-stu-id="54122-127">Unread mail</span></span>  <br/> |<span data-ttu-id="54122-128">0x00000101</span><span class="sxs-lookup"><span data-stu-id="54122-128">0x00000101</span></span>  <br/> |
|<span data-ttu-id="54122-129">Gesendete e-Mail</span><span class="sxs-lookup"><span data-stu-id="54122-129">Submitted mail</span></span>  <br/> |<span data-ttu-id="54122-130">0x00000102</span><span class="sxs-lookup"><span data-stu-id="54122-130">0x00000102</span></span>  <br/> |
|<span data-ttu-id="54122-131">Nicht gesendeten Nachrichten</span><span class="sxs-lookup"><span data-stu-id="54122-131">Unsent mail</span></span>  <br/> |<span data-ttu-id="54122-132">0x00000103</span><span class="sxs-lookup"><span data-stu-id="54122-132">0x00000103</span></span>  <br/> |
|<span data-ttu-id="54122-133">Bestätigung e-Mail</span><span class="sxs-lookup"><span data-stu-id="54122-133">Receipt mail</span></span>  <br/> |<span data-ttu-id="54122-134">0x00000104</span><span class="sxs-lookup"><span data-stu-id="54122-134">0x00000104</span></span>  <br/> |
|<span data-ttu-id="54122-135">Beantwortete</span><span class="sxs-lookup"><span data-stu-id="54122-135">Replied mail</span></span>  <br/> |<span data-ttu-id="54122-136">0x00000105</span><span class="sxs-lookup"><span data-stu-id="54122-136">0x00000105</span></span>  <br/> |
|<span data-ttu-id="54122-137">Weitergeleitete e-Mail-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="54122-137">Forwarded mail</span></span>  <br/> |<span data-ttu-id="54122-138">0x00000106</span><span class="sxs-lookup"><span data-stu-id="54122-138">0x00000106</span></span>  <br/> |
|<span data-ttu-id="54122-139">Remote-mail</span><span class="sxs-lookup"><span data-stu-id="54122-139">Remote mail</span></span>  <br/> |<span data-ttu-id="54122-140">0x00000107</span><span class="sxs-lookup"><span data-stu-id="54122-140">0x00000107</span></span>  <br/> |
|<span data-ttu-id="54122-141">Übermittlung mail</span><span class="sxs-lookup"><span data-stu-id="54122-141">Delivery mail</span></span>  <br/> |<span data-ttu-id="54122-142">0x00000108</span><span class="sxs-lookup"><span data-stu-id="54122-142">0x00000108</span></span>  <br/> |
|<span data-ttu-id="54122-143">E-Mail lesen</span><span class="sxs-lookup"><span data-stu-id="54122-143">Read mail</span></span>  <br/> |<span data-ttu-id="54122-144">0x00000109</span><span class="sxs-lookup"><span data-stu-id="54122-144">0x00000109</span></span>  <br/> |
|<span data-ttu-id="54122-145">NonDelivery mail</span><span class="sxs-lookup"><span data-stu-id="54122-145">Nondelivery mail</span></span>  <br/> |<span data-ttu-id="54122-146">0x0000010A</span><span class="sxs-lookup"><span data-stu-id="54122-146">0x0000010A</span></span>  <br/> |
|<span data-ttu-id="54122-147">Nonread mail</span><span class="sxs-lookup"><span data-stu-id="54122-147">Nonread mail</span></span>  <br/> |<span data-ttu-id="54122-148">0x0000010B</span><span class="sxs-lookup"><span data-stu-id="54122-148">0x0000010B</span></span>  <br/> |
|<span data-ttu-id="54122-149">Recall_S mail</span><span class="sxs-lookup"><span data-stu-id="54122-149">Recall_S mail</span></span>  <br/> |<span data-ttu-id="54122-150">0x0000010C</span><span class="sxs-lookup"><span data-stu-id="54122-150">0x0000010C</span></span>  <br/> |
|<span data-ttu-id="54122-151">Recall_F mail</span><span class="sxs-lookup"><span data-stu-id="54122-151">Recall_F mail</span></span>  <br/> |<span data-ttu-id="54122-152">0x0000010D</span><span class="sxs-lookup"><span data-stu-id="54122-152">0x0000010D</span></span>  <br/> |
|<span data-ttu-id="54122-153">Nachverfolgen von e-Mail-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="54122-153">Tracking mail</span></span>  <br/> |<span data-ttu-id="54122-154">0x0000010E</span><span class="sxs-lookup"><span data-stu-id="54122-154">0x0000010E</span></span>  <br/> |
|<span data-ttu-id="54122-155">Nicht genügend Office mail</span><span class="sxs-lookup"><span data-stu-id="54122-155">Out of office mail</span></span>  <br/> |<span data-ttu-id="54122-156">0x0000011B</span><span class="sxs-lookup"><span data-stu-id="54122-156">0x0000011B</span></span>  <br/> |
|<span data-ttu-id="54122-157">Zurückrufen mail</span><span class="sxs-lookup"><span data-stu-id="54122-157">Recall mail</span></span>  <br/> |<span data-ttu-id="54122-158">0x0000011C</span><span class="sxs-lookup"><span data-stu-id="54122-158">0x0000011C</span></span>  <br/> |
|<span data-ttu-id="54122-159">Nachverfolgte e-Mail</span><span class="sxs-lookup"><span data-stu-id="54122-159">Tracked mail</span></span>  <br/> |<span data-ttu-id="54122-160">0x00000130</span><span class="sxs-lookup"><span data-stu-id="54122-160">0x00000130</span></span>  <br/> |
|<span data-ttu-id="54122-161">Kontakt</span><span class="sxs-lookup"><span data-stu-id="54122-161">Contact</span></span>  <br/> |<span data-ttu-id="54122-162">0 x 00000200</span><span class="sxs-lookup"><span data-stu-id="54122-162">0x00000200</span></span>  <br/> |
|<span data-ttu-id="54122-163">Verteilerliste</span><span class="sxs-lookup"><span data-stu-id="54122-163">Distribution list</span></span>  <br/> |<span data-ttu-id="54122-164">0x00000202</span><span class="sxs-lookup"><span data-stu-id="54122-164">0x00000202</span></span>  <br/> |
|<span data-ttu-id="54122-165">Kurznotiz-Blau</span><span class="sxs-lookup"><span data-stu-id="54122-165">Sticky note blue</span></span>  <br/> |<span data-ttu-id="54122-166">0x00000300</span><span class="sxs-lookup"><span data-stu-id="54122-166">0x00000300</span></span>  <br/> |
|<span data-ttu-id="54122-167">Kurznotiz Grün</span><span class="sxs-lookup"><span data-stu-id="54122-167">Sticky note green</span></span>  <br/> |<span data-ttu-id="54122-168">0x00000301</span><span class="sxs-lookup"><span data-stu-id="54122-168">0x00000301</span></span>  <br/> |
|<span data-ttu-id="54122-169">Kurznotiz rosa</span><span class="sxs-lookup"><span data-stu-id="54122-169">Sticky note pink</span></span>  <br/> |<span data-ttu-id="54122-170">0x00000302</span><span class="sxs-lookup"><span data-stu-id="54122-170">0x00000302</span></span>  <br/> |
|<span data-ttu-id="54122-171">Kurznotiz Gelb</span><span class="sxs-lookup"><span data-stu-id="54122-171">Sticky note yellow</span></span>  <br/> |<span data-ttu-id="54122-172">0x00000303</span><span class="sxs-lookup"><span data-stu-id="54122-172">0x00000303</span></span>  <br/> |
|<span data-ttu-id="54122-173">Kurznotiz weiß</span><span class="sxs-lookup"><span data-stu-id="54122-173">Sticky note white</span></span>  <br/> |<span data-ttu-id="54122-174">0x00000304</span><span class="sxs-lookup"><span data-stu-id="54122-174">0x00000304</span></span>  <br/> |
|<span data-ttu-id="54122-175">Einzelne Instanz eines Termins</span><span class="sxs-lookup"><span data-stu-id="54122-175">Single instance appointment</span></span>  <br/> |<span data-ttu-id="54122-176">0 x 00000400</span><span class="sxs-lookup"><span data-stu-id="54122-176">0x00000400</span></span>  <br/> |
|<span data-ttu-id="54122-177">Terminserie</span><span class="sxs-lookup"><span data-stu-id="54122-177">Recurring appointment</span></span>  <br/> |<span data-ttu-id="54122-178">0x00000401</span><span class="sxs-lookup"><span data-stu-id="54122-178">0x00000401</span></span>  <br/> |
|<span data-ttu-id="54122-179">Einzelinstanz-Besprechung</span><span class="sxs-lookup"><span data-stu-id="54122-179">Single instance meeting</span></span>  <br/> |<span data-ttu-id="54122-180">0x00000402</span><span class="sxs-lookup"><span data-stu-id="54122-180">0x00000402</span></span>  <br/> |
|<span data-ttu-id="54122-181">Wiederkehrende Besprechung</span><span class="sxs-lookup"><span data-stu-id="54122-181">Recurring meeting</span></span>  <br/> |<span data-ttu-id="54122-182">0x00000403</span><span class="sxs-lookup"><span data-stu-id="54122-182">0x00000403</span></span>  <br/> |
|<span data-ttu-id="54122-183">Besprechungsanfrage</span><span class="sxs-lookup"><span data-stu-id="54122-183">Meeting request</span></span>  <br/> |<span data-ttu-id="54122-184">0 x 00000404</span><span class="sxs-lookup"><span data-stu-id="54122-184">0x00000404</span></span>  <br/> |
|<span data-ttu-id="54122-185">Annehmen</span><span class="sxs-lookup"><span data-stu-id="54122-185">Accept</span></span>  <br/> |<span data-ttu-id="54122-186">0x00000405</span><span class="sxs-lookup"><span data-stu-id="54122-186">0x00000405</span></span>  <br/> |
|<span data-ttu-id="54122-187">Ablehnen</span><span class="sxs-lookup"><span data-stu-id="54122-187">Decline</span></span>  <br/> |<span data-ttu-id="54122-188">0x00000406</span><span class="sxs-lookup"><span data-stu-id="54122-188">0x00000406</span></span>  <br/> |
|<span data-ttu-id="54122-189">Tentativly</span><span class="sxs-lookup"><span data-stu-id="54122-189">Tentativly</span></span>  <br/> |<span data-ttu-id="54122-190">0 x 00000407</span><span class="sxs-lookup"><span data-stu-id="54122-190">0x00000407</span></span>  <br/> |
|<span data-ttu-id="54122-191">Stornierung</span><span class="sxs-lookup"><span data-stu-id="54122-191">Cancellation</span></span>  <br/> |<span data-ttu-id="54122-192">0x00000408</span><span class="sxs-lookup"><span data-stu-id="54122-192">0x00000408</span></span>  <br/> |
|<span data-ttu-id="54122-193">Informative update</span><span class="sxs-lookup"><span data-stu-id="54122-193">Informational update</span></span>  <br/> |<span data-ttu-id="54122-194">0 x 00000409</span><span class="sxs-lookup"><span data-stu-id="54122-194">0x00000409</span></span>  <br/> |
|<span data-ttu-id="54122-195">Aufgabe/Aufgabe</span><span class="sxs-lookup"><span data-stu-id="54122-195">Task/task</span></span>  <br/> |<span data-ttu-id="54122-196">0x00000500</span><span class="sxs-lookup"><span data-stu-id="54122-196">0x00000500</span></span>  <br/> |
|<span data-ttu-id="54122-197">Nicht zugewiesene Aufgabenserie</span><span class="sxs-lookup"><span data-stu-id="54122-197">Unassigned recurring task</span></span>  <br/> |<span data-ttu-id="54122-198">0x00000501</span><span class="sxs-lookup"><span data-stu-id="54122-198">0x00000501</span></span>  <br/> |
|<span data-ttu-id="54122-199">Benutzer, dem die Aufgabe</span><span class="sxs-lookup"><span data-stu-id="54122-199">Assignee's task</span></span>  <br/> |<span data-ttu-id="54122-200">0x00000502</span><span class="sxs-lookup"><span data-stu-id="54122-200">0x00000502</span></span>  <br/> |
|<span data-ttu-id="54122-201">Aufgabe des delegierende Person</span><span class="sxs-lookup"><span data-stu-id="54122-201">Assigner's task</span></span>  <br/> |<span data-ttu-id="54122-202">0x00000503</span><span class="sxs-lookup"><span data-stu-id="54122-202">0x00000503</span></span>  <br/> |
|<span data-ttu-id="54122-203">Aufgabenanfrage</span><span class="sxs-lookup"><span data-stu-id="54122-203">Task request</span></span>  <br/> |<span data-ttu-id="54122-204">0x00000504</span><span class="sxs-lookup"><span data-stu-id="54122-204">0x00000504</span></span>  <br/> |
|<span data-ttu-id="54122-205">Annahme der Aufgabe</span><span class="sxs-lookup"><span data-stu-id="54122-205">Task acceptance</span></span>  <br/> |<span data-ttu-id="54122-206">0x00000505</span><span class="sxs-lookup"><span data-stu-id="54122-206">0x00000505</span></span>  <br/> |
|<span data-ttu-id="54122-207">Aufgabe Ablehnung</span><span class="sxs-lookup"><span data-stu-id="54122-207">Task rejection</span></span>  <br/> |<span data-ttu-id="54122-208">0x00000506</span><span class="sxs-lookup"><span data-stu-id="54122-208">0x00000506</span></span>  <br/> |
|<span data-ttu-id="54122-209">Journal-Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="54122-209">Journal conversation</span></span>  <br/> |<span data-ttu-id="54122-210">0x00000601</span><span class="sxs-lookup"><span data-stu-id="54122-210">0x00000601</span></span>  <br/> |
|<span data-ttu-id="54122-211">Journal-e-Mail-Nachricht</span><span class="sxs-lookup"><span data-stu-id="54122-211">Journal email message</span></span>  <br/> |<span data-ttu-id="54122-212">0x00000602</span><span class="sxs-lookup"><span data-stu-id="54122-212">0x00000602</span></span>  <br/> |
|<span data-ttu-id="54122-213">Journal-Besprechungsanfrage</span><span class="sxs-lookup"><span data-stu-id="54122-213">Journal meeting request</span></span>  <br/> |<span data-ttu-id="54122-214">0x00000603</span><span class="sxs-lookup"><span data-stu-id="54122-214">0x00000603</span></span>  <br/> |
|<span data-ttu-id="54122-215">Journal Besprechungsantwort</span><span class="sxs-lookup"><span data-stu-id="54122-215">Journal meeting response</span></span>  <br/> |<span data-ttu-id="54122-216">0x00000604</span><span class="sxs-lookup"><span data-stu-id="54122-216">0x00000604</span></span>  <br/> |
|<span data-ttu-id="54122-217">Journal Aufgabenanfrage</span><span class="sxs-lookup"><span data-stu-id="54122-217">Journal task request</span></span>  <br/> |<span data-ttu-id="54122-218">0x00000606</span><span class="sxs-lookup"><span data-stu-id="54122-218">0x00000606</span></span>  <br/> |
|<span data-ttu-id="54122-219">Journal Aufgabenantwort</span><span class="sxs-lookup"><span data-stu-id="54122-219">Journal task response</span></span>  <br/> |<span data-ttu-id="54122-220">0x00000607</span><span class="sxs-lookup"><span data-stu-id="54122-220">0x00000607</span></span>  <br/> |
|<span data-ttu-id="54122-221">Journal-Notiz</span><span class="sxs-lookup"><span data-stu-id="54122-221">Journal note</span></span>  <br/> |<span data-ttu-id="54122-222">0x00000608</span><span class="sxs-lookup"><span data-stu-id="54122-222">0x00000608</span></span>  <br/> |
|<span data-ttu-id="54122-223">Journal fax</span><span class="sxs-lookup"><span data-stu-id="54122-223">Journal fax</span></span>  <br/> |<span data-ttu-id="54122-224">0x00000609</span><span class="sxs-lookup"><span data-stu-id="54122-224">0x00000609</span></span>  <br/> |
|<span data-ttu-id="54122-225">Journal Telefonanrufs</span><span class="sxs-lookup"><span data-stu-id="54122-225">Journal phone call</span></span>  <br/> |<span data-ttu-id="54122-226">0x0000060A</span><span class="sxs-lookup"><span data-stu-id="54122-226">0x0000060A</span></span>  <br/> |
|<span data-ttu-id="54122-227">Journal Buchstabe</span><span class="sxs-lookup"><span data-stu-id="54122-227">Journal letter</span></span>  <br/> |<span data-ttu-id="54122-228">0x0000060C</span><span class="sxs-lookup"><span data-stu-id="54122-228">0x0000060C</span></span>  <br/> |
|<span data-ttu-id="54122-229">Journal Microsoft Office Word</span><span class="sxs-lookup"><span data-stu-id="54122-229">Journal Microsoft Office Word</span></span>  <br/> |<span data-ttu-id="54122-230">0x0000060D</span><span class="sxs-lookup"><span data-stu-id="54122-230">0x0000060D</span></span>  <br/> |
|<span data-ttu-id="54122-231">Journal Microsoft Office Excel</span><span class="sxs-lookup"><span data-stu-id="54122-231">Journal Microsoft Office Excel</span></span>  <br/> |<span data-ttu-id="54122-232">0x0000060E</span><span class="sxs-lookup"><span data-stu-id="54122-232">0x0000060E</span></span>  <br/> |
|<span data-ttu-id="54122-233">Journal Microsoft Office PowerPoint</span><span class="sxs-lookup"><span data-stu-id="54122-233">Journal Microsoft Office PowerPoint</span></span>  <br/> |<span data-ttu-id="54122-234">0x0000060F</span><span class="sxs-lookup"><span data-stu-id="54122-234">0x0000060F</span></span>  <br/> |
|<span data-ttu-id="54122-235">Journal Microsoft Office Access</span><span class="sxs-lookup"><span data-stu-id="54122-235">Journal Microsoft Office Access</span></span>  <br/> |<span data-ttu-id="54122-236">0x00000610</span><span class="sxs-lookup"><span data-stu-id="54122-236">0x00000610</span></span>  <br/> |
|<span data-ttu-id="54122-237">Journal-Dokument</span><span class="sxs-lookup"><span data-stu-id="54122-237">Journal document</span></span>  <br/> |<span data-ttu-id="54122-238">0x00000612</span><span class="sxs-lookup"><span data-stu-id="54122-238">0x00000612</span></span>  <br/> |
|<span data-ttu-id="54122-239">Journal-Besprechung</span><span class="sxs-lookup"><span data-stu-id="54122-239">Journal meeting</span></span>  <br/> |<span data-ttu-id="54122-240">0x00000613</span><span class="sxs-lookup"><span data-stu-id="54122-240">0x00000613</span></span>  <br/> |
|<span data-ttu-id="54122-241">Journal Besprechungsabsage</span><span class="sxs-lookup"><span data-stu-id="54122-241">Journal meeting cancellation</span></span>  <br/> |<span data-ttu-id="54122-242">0x00000614</span><span class="sxs-lookup"><span data-stu-id="54122-242">0x00000614</span></span>  <br/> |
|<span data-ttu-id="54122-243">Journal-Remotesitzung</span><span class="sxs-lookup"><span data-stu-id="54122-243">Journal remote session</span></span>  <br/> |<span data-ttu-id="54122-244">0x00000615</span><span class="sxs-lookup"><span data-stu-id="54122-244">0x00000615</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="54122-245">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="54122-245">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="54122-246">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="54122-246">Protocol specifications</span></span>

<span data-ttu-id="54122-247">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="54122-247">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="54122-248">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="54122-248">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="54122-249">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="54122-249">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="54122-250">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="54122-250">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="54122-251">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="54122-251">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="54122-252">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="54122-252">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="54122-253">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="54122-253">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="54122-254">Gibt die Eigenschaften und Operationen, die auf Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="54122-254">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="54122-255">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="54122-255">Header files</span></span>

<span data-ttu-id="54122-256">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="54122-256">Mapidefs.h</span></span>
  
> <span data-ttu-id="54122-257">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="54122-257">Provides data type definitions.</span></span>
    
<span data-ttu-id="54122-258">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="54122-258">Mapitags.h</span></span>
  
> <span data-ttu-id="54122-259">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="54122-259">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="54122-260">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54122-260">See also</span></span>



[<span data-ttu-id="54122-261">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="54122-261">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="54122-262">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="54122-262">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="54122-263">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="54122-263">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="54122-264">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="54122-264">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

