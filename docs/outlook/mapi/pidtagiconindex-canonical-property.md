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
ms.openlocfilehash: 35d9d0a50539f8aab2d26730dd4e4544c2535e60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346620"
---
# <a name="pidtagiconindex-canonical-property"></a><span data-ttu-id="ea324-103">PidTagIconIndex (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ea324-103">PidTagIconIndex Canonical Property</span></span>

  
  
<span data-ttu-id="ea324-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea324-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea324-105">Enthält eine Zahl, die angibt, welches Symbol beim Anzeigen einer Gruppe von E-Mail-Objekten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ea324-105">Contains a number that indicates which icon to use when you display a group of email objects.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ea324-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ea324-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ea324-107">PR_ICON_INDEX</span><span class="sxs-lookup"><span data-stu-id="ea324-107">PR_ICON_INDEX</span></span>  <br/> |
|<span data-ttu-id="ea324-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="ea324-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ea324-109">0x1080</span><span class="sxs-lookup"><span data-stu-id="ea324-109">0x1080</span></span>  <br/> |
|<span data-ttu-id="ea324-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ea324-110">Data type:</span></span>  <br/> |<span data-ttu-id="ea324-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ea324-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ea324-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ea324-112">Area:</span></span>  <br/> |<span data-ttu-id="ea324-113">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="ea324-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ea324-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ea324-114">Remarks</span></span>

<span data-ttu-id="ea324-115">Diese Eigenschaft ist, falls vorhanden, ein Hinweis an den Client.</span><span class="sxs-lookup"><span data-stu-id="ea324-115">This property, if it exists, is a hint to the client.</span></span> <span data-ttu-id="ea324-116">Der Client kann den Wert dieser Eigenschaft ignorieren.</span><span class="sxs-lookup"><span data-stu-id="ea324-116">The client may ignore the value of this property.</span></span> 
  
