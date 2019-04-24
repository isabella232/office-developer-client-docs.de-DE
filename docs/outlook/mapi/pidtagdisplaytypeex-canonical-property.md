---
title: Kanonische PidTagDisplayTypeEx-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayTypeEx
api_type:
- HeaderDef
ms.assetid: 23074402-6ac1-47f1-8a49-b8909f98a26e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6eea30188543cb06545a9efad705f5593d4227a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360774"
---
# <a name="pidtagdisplaytypeex-canonical-property"></a><span data-ttu-id="b2b14-103">Kanonische PidTagDisplayTypeEx-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b2b14-103">PidTagDisplayTypeEx Canonical Property</span></span>

  
  
<span data-ttu-id="b2b14-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2b14-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2b14-105">Enthält den Typ eines Eintrags im Hinblick darauf, wie der Eintrag in einer Zeile in einer Tabelle für die globale Adressliste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2b14-105">Contains the type of an entry, with respect to how the entry should be displayed in a row in a table for the Global Address List.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b2b14-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b2b14-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b2b14-107">PR_DISPLAY_TYPE_EX</span><span class="sxs-lookup"><span data-stu-id="b2b14-107">PR_DISPLAY_TYPE_EX</span></span>  <br/> |
|<span data-ttu-id="b2b14-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="b2b14-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b2b14-109">0x3905</span><span class="sxs-lookup"><span data-stu-id="b2b14-109">0x3905</span></span>  <br/> |
|<span data-ttu-id="b2b14-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b2b14-110">Data type:</span></span>  <br/> |<span data-ttu-id="b2b14-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b2b14-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b2b14-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b2b14-112">Area:</span></span>  <br/> |<span data-ttu-id="b2b14-113">MAPI-Adressbuch</span><span class="sxs-lookup"><span data-stu-id="b2b14-113">MAPI address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b2b14-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2b14-114">Remarks</span></span>

<span data-ttu-id="b2b14-115">Diese Eigenschaft gibt den Typ eines Eintrags an, der angibt, wie er in der globalen Adressliste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2b14-115">This property specifies the type of an entry, with respect to how it should be displayed in the Global Address List.</span></span> <span data-ttu-id="b2b14-116">Sie bietet zusätzliche Informationen, die in **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) nicht dargestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="b2b14-116">It provides additional information that cannot be represented in **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span></span>
  
> [!NOTE]
> <span data-ttu-id="b2b14-117">Die Werte von **PR_DISPLAY_TYPE** und dieser Eigenschaft beginnen mit "dt_" und sind in Mapitags. h definiert.</span><span class="sxs-lookup"><span data-stu-id="b2b14-117">The values of both **PR_DISPLAY_TYPE** and this property begin with "DT_" and are defined in Mapitags.h.</span></span> <span data-ttu-id="b2b14-118">Alle nicht dokumentierten Werte sind für MAPI reserviert.</span><span class="sxs-lookup"><span data-stu-id="b2b14-118">All values not documented are reserved for MAPI.</span></span> <span data-ttu-id="b2b14-119">Client Anwendungen dürfen keine neuen Werte definieren und müssen auf den Umgang mit einem nicht dokumentierten Wert vorbereitet sein.</span><span class="sxs-lookup"><span data-stu-id="b2b14-119">Client applications must not define any new values and must be prepared to deal with an undocumented value.</span></span> 
  
<span data-ttu-id="b2b14-120">Es gibt einige Makros, die dazu beitragen können, die Attribute eines Objekts zu ermitteln, beispielsweise ob es lokal, Remote oder Sicherheits gesteuert ist.</span><span class="sxs-lookup"><span data-stu-id="b2b14-120">There are some macros that can help determine attributes of an object such as whether it is local, remote, or security-controlled.</span></span> <span data-ttu-id="b2b14-121">Zu diesen Makros gehört Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b2b14-121">These macros include:</span></span> 
  
