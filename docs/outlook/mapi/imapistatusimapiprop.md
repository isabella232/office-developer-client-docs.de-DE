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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e36a987174ffb2abb4c0f5fc95bf695f31af942e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792342"
---
# <a name="imapistatus--imapiprop"></a>IMAPIStatus: IMAPIProp

  
  
**Betrifft**: Outlook 
  
Enthält Statusinformationen zu MAPI-Subsystems, integrierte des Adressbuchs und die MAPI-Warteschlange. Ein Dienstanbieter implementiert **IMAPIStatus** , um Informationen über einen eigenen Status bereitzustellen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Status-Objekte  <br/> |
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
   
|**Erforderliche Eigenschaften**|**Zugriff**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lese-/Schreibzugriff  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |Lese-/Schreibzugriff  <br/> |
|**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
   
## <a name="remarks"></a>Hinweise

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

