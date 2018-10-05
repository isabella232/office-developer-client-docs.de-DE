---
title: PidTagMemberRights (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dcbf8a323f5178a5a2e39d0963dd19415ab835bd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397338"
---
# <a name="pidtagmemberrights-canonical-property"></a><span data-ttu-id="e2371-103">PidTagMemberRights (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e2371-103">PidTagMemberRights Canonical Property</span></span>

  
  
<span data-ttu-id="e2371-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2371-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2371-105">Enthält eine Reihe von Bits an, die die Rechte von dieser Member in einem Ordner oder Postfach angegeben.</span><span class="sxs-lookup"><span data-stu-id="e2371-105">Contains a set of bits that indicated the rights of this member on a folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e2371-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e2371-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e2371-107">PR_MEMBER_RIGHTS</span><span class="sxs-lookup"><span data-stu-id="e2371-107">PR_MEMBER_RIGHTS</span></span>  <br/> |
|<span data-ttu-id="e2371-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e2371-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e2371-109">0x6673</span><span class="sxs-lookup"><span data-stu-id="e2371-109">0x6673</span></span>  <br/> |
|<span data-ttu-id="e2371-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e2371-110">Data type:</span></span>  <br/> |<span data-ttu-id="e2371-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e2371-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e2371-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e2371-112">Area:</span></span>  <br/> |<span data-ttu-id="e2371-113">Steuerung des Zugriffs</span><span class="sxs-lookup"><span data-stu-id="e2371-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2371-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e2371-114">Remarks</span></span>

<span data-ttu-id="e2371-115">Diese Eigenschaft wird von der [IExchangeModifyTable](iexchangemodifytableiunknown.md) -Schnittstelle zum Rechte eines Elements in einem Ordner zu definieren.</span><span class="sxs-lookup"><span data-stu-id="e2371-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to define rights of a member on a folder.</span></span> <span data-ttu-id="e2371-116">Diese Rechte können angezeigt und geändert werden.</span><span class="sxs-lookup"><span data-stu-id="e2371-116">These rights can be displayed and modified.</span></span> <span data-ttu-id="e2371-117">Die folgenden Werte sind für diese Eigenschaft festgelegten Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="e2371-117">The following values are rights defined for this property.</span></span> 
  
<span data-ttu-id="e2371-118">frightsReadAny</span><span class="sxs-lookup"><span data-stu-id="e2371-118">frightsReadAny</span></span>
  
> <span data-ttu-id="e2371-119">Member kann Nachrichten nicht gelesen.</span><span class="sxs-lookup"><span data-stu-id="e2371-119">Member can read any messages.</span></span>
    
<span data-ttu-id="e2371-120">frightsCreate</span><span class="sxs-lookup"><span data-stu-id="e2371-120">frightsCreate</span></span>
  
> <span data-ttu-id="e2371-121">Member kann Nachrichten erstellen.</span><span class="sxs-lookup"><span data-stu-id="e2371-121">Member can create messages.</span></span>
    
<span data-ttu-id="e2371-122">frightsEditOwned</span><span class="sxs-lookup"><span data-stu-id="e2371-122">frightsEditOwned</span></span>
  
> <span data-ttu-id="e2371-123">Member kann alle Nachrichten, deren Besitzer der Benutzer bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="e2371-123">Member can edit any messages owned by the user.</span></span>
    
<span data-ttu-id="e2371-124">frightsDeleteOwned</span><span class="sxs-lookup"><span data-stu-id="e2371-124">frightsDeleteOwned</span></span>
  
> <span data-ttu-id="e2371-125">Member kann alle Nachrichten, deren Besitzer der Benutzer löschen.</span><span class="sxs-lookup"><span data-stu-id="e2371-125">Member can delete any messages owned by the user.</span></span>
    
<span data-ttu-id="e2371-126">frightsEditAny</span><span class="sxs-lookup"><span data-stu-id="e2371-126">frightsEditAny</span></span>
  
> <span data-ttu-id="e2371-127">Member kann eine beliebige Nachricht bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="e2371-127">Member can edit any message.</span></span>
    
<span data-ttu-id="e2371-128">frightsDeleteAny</span><span class="sxs-lookup"><span data-stu-id="e2371-128">frightsDeleteAny</span></span>
  
> <span data-ttu-id="e2371-129">Member kann eine beliebige Nachricht löschen.</span><span class="sxs-lookup"><span data-stu-id="e2371-129">Member can delete any message.</span></span>
    
<span data-ttu-id="e2371-130">frightsCreateSubfolder</span><span class="sxs-lookup"><span data-stu-id="e2371-130">frightsCreateSubfolder</span></span>
  
> <span data-ttu-id="e2371-131">Member kann Unterordner für den Ordner erstellen.</span><span class="sxs-lookup"><span data-stu-id="e2371-131">Member can create subfolders for the folder.</span></span>
    
<span data-ttu-id="e2371-132">frightsOwner</span><span class="sxs-lookup"><span data-stu-id="e2371-132">frightsOwner</span></span>
  
> <span data-ttu-id="e2371-133">Mitglied hat alle vorherigen Rechte für den Ordner.</span><span class="sxs-lookup"><span data-stu-id="e2371-133">Member has all the previous rights on the folder.</span></span>
    
<span data-ttu-id="e2371-134">frightsContact</span><span class="sxs-lookup"><span data-stu-id="e2371-134">frightsContact</span></span>
  
> <span data-ttu-id="e2371-135">Member können Ihren Namen als den Kontakt für den Ordner angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e2371-135">Member can have your name appear as the contact on the folder.</span></span>
    
<span data-ttu-id="e2371-136">frightsVisible</span><span class="sxs-lookup"><span data-stu-id="e2371-136">frightsVisible</span></span>
  
> <span data-ttu-id="e2371-137">Member kann sehen, dass der Ordner vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e2371-137">Member can see that the folder exists.</span></span>
    
<span data-ttu-id="e2371-138">rightsNone</span><span class="sxs-lookup"><span data-stu-id="e2371-138">rightsNone</span></span>
  
> <span data-ttu-id="e2371-139">Member verfügt nicht Rechte für den Ordner.</span><span class="sxs-lookup"><span data-stu-id="e2371-139">Member does not have rights on the folder.</span></span>
    
<span data-ttu-id="e2371-140">rightsReadOnly</span><span class="sxs-lookup"><span data-stu-id="e2371-140">rightsReadOnly</span></span>
  
> <span data-ttu-id="e2371-141">Member kann eine beliebige Nachricht im Ordner lesen.</span><span class="sxs-lookup"><span data-stu-id="e2371-141">Member can read any message in the folder.</span></span>
    
<span data-ttu-id="e2371-142">rightsReadWrite</span><span class="sxs-lookup"><span data-stu-id="e2371-142">rightsReadWrite</span></span>
  
> <span data-ttu-id="e2371-143">Member kann aus lesen und Schreiben in eine beliebige Nachricht im Ordner.</span><span class="sxs-lookup"><span data-stu-id="e2371-143">Member can read from and write to any message in the folder.</span></span>
    
<span data-ttu-id="e2371-144">rightsAll</span><span class="sxs-lookup"><span data-stu-id="e2371-144">rightsAll</span></span>
  
> <span data-ttu-id="e2371-145">Mitglied hat alle vorherigen Rechte für den Ordner.</span><span class="sxs-lookup"><span data-stu-id="e2371-145">Member has all the previous rights on the folder.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="e2371-146">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e2371-146">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e2371-147">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e2371-147">Protocol specifications</span></span>

<span data-ttu-id="e2371-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2371-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2371-149">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e2371-149">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e2371-150">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2371-150">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2371-151">Ordner Vorgänge behandelt.</span><span class="sxs-lookup"><span data-stu-id="e2371-151">Handles folder operations.</span></span>
    
<span data-ttu-id="e2371-152">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2371-152">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2371-153">Behandelt das Abrufen von Ordner Berechtigungslisten, die auf dem Server gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="e2371-153">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="e2371-154">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2371-154">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2371-155">Gibt die Methoden zum Verbinden mit und Postfächer als Stellvertreter und Interaktionen mit Nachrichten und Kalenderelemente konfigurieren, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="e2371-155">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e2371-156">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="e2371-156">Header files</span></span>

<span data-ttu-id="e2371-157">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e2371-157">Mapidefs.h</span></span>
  
> <span data-ttu-id="e2371-158">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e2371-158">Provides data type definitions.</span></span>
    
<span data-ttu-id="e2371-159">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e2371-159">Mapitags.h</span></span>
  
> <span data-ttu-id="e2371-160">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e2371-160">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e2371-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2371-161">See also</span></span>



[<span data-ttu-id="e2371-162">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e2371-162">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="e2371-163">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e2371-163">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e2371-164">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e2371-164">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e2371-165">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e2371-165">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e2371-166">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e2371-166">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

