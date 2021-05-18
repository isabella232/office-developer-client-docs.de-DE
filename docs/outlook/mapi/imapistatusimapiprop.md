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
ms.openlocfilehash: f90cf661c069ecd476bd02c5719147633a8392e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408299"
---
# <a name="imapistatus--imapiprop"></a>IMAPIStatus : IMAPIProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt Statusinformationen zum MAPI-Subsystem, zum integrierten Adressbuch und zum MAPI-Spooler zur Verfügung. Ein Dienstanbieter implementiert **IMAPIStatus,** um Informationen zu seinem eigenen Status zu liefern. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Statusobjekte  <br/> |
|Implementiert von:  <br/> |Dienstanbieter und MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIStatus  <br/> |
|Zeigertyp:  <br/> |LPMAPISTATUS  <br/> |
|Transaktionsmodell:  <br/> |Nichttransaktioniert  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[ValidateState](imapistatus-validatestate.md) <br/> |Bestätigt die externen Statusinformationen, die für die MAPI-Ressource oder den Dienstanbieter verfügbar sind.  <br/> |
|[SettingsDialog](imapistatus-settingsdialog.md) <br/> |Zeigt ein Eigenschaftenblatt an, mit dem der Benutzer die Konfiguration eines Dienstanbieters ändern kann.  <br/> |
|[ChangePassword](imapistatus-changepassword.md) <br/> |Ändert das Kennwort eines Dienstanbieters, ohne dass eine Benutzeroberfläche angezeigt wird.  <br/> |
|[FlushQueues](imapistatus-flushqueues.md) <br/> |Erzwingt, dass alle Nachrichten, die auf das Senden oder Empfangen warten, sofort hochgeladen oder heruntergeladen werden.  <br/> |
   
|**Erforderliche Eigenschaften**|**Access**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
|**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>Hinweise

Die von MAPI implementierten Statusobjekte unterstützen die folgenden Methoden:
  
|**Status-Objekt**|**Unterstützte Methoden**|
|:-----|:-----|
|MAPI-Subsystem  <br/> |**Nur ValidateState**  <br/> |
|MAPI-Adressbuch  <br/> |**Nur ValidateState**  <br/> |
|MAPI-Spooler  <br/> |**ValidateState** und **FlushQueues** <br/> |
   
Die von MAPI implementierten Statusobjekte müssen über eine schreibgeschützte Version der Methoden der [IMAPIProp-Schnittstelle](imapipropiunknown.md) verfügen und die **ValidateState-Methode** unterstützen. Transportanbieter sollten auch **FlushQueues unterstützen.** Alle Anbieter sollten **SettingsDialog unterstützen;** Die Unterstützung **für ChangePassword** ist optional. 
  
Clients verwenden Statusobjekte, um die Konfiguration durchzuführen und mehr über den Status der Sitzung zu erfahren. Sie greifen auf ein Statusobjekt zu, indem sie die **OpenStatusEntry-Methode** eines Anmeldeobjekts eines Dienstanbieters oder die [IMAPISession::GetStatusTable-Methode](imapisession-getstatustable.md) aufrufen, um das Statusobjekt abzurufen. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

