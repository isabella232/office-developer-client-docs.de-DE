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
ms.openlocfilehash: 333e1d5cacc069ee1faef01426a1c0a60ef07f8e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418106"
---
# <a name="iexchangemodifytable--iunknown"></a>IExchangeModifyTable : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Unterstützt den Zugriff auf Microsoft Exchange Server Tabellenobjekte, insbesondere SACL-Tabellenobjekte (System Access Control List) und Regeltabelle-Objekte in Microsoft Exchange Server Ordnern. Diese Schnittstelle ähnelt der [IMAPITable : IUnknown-Schnittstelle,](imapitableiunknown.md) bietet jedoch Unterstützung für Microsoft Exchange Server-spezifische Strukturen, die zum Steuern von SACLs und Regeln verwendet werden. 
  
|||
|:-----|:-----|
|Verf�gbar gemacht von:  <br/> |Keine  <br/> |
|Implementiert von:  <br/> |Server-Tabellenobjekte  <br/> |
|Aufgerufen von:  <br/> |MAPI- und Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IExchangeModifyTable  <br/> |
|Zeigertyp:  <br/> |LPEXCHANGEMODIFYTABLE  <br/> |
|Transaktionsmodell:  <br/> |Transacted  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetLastError](iexchangemodifytable-getlasterror.md) <br/> |Gibt Informationen zum letzten Fehler zurück, der in einem Tabellenobjekt aufgetreten ist.  <br/> |
|[GetTable](iexchangemodifytable-gettable.md) <br/> |Gibt einen Zeiger auf eine Schnittstelle für ein MAPI-Tabellenobjekt zurück.  <br/> |
|[ModifyTable](iexchangemodifytable-modifytable.md) <br/> |Aktualisiert ein MAPI-Tabellenobjekt.  <br/> |
   
|**Eigenschaften zum Ändern einer Regeltabelle**|**Access**|
|:-----|:-----|
|**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
   
|**Eigenschaften zum Ändern einer SACL-Tabelle**|**Access**|
|:-----|:-----|
|**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>Hinweise

Rufen Sie zum Abrufen der **IExchangeModifyTable-Schnittstelle** die MAPI-IMAPIProp::OpenProperty-Methode für eine Eigenschaft vom Typ PT_OBJECT ordnerobjekt auf. [](imapiprop-openproperty.md) Wenn Sie die **OpenProperty-Methode** aufrufen, übergeben Sie den Wert **IID_IExchangeModifyTable** im _lpiid-Parameter._ 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