|<span data-ttu-id="b2b14-122">**Makro**</span><span class="sxs-lookup"><span data-stu-id="b2b14-122">**Macro**</span></span>|<span data-ttu-id="b2b14-123">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b2b14-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b2b14-124">DTE_FLAG_REMOTE_VALID</span><span class="sxs-lookup"><span data-stu-id="b2b14-124">DTE_FLAG_REMOTE_VALID</span></span>  <br/> |<span data-ttu-id="b2b14-125">0x80000000</span><span class="sxs-lookup"><span data-stu-id="b2b14-125">0x80000000)</span></span>  <br/> |
|<span data-ttu-id="b2b14-126">DTE_FLAG_ACL_CAPABLE</span><span class="sxs-lookup"><span data-stu-id="b2b14-126">DTE_FLAG_ACL_CAPABLE</span></span>  <br/> |<span data-ttu-id="b2b14-127">0x40000000</span><span class="sxs-lookup"><span data-stu-id="b2b14-127">0x40000000</span></span>  <br/> |
|<span data-ttu-id="b2b14-128">DTE_MASK_REMOTE</span><span class="sxs-lookup"><span data-stu-id="b2b14-128">DTE_MASK_REMOTE</span></span>  <br/> |<span data-ttu-id="b2b14-129">0x0000ff00</span><span class="sxs-lookup"><span data-stu-id="b2b14-129">0x0000ff00</span></span>  <br/> |
|<span data-ttu-id="b2b14-130">DTE_MASK_LOCAL</span><span class="sxs-lookup"><span data-stu-id="b2b14-130">DTE_MASK_LOCAL</span></span>  <br/> |<span data-ttu-id="b2b14-131">0x000000ff</span><span class="sxs-lookup"><span data-stu-id="b2b14-131">0x000000ff</span></span>  <br/> |
|<span data-ttu-id="b2b14-132">DTE_IS_REMOTE_VALID (v)</span><span class="sxs-lookup"><span data-stu-id="b2b14-132">DTE_IS_REMOTE_VALID(v)</span></span>  <br/> |<span data-ttu-id="b2b14-133">(!! ((v) &amp; DTE_FLAG_REMOTE_VALID)</span><span class="sxs-lookup"><span data-stu-id="b2b14-133">(!!((v) &amp; DTE_FLAG_REMOTE_VALID)</span></span>  <br/> |
|<span data-ttu-id="b2b14-134">DTE_IS_ACL_CAPABLE (v)</span><span class="sxs-lookup"><span data-stu-id="b2b14-134">DTE_IS_ACL_CAPABLE(v)</span></span>  <br/> |<span data-ttu-id="b2b14-135">(!! ((v) &amp; DTE_FLAG_ACL_CAPABLE))</span><span class="sxs-lookup"><span data-stu-id="b2b14-135">(!!((v) &amp; DTE_FLAG_ACL_CAPABLE))</span></span>  <br/> |
|<span data-ttu-id="b2b14-136">DTE_REMOTE (v)</span><span class="sxs-lookup"><span data-stu-id="b2b14-136">DTE_REMOTE(v)</span></span>  <br/> |<span data-ttu-id="b2b14-137">(((v) &amp; DTE_MASK_REMOTE \> \> ) 8)</span><span class="sxs-lookup"><span data-stu-id="b2b14-137">(((v) &amp; DTE_MASK_REMOTE) \>\> 8)</span></span>  <br/> |
|<span data-ttu-id="b2b14-138">DTE_LOCAL (v)</span><span class="sxs-lookup"><span data-stu-id="b2b14-138">DTE_LOCAL(v)</span></span>  <br/> |<span data-ttu-id="b2b14-139">((v) &amp; DTE_MASK_LOCAL)</span><span class="sxs-lookup"><span data-stu-id="b2b14-139">((v) &amp; DTE_MASK_LOCAL)</span></span>  <br/> |
|<span data-ttu-id="b2b14-140">DT_ROOM</span><span class="sxs-lookup"><span data-stu-id="b2b14-140">DT_ROOM</span></span>  <br/> |<span data-ttu-id="b2b14-141">((ULONG) 0x00000007)</span><span class="sxs-lookup"><span data-stu-id="b2b14-141">((ULONG) 0x00000007)</span></span>  <br/> |
|<span data-ttu-id="b2b14-142">DT_EQUIPMENT</span><span class="sxs-lookup"><span data-stu-id="b2b14-142">DT_EQUIPMENT</span></span>  <br/> |<span data-ttu-id="b2b14-143">((ULONG) 0x00000008)</span><span class="sxs-lookup"><span data-stu-id="b2b14-143">((ULONG) 0x00000008)</span></span>  <br/> |
|<span data-ttu-id="b2b14-144">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="b2b14-144">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="b2b14-145">((ULONG) 0x00000009)</span><span class="sxs-lookup"><span data-stu-id="b2b14-145">((ULONG) 0x00000009)</span></span>  <br/> |
   
<span data-ttu-id="b2b14-146">Im folgenden finden Sie einige Hinweise zur Verwendung dieser Makros.</span><span class="sxs-lookup"><span data-stu-id="b2b14-146">The following are a few notes about how to use these macros.</span></span> 
  
- <span data-ttu-id="b2b14-147">Um zu überprüfen, ob ein Eintrag ein Remote Eintrag in einer anderen Gesamtstruktur ist, wenden Sie das DTE_IS_REMOTE_VALID-Makro auf den Wert dieser Eigenschaft an, um zu überprüfen, ob das DTE_FLAG_REMOTE_VALID-Flag im Eintrag festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b2b14-147">To check whether an entry is a remote entry in another forest, apply the DTE_IS_REMOTE_VALID macro to the value of this property to check whether the DTE_FLAG_REMOTE_VALID flag is set in the entry.</span></span> <span data-ttu-id="b2b14-148">Wenn es sich um einen Remote Eintrag handelt, können Sie den Typ des Remote Eintrags mithilfe des DTE_REMOTE-Makros herausfinden.</span><span class="sxs-lookup"><span data-stu-id="b2b14-148">If it is a remote entry, you can then find out the type of the remote entry by using the DTE_REMOTE macro.</span></span> 
    
- <span data-ttu-id="b2b14-149">Wenn **PR_DISPLAY_TYPE** den Wert DT_DISTLIST und DTE_IS_REMOTE_VALID auf false festgelegt ist, kann das Makro DTE_LOCAL auf den Wert dieser Eigenschaft angewendet werden, um den Typ des Objekts weiter zu identifizieren, wenn entweder DT_DISTLIST (eine Verteilerliste) oder DT_SEC_DISTLIST (eine Sicherheits Verteilerliste).</span><span class="sxs-lookup"><span data-stu-id="b2b14-149">In both single-forest and cross-forest configurations, when **PR_DISPLAY_TYPE** has the value of DT_DISTLIST, and DTE_IS_REMOTE_VALID is false, applying the macro DTE_LOCAL to the value of this property can let you further identify the type of the object as either DT_DISTLIST (a distribution list) or DT_SEC_DISTLIST (a security distribution list).</span></span> 
    
- <span data-ttu-id="b2b14-150">Wenn Sie das Makro DTE_LOCAL auf den Wert von **PR_DISPLAY_TYPE_EX** anwenden und den Typ DT_REMOTE_MAILUSER zurückgibt, handelt es sich bei dem Eintrag um einen Remote Eintrag.</span><span class="sxs-lookup"><span data-stu-id="b2b14-150">If you apply the macro DTE_LOCAL to the value of **PR_DISPLAY_TYPE_EX** and it returns the type DT_REMOTE_MAILUSER, then the entry is a remote entry.</span></span> 
    
- <span data-ttu-id="b2b14-151">In einer einzelnen Gesamtstruktur oder in einer gesamtstrukturübergreifenden Konfiguration, bei der die Replikation durch eine Zugriffssteuerungsliste (Access Control List, ACL) gesteuert wird, können Sie mithilfe des DTE_IS_ACL_CAPABLE-Makros ermitteln, ob ein Eintrag ein Sicherheitsprinzipal ist.</span><span class="sxs-lookup"><span data-stu-id="b2b14-151">In a single forest or in a cross-forest configuration where replication is controlled by an Access Control List (ACL), you can use the DTE_IS_ACL_CAPABLE macro to determine whether an entry is a security principal.</span></span>
    
<span data-ttu-id="b2b14-152">Bei einer gesamtstrukturübergreifenden Konfiguration besitzt **PR_DISPLAY_TYPE** den Wert von DT_REMOTE_MAILUSER.</span><span class="sxs-lookup"><span data-stu-id="b2b14-152">In a cross-forest configuration, **PR_DISPLAY_TYPE** has the value of DT_REMOTE_MAILUSER.</span></span> <span data-ttu-id="b2b14-153">Wenn Sie das Makro DTE_REMOTE auf den Wert dieser Eigenschaft anwenden, können Sie den Typ des Remote Eintrags abrufen.</span><span class="sxs-lookup"><span data-stu-id="b2b14-153">Applying the macro DTE_REMOTE to the value of this property can let you obtain the type of the remote entry.</span></span> <span data-ttu-id="b2b14-154">Folgende Arten von Remote Einträgen sind möglich:</span><span class="sxs-lookup"><span data-stu-id="b2b14-154">The possible types of remote entry are the following:</span></span> 
  
|<span data-ttu-id="b2b14-155">**Typ des Remote Eintrags**</span><span class="sxs-lookup"><span data-stu-id="b2b14-155">**Type of Remote Entry**</span></span>|<span data-ttu-id="b2b14-156">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b2b14-156">**Value**</span></span>|<span data-ttu-id="b2b14-157">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b2b14-157">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b2b14-158">DT_AGENT</span><span class="sxs-lookup"><span data-stu-id="b2b14-158">DT_AGENT</span></span>  <br/> |<span data-ttu-id="b2b14-159">((ULONG) 0x00000003)</span><span class="sxs-lookup"><span data-stu-id="b2b14-159">((ULONG) 0x00000003)</span></span>  <br/> |<span data-ttu-id="b2b14-160">Dynamische Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="b2b14-160">Dynamic distribution list.</span></span>  <br/> |
|<span data-ttu-id="b2b14-161">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="b2b14-161">DT_DISTLIST</span></span>  <br/> |<span data-ttu-id="b2b14-162">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="b2b14-162">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="b2b14-163">Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="b2b14-163">Distribution list.</span></span>  <br/> |
|<span data-ttu-id="b2b14-164">DT_EQUIPMENT</span><span class="sxs-lookup"><span data-stu-id="b2b14-164">DT_EQUIPMENT</span></span>  <br/> |<span data-ttu-id="b2b14-165">((ULONG) 0x00000008)</span><span class="sxs-lookup"><span data-stu-id="b2b14-165">((ULONG) 0x00000008)</span></span>  <br/> |<span data-ttu-id="b2b14-166">Geräte, beispielsweise einen Drucker oder einen Projektor.</span><span class="sxs-lookup"><span data-stu-id="b2b14-166">Equipment, for example, a printer or a projector.</span></span>  <br/> |
|<span data-ttu-id="b2b14-167">DT_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="b2b14-167">DT_MAILUSER</span></span>  <br/> |<span data-ttu-id="b2b14-168">((ULONG) 0x00000000)</span><span class="sxs-lookup"><span data-stu-id="b2b14-168">((ULONG) 0x00000000)</span></span>  <br/> |<span data-ttu-id="b2b14-169">Benutzer mit einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="b2b14-169">User with a mailbox.</span></span>  <br/> |
|<span data-ttu-id="b2b14-170">DT_REMOTE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="b2b14-170">DT_REMOTE_MAILUSER</span></span>  <br/> |<span data-ttu-id="b2b14-171">((ULONG) 0x00000000)</span><span class="sxs-lookup"><span data-stu-id="b2b14-171">((ULONG) 0x00000000)</span></span>  <br/> |<span data-ttu-id="b2b14-172">Ein Adresslisten Eintrag in der globalen Adressliste.</span><span class="sxs-lookup"><span data-stu-id="b2b14-172">An address list entry in the Global Address List.</span></span>  <br/> |
|<span data-ttu-id="b2b14-173">DT_ROOM</span><span class="sxs-lookup"><span data-stu-id="b2b14-173">DT_ROOM</span></span>  <br/> |<span data-ttu-id="b2b14-174">((ULONG) 0x00000007)</span><span class="sxs-lookup"><span data-stu-id="b2b14-174">((ULONG) 0x00000007)</span></span>  <br/> |<span data-ttu-id="b2b14-175">Konferenzraum.</span><span class="sxs-lookup"><span data-stu-id="b2b14-175">Conference room.</span></span>  <br/> |
|<span data-ttu-id="b2b14-176">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="b2b14-176">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="b2b14-177">((ULONG) 0x00000009)</span><span class="sxs-lookup"><span data-stu-id="b2b14-177">((ULONG) 0x00000009)</span></span>  <br/> |<span data-ttu-id="b2b14-178">Sicherheits Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="b2b14-178">Security distribution list.</span></span>  <br/> |
   
<span data-ttu-id="b2b14-179">In einer einzelnen Gesamtstruktur und in einer gesamtstrukturübergreifenden Konfiguration, wenn **PR_DISPLAY_TYPE** den Wert DT_DISTLIST und DTE_IS_REMOTE_VALID ist false ist, kann Anwenden des DTE_LOCAL-Makros auf den Wert dieser Eigenschaft können Sie den Typ der Verteilerliste abrufen .</span><span class="sxs-lookup"><span data-stu-id="b2b14-179">In both a single forest and in a cross-forest configuration, when **PR_DISPLAY_TYPE** has the value of DT_DISTLIST and DTE_IS_REMOTE_VALID is false, applying the DTE_LOCAL macro to the value of this property can let you obtain the type of the distribution list.</span></span> <span data-ttu-id="b2b14-180">Folgende Arten von Verteilerlisten sind möglich:</span><span class="sxs-lookup"><span data-stu-id="b2b14-180">The possible types of distribution list are the following:</span></span> 
  
|<span data-ttu-id="b2b14-181">**Typ der Verteilerliste**</span><span class="sxs-lookup"><span data-stu-id="b2b14-181">**Type of Distribution List**</span></span>|<span data-ttu-id="b2b14-182">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b2b14-182">**Value**</span></span>|<span data-ttu-id="b2b14-183">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b2b14-183">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b2b14-184">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="b2b14-184">DT_DISTLIST</span></span>  <br/> |<span data-ttu-id="b2b14-185">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="b2b14-185">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="b2b14-186">Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="b2b14-186">Distribution list.</span></span>  <br/> |
|<span data-ttu-id="b2b14-187">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="b2b14-187">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="b2b14-188">((ULONG) 0x00000009)</span><span class="sxs-lookup"><span data-stu-id="b2b14-188">((ULONG) 0x00000009)</span></span>  <br/> |<span data-ttu-id="b2b14-189">Sicherheits Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="b2b14-189">Security distribution list.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b2b14-190">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b2b14-190">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b2b14-191">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b2b14-191">Protocol specifications</span></span>

<span data-ttu-id="b2b14-192">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b2b14-192">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b2b14-193">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="b2b14-193">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b2b14-194">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b2b14-194">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b2b14-195">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="b2b14-195">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b2b14-196">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="b2b14-196">Header files</span></span>

<span data-ttu-id="b2b14-197">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b2b14-197">Mapidefs.h</span></span>
  
> <span data-ttu-id="b2b14-198">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="b2b14-198">Provides data type definitions.</span></span>
    
<span data-ttu-id="b2b14-199">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="b2b14-199">Mapitags.h</span></span>
  
> <span data-ttu-id="b2b14-200">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b2b14-200">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b2b14-201">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2b14-201">See also</span></span>



[<span data-ttu-id="b2b14-202">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2b14-202">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b2b14-203">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2b14-203">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b2b14-204">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b2b14-204">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b2b14-205">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b2b14-205">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

