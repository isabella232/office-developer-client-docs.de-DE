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
# <a name="iexchangemodifytable--iunknown"></a>IExchangeModifyTable : IUnknown

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Unterstützt den Zugriff auf Microsoft Exchange Server Table-Objekte, insbesondere Systemzugriff (List, SACL) Table-Objekte zu steuern und Regel Table-Objekte in Microsoft Exchange Server-Ordnern. Diese Schnittstelle ähnelt der [IMAPITable: IUnknown](imapitableiunknown.md) -Schnittstelle, aber es fügt die Unterstützung für Microsoft Exchange Server-spezifische Strukturen, die zur Steuerung der SACLs und Regeln hinzu. 
  
|||
|:-----|:-----|
|Verfügbar gemacht von:  <br/> |Keine  <br/> |
|Implementiert von:  <br/> |Server Table-Objekte  <br/> |
|Aufgerufen von:  <br/> |MAPI-und Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IExchangeModifyTable  <br/> |
|Zeigertyp:  <br/> |LPEXCHANGEMODIFYTABLE  <br/> |
|Transaktionsmodell:  <br/> |Durchgeführt  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetLastError](iexchangemodifytable-getlasterror.md) <br/> |Gibt Informationen zu den letzten aufgetretenen Fehler in einem Table-Objekt zurück.  <br/> |
|[GetTable](iexchangemodifytable-gettable.md) <br/> |Gibt einen Zeiger auf eine Schnittstelle für ein MAPI-Table-Objekt zurück.  <br/> |
|[ModifyTable](iexchangemodifytable-modifytable.md) <br/> |Aktualisiert ein MAPI-Table-Objekt.  <br/> |
   
|**Eigenschaften, die zum Ändern einer Regeltabelle**|**Access**|
|:-----|:-----|
|**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
   
|**Eigenschaften, die zum Ändern einer SACL-Tabelle**|**Access**|
|:-----|:-----|
|**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Rufen Sie zum Abrufen der **IExchangeModifyTable** -Schnittstelle, die MAPI- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode für eine Eigenschaft vom Typ PT_OBJECT auf ein Folder-Objekt. Wenn Sie die **OpenProperty** -Methode aufrufen, übergeben Sie den Wert **IID_IExchangeModifyTable** im _Lpiid_ -Parameter. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

