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
ms.openlocfilehash: f90cf661c069ecd476bd02c5719147633a8392e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331528"
---
# <a name="imapistatus--imapiprop"></a>IMAPIStatus : IMAPIProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt Statusinformationen zum MAPI-Subsystem, dem integrierten Adressbuch und dem MAPI-Spooler bereit. Ein Dienstanbieter implementiert **IMAPIStatus** , um Informationen über seinen eigenen Status bereitzustellen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Verf�gbar gemacht von:  <br/> |Statusobjekte  <br/> |
|Implementiert von:  <br/> |Dienstanbieter und MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIStatus  <br/> |
|Zeigertyp:  <br/> |LPMAPISTATUS  <br/> |
|Transaktionsmodell:  <br/> |Nicht durchgeführten  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[ValidateState](imapistatus-validatestate.md) <br/> |Bestätigt die externen Statusinformationen für die MAPI-Ressource oder den Dienstanbieter.  <br/> |
|[SettingsDialog](imapistatus-settingsdialog.md) <br/> |Zeigt ein Eigenschaftenfenster an, in dem der Benutzer die Konfiguration eines Dienstanbieters ändern kann.  <br/> |
|[ChangePassword](imapistatus-changepassword.md) <br/> |Ändert das Kennwort eines Dienstanbieters, ohne eine Benutzeroberfläche anzuzeigen.  <br/> |
|[FlushQueues](imapistatus-flushqueues.md) <br/> |ErZwingt, dass alle Nachrichten, die darauf warten, gesendet oder empfangen werden, sofort hochgeladen oder heruntergeladen werden.  <br/> |
   
|**Erforderliche Eigenschaften**|**Access**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
|**PR_PROVIDER_DISPLAY** ([Pidtagproviderdisplay (](pidtagproviderdisplay-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
|**PR_PROVIDER_DLL_NAME** ([Pidtagproviderdllname (](pidtagproviderdllname-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RESOURCE_FLAGS** ([Pidtagresourceflags (](pidtagresourceflags-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RESOURCE_METHODS** ([Pidtagresourcemethods (](pidtagresourcemethods-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RESOURCE_TYPE** ([Pidtagresourcetype (](pidtagresourcetype-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_STATUS_CODE** ([Pidtagstatuscode (](pidtagstatuscode-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die von MAPI implementierten Statusobjekte unterstützen die folgenden Methoden:
  
|**Status-Objekt**|**Unterstützte Methoden**|
|:-----|:-----|
|MAPI-Subsystem  <br/> |Nur **ValidateState**  <br/> |
|MAPI-Adressbuch  <br/> |Nur **ValidateState**  <br/> |
|MAPI-Spooler  <br/> |**ValidateState** und **FlushQueues** <br/> |
   
Die von MAPI implementierten Statusobjekte sind erforderlich, um eine schreibgeschützte Version der Methoden der [IMAPIProp](imapipropiunknown.md) -Schnittstelle und die **ValidateState** -Methode zu unterstützen. Transport Anbieter sollten auch **FlushQueues**unterstützen. Alle Anbieter sollten **Settingsdialog**unterstützen; die Unterstützung für **ChangePassword** ist optional. 
  
Clients verwenden Statusobjekte, um die Konfiguration auszuführen und um den Status der Sitzung zu erfahren. Sie greifen auf ein Status-Objekt zu, indem Sie die **OpenStatusEntry** -Methode eines Dienstanbieter-Anmelde Objekts oder die [IMAPISession::](imapisession-getstatustable.md) getstatusable-Methode aufrufen, um das Status-Objekt abzurufen. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

