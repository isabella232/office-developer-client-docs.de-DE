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
ms.openlocfilehash: 1093975e6cbdd79004125a0a4a3098ffa421ab0b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792054"
---
# <a name="iexchangemodifytable--iunknown"></a><span data-ttu-id="21110-103">IExchangeModifyTable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="21110-103">IExchangeModifyTable : IUnknown</span></span>

  
  
<span data-ttu-id="21110-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="21110-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="21110-105">Unterstützt den Zugriff auf Microsoft Exchange Server Table-Objekte, insbesondere Systemzugriff (List, SACL) Table-Objekte zu steuern und Regel Table-Objekte in Microsoft Exchange Server-Ordnern.</span><span class="sxs-lookup"><span data-stu-id="21110-105">Supports access to Microsoft Exchange Server table objects, specifically system access control list (SACL) table objects and rule table objects on Microsoft Exchange Server folders.</span></span> <span data-ttu-id="21110-106">Diese Schnittstelle ähnelt der [IMAPITable: IUnknown](imapitableiunknown.md) -Schnittstelle, aber es fügt die Unterstützung für Microsoft Exchange Server-spezifische Strukturen, die zur Steuerung der SACLs und Regeln hinzu.</span><span class="sxs-lookup"><span data-stu-id="21110-106">This interface resembles the [IMAPITable : IUnknown](imapitableiunknown.md) interface, but it adds support for Microsoft Exchange Server-specific structures that are used to control SACLs and rules.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="21110-107">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="21110-107">Exposed by:</span></span>  <br/> |<span data-ttu-id="21110-108">Keine</span><span class="sxs-lookup"><span data-stu-id="21110-108">None</span></span>  <br/> |
|<span data-ttu-id="21110-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="21110-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="21110-110">Server Table-Objekte</span><span class="sxs-lookup"><span data-stu-id="21110-110">Server table objects</span></span>  <br/> |
|<span data-ttu-id="21110-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="21110-111">Called by:</span></span>  <br/> |<span data-ttu-id="21110-112">MAPI-und Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="21110-112">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="21110-113">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="21110-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="21110-114">IID_IExchangeModifyTable</span><span class="sxs-lookup"><span data-stu-id="21110-114">IID_IExchangeModifyTable</span></span>  <br/> |
|<span data-ttu-id="21110-115">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="21110-115">Pointer type:</span></span>  <br/> |<span data-ttu-id="21110-116">LPEXCHANGEMODIFYTABLE</span><span class="sxs-lookup"><span data-stu-id="21110-116">LPEXCHANGEMODIFYTABLE</span></span>  <br/> |
|<span data-ttu-id="21110-117">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="21110-117">Transaction model:</span></span>  <br/> |<span data-ttu-id="21110-118">Durchgeführt</span><span class="sxs-lookup"><span data-stu-id="21110-118">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="21110-119">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="21110-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="21110-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="21110-120">GetLastError</span></span>](iexchangemodifytable-getlasterror.md) <br/> |<span data-ttu-id="21110-121">Gibt Informationen zu den letzten aufgetretenen Fehler in einem Table-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="21110-121">Returns information about the last error that occurred in a table object.</span></span>  <br/> |
|[<span data-ttu-id="21110-122">GetTable</span><span class="sxs-lookup"><span data-stu-id="21110-122">GetTable</span></span>](iexchangemodifytable-gettable.md) <br/> |<span data-ttu-id="21110-123">Gibt einen Zeiger auf eine Schnittstelle für ein MAPI-Table-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="21110-123">Returns a pointer to an interface for a MAPI table object.</span></span>  <br/> |
|[<span data-ttu-id="21110-124">ModifyTable</span><span class="sxs-lookup"><span data-stu-id="21110-124">ModifyTable</span></span>](iexchangemodifytable-modifytable.md) <br/> |<span data-ttu-id="21110-125">Aktualisiert ein MAPI-Table-Objekt.</span><span class="sxs-lookup"><span data-stu-id="21110-125">Updates a MAPI table object.</span></span>  <br/> |
   
|<span data-ttu-id="21110-126">**Eigenschaften, die zum Ändern einer Regeltabelle**</span><span class="sxs-lookup"><span data-stu-id="21110-126">**Properties used to modify a rules table**</span></span>|<span data-ttu-id="21110-127">**Zugriff**</span><span class="sxs-lookup"><span data-stu-id="21110-127">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="21110-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21110-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="21110-129">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="21110-129">Read-only</span></span>  <br/> |
|<span data-ttu-id="21110-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21110-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="21110-131">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="21110-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="21110-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21110-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="21110-133">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="21110-133">Read-only</span></span>  <br/> |
|<span data-ttu-id="21110-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21110-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="21110-135">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="21110-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="21110-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21110-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="21110-137">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="21110-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="21110-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21110-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="21110-139">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="21110-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="21110-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21110-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="21110-141">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="21110-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="21110-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21110-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="21110-143">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="21110-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="21110-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21110-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="21110-145">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="21110-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="21110-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21110-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="21110-147">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="21110-147">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="21110-148">**Eigenschaften, die zum Ändern einer SACL-Tabelle**</span><span class="sxs-lookup"><span data-stu-id="21110-148">**Properties used to modify a SACL table**</span></span>|<span data-ttu-id="21110-149">**Zugriff**</span><span class="sxs-lookup"><span data-stu-id="21110-149">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="21110-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21110-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="21110-151">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="21110-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="21110-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21110-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="21110-153">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="21110-153">Read-only</span></span>  <br/> |
|<span data-ttu-id="21110-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21110-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="21110-155">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="21110-155">Read-only</span></span>  <br/> |
|<span data-ttu-id="21110-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21110-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="21110-157">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="21110-157">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="21110-158">Hinweise</span><span class="sxs-lookup"><span data-stu-id="21110-158">Remarks</span></span>

<span data-ttu-id="21110-159">Rufen Sie zum Abrufen der **IExchangeModifyTable** -Schnittstelle, die MAPI- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode für eine Eigenschaft vom Typ PT_OBJECT auf ein Folder-Objekt.</span><span class="sxs-lookup"><span data-stu-id="21110-159">To obtain the **IExchangeModifyTable** interface, call the MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on a property of type PT_OBJECT on a folder object.</span></span> <span data-ttu-id="21110-160">Wenn Sie die **OpenProperty** -Methode aufrufen, übergeben Sie den Wert **IID_IExchangeModifyTable** im _Lpiid_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="21110-160">When you call the **OpenProperty** method, pass the value **IID_IExchangeModifyTable** in the  _lpiid_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="21110-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21110-161">See also</span></span>



[<span data-ttu-id="21110-162">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="21110-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

