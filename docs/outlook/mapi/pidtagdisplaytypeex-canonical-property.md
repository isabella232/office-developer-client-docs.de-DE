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
ms.openlocfilehash: a21eecfb1bf3bc4f09fc5becb9a4a99a97193330
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794338"
---
# <a name="pidtagdisplaytypeex-canonical-property"></a><span data-ttu-id="65682-103">Kanonische PidTagDisplayTypeEx-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="65682-103">PidTagDisplayTypeEx Canonical Property</span></span>

  
  
<span data-ttu-id="65682-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="65682-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="65682-105">Enthält den Typ eines Eintrags im Hinblick auf wie der Eintrag für die globale Adressliste in einer Zeile in einer Tabelle angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="65682-105">Contains the type of an entry, with respect to how the entry should be displayed in a row in a table for the Global Address List.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="65682-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="65682-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="65682-107">PR_DISPLAY_TYPE_EX</span><span class="sxs-lookup"><span data-stu-id="65682-107">PR_DISPLAY_TYPE_EX</span></span>  <br/> |
|<span data-ttu-id="65682-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="65682-108">Identifier:</span></span>  <br/> |<span data-ttu-id="65682-109">0x3905</span><span class="sxs-lookup"><span data-stu-id="65682-109">0x3905</span></span>  <br/> |
|<span data-ttu-id="65682-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="65682-110">Data type:</span></span>  <br/> |<span data-ttu-id="65682-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="65682-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="65682-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="65682-112">Area:</span></span>  <br/> |<span data-ttu-id="65682-113">MAPI-Adressbuch</span><span class="sxs-lookup"><span data-stu-id="65682-113">MAPI address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="65682-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="65682-114">Remarks</span></span>

<span data-ttu-id="65682-115">Diese Eigenschaft gibt den Typ eines Eintrags im Hinblick auf, wie er in der globalen Adressliste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="65682-115">This property specifies the type of an entry, with respect to how it should be displayed in the Global Address List.</span></span> <span data-ttu-id="65682-116">Bietet zusätzliche Informationen, die im **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) dargestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="65682-116">It provides additional information that cannot be represented in **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span></span>
  
> [!NOTE]
> <span data-ttu-id="65682-117">Die Werte der **PR_DISPLAY_TYPE** und diese Eigenschaft mit "DT_" beginnen und in Mapitags.h definiert sind.</span><span class="sxs-lookup"><span data-stu-id="65682-117">The values of both **PR_DISPLAY_TYPE** and this property begin with "DT_" and are defined in Mapitags.h.</span></span> <span data-ttu-id="65682-118">Alle Werte, die nicht dokumentiert sind für die MAPI reserviert.</span><span class="sxs-lookup"><span data-stu-id="65682-118">All values not documented are reserved for MAPI.</span></span> <span data-ttu-id="65682-119">Clientanwendungen dürfen Sie keine neue Werte definieren und für den Umgang mit eine nicht dokumentierte Wert vorbereitet sein.</span><span class="sxs-lookup"><span data-stu-id="65682-119">Client applications must not define any new values and must be prepared to deal with an undocumented value.</span></span> 
  
<span data-ttu-id="65682-120">Es gibt einige Makros, die Attribute eines Objekts wie gibt an, ob es sich um lokale, Remote- oder Sicherheit gesteuerte ist bestimmen helfen kann.</span><span class="sxs-lookup"><span data-stu-id="65682-120">There are some macros that can help determine attributes of an object such as whether it is local, remote, or security-controlled.</span></span> <span data-ttu-id="65682-121">Diese Makros enthalten:</span><span class="sxs-lookup"><span data-stu-id="65682-121">These macros include:</span></span> 
  
