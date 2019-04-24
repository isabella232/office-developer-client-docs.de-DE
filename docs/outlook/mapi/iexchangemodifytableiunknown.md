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
# <a name="iexchangemodifytable--iunknown"></a>IExchangeModifyTable : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Unterstützt den Zugriff auf Microsoft Exchange Server-Tabellenobjekte, insbesondere auf SACL-Tabellenobjekte und Regel Tabellenobjekte in Microsoft Exchange Server-Ordnern. Diese Schnittstelle ähnelt der [IMAPITable: IUnknown](imapitableiunknown.md) -Schnittstelle, fügt jedoch Unterstützung für Microsoft Exchange Server-spezifische Strukturen hinzu, die zum Steuern von SACLs und Regeln verwendet werden. 
  
|||
|:-----|:-----|
|Verf�gbar gemacht von:  <br/> |Keine  <br/> |
|Implementiert von:  <br/> |Server Tabellenobjekte  <br/> |
|Aufgerufen von:  <br/> |MAPI-und Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IExchangeModifyTable  <br/> |
|Zeigertyp:  <br/> |LPEXCHANGEMODIFYTABLE  <br/> |
|Transaktionsmodell:  <br/> |Durchgeführt  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[Getlasterroraufzurufen](iexchangemodifytable-getlasterror.md) <br/> |Gibt Informationen zum letzten Fehler zurück, der in einem Table-Objekt aufgetreten ist.  <br/> |
|[GetTable](iexchangemodifytable-gettable.md) <br/> |Gibt einen Zeiger auf eine Schnittstelle für ein MAPI-Tabellenobjekt zurück.  <br/> |
|[Modifyable](iexchangemodifytable-modifytable.md) <br/> |Aktualisiert ein MAPI-Tabellenobjekt.  <br/> |
   
|**Zum Ändern einer Regeltabelle verwendete Eigenschaften**|**Access**|
|:-----|:-----|
|**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RULE_CONDITION** ([Pidtagrulecondition (](pidtagrulecondition-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RULE_ID** ([Pidtagruleid (](pidtagruleid-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RULE_LEVEL** ([Pidtagrulelevel (](pidtagrulelevel-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RULE_NAME** ([Pidtagrulename (](pidtagrulename-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RULE_PROVIDER** ([Pidtagruleprovider (](pidtagruleprovider-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RULE_PROVIDER_DATA** ([Pidtagruleproviderdata (](pidtagruleproviderdata-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RULE_SEQUENCE** ([Pidtagrulesequence (](pidtagrulesequence-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RULE_STATE** ([Pidtagrulestate (](pidtagrulestate-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RULE_USER_FLAGS** ([Pidtagruleuserflags (](pidtagruleuserflags-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
   
|**Zum Ändern einer SACL-Tabelle verwendete Eigenschaften**|**Access**|
|:-----|:-----|
|**PR_MEMBER_ENTRYID** ([Pidtagmemberentryid (](pidtagmemberentryid-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_MEMBER_ID** ([Pidtagmemberid (](pidtagmemberid-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_MEMBER_NAME** ([Pidtagmembername (](pidtagmembername-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_MEMBER_RIGHTS** ([Pidtagmemberrights (](pidtagmemberrights-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Rufen Sie zum Abrufen der **IExchangeModifyTable** -Schnittstelle die MAPI- [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode für eine Eigenschaft vom Typ PT_OBJECT für ein Folder-Objekt auf. Wenn Sie die **OpenProperty** -Methode aufrufen, übergeben Sie den Wert **IID_IExchangeModifyTable** im _lpIID_ -Parameter. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

