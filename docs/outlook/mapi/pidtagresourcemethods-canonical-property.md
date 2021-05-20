---
title: PidTagResourceMethods (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceMethods
api_type:
- COM
ms.assetid: 60ebbcd5-b758-4c96-b8ec-089e0aae1a5f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e9aee3280edbed60e97ef6e00e61f3086f6f07ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436335"
---
# <a name="pidtagresourcemethods-canonical-property"></a>PidTagResourceMethods (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske mit Flags, die die Methoden in der **IMAPIStatus-Schnittstelle** angeben, die vom Statusobjekt unterstützt werden. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RESOURCE_METHODS  <br/> |
|Kennung:  <br/> |0x3E02  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft gibt an, welche methoden in der Implementierung von **IMAPIStatus** eines Statusobjekts unterstützt werden. Statusobjekte können MAPI_E_NO_SUPPORT nicht unterstützten Methoden zurückgeben. 
  
Clients verwenden die eigenschaft PR_RESOURCE_METHODS **eines** Statusobjekts, um Aufrufe nicht unterstützter Methoden zu vermeiden. Wenn das Flag festgelegt ist, das einer bestimmten Methode entspricht, ist die Methode vorhanden und kann aufgerufen werden. Wenn dieses Flag eindeutig ist, sollte die Methode nicht aufgerufen werden. 
  
Die von MAPI implementierten Statusobjekte unterstützen die folgenden Methoden:
  
|**Status-Objekt**|**Unterstützte Methoden**|
|:-----|:-----|
|MAPI-Subsystem  <br/> |**Nur ValidateState**  <br/> |
|MAPI-Adressbuch  <br/> |**Nur ValidateState**  <br/> |
|MAPI-Spooler  <br/> |**ValidateState** und **FlushQueues** <br/> |
   
Mindestens eines der folgenden Flags kann in der folgenden **PR_RESOURCE_METHODS:**
  
STATUS_CHANGE_PASSWORD 
  
> Gibt an, dass die [IMAPIStatus::ChangePassword-Methode](imapistatus-changepassword.md) unterstützt wird. 
    
STATUS_FLUSH_QUEUES 
  
> Gibt an, dass die [IMAPIStatus::FlushQueues-Methode](imapistatus-flushqueues.md) unterstützt wird. 
    
STATUS_SETTINGS_DIALOG 
  
> Gibt an, dass die [IMAPIStatus::SettingsDialog-Methode](imapistatus-settingsdialog.md) unterstützt wird. 
    
STATUS_VALIDATE_STATE 
  
> Gibt an, dass die [IMAPIStatus::ValidateState-Methode](imapistatus-validatestate.md) unterstützt wird. 
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