|<span data-ttu-id="65682-122">**Makro**</span><span class="sxs-lookup"><span data-stu-id="65682-122">**Macro**</span></span>|<span data-ttu-id="65682-123">**Wert**</span><span class="sxs-lookup"><span data-stu-id="65682-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="65682-124">DTE_FLAG_REMOTE_VALID</span><span class="sxs-lookup"><span data-stu-id="65682-124">DTE_FLAG_REMOTE_VALID</span></span>  <br/> |<span data-ttu-id="65682-125">0 x 80000000)</span><span class="sxs-lookup"><span data-stu-id="65682-125">0x80000000)</span></span>  <br/> |
|<span data-ttu-id="65682-126">DTE_FLAG_ACL_CAPABLE</span><span class="sxs-lookup"><span data-stu-id="65682-126">DTE_FLAG_ACL_CAPABLE</span></span>  <br/> |<span data-ttu-id="65682-127">0 x 40000000</span><span class="sxs-lookup"><span data-stu-id="65682-127">0x40000000</span></span>  <br/> |
|<span data-ttu-id="65682-128">DTE_MASK_REMOTE</span><span class="sxs-lookup"><span data-stu-id="65682-128">DTE_MASK_REMOTE</span></span>  <br/> |<span data-ttu-id="65682-129">0x0000FF00</span><span class="sxs-lookup"><span data-stu-id="65682-129">0x0000ff00</span></span>  <br/> |
|<span data-ttu-id="65682-130">DTE_MASK_LOCAL</span><span class="sxs-lookup"><span data-stu-id="65682-130">DTE_MASK_LOCAL</span></span>  <br/> |<span data-ttu-id="65682-131">0x000000ff</span><span class="sxs-lookup"><span data-stu-id="65682-131">0x000000ff</span></span>  <br/> |
|<span data-ttu-id="65682-132">DTE_IS_REMOTE_VALID(v)</span><span class="sxs-lookup"><span data-stu-id="65682-132">DTE_IS_REMOTE_VALID(v)</span></span>  <br/> |<span data-ttu-id="65682-133">(!! ((V) &amp; DTE_FLAG_REMOTE_VALID)</span><span class="sxs-lookup"><span data-stu-id="65682-133">(!!((v) &amp; DTE_FLAG_REMOTE_VALID)</span></span>  <br/> |
|<span data-ttu-id="65682-134">DTE_IS_ACL_CAPABLE(v)</span><span class="sxs-lookup"><span data-stu-id="65682-134">DTE_IS_ACL_CAPABLE(v)</span></span>  <br/> |<span data-ttu-id="65682-135">(!! ((V) &amp; DTE_FLAG_ACL_CAPABLE))</span><span class="sxs-lookup"><span data-stu-id="65682-135">(!!((v) &amp; DTE_FLAG_ACL_CAPABLE))</span></span>  <br/> |
|<span data-ttu-id="65682-136">DTE_REMOTE(v)</span><span class="sxs-lookup"><span data-stu-id="65682-136">DTE_REMOTE(v)</span></span>  <br/> |<span data-ttu-id="65682-137">(((V) &amp; DTE_MASK_REMOTE) \> \> 8)</span><span class="sxs-lookup"><span data-stu-id="65682-137">(((v) &amp; DTE_MASK_REMOTE) \>\> 8)</span></span>  <br/> |
|<span data-ttu-id="65682-138">DTE_LOCAL(v)</span><span class="sxs-lookup"><span data-stu-id="65682-138">DTE_LOCAL(v)</span></span>  <br/> |<span data-ttu-id="65682-139">((V) &amp; DTE_MASK_LOCAL)</span><span class="sxs-lookup"><span data-stu-id="65682-139">((v) &amp; DTE_MASK_LOCAL)</span></span>  <br/> |
|<span data-ttu-id="65682-140">DT_ROOM</span><span class="sxs-lookup"><span data-stu-id="65682-140">DT_ROOM</span></span>  <br/> |<span data-ttu-id="65682-141">((ULONG) 0 X 00000007)</span><span class="sxs-lookup"><span data-stu-id="65682-141">((ULONG) 0x00000007)</span></span>  <br/> |
|<span data-ttu-id="65682-142">DT_EQUIPMENT</span><span class="sxs-lookup"><span data-stu-id="65682-142">DT_EQUIPMENT</span></span>  <br/> |<span data-ttu-id="65682-143">((ULONG) 0 X 00000008)</span><span class="sxs-lookup"><span data-stu-id="65682-143">((ULONG) 0x00000008)</span></span>  <br/> |
|<span data-ttu-id="65682-144">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="65682-144">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="65682-145">((ULONG) 0X00000009)</span><span class="sxs-lookup"><span data-stu-id="65682-145">((ULONG) 0x00000009)</span></span>  <br/> |
   
<span data-ttu-id="65682-146">Es folgen einige Hinweise zur Verwendung dieser Makros.</span><span class="sxs-lookup"><span data-stu-id="65682-146">The following are a few notes about how to use these macros.</span></span> 
  
- <span data-ttu-id="65682-147">Um zu überprüfen, ob ein Eintrag einer remote-Eintrag in einer anderen Gesamtstruktur ist, wenden Sie das Makro DTE_IS_REMOTE_VALID auf den Wert dieser Eigenschaft zu überprüfen, ob das Flag DTE_FLAG_REMOTE_VALID in den Eintrag festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="65682-147">To check whether an entry is a remote entry in another forest, apply the DTE_IS_REMOTE_VALID macro to the value of this property to check whether the DTE_FLAG_REMOTE_VALID flag is set in the entry.</span></span> <span data-ttu-id="65682-148">Wenn sie einen remote-Eintrag ist, klicken Sie dann finden, den Typ des remote-Eintrags Sie mithilfe des Makros DTE_REMOTE.</span><span class="sxs-lookup"><span data-stu-id="65682-148">If it is a remote entry, you can then find out the type of the remote entry by using the DTE_REMOTE macro.</span></span> 
    
- <span data-ttu-id="65682-149">In einer einzelnen Gesamtstruktur und gesamtstrukturübergreifende Konfigurationen Wenn **PR_DISPLAY_TYPE** hat der Wert der DT_DISTLIST und DTE_IS_REMOTE_VALID false ist, auf den Wert dieser Eigenschaft das Makro DTE_LOCAL angewendet, lassen Sie näher an den Typ des Objekts als DT_DISTLIST (eine Verteilerliste) oder DT_SEC_DISTLIST (einer Verteilerliste Sicherheit).</span><span class="sxs-lookup"><span data-stu-id="65682-149">In both single-forest and cross-forest configurations, when **PR_DISPLAY_TYPE** has the value of DT_DISTLIST, and DTE_IS_REMOTE_VALID is false, applying the macro DTE_LOCAL to the value of this property can let you further identify the type of the object as either DT_DISTLIST (a distribution list) or DT_SEC_DISTLIST (a security distribution list).</span></span> 
    
- <span data-ttu-id="65682-150">Wenn Sie das Makro DTE_LOCAL auf den Wert der **PR_DISPLAY_TYPE_EX** anwenden, und es den Typ DT_REMOTE_MAILUSER gibt, ist der Eintrag einen remote-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="65682-150">If you apply the macro DTE_LOCAL to the value of **PR_DISPLAY_TYPE_EX** and it returns the type DT_REMOTE_MAILUSER, then the entry is a remote entry.</span></span> 
    
- <span data-ttu-id="65682-151">In einer einzelnen Gesamtstruktur oder in einer gesamtstrukturübergreifenden Konfiguration, in dem Replikation durch eine Zugriffssteuerungsliste (ACL) gesteuert wird, können Sie das Makro DTE_IS_ACL_CAPABLE verwenden, um festzustellen, ob ein Eintrag ein Sicherheitsprinzipal ist.</span><span class="sxs-lookup"><span data-stu-id="65682-151">In a single forest or in a cross-forest configuration where replication is controlled by an Access Control List (ACL), you can use the DTE_IS_ACL_CAPABLE macro to determine whether an entry is a security principal.</span></span>
    
<span data-ttu-id="65682-152">In einer Konfiguration gesamtstrukturübergreifenden hat **PR_DISPLAY_TYPE** den Wert des DT_REMOTE_MAILUSER.</span><span class="sxs-lookup"><span data-stu-id="65682-152">In a cross-forest configuration, **PR_DISPLAY_TYPE** has the value of DT_REMOTE_MAILUSER.</span></span> <span data-ttu-id="65682-153">Anwenden von Makros DTE_REMOTE auf den Wert dieser Eigenschaft können Sie die Abrufen des Typs des remote-Eintrags lassen.</span><span class="sxs-lookup"><span data-stu-id="65682-153">Applying the macro DTE_REMOTE to the value of this property can let you obtain the type of the remote entry.</span></span> <span data-ttu-id="65682-154">Dies sind die möglichen Typen von remote-Eintrag:</span><span class="sxs-lookup"><span data-stu-id="65682-154">The possible types of remote entry are the following:</span></span> 
  
|<span data-ttu-id="65682-155">**Typ des Remote-Eintrags**</span><span class="sxs-lookup"><span data-stu-id="65682-155">**Type of Remote Entry**</span></span>|<span data-ttu-id="65682-156">**Wert**</span><span class="sxs-lookup"><span data-stu-id="65682-156">**Value**</span></span>|<span data-ttu-id="65682-157">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="65682-157">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="65682-158">DT_AGENT</span><span class="sxs-lookup"><span data-stu-id="65682-158">DT_AGENT</span></span>  <br/> |<span data-ttu-id="65682-159">((ULONG) 0 X 00000003)</span><span class="sxs-lookup"><span data-stu-id="65682-159">((ULONG) 0x00000003)</span></span>  <br/> |<span data-ttu-id="65682-160">Dynamische Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="65682-160">Dynamic distribution list.</span></span>  <br/> |
|<span data-ttu-id="65682-161">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="65682-161">DT_DISTLIST</span></span>  <br/> |<span data-ttu-id="65682-162">((ULONG) 0 X 00000001)</span><span class="sxs-lookup"><span data-stu-id="65682-162">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="65682-163">Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="65682-163">Distribution list.</span></span>  <br/> |
|<span data-ttu-id="65682-164">DT_EQUIPMENT</span><span class="sxs-lookup"><span data-stu-id="65682-164">DT_EQUIPMENT</span></span>  <br/> |<span data-ttu-id="65682-165">((ULONG) 0 X 00000008)</span><span class="sxs-lookup"><span data-stu-id="65682-165">((ULONG) 0x00000008)</span></span>  <br/> |<span data-ttu-id="65682-166">Geräte, beispielsweise einen Drucker oder einen Projektor.</span><span class="sxs-lookup"><span data-stu-id="65682-166">Equipment, for example, a printer or a projector.</span></span>  <br/> |
|<span data-ttu-id="65682-167">DT_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="65682-167">DT_MAILUSER</span></span>  <br/> |<span data-ttu-id="65682-168">((ULONG) 0 X 00000000)</span><span class="sxs-lookup"><span data-stu-id="65682-168">((ULONG) 0x00000000)</span></span>  <br/> |<span data-ttu-id="65682-169">Benutzer mit einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="65682-169">User with a mailbox.</span></span>  <br/> |
|<span data-ttu-id="65682-170">DT_REMOTE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="65682-170">DT_REMOTE_MAILUSER</span></span>  <br/> |<span data-ttu-id="65682-171">((ULONG) 0 X 00000000)</span><span class="sxs-lookup"><span data-stu-id="65682-171">((ULONG) 0x00000000)</span></span>  <br/> |<span data-ttu-id="65682-172">Ein Adresseintrag des Liste in der globalen Adressliste.</span><span class="sxs-lookup"><span data-stu-id="65682-172">An address list entry in the Global Address List.</span></span>  <br/> |
|<span data-ttu-id="65682-173">DT_ROOM</span><span class="sxs-lookup"><span data-stu-id="65682-173">DT_ROOM</span></span>  <br/> |<span data-ttu-id="65682-174">((ULONG) 0 X 00000007)</span><span class="sxs-lookup"><span data-stu-id="65682-174">((ULONG) 0x00000007)</span></span>  <br/> |<span data-ttu-id="65682-175">Konferenzraum.</span><span class="sxs-lookup"><span data-stu-id="65682-175">Conference room.</span></span>  <br/> |
|<span data-ttu-id="65682-176">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="65682-176">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="65682-177">((ULONG) 0X00000009)</span><span class="sxs-lookup"><span data-stu-id="65682-177">((ULONG) 0x00000009)</span></span>  <br/> |<span data-ttu-id="65682-178">Sicherheit-Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="65682-178">Security distribution list.</span></span>  <br/> |
   
<span data-ttu-id="65682-179">In beiden einer einzelnen Gesamtstruktur und in einem gesamtstrukturübergreifenden Konfiguration, wenn **PR_DISPLAY_TYPE** den Wert der DT_DISTLIST und DTE_IS_REMOTE_VALID hat false ist, das Makro DTE_LOCAL auf den Wert dieser Eigenschaft angewendet, lassen Sie das Abrufen des Typs der Verteilerliste .</span><span class="sxs-lookup"><span data-stu-id="65682-179">In both a single forest and in a cross-forest configuration, when **PR_DISPLAY_TYPE** has the value of DT_DISTLIST and DTE_IS_REMOTE_VALID is false, applying the DTE_LOCAL macro to the value of this property can let you obtain the type of the distribution list.</span></span> <span data-ttu-id="65682-180">Dies sind die möglichen Typen der Verteilerliste:</span><span class="sxs-lookup"><span data-stu-id="65682-180">The possible types of distribution list are the following:</span></span> 
  
|<span data-ttu-id="65682-181">**Typ der Verteilerliste**</span><span class="sxs-lookup"><span data-stu-id="65682-181">**Type of Distribution List**</span></span>|<span data-ttu-id="65682-182">**Wert**</span><span class="sxs-lookup"><span data-stu-id="65682-182">**Value**</span></span>|<span data-ttu-id="65682-183">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="65682-183">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="65682-184">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="65682-184">DT_DISTLIST</span></span>  <br/> |<span data-ttu-id="65682-185">((ULONG) 0 X 00000001)</span><span class="sxs-lookup"><span data-stu-id="65682-185">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="65682-186">Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="65682-186">Distribution list.</span></span>  <br/> |
|<span data-ttu-id="65682-187">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="65682-187">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="65682-188">((ULONG) 0X00000009)</span><span class="sxs-lookup"><span data-stu-id="65682-188">((ULONG) 0x00000009)</span></span>  <br/> |<span data-ttu-id="65682-189">Sicherheit-Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="65682-189">Security distribution list.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="65682-190">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="65682-190">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="65682-191">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="65682-191">Protocol specifications</span></span>

<span data-ttu-id="65682-192">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="65682-192">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="65682-193">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="65682-193">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="65682-194">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="65682-194">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="65682-195">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="65682-195">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="65682-196">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="65682-196">Header files</span></span>

<span data-ttu-id="65682-197">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="65682-197">Mapidefs.h</span></span>
  
> <span data-ttu-id="65682-198">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="65682-198">Provides data type definitions.</span></span>
    
<span data-ttu-id="65682-199">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="65682-199">Mapitags.h</span></span>
  
> <span data-ttu-id="65682-200">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="65682-200">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="65682-201">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65682-201">See also</span></span>



[<span data-ttu-id="65682-202">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="65682-202">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="65682-203">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="65682-203">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="65682-204">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="65682-204">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="65682-205">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="65682-205">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