|<span data-ttu-id="ea324-117">**E-Mail-Elementstatus**</span><span class="sxs-lookup"><span data-stu-id="ea324-117">**Mail item state**</span></span>|<span data-ttu-id="ea324-118">**Symbolindex**</span><span class="sxs-lookup"><span data-stu-id="ea324-118">**Icon Index**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ea324-119">Neue E-Mails</span><span class="sxs-lookup"><span data-stu-id="ea324-119">New mail</span></span>  <br/> |<span data-ttu-id="ea324-120">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="ea324-120">0xFFFFFFFF</span></span>  <br/> |
|<span data-ttu-id="ea324-121">Beitrag</span><span class="sxs-lookup"><span data-stu-id="ea324-121">Post</span></span>  <br/> |<span data-ttu-id="ea324-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ea324-122">0x00000001</span></span>  <br/> |
|<span data-ttu-id="ea324-123">Andere</span><span class="sxs-lookup"><span data-stu-id="ea324-123">Other</span></span>  <br/> |<span data-ttu-id="ea324-124">0x00000003</span><span class="sxs-lookup"><span data-stu-id="ea324-124">0x00000003</span></span>  <br/> |
|<span data-ttu-id="ea324-125">Lesen von E-Mails</span><span class="sxs-lookup"><span data-stu-id="ea324-125">Read mail</span></span>  <br/> |<span data-ttu-id="ea324-126">0x00000100</span><span class="sxs-lookup"><span data-stu-id="ea324-126">0x00000100</span></span>  <br/> |
|<span data-ttu-id="ea324-127">Ungelesene E-Mails</span><span class="sxs-lookup"><span data-stu-id="ea324-127">Unread mail</span></span>  <br/> |<span data-ttu-id="ea324-128">0x00000101</span><span class="sxs-lookup"><span data-stu-id="ea324-128">0x00000101</span></span>  <br/> |
|<span data-ttu-id="ea324-129">Gesendete E-Mails</span><span class="sxs-lookup"><span data-stu-id="ea324-129">Submitted mail</span></span>  <br/> |<span data-ttu-id="ea324-130">0x00000102</span><span class="sxs-lookup"><span data-stu-id="ea324-130">0x00000102</span></span>  <br/> |
|<span data-ttu-id="ea324-131">Nicht gesendete E-Mails</span><span class="sxs-lookup"><span data-stu-id="ea324-131">Unsent mail</span></span>  <br/> |<span data-ttu-id="ea324-132">0x00000103</span><span class="sxs-lookup"><span data-stu-id="ea324-132">0x00000103</span></span>  <br/> |
|<span data-ttu-id="ea324-133">Empfangsmail</span><span class="sxs-lookup"><span data-stu-id="ea324-133">Receipt mail</span></span>  <br/> |<span data-ttu-id="ea324-134">0x00000104</span><span class="sxs-lookup"><span data-stu-id="ea324-134">0x00000104</span></span>  <br/> |
|<span data-ttu-id="ea324-135">Beantwortete E-Mails</span><span class="sxs-lookup"><span data-stu-id="ea324-135">Replied mail</span></span>  <br/> |<span data-ttu-id="ea324-136">0x00000105</span><span class="sxs-lookup"><span data-stu-id="ea324-136">0x00000105</span></span>  <br/> |
|<span data-ttu-id="ea324-137">Weitergeleitete E-Mails</span><span class="sxs-lookup"><span data-stu-id="ea324-137">Forwarded mail</span></span>  <br/> |<span data-ttu-id="ea324-138">0x00000106</span><span class="sxs-lookup"><span data-stu-id="ea324-138">0x00000106</span></span>  <br/> |
|<span data-ttu-id="ea324-139">Remote-E-Mail</span><span class="sxs-lookup"><span data-stu-id="ea324-139">Remote mail</span></span>  <br/> |<span data-ttu-id="ea324-140">0x00000107</span><span class="sxs-lookup"><span data-stu-id="ea324-140">0x00000107</span></span>  <br/> |
|<span data-ttu-id="ea324-141">Zustellungs-E-Mails</span><span class="sxs-lookup"><span data-stu-id="ea324-141">Delivery mail</span></span>  <br/> |<span data-ttu-id="ea324-142">0x00000108</span><span class="sxs-lookup"><span data-stu-id="ea324-142">0x00000108</span></span>  <br/> |
|<span data-ttu-id="ea324-143">Lesen von E-Mails</span><span class="sxs-lookup"><span data-stu-id="ea324-143">Read mail</span></span>  <br/> |<span data-ttu-id="ea324-144">0x00000109</span><span class="sxs-lookup"><span data-stu-id="ea324-144">0x00000109</span></span>  <br/> |
|<span data-ttu-id="ea324-145">Nondelivery-E-Mails</span><span class="sxs-lookup"><span data-stu-id="ea324-145">Nondelivery mail</span></span>  <br/> |<span data-ttu-id="ea324-146">0x0000010A</span><span class="sxs-lookup"><span data-stu-id="ea324-146">0x0000010A</span></span>  <br/> |
|<span data-ttu-id="ea324-147">Nicht gelesene E-Mails</span><span class="sxs-lookup"><span data-stu-id="ea324-147">Nonread mail</span></span>  <br/> |<span data-ttu-id="ea324-148">0x0000010B</span><span class="sxs-lookup"><span data-stu-id="ea324-148">0x0000010B</span></span>  <br/> |
|<span data-ttu-id="ea324-149">Recall_S E-Mail</span><span class="sxs-lookup"><span data-stu-id="ea324-149">Recall_S mail</span></span>  <br/> |<span data-ttu-id="ea324-150">0x0000010C</span><span class="sxs-lookup"><span data-stu-id="ea324-150">0x0000010C</span></span>  <br/> |
|<span data-ttu-id="ea324-151">Recall_F E-Mail</span><span class="sxs-lookup"><span data-stu-id="ea324-151">Recall_F mail</span></span>  <br/> |<span data-ttu-id="ea324-152">0x0000010D</span><span class="sxs-lookup"><span data-stu-id="ea324-152">0x0000010D</span></span>  <br/> |
|<span data-ttu-id="ea324-153">Nachverfolgen von E-Mails</span><span class="sxs-lookup"><span data-stu-id="ea324-153">Tracking mail</span></span>  <br/> |<span data-ttu-id="ea324-154">0x0000010E</span><span class="sxs-lookup"><span data-stu-id="ea324-154">0x0000010E</span></span>  <br/> |
|<span data-ttu-id="ea324-155">Out-of-Office-E-Mails</span><span class="sxs-lookup"><span data-stu-id="ea324-155">Out of office mail</span></span>  <br/> |<span data-ttu-id="ea324-156">0x0000011B</span><span class="sxs-lookup"><span data-stu-id="ea324-156">0x0000011B</span></span>  <br/> |
|<span data-ttu-id="ea324-157">Rückruf von E-Mails</span><span class="sxs-lookup"><span data-stu-id="ea324-157">Recall mail</span></span>  <br/> |<span data-ttu-id="ea324-158">0x0000011C</span><span class="sxs-lookup"><span data-stu-id="ea324-158">0x0000011C</span></span>  <br/> |
|<span data-ttu-id="ea324-159">Nachverfolgte E-Mails</span><span class="sxs-lookup"><span data-stu-id="ea324-159">Tracked mail</span></span>  <br/> |<span data-ttu-id="ea324-160">0x00000130</span><span class="sxs-lookup"><span data-stu-id="ea324-160">0x00000130</span></span>  <br/> |
|<span data-ttu-id="ea324-161">Kontakt</span><span class="sxs-lookup"><span data-stu-id="ea324-161">Contact</span></span>  <br/> |<span data-ttu-id="ea324-162">0x00000200</span><span class="sxs-lookup"><span data-stu-id="ea324-162">0x00000200</span></span>  <br/> |
|<span data-ttu-id="ea324-163">Verteilerliste</span><span class="sxs-lookup"><span data-stu-id="ea324-163">Distribution list</span></span>  <br/> |<span data-ttu-id="ea324-164">0x00000202</span><span class="sxs-lookup"><span data-stu-id="ea324-164">0x00000202</span></span>  <br/> |
|<span data-ttu-id="ea324-165">Sticky note blue</span><span class="sxs-lookup"><span data-stu-id="ea324-165">Sticky note blue</span></span>  <br/> |<span data-ttu-id="ea324-166">0x00000300</span><span class="sxs-lookup"><span data-stu-id="ea324-166">0x00000300</span></span>  <br/> |
|<span data-ttu-id="ea324-167">Sticky note green</span><span class="sxs-lookup"><span data-stu-id="ea324-167">Sticky note green</span></span>  <br/> |<span data-ttu-id="ea324-168">0x00000301</span><span class="sxs-lookup"><span data-stu-id="ea324-168">0x00000301</span></span>  <br/> |
|<span data-ttu-id="ea324-169">Sticky note pink</span><span class="sxs-lookup"><span data-stu-id="ea324-169">Sticky note pink</span></span>  <br/> |<span data-ttu-id="ea324-170">0x00000302</span><span class="sxs-lookup"><span data-stu-id="ea324-170">0x00000302</span></span>  <br/> |
|<span data-ttu-id="ea324-171">Klebenotiz gelb</span><span class="sxs-lookup"><span data-stu-id="ea324-171">Sticky note yellow</span></span>  <br/> |<span data-ttu-id="ea324-172">0x00000303</span><span class="sxs-lookup"><span data-stu-id="ea324-172">0x00000303</span></span>  <br/> |
|<span data-ttu-id="ea324-173">Klebenotiz weiß</span><span class="sxs-lookup"><span data-stu-id="ea324-173">Sticky note white</span></span>  <br/> |<span data-ttu-id="ea324-174">0x00000304</span><span class="sxs-lookup"><span data-stu-id="ea324-174">0x00000304</span></span>  <br/> |
|<span data-ttu-id="ea324-175">Termin für eine einzelne Instanz</span><span class="sxs-lookup"><span data-stu-id="ea324-175">Single instance appointment</span></span>  <br/> |<span data-ttu-id="ea324-176">0x00000400</span><span class="sxs-lookup"><span data-stu-id="ea324-176">0x00000400</span></span>  <br/> |
|<span data-ttu-id="ea324-177">Terminserie</span><span class="sxs-lookup"><span data-stu-id="ea324-177">Recurring appointment</span></span>  <br/> |<span data-ttu-id="ea324-178">0x00000401</span><span class="sxs-lookup"><span data-stu-id="ea324-178">0x00000401</span></span>  <br/> |
|<span data-ttu-id="ea324-179">Besprechung mit einer instanz</span><span class="sxs-lookup"><span data-stu-id="ea324-179">Single instance meeting</span></span>  <br/> |<span data-ttu-id="ea324-180">0x00000402</span><span class="sxs-lookup"><span data-stu-id="ea324-180">0x00000402</span></span>  <br/> |
|<span data-ttu-id="ea324-181">Besprechungsserie:</span><span class="sxs-lookup"><span data-stu-id="ea324-181">Recurring meeting</span></span>  <br/> |<span data-ttu-id="ea324-182">0x00000403</span><span class="sxs-lookup"><span data-stu-id="ea324-182">0x00000403</span></span>  <br/> |
|<span data-ttu-id="ea324-183">Besprechungsanfrage</span><span class="sxs-lookup"><span data-stu-id="ea324-183">Meeting request</span></span>  <br/> |<span data-ttu-id="ea324-184">0x00000404</span><span class="sxs-lookup"><span data-stu-id="ea324-184">0x00000404</span></span>  <br/> |
|<span data-ttu-id="ea324-185">Annehmen</span><span class="sxs-lookup"><span data-stu-id="ea324-185">Accept</span></span>  <br/> |<span data-ttu-id="ea324-186">0x00000405</span><span class="sxs-lookup"><span data-stu-id="ea324-186">0x00000405</span></span>  <br/> |
|<span data-ttu-id="ea324-187">Decline</span><span class="sxs-lookup"><span data-stu-id="ea324-187">Decline</span></span>  <br/> |<span data-ttu-id="ea324-188">0x00000406</span><span class="sxs-lookup"><span data-stu-id="ea324-188">0x00000406</span></span>  <br/> |
|<span data-ttu-id="ea324-189">Tentativ</span><span class="sxs-lookup"><span data-stu-id="ea324-189">Tentativly</span></span>  <br/> |<span data-ttu-id="ea324-190">0x00000407</span><span class="sxs-lookup"><span data-stu-id="ea324-190">0x00000407</span></span>  <br/> |
|<span data-ttu-id="ea324-191">Stornierung</span><span class="sxs-lookup"><span data-stu-id="ea324-191">Cancellation</span></span>  <br/> |<span data-ttu-id="ea324-192">0x00000408</span><span class="sxs-lookup"><span data-stu-id="ea324-192">0x00000408</span></span>  <br/> |
|<span data-ttu-id="ea324-193">Informationsupdate</span><span class="sxs-lookup"><span data-stu-id="ea324-193">Informational update</span></span>  <br/> |<span data-ttu-id="ea324-194">0x00000409</span><span class="sxs-lookup"><span data-stu-id="ea324-194">0x00000409</span></span>  <br/> |
|<span data-ttu-id="ea324-195">Aufgabe/Aufgabe</span><span class="sxs-lookup"><span data-stu-id="ea324-195">Task/task</span></span>  <br/> |<span data-ttu-id="ea324-196">0x00000500</span><span class="sxs-lookup"><span data-stu-id="ea324-196">0x00000500</span></span>  <br/> |
|<span data-ttu-id="ea324-197">Nicht zugewiesene Wiederkehrende Aufgabe</span><span class="sxs-lookup"><span data-stu-id="ea324-197">Unassigned recurring task</span></span>  <br/> |<span data-ttu-id="ea324-198">0x00000501</span><span class="sxs-lookup"><span data-stu-id="ea324-198">0x00000501</span></span>  <br/> |
|<span data-ttu-id="ea324-199">Aufgabe des Assignee</span><span class="sxs-lookup"><span data-stu-id="ea324-199">Assignee's task</span></span>  <br/> |<span data-ttu-id="ea324-200">0x00000502</span><span class="sxs-lookup"><span data-stu-id="ea324-200">0x00000502</span></span>  <br/> |
|<span data-ttu-id="ea324-201">Aufgabe des Assigners</span><span class="sxs-lookup"><span data-stu-id="ea324-201">Assigner's task</span></span>  <br/> |<span data-ttu-id="ea324-202">0x00000503</span><span class="sxs-lookup"><span data-stu-id="ea324-202">0x00000503</span></span>  <br/> |
|<span data-ttu-id="ea324-203">Aufgabenanforderung</span><span class="sxs-lookup"><span data-stu-id="ea324-203">Task request</span></span>  <br/> |<span data-ttu-id="ea324-204">0x00000504</span><span class="sxs-lookup"><span data-stu-id="ea324-204">0x00000504</span></span>  <br/> |
|<span data-ttu-id="ea324-205">Aufgabenakzeptanz</span><span class="sxs-lookup"><span data-stu-id="ea324-205">Task acceptance</span></span>  <br/> |<span data-ttu-id="ea324-206">0x00000505</span><span class="sxs-lookup"><span data-stu-id="ea324-206">0x00000505</span></span>  <br/> |
|<span data-ttu-id="ea324-207">Vorgangsverweigerung</span><span class="sxs-lookup"><span data-stu-id="ea324-207">Task rejection</span></span>  <br/> |<span data-ttu-id="ea324-208">0x00000506</span><span class="sxs-lookup"><span data-stu-id="ea324-208">0x00000506</span></span>  <br/> |
|<span data-ttu-id="ea324-209">Journal-Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="ea324-209">Journal conversation</span></span>  <br/> |<span data-ttu-id="ea324-210">0x00000601</span><span class="sxs-lookup"><span data-stu-id="ea324-210">0x00000601</span></span>  <br/> |
|<span data-ttu-id="ea324-211">Journal-E-Mail-Nachricht</span><span class="sxs-lookup"><span data-stu-id="ea324-211">Journal email message</span></span>  <br/> |<span data-ttu-id="ea324-212">0x00000602</span><span class="sxs-lookup"><span data-stu-id="ea324-212">0x00000602</span></span>  <br/> |
|<span data-ttu-id="ea324-213">Journal-Besprechungsanfrage</span><span class="sxs-lookup"><span data-stu-id="ea324-213">Journal meeting request</span></span>  <br/> |<span data-ttu-id="ea324-214">0x00000603</span><span class="sxs-lookup"><span data-stu-id="ea324-214">0x00000603</span></span>  <br/> |
|<span data-ttu-id="ea324-215">Journal-Besprechungsantwort</span><span class="sxs-lookup"><span data-stu-id="ea324-215">Journal meeting response</span></span>  <br/> |<span data-ttu-id="ea324-216">0x00000604</span><span class="sxs-lookup"><span data-stu-id="ea324-216">0x00000604</span></span>  <br/> |
|<span data-ttu-id="ea324-217">Journal-Aufgabenanforderung</span><span class="sxs-lookup"><span data-stu-id="ea324-217">Journal task request</span></span>  <br/> |<span data-ttu-id="ea324-218">0x00000606</span><span class="sxs-lookup"><span data-stu-id="ea324-218">0x00000606</span></span>  <br/> |
|<span data-ttu-id="ea324-219">Antwort auf Journalaufgabe</span><span class="sxs-lookup"><span data-stu-id="ea324-219">Journal task response</span></span>  <br/> |<span data-ttu-id="ea324-220">0x00000607</span><span class="sxs-lookup"><span data-stu-id="ea324-220">0x00000607</span></span>  <br/> |
|<span data-ttu-id="ea324-221">Journalnotiz</span><span class="sxs-lookup"><span data-stu-id="ea324-221">Journal note</span></span>  <br/> |<span data-ttu-id="ea324-222">0x00000608</span><span class="sxs-lookup"><span data-stu-id="ea324-222">0x00000608</span></span>  <br/> |
|<span data-ttu-id="ea324-223">Journalfax</span><span class="sxs-lookup"><span data-stu-id="ea324-223">Journal fax</span></span>  <br/> |<span data-ttu-id="ea324-224">0x00000609</span><span class="sxs-lookup"><span data-stu-id="ea324-224">0x00000609</span></span>  <br/> |
|<span data-ttu-id="ea324-225">Journaltelefonanruf</span><span class="sxs-lookup"><span data-stu-id="ea324-225">Journal phone call</span></span>  <br/> |<span data-ttu-id="ea324-226">0x0000060A</span><span class="sxs-lookup"><span data-stu-id="ea324-226">0x0000060A</span></span>  <br/> |
|<span data-ttu-id="ea324-227">Journalbuchstabe</span><span class="sxs-lookup"><span data-stu-id="ea324-227">Journal letter</span></span>  <br/> |<span data-ttu-id="ea324-228">0x0000060C</span><span class="sxs-lookup"><span data-stu-id="ea324-228">0x0000060C</span></span>  <br/> |
|<span data-ttu-id="ea324-229">Journal Microsoft Office Word</span><span class="sxs-lookup"><span data-stu-id="ea324-229">Journal Microsoft Office Word</span></span>  <br/> |<span data-ttu-id="ea324-230">0x0000060D</span><span class="sxs-lookup"><span data-stu-id="ea324-230">0x0000060D</span></span>  <br/> |
|<span data-ttu-id="ea324-231">Journal Microsoft Office Excel</span><span class="sxs-lookup"><span data-stu-id="ea324-231">Journal Microsoft Office Excel</span></span>  <br/> |<span data-ttu-id="ea324-232">0x0000060E</span><span class="sxs-lookup"><span data-stu-id="ea324-232">0x0000060E</span></span>  <br/> |
|<span data-ttu-id="ea324-233">Journal Microsoft Office PowerPoint</span><span class="sxs-lookup"><span data-stu-id="ea324-233">Journal Microsoft Office PowerPoint</span></span>  <br/> |<span data-ttu-id="ea324-234">0x0000060F</span><span class="sxs-lookup"><span data-stu-id="ea324-234">0x0000060F</span></span>  <br/> |
|<span data-ttu-id="ea324-235">Journal Microsoft Office Access</span><span class="sxs-lookup"><span data-stu-id="ea324-235">Journal Microsoft Office Access</span></span>  <br/> |<span data-ttu-id="ea324-236">0x00000610</span><span class="sxs-lookup"><span data-stu-id="ea324-236">0x00000610</span></span>  <br/> |
|<span data-ttu-id="ea324-237">Journaldokument</span><span class="sxs-lookup"><span data-stu-id="ea324-237">Journal document</span></span>  <br/> |<span data-ttu-id="ea324-238">0x00000612</span><span class="sxs-lookup"><span data-stu-id="ea324-238">0x00000612</span></span>  <br/> |
|<span data-ttu-id="ea324-239">Journal besprechung</span><span class="sxs-lookup"><span data-stu-id="ea324-239">Journal meeting</span></span>  <br/> |<span data-ttu-id="ea324-240">0x00000613</span><span class="sxs-lookup"><span data-stu-id="ea324-240">0x00000613</span></span>  <br/> |
|<span data-ttu-id="ea324-241">Besprechungsabsagen in Journalen</span><span class="sxs-lookup"><span data-stu-id="ea324-241">Journal meeting cancellation</span></span>  <br/> |<span data-ttu-id="ea324-242">0x00000614</span><span class="sxs-lookup"><span data-stu-id="ea324-242">0x00000614</span></span>  <br/> |
|<span data-ttu-id="ea324-243">Journal-Remotesitzung</span><span class="sxs-lookup"><span data-stu-id="ea324-243">Journal remote session</span></span>  <br/> |<span data-ttu-id="ea324-244">0x00000615</span><span class="sxs-lookup"><span data-stu-id="ea324-244">0x00000615</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ea324-245">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ea324-245">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ea324-246">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ea324-246">Protocol specifications</span></span>

<span data-ttu-id="ea324-247">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ea324-247">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ea324-248">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="ea324-248">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ea324-249">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ea324-249">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ea324-250">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="ea324-250">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="ea324-251">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ea324-251">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ea324-252">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="ea324-252">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="ea324-253">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ea324-253">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ea324-254">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="ea324-254">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ea324-255">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="ea324-255">Header files</span></span>

<span data-ttu-id="ea324-256">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ea324-256">Mapidefs.h</span></span>
  
> <span data-ttu-id="ea324-257">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ea324-257">Provides data type definitions.</span></span>
    
<span data-ttu-id="ea324-258">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ea324-258">Mapitags.h</span></span>
  
> <span data-ttu-id="ea324-259">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="ea324-259">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ea324-260">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea324-260">See also</span></span>



[<span data-ttu-id="ea324-261">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ea324-261">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ea324-262">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="ea324-262">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ea324-263">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ea324-263">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ea324-264">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ea324-264">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

