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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 51a83e1e28534cc237419d9c4ae475c1d719c5de
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565074"
---
# <a name="iexchangemodifytable--iunknown"></a><span data-ttu-id="83dc0-103">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="83dc0-103">IExchangeModifyTable : IUnknown</span></span>

  
  
<span data-ttu-id="83dc0-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="83dc0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="83dc0-105">Unterstützt den Zugriff auf Microsoft Exchange Server Table-Objekte, insbesondere Systemzugriff (List, SACL) Table-Objekte zu steuern und Regel Table-Objekte in Microsoft Exchange Server-Ordnern.</span><span class="sxs-lookup"><span data-stu-id="83dc0-105">Supports access to Microsoft Exchange Server table objects, specifically system access control list (SACL) table objects and rule table objects on Microsoft Exchange Server folders.</span></span> <span data-ttu-id="83dc0-106">Diese Schnittstelle ähnelt der [IMAPITable: IUnknown](imapitableiunknown.md) -Schnittstelle, aber es fügt die Unterstützung für Microsoft Exchange Server-spezifische Strukturen, die zur Steuerung der SACLs und Regeln hinzu.</span><span class="sxs-lookup"><span data-stu-id="83dc0-106">This interface resembles the [IMAPITable : IUnknown](imapitableiunknown.md) interface, but it adds support for Microsoft Exchange Server-specific structures that are used to control SACLs and rules.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="83dc0-107">Verfügbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="83dc0-107">Exposed by:</span></span>  <br/> |<span data-ttu-id="83dc0-108">Keine</span><span class="sxs-lookup"><span data-stu-id="83dc0-108">None</span></span>  <br/> |
|<span data-ttu-id="83dc0-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="83dc0-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="83dc0-110">Server Table-Objekte</span><span class="sxs-lookup"><span data-stu-id="83dc0-110">Server table objects</span></span>  <br/> |
|<span data-ttu-id="83dc0-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="83dc0-111">Called by:</span></span>  <br/> |<span data-ttu-id="83dc0-112">MAPI-und Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="83dc0-112">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="83dc0-113">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="83dc0-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="83dc0-114">IID_IExchangeModifyTable</span><span class="sxs-lookup"><span data-stu-id="83dc0-114">IID_IExchangeModifyTable</span></span>  <br/> |
|<span data-ttu-id="83dc0-115">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="83dc0-115">Pointer type:</span></span>  <br/> |<span data-ttu-id="83dc0-116">LPEXCHANGEMODIFYTABLE</span><span class="sxs-lookup"><span data-stu-id="83dc0-116">LPEXCHANGEMODIFYTABLE</span></span>  <br/> |
|<span data-ttu-id="83dc0-117">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="83dc0-117">Transaction model:</span></span>  <br/> |<span data-ttu-id="83dc0-118">Durchgeführt</span><span class="sxs-lookup"><span data-stu-id="83dc0-118">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="83dc0-119">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="83dc0-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="83dc0-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="83dc0-120">GetLastError</span></span>](iexchangemodifytable-getlasterror.md) <br/> |<span data-ttu-id="83dc0-121">Gibt Informationen zu den letzten aufgetretenen Fehler in einem Table-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="83dc0-121">Returns information about the last error that occurred in a table object.</span></span>  <br/> |
|[<span data-ttu-id="83dc0-122">GetTable</span><span class="sxs-lookup"><span data-stu-id="83dc0-122">GetTable</span></span>](iexchangemodifytable-gettable.md) <br/> |<span data-ttu-id="83dc0-123">Gibt einen Zeiger auf eine Schnittstelle für ein MAPI-Table-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="83dc0-123">Returns a pointer to an interface for a MAPI table object.</span></span>  <br/> |
|[<span data-ttu-id="83dc0-124">ModifyTable</span><span class="sxs-lookup"><span data-stu-id="83dc0-124">ModifyTable</span></span>](iexchangemodifytable-modifytable.md) <br/> |<span data-ttu-id="83dc0-125">Aktualisiert ein MAPI-Table-Objekt.</span><span class="sxs-lookup"><span data-stu-id="83dc0-125">Updates a MAPI table object.</span></span>  <br/> |
   
|<span data-ttu-id="83dc0-126">**Eigenschaften, die zum Ändern einer Regeltabelle**</span><span class="sxs-lookup"><span data-stu-id="83dc0-126">**Properties used to modify a rules table**</span></span>|<span data-ttu-id="83dc0-127">**Access**</span><span class="sxs-lookup"><span data-stu-id="83dc0-127">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="83dc0-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83dc0-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83dc0-129">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="83dc0-129">Read-only</span></span>  <br/> |
|<span data-ttu-id="83dc0-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83dc0-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83dc0-131">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="83dc0-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="83dc0-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83dc0-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83dc0-133">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="83dc0-133">Read-only</span></span>  <br/> |
|<span data-ttu-id="83dc0-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83dc0-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83dc0-135">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="83dc0-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="83dc0-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83dc0-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83dc0-137">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="83dc0-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="83dc0-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83dc0-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83dc0-139">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="83dc0-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="83dc0-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83dc0-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83dc0-141">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="83dc0-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="83dc0-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83dc0-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83dc0-143">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="83dc0-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="83dc0-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83dc0-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83dc0-145">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="83dc0-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="83dc0-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83dc0-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83dc0-147">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="83dc0-147">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="83dc0-148">**Eigenschaften, die zum Ändern einer SACL-Tabelle**</span><span class="sxs-lookup"><span data-stu-id="83dc0-148">**Properties used to modify a SACL table**</span></span>|<span data-ttu-id="83dc0-149">**Access**</span><span class="sxs-lookup"><span data-stu-id="83dc0-149">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="83dc0-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83dc0-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83dc0-151">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="83dc0-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="83dc0-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83dc0-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83dc0-153">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="83dc0-153">Read-only</span></span>  <br/> |
|<span data-ttu-id="83dc0-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83dc0-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83dc0-155">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="83dc0-155">Read-only</span></span>  <br/> |
|<span data-ttu-id="83dc0-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="83dc0-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="83dc0-157">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="83dc0-157">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="83dc0-158">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="83dc0-158">Remarks</span></span>

<span data-ttu-id="83dc0-159">Rufen Sie zum Abrufen der **IExchangeModifyTable** -Schnittstelle, die MAPI- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode für eine Eigenschaft vom Typ PT_OBJECT auf ein Folder-Objekt.</span><span class="sxs-lookup"><span data-stu-id="83dc0-159">To obtain the **IExchangeModifyTable** interface, call the MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on a property of type PT_OBJECT on a folder object.</span></span> <span data-ttu-id="83dc0-160">Wenn Sie die **OpenProperty** -Methode aufrufen, übergeben Sie den Wert **IID_IExchangeModifyTable** im _Lpiid_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="83dc0-160">When you call the **OpenProperty** method, pass the value **IID_IExchangeModifyTable** in the  _lpiid_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="83dc0-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83dc0-161">See also</span></span>



[<span data-ttu-id="83dc0-162">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="83dc0-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

