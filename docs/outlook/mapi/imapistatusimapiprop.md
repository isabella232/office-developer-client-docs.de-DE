---
title: IMAPIStatus IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIStatus
api_type:
- COM
ms.assetid: 17b2aa43-0267-45b6-8c57-11b7a5c67333
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a63b6cb77f4bcbd4919016630c09699ddf961f60
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584395"
---
# <a name="imapistatus--imapiprop"></a>IMAPIStatus : IMAPIProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt Statusinformationen zum MAPI-Subsystem, zum integrierten Adressbuch und zum MAPI-Spooler bereit. Ein Dienstanbieter implementiert **IMAPIStatus,** um Informationen über seinen eigenen Status zu liefern. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Statusobjekte  <br/> |
|Implementiert von:  <br/> |Dienstanbieter und MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIStatus  <br/> |
|Zeigertyp:  <br/> |LPMAPISTATUS  <br/> |
|Transaktionsmodell:  <br/> |Nicht übersetzt  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[ValidateState](imapistatus-validatestate.md) <br/> |Bestätigt die für die MAPI-Ressource oder den Dienstanbieter verfügbaren externen Statusinformationen.  <br/> |
|[SettingsDialog](imapistatus-settingsdialog.md) <br/> |Zeigt ein Eigenschaftenblatt an, mit dem der Benutzer die Konfiguration eines Dienstanbieters ändern kann.  <br/> |
|[ChangePassword](imapistatus-changepassword.md) <br/> |Ändert das Kennwort eines Dienstanbieters, ohne eine Benutzeroberfläche anzuzeigen.  <br/> |
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
   
## <a name="remarks"></a>HinwBemerkungeneise

Die von MAPI implementierten Statusobjekte unterstützen die folgenden Methoden:
  
|**Status-Objekt**|**Unterstützte Methoden**|
|:-----|:-----|
|MAPI-Subsystem  <br/> |**Nur ValidateState**  <br/> |
|MAPI-Adressbuch  <br/> |**Nur ValidateState**  <br/> |
|MAPI-Spooler  <br/> |**ValidateState** und **FlushQueues** <br/> |
   
Die von MAPI implementierten Statusobjekte müssen über eine schreibgeschützte Version der Methoden der [IMAPIProp-Schnittstelle](imapipropiunknown.md) verfügen und die **ValidateState-Methode** unterstützen. Transportanbieter sollten auch **FlushQueues** unterstützen. Alle Anbieter sollten **SettingsDialog** unterstützen; Die Unterstützung für **ChangePassword** ist optional. 
  
Clients verwenden Statusobjekte, um die Konfiguration durchzuführen und informationen zum Status der Sitzung zu erhalten. Sie greifen auf ein Statusobjekt zu, indem sie die **OpenStatusEntry-Methode** eines Dienstanbieter-Anmeldeobjekts oder die [IMAPISession::GetStatusTable-Methode](imapisession-getstatustable.md) aufrufen, um das Statusobjekt abzurufen. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

