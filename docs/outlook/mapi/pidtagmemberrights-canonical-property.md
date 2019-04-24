---
title: Kanonische Pidtagmemberrights (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberRights
api_type:
- HeaderDef
ms.assetid: 3e526b93-1f64-41ea-b43c-5b03fe1c56ed
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: dcbf8a323f5178a5a2e39d0963dd19415ab835bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342694"
---
# <a name="pidtagmemberrights-canonical-property"></a><span data-ttu-id="9bdfb-103">Kanonische Pidtagmemberrights (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9bdfb-103">PidTagMemberRights Canonical Property</span></span>

  
  
<span data-ttu-id="9bdfb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9bdfb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9bdfb-105">Enthält eine Reihe von Bits, die die Rechte dieses Members für einen Ordner oder ein Postfach angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="9bdfb-105">Contains a set of bits that indicated the rights of this member on a folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9bdfb-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9bdfb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9bdfb-107">PR_MEMBER_RIGHTS</span><span class="sxs-lookup"><span data-stu-id="9bdfb-107">PR_MEMBER_RIGHTS</span></span>  <br/> |
|<span data-ttu-id="9bdfb-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="9bdfb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9bdfb-109">0x6673</span><span class="sxs-lookup"><span data-stu-id="9bdfb-109">0x6673</span></span>  <br/> |
|<span data-ttu-id="9bdfb-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9bdfb-110">Data type:</span></span>  <br/> |<span data-ttu-id="9bdfb-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9bdfb-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9bdfb-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9bdfb-112">Area:</span></span>  <br/> |<span data-ttu-id="9bdfb-113">Zugriffssteuerung</span><span class="sxs-lookup"><span data-stu-id="9bdfb-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9bdfb-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9bdfb-114">Remarks</span></span>

<span data-ttu-id="9bdfb-115">Diese Eigenschaft wird von der [IExchangeModifyTable](iexchangemodifytableiunknown.md) -Schnittstelle verwendet, um die Rechte eines Members für einen Ordner zu definieren.</span><span class="sxs-lookup"><span data-stu-id="9bdfb-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to define rights of a member on a folder.</span></span> <span data-ttu-id="9bdfb-116">Diese Rechte können angezeigt und geändert werden.</span><span class="sxs-lookup"><span data-stu-id="9bdfb-116">These rights can be displayed and modified.</span></span> <span data-ttu-id="9bdfb-117">Die folgenden Werte sind für diese Eigenschaft definierte Rechte.</span><span class="sxs-lookup"><span data-stu-id="9bdfb-117">The following values are rights defined for this property.</span></span> 
  
<span data-ttu-id="9bdfb-118">frightsReadAny</span><span class="sxs-lookup"><span data-stu-id="9bdfb-118">frightsReadAny</span></span>
  
> <span data-ttu-id="9bdfb-119">Mitglieder können alle Nachrichten lesen.</span><span class="sxs-lookup"><span data-stu-id="9bdfb-119">Member can read any messages.</span></span>
    
<span data-ttu-id="9bdfb-120">frightsCreate</span><span class="sxs-lookup"><span data-stu-id="9bdfb-120">frightsCreate</span></span>
  
> <span data-ttu-id="9bdfb-121">Mitglied kann Nachrichten erstellen.</span><span class="sxs-lookup"><span data-stu-id="9bdfb-121">Member can create messages.</span></span>
    
<span data-ttu-id="9bdfb-122">frightsEditOwned</span><span class="sxs-lookup"><span data-stu-id="9bdfb-122">frightsEditOwned</span></span>
  
> <span data-ttu-id="9bdfb-123">Mitglieder können alle Nachrichten bearbeiten, die dem Benutzer gehören.</span><span class="sxs-lookup"><span data-stu-id="9bdfb-123">Member can edit any messages owned by the user.</span></span>
    
<span data-ttu-id="9bdfb-124">frightsDeleteOwned</span><span class="sxs-lookup"><span data-stu-id="9bdfb-124">frightsDeleteOwned</span></span>
  
> <span data-ttu-id="9bdfb-125">Das Mitglied kann alle Nachrichten löschen, die dem Benutzer gehören.</span><span class="sxs-lookup"><span data-stu-id="9bdfb-125">Member can delete any messages owned by the user.</span></span>
    
<span data-ttu-id="9bdfb-126">frightsEditAny</span><span class="sxs-lookup"><span data-stu-id="9bdfb-126">frightsEditAny</span></span>
  
> <span data-ttu-id="9bdfb-127">Mitglied kann jede Nachricht bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="9bdfb-127">Member can edit any message.</span></span>
    
<span data-ttu-id="9bdfb-128">frightsDeleteAny</span><span class="sxs-lookup"><span data-stu-id="9bdfb-128">frightsDeleteAny</span></span>
  
> <span data-ttu-id="9bdfb-129">Mitglied kann jede Nachricht löschen.</span><span class="sxs-lookup"><span data-stu-id="9bdfb-129">Member can delete any message.</span></span>
    
<span data-ttu-id="9bdfb-130">frightsCreateSubfolder</span><span class="sxs-lookup"><span data-stu-id="9bdfb-130">frightsCreateSubfolder</span></span>
  
> <span data-ttu-id="9bdfb-131">Mitglied kann Unterordner für den Ordner erstellen.</span><span class="sxs-lookup"><span data-stu-id="9bdfb-131">Member can create subfolders for the folder.</span></span>
    
<span data-ttu-id="9bdfb-132">frightsOwner</span><span class="sxs-lookup"><span data-stu-id="9bdfb-132">frightsOwner</span></span>
  
> <span data-ttu-id="9bdfb-133">Mitglied verfügt über alle vorherigen Rechte für den Ordner.</span><span class="sxs-lookup"><span data-stu-id="9bdfb-133">Member has all the previous rights on the folder.</span></span>
    
<span data-ttu-id="9bdfb-134">Berechtigung frightsContact</span><span class="sxs-lookup"><span data-stu-id="9bdfb-134">frightsContact</span></span>
  
> <span data-ttu-id="9bdfb-135">Member kann Ihren Namen als Kontakt im Ordner angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9bdfb-135">Member can have your name appear as the contact on the folder.</span></span>
    
<span data-ttu-id="9bdfb-136">frightsVisible umgewandelt</span><span class="sxs-lookup"><span data-stu-id="9bdfb-136">frightsVisible</span></span>
  
> <span data-ttu-id="9bdfb-137">Mitglied kann sehen, dass der Ordner vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9bdfb-137">Member can see that the folder exists.</span></span>
    
<span data-ttu-id="9bdfb-138">rightsNone</span><span class="sxs-lookup"><span data-stu-id="9bdfb-138">rightsNone</span></span>
  
> <span data-ttu-id="9bdfb-139">Member verfügt nicht über Rechte für den Ordner.</span><span class="sxs-lookup"><span data-stu-id="9bdfb-139">Member does not have rights on the folder.</span></span>
    
<span data-ttu-id="9bdfb-140">rightsReadOnly</span><span class="sxs-lookup"><span data-stu-id="9bdfb-140">rightsReadOnly</span></span>
  
> <span data-ttu-id="9bdfb-141">Mitglied kann alle Nachrichten im Ordner lesen.</span><span class="sxs-lookup"><span data-stu-id="9bdfb-141">Member can read any message in the folder.</span></span>
    
<span data-ttu-id="9bdfb-142">rightsReadWrite</span><span class="sxs-lookup"><span data-stu-id="9bdfb-142">rightsReadWrite</span></span>
  
> <span data-ttu-id="9bdfb-143">Mitglied kann aus einer beliebigen Nachricht im Ordner lesen und diese schreiben.</span><span class="sxs-lookup"><span data-stu-id="9bdfb-143">Member can read from and write to any message in the folder.</span></span>
    
<span data-ttu-id="9bdfb-144">rightsAll</span><span class="sxs-lookup"><span data-stu-id="9bdfb-144">rightsAll</span></span>
  
> <span data-ttu-id="9bdfb-145">Mitglied verfügt über alle vorherigen Rechte für den Ordner.</span><span class="sxs-lookup"><span data-stu-id="9bdfb-145">Member has all the previous rights on the folder.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="9bdfb-146">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9bdfb-146">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9bdfb-147">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="9bdfb-147">Protocol specifications</span></span>

<span data-ttu-id="9bdfb-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9bdfb-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9bdfb-149">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="9bdfb-149">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9bdfb-150">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9bdfb-150">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9bdfb-151">Behandelt Ordner Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="9bdfb-151">Handles folder operations.</span></span>
    
<span data-ttu-id="9bdfb-152">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9bdfb-152">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9bdfb-153">Behandelt das Abrufen von Ordner Berechtigungslisten, die auf dem Server gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="9bdfb-153">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="9bdfb-154">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9bdfb-154">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9bdfb-155">Gibt Methoden zum Herstellen einer Verbindung mit und Konfigurieren von Postfächern als Stellvertreter sowie Interaktionen mit Nachrichten-und Kalenderelementen an, wenn Sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="9bdfb-155">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9bdfb-156">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="9bdfb-156">Header files</span></span>

<span data-ttu-id="9bdfb-157">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9bdfb-157">Mapidefs.h</span></span>
  
> <span data-ttu-id="9bdfb-158">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="9bdfb-158">Provides data type definitions.</span></span>
    
<span data-ttu-id="9bdfb-159">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="9bdfb-159">Mapitags.h</span></span>
  
> <span data-ttu-id="9bdfb-160">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="9bdfb-160">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9bdfb-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9bdfb-161">See also</span></span>



[<span data-ttu-id="9bdfb-162">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9bdfb-162">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="9bdfb-163">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9bdfb-163">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9bdfb-164">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9bdfb-164">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9bdfb-165">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9bdfb-165">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9bdfb-166">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9bdfb-166">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

