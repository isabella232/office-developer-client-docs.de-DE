---
title: IExchangeModifyTable IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable
api_type:
- COM
ms.assetid: 45a73c7b-5855-4b70-866b-facb41cb3c32
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 333e1d5cacc069ee1faef01426a1c0a60ef07f8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350883"
---
# <a name="iexchangemodifytable--iunknown"></a><span data-ttu-id="2aef1-103">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2aef1-103">IExchangeModifyTable : IUnknown</span></span>

  
  
<span data-ttu-id="2aef1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2aef1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2aef1-105">Unterstützt den Zugriff auf Microsoft Exchange Server-Tabellenobjekte, insbesondere auf SACL-Tabellenobjekte und Regel Tabellenobjekte in Microsoft Exchange Server-Ordnern.</span><span class="sxs-lookup"><span data-stu-id="2aef1-105">Supports access to Microsoft Exchange Server table objects, specifically system access control list (SACL) table objects and rule table objects on Microsoft Exchange Server folders.</span></span> <span data-ttu-id="2aef1-106">Diese Schnittstelle ähnelt der [IMAPITable: IUnknown](imapitableiunknown.md) -Schnittstelle, fügt jedoch Unterstützung für Microsoft Exchange Server-spezifische Strukturen hinzu, die zum Steuern von SACLs und Regeln verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2aef1-106">This interface resembles the [IMAPITable : IUnknown](imapitableiunknown.md) interface, but it adds support for Microsoft Exchange Server-specific structures that are used to control SACLs and rules.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2aef1-107">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="2aef1-107">Exposed by:</span></span>  <br/> |<span data-ttu-id="2aef1-108">Keine</span><span class="sxs-lookup"><span data-stu-id="2aef1-108">None</span></span>  <br/> |
|<span data-ttu-id="2aef1-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="2aef1-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="2aef1-110">Server Tabellenobjekte</span><span class="sxs-lookup"><span data-stu-id="2aef1-110">Server table objects</span></span>  <br/> |
|<span data-ttu-id="2aef1-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="2aef1-111">Called by:</span></span>  <br/> |<span data-ttu-id="2aef1-112">MAPI-und Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="2aef1-112">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="2aef1-113">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="2aef1-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2aef1-114">IID_IExchangeModifyTable</span><span class="sxs-lookup"><span data-stu-id="2aef1-114">IID_IExchangeModifyTable</span></span>  <br/> |
|<span data-ttu-id="2aef1-115">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="2aef1-115">Pointer type:</span></span>  <br/> |<span data-ttu-id="2aef1-116">LPEXCHANGEMODIFYTABLE</span><span class="sxs-lookup"><span data-stu-id="2aef1-116">LPEXCHANGEMODIFYTABLE</span></span>  <br/> |
|<span data-ttu-id="2aef1-117">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="2aef1-117">Transaction model:</span></span>  <br/> |<span data-ttu-id="2aef1-118">Durchgeführt</span><span class="sxs-lookup"><span data-stu-id="2aef1-118">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2aef1-119">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="2aef1-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="2aef1-120">Getlasterroraufzurufen</span><span class="sxs-lookup"><span data-stu-id="2aef1-120">GetLastError</span></span>](iexchangemodifytable-getlasterror.md) <br/> |<span data-ttu-id="2aef1-121">Gibt Informationen zum letzten Fehler zurück, der in einem Table-Objekt aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="2aef1-121">Returns information about the last error that occurred in a table object.</span></span>  <br/> |
|[<span data-ttu-id="2aef1-122">GetTable</span><span class="sxs-lookup"><span data-stu-id="2aef1-122">GetTable</span></span>](iexchangemodifytable-gettable.md) <br/> |<span data-ttu-id="2aef1-123">Gibt einen Zeiger auf eine Schnittstelle für ein MAPI-Tabellenobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="2aef1-123">Returns a pointer to an interface for a MAPI table object.</span></span>  <br/> |
|[<span data-ttu-id="2aef1-124">Modifyable</span><span class="sxs-lookup"><span data-stu-id="2aef1-124">ModifyTable</span></span>](iexchangemodifytable-modifytable.md) <br/> |<span data-ttu-id="2aef1-125">Aktualisiert ein MAPI-Tabellenobjekt.</span><span class="sxs-lookup"><span data-stu-id="2aef1-125">Updates a MAPI table object.</span></span>  <br/> |
   
