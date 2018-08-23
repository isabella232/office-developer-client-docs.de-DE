---
title: IMAPIStatus IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus
api_type:
- COM
ms.assetid: 17b2aa43-0267-45b6-8c57-11b7a5c67333
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 23663cea49c50f3f584d6b06e331545320e8283b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565382"
---
# <a name="imapistatus--imapiprop"></a>IMAPIStatus : IMAPIProp

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält Statusinformationen zu MAPI-Subsystems, integrierte des Adressbuchs und die MAPI-Warteschlange. Ein Dienstanbieter implementiert **IMAPIStatus** , um Informationen über einen eigenen Status bereitzustellen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verfügbar gemacht von:  <br/> |Status-Objekte  <br/> |
|Implementiert von:  <br/> |Dienstanbieter und MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIStatus  <br/> |
|Zeigertyp:  <br/> |LPMAPISTATUS  <br/> |
|Transaktionsmodell:  <br/> |Nontransacted  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[ValidateState](imapistatus-validatestate.md) <br/> |Bestätigen Sie die externen Statusinformationen für die MAPI-Ressource oder den Dienstanbieter.  <br/> |
|[SettingsDialog](imapistatus-settingsdialog.md) <br/> |Zeigt ein Eigenschaftenfenster, mit dem den Benutzer einem Dienstanbieter Konfiguration ändern kann.  <br/> |
|[ChangePassword](imapistatus-changepassword.md) <br/> |Ändert das Kennwort des Dienstanbieters ohne eine Benutzeroberfläche anzuzeigen.  <br/> |
|[FlushQueues](imapistatus-flushqueues.md) <br/> |Erzwingt, dass alle Nachrichten gesendet oder empfangen, um sofort hoch- oder heruntergeladen werden.  <br/> |
   
|**Erforderliche Eigenschaften**|**Access**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lese-/Schreibzugriff  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |Lese-/Schreibzugriff  <br/> |
|**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Status, die von MAPI implementierte Objekte unterstützen die folgenden Methoden:
  
|**Statusobjekt**|**Unterstützte Methoden**|
|:-----|:-----|
|MAPI-Subsystems  <br/> |Nur **ValidateState**  <br/> |
|MAPI-Adressbuch  <br/> |Nur **ValidateState**  <br/> |
|MAPI-Warteschlange  <br/> |**ValidateState** und **FlushQueues** <br/> |
   
Der Status, die von MAPI implementierte Objekte sind erforderlich, um eine schreibgeschützte Version der Methoden der Schnittstelle [IMAPIProp](imapipropiunknown.md) haben und die **ValidateState** -Methode unterstützen. Transportanbieter sollten auch **FlushQueues**unterstützen. Alle Anbieter sollte **SettingsDialog**unterstützen. Unterstützung für **ChangePassword** optional ist. 
  
Clients verwenden Status Objekte zum Ausführen der Konfiguration und zum Status der Sitzung zu erfahren. Sie haben ein Statusobjekt durch Aufrufen der **OpenStatusEntry** -Methode eines Service Provider Anmeldung-Objekts oder die [IMAPISession::GetStatusTable](imapisession-getstatustable.md) -Methode zum Abrufen des Status-Objekts zugreifen. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