|<span data-ttu-id="2aef1-126">**Zum Ändern einer Regeltabelle verwendete Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="2aef1-126">**Properties used to modify a rules table**</span></span>|<span data-ttu-id="2aef1-127">**Access**</span><span class="sxs-lookup"><span data-stu-id="2aef1-127">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2aef1-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2aef1-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2aef1-129">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2aef1-129">Read-only</span></span>  <br/> |
|<span data-ttu-id="2aef1-130">**PR_RULE_CONDITION** ([Pidtagrulecondition (](pidtagrulecondition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2aef1-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2aef1-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2aef1-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="2aef1-132">**PR_RULE_ID** ([Pidtagruleid (](pidtagruleid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2aef1-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2aef1-133">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2aef1-133">Read-only</span></span>  <br/> |
|<span data-ttu-id="2aef1-134">**PR_RULE_LEVEL** ([Pidtagrulelevel (](pidtagrulelevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2aef1-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2aef1-135">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2aef1-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="2aef1-136">**PR_RULE_NAME** ([Pidtagrulename (](pidtagrulename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2aef1-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2aef1-137">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2aef1-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="2aef1-138">**PR_RULE_PROVIDER** ([Pidtagruleprovider (](pidtagruleprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2aef1-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2aef1-139">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2aef1-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="2aef1-140">**PR_RULE_PROVIDER_DATA** ([Pidtagruleproviderdata (](pidtagruleproviderdata-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2aef1-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2aef1-141">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2aef1-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="2aef1-142">**PR_RULE_SEQUENCE** ([Pidtagrulesequence (](pidtagrulesequence-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2aef1-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2aef1-143">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2aef1-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="2aef1-144">**PR_RULE_STATE** ([Pidtagrulestate (](pidtagrulestate-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2aef1-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2aef1-145">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2aef1-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="2aef1-146">**PR_RULE_USER_FLAGS** ([Pidtagruleuserflags (](pidtagruleuserflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2aef1-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2aef1-147">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2aef1-147">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="2aef1-148">**Zum Ändern einer SACL-Tabelle verwendete Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="2aef1-148">**Properties used to modify a SACL table**</span></span>|<span data-ttu-id="2aef1-149">**Access**</span><span class="sxs-lookup"><span data-stu-id="2aef1-149">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2aef1-150">**PR_MEMBER_ENTRYID** ([Pidtagmemberentryid (](pidtagmemberentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2aef1-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2aef1-151">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2aef1-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="2aef1-152">**PR_MEMBER_ID** ([Pidtagmemberid (](pidtagmemberid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2aef1-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2aef1-153">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2aef1-153">Read-only</span></span>  <br/> |
|<span data-ttu-id="2aef1-154">**PR_MEMBER_NAME** ([Pidtagmembername (](pidtagmembername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2aef1-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2aef1-155">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2aef1-155">Read-only</span></span>  <br/> |
|<span data-ttu-id="2aef1-156">**PR_MEMBER_RIGHTS** ([Pidtagmemberrights (](pidtagmemberrights-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2aef1-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2aef1-157">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2aef1-157">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2aef1-158">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2aef1-158">Remarks</span></span>

<span data-ttu-id="2aef1-159">Rufen Sie zum Abrufen der **IExchangeModifyTable** -Schnittstelle die MAPI- [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode für eine Eigenschaft vom Typ PT_OBJECT für ein Folder-Objekt auf.</span><span class="sxs-lookup"><span data-stu-id="2aef1-159">To obtain the **IExchangeModifyTable** interface, call the MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on a property of type PT_OBJECT on a folder object.</span></span> <span data-ttu-id="2aef1-160">Wenn Sie die **OpenProperty** -Methode aufrufen, übergeben Sie den Wert **IID_IExchangeModifyTable** im _lpIID_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="2aef1-160">When you call the **OpenProperty** method, pass the value **IID_IExchangeModifyTable** in the  _lpiid_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2aef1-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2aef1-161">See also</span></span>



[<span data-ttu-id="2aef1-162">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="2aef1-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

